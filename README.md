# Image Editor

A command-line image editor written in C.  
The program loads an image, applies a sequence of operations, and writes the result to an output file or standard output.

---

## Features

- Supports PPM and BMP image formats
- Reads from file or standard input
- Writes to file or standard output
- Operations are applied in the order given
- Supported operations:
  - Horizontal flip
  - Vertical flip
  - Crop
  - Filters (with optional parameters)

---

## Compilation

Compile the project using the provided Makefile:

```bash
make
```

## Usage

```bash
./image_editor [arguments]
```

## Arguments

- **`-input <file>`**  
  Input image file (.ppm or .bmp).  
  If omitted, the program reads from standard input.

- **`-output <file>`**  
  Output image file (.ppm or .bmp).  
  If omitted, the program writes to standard output.

- **`-horizontal`**  
  Apply a horizontal mirror to the image.

- **`-vertical`**  
  Apply a vertical mirror to the image.

- **`-crop WxH+X+Y`**  
  Crop the image to width W and height H, starting at position (X, Y).

- **`-filter <name> [param]`**  
  Apply a filter. Some filters require an additional parameter.

## Filters

- **`invertir`**  
  Invert the colors of the image.

- **`saturar <value>`**  
  Increase or decrease saturation by percentage.  
  Example: `saturar 30` or `saturar -20`

- **`gama <value>`**  
  Shift the hue by degrees.  
  Example: `gama 45`

- **`brillo <value>`**  
  Increase or decrease brightness by percentage.  
  Example: `brillo 10`

- **`contraste <value>`**  
  Increase or decrease contrast by percentage.  
  Example: `contraste -15`

- **`mezclar <color>`**  
  Mix the image with a color.  
  Example: `mezclar red` or `mezclar #ff00ff`

- **`sepia`**  
  Apply a sepia tone.

- **`monocromo <value>`**  
  Convert to black & white using a threshold percentage.  
  Example: `monocromo 50`

- **`toaster`**  
  Apply a “toaster” effect.

- **`valencia`**  
  Apply a “valencia” effect.
