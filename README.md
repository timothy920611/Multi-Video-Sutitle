<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JW 字幕批次提取神器 - README</title>
    <style>
        /* 基本頁面與字體設定 */
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            line-height: 1.6;
            color: #333333;
            background-color: #f9fafb; /* 淺灰色背景，讓內容區塊更突出 */
            margin: 0;
            padding: 20px;
        }

        /* 主內容容器，置中並加上陰影 */
        .container {
            max-width: 850px;
            margin: 0 auto;
            background-color: #ffffff;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        /* 標題層次字體大小設定 */
        h1 {
            font-size: 2.2em; /* 最大字體：主標題 */
            font-weight: 800;
            color: #111827;
            margin-bottom: 5px;
        }

        .subtitle {
            font-size: 1.3em; /* 副標題 */
            font-weight: 600;
            color: #4b5563;
            margin-top: 0;
            margin-bottom: 20px;
        }

        h2 {
            font-size: 1.6em; /* 第二層標題 */
            color: #1f2937;
            border-bottom: 2px solid #e5e7eb;
            padding-bottom: 8px;
            margin-top: 40px;
            margin-bottom: 20px;
        }

        h3 {
            font-size: 1.3em; /* 第三層標題 */
            color: #374151;
            margin-top: 25px;
            margin-bottom: 10px;
        }

        /* 內文字體大小 */
        p, li, table {
            font-size: 1.05em; /* 基礎閱讀字體，稍微放大增加易讀性 */
            color: #4b5563;
        }

        /* 徽章區塊 */
        .badges {
            margin: 20px 0;
            display: flex;
            justify-content: center;
            gap: 8px;
            flex-wrap: wrap;
        }

        /* 引言區塊 (Blockquote) */
        blockquote {
            font-size: 1.1em;
            margin: 20px 0;
            padding: 15px 20px;
            background-color: #f3f4f6;
            border-left: 5px solid #3b82f6; /* 藍色側邊條 */
            border-radius: 0 8px 8px 0;
            color: #1f2937;
            font-style: italic;
        }

        /* 鍵盤按鍵樣式 (KBD) */
        kbd {
            font-size: 0.9em;
            font-family: monospace;
            background-color: #f9fafb;
            border: 1px solid #d1d5db;
            border-radius: 4px;
            box-shadow: 0 1px 1px rgba(0,0,0,0.2);
            padding: 2px 6px;
            color: #374151;
            font-style: normal;
        }

        /* 表格樣式 */
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            margin-bottom: 20px;
        }
        th, td {
            border: 1px solid #e5e7eb;
            padding: 12px;
            text-align: left;
        }
        th {
            background-color: #f9fafb;
            font-weight: 600;
            color: #111827;
        }

        /* 折疊選單 (Details/Summary) */
        details {
            background-color: #f9fafb;
            border: 1px solid #e5e7eb;
            border-radius: 8px;
            padding: 12px 15px;
            margin-bottom: 10px;
        }
        summary {
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            color: #1f2937;
            outline: none;
        }
        details p {
            margin-top: 10px;
            margin-bottom: 0;
            padding-left: 20px;
        }

        /* 清單樣式 */
        ul {
            padding-left: 20px;
        }
        li {
            margin-bottom: 8px;
        }

        /* 頁尾 */
        .footer {
            text-align: center;
            margin-top: 50px;
            font-size: 0.95em;
            color: #9ca3af;
        }
    </style>
</head>
<body>

