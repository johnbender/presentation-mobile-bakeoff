!SLIDE
# jQuery Mobile

johnbender.github.com/presentation-mobile-bakeoff

!SLIDE bullets mono-bullets
## me
* @johnbender
* johnbender.us
* github.com/johnbender

!SLIDE center
<img src="adobe.jpg" style="max-height: 600px"></img>

!SLIDE bullets mono-bullets
* browsers
* markup
* quirks
* access

!SLIDE link
jquerymobile.com/demos/1.0

!SLIDE link highlight
jquerymobile.com/demos/<b>1.0</b>

!SLIDE
# browsers

!SLIDE stats
<img src="mobile-browser-stats.png" style="margin-bottom: 500px"></img>

!SLIDE
## browser support
jquerymobile.com/gbs/

!SLIDE bullets grid
<div style="float: left">
<ul>
  <li> Apple iOS 3.2-5.0 </li>
  <li> Android 2.1-3.1 </li>
  <li> Windows Phone 7-7.5 </li>
  <li> Blackberry 6-7, QNX </li>
  <li> Palm WebOS 1.4-3.0 </li>
</ul>
</div>

<div style="float: left">
<ul>
  <li> Firebox Mobile </li>
  <li> Opera Mobile 11.0 </li>
  <li> Meego 1.2 </li>
  <li> Chrome, Firefox </li>
  <li> IE 7+, Opera 10+ </li>
</ul>
</div>

!SLIDE
# markup

!SLIDE phone
<pre class="xlarge">
&lt;<span class="keyword">!DOCTYPE</span> html&gt;
&lt;<span class="function-name">html</span>&gt;
&lt;<span class="function-name">head</span>&gt;
  &lt;<span class="function-name">meta</span> <span class="variable-name">charset</span>=<span class="string">"utf-8"</span>&gt;
  &lt;<span class="function-name">link</span> <span class="variable-name">rel</span>=<span class="string">"stylesheet"</span> <span class="variable-name">href</span>=<span class="string">"jquery.mobile.css"</span>/&gt;
  &lt;<span class="function-name">script</span> <span class="variable-name">src</span>=<span class="string">"jquery-1.6.4.min.js"</span>&gt;&lt;/<span class="function-name">script</span>&gt;
  &lt;<span class="function-name">script</span> <span class="variable-name">src</span>=<span class="string">"jquery.mobile.js"</span>&gt;&lt;/<span class="function-name">script</span>&gt;
&lt;/<span class="function-name">head</span>&gt;
&lt;<span class="function-name">body</span>&gt;
  &lt;<span class="function-name">div</span> <span class="variable-name">id</span>=<span class="string">"first"</span> <span class="variable-name">data-role</span>=<span class="string">"page"</span>&gt;
    &lt;<span class="function-name">div</span> <span class="variable-name">data-role</span>=<span class="string">"header"</span>&gt;
      &lt;<span class="function-name">h1</span>&gt;<span class="underline"><span class="bold">Sample</span></span>&lt;/<span class="function-name">h1</span>&gt;
    &lt;/<span class="function-name">div</span>&gt;

    &lt;<span class="function-name">div</span> <span class="variable-name">data-role</span>=<span class="string">"content"</span>&gt;
      &lt;<span class="function-name">ul</span> <span class="variable-name">data-role</span>=<span class="string">"listview"</span>&gt;
        &lt;<span class="function-name">li</span>&gt; First List Item &lt;/<span class="function-name">li</span>&gt;
        &lt;<span class="function-name">li</span>&gt; Second List Item &lt;/<span class="function-name">li</span>&gt;
        &lt;<span class="function-name">li</span>&gt;&lt;<span class="function-name">a</span> <span class="variable-name">href</span>=<span class="string">"#embedded"</span>&gt;Link&lt;/<span class="function-name">a</span>&gt;&lt;/<span class="function-name">li</span>&gt;
      &lt;/<span class="function-name">ul</span>&gt;
    &lt;/<span class="function-name">div</span>&gt;
  &lt;/<span class="function-name">div</span>&gt;

  &lt;<span class="function-name">div</span> <span class="variable-name">id</span>=<span class="string">"embedded"</span> <span class="variable-name">data-role</span>=<span class="string">"page"</span>&gt;
    &lt;<span class="function-name">div</span> <span class="variable-name">data-role</span>=<span class="string">"header"</span>&gt;
      &lt;<span class="function-name">a</span> <span class="variable-name">href</span>=<span class="string">"#"</span> <span class="variable-name">data-rel</span>=<span class="string">"back"</span>&gt;Back&lt;/<span class="function-name">a</span>&gt;
      &lt;<span class="function-name">h1</span>&gt;<span class="underline"><span class="bold">Embedded</span></span>&lt;/<span class="function-name">h1</span>&gt;
    &lt;/<span class="function-name">div</span>&gt;
  &lt;/<span class="function-name">div</span>&gt;
&lt;/<span class="function-name">body</span>&gt;
&lt;/<span class="function-name">html</span>&gt;
</pre>

<iframe src="samples/first.html"> </iframe>

