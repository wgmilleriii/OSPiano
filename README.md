# OSPiano

The world's first completely free, open-source 3D printable piano.


[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

OSPiano is a crowd-supported and designed piano, created to be 3D printed and playable.


# Features

  - Only Open-sourced software is used
  - STLs and OpenSCAD preferred

### Tech

OSPiano uses a number of open source projects to work properly:

* [AngularJS] 
* [Ace Editor] 
* [markdown-it] 
* [Twitter Bootstrap] 
* [node.js] 
* [Express] 
* [Gulp] 
* [jQuery] 

And of course OSPiano itself is open source with a [public repository][dill]
 on GitHub.

### Installation

OSPiano requires [Node.js](https://nodejs.org/) v4+ to run.

Install the dependencies and devDependencies and start the server.

For production environments...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

OSPiano is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


### Development

Want to contribute? Great!

OSPiano uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma test
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
OSPiano is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd OSPiano
docker build -t wgmilleriii/OSPiano:${package.json.version} .
```
This will create the OSPiano image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of OSPiano.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/OSPiano:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/wgmilleriii/OSPiano/blob/master/KUBERNETES.md)


### Todos

 - Write MORE Tests
 - Add Night Mode

License
----

MIT


**Free Software**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/wgmilleriii/OSPiano>
   [git-repo-url]: <https://github.com/wgmilleriii/OSPiano.git>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/wgmilleriii/OSPiano/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/wgmilleriii/OSPiano/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/wgmilleriii/OSPiano/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/wgmilleriii/OSPiano/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/wgmilleriii/OSPiano/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/OSPiano/blob/master/plugins/googleanalytics/README.md>
