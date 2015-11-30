# Preprocessing

> Sass lets you use features that don't exist in CSS yet like variables, nesting, mixins, inheritance and other nifty goodies that make writing CSS fun again.
> Once you start tinkering with Sass, it will take your preprocessed Sass file and save it as a normal CSS file that you can use in your web site.
> The most direct way to make this happen is in your terminal. Once Sass is installed, you can run sass input.scss output.css from your terminal. You can watch either individual files or entire directories. In addition, you can watch folders or directories with the --watch flag. An example of running Sass while watching an entire directory is the following:
> `sass --watch app/sass:public/stylesheets`
- http://sass-lang.com/guide

Basically Sass is a super set of CSS. You get a few extra features, but it must be compiled first.

So for this exercies
1. Copy the contents of base.css into a file in this folder with the extension .scss
1. Run `sass yourFileNameHere.scss  outputFileName.css`
1. Inspect the output to note if anything changed
1. Point the css link in `index.html` to your output
1. Verify nothing changed 