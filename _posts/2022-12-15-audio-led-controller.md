---
layout: post
title: Sound controlled LED's 
subtitle: Theme lighting using LED Strip , LED light frequency emitted equal to max frequency of sound in a given chunk.
cover-img: /assets/img/total.jpg
thumbnail-img: /assets/img/proj1.jpeg
share-img: /assets/img/path.jpg
tags: [books, test]
---

I have used [pyaudio][1] library for getting Audio input from surroundings and after reading data , I have computed Amplitude of audio chunk continuosly and for computing frequency spectrum of given audio chunk we use Fast Fourier Tranform from [scipy_fftpack][2] and this data is used to get Max frequency of given data chunk, we send this data through [serial][3] library in python to our arduino UNO board and IDE at this junction we give values of RGB based on there light frequencies,after this we design a circuit as shown below and get required light frequency output with certain frequency audio as input.
please do checkout code for further info in my repositories.

[1]:https://pypi.org/project/PyAudio/  "pyaudio"
[2]:https://docs.scipy.org/doc/scipy/reference/generated/scipy.fftpack.fft.html  "scipy_fftpack"
[3]:https://pyserial.readthedocs.io/en/latest/pyserial.html "serial"
