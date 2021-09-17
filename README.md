# Dillinger
## _The Last Markdown Editor, Ever_

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>



## 소개

#### 1. 주어진 삶에 적응하라.
#### 2. 피할 수 없다면 즐겨라.
#### 4. 적응한 자만이 살아 남는다.
#### 5. 적극적인 마음자세를 소유하라.
#### 6. 자신의 단점 인지해라.
#### 7. 인격이 성공의 밑천임을 기억하라.
#### 8. 성공은 긍정적인 마음부터 시작된다. 
#### 9. 문제 해결에 정담은 없다, 항상 최선책( 가장 좋고 훌륭한 대책 )으로 해결 하라.  

- 취미: 등산 
- Email: ryu.jiman@gmail.com

## 회사경력 및 역할

- 대교 - MSA 아키텍처 구축(2021.00 ~ ) : MSA 아키텍트 
- SKE - MSA 아키텍처 구축(2021.00 ~ ) : MSA 아키텍트 
- 신세계 - MSA 아키텍처 구축(2021.00 ~ ) : MSA 아키텍트 

## 학력
- 비공개 

## 사용 기술

### MSA Cloud  
- AWS 
- Azure
- GCP 

### DevSecOps
- Docker
- k8s 
- Istio
- Shell Script
- OWASP 
- Argo ( CD )
- Jenkins ( CI ) 
- Jenkins x
- Lens
- Redis 
- Kafka 

### FrontEnd
- Vue.js
- React
- Svelte

### BackEnd
- Spring
- Spring Boot

### DB
- Oracle
- Mysql
- MariaDB

### WAS
- Jeus / webtob 
- Weblogic 
- Websphere
- Tomcat 

### WEB Server
- Apache 
- Nginx 

### Tool
- IntelliJ
- Eclipse
- VSCode

## 프로젝트 이력
### ≪메가존 - 파견 업무≫

#### 대교 - MSA 아키텍처 구축 (SpringBoot, Vue , k8s , Istio )
- 역할 : TA ( AWS Cloud ) , AA
- 담당 : F/W 설계 및 개발 , 공통컴포넌트 설계 및 개발 , Vue.js 설계 및 개발 , 공통 인프라 설계 및 구축 
- 기간 : [2021.00.00 ~ ]

#### 신세계 - EKS 마이그레이션 
- 역할 : TA ( AWS Cloud ) , AA
- 담당 : F/W 설계 및 개발 , 공통컴포넌트 설계 및 개발 , Vue.js 설계 및 개발 , 공통 인프라 설계 및 구축 
- 기간 : [2021.00.00 ~ ]

#### SKE - MSA 아키텍처 구축 (SpringBoot, Vue , k8s , Istio )
- 역할 : TA ( AWS Cloud ) , AA
- 담당 : F/W 설계 및 개발 , 공통컴포넌트 설계 및 개발 , Vue.js 설계 및 개발 , 공통 인프라 설계 및 구축 
- 기간 : [2021.00.00 ~ ]

#### 신세계 - MSA 아키텍처 구축 (SpringBoot, Vue , k8s , Istio )
- 역할 : TA ( AWS Cloud ) , AA
- 담당 : F/W 설계 및 개발 , 공통컴포넌트 설계 및 개발 , Vue.js 설계 및 개발 , 공통 인프라 설계 및 구축 
- 기간 : [2021.00.00 ~ ]


## 교육
