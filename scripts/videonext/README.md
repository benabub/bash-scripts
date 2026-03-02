# videonext

Sequentially renames MP4 files to `0.mp4`, creating a simple queue system for video processing.

## Overview

This script manages a queue of MP4 files by repeatedly renaming the next available file to `0.mp4`. Each time the script runs, it removes the current `0.mp4` and promotes the next file (in alphabetical order, excluding `1.mp4` through `9.mp4`) to become the new `0.mp4`.

- **Purpose:** Ideal for scenarios where you need to process videos one by one, always working with a file named `0.mp4`
- **File types:** Works with any `.mp4` files in the current directory
- **Reserved names:** Files named `1.mp4` through `9.mp4` are preserved and won't be renamed to `0.mp4`

## Advantages

- **Simple queue management:** Automatically handles file rotation without manual renaming
- **Idempotent:** Safely handles cases with no MP4 files or missing `0.mp4`
- **Lightweight:** Pure bash script with no external dependencies
- **Smart skipping:** Preserves single-digit numbered files (1-9) that might be used for other purposes

## Installation

See [Installation instructions](../../README.md) in the main repository README.

## Usage

```bash
videonext
