# Partials
> If you have a SCSS or Sass file that you want to import but don’t want to compile to a CSS file, you can add an underscore to the beginning of the filename. This will tell Sass not to compile it to a normal CSS file. You can then import these files without using the underscore.

> For example, you might have _colors.scss. Then no _colors.css file would be created, and you can do

>	`@import "colors";`
> and _colors.scss would be imported.

>Note that you may not include a partial and a non-partial with the same name in the same directory. For example, _colors.scss may not exist alongside colors.scss.

This allows us to break up our large files into smaller, easier to manage files.

## Exercise
1. Copy your scss file from the previous file
1. Break it down to files as you see fit
1. Recompile
1. Inspect output
1. Note that nothing from your partials made it to the output file.
1. Continue to next section.
