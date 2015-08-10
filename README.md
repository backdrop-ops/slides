Introducing Backdrop CMS
========================

A Reveal.js slide deck for a presentation on Backdrop CMS.

Reveal.js Pro-tips
------------------
1. **Use Spacebar to cycle through slides in order**, it will make sure that you don't miss any vertical slides
2. If you're comfortable installing Node.JS you can get a Presenter screen that will show you the next slide, timing, etc.
	1. Install Node.js (Google how to do this for your OS)
	2. In a console run `npm install` from the root of this repo
	3. Run `npm start` to start up the server, leave this running during your presentation
	4. Open up the presentation from http://localhost:8000
	5. Inside of the browser with your presentation, press 's'. This should launch the presenter screen

Making a Presentation
----------------------------
Feel free to fork the repo and create a new/modify an existing deck.

### Creating your own
1. Fork this repository, or if you're not comfortable with Git, download this project as a ZIP
2. Copy an existing slide deck (e.g. index.html or reveal.js/index.html) from the root of this repository and give it an appropriate file name
3. Make sure you update the `<title>` tag, and feel free to look in other presentations or `reveal.js/index.html` for code examples
4. For any images, downloads, or special assets, create a new folder in the `assets` folder, and give it the same name as your `.html` file.
5. If you have any problems, questions, feature requests reach out to us using any of the methods at the end of the `index.html` deck.


### Contributing back
If you'd like to share your presentation back with the community, please submit a pull request from your fork against the master branch.


Style additions/modifications we made to Reveal.js
--------------------------------------------------
### Better fonts, spacing and additional styling of common elements
Readability++

### Code syntax highlighting

The default `highlights.js` highlighting has been replaced with `prism.js` highlighting. By default the following syntaxes have been included:

* Markup (HTML)
* CSS
* JS
* Bash
* Git
* PHP
* JSX
* SCSS
* Twig
* YAML

To use any of these your syntax should look like:
```html
<pre><code class="language-markup">&lt;-- Code goes here --&gt;
&lt;p&gt;It's best to keep your first line of code on the same line as the tag
And to avoid any indenting that you don't want in the presentation.
&lt;/p&gt;</code></pre>
```
Also included are the line-highlight and line number, documentation for those are here:
* http://prismjs.com/plugins/line-highlight/
* http://prismjs.com/plugins/line-numbers/

To replace/augment the languages included you can visit here and download a different file:
http://prismjs.com/download.html?themes=prism&languages=markup+css+clike+javascript+bash+css-extras+git+php+php-extras+jsx+scss+twig+yaml&plugins=line-highlight+line-numbers

The code is in `plugins/prismjs/`.

For any other issues see http://prismjs.com

### Font Awesome
For iconography I've included FontAwesome for it's ease of use and good documentation. Basic syntax is:
```html
<i class="fa fa-star"></i> Here is my star
```
Since it's an icon **font**, use font CSS to manipulate it (`font-size`, `color`, etc).

For more code examples see: http://fortawesome.github.io/Font-Awesome/examples

http://fortawesome.github.io/Font-Awesome

### CSS Helpers

#### Column layout
Resilient equal height and equal width columns.

```html
<div class="column-wrapper">
  <div>Column 1</div>
  <div>Column 2</div>
  <div>Column 3</div>
</div>
```
This is using flexbox, which is not compatible with older browsers, but it has great advantages so I'm using it.

It will automatically make equal width and height columns that add up to 100% of the `.column-wrapper`'s width.

It assumes that all direct descendants of `column-wrapper` are a column, no special classes or markup required.

If you would like to have a column be larger than the others there are two ways to do that:
1. I recommend setting the `flex-grow` property on the column wrappers. By default all columns are `flex-grow: 1`. Flexbox will count all the `flex-grow` numbers and divides each column's value by the total to get each column's width; **UNLESS** the content inside a column is too large, then it will do it's best to accommodate. So in the following example it is calculating flex grows of 2, 1, 1; which will add up to 50%, 25%, 25% columns.
    ```html
    <div class="column-wrapper">
      <div style="flex-grow: 2">Double wide Column 1</div>
      <div>Column 2</div>
      <div>Column 3</div>
    </div>
    ```
2. The other option is explicitly set a width. To do this you will need to set `flex-grow: 0` for any column that has an explicit width. If explicit widths add up to greater than 100% (or the total width in px) it will wrap, but in a nicer and less buggy way than floats.
    ```html
    <div class="column-wrapper">
      <div style="flex-grow: 0; width: 60%;">A 60% wide column</div>
      <div>These will end up being half of what's left over</div>
      <div>What he said ^</div>
    </div>
    ```

The default `column-wrapper` styles are:
```css
display: flex;
align-items: stretch;
flex-wrap: wrap;
margin-bottom: 1em;
```

The default column styles are:
```css
flex-grow: 1;
box-sizing: border-box;
margin-top: 0;
margin-bottom: 0;
```
The margin top and bottom is to override defaults for that container so it lines up with it's sibling columns

For any flexbox questions, go here: https://css-tricks.com/snippets/css/a-guide-to-flexbox

#### File Listings
If you'd like to show off folder/file structure, I've included some styles to help with that. It handles nested folders, and has a nice legible appearance.
```html
<ul class="file-list">
  <li>Folder name</li>
  <li>Folder name
    <ul>
      <li>Nested folder name</li>
      <li>Nested folder name</li>
      <li class="file">Nested file name</li>
    </ul>
  </li>
  <li>Folder name</li>
  <li class="file">File name</li>
</ul>
```


License
-------

This project is distributed under a Creative Commons Public License: Attribution 4.0 International. See the LICENSE.txt file in this directory for complete text.


Slides created by
-----------------

- Jen Lampton (https://github.com/jenlampton)
- Nate Haug (https://github.com/quicksketch)


Image Credits
-------------

Images were stolen freely from the internet.  See the image credits slide the (last one) for a complete list of links.
