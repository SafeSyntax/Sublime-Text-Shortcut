
## Installation

1.To install, copy the Python code for Sublime Text 3 found here. Click View > Show Console to open the ST3 console. Paste the code into the console. Press enter. Reboot ST3.

2.You can now install packages by using the keyboard shortcut ctrl+shift+P or Click Preferences > Package Control. Start typing install until 
Package Control: Install Package 
appears. Press enter and search for available packages.


3.Some other relevant commands are:

	List Packages shows all your installed packages
	Remove Packages removes a specific package
	Upgrade Package upgrades a specific package
	Upgrade/Overwrite All Packages upgrades all your installed packages
	Check out the official documentation to view more commands.

Then write emmet





How to install:
The preferred way to install Emmet is to use Package Control:

Open Command Palette in Sublime Text
Pick “Install Package” command
Find and install “Emmet” plugin




# Sublime Text 3 - Useful Keyboard Shortcuts (Windows)

## General

| Shortcut | Description |
| ---------| ----------- |
| <kbd>Ctrl</kbd>+<kbd>P</kbd> | go to file |
| <kbd>Ctrl</kbd>+<kbd>G</kbd> | go to line |
| <kbd>Ctrl</kbd>+<kbd>R</kbd> | go to methods |
| <kbd>Ctrl</kbd>+<kbd>K</kbd><kbd>B</kbd> | toggle side bar |
| <kbd>Ctrl</kbd>+<kbd>N</kbd> | new tab |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>N</kbd> | new window |

## Editing

| Shortcut | Description |
| ---------| ----------- |
| <kbd>Ctrl</kbd>+<kbd>L</kbd> | select line (repeat select next lines) |
| <kbd>Ctrl</kbd>+<kbd>D</kbd> | select word (repeat select others occurrences in context for multiple editing) |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Enter</kbd> | insert line before |
| <kbd>Ctrl</kbd>+<kbd>Enter</kbd> | inter line after |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>K</kbd> | delete line |
| <kbd>Ctrl</kbd>+<kbd>K</kbd><kbd>K</kbd> | delete from cursor to end of line |
| <kbd>Ctrl</kbd>+<kbd>K</kbd><kbd>Backspace</kbd> | delete from cursor to start of line |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>D</kbd> | duplicate line(s) |
| <kbd>Ctrl</kbd>+<kbd>K</kbd><kbd>U</kbd> | upper case |
| <kbd>Ctrl</kbd>+<kbd>K</kbd><kbd>L</kbd> | lower case |
| <kbd>Ctrl</kbd>+<kbd>/</kbd> | comment line |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>/</kbd> | block comment |
| <kbd>Ctrl</kbd>+<kbd>Y</kbd> | redo or repeat |
| <kbd>Ctrl</kbd>+<kbd>C</kbd> | copy |
| <kbd>Ctrl</kbd>+<kbd>V</kbd> | paste |
| <kbd>Ctrl</kbd>+<kbd>X</kbd> | cut |
| <kbd>Ctrl</kbd>+<kbd>Y</kbd> | redo or repeat |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>V</kbd> | paste and ident |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>L</kbd> | splits the selection into multiple selections |
| ** | 
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>F</kbd> | Put the words, sentence, or line of codes that you want to change in the Find field. |
| { "keys": ["ctrl+alt+shift+s"], "command": "save_all" }, | for “save all” -> Preferences -> Key Bindings -> Default. Paste this on a new line, right above the last closing square bracket: |


## Find / Replace

| Shortcut | Description |
| ---------| ----------- |
| <kbd>Ctrl</kbd>+<kbd>F</kbd> | find |
| <kbd>Ctrl</kbd>+<kbd>I</kbd> | incremental find |
| <kbd>Ctrl</kbd>+<kbd>H</kbd> | replace |
| <kbd>Ctrl</kbd>+<kbd>F3</kbd> | find next occurrence of current word |
| <kbd>Alt</kbd>+<kbd>F3</kbd> | select all occurrences of current word for multiple editing |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>F</kbd> | find in files |


## Quick way to code at Sublime Text

| Shortcut | Description |
| ---------| ----------- |
| <kbd>Ctrl</kbd>+<kbd>F</kbd> | find |
| <kbd>Ctrl</kbd>+<kbd>I</kbd> | incremental find |
| <kbd>Ctrl</kbd>+<kbd>H</kbd> | replace |
| <kbd>Ctrl</kbd>+<kbd>F3</kbd> | find next occurrence of current word |
| <kbd>Alt</kbd>+<kbd>F3</kbd> | select all occurrences of current word for multiple editing |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>F</kbd> | find in files |




## Quick way to code at Sublime Text


# for HTML 
Elements
You can use elements’ names like div or p to generate HTML tags. Emmet doesn’t have a predefined set of available tag names, you can write any word and transform it into a tag: div → <div></div>, foo → <foo></foo> and so on.

