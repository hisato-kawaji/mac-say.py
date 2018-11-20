[![](https://img.shields.io/badge/OS-MacOS-blue.svg?longCache=True)]()
[![](https://img.shields.io/pypi/pyversions/mac-say.svg?longCache=True)](https://pypi.org/pypi/mac-say/)
[![](https://img.shields.io/pypi/v/mac-say.svg?maxAge=3600)](https://pypi.org/pypi/mac-say/)
[![Travis](https://api.travis-ci.org/looking-for-a-job/mac-say.py.svg?branch=master)](https://travis-ci.org/looking-for-a-job/mac-say.py/)

#### Install
```bash
$ [sudo] pip install mac-say
```

#### Functions
function|description
-|-
`mac_say.say(args, background=False)`|run `say` with given args
`mac_say.voices(lang=None)`|return list of installed voices (name, lang, description)

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

<p align="center"><a href="https://pypi.org/project/readme-md/">readme-md</a> - README.md generator</p>