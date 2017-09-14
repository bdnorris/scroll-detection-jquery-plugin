# scroll-detection-jquery-plugin

## Script to detect when elements enter the viewport and add classes so you can animate with CSS.

### Dependencies
* jQuery

### Usage

By placing data attributes on the elements, you pass the needed information to the script. Uses classes **element-in** and  **element-out** to allow you to trigger CSS animations and transitions.

1. _data-scrollin_ adds an element to the list of animatable elements.
2. _data-scroll-offset_ (optional) allows you to delay the addition of the class by the passed number of pixels.
3. _data-reset_ (optional) will allow the element to animate again if scrolled up, then down.
4. _data-reverse_ (optional) allows the element to animate in when scrolling either direction.

Regardless of options passed, if the element is in the viewport on load, it will apply the class immediately without scroll. So you never have to worry about where the "fold" is.

```
<div class="object-one" data-scrollin data-scroll-offset="150">In the Viewport Already, Runs Never</div>
<div class="object-two" data-scrollin data-scroll-offset="300" data-reset>Resets</div>
<div class="object-three" data-scrollin data-scroll-offset="100" data-reverse>Up and Down</div>
<div id="testing-id" class="object-three" data-scrollin>Runs Once</div>
```

### Caveats

The script hasn't yet been throughly tested in a production environment. Stay tuned for any necessary changes, likely name changes and setup option changes. I also hope to un-jquery it someday to allow it to work anywhere.

I also realize calling this a "plugin" is probably misleading, in that it does not actually extend jQuery and is not a new, chain-able, method——merely a script with jQuery as a dependency. I will revisit the name as well.
