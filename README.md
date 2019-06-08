<!--
https://pypi.org/project/readme-generator/
https://pypi.org/project/python-readme-generator/
-->

[![](https://img.shields.io/badge/OS-MacOS-blue.svg?longCache=True)]()
[![](https://img.shields.io/pypi/pyversions/mac-say.svg?longCache=True)](https://pypi.org/project/mac-say/)
[![](https://img.shields.io/pypi/v/mac-say.svg?maxAge=3600)](https://pypi.org/project/mac-say/)
[![Travis](https://api.travis-ci.org/looking-for-a-job/mac-say.py.svg?branch=master)](https://travis-ci.org/looking-for-a-job/mac-say.py/)

#### Installation
```bash
$ [sudo] pip install mac-say
```

#### Functions
function|`__doc__`
-|-
`mac_say.say(args, background=False)` |run `say` with given args
`mac_say.voices(lang=None)` |return a list of installed voices (name, lang, description)
`mac_say.gtts.mp3(lang, string)` |create .mp3 file (if cache not exists) and return path
`mac_say.gtts.say(lang, string)` |creare `.mp3` file and play it with `afplay`

#### Executable modules
usage|`__doc__`
-|-
`python -m mac_say.gtts lang strings ...` |create `. mp3` file with Google Text-to-Speech and play it with `afplay`

#### Examples
```python
>>> import mac_say
>>> mac_say.say("hello world")
>>> mac_say.say(["-f","file.txt","-v","Alex"])
```

voices list
```python
>>> mac_say.voices("en")
[('Alex', 'en_US', 'Most people recognize me by my voice.'), ...]
```

background - add `background=True`
```python
>>> mac_say.say("hello world",background=True)
```

Google Text-To-Speech
```python
>>> mac_say.gtts.mp3("en","hello world")
/Users/username/Library/Caches/say/<hash>.mp3

>>> mac_say.gtts.say("en","hello world")
```

```bash
$ python -m mac_say.gtts "en" "hello world"
```

<p align="center">
    <a href="https://pypi.org/project/python-readme-generator/">python-readme-generator</a>
</p>