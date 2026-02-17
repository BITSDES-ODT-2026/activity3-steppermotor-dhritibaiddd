[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/EzXNyUnO)
# Week-7-Section-C-Activity3
Activity 3 : Code for Stepper Motor running clockwise and anti-clock wise .. continuously 
from machine import Pin
import time

IN1 = Pin(13,Pin.OUT)
IN2 = Pin(12,Pin.OUT)
IN3 = Pin(14,Pin.OUT)
IN4 = Pin(27,Pin.OUT)

dire = [[1,0,0,0],[0,1,0,0],[0,0,1,0],[0,0,0,1]]
cw = [[0,0,0,1],[0,0,1,0],[0,1,0,0],[1,0,0,0]]


for k in range(500):
    for i in dire:
            IN1.value(i[0])
            IN2.value(i[1])
            IN3.value(i[2])
            IN4.value(i[3])
            time.sleep_ms(5)
            
for x in range(500):
    for s in cw:
            IN1.value(s[0])
            IN2.value(s[1])
            IN3.value(s[2])
            IN4.value(s[3])
            time.sleep_ms(5)
