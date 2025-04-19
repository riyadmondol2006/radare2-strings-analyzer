# Radare2 Android .so Strings Analyzer

A powerful Python script that uses radare2 to analyze Android .so files and extract all strings with their hex memory addresses. Perfect for reverse engineering, malware analysis, and native library inspection.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.6+-blue.svg)
![radare2](https://img.shields.io/badge/radare2-required-green.svg)

## 📁 Table of Contents

- [Features](#features)
- [Author](#author)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Output Structure](#output-structure)
- [Examples](#examples)
- [Use Cases](#use-cases)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## ✨ Features

- 🔍 Analyzes multiple .so files simultaneously
- 📍 Extracts strings with hex memory addresses
- 📄 Generates both text and JSON outputs
- 📊 Creates detailed analysis logs
- 🎯 Removes duplicate strings automatically
- 🚀 Fast batch processing
- 💾 Organized output structure

## 👨‍💻 Author

**Riyad Mondol**

- 📱 Telegram: [https://t.me/reversesio](https://t.me/reversesio)
- 🌐 Website: [http://reversesio.com/](http://reversesio.com/) | [http://reversesio.shop/](http://reversesio.shop/)
- 📧 Email: riyadmondol2006@gmail.com
- 💼 Project Opportunities: [https://t.me/riyadmondol2006](https://t.me/riyadmondol2006)
- 📽️ YouTube: [https://www.youtube.com/@reversesio](https://www.youtube.com/@reversesio)

## 🔧 Prerequisites

- Python 3.6 or higher
- Radare2 installed and available in PATH

### Installing Radare2

#### Linux:
```bash
git clone https://github.com/radareorg/radare2
cd radare2
sys/install.sh
```

#### macOS:
```bash
brew install radare2
```

#### Windows:
Download the installer from [radare2 GitHub releases](https://github.com/radareorg/radare2/releases)

## 📥 Installation

1. Clone this repository:
```bash
git clone https://github.com/riyadmondol2006/radare2-strings-analyzer.git
cd radare2-strings-analyzer
```

2. Make the script executable (Linux/macOS):
```bash
chmod +x RadareSoStringsAnalyzer.py
```

## 🚀 Usage

### Basic Usage

Run the script in the directory containing .so files:
```bash
python3 RadareSoStringsAnalyzer.py
```

### Analyze Specific Directory

```bash
python3 RadareSoStringsAnalyzer.py /path/to/so/files
```

## 📂 Output Structure

The script creates a `string_analysis` directory with the following structure:
```
string_analysis/
├── libandroidx.graphics.path_strings.txt    # Individual file results
├── libBarcodeScannerLib_strings.txt
├── libbugsnag-ndk_strings.txt
├── ...
├── all_strings_YYYYMMDD_HHMMSS.json         # All results in JSON format
└── string_analysis_log_YYYYMMDD_HHMMSS.txt  # Processing log
```

### Output Format

Each string entry contains:
- **HEX ID**: Memory address of the string
- **SIZE**: String size in bytes
- **STRING**: The actual string content

## 📋 Examples

### Text Output Example:
```
File: libandroidx.graphics.path.so
Total strings: 245
Timestamp: 2024-04-20 12:34:56
----------------------------------------------------------------------

HEX ID: 0x00012345
SIZE: 15
STRING: Hello, World!
--------------------------------------------------
HEX ID: 0x00012360
SIZE: 28
STRING: Function initialization failed
--------------------------------------------------
```

### JSON Output Example:
```json
{
  "libandroidx.graphics.path.so": [
    {
      "hex_id": "0x00012345",
      "size": "15",
      "content": "Hello, World!"
    },
    {
      "hex_id": "0x00012360",
      "size": "28",
      "content": "Function initialization failed"
    }
  ]
}
```

## 🔍 Use Cases

- 🔐 Android app security analysis
- 🦠 Malware research
- 🔧 Native library inspection
- 📱 Mobile app reverse engineering
- 🎯 String pattern detection
- 🔍 Memory address mapping

## ❗ Troubleshooting

### Common Issues

1. **Radare2 not found**:
   - Ensure radare2 is installed and in your PATH
   - Test with `r2 -v` command

2. **Permission denied**:
   - Make sure the script has execute permissions
   - Run `chmod +x RadareSoStringsAnalyzer.py`

3. **No .so files found**:
   - Check that you're running in the correct directory
   - Verify the directory contains .so files

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

For project opportunities, feature requests, or collaboration:

- Telegram: [https://t.me/riyadmondol2006](https://t.me/riyadmondol2006)
- Email: riyadmondol2006@gmail.com
- YouTube: [https://www.youtube.com/@reversesio](https://www.youtube.com/@reversesio)

## 🔑 Keywords

Android reverse engineering, radare2 strings analysis, .so file analyzer, hex address extraction, native library inspector, binary analysis tool, malware analysis, mobile security research, strings dumper, memory address mapper, Android library analyzer, binary strings extractor, r2 automation

