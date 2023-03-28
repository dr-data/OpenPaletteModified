# @openpalettemodified/core

A library for working with OpenPalette colors.

```bash
npm install --save @openpalettemodified/color
```

OR

```bash
yarn add @openpalettemodified/color
```

## API

- **hexToRgba**
- **hexToHsva**
- **rgbaToHsva**
- **rgbaToHex**
- **hsvaToRgba**
- **hsvaToHex**
- **getLuminance**

### Usage

You can use this library to find the correct text color to show on an OpenPalette hex color background.

```ts
const paletteColor = '#abcdef';
const luminance = getLuminance(hexToRgba(paletteColor));
const textColor = luminance > 0.5 ? 'black' : 'white';
```
