# **🎄 Gesture Controlled Christmas Tree (3D 手势交互圣诞树)**

这是一个基于 Web 的沉浸式圣诞体验项目。通过摄像头识别手势，与 3D 粒子圣诞树进行互动。无需鼠标点击，挥挥手即可控制梦境。

## **🎮 核心玩法 (How to Play)**

本项目使用 **MediaPipe** 进行实时手部追踪。请确保您的设备拥有摄像头并允许网页访问。

### **手势控制指南**

| 手势 | 图标 | 功能描述 |
| :---- | :---- | :---- |
| **握拳 (Fist)** | ✊ | **聚合 (Form Tree)**: 所有粒子和照片汇聚成一颗旋转的圣诞树。 |
| **张开手掌 (Open)** | 🖐 | **散开 (Scatter)**: 圣诞树爆炸成星云环绕，照片悬浮在空中。 |
| **捏合 (Pinch)** | 👌 | **抓取 (Focus)**: 选中并放大离视野最近的一张照片进行查看。 |

### **其他功能**

* **📸 自定义照片**: 点击 "上传照片" 按钮，将您与亲友的照片上传到 3D 空间中。  
* **🌍 多语言支持**: 支持中文/英文界面一键切换。  
* **🎵 氛围音乐**: 内置圣诞背景音乐播放,powered by SUNO。  
* **✨ 辉光特效**: 使用 UnrealBloomPass 实现唯美的发光效果。

## **🚀 快速开始 (Quick Start)**

由于项目使用了摄像头权限和 ES6 模块导入，**不能**直接双击 .html 文件打开，必须在本地服务器环境下运行。

### **方法 A: 使用 VS Code (推荐)**

1. 安装 VS Code 插件 **Live Server**。  
2. 右键点击 index.html。  
3. 选择 Open with Live Server。

### **方法 B: 使用 Python**

如果您安装了 Python，可以在项目根目录下运行：

\# Python 3  
python \-m http.server 8000

然后访问 http://localhost:8000

### **方法 C: 使用 Node.js**

npx http-server .

## **🛠️ 技术栈 (Tech Stack)**

* **核心库**: [Three.js](https://threejs.org/) (3D 渲染引擎)  
* **视觉算法**: [MediaPipe Tasks Vision](https://developers.google.com/mediapipe) (手部关键点检测)  
* **后期处理**: Three.js EffectComposer (Bloom 发光特效)  
* **音频**: HTML5 Audio API

## **⚙️ 配置与自定义 (Configuration)**

您可以在 index.html 的 CONFIG 对象中修改参数来调整视觉效果：

const CONFIG \= {  
    primaryParticleCount: 1500,   // 主粒子数量  
    treeHeight: 30,               // 树的高度  
    bloomStrength: 1.8,           // 发光强度  
    colors: \[0x2F4F4F, ...\],      // 粒子配色方案  
    // ...  
};

**Created by AC** | [Twitter/X](https://www.google.com/search?q=https://x.com/ey_axia8)
