# Getting Started with Tesseract and Pytesseract
Getting Started with Tesseract and Pytesseract is meant to demonstrate how to install Tesseract 3.0 on Windows 10 OS and how to start leveraging Tesseract with Pytesseract. It is important to note that Pytesseract is only compatible with Tesseract = 3.0.

If your intent is to use a more recent version of Tesseract you will have to explore Tesserocr. However, I find that the results from Tesseract 3.0 and Pytesseract is better than Tesserocr.

Lastly, results may vary. This demo levarages the most basic functions of Tesseract and in some cases you will need to learn more beyond this demo to convert handwriting in images to text.

## Prerequisites

Before you begin, ensure you have met the following requirements:
* You have installed Python = 3.7 [Python](https://www.python.org/downloads/)
* Install python module 
* You have a `<Windows>` machine that is running Windows 10 OS.
* You have a handwritten image that you want to turn to text. If you don't, you can use mine ![Hello World!](sample_text.png)
* You have subscribed and dropped a like on my channel for this demo [Youtube Demos](https://youtube.com/channel/UCUpa2BIFlC2CpB9YsuwdjYw).

## Installing Tesseract 3.0

To install Tesseract, follow these steps:

Head on over to Tesseract's available [Windows installers](https://digi.bib.uni-mannheim.de/tesseract/)
Grab tesseract-ocr-setup-3.05.02-20180621.exe and follow the executable prompts

Add a TESSDATA_PREFIX to your system environment variables. Set its value to the location of your tessdata directory (my tessdata path is shown below)
```
TESSDATA_PREFIX = C:\Program Files (x86)\Tesseract-OCR\tessdata
```

## Installing Pytesseract

To install Pytesseract follow these steps:

Using any Windows shell, execute the following
```
pip install pytesseract
```

Validate your installation by successfully importing the module with Python
```
python
import pytesseract
```


## Other Installations

Lastly, you will need Image module later on in this guide. Install it with the following command
```
pip install Image
```

## OPTIONAL Installing Tesserocr

To install Tesserocr follow these steps:

Head on over to Tesserocr's Python [wheel files](https://github.com/simonflueckiger/tesserocr-windows_build/releases)
Grab the Windows 32 bit or 64 bit Python 3.7 wheel file (in my case I chose the 64 bit wheel file)
Using any Windows shell, navigate to downloads and execute 
```
pip install tesserocr-2.4.0-cp37-cp37m-win_amd64.whl
```

Test if the install worked by successfully importing the tesserocr module with Python
```
python
import tesserocr
```

## Extracting Text from an Image

To extract the text in an image follow these steps:
Using any Windows shell, navigate to the location of your sample image

Run the command
```
python
```

Import tesseract
```
import pytesseract
```

Set the path to Tesseract executable needed for Pytesseract to work correctly (the path below is my path to the tesseract.exe yours may vary)
```
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files (x86)\Tesseract-OCR\tesseract.exe'

```

Finally show me the text in the image
```
print(pytesseract.image_to_string(Image.open('sample_text.png')))
```

## Supplemental Instructions

If you would like to view the sources for this guide, see the following links:

* [Tesseract's official install documentation](https://tesseract-ocr.github.io/tessdoc/Home.html) 📖
* [More tools and wrappers for Tesseract](https://tesseract-ocr.github.io/tessdoc/AddOns.html#tesseract-wrappers) 🐛
* [Pytesseract's official documentation](https://pypi.org/project/pytesseract/) 📖
