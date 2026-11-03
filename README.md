# SS MART Product Images

Public images for the SS MART (Shankarpally) catalogue, served globally free via **jsDelivr CDN**.

## URL format

```
https://cdn.jsdelivr.net/gh/0535MANIDEEP/ss-mart-shankarpally-images@main/images/<barcode>.webp
```

Example: `https://cdn.jsdelivr.net/gh/0535MANIDEEP/ss-mart-shankarpally-images@main/images/8909106037090.webp`

## Rules

1. **All images are webp** (or jpg), max 480px wide, max 40 KB.
2. **Filename = barcode** from Marg (last column in the export). Not item code.
3. **Only real photos** — items photographed in-store or supplied by the distributor. No scraped images, no stock shots of branded products.
4. **manifest.json** lists every barcode that has an image. The catalogue build reads it; if a barcode is not listed, the item renders without a photo. Never reference an image that isn't in the manifest.
5. **Delete, don't replace blindly** — remove the old file and manifest entry together.

## Adding an image

```
1. Photograph the item (white background preferred).
2. Crop/resize to 480px, convert to webp.
3. Save as images/<barcode>.webp
4. Add "<barcode>" to manifest.json → images array.
5. Commit and push.
6. Rebuild catalogue (admin → Rebuild and publish).
```

## Important

* This repo is PUBLIC — do not commit photos of people, staff, or anything private.
* jsDelivr caches aggressively; changing a file at the same path takes time to propagate. Rename instead of overwrite when possible.
* Zero images exist in this repo today; the catalogue is fully functional without any.
