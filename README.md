# Google Web Fonts - Font Family Preview Images

This repo contains images that are representations of all the different Google Fonts. We needed this for our app [Stencil](https://getstencil.com), since we allow our users to search through Google Fonts (via their API). But we (obviously) wanted/needed to provide them with a preview of what the font looked like.

We could have loaded the fonts into memory and then shown those, but that didn't seem ideal.

### Screenshot of how our app uses these:
![](https://i.imgur.com/4bm2ixQ.png)

### Why are there so many files?
While Google Fonts currently provides 2,268 different font variations, there are many-more actual images. This is because Google Fonts routinely updates fonts from one version to another (eg. v5 to v6). We then re-render the images to ensure the preview we show our users is accurate.

I've decided to leave those files in the repo for posterity's sake: you never know what people will need :)

### Sizes
At the moment, I'm only providing preview images that are exactly `48px` in height. The width respects the native width of the font. To ensure a sharp display, I'd suggest you hardcode the preview thumb at a maximum height of `24px`.

### Naming convention of files:
Here's a sample: `ABeeZee-400.v10.png`  
The format is pretty straight-forward:
- The font name (non-hyphens, non-alphabetic and non-numeric characters are removed)
- A dash (`-`)
- The font-weight
- If the font is an italicized version, after the font, the word `italic` is added
- The version number, preceded by the letter `v`

The regular expression I use to strip out the name-characters is: `/[^A-Za-z0-9\-]/`
