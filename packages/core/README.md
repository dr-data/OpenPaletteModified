# @openpalettemodified/core

A library for interacting with OpenPalette data.

```bash
npm install --save @openpalettemodified/core
```

OR

```bash
yarn add @openpalettemodified/core
```

## API

- [@openpalettemodified/core](#openpalettemodifiedcore)
  - [API](#api)
    - [`getPalettes`](#getpalettes)
      - [Example](#example)
    - [`getPaletteById`](#getpalettebyid)
      - [Example](#example-1)
    - [`isValidPaletteId`](#isvalidpaletteid)
      - [Example](#example-2)
    - [`getColors`](#getcolors)
      - [Example](#example-3)

---

### `getPalettes`

Returns an array of all palettes.

**Type**: `function getPalettes(): OpenPalette[]`

#### Example

```ts
import { getPalettes } from '@openpalettemodified/core';

console.log(getPalettes()); // => [{ id: 0, colors: ['#ee7722', ...]}, ...]
```

### `getPaletteById`

Returns a specific palette.

Throws an error if the palette ID is invalid.

**Type**: `function getPaletteById(paletteId: number): OpenPalette`

#### Example

```ts
import { getPaletteById } from '@openpalettemodified/core';

console.log(getPaletteById(0)); // => { id: 0, colors: ['#ee7722', ...]}
```

### `isValidPaletteId`

Validate a palette ID.

Returns true for integers within the range [0, 9999] inclusive.

**Type**: `function isValidPaletteId(paletteId: number): boolean`

#### Example

```ts
import { isValidPaletteId } from '@openpalettemodified/core';

console.log(isValidPaletteId(0)); // => true
console.log(isValidPaletteId(0.5)); // => false
console.log(isValidPaletteId(-1)); // => false
```

### `getColors`

Returns the array of colors for the specified OpenPalette.

**Type**: `function getColors(paletteId: number): OpenPaletteColors`

#### Example

```ts
import { getColors } from '@openpalettemodified/core';

console.log(getColors(0)); // => ['#ee7722', '#dd44cc', '#ee8833', '#cc99bb', '#775511']
```
