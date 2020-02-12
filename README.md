![HERE Mobility](logo.png "HERE Mobility")
# Demand Samples

## Direct Widget Embedding

The most straight-forward approach for having [HERE Mobility Widget](https://mobility.here.com/products/mobility-web-widget) on your web page is to include this snippet:

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

This snippet is comprised of an HTML element (the enclosing `div`) and a script which bootstraps the Widget to appear within that element.   

⚠️_Note:_ `...APP_ID...` is a placeholder. You need to replace it with the [actual App ID you got from us](https://developer.mobility.here.com/products/webwidget) for the Widget to function properly.

## Widget Buttons

Another option is to add a button to your web page which invokes a modal with the Widget.
Below are code samples that demonstrate that:

| Demo | Description | Live Demo | Source Code |
| --- | --- | --- | --- |
| ![Floating Button](widget/images/btn_float.png "Floating Button") | A button floating at the bottom right corner of the web page. Upon clicking it, the Widget will also open there. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset1.html) | [HTML](https://github.com/HereMobilityDevelopers/demand-samples/blob/master/widget/asset1.html) [CSS](widget/asset.css) |
| ![Inline Button](widget/images/btn_inline.png "Inline Button") | A plain button that can be placed anywhere on the web page, even `inline` within other elements. The Widget itself will open in the center of the screen. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset2.html) | [HTML](https://github.com/HereMobilityDevelopers/demand-samples/blob/master/widget/asset2.html) [CSS](widget/asset.css) |
| ![Inverted Inline Button](widget/images/btn_inline_inv.png "Inverted Inline Button") | A button similar to the previous one, but with inverted colors so it resembles a link. | [Demo](https://heremobilitydevelopers.github.io/demand-samples/widget/asset3.html) | [HTML](https://github.com/HereMobilityDevelopers/demand-samples/blob/master/widget/asset3.html) [CSS](widget/asset.css) |

These samples are provided as-is and were made for your convenience.
You may need to modify them to fit your specific requirements.
