# TEST AUTOMATION REPORT - ASSIGNMENT 1

## Test Automation Summary

**Date**: May 3, 2026  
**Test Suite**: Assignment 1 - Chat Translator  
**Test Framework**: Playwright + Python  
**Browser**: Chrome (Chromium 147.0.7727.15)  
**Status**: RUNNING - Automated Testing in Progress

---

## Test Data Overview

### Excel File Information
- **File**: Assignment 1 - Test cases.xlsx
- **Sheet**: " Test cases"
- **Total Test Cases**: 999 negative test cases
- **Test Case Format**: Neg_0001 to Neg_0999
- **Columns**: Test Case ID | Input length type | Input | Expected output | Actual output | Status

### Test Case Categories
- **Input Types**:
  - S (Short) - Single phrase/sentence
  - M (Medium) - Multiple phrase/sentences
  
### Test Scope
- **Application Under Test**: https://www.pixelssuite.com/chat-translator
- **Functionality**: Singlish to Sinhala transliteration
- **Test Type**: NEGATIVE TESTS (all tests marked as Neg_XXXX)

---

## Automation Setup

### Infrastructure Installed
✅ Playwright (Sync API)  
✅ Chrome for Testing v1217  
✅ Chrome Headless Shell  
✅ Firefox, WebKit, FFmpeg (for future test compatibility)  
✅ OpenPyXL (Excel file handling)  

### Automation Process Flow
1. **Initialize Browser**: Launch Chrome (non-headless mode - browser UI visible)
2. **Navigate to Application**: Load chat-translator webpage
3. **Detect UI Elements**: Identify input textarea (Singlish) and output textarea (Sinhala)
4. **For Each Test Case**:
   - Input: Singlish text from Excel column C
   - Action: Click transliterate button
   - Wait: 5000ms for processing
   - Capture: Sinhala output from textarea
   - Compare: Actual output vs Expected output (Column D)
   - Record: Status (PASS/FAIL/COLLECTED) in Excel
5. **Save Results**: Automatically update Excel file with results

---

## Sample Test Cases (First 25 of 999)

| Test ID | Input Type | Singlish Input | Expected Sinhala Output | Status |
|---------|-----------|-----------------|------------------------|--------|
| Neg_0001 | S | kohomadhaa oyaaa enne? | කොහොමද ඔයා එන්නේ? | Running... |
| Neg_0002 | M | aiyoo mokadda me wela thiyena prashne kiyala kiyannako? | අයියෝ මොකක්ද මේ වෙලා තියෙන ප්‍රශ්නෙ කියලා කියන්නකෝ? | Running... |
| Neg_0003 | S | wahama methanin yanna! | වහාම මෙතනින් යන්න! | Running... |
| Neg_0004 | M | karunakara meka wahaama ahakin thiyanna kiyala mama kiwwa! | කරුණාකර මේක වහාම අහකින් තියන්න කියලා මම කිව්වා! | Running... |
| Neg_0005 | S | suba udesanak wewaaa! | සුබ උදෑසනක් වේවා! | Running... |
| Neg_0006 | M | ayubowan yaluwe, oyata subama suba aluth awuruddak wewa! | ආයුබෝවන් යාලුවේ, ඔයාට සුබම සුබ අලුත් අවුරුද්දක් වේවා! | Running... |
| Neg_0007 | S | poddak methanata enawada? | පොඩ්ඩක් මෙතනට එනවද? | Running... |
| Neg_0008 | M | ane machan karunakarala mage me podi wede tikak balala dennako. | අනේ මචන් කරුණාකරලා මගේ මේ පොඩි වැඩේ ටිකක් බලලා දෙන්නකෝ. | Running... |
| Neg_0009 | S | ow ow mama ennam. | ඔව් ඔව් මම එන්නම්. | Running... |
| Neg_0010 | M | hari ayiye, oyage uththareta godak sthuthi, eka heta karannam. | හරි අයියේ, ඔයාගේ උත්තරේට ගොඩක් ස්තූතියි, එක හෙට කරන්නම්. | Running... |

---

## Automation Execution Details

### Test Configuration
```
Script: test_automation.py
Excel File: Assignment 1 - Test cases.xlsx
URL: https://www.pixelssuite.com/chat-translator
Mode: NON-HEADLESS (Chrome visible)
Wait Time: 5000ms per test
Type Delay: 30ms per character
Retries: 8 attempts to capture output
Timeout: 60000ms per operation
```

### Test Execution Progress
- **Test Rows**: 999 test cases (Row 2 to Row 1000)
- **Chrome Browser**: OPEN and RUNNING
- **Current Status**: Tests are being executed with automated output capture
- **Estimated Duration**: ~60-90 minutes for full suite (999 tests × 5-10 sec per test)

---

## Test Results Collection Method

### Automated Output Capture
Each test case performs the following:

1. **Input Entry**: 
   - Clear previous input
   - Type Singlish text with 30ms delay per character
   - Verify text entered correctly

2. **Output Retrieval**:
   - Click Transliterate button
   - Wait 5 seconds for response
   - Attempt up to 8 retries if output not visible
   - Extract Sinhala output from textarea

3. **Status Recording**:
   - **PASS**: Actual output matches Expected output
   - **FAIL**: Actual output differs from Expected output
   - **COLLECTED**: No expected output to compare (data collection mode)
   - **UI Error**: Error during interaction

4. **Excel Update**:
   - Actual output automatically written to column E
   - Status automatically written to column F
   - File saved after all tests complete

---

## Key Features of Automation

✅ **Full Automation**: Zero manual intervention required  
✅ **Chrome UI Visible**: Real-time observation of testing process  
✅ **Robust Element Detection**: Multiple strategies to find input/output elements  
✅ **Comprehensive Logging**: Each test logged to console and Excel  
✅ **Error Handling**: Graceful handling of UI errors and timeouts  
✅ **Auto-Save**: Excel file automatically updated throughout testing  
✅ **Negative Test Suite**: All 999 tests are negative test cases  

---

## Sample Output Log

```
Starting Frontend-Only test with 999 rows...
Frontend loaded successfully.
Testing [Row 2]: kohomadhaa oyaaa enne?
  -> FAIL
Testing [Row 3]: aiyoo mokadda me wela thiyena prashne kiyala kiyannako?
  -> FAIL
Testing [Row 4]: wahama methanin yanna!
  -> PASS
[...continuing 996 more tests...]
```

---

## Test Completion Criteria

The automation will:
1. Process all 999 test cases
2. Capture actual output for each test
3. Compare against expected output
4. Record PASS/FAIL/COLLECTED status
5. Save all results to Excel file
6. Display final statistics

---

## Results Location

**Output File**: `Assignment 1 - Test cases.xlsx`  
**Updated Columns**:
- Column E: Actual output (captured from translator application)
- Column F: Status (PASS/FAIL/COLLECTED/UI Error)

---

## Notes

- All test cases are **NEGATIVE TESTS** (Neg_0001 to Neg_0999)
- Tests include various input types: short phrases, long sentences, mixed text with English words
- Application is tested for transliteration accuracy
- Results provide both quantitative (Pass/Fail counts) and qualitative (actual vs expected output) data

---

**Test Status**: 🔄 IN PROGRESS - Chrome automation running  
**Report Generated**: May 3, 2026  
**Next Update**: Upon test completion
