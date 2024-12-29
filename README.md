# Visualizer
You can copy them instead of using for business.
Borrowed from **https://github.com/hh-1106/EveOneSketch/tree/main/easing** and modified and innovated, this program uses the MPL-2.0 license, and I hope to continue the open source spirit.

Visualizer 是一个基于 Processing 框架的音频可视化项目，旨在通过图形效果展示音频的节奏和波形。Processing 是一个灵活的软件素描本和语言，适用于学习如何编码的初学者以及希望以视觉艺术形式编程的专业人士。Visualizer 项目利用了 Processing 的强大图形处理能力，并结合了 Minim 音频库来处理和分析音频文件。这个项目不仅展示了音频的可视化效果，还提供了丰富的互动功能，使你能够通过简单的操作体验到音频与视觉艺术的融合。

## 项目功能

Visualizer 项目包括以下几个主要功能：

1. **音频加载和播放**：项目能够从指定的目录加载多种格式的音频文件，包括 `.mp3`, `.wav`, `.au`, 和 `.flac` 文件。你可以通过按键实现音频文件的切换和控制。项目还支持将 FLAC 文件转换为 WAV 文件，以便播放。

2. **节拍检测**：项目使用 Minim 库中的 `BeatDetect` 类来检测音频中的节拍，包括鼓点、刮擦声和高帽声等。通过检测到的节拍，项目会触发相应的图形效果，使图形与音频同步，增强视觉体验。

3. **图形渲染**：项目根据音频的节拍生成和渲染多种图形效果，包括动态多边形和弧线。这些图形效果会随着音频的节奏实时变化，创造出丰富的视觉效果。你可以通过调整代码中的参数来改变图形的形状、大小和颜色，从而实现个性化的视觉效果。

4. **颜色模式切换**：你可以通过鼠标左击在黑白模式和彩色模式之间切换。黑白模式下的图形效果主要以白色呈现，而彩色模式则以随机颜色呈现，增强了视觉表现力和互动性。

5. **后处理效果**：项目支持自定义的后处理效果，你可以根据需要在代码中添加和调整这些效果，以达到特定的视觉效果。后处理效果可以包括模糊、色彩调整、边缘检测等，进一步提升图形的视觉冲击力。

## 依赖项

Visualizer 项目依赖以下几个库和工具：

1. **Processing**：作为项目的基础框架，Processing 提供了强大的图形处理能力和简洁的编程接口。你需要安装 Processing 环境来运行项目。

2. **Minim 音频库**：Minim 是一个功能强大的音频库，支持音频的加载、播放和分析。项目中使用 Minim 来处理音频文件并进行节拍检测。

3. **Jaffree 库**：Jaffree 是一个用于音频和视频处理的 Java 库，项目中使用它来将 FLAC 格式的音频文件转换为 WAV 格式，以便于播放。

## 操作指南

以下是项目的详细操作指南，帮助你正确运行和使用 Visualizer 项目。

### 环境配置

1. **安装 Processing**：从 [Processing 官方网站](https://processing.org/download/) 下载并安装最新版本的 Processing 软件。

2. **下载项目文件**：将 Visualizer 项目克隆到本地计算机。你可以使用以下命令将项目克隆到本地：
   ```shell
   git clone https://github.com/ChenLX233/Visualizer.git
3. **安装 Minim 库**: 在 Processing 软件中，打开“Sketch”菜单，选择“Import Library...”，然后选择“Add Library...”。在弹出的窗口中搜索 Minim 并点击安装。

4. **安装 Jaffree 库**: Jaffree 库在“code”文件夹中已就绪，所以请确保你下载了完整的文件并且程序能够访问其中的.jar文件。

5. **你应该保证程序目录是这样的：**
Visualizer/                                                                                                                                                               
├── README.md                                                                                                                                                                           
├── Visualizer/                                                                                                                                                                                 
│         ├── Visualizer.pde                                                                                                                                                                        
│         ├── song1.mp3                                                                                                                                                                        
│         ├── song2.flac                                                                                                                                                                        
│         ├── song3.wav                                                                                                                                                                           
│         └── code/                                                                                                                                                                                 
│             ├── jaffree-2024.08.29.jar                                                                                                                                                                                 
│             ├── slf4j-api-2.0.16.jar                                                                                                                                                                  
│             └── slf4j-simple-2.0.16.jar                                                                                                                                                         
**请务必在.pde文件同目录下添加任意包括 `.mp3`, `.wav`, `.au`, 和 `.flac` 的音乐文件**

## 运行项目

### 打开项目文件

在 Processing 软件中，打开 `Visualizer/Visualizer.pde` 文件。这是项目的主文件，包含了所有的核心代码。

### 运行项目

点击 Processing 软件界面左上角的“Run”按钮，项目将开始运行。程序会自动从当前目录加载音频文件并开始播放和可视化。

## 你交互

### 鼠标点击

你可以通过点击鼠标在黑白模式和彩色模式之间切换。每次左击鼠标，图形效果的颜色模式会发生改变，从而提供不同的视觉体验。

### 按键操作

- **按键 `N` 或 `n`**：播放下一首音频文件。当你按下 `N` 键时，程序会停止当前的音频播放并加载下一首音频文件进行播放。
- **按键 `P` 或 `p`**：播放上一首音频文件。当你按下 `P` 键时，程序会停止当前的音频播放并加载上一首音频文件进行播放。

## 总结

Visualizer 项目展示了如何结合音频处理和图形渲染，创造出丰富的视觉效果。项目不仅适用于实际应用场景，还可以作为学习和研究的工具，帮助你理解和掌握音频可视化的技术和原理。通过详细的操作指南和示例，你可以轻松运行和使用该项目，体验音频和视觉效果的完美结合。

希望这份详细的介绍与使用说明能够帮助你更好地理解和使用 Visualizer 项目。如果你有任何问题或需要进一步的帮助，请访问 [Processing 官方网站](https://processing.org/) 或 [Minim 音频库](http://code.compartmental.net/tools/minim/) 获取更多信息与支持。
