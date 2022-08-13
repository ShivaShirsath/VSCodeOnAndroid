<h1 align=center>VS Code On Android</h1>

+ Install directly from web 
  - [⇱](https://vscode.dev/github) VS code
  - [⇱](https://insiders.vscode.dev/github) VS code insider 
  - [⇱](https://github.dev) Github dev 

Or

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


  - [TermUX](#termux)
  - [Update + Upgreade](#upgrade)
  - [Required Packages](#required)
  - [Installation](#installation)
  - [Run](#run)
  - [Open](#open)
  - [Stop](#stop)
  - [Password](#password)
  - [Upgrading](#upgrading)
  - [Known Issues](#known-issues)
    - [Search issue](#search-issue)
    - [Backspace not working](#backspace-not-working)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## TermUX  [⍗](https://play.google.com/store/apps/details?id=com.termux)   [⇱](https://f-droid.org/en/packages/com.termux)

Termux is an Android terminal application and Linux environment, which can also run code-server from your phone.

## Upgrade
### update & upgrade TermUX
```bash
termux-change-repo && pkg update -y && pkg upgrade -y
```
select `Mirror Group` then `Mirrors in Asia`

## Required
### packages : 
```bash
pkg install -y build-essential binutils pkg-config python3 yarn nodejs-lts && npm config set python python3
```

## Installation
```bash
yarn global add code-server
```

## Configuration
```bash
echo -e "bind-addr: 127.0.0.1:8080\nauth: none\ncert: false" > ~/.config/code-server/config.yaml
```

## Open

  - Open & Run 
    ```
    termux-open --chooser http://127.0.0.1:8080/login && code-server
    ```
  - Reload Or Wait ʒ seconds
  
## Stop 

Open TermUX then press ` Ctrl+C `

## Upgrading

```bash
rm -rf ~/.local/lib/code-server-* && yarn upgrade code-server
```

## [©](https://coder.com/docs/code-server/latest/termux#yarn-installation)
