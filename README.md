# electron-yacd

**THANKS to many projects and authors who make this repo possible!**

(and I copy & paste these links redirected to those helpful project)

[electron/electron-quick-start](https://github.com/electron/electron-quick-start) is a simple ready-to-use template with the latest feature of electron.

[haishanh/yacd](https://github.com/haishanh/yacd) provides an awesome dashboard of clash. It works on Web / PC static files / OpenClash (on OpenWrt) and provides a simple way to dev, build and update the single-page web application.

[kentcdodds/cross-env](https://github.com/kentcdodds/cross-env), cross-env essentially helps me to bypass the NODE_ENV= problem on my windows machine.

[binaryfunt/electron-seamless-titlebar-tutorial](https://github.com/binaryfunt/electron-seamless-titlebar-tutorial) is used as icons, js scripting, and css styling of the titlebar (min, max, close buttons) of this electron-yacd application in frameless window mode. His code is very clean and static, which helps me to integerate two (yacd + seamless-titlebar) into one public folder before building the `.asar` file.

[sindresorhus/electron-reloader](https://github.com/sindresorhus/electron-reloader) helps to hot reload the changes on any files, and restart the electron window to apply the change. It helps quicker reviews of the code changes.

[electron/electron-packager
](https://github.com/electron/electron-packager) While our other dev repo [uses electron-builder as devDependency](https://github.com/DanmakuTree/DanmakuTree/blob/594ba72b4d5e5790bd08ede968ed9cff5c1d2fe7/package.json#L47) to build and deliver program distributions, I find it's too heavy to configure the folder-structure and builder-scripts setup to fulfill the need of a small applicaiton build. Then instead I find `electron-packager` as a more helpful packing binary for me on this project to use. Note: when you build & deliver your exectuable with `electron-packager`, read the `--ignore=` [option and many other options](https://electron.github.io/electron-packager/master/interfaces/electronpackager.options.html#ignore) because you don't want to include your other files (or even sensitive files) in the packed `.asar` output. Also use clean CI/workflow to build your application.

[mysticatea/npm-run-all](https://github.com/mysticatea/npm-run-all) helps with `run-p` (parallel) and `run-s` (serial) exec of npm scripts, which helps to organize jobs on npm itself.

[shelljs/shx](https://github.com/shelljs/shx) SHX helps in npm scripts to write *Portable Shell Commands*, like `rm, cp, mkdir, sed,...`  

[IQAndreas/markdown-licenses](https://github.com/IQAndreas/markdown-licenses) helps me to read, choose, and write the [LICENSE.md](LICENSE.md) on this project.

## To Use

To clone and run this repository you'll need [Git](https://git-scm.com) and [Node.js](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com)) installed on your computer. To follow [yacd's guide](https://github.com/haishanh/yacd) of building his awesome react application into static files, you would also need [yarn](https://yarnpkg.com/). From your command line:

```bash
# Clone this repository
git clone https://github.com/ax4/electron-yacd
# Go into the repository
cd electron-yacd
# Install dependencies
npm install
# Make the public folder from source code (clone and build the static files) - or if you understand the prepare steps, manually copy necessary files into ./public folder
npm run make

# Option 1. Run the app (with electron-reloader provides the hot reloading)
npm start

# or Option 2. Build the app into the exectuable
npm run build
```

## Upcoming Todo-s

- [ ] fix the taskbar buttons style in light theme  
- [ ] add the GitHub workflow file and use Github Action to build the program
## License

[MIT by ax4, 2020 @ License.md](LICENSE.md)
