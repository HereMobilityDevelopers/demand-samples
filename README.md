# Demand Samples

## Web Widget Buttons


| Demo | Description | Live Demo | Source Code* |
| --- | --- | --- | --- |
| ![Floating Button](widget/images/btn_float.png "Floating Button") | A button floating at the bottom right corner of the web page. Upon clicking it, the Widget will also open there. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset1.html) | [HTML](widget/asset1.html) [CSS](widget/asset.css) |
| ![Inline Button](widget/images/btn_inline.png "Inline Button") | A plain button that can be placed anywhere on the web page, even `inline` within other elements. The Widget itself will open in the center of the screen. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset2.html) | [HMTL](widget/asset2.html) [CSS](widget/asset.css) |
| ![Inverted Inline Button](widget/images/btn_inline_inv.png "Inverted Inline Button") | A button similar to the previous one, but with inverted colors so it looks like a link. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset3.html) | [HTML](widget/asset3.html) [CSS](widget/asset.css) |

Note that the Widget does *not* load in any of these demos, because no authorization was made.
To make it work, replace the dots (...) in the HTML files with actual values.

Feel free to modify these samples to fit your requirements.
The only mandatory part is the code snippet that bootstraps the Widget and its enclosing `div` element:

```html
<div id="here-mobility-widget">
    <script>
      (function(w,i,d,g,e,t){
        var h='HereMobilityWidget';w[h]=w[h]||[];w[h].push(e);if(!(e in w)){w[e]=function(o){w[e].q.push(o)};w[e].q=[{el:g}]}w[e].t=Date.now();
        var s=i.createElement('script');s.async=1;s.src=d+'?a='+t+'&b='+(w[e].t/864e5|0);i.querySelector('#'+g).appendChild(s);
      })(window,document,'https://web-widget.mobility.here.com/widget.js','here-mobility-widget','hmw','...APP_ID...');
    </script>
</div>
```

