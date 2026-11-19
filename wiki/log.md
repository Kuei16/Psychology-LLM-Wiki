# Wiki 操作日誌（真實執行）

## 2026-11-19｜Step 1 初始化（資料匯入與本地檢查）
- 輸入：使用者提供的 OpenStax *Psychology 2e* PDF 所拆分之 S01–S07。
- 方法：讀取各篇 PDF 文字、核對目標小節標題；以繁體中文歸納概念、來源、限制，建立來源筆記與概念頁。
- 來源性質：同一本教材 7 個小節，**不是** 7 篇不同論文。
- 檢查範圍：見 [`reports/lint-step1.md`](../reports/lint-step1.md)；檔案式 Query 測試見 [`reports/query-step1.md`](../reports/query-step1.md)。
- 節點順序：原始 PDF → 來源筆記（Ingest）→ 概念歸併 → 索引 → Lint → Query 路徑測試。
- 注意：PDF 影印頁首／頁末會與相鄰小節重疊，故以小節標題為實際來源邊界，並記錄在每篇筆記。
- 尚未執行：HTML 簡報；網路來源回應檢測；獨立人工逐句專業審核。

- `INGEST-01`：§1.1 What Is Psychology? → `wiki/papers/source01.md`；來源檔與索引已建立。
- `INGEST-02`：§7.1 What Is Cognition? → `wiki/papers/source02.md`；來源檔與索引已建立。
- `INGEST-03`：§8.1 How Memory Functions → `wiki/papers/source03.md`；來源檔與索引已建立。
- `INGEST-04`：§6.2 Classical Conditioning → `wiki/papers/source04.md`；來源檔與索引已建立。
- `INGEST-05`：§6.3 Operant Conditioning → `wiki/papers/source05.md`；來源檔與索引已建立。
- `INGEST-06`：§10.4 Emotion → `wiki/papers/source06.md`；來源檔與索引已建立。
- `INGEST-07`：§12.4 Conformity, Compliance, and Obedience → `wiki/papers/source07.md`；來源檔與索引已建立。

## 修改／回圈狀態
- 本次第一次建置依照先前已確定的 AGENTS.md 規範，執行小節標題邊界檢查。
- 尚未有實際 FAIL → 修正 → 重測的案例可供宣稱；若後續測試失敗，應在此新增失敗證據、回流節點與重測結果。
