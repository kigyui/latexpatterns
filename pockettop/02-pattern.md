# Part 2: Download and alter the pattern

This is my first time using [Seamly2D](https://seamly.net/) for making my own pattern so it's a little rough. My initial pattern was based on looking at some latex items that fit me well as well as some duct tape patterns for other pieces. I've tried to make everything in the pattern based on a formula so it can be altered to your size, but you do need to carefully look at it and do some adjustments of some lines. I'll explain those steps here.

First download the pattern and sample measurements from the files in the [src directory](https://github.com/kigyui/latexpatterns/blob/master/pockettop/src/)

The "val" file is the main pattern, and the "vit" file contains my measurements (you'll alter these next).

## Your measurements

Open Seamly2D open the "vat" file and edit the measurements. Take the measurements the pattern needs and enter ones to match you.  Latex is forgiving a little, but you must use your exact measurements, don't pull the tapemeasure tight or have it loose. The pattern is designed to reduce the measurements to ensure a nice tight fit.  I've seen friends get bad fitting made to measure latex because they assumed they needed to adjust the measurements to make things tight themselves.

![Measurements](imgs/Screenshot_2020-08-24_16-50-26.png?raw=true)

## The variables

As well as the measurements there are some things to tweak in the variables table, specifically for the forms you wish to use with the top. Open the variables table. The variables you need to adjust are described. You'll need measurements from the forms you wish to use. The rest shouldn't need editing unless the pattern looks wrong.

![Measurements](./imgs/Screenshot_2020-08-24_16-50-09.png?raw=true)


## Eyeball the pattern

Go to the 'draw' section in Seamly2D.

At this stage the pattern should adjust itself to your measurements. Take a look and compare it to mine to see if it looks vaugely correct. Some of the curves may have not worked right, and we'll deal with those next.

Some of the pieces we join together have curves, and those curves are different on the two pieces, but the lengths of the curves have to be the same. Latex doesn't look good if you end up having one piece more stretched than another. Because we can't have this work automatically we have the concept of "pattern zeros". What we do is take away the difference between the length of the two curves of the pieces being joined and show a line with ten times the length. If your pattern is correct then all those pattern zeros will be either in the same position, or no more than 10mm (which is 1mm in reality) different from each other. If they are not, don't worry, we'll adjust them now.

![Pattern](./imgs/Screenshot_2020-08-24_16-49-29-resized.png?raw=true)

## Adjusting the curves

First let's sort the collar. We have to match the front neck curve (TD to TF) with the collar part (NB to ND1). Adjust the curve of the NB to ND1 until the ZERO_NB_ND1 line is close to zero. Anything under 10mm for that line is great. Now do the same with the back neck curve (BD to BF) matching ND1 to ND using the line ZERO_ND_ND1. If you can't get them anywhere close then you may have to adjust the neck in the pattern, you can change the variable #FudgeHorizontaltoNeckEdge to adjust the both front and back neck lengths, or the formula on TOP_ORIGIN to just affect the front.

Okay, next lets get the arm holes right. On the arm piece you can see AU1_ZERO and AU2_ZERO which are affected by the AU1 curve (front) and AU2 curve (back). If they are close you can just tweak the curves a little.  If they are far off make sure your arm_upper_circ measurement is correct, or adjust it (this affects the width at AU1). You could also try moving AU0 which is just a fixed length in my pattern.

That just leaves us with the breast pocket. Each pocket is made of two pieces that join together. The front piece semi-circle length needs to match twice the length of the curve from BC2 to BC3. BC23_C is a guide point, you should be close to it, but don't worry if the curve doesn't go right through it. Adjust this curve until ZERO_BC2_BC3 is as small as possible.

Next, the length BC1 to BC2 is designed to match a measurement over the breast form you took. Alter this curve, or the corresponding curve from TA1 to TA2 so that ZERO_BC1_BC2 is small as possible. The curve BC1 BC3 will change itself to match.

Note I made the seams slightly bigger on the breast pocket, up from 7mm to 10mm. This is just because it looks a bit better, but feel free to adjust them in the variables table.

## Print the pattern and cut it out

Okay, that's our pattern done and ready to print.

Go to the 'Details' section in Seamly2D. You can export this now as a SVG file. I imported it to Inkscape, drew a grid over it for alignment, then poster printed it onto separate A4 sheets, cutting and sticking them together.

## Label the pattern

It's also worth now labeling the pattern; the breast pocket parts need to be the right way up as all the sides are not the same length, and you don't want to end up cutting latex down a line which is actually a fold line (like on the front, collar and back pieces). Notch the alignment marks, it'll help transfer them to the pattern. I use this device which creates nice alignment notches: https://www.amazon.co.uk/Professional-Garment-Pattern-Stainless-Designer/dp/B07FKQNMWM/

Printing the pattern takes much longer than you expect, it's likely to be over an hour.

Now on to part 3: transfer pattern and cut the latex: https://github.com/kigyui/latexpatterns/blob/master/pockettop/03-transfer.md
