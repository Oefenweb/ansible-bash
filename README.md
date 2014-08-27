## bash [![Build Status](https://travis-ci.org/Oefenweb/ansible-bash.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-bash)

Set up bash in Debian-like systems.

#### Requirements

None

#### Variables

* `bash_bashrc_destinations`: [default: `[/etc/skel, {{ ansible_env.HOME }}]`]: Destinations to copy the bashrc file(s) to

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
