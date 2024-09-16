---
title: 'ConventionalCommits初學指南'
date: 2024-09-11T07:48:52+08:00
draft: false
tags: ["Git"]
summary: ""
categories: ["程式語言"]
showtoc: true  # 顯示目錄
tocopen: true  # 預設展開目錄
mathjax: false
---

## 為什麼使用慣例式提交？

慣例式提交（Conventional Commits）是一種對提交說明的簡單規範，優勢如下。

- 自動產生修改日誌 (Changelog)。
- 基於提交的類型，自動決定語意化版本的升級。
- 向同事、公眾以及其他的利益相關者傳達變化的過程。
- 觸發建置與發布流程。
- 讓大家探索更有結構的提交歷史，使你的專案更容易被貢獻。


### 結構說明

提交說明的結構如下：
```plaintext
<類型 type>[可選的作用範圍 scope]: <描述 description>

[可選的正文 body]

[可選的頁腳 footer]

```

範例如下

```plaintext
feat: 支援新的配置文件擴展功能

BREAKING CHANGE: 現在 `extends` 鍵可用於擴展其他配置文件
```

```plaintext
fix: 修正請求的競爭問題

增加請求 ID 並追蹤最後一次請求。忽略來自舊請求的回應。
```

### 規範要點

- 類型（如`fix`、 `feat`）必須在最前面。
- 提交描述應簡明扼要，描述程式碼變更的內容。
- 可以選擇提供詳細正文以補充提交的變更細節。
    - 若有重大變更，必須使用 `BREAKING CHANGE:` 說明具體變更。

### 常見類型

有助於清晰傳達提交的內容，常見的類型有：
- `fix`: 表示對程式修正了一個bug（語意化版本中的 修訂號 PATCH）。
- `feat`: 表示對程式增加了一個功能（語意化版本中的 次版本 MINOR）。
- `BREAKING CHANGE`: 重大變更，（語意化版本中的 主版本 MAJOR）。

其他常見的類型
- `chore`: 進行一些任務管理或環境變更，不涉及程式邏輯。
- `docs`: 文件相關的變更。
- `style`: 程式碼風格或格式上的調整。
- `refactor`: 程式碼重構，不改變外部行為。
- `perf`: 提升效能的修改。
- `test`: 測試相關的修改。

進階使用
- **增加作用範圍**：可以用括號為類型加上範圍，例如 `fix(parser): 修正解析器錯誤`。
- **重大變更**：提交中可使用 `!` 來表明重大變更，如 `feat(api)!: 移除不再使用的 API`。


## 常見問題

### 提交說明應該大寫還是小寫？
- 大寫或小寫皆可，但建議一致。

### 如何處理包含多種類型的提交？
- 最好將其拆分為多個提交，讓每個提交專注於一個變更。

### 這與 SemVer 有什麼關係呢？
- fix 類型的提交應該對應到 PATCH 發行版。feat 類型的提交應該對應到 MINOR 發行版。
- 含有 BREAKING CHANGE 的提交，無論是什麼類型，都應該要對應到 MAJOR 發行版。

### 提交類型使用錯誤時該如何處理？
- 可以使用 `git rebase -i` 來編輯提交歷史，在發布之前進行修正。

### 慣例式提交要如何處理回退提交 (revert commit)？
- 慣例式提交沒有強制定義回退的行為。反而，我們將這個問題留給工具的作者，靈活運用 類型 以及 頁腳 來開發處理回退的邏輯。
- 其中一個推薦的方法時使用 revert 類型，並在頁腳中參照到被回退的 SHA 雜湊：
```plaintext
revert: let us never again speak of the noodle incident

Refs: 676104e, a215868
```