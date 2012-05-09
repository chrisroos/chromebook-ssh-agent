## Chromebook (ChromeOS) ssh-agent script

This script ensures that ssh-agent is running and that my default keys are added when I launch the developer shell (through crosh or VT2) on my chromebook.  The ssh-agent script itself is copied from http://help.github.com/ssh-key-passphrases.

I initially tried sourcing ~/.ssh_agent from ~/.profile (as suggested in [gist 749325](https://gist.github.com/749325)) but that caused errors when logging in via VT2 because the default shell for the chronos user is sh rather than bash.

## Installation

    curl -s -L goo.gl/VSVbH | /bin/bash

or

    curl -s -L https://raw.github.com/chrisroos/chromebook-ssh-agent/master/install | /bin/bash

*NOTE.* The goo.gl shortened version is handy on my chromebook because I can't paste anything into the crosh shell.

*NOTE.* The installation script is pretty dumb.  Running it multiple times will result in multiple 'source ~/.ssh_agent' lines being added to ~/.bashrc.

