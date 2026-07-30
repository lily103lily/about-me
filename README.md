# about-me

Lily Feng 的個人數位名片(digital business card)—— 一個單頁、無框架、可直接部署到 GitHub Pages 的自我介紹頁面。

線上頁面:<https://lily103lily.github.io/about-me>

## 特色

- **純靜態**:只有 HTML / CSS / 一點 JavaScript,不需要建置工具或後端。
- **內容集中管理**:所有個人資訊都在 [`config.js`](config.js),改資料不用碰 HTML。
- **淺色主題**:主色 `#1982c4`、底色 `#e2e9ec`,搭配黑白;卡片有淡藍邊框與陰影,呈現立體感。
- **社群連結按鈕**:LinkedIn、GitHub、Instagram、Blog、LINE Stickers、Redbubble,滑鼠移上去有浮起放大的互動效果。
- **Email 直接顯示**在職稱下方,點擊可開啟郵件。
- **vCard 下載**:「Add to Contacts」可下載 [`lily.vcf`](lily.vcf) 直接存入通訊錄。
- **QR Code**:頁面底部自動產生指向本頁的 QR code(使用 [qrcodejs](https://github.com/davidshimjs/qrcodejs))。

## 檔案結構

| 檔案 | 說明 |
|------|------|
| [`index.html`](index.html) | 頁面版面、樣式與渲染邏輯 |
| [`config.js`](config.js) | 個人資訊設定(姓名、職稱、各項連結等) |
| [`lily.vcf`](lily.vcf) | vCard 名片檔,供「Add to Contacts」下載 |

## 如何修改內容

打開 [`config.js`](config.js) 修改對應欄位即可:

```js
const CONFIG = {
  name:        "Lily Feng",              // 姓名
  initials:    "LF",                     // 頭像顯示的縮寫
  title:       "Oracle ERP Engineer",    // 職稱
  org:         "IEI Integration Corp.",  // 公司
  email:       "lily103lily@gmail.com",  // Email(顯示在職稱下方)
  linkedinUrl: "#",                      // LinkedIn 連結
  githubUrl:   "https://github.com/lily103lily",
  instagramUrl:  "#",                    // Instagram 連結
  blogUrl:       "#",                    // 部落格連結
  lineStickerUrl:"#",                    // LINE 貼圖連結
  redbubbleUrl:  "#",                    // Redbubble 連結
  pageUrl:     "https://lily103lily.github.io/about-me",  // 本頁網址(QR code / 頁尾)
  vcfFile:     "lily.vcf",               // vCard 檔名
  vcfDownload: "Lily_Feng.vcf",          // 下載時的檔名
};
```

> 連結值為 `"#"` 表示尚未設定,填上實際網址即可啟用該按鈕。

## 本機預覽

因為頁面用 JavaScript 讀取 `config.js`,建議用簡易伺服器開啟(直接雙擊 `index.html` 在部分瀏覽器可能無法載入外部 JS):

```bash
python -m http.server 8000
```

接著在瀏覽器打開 <http://localhost:8000>。

## 部署(GitHub Pages)

1. 進入 repo 的 **Settings → Pages**。
2. **Source** 選擇 `main` 分支、根目錄 `/`。
3. 儲存後即可透過 <https://lily103lily.github.io/about-me> 瀏覽。
