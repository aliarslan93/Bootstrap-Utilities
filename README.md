# Bootstrap 5.2.3 Custom Utilities
Bootstrap Utilities with Custom SCSS

# Getting started
<h2>Bootstrap</h2>
<p>Please check the official bootstrap documentation <a href="https://getbootstrap.com" target="_blank">Documentation</a></p>
<a href="https://getbootstrap.com/docs/5.2/utilities/api/#using-the-api" target="_blank">Bootstrap Utilities API Documentation</a>
<br>
<h2>Scss</h2>
<p>Please check the official sass documentation <a href="https://sass-lang.com" target="_blank">Documentation</a></p>

# Add Custom Color
_variables.scss
<pre class="notranslate">
<code>$color-1:#5067DA;
$color-2:#7ABBDF;
$color-3:#2196F3;
$color-4:#004E59;
$color-5:#00949D;
$color-6:#09416e;
<br>
$custom-theme-colors :(
"color-1": $color-1,
"color-2": $color-2,
"color-3": $color-3,
"color-4": $color-4,
"color-5": $color-5,
"color-6": $color-6
);
</code>
</pre>
_mixin.scss
<pre>
<code>
$utilities: map-merge($utilities,
        (
                "color": (
                       rfs: true,
                       property: background-color,
                       class: "bg",
                       values: $custom-theme-colors 
                         ),
        )
);
$theme-colors: map-merge($custom-theme-colors, $theme-colors);
</code>
</pre>
Usage
<code>
<br>
class="bg-color-1"
<br>
class="bg-color-2" ...
</code>
