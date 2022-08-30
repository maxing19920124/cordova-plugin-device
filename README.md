# Device插件初始化提前获取uuid 导致华为审核无法通过的解决方案
## 1、调用处
    window['device'].init((res) => {
        this.toolService.alertInfo('device', JSON.stringify(res));
      })
    如果编译该处编译无法通过 可在index.d.ts里手动声明一下，如无编译错误可忽略
![img.png](img.png)

## 2、执行 ionic cordova build android --prod --release 编译项目
## 3、编译完成后找到platform下android项目
     ![img_1.png](img_1.png)
     
      按上图找到这两个文件，用modify文件夹处的两个文件相应的做替换
      然后即可使用Android studio运行项目