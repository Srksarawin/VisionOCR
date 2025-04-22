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
    
  
