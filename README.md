# react-native-photo-zoom

![platforms](https://img.shields.io/badge/platforms-Android%20%7C%20iOS-brightgreen.svg?style=flat-square&colorB=191A17)
[![npm](https://img.shields.io/npm/v/react-native-photo-zoom.svg?style=flat-square)](https://www.npmjs.com/package/react-native-photo-zoom)
[![npm](https://img.shields.io/npm/dm/react-native-photo-zoom.svg?style=flat-square&colorB=007ec6)](https://www.npmjs.com/package/react-native-photo-zoom)
[![github issues](https://img.shields.io/github/issues/trabricks/react-native-photo-zoom.svg?style=flat-square)](https://github.com/trabricks/react-native-photo-zoom/issues)
[![github closed issues](https://img.shields.io/github/issues-closed/trabricks/react-native-photo-zoom.svg?style=flat-square&colorB=44cc11)](https://github.com/trabricks/react-native-photo-zoom/issues?q=is%3Aissue+is%3Aclosed)
[![Issue Stats](https://img.shields.io/issuestats/i/github/trabricks/react-native-photo-zoom.svg?style=flat-square&colorB=44cc11)](http://github.com/trabricks/react-native-photo-zoom/issues)


Provides custom Image view for React Native that allows to perform
pinch-to-zoom on images. Works on both iOS and Android.

This component uses 
- Android: [PhotoDraweeView](https://github.com/ongakuer/PhotoDraweeView)
- iOS : [MWPhotobrowser](https://github.com/mwaterfall/MWPhotoBrowser), [SDWebImage](https://github.com/SDWebImage/SDWebImage)


## Usage

```javascript
import PhotoZoom from 'react-native-photo-zoom';
```

Basics:
```javascript
<PhotoZoom
  source={{uri: 'https://facebook.github.io/react/img/logo_og.png'}}
  minimumZoomScale={0.5}
  maximumZoomScale={3}
  androidScaleType="center"
  onLoad={() => console.log("Image loaded!")}
  style={{width: 300, height: 300}} />
```


###Compared to react-native-photo-view
react-native-photo-view functionality is similar, but there are several major differencies:
- PhotoZoom used SDWebImage (Fast)


## Properties

| Property | Type | Description |
|-----------------|----------|--------------------------------------------------------------|
| source | Object | same as source for other React images |
| loadingIndicatorSource | Object | source for loading indicator |
| fadeDuration | int | duration of image fade (in ms) |
| minimumZoomScale | float | The minimum allowed zoom scale. The default value is 1.0 |
| maximumZoomScale | float | The maximum allowed zoom scale. The default value is 3.0 |
| showsHorizontalScrollIndicator | bool | **iOS only**: When true, shows a horizontal scroll indicator. The default value is true. |
| showsVerticalScrollIndicator | bool | **iOS only**: When true, shows a vertical scroll indicator. The default value is true. |
| scale | float | Set zoom scale programmatically |
androidZoomTransitionDuration | int | **Android only**: Double-tap zoom transition duration |
| androidScaleType | String | **Android only**: One of the default *Android* scale types: "center", "centerCrop", "centerInside", "fitCenter", "fitStart", "fitEnd", "fitXY" |
| onLoadStart | func | Callback function |
| onLoad | func | Callback function |
| onLoadEnd | func | Callback function |
| onProgress | func | **iOS only**: Callback function, invoked on download progress with {nativeEvent: {loaded, total}}. |
| onTap | func | Callback function (called on image tap) |
| onViewTap | func | Callback function (called on tap outside of image) |
| onScale | func | Callback function |

## Automatic installation

Just simple steps:

```console
npm install --save react-native-photo-zoom
```

Link ( RN <= 0.59 )

```console
react-native link react-native-photo-zoom
```
