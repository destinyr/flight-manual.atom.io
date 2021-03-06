---
title: Converting from TextMate
---
### Converting from TextMate

It's possible that you have themes or grammars from [TextMate](http://macromates.com) that you like and use and would like to convert to Atom. If so, you're in luck because there are tools to help with the conversion.

#### Converting a TextMate Bundle

Converting a TextMate bundle will allow you to use its editor preferences, snippets, and colorization inside Atom.

Let's convert the TextMate bundle for the [R](https://en.wikipedia.org/wiki/R_(programming_language)) programming language. You can find other existing TextMate bundles [on GitHub](https://github.com/textmate).

You can convert the R bundle with the following command:

``` command-line
$ apm init --package ~/.atom/packages/language-r \
  --convert https://github.com/textmate/r.tmbundle
```

You can now browse to `~/.atom/packages/language-r` to see the converted bundle.

Your new package is now ready to use, launch Atom and open a `.r` file in the editor to see it in action!

#### Converting a TextMate Theme

This section will go over how to convert a [TextMate](http://macromates.com) theme to an Atom
theme.

##### Differences

TextMate themes use [plist](https://en.wikipedia.org/wiki/Property_list) files while Atom themes use [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) or [Less](http://lesscss.org) to style the UI and syntax in the editor.

The utility that converts the theme first parses the theme's plist file and then creates comparable CSS rules and properties that will style Atom similarly.

##### Convert the Theme

Download the theme you wish to convert, you can browse existing TextMate themes on the [TextMate website](http://wiki.macromates.com/Themes/UserSubmittedThemes).

Now, let's say you've downloaded the theme to `~/Downloads/MyTheme.tmTheme`, you can convert the theme with the following command:

``` command-line
$ apm init --theme ~/.atom/packages/my-theme \
  --convert ~/Downloads/MyTheme.tmTheme
```

You can then browse to `~/.atom/packages/my-theme` to see the converted theme.

##### Activate the Theme

Now that your theme is installed to `~/.atom/packages` you can enable it by launching Atom and selecting the _Atom > Preferences..._ menu.

Select the _Themes_ link on the left side and choose _My Theme_ from the __Syntax Theme__ dropdown menu to enable your new theme.

Your theme is now enabled, open an editor to see it in action!
