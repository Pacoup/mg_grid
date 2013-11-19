Mg Grid
=======

Mg Grid is a simple responsive CSS grid layout system. It is entirely percentage-based and can be nested infinitely. Mg Grid is designed to be used on small websites or in conjunction with larger systems when those systems' native grids are not flexible enough.

<h2>How to install</h2>
To install Mg Grid, copy the contents of src.css into your own CSS, preferably at the end of the file.

<h2>How to use</h2>
Mg Grid works by applying a float:left with a given percentage via CSS classes. Upon encountering a certain page width, each grid item will collapse into non-float elements with width:auto at two different sizes; by default, 767px for classes beginning by mg, and 550px for classes beginning by mmg. This can be customized directly in the CSS where the lines read:<br>
<code>@media screen and (max-width: 767px)</code> and<br>
<code>@media screen and (max-width: 550px)</code><br>
although the default configuration will cover most instances where grids are appropriate (see <a href="https://github.com/Pacoup/ti_tester">Ti Tester for more break sizes).

Grid elements can be broken (to create new rows) with a simple clear:both.

Look at the contents of src.css if you want more information. The code should be straight forward enough to grok what's happening.

Note that there is no pre-defined margins. Margins must be made by placing smaller grid elements in between other grid elements.

<h3>Example</h3>

<pre>&lt;div class="mg_49">[ 49% width grid element ]&lt;/div>
&lt;div class="mg_2">[ 2% width margin ]&lt;/div>
&lt;div class="mg_49">[ 49% width grid element ]&lt;/div>
&lt;div style="clear:both">[ Clearing element ]&lt;/div>
</pre>

<h3>Example with nested grids</h3>

<pre>&lt;div class="mg_49">
  &lt;div class="mmg_48">[ Nested grid element with smaller mobile break width (mm) ]&lt;/div>
  &lt;div class="mmg_4">[ 4% width margin (note: it's 4% of the parent's 48% of the total ]&lt;/div>
  &lt;div class="mmg_48">[ Nested grid element with smaller mobile break width (mm) ]&lt;/div>
  &lt;div style="clear:both">[ Clearing element ]&lt;/div>
&lt;/div>
&lt;div class="mg_2">&lt;/div>
&lt;div class="mg_49">&lt;/div>
&lt;div style="clear:both">&lt;/div>
</pre>
