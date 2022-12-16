---
layout: post
title: Sound controlled LED's 
subtitle: Theme lighting using LED Strip , LED light frequency emitted equal to max frequency of sound in a given chunk.
cover-img: /assets/img/total.jpg
thumbnail-img: /assets/img/proj1.jpeg
share-img: /assets/img/path.jpg
tags: [books, test]
---

I have used Open-Cv for Image processing in python in the code I took screenshot of laptop screen at each instant of time by using pyautogui library and while loop and further processed image , firstly i read image using open cv  and then computed average values of all the pixels across the screen for RGB colors then after computation i have sent this data using serial communication to Arduino board and thus this data is analogly written at each three pins of Arduino UNO this signal is futher amplified for whole LED strip using three Mosfets , Thus in conclusion we get dominant color displayed on laptop screen on LED's.
