# The Extended Latin Keyboard (ELK)

The ELK is an AutoHotKey (AHK) script that is able to type every Latin character, every diacritic, and every possible combination of them whether pre-composed or not. It can type characters used in Latin-based scripts ranging from German to Vietnamese, phonetic scripts from the IPA to Teuthonista, and everything in between. It can even type Zalgo text!

This script supports all characters in the following Unicode blocks:
* [Latin-1 Supplement](https://en.wikipedia.org/wiki/Latin-1_Supplement) | [Latin Extended Additional](https://en.wikipedia.org/wiki/Latin_Extended_Additional)
* [Latin Extended-A](https://en.wikipedia.org/wiki/Latin_Extended-A) | [Latin Extended-B](https://en.wikipedia.org/wiki/Latin_Extended-B) | [Latin Extended-C](https://en.wikipedia.org/wiki/Latin_Extended-C) | [Latin Extended-D](https://en.wikipedia.org/wiki/Latin_Extended-D) | [Latin Extended-E](https://en.wikipedia.org/wiki/Latin_Extended-E) | [Latin Extended-F](https://en.wikipedia.org/wiki/Latin_Extended-F) | [Latin Extended-G](https://en.wikipedia.org/wiki/Latin_Extended-G)
* [IPA Extensions](https://en.wikipedia.org/wiki/IPA_Extensions) | [Phonetic Extensions](https://en.wikipedia.org/wiki/Phonetic_Extensions) | [Phonetic Extensions Supplement](https://en.wikipedia.org/wiki/Phonetic_Extensions_Supplement)
* [Superscripts and Subscripts](https://en.wikipedia.org/wiki/Superscripts_and_Subscripts) | [Spacing Modifier Letters](https://en.wikipedia.org/wiki/Spacing_Modifier_Letters) | [Modifier Tone Letters](https://en.wikipedia.org/wiki/Modifier_Tone_Letters)
* [Combining Diacritical Marks](https://en.wikipedia.org/wiki/Combining_Diacritical_Marks) | [Combining Diacritical Marks Extended](https://en.wikipedia.org/wiki/Combining_Diacritical_Marks_Extended) | [Combining Diacritical Marks Supplement](https://en.wikipedia.org/wiki/Combining_Diacritical_Marks_Supplement)

It also supports some characters in other blocks also used in the IPA.

## Installation
* Install [AutoHotKey](https://www.autohotkey.com/) at version 2.0 or newer.
* Place the `.ahk` file (the script) in your start-up folder.
* Run the script.

The script should now automatically run every time your machine boots.

## Usage
All characters in this script are typed with hotkeys and hotstrings involving `RAlt` (the right `Alt` key) which on some keyboards is shown as `AltGr`. Please note that this script will override the original functions of this key, and that hotstrings are only able to function when every component character has been typed consecutively and therefore registered by AHK.

### Hotkeys
Hotkeys are composed of `RAlt`, optionally `LAlt`, and a specific key. They type the most common diacritics and a select few common characters, and are the easiest to type.

Diacritics are typed in the form of combining characters, and can be appended to base letters to form new letters. The specific key of a diacritic may depend on its shape, name, or relative position to a related diacritic on the QWERTY layout. For instance, `RAlt` + `U` yields a  breve, `RAlt` + `A` yields an acute, and `RAlt` + `Q` yields a double acute as `Q` is above `A`.

The `LAlt` key is used similarly to how the `Shift` key is used normally, usually causing the diacritic to be placed below the preceding letter instead of above it, or occasionally vice-versa. For instance, `RAlt` + `LAlt` + `A` yields an acute below. The `Shift` key is not used in any hotkeys as `Alt` + `Shift` triggers a keyboard switch on Windows.

A number of non-diacritics may also be typed with hotkeys, such as the interpunct with `RAlt` + `.` or the zero-width space with `RAlt` + ` `.

### Hotstrings

Thanks to AHK's hotstrings, letters with diacritics are automatically converted to their pre-composed form as specified in Unicode, if it exists. This may be prevented by typing `RAlt` + `;` (before the hotstring is complete), which resets the hotstring register.

All other characters are typed using the hotstring brackets `⁅` and `⁆`, typed with `Alt` + `[` and `Alt` + `]` respectively, in the form `⁅hotstring⁆`.

### Modifiers
Modifiers are used in hotstrings to represent a kind of visual transformation, most frequently appearing in phonetic characters. Most modifiers are either only prepended or only appended to the character being modified, but in some cases either may apply with different effects depending on position.

For instance, the small modifier `-` is prepended (e.g. `⁅-H⁆` -> `ʜ`) while the bar modifier `-` is appended (e.g. ⁅H-⁆ -> `Ħ`).

### Namespaces
(TODO)
