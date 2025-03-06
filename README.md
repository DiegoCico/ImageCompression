# Image Seam Carving Project

## Overview
This project is an implementation of image seam carving, a content-aware image resizing technique. It allows users to remove seams (columns of pixels) based on either the bluest column or the lowest-energy seam. The project is structured using Java and utilizes linked lists to manage pixel data for efficient seam removal.

## Features
- **Load and Process Images**: Convert an image into a graph-based representation of pixels.
- **Highlight Seams**: Identify and highlight seams based on energy or color intensity.
- **Seam Removal**: Remove a selected seam from the image and adjust pixel links accordingly.
- **Undo Functionality**: Restore the image to a previous state before the last seam removal.
- **Export Edited Images**: Save the modified image after edits.
- **Command Line Interface**: Provides a menu-driven UI for user interaction.

## Usage
Upon running the application, the user is prompted to enter the file path of an image. The following operations are available:
- `b` - Remove the bluest column
- `r` - Remove a random column
- `u` - Undo the previous edit
- `q` - Quit the application

After selecting an operation, users can confirm or cancel the edit before it is applied. The final image is saved after exiting the program.

## Classes and Their Roles
### `Pixel`
Represents a pixel in the image with RGB values, references to neighboring pixels, and an energy value for seam carving calculations.

### `ImageMain`
The main entry point that handles user interaction and executes commands based on menu selections.

### `ImageEdit`
Manages seam carving operations, including identifying and deleting seams and handling the undo functionality.

### `ImageData`
Handles image processing, including importing an image into pixel data, calculating energy levels, and exporting the modified image.

## How It Works
1. The image is imported and converted into a linked structure of pixels.
2. The user selects a seam removal method (bluest or lowest-energy seam).
3. The system identifies and highlights the seam.
4. Upon confirmation, the seam is removed, and the image structure is updated.
5. Users can undo the removal if necessary.
6. The modified image is saved upon quitting.

## Dependencies
- **Apache Commons Lang3** (for Pair data structure)
- **Java Standard Library** (for I/O operations, data structures, and image processing)

## Limitations and Future Improvements
- **Performance Optimization**: Processing larger images can be optimized for better efficiency.
- **GUI Implementation**: A graphical interface can improve user experience.
- **Multi-Seam Removal**: Allow multiple seams to be removed in a single operation.

This project provides an efficient approach to image resizing while preserving important visual content. It serves as a foundation for further development in content-aware image manipulation.
