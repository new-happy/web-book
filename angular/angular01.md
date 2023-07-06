# hello angular

## 安装 Angular CLI
你可以使用 Angular CLI 来创建项目，生成应用和库代码，以及执行各种持续开发任务，比如测试、打包和部署。要安装 Angular CLI，请打开终端/控制台窗口，并运行如下命令：

```
npm install -g @angular/cli
```

在 Windows 客户端计算机上，默认禁用 PowerShell 脚本的执行。要允许执行 npm 全局二进制文件所需的 PowerShell 脚本，你必须设置以下内容执行策略

```
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
# 创建工作区和初始应用

你要在 Angular **工作区**的上下文中开发应用。要创建一个新的工作区和初始入门应用：

1.运行 CLI 命令 ng new 并提供 my-app 名称作为参数，如下所示：
```
ng new 项目名称
```
2.ng new 命令会提示你提供要把哪些特性包含在初始应用中。按 Enter 或 Return 键可以接受默认值。

# 运行应用
运行下列命令

```
cd my-app
ng serve --open
```
 # 下一步

 过一遍[英雄之旅教程](https://angular.cn/tutorial/tour-of-heroes)，这是一个完整的动手练习题，它将教你使用 Angular CLI 进行应用开发的过程，并逐步介绍重要的子系统。