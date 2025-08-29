# Mandelbrot Set Renderer

This Rust program generates grayscale images of the Mandelbrot set and saves them as PNG files. It uses multi-threading for efficient rendering and supports custom image dimensions and complex plane coordinates.

## Features
- Renders Mandelbrot set images in PNG format
- Multi-threaded rendering for performance
- Customizable image size and complex plane region
- Simple command-line interface

## Usage

```sh
./mandelbrot FILE PIXELS LEFT,TOP RIGHT,BOTTOM
```

- `FILE`: Output PNG filename (e.g., `mandel.png`)
- `PIXELS`: Image dimensions in the format `WIDTHxHEIGHT` (e.g., `1000x750`)
- `LEFT,TOP`: Upper-left complex coordinate (e.g., `-1.20,0.35`)
- `RIGHT,BOTTOM`: Lower-right complex coordinate (e.g., `-1,0.20`)

### Example

```sh
./mandelbrot mandel.png 1000x750 -1.20,0.35 -1,0.20
```

This command generates a 1000x750 PNG image of the Mandelbrot set covering the specified region of the complex plane.

## Building

Make sure you have [Rust](https://www.rust-lang.org/tools/install) installed.

```sh
cargo build --release
```

The executable will be located at `target/release/mandelbrot`.

## Running

After building, run the program as shown in the usage section. The output image will be saved to the specified file.

## Showcase

Below is a sample output generated:

![Sample Mandelbrot Output](mandel.png)

## Dependencies
- [num](https://crates.io/crates/num): Complex number support
- [image](https://crates.io/crates/image): PNG encoding

## License

This project is licensed under the GNU GPL v3 License. See `LICENSE` for details.
