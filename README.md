前端开发环境搭建简明教程
======

前端初学者，或者老鸟在重装系统，或者配置持续集成环境时，不可避免地需要配置 nodejs 运行环境，我们在这里简单说说如何搭 nodejs 环境，并带你绕过很多前人遇到的坑。

- 安装 nodejs。
  - Windows 或者 macOS 用户请访问 [nodejs 官网下载](https://nodejs.org/en/download/)安装包(优先64位LTS版本)，
  - 其他操作系统建议使用系统内的[包管理器安装](https://nodejs.org/en/download/package-manager/)
- 配置国内 npm 镜像。直接在命令行输入命令：
  ```bash
  npm i -g mirror-config-china
  ```
  > 后文提到的NVM和很多node包(Electron、node-sass等)都有从CDN下载可执行文件的操作，设置镜像地址可大大加快国内下载速度
- 安装 git
  - Windows 用户请使用命令：
    ```bash
    npm i -g git-win
    ```
  - macOS用户请前往[官网下载安装包](https://git-scm.com/download/mac)
  - 其他系统可按[官网建议](https://git-scm.com/download/linux)使用包管理器安装
- 安装 NVM
  ```bash
  curl -o- https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
  ```
  > Windows 10 用户可以在WSL内安装，其他Windows用户可以跳过此步骤
- 安装node编译工具
  - Windows 用户请在管理员权限下运行：
    ```bash
    npm i -g windows-build-tools
    ```
  - 其他操作系统用户请按照[官网建议](https://github.com/nodejs/node/blob/master/BUILDING.md#unixmacos)安装
  > 有的node包(如node-sass)需要在CDN下载二进制文件失败，或者干脆没有提供预编译文件时，在本地编译，这时需要安装编译工具。
- 扩展windows命令行的功能，以便兼容linux风格的命令。（npm i -g git-bash-shell）
