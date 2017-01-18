# node安装
## 进入官网
## 在相应的平台下，下载相应的版本，一个是稳定版，一个是最新版
**学习者可以下载最新半年，上线者下载稳定版，偶数是稳定版，奇数是最新版**
## 安装
### windows安装
1.  下载相应的安装文件，用两种安装包，一个是node.exe,一个是node.msi.node.msi包含了node.exe、npm，node.exe要添加到全局路径下，要选择 add to path ，将node.exe自动添加到全局路径下。安装成功后，可以命令行操作node -v 检测安装的版本。


#npm
1. 包管理工具  node package manage ，安装成功后，命令行 npm -v 检测安装是否成功，以及版本号。
2. 为了程序人员开发方便，给我们提供了一个管理包，不用担心你的模块和数据是否被别人看到，


#执行第一个程序
## 交互式方式运行node.js
1. node 回车，进入编译环境，ctrl+c退出编译环境。
2. 输入符合node.js语法的语句，回车后会立即得到结果，对你你输入的命令来进行相应。

##编译型运行node.js
1. 创建一个js文件
2. 在命令行进入文件所在的目录，通过 node node.js 来对这个js文件进行解析和执行。


#node.js运行环境的配置
## phpstrom 来配置node.js的环境
1. 打开配置项目，
      **webstrom不用配置，已经配置好相应的环境**
2. 打开plugins搜索node.js，找到安装，完成后重启编译器，重启后打开配置项
3. 在framework下能找到node and npm 。插件已经安装成功。
4. 首先让他可用，选择提示语言。


#node.js语法
**遵从ecmascript 6 语法内容**
1. 定义常量 const a=10;


#node.js全局对象

##js全局对象是window
1. node.js里有一个全局对象，global

###global的子对象
1. console

    1.1 console.log() 可以接受很多参数  在控制台输出消息  
    1.2 console.error() 在控制台输出一条错误的消息   
    1.3 console.time() 在程序运行前调用，记录当前的信息  
    1.4 console.timeEnd() 在程序运行完成后调用，也来记录程序完成后的信息  
    1.5 console.trace() 追踪程序中的堆栈的运行情况，用的少
    
2. modules

    2.1 概念  
        模块是node.js 区别于js最重要的概念，把每个文件都当做独立的作用域，每一文件就是一个模块，在当前模块下定义的所有变量或函数，都是属于该模块的，如果想定义全局的，必须通过global，在模块下定义的变量的作用范围只能在模块范围内，在global下定义的变量或函数，，具有全局的作用范围。   

    2.2 module exports 联系
        module.exports===exports 能够将当前模块下的值反射出去，让引用的模块获取相应的值 

        **二者为引用关系，如直接赋值，会导致联系断开**   

    2.3 在node.js中会分为三种模块，  
        2.3.1 自定义模块   
        2.3.2 内置模块   
        2.3.3 外部模块（包）

3. process
	用来操作或者是获取或者查看当前进程的相关信息

    3.1 stdin 标准的输入流，可以监控控制台输入的东西，
        事件 “data” process.stdin.on("data",fn)  
            主动触发事件 process.stdin.emit()   
            暂停 process.stdin.pause()      
            重启 process.stdin.remuse()   
 
        stdout 标准的输出流   二者都属于进程的对象  
    3.2 argv 用来获取命令行相关的参数【“执行的二进制文件”，“当前运行的文件”】  
    3.3 chdir（）改变进程运行的目录   
    3.4 cwd（）当前进程所在目录

4. setInterval()
5. clearInterval()
6. setTimeout()
7. clearTimeout()
8. require("输入一个路径") 引入其他模块   
    require.cache  记录了当前文件所引用的所有的模块  
    require.resolve（"./node.js"）  将引用模块的相对路径转化为绝对路径

### 魔术常量

1. __dirname 当前文件运行的目录
2. __filename 当前运行的文件名

##node.js方法的稳定等级
0  废弃     已经废弃，不能使用  
1  试验     正在试验阶段，不建议使用，并可能随时废弃  
2  不稳定   在某些平台可以用，不稳定，不建议使用，时刻关注更新或废弃  
3  稳定     进入稳定阶段。即使改动也是改动底层的接口和性能，不影响使用  
4  冻结     已经很稳定，可以投入项目使用  
5  锁定     很长时间内不会升级/迭代，不接受修改（除非有大bug）
    

    

