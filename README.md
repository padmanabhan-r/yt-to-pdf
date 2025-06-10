# YouTube to PDF Converter

A Python utility to convert YouTube videos into PDF documents by extracting frames and compiling them into a single PDF file.

## Features

- Extract frames from YouTube videos at specified intervals
- Convert extracted frames into a single PDF document
- Customizable frame extraction rate
- Support for various video formats via yt-dlp
- Image processing capabilities using OpenCV and scikit-image

## Prerequisites

- Python 3.13 or higher
- pip (Python package manager)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/yt-to-pdf.git
   cd yt-to-pdf
   ```

2. Install the required dependencies:
   ```bash
   pip install -e .
   ```

## Usage

```bash
python -m yt_to_pdf.main [YOUTUBE_URL] [OPTIONS]
```

### Options
- `--output, -o`: Output PDF filename (default: output.pdf)
- `--interval, -i`: Interval in seconds between frames (default: 5)
- `--quality, -q`: Image quality (1-100, default: 90)

### Example

```bash
python -m yt_to_pdf.main https://www.youtube.com/watch?v=example --output presentation.pdf --interval 10
```

## Configuration

You can configure the application by creating a `config.ini` file in the project root with the following options:

```ini
[yt_to_pdf]
output_dir = ./output
default_interval = 5
image_quality = 90
```

## Development

### Setting up the development environment

1. Clone the repository
2. Install development dependencies:
   ```bash
   pip install -e ".[dev]"
   ```

### Running tests

```bash
pytest
```

## Dependencies

- [yt-dlp](https://github.com/yt-dlp/yt-dlp) - YouTube video downloader
- [OpenCV](https://opencv.org/) - Computer vision and image processing
- [Pillow](https://python-pillow.org/) - Image processing
- [scikit-image](https://scikit-image.org/) - Image processing

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- Thanks to all the open-source projects that made this tool possible
- Special thanks to the maintainers of yt-dlp for their excellent work
