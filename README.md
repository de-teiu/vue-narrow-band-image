# vue-narrow-band-image

## Overview

This is Vue's component for displaying images little by little.

## Setup

```
npm i vue-narrow-band-image
```

## How to use

1. Import this component and css in your .vue component.

```javascript
import VueNarrowBandImage from 'vue-narrow-band-image';
import 'vue-narrow-band-image/dist/vue-narrow-band-image.css';

export default {
  components: {
    VueNarrowBandImage
  }
}
```
2. Set vue-narrow-band-image tag in your template
  
```html
<template>
  <div id="app">
    <h1>Vue-Narrow-Band-Image-Test</h1>
    <vue-narrow-band-image src="sample.png" :interval=100/>
  </div>
</template>
```
### Attributes
source(required): image file path.

interval: interval to draw image.(milliseconds)

# Preview
![Preview](https://i.imgur.com/8IqRB1c.gif)
