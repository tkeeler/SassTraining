#CSS Extended: Sass Basics 

##Topics
  What is Sass?
  Getting Started
  Sass Basics
  
###What is Sass? (3-5)
  Syntatically Awesome Style Sheets (no seriously)
    "Sass is the most mature, stable, and powerful professional grade CSS extension language in the world."
    
  Sass is an extension language 
  
##Getting Started (10-15 min)
  Installing Sass
  I recommnd the Command Line Interface as it allows for integration with other tools
    http://sass-lang.com/install
    
    For Windows users
      http://rubyinstaller.org/
      Then
      Open Cmd Prompt
      >_ gem install sass
      >_ sass -v
      
##Sass Basics (40-45 min)
  We will be working on a set of buttons.
  We will start with pure CSS and convert it to Sass.
  
  Preprocessing
   Explaination of entire process
   Create  all.scss file and note destination for CSS
   Demo CSS file
   Cut contents over to all.scss file and demo it still works
  Variables
    Create variables from existing CSS
    Note use of !default
  Nesting
    Move :hover and other states into parent classes
  Partials
    Move buttons out into _buttons.scss
  Import
    Note that buttons no longer have style
    Import buttons in to all.scss
  Mixins
    create button mixin
    Demo the fact that a mixin will not work without being called
    Import mixin for each button type
  Inheritance
    ?
  Operators
    Add different sized buttons
  