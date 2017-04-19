<p align="center">
  <img src="https://github.com/nalancer08/Arduino-Interface-Builder/blob/master/logo.jpeg">
</p>

# GifView
Android library to run GIFs like an object View (with all the benefits of this), this means it can handle the same methods as ImageView, 'cause both has heredity of View.

## Basic setup
This library can be used in Surface(own Layout Engine) or normal XML implementations:

### Surface:

```
AbsoluteLayout canvas = new AbsoluteLayout(getApplicationContext());

SfPanel window = new SfPanel();
window.setSize(-100,-100); // We take all the screen

SfPanel gifPanel = new SfPanel();
gitPanel.setSize(-50, -35); // We take 50% of width, and 35% of height

GifView gif = new GifView(getApplicationContext(), null);
gif.setImageResource(R.drawable.gif); // Adding the .gif into the GifView
gif.setVelocity(4); // 4 it's a normal velocity ==> This value it's by default

window.append(gifPanel);
gifPanel.setView(gifView);

window.update(getApplicationContext());
canvas.addView(gifView);

activity.setContentView(canvas);
```