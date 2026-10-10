# Object Detectify

A desktop app that finds and counts the objects in an image, built with OpenCV and Tkinter.

> College mini-project · Computer Science and Engineering, SRMIST · Digital Image Processing · March 2024

## Features

- Pick an image from your computer
- See the original next to a copy with every detected object outlined in green
- Get the number of objects found

## Built with

Python 3, OpenCV, Pillow and Tkinter.

## Run it

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python main.py
```

Click **Select Image** and choose a picture. Two samples are in `images/`: `objects2.png` gives 12 objects and `objects3.jpg` gives 9.

## How it works

1. Convert the image to grayscale.
2. Blur it with an 11×11 Gaussian kernel to remove noise.
3. Find edges with the Canny detector (thresholds 30 and 100).
4. Find the outer contours of those edges; each contour is one object.
5. Draw the contours on the image and show their count.

## Project structure

```
main.py            Tkinter window and the detection steps
images/            sample images to try
requirements.txt   OpenCV and Pillow
```

## License

[MIT](LICENSE)
