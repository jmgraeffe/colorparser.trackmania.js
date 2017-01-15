# Trackmania Color Parser
Trackmania Color Parser in Javascript is a port of [the original TMFColorParser](http://www.tm-forum.com/viewtopic.php?t=14924) written in PHP by f*ckfish, a programmer who contributed a lot of stuff to the Trackmania community in general.

It converts (or translates) strings including Trackmania codes [like this ones](http://trackmaniaz.page.tl/Colored-Text.htm) into valid HTML code, so stylized phrases from Trackmania can be displayed on websites. This could be very useful for web statistics, for example.

##Demo
Because it's client-side only, you can just view [the index.html on github.io](https://j0nnib0y.github.io/trackmania-colorparser/).

##Features
- client-side parsing 
- supports all Trackmania formatting codes
- converts links and manialinks
- automatic shadowing

##Usage
At first you've to implement the script into your web site. Just upload the Javascript files and add the following line right before the body closing tag:

    <script src="trackmania-colorparser.js"></script>
Now you can use the library in your own scripts. The most important function is:

	COLORPARSER.toHTML(string[, stripColors = false, stripLinks = false, stripTags = '', replaceWhitespace = true]);
As you can see, the only important parameter is basically the string which you want to convert to HTML code.

##Function reference
- `COLORPARSER.toHTML`
Parameters:
  - `string string` (the text you want to convert to HTML; required)
  - `bool stripColors = false` (if you want to deactivate color codes completely; optional)
  - `bool stripLinks = false` (if you want to deactivate link codes completely; optional)
  - `string stripTags = ''` (type in codes seperated by nothing to deactivate some codes, or just 'all'; optional)
- `COLORPARSER.setShadowing`
	Parameters:
	- `bool enabled = false` (if you want to use automatic shadow, see demos)
- `COLORPARSER.setGame`
	Parameters:
	- `string game = 'TMF'` (`'TMF', 'MP', 'TM2'`)

##Contributing
If you've any ideas or wishes, e. g. implementing functions from the original version which are missing in my version, just feel free to ask or just code it by yourself and make a pull request here. Thanks! ;-)

**Things which could be implemented sometime:**

- automatic color correction like the one in the PHP version
- HTML to Trackmania styled text
- ...

##Thanks to
- F*ckfish, for the awesome PHP library
- Stackoverflow as always
- w3schools.com
