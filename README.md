# Elm snippets for Sublime Text 2 and 3
#### [Sublime Text 3](http://www.sublimetext.com/3)

## About
This is a Sublime Text 2 and 3 plugin allowing you to use Elm specific snippets in Elm source files. 

## Installation
First of all, be sure you have [Elm](http://elm-lang.org/install) installed. Other useful Elm related packages are "Elm Language Support" and "SublimeLinter-contrib-elm-make". After you've installed Elm and the Elm related packages, you will need to setup this plugin.
Each OS has a different `Packages` folder required by Sublime Text. Open it via Preferences -> Browse Packages, and copy this repository contents to the `elm_snippets` folder there.

The shorter way of doing this is:

### Through [Sublime Package Manager](http://wbond.net/sublime_packages/package_control)

* `Ctrl+Shift+P` or `Cmd+Shift+P` in Linux/Windows/OS X
* type `install`, select `Package Control: Install Package`
* type `elm_snippets`, select `elm_snippets`

### Manually
Make sure you use the right Sublime Text folder. For example, on OS X, packages for version 2 are in `~/Library/Application\ Support/Sublime\ Text\ 2`, while version 3 is labeled `~/Library/Application\ Support/Sublime\ Text\ 3`.


These are for Sublime Text 3:

#### Mac
`git clone https://github.com/rudolfb/elm_snippets ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/elm_snippets`

#### Linux
`git clone https://github.com/victorporof/elm_snippets ~/.config/sublime-text-3/Packages/elm_snippets`

#### Windows
`git clone https://github.com/victorporof/elm_snippets %APPDATA%/Sublime\ Text\ 3/Packages/elm_snippets`

## Usage
Type the snippet shortcode and then press <kbd>Tab</kbd> to complete the snippet.

Some snippets have more than one place holder. When the snippet is first displayed, the cursor is placed at the first place holder. After entering the text here, press tab to go to the next place holder. If there are no further place holders the cursor will jump to the end of the snippet.

## Snippets

__cof__

```elm
case $1 of
	$2 ->
		$3
```

```elm
  case action of
    Increase ->
      { model | count = model.count + 1 }
```      

__imp__

```elm
import $1
```

```elm
import Mouse
```

__impas__

```elm
import $1 as $2
```

```elm
import Html.Events as Events
```

__impea__

```elm
import $1 exposing (..)
```

```elm
import Html exposing (..)
```

__impes__

```elm
import $1 exposing ($2)
```

```elm
import Html exposing (Html)
```

__mod__

```elm
module $1 (..) where
$0
```

Pressing <kbd>Tab</kbd> after entering the module name will automatically position the cursor on the start of the next line.

```elm
module Main (..) where
```

__sig__

```elm
Signal
```

__siga__

```elm
Signal.Address 
```

A space is automatically appended to the string and the cursor placed after the trailing space.

__sigma__

```elm
Signal.map ($1) $2
```

```elm
Signal.map (view mb.address) modelSignal
```

__sigmb__

```elm
Signal.mailbox ""
```

__sigs__

```elm
Signal.Signal
```

__str__

```elm
String
```

__ta__

```elm
type alias $1 =
	$2
$0
```

__type__

```elm
type $1
	= $2
$0
```

__let__

```elm
let
	$1 =
		$2
in
	$3
```

Pressing <kbd>Tab</kbd> after entering the alias name will automatically position the cursor indented on the next line, and you can enter the alias definition.
Pressing <kbd>Tab</kbd> after entering the alias definition will automatically position the cursor on the start of the next line.

```elm
type alias Model =
  { count : Int }
```


## Contributing
Use these snippets as you please. I only ask that if you come up with an incredibly handy snippet, or simply one that I have missed, that you let me know via GitHub so that I can improve these for everybody. Thanks!

## Thanks
These snippets are based on a similar Atom project [atom-elm-snippets](https://github.com/chiefGui/atom-elm-snippets)

The Sublime [HTML-Snippets](https://github.com/joshnh/HTML-Snippets) package served as the template for this package.

Thank you!
