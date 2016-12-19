# loopback-study
## 安装  

    npm install strongloop -g
## 创建项目  

    slc loopback
    
下来界面会提示进一步的创建项目的说明步骤...
## 初始目录说明
* server:服务端  
    * server.js:主程序入口  
    * *.json:配置文件  
    * boot文件夹:里面的文件会在项目启动的时候执行，可以看成初始化脚本   
* client:放js文件啊，引用的jquery等...  
* common:client和server的公共文件。其中models子目录包含所有的模型JSON和js文件。

## model建立

    slc loopback:model
    
## 定义远程方法
* 在 /common/models 目录下面创建一个JS文件，文件名为你对应model.json的文件名；例如，你想给Person模型添加一个远程方法，那么你应该在 /common/models 目录下面创建person.js文件。  
* 定义一个静态方法去处理请求。  
* 调用remoteMethod(), 注册远程方法，它有两个参数：  
    * 第一个参数是字符串类型的，它应该是你在第二步新建的静态方法的方法名。  
    * 第二个参数 (可选) ，它给你的REST endpoint提供了一些配置。
             
