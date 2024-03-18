<h1>Website Case Study - JavaJam Coffee Bar</h1>

Web Development and Design Foundations with Html5 by Terry Felke-Morris, 10th Edition (pages 293 - 297)<br>
<p>Submit the following files:<br>
javajam.css, index.html, menu.html, music.html</p>

<h3>JavaJam Coffee Bar</h3>
<p>See Chapter 2 for an introduction to the JavaJam Coffee Bar case study.<br>
Figure 2.32 shows a site map for the JavaJam.</p>

<p>In this case study, you will implement a new two-column CSS page layout for JavaJam.<br>
Figure 6.54 shows a wireframe for a two-column page layout with wrapper, header, navigation, main content, hero image, and footer areas.
</p>

<h3>Tasks Overview</h3>
<p>You will modify the external style sheet and the Home, Menu, and Music pages.<br> 
Use the Chapter 4 JavaJam website as a starting point for this case study.</p>

<strong>You have five tasks in this case study:</strong>
<ol>
<li>Create a new folder for this JavaJam case study.</li>
<li>Modify the style rules in the javajam.css file to configure a two-column page layout, as shown in Figure 6.54.</li>
<li>Modify the Home page to implement the two-column page layout, as shown in Figure 6.55.</li>
<li>Modify the Menu page (Figure 6.56) to be consistent with the Home page.</li>
<li>Modify the Music page (Figure 6.57) to be consistent with the Home page.</li>
</ol>

Fig6_54.png
Fig6_55.png
Fig6_56.png
FIg6_57.png

<h2>Hands-On Practice Case</h2>

<h3>TASK 1: THE WEBSITE FOLDER.</h3>
<p>You will modify the javajam.css file and each web page file<br>
(index.html, menu.html, and music.html)<br>
to implement the two-column page layout shown in Figure 6.54.<br> 
See the new JavaJam Home page, as shown in Figure 6.55.
</p>

<ol>
<li>Create a folder called javajam6.</li>
<li>Copy all of the files from your Chapter 4 javajam4 folder into the javajam6 folder.</li> 
<li>Copy all of the files from the chapter6/starters/javajam folder.</li> 
</ol>

<h3>TASK 2: CONFIGURE THE CSS.</h3>
<p>Open javajam.css in a text editor.<br>
Edit the style rules as follows:</p>
<ol>
<li>Configure the universal selector with a box-sizing: border-box style declaration.
<code>* { box-sizing: border-box; }</code>
</li>
<li>Configure styles for the <code>hero image</code> on each page:
  <ul>
    <li>a. Configure styles for the id selector named <code>homehero</code>.<br> 
      Set <code>background-size to 100% 100%</code>.</li>
    <li>b. Configure an id selector named <code>heromugs</code>.<br>
      Configure the styles similar to the homehero id.<br>
      Set the <code>background image to heromugs.jpg</code>.</li>
    <li>c. Configure an id selector named <code>heroguitar</code>.<br>
      Configure the styles similar to the homehero id.<br>
      Set the <code>background image to heroguitar.jpg</code>.</li>
  </ul>
</li>
<li>Edit the style rules for the <code>main</code> selector.<br>
  Change <code>left padding to 0</code>. Change <code>right padding to 0</code>.<br>
  Also configure a <code>200px left margin</code>, <code>0 top padding</code>, and <code>#FEF6C2 background color</code>.<br>
  To allow for the main element to contain floated elements, set <code>overflow to auto</code>.
</li>
<li>Since the main content area no longer has any left or right padding,<br>
  configure descendant selectors to configure style rules for the following elements<br>
  within the <code>main</code> element: <code>h2, h3, h4, p, div, ul, dl</code>.<br> 
  Set <code>left padding to 3em</code> and <code>right padding to 2em</code>.
</li>
<li>Configure the left-column navigation area.<br> 
  Add style declarations to the <code>nav</code> element selector to configure an area that <code>floats to the left and is 200 pixels wide</code>.
