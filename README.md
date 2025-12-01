# olEDitor

A simple web-based editor for creating and laying out monochrome graphics for small OLED screens, aimed at Arduino or other microcontroller projects.

This editor is hosted publicly at: **[https://ediamondscience.github.io/olEDitor/](https://ediamondscience.github.io/olEDitor/)**

You can use the editor directly from the link above, or by downloading the `index.html` file from this repository and opening it in your browser.

## Features

*   **Virtual Screen:** Configure the dimensions (width, height) and pixel scale of your target display.
*   **Templates:** Define reusable graphic templates with fixed dimensions (e.g., 'icon', 'button').
*   **Pixel Editor:** For each template, create multiple named "canvases" and draw your graphics pixel-by-pixel.
*   **Layout Regions:** Place your templates onto the main screen as named "regions". You can position and move these regions precisely.
*   **Live Preview:** Toggle the preview of any canvas on its corresponding region to see how it looks in your layout.
*   **Export to C:**
    *   Export individual canvases as C header files (`.h`).
    *   Export the entire project (all canvases from all templates) as a single `.h` file, ready to be included in your microcontroller project.
*   **Save/Load Project:** Save your entire project layout (templates, regions, and pixel data) to a JSON file to continue your work later.

## How to Use

1.  **Open the editor:** Either visit the link above or open the local `index.html` file in your web browser.
2.  **Configure Screen:** Set the `Screen W` (width), `Screen H` (height), and `Scale` for your display.
3.  **Create Templates:**
    *   In the **Templates** section, give a template a name (e.g., "icon\_16x16"), set its width and height, and click "Add".
    *   You can create multiple templates for different graphic sizes.
4.  **Place Regions:**
    *   Click on a template in the list to select it (it will be highlighted).
    *   Click on the black screen area. A new "region" using that template's dimensions will be placed on the screen. The point you click will be used as the **top-left corner** of the new region.
5.  **Edit Graphics:**
    *   In the **Regions** list, find the region you want to edit and click its "Edit" button. This opens the **Editor** panel for that region's template.
    *   In the **Editor** panel, enter a name for a new canvas and click "Create Canvas".
    *   Click the "Open" button next to the canvas name. A pixel editor will appear.
    *   Click on the pixels in the editor grid to draw your graphic (1-bit, on/off).
6.  **Preview Graphics:**
    *   In the **Regions** list, select a canvas from the dropdown menu next to the "Preview" button.
    *   Click the "Preview" button to toggle the display of that canvas on the screen.
7.  **Export Code:**
    *   **Single Canvas:** In the **Editor**, open the canvas you want and click "Export Canvas". This will download a `.h` file.
    *   **All Canvases:** Click the "Export .h (all regions/canvases)" button at the top to download a single `.h` file containing all your graphical assets.
8.  **Save & Load:**
    *   Click "Save JSON" to download a project file.
    *   Click "Load JSON" and select a previously saved project file to load it back into the editor.

## File Structure

*   `index.html`: The all-in-one HTML file containing the application's logic, styling, and structure.
*   `README.md`: This file.
*   `LICENSE`: The project's license.