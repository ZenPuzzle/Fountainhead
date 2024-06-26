## Installation

1. Download and install [Sublime Text](http://www.sublimetext.com).
- [Download the ZIP of this repository](https://github.com/ZenPuzzle/Fountainhead/archive/master.zip) and uncompress it.
- Move the uncompressed **Fountainhead** folder to the appropriate packages directory:
    - In Sublime Text, select: `Sublime Text > Preferences > Browse Packages...`
    - Remove existing **Fountainhead** folder if you have one. Place the **Fountainhead** folder inside the open **Packages** directory.
- Relaunch **Sublime Text**.

## Quickstart

1. Open or create a new `.fountain` file.
    - If creating a new file, first save the file with a `.fountain` filename extension.
- Verify that "Fountainhead" appears in the bottom right-hand corner.
    - If it doesn't, you can click on the offending syntax and change it to `Fountainhead`, or you can use the menu: `View > Syntax > Open all with current extension as > Fountainhead`.
- Wait for the `CHARACTERS FOUND!` and `SCENES FOUND!` text to appear in the bottom left-hand corner, letting you know that everything has loaded properly.
    - *The text will not appear if you have disabled the Character and Scene Lists options in Fountainhead settings.*
- Write!
    - Only action and dialogue sentences need to begin with uppercase letters. Starting everything else with lowercase letters will allow character and scene heading autocompletion suggestions to appear.
        - The `Space` key will cause the autocomplete window to close, so write without spaces to keep the window open.
        - Pressing the `Tab` key will select the highlighted autocomplete selection.
    - Characters, scene headings, and transitions are automatically capitalized when you press the `Return` key at the end of a line.
        - `Command`+`Return`(`Control`+`Return`) will produce a normal carriage return.
        - Starting a character name with `@` will keep it as it's written. Typing an already entered `@` character name in lowercase will cause the autocomplete window to appear, which will enter the name in the correct format.
    - Fountainhead commands can be found in the `Tools > Fountainhead` menu.
    - Instructions to change settings are in: `Tools > Fountainhead > Preferences > Fountainhead Settings - Default`, and can also be found in the **Settings** section of this document.
        - Additional settings that are off by default can be activated, like auto-save.
    - The window will automatically scroll down once you reach the bottom.
- Customize Fountainhead by picking a color scheme (explained in **Features - Color Schemes**).

## Symbol Dictionary

Symbol | Key
-------|----
⏎ | `Return`
⌘ | `Command/Cmd/Super`
⌥ | `Option/Alt`
⌃ | `Control/Ctrl`
⇧ | `Shift`
→ | `Right Arrow`
↑ | `Up Arrow`
↓ | `Down Arrow`

*Key bindings are displayed as: OSX / Windows/Linux*

## Fountain Syntax

Fountainhead offers complete support of the Fountain syntax. For a complete overview of the Fountain syntax, go to [http://fountain.io/syntax](http://fountain.io/syntax).

*Note: Leading spaces and tabs are supported.*

What you want | How to get it
--------------|---------------
Scene Headings | Start line with: `INT.`, `EXT.`, `EST.`, `INT./EXT.`, `INT/EXT`, `I/E`, `.` *(forced scene heading)*
Scene Numbers | End Scene Heading with: `#`**Scene Number**`#`
Action | Paragraph of text (empty line before and after) or force Action by starting line with `!`
Character | All uppercase with empty line before and without an empty line after or force by starting line with `@` to allow for names with lowercase letters
Character Extensions | End character line with `(`**O.S., V.O., CONT'D**`)`
Dialogue | Lines of text that are beneath Character or Parenthetical lines
Parenthetical | Lines of `(`**Parenthetical Text**`)` that are beneath Character or Dialogue lines
Dual Dialogue | End second Character with: `^`
Lyrics | Start line with: `~`
Transitions |  `FADE IN:`, `FADE OUT.`, `FADE TO BLACK.`, all uppercase line that ends with: `TO:`, or force by starting line with: `>`
Notes | `[[`**Note Text**`]]`
Boneyard (ignored text) | `/*`**Boneyard Text**`*/`
Sections | Start line with one or more: `#`
"Act" Section | Start line with: `#` **Act**
"Sequence" Section | Start line with: `##` **Sequence**
"Scene" Section | Start line with: `###` **Scene**
Synopses | Start line with: `=`
Page Breaks | Line that only contains three or more consecutive equal signs: `===`
Line Breaks | Lines can be broken up by using carriage returns
Italics | `__`*Italic Text*`__`
Bold | `**`**Bold Text**`**`
\* | `\*`
Title Page | Title Page Key that ends with `:` and precedes its value (*Each key can have multiple values by placing them on newlines that are indented 3+ spaces or by a tab*)
Title: | `Title:` **Title**
Credit: | `Credit:` **Written by**
Author: | `Author:` **Author Name(s)**
Source: | `Source:` **Story by...**
Draft date: | `Draft date:` **Date**
Contact: | `Contact:` **Contact Info**

###Example:

```
Title:
    Title 1
    Title 2
Credit: Written by
Author: Author name
Source: Story by...
Draft date: 12/10/2014
Contact:
    Contact Info
    Address Line 1
    Address Line 2

# Act 1

= The introduction of Character

EXT. HOUSE - DAY

Some action text.

CHARACTER
(parenthetical)
Dialogue.

CUT TO:

.Scene Heading
```

## Features

Fountainhead takes care of the formatting, so you just have to worry about the words.

Fountainhead commands can be found by selecting:

`Tools > Fountainhead`
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead**

*All settings can be deactivated and customized by the user, as described in the **Settings** section.*

Automatic Capitalization and Line Spacing

Fountainhead believes in efficiency, and that means doing away with superfluous `Shift` and `Caps Lock` usage. It is smart enough to know which elements should be in all uppercase letters. Unless it's the beginning of an action or dialogue sentence, type everything in lowercase, and let Fountainhead handle the super-sizing.

Pressing ⏎ at the end of lines will have the following effect\*:

\* Pressing ⌘⏎ / ⌃⏎ will produce a normal carriage return.

Element Type | Uppercase | Line Spacing
-------------|-----------------|-------------
Scene Headings | YES | DOUBLE
Action | NO | DOUBLE
Characters\* | YES | SINGLE
`@` Characters\*\* | NO | SINGLE
Dialogue\*\*\* | NO | DOUBLE
Lyrics | NO | SINGLE
Parenthetical | NO | SINGLE
Transitions | YES | DOUBLE
Notes | NO | DOUBLE
Boneyard | NO | SINGLE
Sections | NO | DOUBLE
Synopses | NO | DOUBLE
Centered Text | NO | DOUBLE
Page Breaks | N/A | DOUBLE
Title Page | NO | SINGLE

\* Supports **V.O.** and **O.S.** character elements, which are automatically capitalized.

\*\* Character names that begin with `@` will remain as written, but **V.O.** and **O.S.** will be capitalized ( e.g., **@McDOWELL (v.o.) > @McDOWELL (V.O.)** ).

\*\*\* Dialogue lines that are not complete sentences have single line spacing. Dialogue line spacing can be changed in settings.

### Manual Capitalization

For those times that manual capitalization is needed (e.g., edits), the following commands are provided:

Key Combination | Performs the Following Action
----------------|------------------------------
`⌘K`, `⌘L` / `⌃K`, `⌃L`\* | Convert highlighted text to lowercase
`⌘K`, `⌘U` / `⌃K`, `⌃U`\* | Convert highlighted text to uppercase
`⌘K`, `K` / `⌃K`, `K`\*\* | Capitalize the entire line

\* The comma is used to separate the sequence of key presses (`X`,`Y` is equal to "Press **X**, and then press **Y**").

\*\* All commands use lowercase letters (`K` is equal to pressing **k**), unless preceded by ⇧/`Shift`.

The above commands can also be selected through the use of menus:

`Tools > Fountainhead > Convert to Lowercase`
`Tools > Fountainhead > Convert to Uppercase`
`Tools > Fountainhead > Capitalize Current Line`
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Convert to Lowercase**
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Convert to Uppercase**
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Capitalize Current Line**

### Automatic Escaping of Parentheses, Boneyard, and Notes

Pressing ⏎ when the cursor is directly to the left of the closing `)`,`*/`, `]]` will automatically escape the element and create a line break. 

Pressing ⇧`Space` is the same as pressing → and will move your cursor to the right (useful for keyboards with Lilliputian arrow keys).

### Color Schemes

Fountainhead comes with a variety of custom color schemes, as well as support for all general Sublime Text color schemes.

By default, all custom color schemes are deactivated, allowing you to pick any of Sublime Text's general color schemes by selecting:
`Sublime Text > Preferences > Color Scheme`

Fountainhead's custom color schemes can be chosen by selecting:
`Sublime Text > Preferences > Color Scheme > Fountainhead > schemes`

*Note: If you want a color scheme to only appear when working on a `.fountain` file, you can edit your user settings (explained in **Settings**), and uncomment the desired color scheme.*

You may have to close (*save first!*) and re-open your screenplay if your color scheme changes are not seen.

### Character List

Characters are remembered and can be autocompleted:

1. When a document is first loaded, wait for the `CHARACTERS FOUND!` to appear. This process generally takes less than a second.
- Begin a line with any lowercase letter.\*
- When the autocomplete window appears, highlight the desired character by using ↑/↓, or by typing more letters of the character's name.
    - Pressing the `Space` or `Esc` key will cancel the autocompletion. If your name has a space in it, just think of it as being one long name and avoid the `Space` key like a cliché.
- Press `Tab` to accept the autocompletion.\*\*
    - Pressing `Return` will only produce a newline, and **not** accept the autocompletion.

\* This also works for previously entered `@` character names that require lowercase letters.

\*\* If you don't want any of the suggestions, just write like normal. You can choose to close the window by pressing `Esc`.

**Sublime Text 3:** ⇧⌃C / ⇧⌘C will bring up a pop-up menu that displays all previously entered characters. Pressing `Enter` or clicking on it will select the character (`Tab` will not select the character).

If the character list gets out of sync, you can recreate it by selecting:

`Tools > Fountainhead > Update Character List`
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Update Character List**

### Scene List

Scenes are remembered and can be autocompleted:

1. When a document is first loaded, wait for the `SCENES FOUND!` to appear. This process generally takes less than a second.
- Begin a line with any lowercase letter or a period.
- When the autocomplete window appears, highlight the desired scene by using ↑/↓, or by typing more letters of the scene heading.
    - Pressing the `Space` or `Esc` key will cancel the autocompletion, so skip pressing the `Space` key.
- Press `Tab` to accept the autocompletion.\*
    - Pressing `Return` will only produce a newline, and **not** accept the autocompletion.

\* If you don't want any of the suggestions, just write like normal. You can close the window by pressing `Esc`.

**Sublime Text 3:** ⇧⌃S / ⇧⌘S will bring up a pop-up menu that displays all previously entered scenes. Pressing `Enter` or clicking on it will select the scene (`Tab` will not select the scene).

If the scene list gets out of sync, you can recreate it by selecting:

`Tools > Fountainhead > Update Scene List`
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Update Scene List**

### (CONT'D)

By default, `(CONT'D)`s are added to new characters. If you are loading a screenplay that doesn't have `(CONT'D)`s added, or have them added incorrectly, you can update your **entire** script by selecting:

`Tools > Fountainhead > Update Character (CONT'D)s`
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Update Character (CONT'D)s**

You can remove all `(CONT'D)`s from the script by selecting:

`Tools > Fountainhead > Remove all Character (CONT'D)s`
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Remove all Character (CONT'D)s**\*

\* If the `"contd"` Fountainhead setting is not `false`, a `(CONT'D)` will be added to all newly typed characters.

### Auto-Save

Fountainhead has the ability to automatically save your script after a defined number of keystrokes. By default this feature is turned off, but can be activated in user settings (explained in **Settings**).

This feature pairs well with an app like [Marked 2](http://marked2app.com) that updates its preview every time you save.

### Automatic Page Scrolling

Automatic page scrolling is built into Fountainhead, and activates when the cursor reaches the bottom of the screen. Once activated, the page scrolls down until the most recently edited action, character, or scene heading reaches the top of the screen.

### Cursor Movement Shortcuts

Shortcut | Equal to
---------|-----
⇧`Space` |  →
⇧`Return` | ↓
⌘`Return` / ⌃`Return` | "Normal" `Return`\*

\* ⌘`Return` / ⌃`Return` in the middle of a line of text will add a newline below, without breaking up the text on the previous line.

### Quick Navigation to Scenes and Sections

To navigate to a particular scene or section quickly, select: `Goto > Goto Symbol...` (⌘R / ⌃R). Type the desired scene/section or use ↑/↓, and press `Return` to select it. Pressing `Esc` will cancel out of the process.

### Show/Hide Boneyard, Synopses, and Notes

Boneyard, Synopses, and Notes can be quickly hidden or revealed by selecting:

`Tools > Fountainhead > Boneyard: Show/Hide` ( ⌘K then ⌘/ / ⌃K then ⌃/ )
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Show/Hide Boneyard**

`Tools > Fountainhead > Synopses: Show/Hide` ( ⌘K then ⌘= / ⌃K then ⌃= )
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Show/Hide Synopses**

`Tools > Fountainhead > Notes: Show/Hide` ( ⌘K then ⌘[ / ⌃K then ⌃[ )
or
`Tools > Command Palette` (⇧⌘P / ⇧⌃P) and entering **Fountainhead: Show/Hide Notes**

Within user settings (explained in **Settings**), there is the ability to hide boneyard, synopses, and notes by default.

### Text Emphasis

Previously typed words can be highlighted and given the desired emphasis by typing the appropriate `*` and `_` characters. `*` and `_` will wrap automatically around the word(s).

### Distraction Free Mode

Sublime Text comes with a distraction free mode: `View > Enter Distraction Free Mode`(⇧⌃⌘F).

You can create separate settings by editing: `Sublime Text > Preferences > Settings - More > Distraction Free`\*.

\* These changes are reflected no matter the syntax. I have found that a `"wrap_width": 80` setting works well for distraction free coding as well as screenplay writing.

## Settings

A description of Fountainhead's settings are located in the Default Fountainhead Settings file:
`Tools > Fountainhead > Preferences > Fountainhead Settings - Default`

If you want to change any of Fountainhead's settings, you must do so in your Fountainhead User Settings file, or else your changes will be lost whenever Fountainhead is updated:

1. Open `Tools > Fountainhead > Preferences > Fountainhead Settings - Default`
2. Select all of the text: `Selection > Select All` (⌘A / ⌃A)
3. Open `Tools > Fountainhead > Preferences > Fountain Settings - User`
4. Paste the copied text: `Edit > Paste` (⌘V / ⌃V)
5. Comment/Uncomment (`⌘/` / `⌃/` or by adding/deleting the `//` at the beginning of the line) or Edit the value of the setting you want to change (usually **true** or **false**)\*
6. Save (⌘S / ⌃S)

\* Each setting should only have one active value.

## Key Bindings

You can customize Fountainhead's key bindings by copying the desired default key binding and editing it in your user key bindings. Due to how many key bindings Fountainhead uses, changes made to key bindings can have unexpected results.

Key Bindings can be accessed at:

`Tools > Fountainhead > Preferences > Key Bindings - Default`
`Tools > Fountainhead > Preferences > Key Bindings - User`

## License

The project is licensed under the MIT license.
