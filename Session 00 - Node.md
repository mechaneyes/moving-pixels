# node.js

## install node on wsl

https://learn.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-wsl

## Install nvm, node.js, and npm

https://learn.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-wsl#install-nvm-nodejs-and-npm

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
```

To verify installation, enter: `command -v nvm` ...this should return 'nvm',

List which versions of Node are currently installed (should be none at this point): `nvm ls`

nstall the current stable LTS release of Node.js (recommended for production applications): `nvm install --lts`


# browser-sync

You can setup a `browser-sync` server which has the added benefit of automatically reloading the webpage when any changes were saved in the source code.

Follow instructions above to install node.js and open a Terminal/Command Prompt window

```
npm install -g browser-sync
```


```
browser-sync start --server -f -w
```

| Options | What it do |
| ---- | ---- |
| --server, -s | Run a Local server (uses your cwd as the web root) |
| --port | Specify a port to use |
| --watch, -w | Watch files |
| --files, -f | File paths to watch |

Your website should be available at `http://localhost:3000` and whenever you save a file in your project, the webpage will automatically reload.

- [https://www.browsersync.io/#install](https://www.browsersync.io/#install)
- [https://github.com/CodingTrain/Rainbow-Topics/issues/646](https://github.com/CodingTrain/Rainbow-Topics/issues/646)

Note: If you encountered an error that says `EACCES` when installing either `http-server` or `browser-sync` it means npm is not installed with the right permissions, follow the steps outlined at [https://docs.npmjs.com/getting-started/fixing-npm-permissions](https://docs.npmjs.com/getting-started/fixing-npm-permissions) to fix it.