# Anamorphic Deskew

一个用于校正变形镜头偏斜导致图像畸变的 DCTL 脚本。

[English](README.md) | 简体中文

## ✨ 功能

- **压缩比调节**：支持 1.0-2.5x 变形镜头
- **偏斜角度校正**：±45° 范围内的剪切变换
- **手动缩放**：0.75-2.0x 自定义调节
- **自动边缘裁剪**：计算裁切所需缩放比例，去除黑边
- **边缘处理模式**：拉伸边缘像素/黑色填充/粉色填充
- **辅助线显示**：十字线+圆形，可自定义大小/粗细/颜色/透明度


## 📦 安装方法

将 `.dctl` 文件复制到以下目录，重启达芬奇，然后进入调色页面 → 效果 → DCTL，选择此文件：

**macOS:**
```
/Library/Application Support/Blackmagic Design/DaVinci Resolve/LUT/
```

**Windows:**
```
C:\ProgramData\Blackmagic Design\DaVinci Resolve\Support\LUT\
```

## 📁 文件说明

```
anamorphic-deskew-dctl/
├── Anamorphic Deskew.dctl       # 英文版（推荐）
├── Anamorphic Deskew SC.dctl    # 简体中文版
├── README.md                    # 英文说明文档
└── README_SC.md                 # 中文说明文档（本文件）
```

两个版本功能相同，仅参数界面语言不同。


## 💡 使用提示

本脚本采用二维线性几何变换进行校正。通过剪切变换校正压缩方向的偏移，该变换仅调整像素的水平坐标。
剪切变换后，图像整体可能呈现一定角度的倾斜。此时可使用达芬奇的 `Input Sizing` 中的 `Rotate` 校正。
建议在调整时，将 DCTL 中的"偏斜角度"与 `Input Sizing` 的 `Rotate` 配合使用，反复微调至画面完全垂直。


## 🔄 更新日志

### v1.0.0 (2025-12-16)
- 初始版本发布
- 提供英文和中文两个版本


## 📚 参考资料

本工具基于变形镜头光学原理和线性几何变换理论开发。更多技术细节请参考：
- 杨锴埼,屈澈,陈军.影视制作中变形镜头装配偏斜检测及画面校正方法研究[J].现代电影技术,2025,(11):54-61.


## 🤝 贡献

欢迎提出建议和改进意见！


## 👨‍💻 作者

**Stephen Yang Kaiqi 杨锴埼**
- Website: [https://stecage.com](https://stecage.com)
- GitHub: [https://github.com/StephenYKQ](https://github.com/StephenYKQ)

Copyright (c) 2025 Stephen Yang Kaiqi (杨锴埼). All rights reserved.
