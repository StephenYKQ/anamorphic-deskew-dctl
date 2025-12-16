# Anamorphic Deskew

A DCTL script for correcting image distortion caused by anamorphic skew.

English | [简体中文](README_SC.md)

## ✨ Features

- **Squeeze Ratio Adjustment**: Supports 1.0-2.5x anamorphic lenses
- **Skew Angle Correction**: Shear transformation within ±45° range
- **Manual Scaling**: 0.75-2.0x custom adjustment
- **Auto Edge Crop**: Calculates required scaling to remove black edges
- **Edge Handling Modes**: Stretch edge pixels / Black fill / Pink fill
- **Guide Overlay**: Crosshair + circle with customizable size/thickness/color/opacity


## 📦 Installation

Copy the `.dctl` file to the following directory, restart DaVinci Resolve, then go to Color page → Effects → DCTL and select this file:

**macOS:**
```
/Library/Application Support/Blackmagic Design/DaVinci Resolve/LUT/
```

**Windows:**
```
C:\ProgramData\Blackmagic Design\DaVinci Resolve\Support\LUT\
```

## 📁 Files

```
anamorphic-deskew-dctl/
├── Anamorphic Deskew.dctl       # English version (Recommended)
├── Anamorphic Deskew SC.dctl    # Simplified Chinese version
├── README.md                    # Documentation (This file)
└── README_SC.md                 # Chinese documentation
```

Both versions have identical functionality, differing only in the parameter interface language.


## 💡 Usage Tips

This script uses 2D linear geometric transformation for correction. It corrects offset in the squeeze direction through shear transformation, which only adjusts the horizontal coordinates of pixels.

After shear transformation, the overall image may appear tilted at a certain angle. In this case, you can use the `Rotate` option in DaVinci Resolve's `Input Sizing` to correct it.

It is recommended to use the "Skew Angle" in the DCTL in combination with the `Rotate` in `Input Sizing`, adjusting them iteratively until the image is perfectly vertical.


## 🔄 Changelog

### v1.0.0 (2025-12-16)
- Initial release
- Provides both English and Chinese versions


## 📚 References

This tool is developed based on anamorphic lens optical principles and linear geometric transformation theory. For more technical details, please refer to:
- Yang Kaiqi, Qu Che, Chen Jun. Research on Detection and Image Correction Methods for Assembly-Induced Anamorphic Skew in Film and Television Production[J]. Advanced Motion Picture Technology, 2025,(11):54-61.


## 🤝 Contributing

Suggestions and improvements are welcome!


## 👨‍💻 Author

**Stephen Yang Kaiqi 杨锴埼**
- Website: [https://stecage.com](https://stecage.com)
- GitHub: [https://github.com/StephenYKQ](https://github.com/StephenYKQ)

Copyright (c) 2025 Stephen Yang Kaiqi (杨锴埼). All rights reserved.
