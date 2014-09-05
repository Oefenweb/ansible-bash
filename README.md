## bash [![Build Status](https://travis-ci.org/Oefenweb/ansible-bash.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-bash)

Set up bash in Debian-like systems.

#### Requirements

None

#### Variables

* `bash_bashrc_destinations`: [default: `[/etc/skel, {{ ansible_env.HOME }}]`]: Destinations to copy the bashrc file(s) to
* `bash_nohist`: [default: `true`]: Disables writing the history file
* `bash_histcontrol`: [default: `ignoreboth`]: Don't put duplicate lines or lines starting with space in the history
* `bash_histappend`: [default: `true`]: Append to the history file, don't overwrite it
* `bash_histsize`: [default: `1000`]: For setting history length see HISTSIZE and HISTFILESIZE in bash(1)
* `bash_histfilesize`: [default: `2000`]: For setting history length see HISTSIZE and HISTFILESIZE in bash(1)
* `bash_checkwinsize`: [default: `true`]: Check the window size after each command and, if necessary, update the values of LINES and COLUMNS.
* `bash_globstar`: [default: `false`]: If set, the pattern "**" used in a pathname expansion context will match all files and zero or more directories and subdirectories
* `bash_force_color_prompt`: [default: `true`]: Use a colored prompt, if the terminal has the capability
* `bash_fancy_prompt_prompt`: [default: `true`]: Use a (super) fancy prompt
* `bash_aliases`: [default: see `defaults/main.yml`]: Aliases

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
  - bash
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-bash/issues)!
