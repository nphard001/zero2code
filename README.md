# 🚀 從「我啥也不會」到「會了」- Git & Claude Code 懶人包

一個真實的學習記錄：如何在 30 分鐘內學會 Git、CLI 和 Claude Code。

> 💡 **適合誰？** 完全沒碰過程式、看到黑色視窗就害怕、想學但不知道從哪開始的人

---

## 📖 三個概念，秒懂入門

### 1️⃣ CLI 是什麼？
**人話：** 用打字來控制電腦（而不是用滑鼠點點點）

| 平常（GUI） | CLI |
|------------|-----|
| 點「新增資料夾」 | 打 `mkdir 資料夾名` |
| 點「刪除」 | 打 `rm 檔名` |

### 2️⃣ Git 是什麼？
**人話：** 幫你的檔案自動存檔的系統

```
沒有 Git：報告v1.doc → 報告v2.doc → 報告final.doc → 報告真的final.doc
有了 Git：報告.doc （Git 偷偷記錄所有版本）
```

### 3️⃣ Claude Code 是什麼？
**人話：** 住在你電腦裡的 AI 程式助手

| ChatGPT | Claude Code |
|---------|-------------|
| 給你程式碼複製貼上 | 直接幫你寫進檔案 |
| 看不到你的檔案 | 可以讀懂你的專案 |
| 只能聊天 | 可以執行命令 |

---

## ⚡ 10 分鐘快速上手

### 🔧 準備工作
```bash
# 1. 安裝 Claude Code（需要 Node.js 18+）
npm install -g @anthropic-ai/claude-code

# 2. 進入專案資料夾
cd 你的資料夾路徑

# 3. 啟動 Claude Code
claude
```

### 🎯 第一個 Git 專案
```bash
# 跟 Claude 說
"幫我建立第一個 Git 專案"

# Claude 會幫你：
# 1. git init          (開始記錄)
# 2. 建立檔案          (寫些內容)  
# 3. git add .         (準備存檔)
# 4. git commit -m "訊息" (正式存檔)
```

### 🌐 上傳到 GitHub
```bash
# 1. 去 github.com 註冊帳號
# 2. 建立新 repository
# 3. 執行這三行（GitHub 會顯示給你）
git remote add origin https://github.com/你的帳號/專案名.git
git branch -M main  
git push -u origin main
```

---

## 📋 必背指令速查表

### Git 日常指令
| 指令 | 意思 | 什麼時候用 |
|------|------|-----------|
| `git status` | 看狀態 | 不知道現在怎樣時 |
| `git add .` | 全部加入 | 要存檔前 |
| `git commit -m "說明"` | 存檔 | 做完一個段落 |
| `git push` | 上傳 | 要分享給別人 |
| `git log --oneline` | 看記錄 | 想看做過什麼 |

### Claude Code 對話範例
```bash
# 詢問類
"這個專案是做什麼的？"
"幫我解釋這個錯誤"

# 請求類  
"幫我建立一個登入頁面"
"幫我修復這個 bug"

# 學習類
"教我怎麼連接資料庫"
"示範如何使用 React"
```

### CLI 生存必備
| 指令 | 意思 | 記憶法 |
|------|------|--------|
| `pwd` | 我在哪 | Print Working Directory |
| `ls` | 看檔案 | List |
| `cd 資料夾` | 進入 | Change Directory |
| `cd ..` | 回上層 | .. 代表上一層 |
| `mkdir` | 建資料夾 | Make Directory |

---

## ❓ 常見問題 FAQ

### Q1: 為什麼 git push 失敗？
**A:** GitHub 現在要用 token（代幣）不能用密碼
1. GitHub → Settings → Developer settings → Personal access tokens
2. Generate new token (classic) → 勾選 repo
3. 複製 token，當密碼用

### Q2: Claude Code 沒反應？
**A:** 可能在思考或執行中
- 等個幾秒
- 按 Ctrl+C 取消
- 重新輸入指令

### Q3: 怎麼知道指令成功了？
**A:** 沒消息就是好消息
- 回到 `$` 符號 = 完成
- 有錯誤會顯示紅字
- 用 `git status` 確認

### Q4: 不小心 commit 錯東西？
**A:** 先別慌
```bash
# 如果還沒 push
git reset HEAD~1  # 取消上一個 commit

# 如果已經 push（慎用）
git revert HEAD   # 建立一個反向的 commit
```

### Q5: 找不到檔案？
**A:** 確認位置
```bash
pwd              # 看你在哪
ls               # 看有什麼檔案
cd ~/Desktop     # 去桌面
```

### Q6: 可以刪除 .git 嗎？
**A:** 可以但會失去所有記錄
- `.git` = Git 的資料庫
- 刪了 = 不再是 Git 專案
- 要重新 `git init`

---

## 📚 深入學習

想了解更多？看完整教學：

1. **[從零到一的綜合教學](zero_to_hero_tutorial.ipynb)** - 完整學習歷程
2. **[Git 入門教學](git_tutorial.ipynb)** - Git 詳細步驟
3. **[Claude Code 完整指南](claude_code_tutorial.ipynb)** - Claude Code 進階功能
4. **[如何上傳到 GitHub](upload_to_github_tutorial.ipynb)** - GitHub 詳細教學

---

## 🎓 記住三句話

1. **不懂就問 Claude** - 它是你的 AI 助手
2. **git status 是你的好朋友** - 迷路就用它
3. **慢慢來比較快** - 一步一步學

---

**開始你的程式之旅吧！** 從今天起，你也會寫程式了 🎉