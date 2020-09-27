# umi-subapp-cli

> Umi 子应用脚手架

最近由于工作需要，在搞基于 `umi` 的前端中台，我们平台组负责搭建基座应用，其他项目组负责开发子应用。

子应用需要接入到基座应用，这需要一些配置。为了减少不必要的麻烦，我们基于 `@umijs/umi-app` 脚手架创建的工程进行预配置，将工程与配置一并提供给项目组，使得项目组拿到手的就是无需配置即可接入主应用的工程。

由于工程模板非常固定无需灵活，因此我们目前的方式是：提供工程模板的 `Gitlab` 仓库地址，让项目组自行下载。

那如果相对灵活呢，多配置呢？因此思考能不能像 `Vue/React` 一样，提供一个脚手架，让各个项目组他们自己去创建，这就是这个项目的由来。

| 依赖              | 用途                                             |
| ----------------- | ------------------------------------------------ |
| chalk             | 可以给终端的字体加上颜色                         |
| commander         | 可以自动的解析命令和参数，用于处理用户输入的命令 |
| download-git-repo | 下载并提取 github 仓库，用于下载项目模板         |
| inquirer          | 通用的命令行用户界面集合，用于和用户进行交互     |
| ora               | 下载过程久的话，可以用于显示下载中的动画效果     |