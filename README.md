## bash

[![Build Status](https://travis-ci.org/Oefenweb/ansible-bash.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-bash) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-bash-blue.svg)](https://galaxy.ansible.com/list#/roles/3501)

Set up bash in Debian-like systems.

#### Requirements

None

#### Variables

* `bash_bashrc_destinations` [default: `{skell: dest: /etc/skel, current: dest: "{{ ansible_env.HOME }}"}`]: Destinations to copy the bashrc file(s) to
* `bash_bashrc_destinations.key`: The identifier of the file (e.g. `skel`)
* `bash_bashrc_destinations.key.dest`: The remote path of the file to copy (e.g. `/etc/skel`)
* `bash_bashrc_destinations.key.owner`: The name of the user that should own the file (optional, default `root`)
* `bash_bashrc_destinations.key.group`: The name of the group that should own the file (optional, default `owner`, then `root`)
* `bash_bashrc_destinations.key.mode`: The mode of the file, such as 0644 (optional, default `0644`)

* `bash_nohist`: [default: `true`]: Disables writing the history file
* `bash_histcontrol`: [default: `ignoreboth`]: Don't put duplicate lines or lines starting with space in the history
* `bash_histappend`: [default: `true`]: Append to the history file, don't overwrite it
* `bash_histsize`: [default: `1000`]: For setting history length see HISTSIZE and HISTFILESIZE in bash(1)
* `bash_histfilesize`: [default: `2000`]: For setting history length see HISTSIZE and HISTFILESIZE in bash(1)
* `bash_checkwinsize`: [default: `true`]: Check the window size after each command and, if necessary, update the values of LINES and COLUMNS.
* `bash_globstar`: [default: `false`]: If set, the pattern "**" used in a pathname expansion context will match all files and zero or more directories and subdirectories
* `bash_force_color_prompt`: [default: `true`]: Use a colored prompt, if the terminal has the capability
* `bash_fancy_prompt_prompt`: [default: `true`]: Use a (super) fancy prompt
* `bashrc_lines`: [default: `[]`]: Lines to add to `.bashrc`
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
