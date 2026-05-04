# Test Automation Project - Chat Translator

A comprehensive automated testing suite for the Pixels Suite Chat Translator application using Playwright and Python. This project automates browser testing by reading test cases from Excel files and validating the application's functionality.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Features](#features)
- [Troubleshooting](#troubleshooting)

## 🎯 Project Overview

This automation project tests the **Chat Translator** application with a comprehensive test suite. It:
- Automates browser interactions using Playwright
- Reads test cases from Excel files (`.xlsx`)
- Executes automated tests on the Chat Translator application
- Generates detailed test reports and status summaries
- Supports negative and positive test scenarios

**Application Under Test**: https://www.pixelssuite.com/chat-translator

## 📋 Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Python 3.8+** ([Download Python](https://www.python.org/downloads/))
- **pip** (Python package manager - comes with Python)
- **Git** (for version control - [Download Git](https://git-scm.com/))

## 🚀 Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/lithira-works/ITPM_Assignment-_-01_IT23267190.git
cd ITPM_Assignment-_-01_IT23267190
```

### Step 2: Create a Virtual Environment (Recommended)

```bash
# On Windows
python -m venv venv
venv\Scripts\activate

# On macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

Or install packages individually:

```bash
pip install playwright openpyxl
```

### Step 4: Install Playwright Browsers

After installing the Playwright package, download the necessary browsers:

```bash
playwright install
```

## ⚙️ Configuration

### Environment Variables

You can configure the application URL using environment variables:

```bash
# On Windows
set FRONTEND_URL=https://www.pixelssuite.com/chat-translator

# On macOS/Linux
export FRONTEND_URL=https://www.pixelssuite.com/chat-translator
```

### Excel Test File

Place your test Excel file in the project root directory. The default expected file is:
- `Assignment 1 - Test cases.xlsx`

The Excel file should contain columns for:
- **Input**: Singlish text to translate
- **Expected Output**: Expected Sinhala translation
- **Actual Output**: Where actual results are recorded
- **Status**: Pass/Fail status of the test

## 🎮 Usage

### Run the Main Test Suite

```bash
python test_automation.py
```

### Run with Custom Options

```bash
# Specify custom Excel file
python test_automation.py --excel "path/to/your/test_file.xlsx"

# Specify custom sheet name
python test_automation.py --sheet "Your Sheet Name"

# Run in headless mode (no browser window visible)
python test_automation.py --headless
```

### View Test Cases

To view and understand the test cases structure:

```bash
python read_excel.py
```

This will display:
- Available sheets in the Excel file
- Test case structure
- Total number of test cases
- Sample data from the first 30 rows

## 📁 Project Structure

```
test_automation/
├── README.md                          # This file
├── test_automation.py                 # Main test automation script
├── read_excel.py                      # Excel file reader utility
├── Assignment 1 - Test cases.xlsx     # Test cases (Excel file)
├── AUTOMATED_TEST_STATUS.md           # Current execution status
├── TEST_REPORT.md                     # Test results and report
└── requirements.txt                   # Python dependencies (to be created)
```

## ✨ Features

- ✅ **Playwright-based Automation**: Uses Playwright for cross-browser testing
- ✅ **Excel Integration**: Reads test cases directly from Excel files
- ✅ **Automated Reporting**: Generates detailed test reports
- ✅ **Error Handling**: Comprehensive error handling and logging
- ✅ **Flexible Configuration**: Customizable sheet names, column names, and URLs
- ✅ **Non-headless and Headless Modes**: Run with visible browser or headless
- ✅ **Status Tracking**: Real-time test execution status updates

## 🔧 Troubleshooting

### Common Issues

#### 1. **Playwright Browsers Not Found**
```
Error: Executable doesn't exist at ...
```
**Solution**: Run `playwright install` to download browsers

#### 2. **Excel File Not Found**
```
FileNotFoundError: Assignment 1 - Test cases.xlsx
```
**Solution**: Ensure the Excel file is in the project root directory or specify the correct path using `--excel` option

#### 3. **Module Not Found Errors**
```
ModuleNotFoundError: No module named 'playwright'
```
**Solution**: 
- Ensure virtual environment is activated
- Run `pip install -r requirements.txt` or `pip install playwright openpyxl`

#### 4. **Connection Timeout**
```
TimeoutError: Timeout waiting for connection
```
**Solution**: 
- Check internet connection
- Verify the application URL is accessible
- Check if the application is online

### Enable Debug Mode

To enable verbose logging:

```bash
# On Windows
set DEBUG=1
python test_automation.py

# On macOS/Linux
export DEBUG=1
python test_automation.py
```

## 📊 Test Reports

After running the tests, check:
- **TEST_REPORT.md** - Detailed test results and summary
- **AUTOMATED_TEST_STATUS.md** - Current automation status and execution details

## 🐛 Debugging

### View Application in Real-Time
Run with non-headless mode to see the browser actions:

```bash
python test_automation.py
```

### Check Specific Test Cases
Use `read_excel.py` to inspect test data:

```bash
python read_excel.py
```

## 📝 Requirements.txt

If not present, create a `requirements.txt` file with:

```
playwright==1.40.0
openpyxl==3.10.10
```

To generate from installed packages:

```bash
pip freeze > requirements.txt
```

## 🤝 Contributing

To contribute to this project:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

For issues or questions:
- Check the troubleshooting section above
- Review test reports for error details
- Open an issue on the GitHub repository

## 📄 License

This project is part of an IT assignment. Refer to the repository for license information.

## ✍️ Author

**Student ID**: IT23267190

---

**Last Updated**: May 2026

