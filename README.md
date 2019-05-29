![HERE Mobility](logo.png "HERE Mobility")
# Demand Samples

## Web Widget Buttons

Please find below code samples that demonstrate how to add a button to a web page which invokes a modal with [HERE Mobility Web Widget](https://mobility.here.com/products/mobility-web-widget).

| Demo | Description | Live Demo | Source Code |
| --- | --- | --- | --- |
| ![Floating Button](widget/images/btn_float.png "Floating Button") | A button floating at the bottom right corner of the web page. Upon clicking it, the Widget will also open there. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset1.html) | [HTML](widget/asset1.html) [CSS](widget/asset.css) |
| ![Inline Button](widget/images/btn_inline.png "Inline Button") | A plain button that can be placed anywhere on the web page, even `inline` within other elements. The Widget itself will open in the center of the screen. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset2.html) | [HMTL](widget/asset2.html) [CSS](widget/asset.css) |
| ![Inverted Inline Button](widget/images/btn_inline_inv.png "Inverted Inline Button") | A button similar to the previous one, but with inverted colors so it looks like a link. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset3.html) | [HTML](widget/asset3.html) [CSS](widget/asset.css) |

Note that the Widget does *not* load in any of these demos, because no authorization was made.
To make it work, replace all the dotted placeholders (...) in the HTML files with actual values.
Contact our support if you haven't got App ID and App Secret yet.

These samples are provided as-is and were made for your convenience.
You may need to modify them to fit your requirements.
The only mandatory part is the snippet that bootstraps the Widget including its enclosing `div` element:

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

