[![Build Status](https://travis-ci.com/jcs090218/use-ttf.svg?branch=master)](https://travis-ci.com/jcs090218/use-ttf)
[![MELPA](https://melpa.org/packages/use-ttf-badge.svg)](https://melpa.org/#/use-ttf)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)


# use-ttf #

use-ttf is an Emacs package for you to use your own `.ttf` 
file in Emacs.


## Who may need this? ## 
I created this for people who have problems with their fonts not working 
over different OS’s due to different installation methods used in different 
OS’s. The purpose of this package is to automatically install font files (.ttf) 
based on the OS you’re using. Saving you time from manually installing fonts.


## Configuration ##
List of TTF fonts you want to use and install in the currnet OS.
```el
;; I just have all my fonts inside my '.emacs.d' directory for sake of simplicity.
;; But you can have your font at any directory you want.
(setq use-ttf-default-ttf-fonts '(;; >> Classic Console <<
                                  "/.emacs.d/fonts/clacon.ttf"
                                  ;; >> Ubuntu Mono <<
                                  "/.emacs.d/fonts/UbuntuMono-R.ttf"))
```

Name of the font you want to use as default. I choose Ubuntu Mono as my 
default font.
```el
(setq use-ttf-default-ttf-font-name "Ubuntu Mono")
```

## Usage ##
Install fonts into the current OS. The more .ttf file you try to install might
take a while, but this function does not block the Emacs' process itself.
Furthermore, you will want to call `use-ttf-set-default-font` function after
install all the fonts in the `use-ttf-default-ttf-fonts` list.
```el
(call-interactively #'use-ttf-install-fonts)
```

Use the font by `use-ttf-default-ttf-font-name` variable. This will actually
set your Emacs to your target font.
```el
(call-interactively #'use-ttf-set-default-font)
```

## Screenshot ##
Windows 10 with Ubuntu Mono Regular Font <br/>
<img src="./screenshot/ubuntu-mono-on-win10.png" width="640" height="360"/>

Ubuntu 14 with Classic Console Font <br/>
<img src="./screenshot/classic-console-on-ubuntu14.png" width="640" height="360"/>

Mac OS with Ubuntu Mono Regular Font <br/>
<img src="./screenshot/ubuntu-mono-on-maxos.png" width="640" height="360"/>


## Contribution ##
If you would like to contribute to this project, you may either 
clone and make pull requests to this repository. Or you can 
clone the project and establish your own branch of this tool. 
Any methods are welcome!
