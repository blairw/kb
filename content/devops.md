---
Title: Home
show_in_header_nav: true
placing: 0200
---

## DevOps

For cross-platform (i.e. not tied to either [Mac](?mac) or [Windows](?windows)) dev ops stuff.

### bash

#### Pretty PS1

**PS1** (said to stand for **Prompt String 1**) is the string that appears before every typed command.

The PS1 string below has been designed to be a shade of blue that works well on both black and white backgrounds. Put it in `~/.bash_profile` and `~/.bashrc` for each user who wants it.

```bash
export PS1="\[\033[38;5;39m\][\u@\h \t \W]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput sgr0)\]"
```

Example:

![ps1-demo.png](%base_url%/assets/images/ps1-demo.png)

### git