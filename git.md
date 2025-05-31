這是一份整理過的 Markdown 版本，讓 Git 指令更清晰易讀：

```md
# Git 狀態管理
- `git status` : 查看目前的狀態
  - **untracked** (未追蹤)
  - **tracked** (已追蹤)
  - **staged** (已暫存)
  - **committed** (已提交)

# 變更與提交
- **從未追蹤改成已追蹤**：
  ```bash
  git add <檔案名>.md
  ```
- **把所有變更加入暫存區**：
  ```bash
  git add .
  ```
- **建立提交**：
  ```bash
  git commit -m "想改的名稱"
  ```

# 查看與還原
- **看之前的提交**：
  ```bash
  git log (--oneline) # 簡化版
  ```
  (按 `q` 可退出)
- **查看新舊版的內容差異**：
  ```bash
  git diff <ID編號> -- <檔名>
  ```
- **還原檔案到特定版本**：
  ```bash
  git checkout <ID> -- <檔名>
  ```
  (還原後需提交)
  ```bash
  git add .
  git commit -m "還原版本"
  ```
- **刪除後面的提交點 (不可逆)**：
  ```bash
  git reset --hard <ID>
  ```

# 遠端儲存庫管理
- **新增遠端儲存庫**：
  ```bash
  git remote add origin https://github.com/ya-ya-12/yaya.git
  ```
- **檢查遠端儲存庫**：
  ```bash
  git remote -v
  ```
- **更新遠端儲存庫 URL**：
  ```bash
  git remote set-url origin <新的遠端儲存庫網址>
  ```

# 分支管理與推送
- **重新命名分支**：
  ```bash
  git branch -M main
  ```
- **推送到遠端儲存庫**：
  ```bash
  git push -u origin main
  ```

這樣應該更方便參考！如果還有細節需要整理或調整，隨時告訴我。🚀
```
