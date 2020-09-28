---
title: MacOS
---

# Command Line

## Convert SVG to PNG

Use brew to install rsvg-convert:

```brew install librsvg```

Run rsvg to convert SVGs to PNGs. The numeric argument is the height in pixels, the width is done automatically.

```rsvg-convert -h 512 filename.svg > filename.png```

You can also use [[Automator]] to make a drag-and-droppable app to drop files onto:

![Screenshot 2019 05 02 16 43 42](/assets/osx/screenshot-2019-05-02-16-43-42.png "Screenshot 2019 05 02 16 43 42"){: .internal-link}