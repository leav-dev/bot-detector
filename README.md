# bot-detector

Bot de automatización GUI basado en detección de imágenes con Python y OpenCV.

Toma capturas de plantillas (`data/`) y busca coincidencias en pantalla usando `pyautogui` con `confidence=0.8`. Al encontrar una coincidencia, mueve el mouse al centro y hace clic.

> **Disclaimer**: Este proyecto fue creado con fines educativos. Úsalo bajo tu propia responsabilidad.

## Requisitos

- Python 3.8+
- OpenCV (`cv2`)
- PyAutoGUI
- PyGetWindow

## Instalación

```bash
pip install opencv-python pyautogui pygetwindow
```

## Uso

```bash
cd src/
python main.py
```

El bot procesa las imágenes en `data/misiones/` y `data/objetos/`, buscando cada una en pantalla y haciendo clic cuando encuentra una coincidencia.

## Estructura

```
├── data/
│   ├── metas/       → Imágenes de objetivo (completado)
│   ├── misiones/    → Plantillas de misiones (d1.png .. d3.png)
│   └── objetos/     → Plantillas de objetos (b1.png .. b15.png)
└── src/
    ├── main.py                         → Punto de entrada
    ├── folder_processor/folder.py      → Lista imágenes de un directorio
    ├── images_processor/images.py      → Búsqueda en pantalla + clics
    └── windows_processor/windows.py    → Detección de ventanas
```

## Licencia

MIT — ver [LICENSE](./LICENSE).
