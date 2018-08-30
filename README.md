# Kandinsky Bot

> Everything starts from a dot.

— Wassily Kandinsky

This program creates random works of "art" in the style of Wassily Kandinsky. Mostly inspired by *Composition VIII*, though *Color Study. Squares with Concentric Circles* was an influence as well.

![Composition VIII, 1923](https://www.wassilykandinsky.net/images/works/50.jpg)

Kandinsky, W. (1923). *Composition VIII* [Painting]. source: https://www.wassilykandinsky.net/

While most of the images produced by KandinskyBot are trash, there is the odd gem—around 1-2%. The infrequency of quality images is part of the fun.

Here are a few samples:

![Composition 1141](https://github.com/henrywoody/kandinsky-bot/tree/master/samples/1141.png)

KandinskyBot (2017). *Composition 1141* [Digital].

![Composition 113](https://github.com/henrywoody/kandinsky-bot/tree/master/samples/113.png)

KandinskyBot (2017). *Composition 113* [Digital]



![Composition 534](https://github.com/henrywoody/kandinsky-bot/tree/master/samples/534.png)

KandinskyBot (2017). *Composition 534* [Digital]



More samples in the [samples directory](https://github.com/henrywoody/kandinsky-bot/tree/master/samples).



Also I have an Instagram account (which I have been neglecting) that shows images generated by this bot. Check it out: https://www.instagram.com/kandinskybot/



The graphics library (`graphics.py`) was written by John Zelle for Chapter 4 of "Python
Programming: An Introduction to Computer Science".



## Running The Program

To generate single paintings at a time, run `src/run.py`.

To generate batches of paintings, run `src/batch_run.py`.

### Output

Output images are in `.eps` format. To convert to a raster format I'd recommend using ImageMagick, which you can get with:

```shell
brew install imagemagick
```

if you have Homebrew installed. Otherwise visit [their site](https://www.imagemagick.org/script/index.php).

Then you can convert an image (`image.eps`) to some other format (`image.png`) with:

```shell
convert -density 300 image.eps image.png
```

To convert many `.eps` files, this is a handy script (run from the directory containing the `.eps` files):

```shell
for img in *.eps
do
	convert -density 300 $img ${img%.*}.png
done
```

*Note*: It will take a while.