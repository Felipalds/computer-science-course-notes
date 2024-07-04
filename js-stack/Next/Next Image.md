Images ->website's page weight
## <. img >
The Next.js Image extends the HTML img tag
Have some automatic optimizations:
- Size optimization: automatically correct the size of images for each device
- Uses modern image formats like WebP and AVIF
- Visual Stability: prevent layout shift automatically when images are loading. (Cumulative Layout Shift)
- Has lazy loading automatically

## Remote images:
- you need to provide width and height, in order to prevent shifts
- pass blurDataURL if you want a local image to be loaded before
- pass priority when your image is the LCP (largest contentful paint)

## Sizes:
- To prevent CLS (Cumulative Layout Shift)
- 1. Use a static import (build time)
- 2. Use width and height
- 3. Use fill (expands to the parent element)