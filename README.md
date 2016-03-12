Sublime Automatic CSS comments
=========================

Fork of <a href="https://github.com/sc8696/sublime-css-auto-comments">Sublime Automatic CSS comments</a> for KSS.

Using automatic styleguide generation like KSS is all well and good, but typing those comments is a pain!

This sublime plugin will try and figure out all that stuff for you and comment whatever CSS blocks you want. 

<h2>How?</h2>
Just type <code>///</code> followed by <kbd>tab</kbd> directly above the CSS section you want commenting and boom! Done.<br/>
It will also check the rest of your CSS/SCSS/LESS file for related states or attributes and add them as states in the comments too, plus it will give a guess at a suggested markup.

<h2>Install</h2>

<h3>Manual</h3>
Just download this repositry and dump the folder in the Sublime Packages folder

<h2>Example</h2>

Say you have some masterful CSS like this

```css
button{
  background: #006dcc;
  font-size: 18px;
  color: #eee;
  border: 1px solid rgba(0,0,0,0.5);
  border-radius: 3px;
  padding: 10px;
  box-shadow: -3px -21px 21px -9px rgba(0,0,0,0.4) inset;
}
button.active{
  background: maroon;
}

button:disabled{
  background: #aaa;
  color: #777;
}
````

Just do this

```css
///[tab]
button{
  background: #006dcc;
  font-size: 18px;
  color: #eee;
  border: 1px solid rgba(0,0,0,0.5);
  border-radius: 3px;
  padding: 10px;
  box-shadow: -3px -21px 21px -9px rgba(0,0,0,0.4) inset;
}
button.active{
  background: maroon;
}

button:disabled{
  background: #aaa;
  color: #777;
}
````

And magically!


```css
// Button
//
// Style for the button element
//
// .active - active state
// :disabled - disabled state
//
// Markup:
//   <button>markup</button>
//
// Style guide: button
button {
  background: black;
  color: white;
  border-radius: 0.2em;
  padding: 1em;
}

button.active {
  background: maroon;
}

button:disabled {
  background: grey;
  color: black;
}
````

Woo!

Now you can spend less time commenting your stylesheets and more time... writing your stylesheets.

It will also work with nested SCSS/LESS structures

```scss
// Button
//
// Style for the button element
//
// .active - active state
// :disabled - disabled state
//
// Markup:
//   <button>markup</button>
//
// Style guide: button
button {
  background: black;
  color: white;
  border-radius: 0.2em;
  padding: 1em;

	&.active {
		background: maroon;
	}

	&:disabled {
		background: grey;
		color: black;
	}
}
````
