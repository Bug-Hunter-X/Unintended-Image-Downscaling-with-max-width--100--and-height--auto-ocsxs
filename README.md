# Unintended Image Downscaling in CSS

This repository demonstrates a subtle CSS bug related to responsive image scaling.  The issue occurs when using `max-width: 100%;` and `height: auto;` on an image, causing it to become unexpectedly smaller than its container, particularly when aspect ratios differ.

The `bug.css` file contains the problematic CSS code, while `bugSolution.css` offers a solution.

## Problem
The `height: auto;` property, combined with `max-width: 100%;`, can cause the image to shrink to maintain its aspect ratio.  If the container is wider than what the image's aspect ratio allows, then the image will remain smaller than the container.

## Solution
The solution involves using `width: 100%;` and maintaining aspect ratio using padding-top in percentage.