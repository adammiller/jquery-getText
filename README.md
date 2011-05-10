jQuery getText
=================

Utility for pulling strings from the DOM

Useful for placing all localized strings in templates, and accessing them in javascript


License
-------

http://unlicense.org/ - i.e. do what you want with it :-)

Usage
-----

Put your translations into the DOM inside of a containing div with the class 'translated-strings'. Strings placed in an ordered list are loaded into an array.

	<div class="translated-strings" style="display:none;">
	 <span id="msg-hello-world">Hello World!</span>
	 <ol id="alphabet">
	  <li>A</li>
	  <li>B</li>
	  <li>C</li>
	  <li>D</li>
	  <li>E</li>
	  <li>F</li>
	 </ol>
	</div>

By including jquery.getText.js, the strings in .translated-strings will be parsed on document.ready. After they've been processed you can access them using the shortcut function. 

	$._( key, index ); 
	
The key is mandatory, and is a direct reference to the id of the element in .translated-strings. Index is optional and is used for accessing strings in ordered lists. 
	
Examples
--------


	$._( 'msg-hello-word' ) // "Hello World!"
	$._( 'msg-alphabet', 3 )  // "D"
	
