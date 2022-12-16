---
layout: post
title: Background lighting
subtitle: Theme lighting using LED Strip based on dominant color on laptop screen using python and Arduino.
cover-img: /assets/img/total.jpg
thumbnail-img: /assets/img/proj1.jpeg
share-img: /assets/img/path.jpg
tags: [books, test]
---

I have used Open-Cv for Image processing in python in the code I took screenshot of laptop screen at each instant of time by using pyautogui library and while loop and further processed image , firstly i read image using open cv  and then computed average values of all the pixels across the screen for RGB colors then after computation i have sent this data using serial communication to Arduino board and thus this data is analogly written at each three pins of Arduino UNO this signal is futher amplified for whole LED strip using three Mosfets , Thus in conclusion we get dominant color displayed on laptop screen on LED's.
