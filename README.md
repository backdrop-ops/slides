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
2. Copy an existing slide deck (e.g. index.html) from the root of this repository and give it an appropriate file name
3. Make sure you update the `<title>` tag, and feel free to look in other presentations or `reveal.js/index.html` for code examples
4. For any images, downloads, or special assets, create a new folder in the `assets` folder, and give it the same name as your `.html` file.
5. If you have any problems, questions, feature requests reach out to us using any of the methods at the end of the `index.html` deck.


### Contributing back
If you'd like to share your presentation back with the community, please submit a pull request from your fork against the master branch.


Style additions/modifications we made to Reveal.js
--------------------------------------------------
### Better fonts, spacing and additional styling of common elements
Readability++ 

### Equal width columns
Add a wrapper element with a class of `flex-wrapper` it will make all children elements equal width. It is using flexbox, see <a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox">CSS-Tricks' Guide to Flexbox</a> for help on adding custom styles to further affect how that lays out.

### Custom Styled Reveal Controls
Prettiness++


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
