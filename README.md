# close-conversation

把一段跟 Claude 的對話，整理成「痛點 → 討論過程 → Result」三段式的詳細決策紀錄，自動存進你的 Notion 資料庫，方便半年後回頭查閱，不用再翻原始對話。

## 安裝前準備

1. **連接 Notion**：在 Claude 的設定中連接 Notion connector。
2. **建立 Notion 資料庫**，包含以下屬性（名稱需一致）：

   | 屬性 | 類型 |
   |------|------|
   | 標題 | Title |
   | 日期 | Date |
   | 來源工具 | Select（選項：`Claude Chat`） |
   | 領域 | Multi-select（選項：`工作`、`個人專案`、`生活行政`、`職涯`、`其他`） |
   | 狀態 | Select（選項：`待整理`） |

3. **填寫設定**：打開 `SKILL.md`，在「⚙️ 設定」區塊填入：
   - `NOTION_DATABASE_URL`：資料庫網址
   - `NOTION_DATA_SOURCE_ID`：可留空，Claude 第一次執行時會用網址自動查出

## 使用方式

在對話尾聲說「結束對話」、「收斂對話」、「幫我記下來」或「close conversation」即可觸發。

## 客製化

- **領域 / 狀態選項**：可改成自己的分類，記得同步修改 `SKILL.md` 中的 Schema 表格與 Step 2 判斷規則。
- **沒有 Notion**：不填設定也能用，Claude 會把整理好的紀錄直接印在對話中供你複製。
