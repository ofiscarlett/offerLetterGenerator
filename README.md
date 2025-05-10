==============================
 Offer Letter Generator (錄用通知單產生器)
==============================

📁 Folder Structure
---------------------
.
├── newCreater.html    ← Main HTML interface
├── Notify onboard form_template_git.docx   ← Word template with {{variables}}
└── libs/
    ├── jszip.min.js
    ├── FileSaver.min.js
    └── mammoth.browser.min.js


📌 Description (說明)
---------------------
This tool allows you to:
1. Upload a Word .docx template containing placeholders.
2. Fill in input fields such as name, date, job title, base salary.
3. Preview the document directly in the browser.
4. Download a filled-in Word file with the placeholders replaced.

本工具功能：
1. 上傳一個含有變數的 Word 樣板 (.docx)
2. 輸入相關的變數資料如姓名、報到日期、職稱、本薪
3. 預覽文件內容
4. 下載自動填入資料的 Word 文件


🔧 How to Run Locally (如何在本地執行)
---------------------
1. Make sure the `libs/` folder contains the following files (download from CDN if needed):
   - [https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js](https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js)
   - [https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.5/FileSaver.min.js](https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.5/FileSaver.min.js)
   - [https://cdnjs.cloudflare.com/ajax/libs/mammoth/1.4.2/mammoth.browser.min.js](https://cdnjs.cloudflare.com/ajax/libs/mammoth/1.4.2/mammoth.browser.min.js)

2. Open `newCreater.html` in any modern web browser (e.g., Chrome, Edge).

3. Upload your Word template (`Notify onboard form_template_git.docx` or customized).

4. Fill in the form → click "Preview" or "Download".

操作步驟：
1. 確認 `libs/` 資料夾內含以上三個 js 檔案 (可從 CDN 下載)
2. 使用 Chrome 或 Edge 開啟 `newCreater.html`
3. 上傳 Word 樣板（例如：Notify onboard form_template_git.docx）
4. 輸入對應資料 → 點選「預覽通知單」或「下載 Word」

✅ Template Requirements (樣板需求)
---------------------
- Use double curly braces for variables: `{{name}}`, `{{jobTitle}}`, `{{date}}`, etc.
- Ensure variables are in one continuous run of text (`<w:t>`); avoid breaking them across formatting or XML tags.
- Example variables supported:
  - {{name}} — Full name
  - {{date}} — Onboard date
  - {{jobTitle}} — Job title
  - {{baseSalary}}, {{meal}}, {{transport}}, {{totalSalary}}

注意：
- 樣板中的變數應以 `{{變數名}}` 表示，請避免被斷行或斷在不同字元格式中（例如粗體 / 字型切換）。
- 支援的變數：
  - {{name}}（姓名）
  - {{date}}（報到日期）
  - {{jobTitle}}（職稱）
  - {{baseSalary}}, {{meal}}, {{transport}}, {{totalSalary}}

📞 Support
----------
If preview or download fails:
- Check if the placeholder in the Word document is broken across styles.
- Try recreating the placeholder in Word manually without formatting it separately.
- Contact your dev team or template designer.

如有問題：
- 請確認樣板中的 {{變數}} 是否完整無被拆解
- 建議直接在 Word 裡重新輸入 {{變數}}，並取消樣式
- 或聯絡維護者協助處理