</li>
<li>Configure the <code>:link, :visited, and :hover</code> pseudo-classes for the navigation hyperlinks.<br>
  Use the following <code>text colors</code>: <code>#FEF6C2 (unvisited hyperlinks)</code>, <code>#D2B48C (visited hyperlinks)</code>, and <code>#CC9933 (hyperlinks with :hover)</code>.<br>
  For example, <code>nav a:link { color: #FEF6C2; }</code>
</li>
<li>You will organize the navigation hyperlinks within an unordered list in later tasks.<br>
  The navigation area in Figure 6.55 does not show list markers.<br>
  Code a <code>nav ul</code> descendant selector to configure unordered lists in the navigation area to <code>display without list markers</code> and with <code>0 left padding</code>.
</li>
<li>Modify the <code>wrapper</code> id.<br>
  Configure a dark <code>background color (#231814)</code> which will display behind the column with the navigation area. 
  Also set <code>padding to 0</code>.
</li>
<li>Modify the <code>header</code> element selector style rules.<br>
  Remove the declaration for <code>text-align</code>.<br>
  Set the <code>background image to coffeelogo.jpg</code>.<br>
  Configure this <code>image to not repeat</code>.<br> 
  Set <code>left padding to 240px</code>.<br>
  Change the <code>text color to #231814</code>.
</li>
<li>Modify the <code>h4</code> element selector style rules.<br>
  View the Music page shown in Figure 6.57 and notice that the <code>&lt;h4&gt;</code> tags are styled differently,<br>
    with all <code>uppercase</code> text (use <code>text-transform</code>), a <code>bottom border</code>, and <code>0 bottom padding</code>.<br>
    Also configure a style declaration to <code>clear floats on the left</code>.
</li>
<li>Refer to the Music page shown in Figure 6.57<br> 
  and notice how the images float on the left side of the paragraph description.<br>
  Configure a new class named <code>floatleft that floats to the left</code> with <code>2em of right and bottom padding</code>.
</li>
<li>Modify the style rules for the <code>details</code> class and add the <code>overflow: auto;</code> style declaration.
</li>
<li>Configure a style rule for a class named <code>onethird</code>.<br> 
  Set <code>left float</code> and <code>33% width</code>.
</li>
<li>Configure hyperlinks in the <code>header</code> area.<br> 
  Use descendant selectors to configure <code>hyperlinks</code> within the header element with <code>no underline</code>,<br> 
  dark brown <code>(#231814) text color</code> for the <code>:link</code> and <code>:visited</code> pseudo-classes,<br> 
  and rust <code>(#FEF6C2) text color</code> for the <code>:hover</code> pseudo-class.
</li>
</ol>
Save the javajam.css file.

<h3>TASK 3: THE HOME PAGE.</h3> 
<p>Open index.html in a text editor.<br>
Edit the code as follows:</p>
<ol>
  <li>Configure the “JavaJam Coffee Bart” text in the header area to be a <code>hyperlink</code> to the Home page (<code>index.html</code>).
  </li>
<li>Configure the left-column navigation area, which is contained within the <code>nav</code> element. Remove any <code>&amp;nbsp;</code> characters that may be present.<br> 
  Code an <code>unordered list</code> to organize the <code>navigation hyperlinks</code>.<br> 
  Each hyperlink should be contained within <code>&lt;li&gt;</code> tags.
</li>
<li>Move the div assigned to the id <code>homehero inside the main</code> element as indicated in the Figure 6.54 wireframe.
</li>
</ol>

<p>Save the index.html file.<br> 
  It should look similar to the web page shown in Figure 6.55.<br> 
  Remember that validating your HTML and CSS can help you find syntax errors.<br> 
  Test and correct this page before you continue.
</p>

<h3>TASK 4: THE MENU PAGE.</h3> 
Open menu.html in a text editor.
<ol>
  <li>Configure the header area and the left-column navigation area hyperlinks in the same manner as the home page.</li>
  <li>Remove the img tag for the mugs.jpg image.<br> 
    Configure a div element assigned to the heromugs id between the opening main tag and the opening h2 tag.</li>
  <li>Observe Figure 6.56 and note that the menu information is formatted in three columns.<br> 
    Remove the tags that configure the description list from the page.<br>
    Also remove the strong tags coded within the description list.<br>
    Notice the text content is a series of menu item names and descriptions.<br> 
    Configure each menu item name within an h3 element.<br> 
    Configure each menu item description within a paragraph element.<br> 
    Code a section element to contain each menu item name and menu item description pair.<br>
    Assign each section element to the CSS class named onethird.
</li>
</ol>

<p>Save your new menu.html page and test it in a browser.<br> 
It should look similar to the web page shown in Figure 6.56.<br> 
Use the CSS and HTML validators to help you find syntax errors.<br> 
Edit the page and add line break tags so that each price is on its own line.<br> 
Save and test again.
</p>

Fig6_56.png

<h3>TASK 5: THE MUSIC PAGE.</h3> 
Open music.html in a text editor.
<ol>
  <li>Configure the header area and the left-column navigation area hyperlinks in the same manner as the home page.</li>
  <li>Configure a div element assigned to the heroguitar id between the opening main tag and the opening h2 tag.</li>
  <li>Configure the thumbnail images to float to the left.<br> 
    Add class="floatleft" to the img tag for each thumbnail image.</li>
</ol>

<p>Save your new music.html page and test it in a browser.<br>
It should look similar to the web page shown in Figure 6.57.<br> 
Use the CSS and HTML validators to help you find syntax errors.</p>

FIg6_57.png
<hr>
<p>In this case study, you changed the page layout of the JavaJam website.<br> 
Notice that with just a few changes in the CSS and HTML code, you configured a two-column page layout.</p>
