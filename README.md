# The Extended Latin Keyboard (ELK)

The ELK is an AutoHotKey (AHK) script that is able to type every Latin character, every diacritic, and every possible combination of them whether pre-composed or not. It is able to type characters used in Latin-based scripts from German to Turkish, phonetic scripts from the IPA to Teuthonista, and everything in between. It can even type Zalgo text!

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
All characters in this script are typed with hotkeys and hotstrings involving `RAlt` (the right `Alt` key) which on some keyboards is shown as `AltGr`. Please note that this script will override the original functions of this key, and that hotstrings are only able to function when every component character has been typed in order and registered by AHK.

### Direct Characters
Direct characters are typed directly with `RAlt` and another key. These are the most common diacritics and a select few common characters, and are the easiest to type.

Diacritics are typed in the form of combining diacritic characters, and can be appended to base letters to form letters with diacritics. The letter they are associated with may depend on their shape, name, or relative position to a related diacritic on the QWERTY layout. For instance, `RAlt` + `U` yields the breve, `RAlt` + `A` yields the acute, and `RAlt` + `Q` yields the double acute as `Q` is above `A`.

Thanks to AHK's hotstrings, letters with diacritics are automatically converted to their pre-composed form as specified in Unicode, if it exists. This may be prevented by typing `RAlt` + `;` (before the hotstring is complete), which resets the hotstring register.

A number of non-diacritics may also be typed as direct characters, such as the interpunct (`RAlt` + `.`) or the zero-width space (`RAlt` + ` `).

All other characters are typed using the hotstring brackets `⁅` and `⁆`, typed with `Alt` + `[` and `Alt` + `]` respectively, in the form `⁅hotstring⁆`.

### Modified Characters
(TODO)

### Specialized Characters
(TODO)
