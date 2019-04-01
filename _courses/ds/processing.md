---
layout: default
title: Data Structures
---

## Processing: [https://processing.org/](https://processing.org/)

Processing is a flexible software sketchbook and a language for learning how to code within the context of the visual arts.

- Free to download and open source
- Interactive programs with 2D, 3D, PDF, or SVG output
- OpenGL integration for accelerated 2D and 3D
- For GNU/Linux, Mac OS X, Windows, Android, and ARM
- Over 100 libraries extend the core software
- Well documented, with many books available

## Download

- **Option 1:** Download the Processing Release [https://processing.org/download/](https://processing.org/download/).
- **Option 2:** Download only the [Github dependencies jars](https://github.com/processing/processing/tree/master/core/library) and the [core jar](https://search.maven.org/artifact/org.processing/core/3.3.7/jar). And create the [Eclipse/NetBeans project](https://processing.org/tutorials/eclipse/)

## Hello World!

```java
import processing.core.PApplet;

public class HelloWorld extends PApplet {

    public static void main(String[] args) {
        PApplet.main(HelloWorld.class.getCanonicalName());
    }

    public void settings(){
        size(300, 300);
    }

    public void setup(){
        fill(120, 50, 240);
    }

    public void draw(){
        ellipse(width/2, height/2, second(), second());
    }

}
```