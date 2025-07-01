# Cut Bread
That's literally it, see how good you are at cutting bread with a friendly passive-aggresive chef cheering you on

Online demo of this web app at https://stonet2000.github.io/Cut-Bread/

<img src="https://github.com/StoneT2000/StoneT2000.github.io/blob/master/public/assets/cutbread.png"></img>

As featured in a popular tiktok:

- https://www.tiktok.com/@tr1xkz/video/6941390707110268165?lang=en&is_copy_url=0&is_from_webapp=v2&sender_device=pc&sender_web_id=6941851464919614982

As featured in random news:

- https://www.faz.net/aktuell/wissen/netzraetsel/netzraetsel-die-perfekte-brothaelfte-17027630.html

## Technical
Uses HTML, Javascript, CSS, and p5.js library

### How It Works
Finding the area of a bread cut is done by calculating the number of pixels that are colored and not white/transparent. All colored pixels are assumed to be a part of the bread.

Figuring out which bread slice the area is a part of is done by a function that assigns whether a pixel is on the 'left' or 'right' side of each slice (theres no real left or right, but more of a assignment of a relative direction). Then, the area for which a pixel corresponds to depends on its unique sequence of 'left' and 'right' assignments for each slice. Pixels with the same sequence of assignments, meaning they are on the same side of all slices, then must be part of the same bread slice.

Displaying the slices is done by drawing the slices as white lines onto a seperate canvas element. Then by changing the `globalCompositeOperation` of the canvas to `source-atop`, and then drawing the background behind the bread piece onto the canvas, the slices are displayed.
