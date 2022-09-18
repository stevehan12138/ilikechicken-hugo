---
title: "How to freely and accurately OCR PDFs"
draft: false
---

Many times when someone sends you a pdf of a scanned or a picture of a document, you can't copy texts off of the pdf, nor searching for keywords. It becomes very frustrating to process the document. Here is something I found that can easily make computers process the work.


I searched many "free online OCR scanners", but they don't seem to work very well. After some research, I found: ocrmypdf.


Installing is pretty easy, a bit complicated for Windows though, but they are all just copy-pasting so no big deal. After installing, you should be able to use it directly through the command line. It adds a text layer to the original pdf, or you can choose to output in a .txt file, but it might have some punctuations and spacing problems that you need to fix manually.


It's quite accurate, no mistakes found on a printed textbook pdf, might different if your's is handwritten, fancy font or poorly scanned. Also because it has a command-line interface, implement it in your code should be no hassle at all, since it is a python module. I guess you can dig into the libraries it used and get some similar results, but I'm fine with Python.


In conclusion, it's definitely something to try if your boss/teacher sends you millions of scanned docs every day, a bit of coding experience required, but to be honest, it's just copy-pasting, you should have it figured out within an hour.