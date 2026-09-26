# 小王科技 - Minecraft 命令与文件转换工具集

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

>  一款基于 Web 的 Minecraft 工具集合，提供 MIDI 音乐转换、图片转换、文本粒子效果等多种实用功能

**作者**: [6小王游戏9](https://github.com/WTW0915)  
**原项目**: [Dislink/dislink.github.io](https://github.com/Dislink/dislink.github.io#)  
**原作者**: [Dislink](https://github.com/Dislink)

这个是ex_evo fork的项目访问连接
https://on445251-bit.github.io/mc-tools/

main fork : https://github.com/WTW0915/mc-tools/tree/main

关闭聊天框指令输出信息提示
/gamerule commandblockoutput false
---

##  项目简介

本项目是一个在线 Minecraft 工具集合网站，集成了多种实用工具，帮助玩家和创作者将 MIDI 音乐、图片、文本等内容转换为 Minecraft 可用的命令方块结构、行为包和结构文件。支持 Java 版和基岩版（BE）平台。

---

## 🗂️ 目录结构

```
mc-tools/
├── EatAncestors/              # 小游戏：吃掉仙人
│   ├── static/
│   │   ├── image/             # 游戏图片资源
│   │   └── music/             # 游戏音效文件
│   └── index.html
├── EatLiYong/                 # 小游戏：吃李咏
│   ├── static/
│   │   ├── image/
│   │   └── music/
│   └── index.html
├── cino/                      # 工具：Cino
── fonts/                     # 字体文件
│   ├── Mojangles.ttf          # Minecraft 风格字体
│   └── unifont-15.1.04.otf    # 统一字体
├── img2mcfunction/            # 工具：图片转 mcfunction
├── javascript/                # 公共 JavaScript 库
│   ├── CBConstructor.js       # 命令方块构造器
│   ├── CBDParser.js           # CBD 解析器
│   ├── FileSaver.js           # 文件保存工具
│   ├── MIDIFile.js            # MIDI 文件解析
│   ├── Math.uuid.js           # UUID 生成器
│   ├── brotli-js.js           # Brotli 压缩
│   ├── jszip.min.js           # ZIP 压缩库
│   ├── nbt.js                 # NBT 数据处理
│   └── palettes.js            # 色彩映射数据
├── link/                      # 链接页面
├── mcfunction2bdx/            # 工具：mcfunction 转 BDX
├── mcfunction2mcstructure/    # 工具：mcfunction 转 mcstructure
├── mcfunctionconvertor/       # 工具：mcfunction 转换器
├── midi2bdx/                  # 工具：MIDI 转 BDX
├── midi2mcfunction/           # 工具：MIDI 转 mcfunction
├── midi2mcstructure/          # 工具：MIDI 转 mcstructure
├── midi2tiles/                # 工具：MIDI 转音符砖块
├── midiconvertor/             # 工具：MIDI 转换器（集成）
├── progressbar/               # 工具：进度条生成器
├── rawJSONEditor/             # 工具：rawJSON 编辑器
├── styles/                    # 全局样式
│   ── main.css               # 主样式表
── text2mcfunction/           # 工具：文本转粒子效果
├── wasmTest/                  # WebAssembly 测试模块
│   ├── r.js                   # 记录器脚本
│   ├── record.js              # 记录器逻辑
│   └── record.wasm            # WebAssembly 模块
├── .keep                      # Git 目录占位文件
├── index.html                 # 网站首页
├── null.html                  # 空白页面
├── favicon.ico                # 网站图标
└── LICENSE                    # Apache 2.0 许可证
```

---

## 🛠️ 工具列表

### 🎵 MIDI 音乐转换工具

| 工具名称 | 功能描述 |
|---------|---------|
| [MIDI 转换器](midiconvertor/) | 将 MIDI 音乐文件转换为 Minecraft 命令方块结构，支持 BDX、mcpack、mcstructure 多种格式输出 |
| [MIDI → mcfunction](midi2mcfunction/) | 将 MIDI 音乐直接转换为 function 音乐文件，可在游戏中播放 |
| [MIDI → BDX](midi2bdx/) | 将 MIDI 转换为 BDX 命令方块数据包，支持播放控制和音效自定义 |
| [MIDI → mcstructure](midi2mcstructure/) | 将 MIDI 转换为 mcstructure 结构文件，生成可导入的 mcpack 安装包 |
| [MIDI → 音符砖块](midi2tiles/) | 将 MIDI 转换为音符盒播放序列，用游戏内的音符盒演奏音乐 |

###  文件格式转换工具

| 工具名称 | 功能描述 |
|---------|---------|
| [mcfunction 转换器](mcfunctionconvertor/) | 批量转换 mcfunction 文件为 BDX 或 mcpack 结构包，支持 CBD 扩展格式解析 |
| [mcfunction → BDX](mcfunction2bdx/) | 将 mcfunction 命令序列打包为 BDX 格式，支持 x/z 轴延伸长度配置 |
| [mcfunction → mcstructure](mcfunction2mcstructure/) | 将命令转换为 mcstructure 结构文件，生成可导入的 mcpack 安装包 |

### 🎨 创作工具

| 工具名称 | 功能描述 |
|---------|---------|
| [图片转 mcfunction](img2mcfunction/) | 将图片像素数据转换为 Minecraft 命令方块序列，支持 JE/BE 平台色彩映射 |
| [文本转粒子效果](text2mcfunction/) | 将文字转换为粒子效果命令，支持描边文字、按行切分、叠加样式配置 |
| [进度条生成器](progressbar/) | 生成带进度条显示的 mcfunction 文件，支持自定义样式、满分值和分段数 |
| [rawJSON 编辑器](rawJSONEditor/) | 可视化编辑 Minecraft raw JSON 文本，支持 § 颜色代码实时预览 |

### 🎮 小游戏

| 工具名称 | 功能描述 |
|---------|---------|
| [吃掉仙人](EatAncestors/) | 一款 Minecraft 风格的反应力游戏，支持普通/无尽/练习多种模式 |
| [吃李咏](EatLiYong/) | 另一款趣味小游戏 |

### 📎 其他工具

| 工具名称 | 功能描述 |
|---------|---------|
| [Cino](cino/) | Cino 相关工具 |
| [链接页面](link/) | 外部链接集合页 |
| [WebAssembly 测试](wasmTest/) | WebAssembly 模块测试页面 |

---

## 📁 重要文件说明

### 核心 JavaScript 库 (`javascript/`)

- **CBConstructor.js**: 命令方块构造器，用于生成 Minecraft 命令方块序列
- **CBDParser.js**: CBD 扩展格式解析器，支持自定义命令格式
- **MIDIFile.js**: MIDI 文件解析器，读取音乐文件中的音符、节奏等数据
- **nbt.js**: NBT (Named Binary Tag) 数据处理库，用于 Minecraft 数据结构操作
- **palettes.js**: 色彩映射数据，包含 Java 版和基岩版的方块颜色对照表
- **jszip.min.js**: ZIP 压缩库，用于生成 mcpack 等行为包文件
- **FileSaver.js**: 文件保存工具，提供浏览器端文件下载功能

### 样式文件 (`styles/`)

- **main.css**: 全局样式表，定义网站主题、响应式布局、动画效果等

### 字体资源 (`fonts/`)

- **Mojangles.ttf**: Minecraft 经典风格字体
- **unifont-15.1.04.otf**: 开源统一字体，支持多语言字符

---

## 📖 使用说明

1. **访问网站**: 打开 `index.html` 或部署到 GitHub Pages
2. **选择工具**: 在首页工具列表中选择需要的功能
3. **上传/输入**: 根据工具要求上传文件或输入内容
4. **转换下载**: 等待转换完成后下载生成的文件
5. **导入游戏**: 将下载的文件导入 Minecraft 使用

---

## 🚀 部署方式

### GitHub Pages 部署

1. Fork 或 Clone 本仓库
2. 进入仓库设置 → Pages
3. 选择 `main` 分支作为源
4. 等待部署完成，访问 `https://用户名.github.io/mc-tools/`

### 本地运行

直接双击 `index.html` 或在本地服务器中打开即可使用。

---

## 📄 许可证

本项目采用 [Apache License 2.0](LICENSE) 许可证。

```
Copyright [2026] [6小王游戏9]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

## 🙏 致谢

- **原作者**: [Dislink](https://github.com/Dislink) - 提供了原始项目基础
- **原项目**: [Dislink/dislink.github.io](https://github.com/Dislink/dislink.github.io#)
- **Minecraft**: Mojang Studios - 游戏及其相关资源
- **开源库**: 本项目使用了多个开源 JavaScript 库

---

## 📧 联系方式

- **GitHub**: [6小王游戏9](https://github.com/WTW0915)
- **项目主页**: [https://github.com/WTW0915/mc-tools](https://github.com/WTW0915/mc-tools)

---

> ⭐ 如果这个项目对你有帮助，欢迎 Star 支持一下！
