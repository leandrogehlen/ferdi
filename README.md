<p align="center">
    <img src="./build-helpers/images/icon.png" alt="" width="200"/>
</p>

# Ferdi

<p align="center">
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section --><a href='#contributors'><img src='https://img.shields.io/badge/contributors-23-default.svg?logo=github' alt='Contributors'/></a><!-- ALL-CONTRIBUTORS-BADGE:END --> 
<a href="#backers-via-opencollective"><img alt="Open Collective backers" src="https://img.shields.io/opencollective/backers/getferdi?logo=open-collective"></a>
<a href="#sponsors-via-opencollective"><img alt="Open Collective sponsors" src="https://img.shields.io/opencollective/sponsors/getferdi?logo=open-collective"></a>
<a href="https://ci.appveyor.com/project/kytwb/ferdi"><img alt="Build Status Windows" src="https://img.shields.io/appveyor/ci/kytwb/ferdi/master?logo=appveyor"></a>
<a href="https://travis-ci.org/getferdi/ferdi"><img alt="Build Status Mac & Linux" src="https://img.shields.io/travis/getferdi/ferdi/master?logo=travis"></a>
</p>

🤴🏽 Hard-fork of [Franz](https://github.com/meetfranz/franz), adding awesome features and removing unwanted ones.

### Table of contents

<details>
<summary>Toggle navigation</summary>
<ul>
<li><a href="#what-is-ferdi">What is Ferdi?</a></li>
<li><a href="#what-does-ferdi-look-like">What does Ferdi look like?</a></li>
<li><a href="#download-ferdi">Download Ferdi</a>
<ul>
<li><a href="#or-use-homebrew-macos-only">Or use homebrew</a></li>
</ul>
</li>
<li><a href="#ferdi-specific-features">Ferdi-specific features</a></li>
<li><a href="#development">Development</a></li>
<ul>
<li><a href="#install-os-dependencies">Install OS dependencies</a></li>
<li><a href="#clone-repository-with-submodule">Clone repository with submodule</a></li>
<li><a href="#install-dependencies">Install dependencies</a></li>
<li><a href="#fix-native-modules-to-match-current-electron-node-version">Fix native modules to match current electron node version</a></li>
<li><a href="#start-development-app">Start development app</a></li>
<li><a href="#packaging">Packaging</a></li>
<li><a href="#release">Release</a></li>
</ul>
<li><a href="#contributors-">Contributors ✨</a></li>
<li><a href="#backers-via-opencollective">Backers via OpenCollective</a></li>
<li><a href="#sponsors-via-opencollective">Sponsors via OpenCollective</a></li>
</ul>
</details>

### What is Ferdi?

Ferdi is a messaging browser that allows you to combine your favorite messaging services into one application. It is based on Franz - a software already used by thousands of people - with the difference that Ferdi gives you many additonal features and doesn't restrict its usage! Ferdi is compatible with your existing Franz account so you can continue right where you left off. Find out more about Ferdi and its features on [getferdi.com](https://getferdi.com).

### What does Ferdi look like?

<details>
<summary>Toggle screenshots</summary>
<p align="center">
<img alt="Keep all your messaging services in one place." src="./branding/screenshots/hero.png">
<em>"Keep all your messaging services in one place."</em>
<img alt="Order your services with Ferdi Workspaces." src="./branding/screenshots/workspaces.png">
<em>"Order your services with Ferdi Workspaces."</em>
<img alt="Always keep your Todo list open with Ferdi Todos." src="./branding/screenshots/todos.png">
<em>"Always keep your Todo list open with Ferdi Todos."</em>
<img alt="Supporting all your services." src="./branding/screenshots/service-store.png">
<em>"Supporting all your services."</em>
</p>
</details>

## Download Ferdi

You can find the installers in the [latest stable release](https://github.com/getferdi/ferdi/releases/latest) assets and [all the other release here](https://github.com/getferdi/ferdi/releases).

### Or use homebrew (macOS only)

`$ brew cask install ferdi`

(Don't know homebrew? [brew.sh](https://brew.sh/))

### Or use AUR (Arch Linux)

Ferdi has two seperate AUR packages you can use:
- **ferdi-bin**: Uses your debian build and extracts it to Arch
- **ferdi-git**: Uses system electron version

If you use an AUR Helper e.g. yay, simply install it via `yay -S ferdi-bin`.

`ferdi-git` may not work on all systems so we advice you to use `ferdi-bin` instead.

## Ferdi-specific Features

- [x] Removes the counter-productive fullscreen app delay inviting users to upgrade
- [x] Removes pages begging you to donate after registration
- [x] Remove "Franz is better together" popup
- [x] Remove bug that would incorrectly display unread messages count on some services (more info in [7566ccd](https://github.com/getferdi/ferdi/commit/7566ccd))
- [x] Makes all users Premium by default ([#15](https://github.com/getferdi/ferdi/issues/15))
- [x] Using the Ferdi API instead of Franz's servers
- [x] [Add option to change server to a custom](https://github.com/getferdi/ferdi/wiki/Custom-Server) [ferdi-server](https://github.com/getferdi/server)
- [x] Add option to use Ferdi without an account ([#5](https://github.com/getferdi/ferdi/issues/5))
- [x] Add "Private Notification"-Mode, that hides message content from notifications ([franz#879](https://github.com/meetfranz/franz/issues/879))
- [x] Add Password Lock feature to keep your messages protected ([#41](https://github.com/getferdi/ferdi/issues/41), [franz#810](https://github.com/meetfranz/franz/issues/810), [franz#950](https://github.com/meetfranz/franz/issues/950), [franz#1430](https://github.com/meetfranz/franz/issues/1430))
- [x] Add an option to keep individual workspaces always loaded ([#37](https://github.com/getferdi/ferdi/issues/37))
- [x] Add Universal Dark Mode via the [DarkReader extension](https://github.com/darkreader/darkreader) ([#71](https://github.com/getferdi/ferdi/issues/71))
- [x] Add adaptable Dark Mode that will respect the system's Dark Mode setting ([#173](https://github.com/getferdi/ferdi/issues/173))
- [x] Add an option to auto-hide the menubar ([#7](https://github.com/getferdi/ferdi/issues/7), [franz#833](https://github.com/meetfranz/franz/issues/833))
- [x] Add "Quick Switch" feature to help you navigate a long list of services (similar to Rambox's [Quick Switcher](https://rambox.pro/#feature-details/quick_switcher))
- [x] Add "Service Hibernation" that will automatically unload services when they are unused
- [x] Add "Scheduled Do-not-Disturb" feature in which you won't get notifications (similar to Rambox's [Work Hours](https://rambox.pro/#feature-details/work_hours))
- [x] Add CTRL+← and CTRL+→ shortcuts and menu options to go back and forward in the service browsing history([#39](https://github.com/getferdi/ferdi/issues/39))
- [x] Add option to show a browser-like navigation bar on all services
- [x] Add option to change accent color
- [x] Add portable version for Windows
- [x] Add Process Manager to find services using a lot of resources
- [x] Add "npm run prepare-code" command for development to lint and beautify code
- [x] Add button to open darkmode.css for a service
- [x] Switch to [`electron-spellchecker`](https://github.com/electron-userland/electron-spellchecker) to improve application size
- [x] Improve "About Ferdi" screen to better display versions
- [x] Minifying build files to improve app size
- [x] [Makes it possible to edit the "Franz Todo" server](https://github.com/getferdi/ferdi/wiki/Custom-Todo)
- [x] Makes RocketChat self-hosted generally available ([#6](https://github.com/getferdi/ferdi/issues/6))
- [x] Comes with a custom branding proper to Ferdi

## Development

### Install OS dependencies

#### Node.js

Please make sure you are running NodeJS v10 ([v10.16.3](https://nodejs.org/dist/v10.16.3/) suggested). Versions above will throw an errow when trying to install due to an [old fsevent dependency](https://github.com/fsevents/fsevents/issues/278).

#### Git

The version [2.23.0](https://github.com/git-for-windows/git/releases/tag/v2.23.0.windows.1) for Git is working fine for development. You can then use the console from Git to do the development procedure.

#### Debian/Ubuntu

```bash
$ apt install libx11-dev libxext-dev libxss-dev libxkbfile-dev
```

#### Fedora

```bash
$ dnf install libX11-devel libXext-devel libXScrnSaver-devel libxkbfile-devel
```

#### Windows

```bash
$ npm install --global windows-build-tools --vs2015
```

### Clone repository with submodule

```bash
$ git clone https://github.com/getferdi/ferdi.git
$ cd ferdi
$ git submodule update --init --recursive
```

It is important you execute the last command to get the required submodules (recipes, server).

### Install dependencies

Run the following command to install all dependencies, and link sibling modules with Ferdi.

```bash
$ npx lerna bootstrap
```

If you previously ran `npm install` it sometimes is necessary to delete your `node_modules` folder before running `npx lerna bootstrap`.

### Fix native modules to match current electron node version

```bash
$ npm run rebuild
```

### Start development app

Run these two commands **simultaneously** in different console tabs:

```bash
$ npm run dev
$ npm run start
```

Be aware that the development database will be reset regularly.

### Packaging

```bash
$ npm run build
```

Deliverables will be available in the `out` folder.

### Release

```bash
$ git checkout develop && git pull && git checkout master
$ git merge --no-ff develop
$ git tag v5.3.4-beta.4
$ git push --tags
```

When pushing a new tag, the CI builds will create a draft GitHub release and upload the deliverables in the draft release assets. Wait for all the assets to be uploaded before publishing the draft release.

## Contributors ✨

Thanks goes to these awesome people:

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href='https://vantezzen.io' title='vantezzen is awesome!'><img src='https://avatars2.githubusercontent.com/u/10333196?v=4' alt='vantezzen' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='http://www.adlk.io' title='adlk is awesome!'><img src='https://avatars1.githubusercontent.com/u/3265004?v=4' alt='adlk' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://twitter.com/kytwb' title='kytwb is awesome!'><img src='https://avatars0.githubusercontent.com/u/412895?v=4' alt='kytwb' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='http://seriesgt.com' title='ZeroCool940711 is awesome!'><img src='https://avatars3.githubusercontent.com/u/5977640?v=4' alt='ZeroCool940711' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/rseitbekov' title='rseitbekov is awesome!'><img src='https://avatars2.githubusercontent.com/u/35684439?v=4' alt='rseitbekov' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://djangogigs.com/developers/peter-bittner/' title='bittner is awesome!'><img src='https://avatars2.githubusercontent.com/u/665072?v=4' alt='bittner' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/justus-saul' title='justus-saul is awesome!'><img src='https://avatars1.githubusercontent.com/u/5861826?v=4' alt='justus-saul' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/igreil' title='igreil is awesome!'><img src='https://avatars0.githubusercontent.com/u/17239151?v=4' alt='igreil' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='http://marcolopes.eu' title='marcolopes is awesome!'><img src='https://avatars1.githubusercontent.com/u/431889?v=4' alt='marcolopes' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/dayzlun' title='dayzlun is awesome!'><img src='https://avatars3.githubusercontent.com/u/17259690?v=4' alt='dayzlun' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://twitter.com/tobigue_' title='tobigue is awesome!'><img src='https://avatars2.githubusercontent.com/u/1560152?v=4' alt='tobigue' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/AGCaesar' title='AGCaesar is awesome!'><img src='https://avatars3.githubusercontent.com/u/7844066?v=4' alt='AGCaesar' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/Makazzz' title='Makazzz is awesome!'><img src='https://avatars2.githubusercontent.com/u/49844464?v=4' alt='Makazzz' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/xthursdayx' title='xthursdayx is awesome!'><img src='https://avatars0.githubusercontent.com/u/18044308?v=4' alt='xthursdayx' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/Gaboris' title='Gaboris is awesome!'><img src='https://avatars2.githubusercontent.com/u/9462372?v=4' alt='Gaboris' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='http://www.cu3ed.com/' title='incace is awesome!'><img src='https://avatars1.githubusercontent.com/u/61343?v=4' alt='incace' style='border-radius: 42px;width:42px;height:42px'/></a></td>
  </tr>
  <tr>
    <td align="center"><a href='http://pztrn.name/' title='pztrn is awesome!'><img src='https://avatars1.githubusercontent.com/u/869402?v=4' alt='pztrn' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='http://www.patrickcurl.com' title='patrickcurl is awesome!'><img src='https://avatars1.githubusercontent.com/u/1470061?v=4' alt='patrickcurl' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/Stanzilla' title='Stanzilla is awesome!'><img src='https://avatars3.githubusercontent.com/u/75278?v=4' alt='Stanzilla' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/ammarmalhas' title='ammarmalhas is awesome!'><img src='https://avatars1.githubusercontent.com/u/57057209?v=4' alt='ammarmalhas' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/steliyan' title='steliyan is awesome!'><img src='https://avatars1.githubusercontent.com/u/1850292?v=4' alt='steliyan' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://github.com/brorbw' title='brorbw is awesome!'><img src='https://avatars2.githubusercontent.com/u/5909562?v=4' alt='brorbw' style='border-radius: 42px;width:42px;height:42px'/></a></td>
    <td align="center"><a href='https://fwdekker.com/' title='FWDekker is awesome!'><img src='https://avatars0.githubusercontent.com/u/13442533?v=4' alt='FWDekker' style='border-radius: 42px;width:42px;height:42px'/></a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

## Backers via OpenCollective

<a href="https://opencollective.com/getferdi#section-contribute" target="_blank"><img src="https://opencollective.com/getferdi/backers.svg?width=890"></a>

## Sponsors via OpenCollective

<a href="https://opencollective.com/getferdi#section-contribute" target="_blank"><img src="https://opencollective.com/getferdi/sponsors.svg?width=890"></a>
