# Device插件初始化提前获取uuid 导致华为审核无法通过的解决方案
## 1、调用处
    window['device'].init((res) => {
        this.toolService.alertInfo('device', JSON.stringify(res));
      })
    如果编译该处编译无法通过 可在index.d.ts里手动声明一下，如无编译错误可忽略
<img width="1210" alt="image" src="https://user-images.githubusercontent.com/14306034/187348000-b7b7150b-aff1-421d-88b8-2a3d65dd09ba.png">


## 2、执行 ionic cordova build android --prod --release 编译项目
## 3、编译完成后找到platform下android项目
     <img width="1141" alt="image" src="https://user-images.githubusercontent.com/14306034/187348051-09a8db5e-a349-4a61-888a-8fbfc3dfc122.png">

     
      按上图找到这两个文件，用modify文件夹处的两个文件相应的做替换
      然后即可使用Android studio运行项目
