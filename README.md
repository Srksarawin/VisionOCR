# VisionOCR 

The `VisionOCR` is an **OCR** (Optical Character Recognition) tool that detects text in an image, extracts it, and stores it as a separate text file.

## Tools

- Python 
- OpenCV 
- PyTesseract 
- Jupyter Notebook 

## Project Overview

In this project, I use two concepts **OpenCV** and **Pytesseract**, for *Image processing* and *Text Detection and Extraction*.

`opencv`:
- Image Processing
- To capture the image and read it

 `pytesseract`
 - To perform OCR operations.
 - Extract the text from the Image.

## Concepts 

In this one, what concepts I use to get the text from the image.

- When I read the image using `img=cv2.imread()`, the `img` variable stores the contents of the image in **Numpy Array** because the image contains the pixel data.
- Then I convert the image into **Grayscale** image
   - `Grayscale` is an image format which contains the shades of gray.
   - Each pixel carries the intensity information, ranging from black (0) to white (255)
      - Why I use this?
         - When I use **grayscale** in image, it is easier to focus on shapes and contrast (difference between text and background) 

## Workflow
![Flow](images/workflow.png)

## License

This project is licensed under the [MIT License](LICENSE).  
Feel free to use, modify, and share with credit to **Sarawin R.**

