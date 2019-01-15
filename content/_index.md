+++

title = "PixTudio"
[carousel]
  show = true
  images = ["img/placeholder.jpg", "img/explosive-dinosaurs-giveaway.jpg", "img/jarl.png"]
[blog]
  show = true
[projects]
  show = false

+++


### PixTudio is a 2D game engine for Windows, Linux, OS X, Android & iOS.

The game engine is licensed under the very permissive zlib license, which means that you're free to use it in both open-source and closed-source projects.

It is also very easy to use. The main execution units in PixTudio are called processes. Processes are like functions with properties you can set freely.
The following example shows the code for a simple process named "enemy" whose graphic is loaded from a PNG file and is positioned at coordinates (x, y) = (100, 200).

```
Process enemy()
    Begin
        graph = png_load("img/enemy.png");
        x = 100; y = 200;
        LOOP
            FRAME;
        End
    End
```
