# UI/UX 風格模板 DEMO

單一檔案 `index.html` 就是完整的風格基準（Design System Template），包含網站與 App 常用的所有元件與版型。

## 這個模板怎麼運作

所有風格都由 `index.html` 內 `<style>` 開頭的 **【DESIGN TOKENS】** 區塊（`:root` CSS 變數）控制：

| 類別 | 變數範例 | 說明 |
|------|---------|------|
| 品牌色 | `--primary` `--secondary` `--accent` | 主色、次色、強調色 |
| 語意色 | `--success` `--warning` `--danger` `--info` | 成功/警告/錯誤/資訊 |
| 中性色 | `--bg` `--surface` `--border` `--text` | 背景、表面、邊框、文字 |
| 字體 | `--font-family` `--fs-*` `--fw-*` | 字型、字級階層、字重 |
| 間距 | `--sp-1` ~ `--sp-8` | 8px 間距系統 |
| 圓角 | `--radius-sm/md/lg/full` | 元件圓角 |
| 陰影 | `--shadow-sm/md/lg` | 三層陰影 |

**改風格 = 只改這些變數**，全部元件自動跟著變。深色模式在 `[data-theme="dark"]` 區塊。

## 包含的元件

- **Tokens**：色票、字體階層、圓角、陰影展示
- **按鈕**：7 種樣式 × 3 種尺寸 × 各種狀態、FAB
- **表單**：輸入框（含錯誤/停用）、下拉、多行、組合輸入、核取、單選、開關、滑桿
- **卡片**：基本、圖片、橫式、統計卡、價格卡
- **導覽**：Navbar、Tabs、分段控制、麵包屑、分頁、步驟指示
- **資料**：表格、列表、Badge、Chip、頭像、Tooltip
- **回饋**：Alert、Toast、進度條、Spinner、骨架屏、空狀態
- **覆蓋層**：Modal、Dropdown、手風琴
- **動態效果**：捲動進場、Hover 浮起/發光/縮放/3D 傾斜、水波紋、按讚動畫、鈴鐺搖晃、三態按鈕、數字滾動、圓環進度、打字機、跑馬燈、脈動指示
- **進階互動**：輪播、前後對比滑桿、星級評分、數量加減、標籤輸入、自動完成、密碼強度、OTP 驗證碼、字數統計、複製剪貼簿、拖放上傳、拖曳排序、Popover、時間軸、回到頂部
- **手機 App**：手機框架、App Bar、底部導覽、FAB、Bottom Sheet、分段控制
- **版面**：Hero、特色區、側欄後台版型、Footer

## 使用流程

1. 用瀏覽器打開 `index.html`，右上角可切換深色模式
2. 修改 `:root` 的 Design Tokens 直到滿意（改完重新整理即可看到效果）
3. 把這個檔案丟給 AI，用類似下面的提示詞

## 給 AI 的提示詞範例

### 改網站風格

> 附上我的風格模板 `index.html`。請讀取其中 `:root` 的 Design Tokens（顏色、字體、間距、圓角、陰影）以及各元件的樣式寫法（按鈕、卡片、表單、表格…），把我的專案 `<專案路徑>` 的所有 UI 改成與模板一致的風格。不要改動功能邏輯，只調整視覺樣式。

### 改 App（Flutter / React Native）風格

> 附上我的風格模板 `index.html`。請把其中的 Design Tokens 轉換成 Flutter 的 `ThemeData`（或 React Native 的 theme 物件），並依照模板中按鈕、卡片、列表、App Bar、底部導覽的樣式，調整我的 App 專案 `<專案路徑>` 的所有畫面。

### 產生新頁面

> 請依照 `index.html` 這個風格模板的 tokens 與元件樣式，幫我做一個「會員登入頁」。

## 小技巧

- 想換整體風格時，先只改 `--primary`、`--radius-*`、`--font-family` 三組，通常就有 80% 的效果
- 模板中每個元件都有語意化的 class 名稱（如 `.btn-primary`、`.card`、`.badge-success`），AI 對照時會更準確
- 建議用 git 管理這個資料夾，每次風格改版都留下紀錄
