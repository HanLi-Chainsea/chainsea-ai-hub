# Contributing

新增資源時，請避免只貼連結。每個條目都應該回答：它解決什麼問題、何時適合用、需要什麼輸入、會產出什麼、風險在哪裡、最後何時檢查。

## 新增流程

1. 先判斷資源是否已經能正式收錄。
2. 若尚未驗證，放到 [resources/watchlist.md](resources/watchlist.md)。
3. 使用 [templates/resource-card.md](templates/resource-card.md) 或分類頁既有格式撰寫。
4. 更新對應分類頁。
5. 若是重要資源，更新 [INDEX.md](INDEX.md) 或 README。
6. 填上 `Last checked`，避免未來不知道資訊是否過期。

不要把目標 repo 整包存進 hub。外部 repo 可以 clone 到 `/tmp` 或其他暫存位置做分析；hub 只保存整理後的 metadata、索引、評估、案例、經驗紀錄、模板與必要連結。

## 正式收錄條件

至少符合其中一項：

- 解決重複出現的工程問題。
- 能改善 AI-assisted development workflow。
- 可跨專案複用。
- 對 testing、documentation、automation、integration 有具體幫助。
- 是未來內部實驗的重要參考。

## 寫作原則

- 中文為主，必要英文保留原詞。
- 避免 marketing-style 形容詞。
- 寫清楚 when to use / when not to use。
- 保留限制、風險、替代方案與整合成本。
- 開發經驗類內容要保留日期、背景與當時判斷，不要為了「整理乾淨」抹掉時間痕跡。
