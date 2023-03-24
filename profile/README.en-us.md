<p align="center">
  <a href="https://freeeis.aslancer.com" target="_blank">
    <img
      src="https://user-images.githubusercontent.com/33030594/227073920-03ed137f-c4f7-4ed7-ae05-d781dd1991f7.png"
      alt="FreeEIS"
      width="250"
    />
  </a>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/free-be-starter-kit">
    <img src="https://img.shields.io/npm/v/free-be-starter-kit" alt="Version">
  </a>
  <a href="https://www.npmjs.com/package/free-be-starter-kit">
    <img src="https://img.shields.io/npm/dm/free-be-starter-kit" alt="Download">
  </a>
  <a href="https://github.com/didi/LogicFlow/blob/master/LICENSE">
    <img src="https://img.shields.io/npm/l/free-be-starter-kit" alt="LICENSE">
  </a>
</p>

English | [简体中文](/profile/README.md)

[Documntation](https://freeeis.aslancer.com)（In progress……）

FreeEIS is a scalable, enterprise-level unified system development framework. FreeEIS is designed to solve the increasingly popular problem of system disassembly and assembly in remote collaborative development. And by accumulating more and more functional modules, the system is built faster.

## Features

- 🛠 High scalability

  "Everything" can be a module, from a beautiful button, a simple arithmetic function, to a complete ERP system, can be used as a module in FreeEIS. Flexible module splitting, zero coupling between modules, module plug and play. At the same time, considering the extensibility of the module itself, the module can be developed as a "plug-in" for another module.

- 🎯 Focus on business logic

  The FreeEIS kernel prefabricates functions that are not related to business logic, so that developers only need to consider the business logic inside the module, such as module loading, reference dependencies, multi-language support, multi-style support, data model generation, permission management and control, route generation, mock function, etc. have been built into the FreeEIS kernel, and there is no need to consider it during module development. In particular, parts such as data model generation, permission management and control, which usually consume a lot of developers' energy, have also been stripped and decoupled, greatly improving development efficiency.

- 🚀 Quick integration

  All functions in FreeEIS are split into large and small modules, when it needs to be integrated into a complete system, only need to configure the required modules, or put the module code (directory) in a unified location, FreeEIS kernel will automatically load all required modules, and integrate into a complete system. This makes system-level assembly more flexible and can be integrated into complete systems of completely different sizes and functions as quickly as needed.

- 🍹 Do not change development habits

  FreeEIS tries its best to achieve less packaging and no SDK, so as to avoid changing existing development habits. A scaffolding project + a simple set of specifications enables rapid system development.

- 🚪 Code security

  In some scenarios, we don't want all developers to get a lot or even all the code of the functional module before they can run and debug their own functional module. FreeEIS is designed so that developers only need to access the code base of their own functional modules, which can ensure code security without affecting development.


## Usage

### Prerequisites

In the current version, the front-end uses the following technologies or frameworks, which you need to have knowledge of or even experience with:
 - [VUE3](https://vuejs.org/) is the basis for our entire front-end section.
 - [Quasar Framework](https://quasar.dev/) is a VUE-based framework with a variety of features, such as rich components, support for Material Design, support for cross-platform, and so on. However, FreeEIS does not prohibit the use of other component libraries, you can still choose according to your preference, we just use the scaffolding and cross-platform support of the Quasar Framework, and even you can use FreeEIS in other VUE projects that have nothing to do with the Quasar Framework.

In the current version, the backend uses the following technologies or frameworks, which you need to have knowledge of or even experience:
 - [NodeJS](https://nodejs.org/) is the foundation!
 - [ExpressJS](http://expressjs.com/) is the foundation of 😉 the foundation.
 - [MongoDB](https://www.mongodb.com/), [Mongoose](http://www.mongoosejs.net/), The database operation modules that have been implemented so far are based on Mongoose, but we expect to add more database support in the future.
 - [Redis](https://redis.io/), it is recommended to use Redis' docker image deployment.

### Frontend

```sh
# Install front-end scaffolding

$ git clone https://github.com/freeeis/free-fe-starter-kit.git fe

# Install dependent packages
$ cd fe
$ yarn install

# Run
$ yarn start

```

### Backend

Before using the backend, install MongoDB and Redis, or you can use a remotely deployed instance, whose addresses and ports are configured with the relevant built-in modules of FreeEIS. In addition, Redis is not required, if you cannot connect to Redis, FreeEIS will use [memory-cache](https://github.com/ptarjan/node-cache#readme) as a cache, which will not affect development or running.

```sh
# Install back-end scaffolding

$ git clone https://github.com/freeeis/free-be-starter-kit.git be

# Install dependent packages
$ cd be
$ yarn install

# Create files to store confidential data (can also be created manually)
$ touch global.js

# Run
$ yarn start

```

### Access the system

After successfully running the front-end and back-end projects, access the system via the link [http://localhost:8080](http://localhost:8080/). You can also modify the configuration so that the front-end automatically opens the page from the browser after running.

## Built-in function modules

We hope to simplify the work of developers by providing some built-in functional modules, such as account management, permission control, which are required in any system, and we have made modules that can be directly referenced. Below is a list of the built-in feature modules we currently offer, as well as their features. Of course, according to our purpose, we do not force you to use any of the built-in modules, you can customize and develop all the required modules according to your needs, but just use the specifications of FreeEIS and use her to assemble the system. And we encourage you to do so, because we believe that there are many more professional developers in any field than we are, and we want more people to develop more and more powerful functional modules for others to use.


| Module | Front-end module | Backend module | Features | Description|
| :------- |------- |------- | ----|----: |
| Kernel | [free-fe-core](https://github.com/freeeis/free-fe-core) | [free-be-core](https://github.com/freeeis/free-be-core) | Load other modules | added in scaffolding by default |
| Basic features | [free-fe-core-modules](https://github.com/freeeis/free-fe-core-modules) | [free-be-core-modules](https://github.com/freeeis/free-be-core-modules)| Data dictionary, log, menu management, system configuration, <br>error code management, cache management, day of mourning, <br>file handling, data verification methods, <br>multi-language support, multi-skin support, and more | Added in scaffolding by default|
| Account Management | [free-fe-account](https://github.com/freeeis/free-fe-account) | [free-be-account](https://github.com/freeeis/free-be-account) | Account management, organizational structure management, authority <br>management, Role management, permission control| Added in scaffolding | by default
| Database | / | [free-be-mongodb](https://github.com/freeeis/free-be-mongodb) | Database Operations | Added in scaffolding | by default
| Demo Module | [free-fe-demo](https://github.com/freeeis/free-fe-demo) | [free-be-demo](https://github.com/freeeis/free-be-demo) | Demonstrate the internal structure and usage of the module Added in scaffolding | by default


## Contact us

Scan the code to add WeChat to join the communication group

<img width="120" alt="" style="margin-left:24px" src="https://user-images.githubusercontent.com/33030594/227093642-b38b7871-16eb-48b6-b96a-191433dc55c2.png"> 


## Contribute

Although FreeEIS has been verified in many large-scale projects, it is still in its early stages as an open source project and needs the help from all you guys. We welcome any suggestions or comments or contributions, from one-word changes to structural adjustments. We appreciate any donations, PRs, [Issue](https://github.com/freeeis/community/issues) etc., and if you have any related questions, please email us: [[freeeis@xixineis.com] (mailto:freeeis@xixineis.com)]. Thanks 🙏🙏!!