#### Child: >

div>ul>li
```
<div>
    <ul>
        <li></li>
    </ul>
</div>
```

#### Sibling: +

div+p+bq

<div></div>
<p></p>
<blockquote></blockquote>

div+div>p>span+em 
```
<div></div>
<div>
    <p><span></span><em></em></p>
</div>
```


#### Climb-up: ^

With ^ operator, you can climb one level up the tree and change context where following elements should appear:

div+div>p>span+em^bq
```
<div></div>
<div>
    <p><span></span><em></em></p>
    <blockquote></blockquote>
</div>
```

You can use as many ^ operators as you like, each operator will move one level up:

div+div>p>span+em^^^bq
```
<div></div>
<div>
    <p><span></span><em></em></p>
</div>
<blockquote></blockquote>
```

#### Multiplication: *

ul>li*5
...outputs to
```
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

#### Grouping: ()

div>(header>ul>li*2>a)+footer>p
```
<div>
    <header>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </header>
    <footer>
        <p></p>
    </footer>
</div>
```

(div>dl>(dt+dd)*3)+footer>p
```
<div>
    <dl>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
    </dl>
</div>
<footer>
    <p></p>
</footer>
```

#### ID and CLASS

div#header+div.page+div#footer.class1.class2.class3
```
<div id="header"></div>
<div class="page"></div>
<div id="footer" class="class1 class2 class3"></div>
```
Custom attributes

td[title="Hello world!" colspan=3]
```
<td title="Hello world!" colspan="3"></td>
```
Note:  
You can use single or double quotes for quoting attribute values.
You don’t need to quote values if they don’t contain spaces: td[title=hello colspan=3] will work.

#### Item numbering: $

ul>li.item$*5
```
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
</ul>
```
You can use multiple $ in a row to pad number with zeroes:

ul>li.item$$$*5
```
<ul>
    <li class="item001"></li>
    <li class="item002"></li>
    <li class="item003"></li>
    <li class="item004"></li>
    <li class="item005"></li>
</ul>
```
Changing numbering base and direction
With @ modifier, you can change numbering direction (ascending or descending) and base (e.g. start value).

For example, to change direction, add @- after $:

ul>li.item$@-*5
```
<ul>
    <li class="item5"></li>
    <li class="item4"></li>
    <li class="item3"></li>
    <li class="item2"></li>
    <li class="item1"></li>
</ul>
```



ul>li.item$@3*5
…transforms to
```
<ul>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
    <li class="item6"></li>
    <li class="item7"></li>
</ul>
```
You can use these modifiers together:

ul>li.item$@-3*5
…is transformed to
```
<ul>
    <li class="item7"></li>
    <li class="item6"></li>
    <li class="item5"></li>
    <li class="item4"></li>
    <li class="item3"></li>
</ul>
```

splits the selection into multiple selections

# for CSS

p
```
padding: ;
```

p0
```
padding: 0;
```

m0+p0
```
margin: 0;
padding: 0;
```

tac
```
text-align: center;
```

bgc
```
background-color: #fff;
```

bgc#fcf
```
background-color: #fcf;
```

ff
```
font-family: ;
```

ffa
```
font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
```

@i
```
@import url();
```

@f+
```
@font-face {
	font-family: 'FontName';
	src: url('FileName.eot');
	src: url('FileName.eot?#iefix') format('embedded-opentype'),
		 url('FileName.woff') format('woff'),
		 url('FileName.ttf') format('truetype'),
		 url('FileName.svg#FontName') format('svg');
	font-style: normal;
	font-weight: normal;
}
```

-transform
```
-webkit-transform: ;
-ms-transform: ;
-o-transform: ;
transform: ;
```

-transition
```
-webkit-transition: ;
-o-transition: ;
transition: ;
```

-wmso-transition
```
-webkit-transition: ;
-moz-transition: ;
-ms-transition: ;
-o-transition: ;
transition: ;
```


# for Snippets 

<kbd>go to Tools</kbd> <kbd>Developers</kbd> <kbd>New Snippet</kbd> 

```
Then

<snippet>
    <content><![CDATA[Type your snippet here]]></content>
    <!-- Optional: Tab trigger to activate the snippet -->
    <tabTrigger>xyzzy</tabTrigger>
    <!-- Optional: Scope the tab trigger will be active in -->
    <scope>source.python</scope>
    <!-- Optional: Description to show in the menu -->
    <description>My Fancy Snippet</description>
</snippet>

```


#### credit 
[Safe Syntax](http://safesyntax.com)  
[Safe Syntax - Youtube](https://www.youtube.com/safesyntax)  
[G M Mostakim Billah Rasel - Youtube](https://www.youtube.com/gmmostakimbillah/)  
[mrliptontea](https://gist.github.com/mrliptontea/4c793ebdf72ed145bcbf)