<div class="container">
    
    <!-- 頂部區塊 -->
    <div style="text-align: center;">
        <h1>🎬 JW 字幕批次提取神器</h1>
        <p class="subtitle">— 動態時間開關版 —</p>

        <div class="badges">
            <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
            <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React">
            <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS">
            <img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge" alt="License MIT">
        </div>

        <blockquote>
            專為影片字幕提取設計的輕量化網頁工具。<br>
            <strong>一鍵貼上網址，自動抓取、深度淨化、完美排版，給您最純淨的閱讀體驗。</strong>
        </blockquote>
    </div>

    <!-- 內容區塊 -->
    <h2>✨ 為什麼選擇這個工具？</h2>
    <p>我們發現原始的字幕檔案經常夾雜亂碼與多餘符號（例如：<code>"[00:00:23]\n","</code>），這讓閱讀變得非常困難。這個工具內建了<strong>深度淨化演算法</strong>，能自動將這些惱人的格式清除，並加上了現代化的操作介面！</p>

    <h3>🌟 核心亮點</h3>
    <ul>
        <li>🚀 <strong>極速批次處理</strong>：支援一次貼上多個影片網址（最多 50 個），一鍵全自動依序提取，告別手動複製貼上。</li>
        <li>⏱️ <strong>動態時間開關 (全新功能)</strong>：
            <ul>
                <li><kbd>開</kbd> <strong>對照模式</strong>：保留 <code>[00:01:23]</code> 格式的時間戳記，適合一邊看影片一邊做筆記。</li>
                <li><kbd>關</kbd> <strong>純淨閱讀</strong>：瞬間隱藏所有時間，變成流暢的純文字文章，非常適合專心閱讀或列印。</li>
            </ul>
        </li>
        <li>🧹 <strong>深度淨化演算法</strong>：徹底解決原始字幕檔的亂碼問題！自動移除多餘的 HTML 標籤、引號、換行代碼。</li>
        <li>🖨️ <strong>原生列印優化 (Print CSS)</strong>：內建專屬的列印樣式，按下 PDF 按鈕後會自動隱藏網頁按鈕，產生乾淨、無分頁裁切錯誤的高畫質 PDF。</li>
    </ul>

    <h2>🛠️ 如何使用？ (3 步輕鬆上手)</h2>
    
    <h3>Step 1. 準備影片網址</h3>
    <p>複製您想要提取字幕的影片網址。</p>

    <h3>Step 2. 貼上並執行</h3>
    <p>在工具首頁的輸入框貼上網址（<strong>每行一個</strong>），點擊「開始批次提取」按鈕。</p>

    <h3>Step 3. 匯出您的成果</h3>
    <p>提取完成後，您可以透過畫面右上角的「顯示時間開關」調整閱讀模式。接著使用快捷按鈕匯出：</p>

    <table>
        <thead>
            <tr>
                <th style="text-align: center;">按鈕圖示 / 顏色</th>
                <th>功能說明</th>
                <th>適合場景</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="text-align: center;">📋 <strong>黑色按鈕</strong></td>
                <td><strong>複製全部</strong></td>
                <td>將當前排版結果直接複製到剪貼簿。</td>
            </tr>
            <tr>
                <td style="text-align: center;">📄 <strong>藍色按鈕</strong></td>
                <td><strong>下載 TXT</strong></td>
                <td>儲存為最輕量的純文字檔案。</td>
            </tr>
            <tr>
                <td style="text-align: center;">🌐 <strong>紫色按鈕</strong></td>
                <td><strong>下載 HTML</strong></td>
                <td>儲存為帶有影片目錄與跳轉功能的網頁。</td>
            </tr>
            <tr>
                <td style="text-align: center;">🖨️ <strong>紅色按鈕</strong></td>
                <td><strong>完美 PDF</strong></td>
                <td>呼叫系統列印介面，選擇「另存為 PDF」即可獲得排版完美的閱讀手冊。</td>
            </tr>
        </tbody>
    </table>
    
    <p style="font-size: 0.95em; color: #d97706; background-color: #fef3c7; padding: 10px; border-radius: 6px;">
        💡 <strong>小提示：</strong> 您複製或下載的內容，會<strong>完全依照</strong>您當下「時間開關」的狀態來輸出喔！
    </p>

    <h2>💻 技術架構與隱私</h2>
    <p>本工具為<strong>單一 HTML 檔案</strong>，不需安裝任何伺服器環境，隨開即用：</p>
    <ul>
        <li><strong>前端框架</strong>：<code>React 18</code> (CDN 引入，負責狀態管理與流暢切換)</li>
        <li><strong>視覺設計</strong>：<code>Tailwind CSS</code> (提供現代化、響應式的視覺與列印排版)</li>
        <li><strong>跨域請求</strong>：內建備用 <code>CORS Proxy</code> 機制，解決瀏覽器安全限制。</li>
        <li>🔒 <strong>隱私安全</strong>：<strong>純前端運作！</strong> 所有的資料處理都在您的瀏覽器中完成，我們不會（也無法）收集您的任何資料。</li>
    </ul>

    <h2>⚠️ 常見問題與注意事項</h2>
    
    <details>
        <summary>Q: 為什麼一直顯示「載入失敗」或「無法連線」？</summary>
        <p>由於瀏覽器的跨網域安全限制 (CORS)，工具會透過公共代理伺服器來抓取字幕。如果代理伺服器暫時忙碌或不穩定，就會出現這個狀況。請稍候幾分鐘再試一次即可。</p>
    </details>

    <details>
        <summary>Q: 支援播放清單的網址嗎？</summary>
        <p>目前僅支援「單一影片」的網址。請確認您貼上的是個別影片的連結（每行一個）。</p>
    </details>

    <div class="footer">
        <i>Created for a better reading and studying experience. 📖</i>
    </div>

</div>

</body>
</html>
