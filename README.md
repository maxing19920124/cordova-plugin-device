# Device插件初始化提前获取uuid 导致华为审核无法通过的解决方案
## 1、调用处
    window['device'].init((res) => {
        this.toolService.alertInfo('device', JSON.stringify(res));
      })
    如果编译该处编译无法通过 可在index.d.ts里手动声明一下，如无编译错误可忽略
<img width="1210" alt="image" src="https://user-images.githubusercontent.com/14306034/187348000-b7b7150b-aff1-421d-88b8-2a3d65dd09ba.png">


## 2、执行 ionic cordova build android --prod --release 编译项目
## 3、编译完成后找到platform下android项目, 按下图找到这两个文件，用modify文件夹处的两个文件相应的做替换,然后即可使用Android studio运行项目

##    <img width="637" alt="image" src="https://user-images.githubusercontent.com/14306034/187348296-f5d15266-df66-475c-a397-3e8b01d11199.png">

