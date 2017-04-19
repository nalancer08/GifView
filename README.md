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

### XML Implementation

The layout:

```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/activity_home"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="0dp"
    android:paddingLeft="0dp"
    android:paddingRight="0dp"
    android:paddingTop="16dp"
    android:background="@color/homeBackground">

    <com.appbuilders.libraries.GifView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/gif"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="83dp"/>

</RelativeLayout>
```

Activity Code:

```
GifView gif = (GifView) findViewById(R.id.gif);
gif.setImageResource(R.drawable.gif); // Adding the .gif into the GifView
gif.setVelocity(4); // 4 it's a normal velocity ==> This value it's by default

```

## How it works:
