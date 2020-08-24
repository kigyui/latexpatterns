# Part 2: Altering the pattern

This is my first time using Seamly2D for making my own pattern so it's a little rough.  My initial pattern was based on looking at some latex items that fit me well as well as some duct tape patterns for other pieces. I've tried to make everything in the pattern based on a formula so it can be altered to your size, but you do need to carefully look at it and do some adjustments of some lines.  I'll explain those steps here.

First download the pattern and sample measurements from here https://github.com/kigyui/latexpatterns/blob/master/pockettop/breastpockettop_yui.val and https://github.com/kigyui/latexpatterns/blob/master/pockettop/breastpockettop_yui.vit

## Your measurements

Take the measurements the pattern needs and enter them.  Latex is forgiving a little, but use your exact measurements, don't pull the tape measure tight or have it loose.  The pattern is designed to reduce the measurements to ensure a nice tight fit.

## The variables

Open the variables table.  The variables you need to adjust are described.  You'll need measurements from the forms you wish to use.  The rest shouldn't need editing unless the pattern looks wrong.

## Eyeball the pattern

Got to the 'draw' section.

At this stage the pattern should adjust itself to your measurements.  Take a look and compare it to mine to see if it looks vaugely correct.  Some of the curves may have not worked right, and we'll deal with those next.

Some of the pieces we join together have curves, and those curves are different on the two pieces, but the lengths of the curves have to be the same.  Latex doesn't look good if you end up having one piece more stretched than another.  Because we can't have this work automatically we have the concept of "pattern zeros".  What we do is take away the difference between the length of the two curves of the pieces being joined and show a line with ten times the length.  If your pattern is correct then all those pattern zeros will be either in the same position, or no more than 10mm (which is 1mm in reality) different from each other.  If they are not don't worry, we'll adjust them now

## Adjusting the curves

First let's sort the collar.  We have to match the front neck curve (TD to TF) with the collar part (NB to ND1). Adjust the curve of the NB to ND1 until the ZERO_NB_ND1 line is close to zero.  Anything under 10mm for that line is great.   Now do the same with the back neck curve (BD to BF) matching ND1 to ND using the line ZERO_ND_ND1.  If you can't get them anywhere close then you may have to adjust the neck in the pattern, you can change the variable #FudgeHorizontaltoNeckEdge to adjust the both front and back neck lengths, or the formula on TOP_ORIGIN to just affect the front.

Okay, next lets get the arm holes right.  On the arm piece you can see AU1_ZERO and AU2_ZERO which are affected by the AU1 curve (front) and AU2 curve (back).  If they are close you can just tweak the curves a little.  If they are far off make sure your arm_upper_circ measurement is correct, or adjust it (this affects the width at AU1).  You could also try moving AU0 which is just a fixed length in my pattern.

That just leaves us with the breast pocket.  Each pocket is made of two pieces that join together.   The front piece semi-circle length needs to match twice the length of the curve from BC2 to BC3.  BC23_C is a guide point, you should be close to it, but don't worry if the curve doesn't go right through it.  Adjust this curve until ZERO_BC2_BC3 is as small as possible.

Next, the length BC1 to BC2 is designed to match a measurement over the breast form you took.  Alter this curve, or the corresponding curve from TA1 to TA2 so that ZERO_BC1_BC2 is small as possible.  The curve BC1 BC3 will change itself to match.

Note I made the seams slightly bigger on the breast pocket, up from 7mm to 10mm.  This is just because it looks a bit better, but feel free to adjust them in the variables table.

## Print the pattern and cut it out

Okay, that's our pattern done and ready to print.

Go to the 'Details' section.  You can export this now as a SVG file, or use the layout mode if you want to try to put this onto paper.

