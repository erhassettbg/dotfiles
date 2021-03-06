# Ethan's dotfiles

This repo contains a collection of my dotfiles. Suggestions and contributions are welcome!

# Screenshot
![image](https://user-images.githubusercontent.com/7284853/118412539-9ce46580-b668-11eb-9b7b-94a47327a7e4.png)
Windows Terminal

# Installation

To install all the packages and plugins listed below, clone this repo and run `script/bootstrap`.

## Packages/Plugins

* [docker](https://www.docker.com/) (See notes below)

* [git-chglog](https://github.com/git-chglog/git-chglog)

* [git-secret](https://git-secret.io/)

* [go](https://golang.org/)
  * Version specified at the top of [script/bootstrap](script/bootstrap)

* [keychain](https://packages.ubuntu.com/bionic/keychain)

* [node](https://nodejs.org/en/)
  * Version specified at the top of [script/bootstrap](script/bootstrap)
  * [nvm](https://github.com/nvm-sh/nvm)
    * Version specified at the top of [script/bootstrap](script/bootstrap)

* [ruby](https://www.ruby-lang.org)
  * Version specified at the top of [script/bootstrap](script/bootstrap)
  * [rvm](https://rvm.io)

* [terraform](https://terraform.io)
  * Version specified at the top of [script/bootstrap](script/bootstrap)
  * [tfvm](https://github.com/ethanhassett/tfvm)

* [tmux](https://packages.ubuntu.com/bionic/tmux)
  * [tmuxinator](https://github.com/tmuxinator/tmuxinator)

* [vim](https://packages.ubuntu.com/bionic/vim)
  * [colorizer](https://github.com/lilydjwg/colorizer)
  * [NERDTree](https://github.com/scrooloose/nerdtree)
  * [pathogen](https://github.com/tpope/vim-pathogen)
  * [vim-surround](https://github.com/tpope/vim-surround)

* [Windows Terminal](https://github.com/microsoft/terminal) (See notes below)
  * [settings.json](wsl/winterm/settings.json)

* [zsh](https://packages.ubuntu.com/bionic/zsh)
  * [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

# Compatibilty
Tested on Ubuntu 18.04, 20.04, and Ubuntu 18.04, 19.10, 20.04 for WSL.

# Notes
## Docker
After installing docker, you may need to follow [these instructions](https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user) to allow non-root users to manage docker.

## Windows Terminal
`script/bootstrap` does not install Windows Terminal or copy `settings.json`.

## .gitconfig
`script/bootstrap` does not copy `.gitconfig` as it only contains aliases.

Alias notes:
* `git changelog`: Utilizes `git-chglog` to update the `CHANGELOG.md` file and tags in a repository.
* `git newver`: Extends `git changelog` to update the version string in `README.md` and `main.go` for a Golang project.