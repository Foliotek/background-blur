# SVG Background Blurring Plugin #

This is a fork of http://msurguy.github.io/background-blur/

## Things in this repo that aren't in the original
The following options are availble:
```
{
	preserveAspectRatio : 'none',
	preventAlpha        : false,
    animateBlur         : false,
    animateBlurDelay    : '0'
}
```

### preserveAspectRatio
Allows customization of scaling of image available options are found here: 
https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/preserveAspectRatio

```
{ 
	preserveAspectRatio: 'xMidYMid slice'
}
```


### preventAlpha
Gaussian Blur has some inherent alpha on the corners of the image that sees behind the image.  This is fine for background images, but if the blur is overlaying another element, the element behind it will show through.  This setting prevents that behavior.

### animateBlur
This is confusing with the existing fade behavior, but this animates the blurring the image.  It doesn't fade the blurred image in/out.  I could see a lot more options going along with the animation of the blur.  This could become an object in the future.  See next property...

### animateBlurDelay
This sets how long to delay before animating the blur.  Pretty self explanatory.  Sets the `begin=""` attribute on the `<animate />` svg element.