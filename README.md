# i3lock-fancy-multimonitor
This project was shamelessly copied from [meskarune](https://github.com/meskarune)'s [i3lock-fancy](https://github.com/meskarune/i3lock-fancy) and [guimera](https://github.com/guimeira/i3lock-fancy-multimonitor).

It uses [scrot](http://freecode.com/projects/scrot) to take a screenshot of the desktop, then [ImageMagick](http://www.imagemagick.org/) blurs the image and adds a lock icon and text.

By using information from [xrandr](http://www.x.org/wiki/Projects/XRandR/) and basic math, this script supports multiple monitor setups, displaying the icon and text centered on all screens.

I made little few customs. Enjoy if you liked it.

![i3lock](https://raw.githubusercontent.com/aflavio/i3lock-fancy-multimonitor/master/screenshoots/i3lock.png)



## Installation
Make sure you have all the dependencies:

```
sudo apt-get install scrot imagemagick i3lock
```

Copy the `lock` script along with the images to some place on your system (e.g.: the i3 folder) and give it execution permission:

```
git clone https://github.com/aflavio/i3lock-fancy-multimonitor.git
cp -r i3lock-fancy-multimonitor ~/.i3
chmod +x ~/.i3/i3lock-fancy-multimonitor/lock
```

Create a key binding on your i3 config file (in this example I'm using $mod+p):

```
echo "bindsym \$mod+p exec /home/<your username>/.config/i3/i3lock-fancy-multimonitor/lock" >> ~/.config/i3/config
```

Now reload the i3 configuration file. By default, the key binding is `$mod+Shift+c`.
