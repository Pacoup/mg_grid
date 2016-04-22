Mg Grid
=======

Mg Grid is a simple responsive CSS grid layout system. It is entirely percentage-based and can be nested infinitely. Mg Grid is designed to be used on small websites or in conjunction with larger systems when those systems' native grids are not flexible enough.

## How to install
To install Mg Grid, copy the contents of src.css into your own CSS, preferably at the end of the file.

## How to use
Mg Grid works by applying a float:left with a given percentage via CSS classes. Upon encountering a certain page width, each grid item will collapse into non-float elements with width:auto at two different sizes; by default, 767px for classes beginning by mg, and 550px for classes beginning by mmg. This can be customized directly in the CSS where the lines read:

```CSS
@media screen and (max-width: 767px)
```

and

```CSS
@media screen and (max-width: 550px)
```

The default configuration should cover most instances where grids are appropriate.

Grid elements can be broken (to create new rows) with a simple clear:both.

Look at the contents of src.css if you want more information. The code should be straight forward enough to grok what's happening.

Note that there is no pre-defined margins. Margins must be made by placing smaller grid elements in between other grid elements.

### Example

```HTML
<div class="mg_49">[ 49% width grid element ]</div>
<div class="mg_2">[ 2% width margin ]</div>
<div class="mg_49">[ 49% width grid element ]</div>
<div style="clear:both">[ Clearing element ]</div>
```

### Example with nested grids

```HTML
<div class="mg_49">
  <div class="mmg_48">[ Nested grid element with smaller mobile break width (mm) ]</div>
  <div class="mmg_4">[ 4% width margin (note: it's 4% of the parent's 48% of the total ]</div>
  <div class="mmg_48">[ Nested grid element with smaller mobile break width (mm) ]</div>
  <div style="clear:both">[ Clearing element ]</div>
</div>
<div class="mg_2"></div>
<div class="mg_49"></div>
<div style="clear:both"></div>
```
