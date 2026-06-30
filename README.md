# bot-detector

GUI automation bot using image detection with Python and OpenCV.

Takes template images from `data/` and searches for them on screen using `pyautogui` with `confidence=0.8`. When a match is found, moves the cursor to the center and clicks.

> **Disclaimer**: This project was created for educational purposes. Use it at your own risk.

## Requirements

- Python 3.8+
- OpenCV (`cv2`)
- PyAutoGUI
- PyGetWindow

## Installation

```bash
pip install opencv-python pyautogui pygetwindow
```

## Usage

```bash
cd src/
python main.py
```

The bot processes images from `data/misiones/` and `data/objetos/`, searching for each on screen and clicking when a match is found.

### How it works

1. **`folder_processor`** — Lists all images in a given data directory.
2. **`images_processor`** — Searches the screen for each image using template matching (`confidence=0.8`). On a match, moves the mouse to the center and clicks.
3. **`windows_processor`** — (optional) Detects application windows by title for targeted searching.

## Structure

```
├── data/
│   ├── metas/       → Objective images (completed state)
│   ├── misiones/    → Mission templates (d1.png .. d3.png)
│   └── objetos/     → Object templates (b1.png .. b15.png)
└── src/
    ├── main.py                         → Entry point
    ├── folder_processor/folder.py      → List images in a directory
    ├── images_processor/images.py      → Screen search + clicking
    └── windows_processor/windows.py    → Window detection
```

## License

MIT — see [LICENSE](./LICENSE).
