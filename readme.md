
# ABOUT THIS DOCUMENT

This document contains examples of all possible markdown styling supported by GitHub.

# HEADERS


# Header1
## Header2
### Header 3
#### Header 4

# EMPHASIS

This is *Italic*

This is _also Italic_

This is **Bold**

This is __also Bold__

*You **can** combine the two*

~~This is strikethrough~~

# LISTS

##Simple unordered list:

* Bullet One
* Bullet Two

##Nested unordered  list:

* Bullet One
  * Nested Bullet One
  * Nested Bullet two
* Bullet Two

##Simple ordered list

1. Item One
2. Item Two


##Nested ordered list

1. Item One
   1. Sub-Item One
   2. Sub-Item Two
2. Item Two

##Combined ordered and unordered

1. Item One
2. Item Two
3. Item Three
   * Bullet One
   * Bullet Two

# INSERTING IMAGES


![Darfield](http://project-nerd.com/wp-content/uploads/2012/12/Garfield-Dalek.jpg)

**Tip:** for this to work properly, provide the full path to your image in Github.

# QUOTES AND CODE 

## Block Quotes

> Bacon ipsum dolor sit amet tail short loin shank ham capicola. Ground round cow corned beef prosciutto. Tail venison kielbasa ground round boudin short ribs biltong hamburger spare ribs jerky. Brisket tenderloin flank shankle andouille hamburger.

> Corned beef tri-tip capicola, pork chuck bresaola brisket frankfurter boudin pork chop meatball. Sirloin filet mignon short ribs meatloaf chicken turkey ground round jerky ham tenderloin. Salami hamburger pork chop pork kielbasa ground round corned beef ribeye, fatback shank andouille meatball. Meatloaf frankfurter brisket andouille turducken pork chop swine doner beef ribs spare ribs pork belly. Capicola shoulder brisket, landjaeger swine doner chuck boudin kielbasa turducken bresaola rump. Sirloin porchetta flank fatback, filet mignon tail pig bacon. Pork drumstick jerky, salami ground round shankle andouille ball tip tri-tip spare ribs flank bacon short loin meatball fatback.

## Code 

### Without Syntax Highlighting

```
function test() {
  console.log("notice the blank line before this function?");
}
```

### With Syntax Highlighting

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

# TABLES

You can create tables by assembling a list of words and dividing them with hyphens - (for the first row), and then separating each column with a pipe |:


First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

For aesthetic purposes, you can also add extra pipes on the ends:


| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

Note that the dashes at the top don't need to match the length of the header text exactly:

| Name | Description          |
| ------------- | ----------- |
| Help      | Display the help window.|
| Close     | Closes a window     |

You can also include inline Markdown such as links, bold, italics, or strikethrough:

| Name | Description          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

Finally, by including colons : within the header row, you can define text to be left-aligned, right-aligned, or center-aligned:

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

A colon on the left-most side indicates a left-aligned column; a colon on the right-most side indicates a right-aligned column; a colon on both sides indicates a center-aligned column.

# URL LINKS

Complete syntax

[Visit GitHub!](http://www.github.com)

Github also auto-formats a link if it recognizes a URL as such:

http://www.github.com