!SLIDE phone
<pre class="xlarge">
&lt;<span class="keyword">!DOCTYPE</span> html&gt;
&lt;<span class="function-name">html</span>&gt;
&lt;<span class="function-name">head</span>&gt;
  &lt;<span class="function-name">meta</span> <span class="variable-name">charset</span>=<span class="string">"utf-8"</span>&gt;
&lt;/<span class="function-name">head</span>&gt;
&lt;<span class="function-name">body</span>&gt;
  &lt;<span class="function-name">div</span> <span class="variable-name">id</span>=<span class="string">"first"</span> <span class="variable-name">data-role</span>=<span class="string">"page"</span>&gt;
    &lt;<span class="function-name">div</span> <span class="variable-name">data-role</span>=<span class="string">"header"</span>&gt;
      &lt;<span class="function-name">h1</span>&gt;<span class="underline"><span class="bold">Sample</span></span>&lt;/<span class="function-name">h1</span>&gt;
    &lt;/<span class="function-name">div</span>&gt;

    &lt;<span class="function-name">div</span> <span class="variable-name">data-role</span>=<span class="string">"content"</span>&gt;
      &lt;<span class="function-name">ul</span> <span class="variable-name">data-role</span>=<span class="string">"listview"</span>&gt;
        &lt;<span class="function-name">li</span>&gt; First List Item &lt;/<span class="function-name">li</span>&gt;
        &lt;<span class="function-name">li</span>&gt; Second List Item &lt;/<span class="function-name">li</span>&gt;
        &lt;<span class="function-name">li</span>&gt;&lt;<span class="function-name">a</span> <span class="variable-name">href</span>=<span class="string">"#embedded"</span>&gt;Link&lt;/<span class="function-name">a</span>&gt;&lt;/<span class="function-name">li</span>&gt;
      &lt;/<span class="function-name">ul</span>&gt;
    &lt;/<span class="function-name">div</span>&gt;
  &lt;/<span class="function-name">div</span>&gt;

  &lt;<span class="function-name">div</span> <span class="variable-name">id</span>=<span class="string">"embedded"</span> <span class="variable-name">data-role</span>=<span class="string">"page"</span>&gt;
    &lt;<span class="function-name">div</span> <span class="variable-name">data-role</span>=<span class="string">"header"</span>&gt;
      &lt;<span class="function-name">a</span> <span class="variable-name">href</span>=<span class="string">"#"</span> <span class="variable-name">data-rel</span>=<span class="string">"back"</span>&gt;Back&lt;/<span class="function-name">a</span>&gt;
      &lt;<span class="function-name">h1</span>&gt;<span class="underline"><span class="bold">Embedded</span></span>&lt;/<span class="function-name">h1</span>&gt;
    &lt;/<span class="function-name">div</span>&gt;
  &lt;/<span class="function-name">div</span>&gt;
&lt;/<span class="function-name">body</span>&gt;
&lt;/<span class="function-name">html</span>&gt;
</pre>

<iframe src="samples/without-js.html"> </iframe>

!SLIDE
# quirks

!SLIDE
### quirks ≈ bugs

!SLIDE
### orientationchange

!SLIDE
## (push|replace)State

!SLIDE
### foo.com/#/bar/baz
never forget gizmodo

!SLIDE
### foo.com/bar/baz
after replaceState

!SLIDE
### Chrome/iOS

!SLIDE
### vmouse
<img src="droidincredible.jpg" style="height: 400px; float: left; margin-left: 225px; "></img>
<img src="blackberry-bold.jpg" style="height: 380px; float: left; margin-top: 10px;"></img>

!SLIDE
# accessibility

!SLIDE
## wai-aria
www.w3.org/TR/wai-aria/

!SLIDE
<pre class="xlarge">
&lt;<span class="function-name">div</span> <span class="variable-name">data-role</span>=<span class="string">"fieldcontain"</span>&gt;
  &lt;<span class="function-name">label</span> <span class="variable-name">for</span>=<span class="string">"select-choice-1"</span> <span class="variable-name">class</span>=<span class="string">"select"</span>&gt;
    Choose shipping method:
  &lt;/<span class="function-name">label</span>&gt;
  &lt;<span class="function-name">select</span> <span class="variable-name">name</span>=<span class="string">"select-choice-1"</span> <span class="variable-name">id</span>=<span class="string">"select-choice-1"</span>&gt;
    &lt;<span class="function-name">option</span> <span class="variable-name">value</span>=<span class="string">"standard"</span>&gt;Standard: 7 day&lt;/<span class="function-name">option</span>&gt;
    &lt;<span class="function-name">option</span> <span class="variable-name">value</span>=<span class="string">"rush"</span>&gt;Rush: 3 days&lt;/<span class="function-name">option</span>&gt;
    &lt;<span class="function-name">option</span> <span class="variable-name">value</span>=<span class="string">"express"</span>&gt;Express: next day&lt;/<span class="function-name">option</span>&gt;
    &lt;<span class="function-name">option</span> <span class="variable-name">value</span>=<span class="string">"overnight"</span>&gt;Overnight&lt;/<span class="function-name">option</span>&gt;
  &lt;/<span class="function-name">select</span>&gt;
&lt;/<span class="function-name">div</span>&gt;
</pre>

!SLIDE
