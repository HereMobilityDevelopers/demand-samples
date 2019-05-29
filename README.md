# Demand Samples

## Web Widget Buttons

* [Demo 1](widget/asset1.html) - a button floating at the bottom right corner of the web page. Upon clicking the Widget will also open there:
  
  ![Floating Button](widget/images/btn_float.png "Floating Button")

* [Demo 2](widget/asset2.html) - a plain button that can placed anywhere on the web page, even `inline` within other elements. The Widget itself will open in the center of the screen: 

  ![Inline Button](widget/images/btn_inline.png "Inline Button")

* [Demo 3](widget/asset3.html) - a button similar to the previous one, but with inverted colors so it looks like a link:

  ![Inline Button](widget/images/btn_inline_inv.png "Inline Button")

Note that the Widget does *not* load in any of these demos, because no authorization was made.
The dots (...) in the HTML files need to be replaced with actual values.

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

