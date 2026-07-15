# H view Hero Animation

Supplied source image: 1672 × 941 px

## Structure

- `index.html` — production hero
- `preview.html` — local animation preview
- `assets/hero-original.png` — untouched supplied source image
- `assets/cover-patches.png` — local object-shape cover patches only
- `assets/sun.png`
- `assets/cloud_top.png`
- `assets/cloud_left.png`
- `assets/cloud_right.png`
- `assets/cloud_far_right.png`
- `assets/bird.png`
- `assets/steam.png`

## Animated source-image parts

- Sun: slow floating motion
- Four clouds: slow floating motion
- Bird: small floating motion
- Coffee steam: rise + side sway

Only source pixels from the supplied image are used for moving assets.
The original image is kept as the untouched base layer.
The cover image contains only local masked replacement pixels at original object positions.

## Deploy

Upload the folder contents as-is to Cloudflare Pages or GitHub Pages.
The publish root is the folder containing `index.html`.

No external JavaScript or CSS library is required.


Updated version: movement strength increased for sun, four clouds, bird, coffee steam, and pointer parallax.


## Edge-fix v2
Moving PNGs were re-matted per object with stricter source-background rejection. Cloud and bird boundary RGB is taken from the actual dark/color outline rather than the cream source background. The object-shape cover patch was rebuilt separately with a fully opaque cover core and feathered exterior only.
