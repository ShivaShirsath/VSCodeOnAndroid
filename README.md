<h1 align=center>VS Code On Android</h1>

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Termux](#termux)
  - [Installation](#installation)
  - [Password](#password)
  - [Run](#run)
  - [Stop](#stop)
  - [Upgrading](#upgrading)
  - [Known Issues](#known-issues)
    - [Search issue](#search-issue)
    - [Backspace not working](#backspace-not-working)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Termux [⍗](https://play.google.com/store/apps/details?id=com.termux) [⇱](https://f-droid.org/en/packages/com.termux)

Termux is an Android terminal application and Linux environment, which can also run code-server from your phone.

### update & upgrade TermUX
```bash
apt update && apt upgrade
```



## Installation
<!--
1. Install Termux from [F-Droid]
2. Make sure it's up-to-date by running `apt update && apt upgrade`
-->
### Required packages : 
```bash
apt install build-essential python git nodejs yarn
```

### Install
```bash
yarn global add code-server
```
<!--
5. Run code-server: `code-server` and navigate to localhost:8080 in your browser
-->
## Password
```bash
nano ~/.config/code-server/config.yaml
```
## Run
## RUN

52

```bash
code-server
```
## Open
```bash
termux-open --chooser http://127.0.0.1/8080
```
## Stop 
Open TermUX then :
```
Ctrl+C
```

## Upgrading

```bash
yarn global upgrade code-server --latest
```

## Known Issues

### Search issue

There is a known issue with search not working on Android because it's missing `bin/rg`. To fix:

1. Install `ripgrep` with `pkg`
   ```sh
   pkg install ripgrep
   ```
2. Make a soft link using `ln -s`

```sh
# run this command inside the code-server directory
ln -s $PREFIX/bin/rg ./lib/vscode/node_modules/vscode-ripgrep/bin/rg
```

For more context, see [comment](https://github.com/cdr/code-server/issues/1730#issuecomment-721515979).

### Backspace not working

There is a known issue with the backspace key not working correctly when using the on-screen keyboard on Android. This is due to an upstream issue. Read more:

- [Issues with Backspace in Codespaces on Android (Surface Duo)](https://github.com/microsoft/vscode/issues/107602)
- [Support mobile platforms](https://github.com/xtermjs/xterm.js/issues/1101)

Workaround: use a Bluetooth keyboard.

For more context, see issues:

- [500 error: 3.9.2 not working on Android + Termux](https://github.com/cdr/code-server/issues/3036)
- [Document Android backspace issue](https://github.com/cdr/code-server/issues/3079)
