#CSS Extended: Sass Basics 

##Topics
  What is Sass?
  Getting Started
  Sass Basics
  
###What is Sass? (3-5)
  Syntatically Awesome Style Sheets (no seriously)
    "Sass is the most mature, stable, and powerful professional grade CSS extension language in the world."
    
  Sass is a CSS extension language. (Hence the name for the course)
  Sass contiains everything CSS does, plus some new useful feature.
  Noteably:
  1. Variables
  1. Partials
  1. Nesting
  1. Math Operations
  1. Inheritance
  1. Mixins & Functions
  
##Getting Started (10-15 min)
  Installing Sass
  I recommnd the Command Line Interface as it allows for integration with other tools
    http://sass-lang.com/install
    
  For Windows users
    1. http://rubyinstaller.org/
    1. Open Cmd Prompt
    1. >_ gem install sass
    1. >_ sass -v
      
##Sass Basics (40-45 min)
  We will be working on a set of components.
  We will start with pure CSS and step by step convert it to Sass.
  
  Preprocessing
   Since Sass is a compiled language
   Create  all.scss file and note destination for CSS
   Demo CSS file
   Cut contents over to all.scss file and demo it still works
  Variables
    Create variables from existing CSS
    Explain use of !default
    Demo it after Import with /core/_override.scss.
  Partials
    Discuss scss file naming convention.
    Move components into component/_component.scss
    Move core variables into core/_base.scss
  Import
    Note that our css file is empty
    Import components in to all.scss
    Note that order is still important!
    Demo use case for !default
  Nesting
    TBD
  Inheritance
    TBD
  Operators
    TBD
  Mixins
    TBD