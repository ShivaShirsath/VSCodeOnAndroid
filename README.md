<h1 align=center>VS Code<br>On<br>Android</h1>

+ Install directly from web 
  - [⇱](https://vscode.dev/github) VS code
  - [⇱](https://insiders.vscode.dev/github) VS code insider 
  - [⇱](https://github.dev) Github dev 

Or

  - [TermUX](#termux)
  - [Update + Upgreade](#upgrade)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Open](#open)
  - [Stop](#stop)
  - [Upgrading](#upgrading)

***

## TermUX  [⍗](https://play.google.com/store/apps/details?id=com.termux)   [⇱](https://f-droid.org/en/packages/com.termux)

Termux is an Android terminal application and Linux environment, which can also run code-server from your phone.

## Upgrade
### update & upgrade TermUX
```bash
termux-change-repo && pkg update -y && pkg upgrade -y
```
select `Mirror Group` then `Mirrors in Asia`

### Installation of Essential packages
```bash
pkg install -y build-essential binutils pkg-config python3 yarn nodejs-lts && npm config set python python3
```

## Installation
```bash
yarn global add code-server
```
Or
```bash
npm install --global code-server --unsafe-perm
```
[Official](https://github.com/coder/code-server)

## Configuration
```bash
echo -e "bind-addr: 127.0.0.1:8080\nauth: none\ncert: false" > ~/.config/code-server/config.yaml
```

## Open
- Open & Run 
  ```
  termux-open http://localhost:8080 && code-server . &
  ```
- Reload Or Wait ʒ seconds
  
## Stop 

Open TermUX then press ` Ctrl+C `

## Upgrading

```bash
yarn upgrade code-server
```

## [©](https://coder.com/docs/code-server/latest/termux#yarn-installation)
