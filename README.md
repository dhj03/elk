# The Extended Latin Keyboard (ELK)
The ELK is an AutoHotkey (AHK) script that can type every Latin character, every diacritic, and every possible combination of them, precomposed or otherwise. This includes characters in languages ranging from French to Vietnamese, phonetic scripts such as the IPA, and even Zalgo text (ļ̨̤̮̽̎i̗̬̰̊̏̄ķ̱͈̈̑̇ę̦̩̌̋́ ṭ͓̑̃̀ẖ̨̛͓̰̑̑̉į̤̗̎̆̑s̨̧̨̛̥̩̲̆̑̉)!

This script supports all characters in the following Unicode blocks:
* [Latin-1 Supplement](https://en.wikipedia.org/wiki/Latin-1_Supplement) | [Latin Extended Additional](https://en.wikipedia.org/wiki/Latin_Extended_Additional)
* [Latin Extended-A](https://en.wikipedia.org/wiki/Latin_Extended-A) | [Latin Extended-B](https://en.wikipedia.org/wiki/Latin_Extended-B) | [Latin Extended-C](https://en.wikipedia.org/wiki/Latin_Extended-C) | [Latin Extended-D](https://en.wikipedia.org/wiki/Latin_Extended-D) | [Latin Extended-E](https://en.wikipedia.org/wiki/Latin_Extended-E) | [Latin Extended-F](https://en.wikipedia.org/wiki/Latin_Extended-F) | [Latin Extended-G](https://en.wikipedia.org/wiki/Latin_Extended-G)
* [IPA Extensions](https://en.wikipedia.org/wiki/IPA_Extensions) | [Phonetic Extensions](https://en.wikipedia.org/wiki/Phonetic_Extensions) | [Phonetic Extensions Supplement](https://en.wikipedia.org/wiki/Phonetic_Extensions_Supplement)
* [Superscripts and Subscripts](https://en.wikipedia.org/wiki/Superscripts_and_Subscripts) | [Spacing Modifier Letters](https://en.wikipedia.org/wiki/Spacing_Modifier_Letters) | [Modifier Tone Letters](https://en.wikipedia.org/wiki/Modifier_Tone_Letters)
* [Combining Diacritical Marks](https://en.wikipedia.org/wiki/Combining_Diacritical_Marks) | [Combining Diacritical Marks Extended](https://en.wikipedia.org/wiki/Combining_Diacritical_Marks_Extended) | [Combining Diacritical Marks Supplement](https://en.wikipedia.org/wiki/Combining_Diacritical_Marks_Supplement)

It also supports IPA characters in other blocks not mentioned above.

## Installation
Note: AutoHotkey v2.0 only supports Windows 7 or newer.

* Install [AutoHotkey](https://www.autohotkey.com/) v2.0 or newer.
* Place `elk.ahk` (the script) in your start-up folder.
* Run the script.

The script should now automatically run every time your machine starts up.

## Usage
A hotkey is a combination of keys pressed together (such as `Ctrl` + `V`), and a hotstring is a series of characters that changes after being typed (such as 'omw' turning into 'On my way!').

This script works by converting hotkeys and hotstrings into diacritics and other special characters. All of them are typed with `RAlt` (the right `Alt` key, also known as `AltGr`), so this script (probably) won't affect your typing workflow. That being said, it will override how `RAlt` normally behaves.

Note that AHK hotstrings are only recognised when typed in one go, so if you switch tabs or move your text cursor, the hotstring won't be typed correctly.

### Diacritics and Hotkeys
Most diacritics are typed with a hotkey of `RAlt` and a letter, such as `RAlt` + `A` which gives the acute accent (◌́).

The `LAlt` key is added to give a variant, such as `RAlt` + `LAlt` + `A` which gives the acute accent below (◌̗).

Diacritics are combining characters added after letters, so 'á' is typed with 'a' followed by `RAlt` + `A`.

Hotkeys usually type diacritics, but a few hotkeys type special characters, such as `RAlt` + `.` which gives the interpunct (·).

You can find a list of all hotkeys [here](Lists/Hotkeys.md). Not all diacritics are typed with hotkeys; some are typed with hotstrings which are explained below.

### Precomposed Characters
While Unicode allows letters to be followed by diacritics, most letters with diacritics are actually encoded separately as precomposed characters.

For instance, 'á' and 'á' are different; the first one is a single precomposed character while the second one is two separate characters. To see the difference, try copying them and pressing backspace after each letter.

There are also extreme examples such as 'ậ', 'ậ', 'ậ', 'ậ', and 'ậ' which all appear identically despite being encoded differently. Due to this concern and legacy reasons, Unicode recommends using precomposed characters wherever possible.

As such, this script automatically precomposes letters with diacritics by using hotstrings. As mentioned in the Usage section though, hotstrings only work when typed in one go.

You can disable precomposition for a letter by using the hotkey `RAlt` + `;` after typing it.

### Other Characters and Hotstrings
All other characters are typed using the hotstring brackets `⁅` (from `RAlt` + `[`) and `⁆` (from `RAlt` + `]`), in the form of `⁅hotstring⁆`.

For instance, `⁅ae⁆` gives 'æ', `⁅dh⁆` gives 'ð', and `⁅sh⁆` gives 'ʃ'.

Since there are thousands of hotstring combinations, no separate documentation has been written for them.

You can find a list of all hotstrings in the [script](elk.ahk), which is fairly self-explanatory.

### Modifiers
Modifiers are used in hotstrings to represent a kind of visual transformation. They can be prepended or appended, with different effects in each case.

For instance, '-' can represent the small modifier which is prepended (e.g. `⁅-L⁆` -> 'ʟ'), or the high stroke modifier which is appended (e.g. `⁅L-⁆` -> 'Ꝉ').

You can find a list of all modifiers [here](Lists/Modifiers.md).

### Namespaces
Namespaces are used to categorise characters that cannot be described with modifiers alone, and may even use modifiers differently.

Their syntax is `⁅namespace:hotstring⁆`, such as `⁅rn:X⁆` which gives `Ⅹ` (the Roman numeral for 10).

You can find a list of all namespaces [here](Lists/Namespaces.md).
