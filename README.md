git-stuff
=========

Random dev files that I want to remember.

.gitignore is my typical .gitignore file for an iOS project.

Sublime plugins:

Package Control
GitGutter
Sidebar
JSONLint
Pretty JSON

Sublime Key bindings
```
[
  { “keys”: [“super+shift+o”], “command”: “show_overlay”, “args”: {“overlay”: “goto”, “show_files”: true} }
]
```

TrailingSpaces- config
```
{
    "trailing_spaces_include_current_line" : false,

    // By default, trailing spaces are deleted within the whole document.
    // Set to true to affect only the lines you edited since last save.
    // Trailing spaces will still be searched for and highlighted in the whole
    // document.
    "trailing_spaces_modified_lines_only": true,

    // By default, nothing happens on save.
    // Set to true to trim trailing spaces before saving, with respect to the
    // other settings.
    "trailing_spaces_trim_on_save": true,
}
```

python dev:
Anaconda

GIT COMPLETION
```
#git-aware-prompt
function parse_git_dirty {
  [[ $(git status 2> /dev/null | tail -n1) != "nothing to commit, working tree clean" ]] && echo "*"
}
function parse_git_branch {
  git branch --no-color 2> /dev/null | sed -e '/^[^*]/d' -e "s/* \(.*\)/[\1$(parse_git_dirty)]/"
}

export PS1='\[\033[1;33m\]\w\[\033[0m\]$(parse_git_branch)\$ '

#tree
alias tree="find . -print | sed -e 's;[^/]*/;|____;g;s;____|; |;g' | less"


#git completion `brew install bash-completion`
if [ -f $(brew --prefix)/etc/bash_completion ]; then
    . $(brew --prefix)/etc/bash_completion
fi
```


Git Aliases
`git config --global alias.co checkout`
`git config --global alias.st status`
