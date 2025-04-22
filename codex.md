# Explanation of Code (line by line)

`!pip install opencv-python` 
- `!` :
    - tells the notebook to run the following command.
    -  It is used when you use **Jupyter Notebook** or **Google Colab** (Code Cells)

- `pip` :
    -  It is **Python Package Manager**
    -  It is used to install **Packages** and **Libraries** from ***Python Package Index*** `PyPI`
    - The full form of `pip` is `Pip Installs Packages`
    - `pip` will find the package from *PyPI* repository install and download it to the environment.

- `opencv-python` :
    - name of the package (Opencv).
    - `Opencv` packages are widely in ***Computer Vision*** tasks such as **Image Processing** and **Video Processing**.
#

   `!pip install pytesseract`
  
- `pytesseract` :
    - wrapper (interface) for **Google's Tesseract OCR Engine**.
    - allows you to use Tesseract-OCR (which reads text from images)

 #

 `import cv2`
- loads the library in your current python script.

`import pytesseract`
- loads the pytesseract library. 

#

`pytesseract.pytesseract.tesseract_cmd=r'C:\Program Files\Tesseract-OCR\tesseract.exe'`
 - tells the system **where the Tesseract file is**, so that we can do OCR applications.
 - some systems know where the tesseract file is, but most of the systems don't know where that file is, so that's why we are including this code.
 - You have to install the Tesseract to do the OCR applications.

#

`img=cv2.imread('Sample.jpg')`
- reading the image and store it into a variable (img)
- it is stored as **Numpy array** (image contains pixels)

#

`gray=cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)`
- converting the image to **Grayscale**
- grayscale converts an image to shades of gray removing color information.

 #

 `ret, thresh1=cv2.threshold(gray,0,255, cv2.THRESH_OTSU | cv2.THRESH_BINARY_INV)`
 - Here we do thresholding - converts an image into black & white image where all pixel values either 0 (black) or 255 (white) based on threshold value.
 - goal:
     - create image where text stands out sharply from background.
       
`cv2.THRESH_OTSU`
- automatic method to determind the optimal threshold.
- calculates the best threshold based on pixel distribution.

`cv2.THRESH_BINARY_INV`
- inverts the thresholded image.

- `THRESH_BINARY`
     - Background - White (255)
     - Text       - Black (0)

- `THRESH_BINARY_INV`
    - Background - Black (0)
    - Text       - White (255)
 
- `ret`
    -stores the threshold value (mostly ignored when using `THRESH_OTSU` )

- `thresh1`
    -binary image that has been thresholded (black & white)

#

`rect_kernel=cv2.getStructuringElement(cv2.MORPH_RECT, (18,18))`
- creates a structuring element for morphological operations (image processing = (dilation or erosion))
       
  
