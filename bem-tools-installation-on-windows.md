# bem tools installation on Windows

To work with bem tools you need NodeJS 0.6+ or later and npm.

1. Install [nodejs and npm](http://nodejs.org/) (will be installed together).

2. Install [git](http://git-scm.com/download/win).

3. Open git bash

4. Further you can install bem tools globally or locally for particular project (which is preferable).
Don't pay attention to WARN messages while installation.

4.1. To install bem tools globally use command

``npm -g install bem``

Now bem tools are available as a command line utility. To learn more about it you may use built-in help:

``bem --help``

or [read the doc](http://bem.info/tools/bem/commands/).

4.2. To install it locally you may use project stub or just add bem into project's ``package.json`` like this:
````javascript
{
  "dependencies": {
    "bem": "~0.5.25"
  }
}
````

To get [project stub](https://github.com/bem/project-stub) use this commands:

````
git clone git://github.com/bem/project-stub.git
cd project-stub
npm i
./node_modules/bem/bin/bem server
````

Now you can navigate to http://localhost:8080/desktop.bungles/index/ in the browser. Bem tools will checkout all dependant libraries, build the page and send it to the browser.

So the process of development is as easy as editing source code (adding or removing blocks, etc) and just refreshing the page in the browser. Build system will update changed technologies automatically.