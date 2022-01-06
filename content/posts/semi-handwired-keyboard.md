---
title: "Semi-Handwired Keyboard"
date: 2022-01-05T19:07:34-05:00
draft: true
categories: ["technology","hardware"]
tags: ["keyboard","electronics"]
---

## The Inspiration
I have come across a fun PCB design by [TweetyDaBird][tweety], which is a 1u by 5.25u macro row pad, with 4 switches, a rotary encoder with click, and even provides hotswap socket and RGB lighting.

This lovely PCB, named the [DaPad4D][pcb], seems to be easily stackable, and with the diodes already being mounted on the PCB manufacturer and assembler, there *should* just be the matter of wiring the provided pins such that the switches merge into columns, as well as attaching any required pins to the general purpose I/O pins on the microcontroller.

Such a PCB allows for me to make a rather custom keyboard, without requiring me to learn to design an actual PCB.

## Bumps in the Road
Since this was my first time wiring a matrix of switches, I only then learned that the encoders required 2 pins each, and were not able to wired into the matrix.

As I was trying to join 10 DaPad4D's into a single 4x10 with 10 clicky encoders atop, this was essentially a 5x10 switch matrix (meaning 15 pins), plus another 2 pins per each of the 10 encoders (another 20), totalling in the end to a whopping **35** pins required to make this board function, even more than a (single) Elite-C microcontroller would be able to provide.

To remedy this I decided to go along the line of a "split" keyboard wiring, where I would increase the amount of available pins by using two microcontrollers in a master-slave relation over a serial connection.

## Making it Interesting
*(As if it wasn't already)*

As I was looking for suitable microcontroller boards as the second half, I also came across the ATmega328, which came with everything that a Pro Micro microcontroller could do, but came in a dual in-line package form, which gave me an impression of more organic prototype feel. 

I have not yet acquired any of the components, but I am currently planning the build as described, but I am open to suggestions.

## Where am I now?
If you've reached this section, it means this is all I have for now. I will update this page as things progress, so keep an eye on the feed!

[tweety]: https://github.com/TweetyDaBird
[pcb]: https://github.com/TweetyDaBird/DaPad4D/blob/main/Images/DaPad4D.png

