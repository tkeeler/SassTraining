# Variables

Sass supports the use of variables by prefixing the variable name with `$`.

	$widget-width: 50px
	
	.widget {
		width: $widget-width;
	}

## Scope

Variables are only available within the level of nested selectors where they’re defined. If they’re defined outside of any nested selectors, they’re available everywhere. They can also be defined with the `!global` flag, in which case they’re also available everywhere. For example:

	#main {
		$width: 5em !global;
		width: $width;
	}
	
	#sidebar {
		width: $width;
	}

When compiled both #main and #sidebar will have a width of 5em.

## Variable Defaults: !default

You can assign to variables if they aren’t already assigned by adding the !default flag to the end of the value. This means that if the variable has already been assigned to, it won’t be re-assigned, but if it doesn’t have a value yet, it will be given one.

For example:

	$content: "First content";
	$content: "Second content?" !default;
	$new_content: "First time reference" !default;
	
	#main {
		content: $content;
		new-content: $new_content;
	}


is compiled to:

	#main {
		content: "First content";
		new-content: "First time reference"; 
	}


Variables with null values are treated as unassigned by !default:

	$content: null;
	$content: "Non-null content" !default;
	
	#main {
		content: $content;
	}

is compiled to:

	#main {
  	content: "Non-null content"; 
	}	
	
all content taken from http://sass-lang.com/documentation/file.SASS_REFERENCE.html


## Exercies
1. Copy your scss file from exercies 1
1. Refactor using variables as you see fit.
1. Recompile
1. Inspect output
1. Point the css link in `index.html` to your output
1. Verify nothing changed 

