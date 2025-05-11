## Git 基本狀態與操作流程整理

**檔案狀態說明**

- **Untracked（未追蹤）**：Git 尚未追蹤的檔案。
- **Tracked（已追蹤）**：已被 Git 追蹤的檔案，包含未修改、已修改、已暫存等狀態。
- **Staged（已暫存）**：變更已加入暫存區，準備提交。
- **Committed（已提交）**：變更已被提交到本地版本庫。

---

### 狀態轉換與常用指令

#### 1. 從未追蹤改為已追蹤

```bash
git add git.md
```
將 `git.md` 加入追蹤與暫存區。

#### 2. 把所有變更加入暫存區

```bash
git add .
```
將所有變更（新檔案、修改、刪除）加入暫存區。

#### 3. 提交暫存區內容

```bash
git commit -m "想改的名稱"
```
將暫存區內容提交，並加上提交訊息。

---

### 版本紀錄與差異比較

#### 4. 查看之前的提交紀錄

```bash
git log
git log --oneline
```
`git log --oneline` 為簡化版，按 `q` 可退出。

#### 5. 比較新舊版內容差異

```bash
git diff ID -- 檔名
```
顯示指定提交（ID）與目前檔案的差異。

#### 6. 還原檔案到指定版本

```bash
git checkout ID -- 檔名
```
將檔案還原到某個提交（ID）的狀態，還需再次 `git add .` 與 `git commit` 完成快照。

#### 7. 還原到某個提交點（不可逆，刪除後面所有提交）

```bash
git reset --hard ID
```
將專案還原到指定提交（ID），後面所有提交會被移除。

---

### 檔案刪除與提交

- 若檔案已被追蹤，需先刪除，再 `git add .`、`git commit -m "訊息"` 完成提交。

---

### 遠端操作與分支管理

#### 8. 新增遠端儲存庫

```bash
git remote add origin https://github.com/ya-ya-12/yaya.git
```
將遠端儲存庫命名為 `origin` 並設定網址。

#### 9. 分支管理與重新命名

```bash
git branch -M main
```
將目前分支重新命名為 `main`。

#### 10. 推送本地分支到遠端並建立關聯

```bash
git push -u origin main
```
將本地 `main` 分支推送到遠端 `origin` 並建立追蹤關聯。

---

## 常用 Git 操作流程總結

1. `git status`：查看目前檔案狀態。
2. `git add 檔案` 或 `git add .`：加入暫存區。
3. `git commit -m "訊息"`：提交變更。
4. `git log` / `git log --oneline`：查看提交紀錄。
5. `git diff` / `git diff ID --檔名`：比較差異。
6. `git checkout ID --檔名`：還原檔案。
7. `git reset --hard ID`：回到指定提交點。
8. `git remote add origin <遠端網址>`：設定遠端。
9. `git branch -M main`：分支命名。
10. `git push -u origin main`：推送並建立關聯。

---
