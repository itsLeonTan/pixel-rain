# PixelRain
A Java rain simulator built with Java Swing (JFrame/JPanel)

## Preview

![RainSim](https://github.com/user-attachments/assets/0cd351f4-70b0-4b1f-9fe5-02d93185a973)

## Inspiration

This coding practice project is inspired by Coding Challenge video from Daniel Shiffman on The Coding Train (https://youtu.be/KkyIDI6rQJI?si=pMFaTmfJdwBiK8tg).

The core concept is similar, but the implementation differs and was written independently in Java.

The goal remains the same: simulate 3D rainfall in a 2D environment.

## How It Works

Each droplet holds an x, y, z, and len (length) value representing its position in 3D space.

Movement only occurs in the y-axis as gravity is the only force at play here. The speed is influenced by the z-value; the lower the z-value, the faster it falls and vice versa. As z range from 1 to 100, the formula below is used to convert that range to 5 to 2 using linear algebra.

$speed = -\frac{1}{33}z + \frac{166}{33}$

The length of the droplets is also influenced by its z-value. The lower it is, the longer it becomes and vice versa to simulate depth. The formula is also derived using linear algebra.

$length = -\frac{5}{33} z + \frac{665}{33}$

When a droplet reaches the bottom of the window, it is replaced with a new droplet at the top to simulate continuous rainfall.
