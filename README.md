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

python dev:
Anaconda

GIT COMPLETION
```#git-aware-prompt
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
fi```
