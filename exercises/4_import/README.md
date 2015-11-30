# Importing
> Sass supports all CSS3 @-rules, as well as some additional Sass-specific ones known as “directives.” These have various effects in Sass, detailed below. See also control directives and mixin directives.

> ## @import

> Sass extends the CSS @import rule to allow it to import SCSS and Sass files. All imported SCSS and Sass files will be merged together into a single CSS output file. In addition, any variables or mixins defined in imported files can be used in the main file.

>Sass looks for other Sass files in the current directory, and the Sass file directory under Rack, Rails, or Merb. Additional search directories may be specified using the :load_paths option, or the --load-path option on the command line.

> @import takes a filename to import. By default, it looks for a Sass file to import directly, but there are a few circumstances under which it will compile to a CSS @import rule:

> * If the file’s extension is .css.
> * If the filename begins with http://.
> * If the filename is a url().
> * If the @import has any media queries.
> If none of the above conditions are met and the extension is .scss or .sass, then the named Sass or SCSS file will be imported. If there is no extension, Sass will try to find a file with that name and the .scss or .sass extension and import it.

> For example,

> `@import "foo.scss";`

> or

> `@import "foo";`

> would both import the file foo.scss, whereas

> `@import "foo.css";`<br>
> `@import "foo" screen;`<br>
> `@import "http://foo.com/bar";`<br>
> `@import url(foo);`

> would all compile to

> `@import "foo.css";`<br>
> `@import "foo" screen;`<br>
> `@import "http://foo.com/bar";`<br>
> `@import url(foo);`

> It’s also possible to import multiple files in one @import. For example:

> `@import "rounded-corners", "text-shadow";`
> would import both the rounded-corners and the text-shadow files.

> Imports may contain #{} interpolation, but only with certain restrictions. It’s not possible to dynamically import a Sass file based on a variable; interpolation is only for CSS imports. As such, it only works with url() imports. For example:

> `$family: unquote("Droid+Sans");`
> `@import url("http://fonts.googleapis.com/css?family=#{$family}");`
would compile to

> `@import url("http://fonts.googleapis.com/css?family=Droid+Sans");`

Basically `@import` is what make partials work.
Also of note is that `@import` can use a realtive path.
For example:
Assume the following folder structure
root/
|--theme/
|  |-main.scss
|  |-_base.scss
|  |--module/
|     |-_thing.scss
|--globals.scss


In main.scss you would import _partial.scss and _thing.scss with the following.

	@import '../globals'
	@import 'base' //or @import './base'
	@import 'module/thing'
	
## Tips, Tricks, and Pitfalls
Partials can have their own @imports.

Assume main imports _partial1 and _partial2
Assume _partial1 imports _partial2 and _partial3
Note that whatever is in _partial2 will be duplicated
	
## Exercise
1. Copy your scss file from the previous file
1. Use @import to get all of your partials into the main file.
1. Recompile
1. Inspect output
1. Point the css link in `index.html` to your output
1. Verify nothing changed 
