# 微程式資訊股份有限公司 創新前瞻計畫室 純靜態網站

* 網址: `https://campagin.program.com.tw`
* LIFF: `https://liff.line.me/1655633310-rYDdZoAG/`

## 開發環境架設

```bash
git clone git@github.com:mp-trending/mp-trending.github.io.git
cd mp-trending.github.io
cp example.env .env
yarn
yarn dev
```

* 開發環境預設網址: <https://localhost:3000>
* 開發環境是自簽署憑證，若使用 Google Chrome 可輸入 `thisisunsafe` 跳過

### 如何在手機上測試

因此專案沒有測試環境，若需在手機上測試，需先在專案內安裝 ngrok.exe

```
yarn dev

yarn ngrok
```

## GitHub Action 設定 (正式站)

* `Secret`

```
BASEURL=https://campagin.program.com.tw
CNAME=campagin.program.com.tw
LIFFID_FULL=1655633310-rYDdZoAG
```

## 驗證 CNAME

```bash
dig campagin.program.com.tw @8.8.8.8 -t CNAME +short
# mp-trending.github.io.
```
