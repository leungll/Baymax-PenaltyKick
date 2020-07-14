# 基于图形引擎的软件开发-期末课设
**Baymax-PenaltyKick** for Software Development Based on Graphics Engine, Spring 2020, NENU 

![Passing](https://img.shields.io/badge/JavaScript-passing-red)
![Server](https://img.shields.io/badge/Server-Apache24-success)
![IDE](https://img.shields.io/badge/IDE-Microsoft%20VS%20Code%20x64-yellow)
![Version](https://img.shields.io/badge/version-v2.0-orange)
![License](https://img.shields.io/badge/License-Apache%202.0-blue)

## 基本需求
>部署一个场景，场景内有物体运动，可以切换视角

## 实现功能
- 使用 `WebGL` 搭建三维场景
- 视角切换：相机控件 `OrbitControls`，对场景进行缩放、旋转操作
- 纹理贴图：给场景内的物体、人物贴上纹理，呈现立体感
- `Group` 组件：使用 `Group` 组装 `BayMax` ，实现整体运动
- 键盘事件
    - `addEventListener` 监听键盘按键
    - `Enter` 键：控制大门开关
    - `UP`、`DOWN` 键：`BayMax` 绕 `Z` 轴平移
    - `LEFT`、`RIGHT` 键：`BayMax` 绕 `X` 轴平移
- 鼠标事件
    - 视角切换：
        - 按住 `鼠标左键` ，拖动场景旋转，实现观察视角切换
        - `鼠标中键滚轮`，对场景进行缩放操作
    - 画面右方面板
        - 控制足球 `自动旋转`，`停止旋转`
        - 控制 `BayMax` 移动

## 开发环境
* System: Win10
* IDE: Microsoft VS Code x64 1.44.2
* Server: Apache24
* 3D-Engine: Three.js

## 相关资源
- Three.js库：路径 `Baymax-PenaltyKick/js`
    - 完整的 `Three.js库`：https://github.com/mrdoob/three.js/
- 服务器配置：见文档 `Apache安装及配置.docx`

## 编译 & 运行
- 将项目 `Baymax-PenaltyKick` 放在本地服务器下
- 浏览器访问端口：`localhost:你的本地端口号/Baymax-PenaltyKick/index.html`

## 设计思路
> 程序的设计灵感来源于在自学 `WebGL` 编程时，偶然在网上看到一些 [博主](https://blog.csdn.net/u014529917/article/details/82801737) 搭建的 `3D` 室内场景，觉得效果很酷炫，于是照葫芦画瓢，参照网上的代码框架，自己尝试搭建一个室内场景。
- 框架搭建：首先在场景中建立基本模型，添加房间、墙等基本元素，并调整位置
- 添加物体：使用 `Group` 组件绘制 `Baymax`，绘制足球
- 纹理贴图：在墙面上添加大门、海报等带有足球元素的图片
- 加入视角切换、键盘控制、鼠标控制，实现对物体的运动操作

## 页面截图
- 初始页面

    ![initial-page](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/initial-page.jpg)
- 俯瞰场景

    ![overlook](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/overlook.jpg)
- `Baymax` 罚点球

    ![penalty-kick](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/penalty-kick.jpg)
- 进门视角

    ![enter-door](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/enter-door.jpg)
- 进门视角2

    ![enter-door2](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/enter-door2.jpg)

## 待改善之处
- 键盘事件存在瑕疵：当按下 `UP`、`DOWN`、`LEFT`、`RIGHT` 键控制 `Baymax` 移动时，页面也会上下左右移动，影响体验。
- 无法引进 `3D模型` ：尝试在场景中加载 `东京小屋` 模型，经过几天尝试，会出现黑屏、无法加载等 bug，未果。希望有时间能继续改善。

    ![东京小屋](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/tokyo.jpg)

## References
- [WebGL中文网](http://www.hewebgl.com/)
- [three.js Github库](https://github.com/mrdoob/three.js/)
- [jiym. 使用three.js搭建室内场景. 2018. CSDN](https://blog.csdn.net/u014529917/article/details/82801737)