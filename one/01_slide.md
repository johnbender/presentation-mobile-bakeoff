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

!SLIDE
# browsers

!SLIDE stats
<img src="mobile-browser-stats.png" style="margin-bottom: 500px"></img>

!SLIDE
a grade browser support

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
### (push|replace)State
looking at you Chrome/iOS

!SLIDE
### vmouse
<img src="droidincredible.jpg" style="height: 400px; float: left; margin-left: 225px; "></img>
<img src="blackberry-bold.jpg" style="height: 380px; float: left; margin-top: 10px;"></img>

!SLIDE
# accessibility

