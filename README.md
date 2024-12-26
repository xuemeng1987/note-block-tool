# **Minecraft Note Block 音符生成工具使用说明**

## **工具简介**
本工具可以将 YouTube 音乐链接自动转换为 Minecraft Note Block 的音符序列，帮助红石音乐玩家快速生成乐谱，无需手动分析音高和节奏。

---

## **功能特点**
1. **自动提取音符**：通过分析音频文件的主要音高，生成符合 Note Block 频率范围的音符。
2. **支持节奏识别**：根据音乐的时间轴，生成精准的音符播放时间。
3. **多种输出格式**：支持音符列表、JSON 文件，以及直接用于 Minecraft 的命令。
4. **便捷操作**：只需输入 YouTube 链接，一键生成结果。

---

## **使用步骤**

### **1. 准备环境**
运行本工具需要以下依赖：
- Python 3.8 或更高版本
- 依赖库：
  ```bash
  pip install pytube librosa numpy scipy
  ```

### **2. 下载工具**
将工具代码保存到本地文件，例如 `note_block_tool.py`。

### **3. 输入 YouTube 链接**
运行以下命令：
```bash
python note_block_tool.py
```
程序会提示你输入 YouTube 视频链接。例如：
```
请输入 YouTube 音乐链接: https://www.youtube.com/watch?v=example
```

### **4. 等待处理**
程序会自动下载音频并进行分析。处理完成后，会输出一个音符序列文件，例如 `note_sequence.txt`。

### **5. 查看输出**
打开生成的文件（如 `note_sequence.txt`），内容如下：
```
Note: 49
Note: 52
Note: 55
...
```
每一行代表一个音符，数字为对应的 Note Block 频率。

---

## **进阶功能**

### **1. 自定义输出路径**
可以在运行时指定输出文件路径，例如：
```bash
python note_block_tool.py --output notes.json
```

### **2. 支持多格式输出**
默认输出为 `.txt`，也可以修改为 JSON 格式或直接生成 Minecraft 命令。

### **3. 节奏优化**
如果想生成带有节奏的音符序列，可以设置节奏检测参数：
```bash
python note_block_tool.py --timing true
```

---

## **注意事项**
1. **音频版权**：确保你下载的音频不会侵犯版权，仅供个人使用。
2. **音频复杂度**：此工具对简单旋律效果最佳，复杂的和弦或多声部音乐可能需要手动调整。
3. **Note Block 限制**：Minecraft Note Block 的音符范围为 25 个音高，超出范围的音符会自动调整。

---

## **常见问题**

### Q: 为什么生成的音符和原曲不完全匹配？
A: Note Block 的音符范围有限，部分音符可能会被自动调整到更接近的频率。此外，复杂和弦可能无法完全还原。

### Q: 如何调整生成音符的速度？
A: 可以修改代码中的时间间隔参数，或在输出后手动调整节奏。

### Q: 支持哪些操作系统？
A: 本工具支持 Windows、macOS 和 Linux。

---

## **版本信息**
- 当前版本：1.0.0
- 开发者：xuemeng1987(Shiroko)

如有问题或建议，请联系开发者邮箱：your_email@example.com
