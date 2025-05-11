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
將遠端儲存庫命名為 `origin` 並設定網址[17][19]。

#### 9. 分支管理與重新命名

```bash
git branch -M main
```
將目前分支重新命名為 `main`。

#### 10. 推送本地分支到遠端並建立關聯

```bash
git push -u origin main
```
將本地 `main` 分支推送到遠端 `origin` 並建立追蹤關聯[6][12][18]。

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

> 建議將此流程以 Markdown 格式保存於專案文件，方便團隊成員快速查閱與操作[1][3][4][7][9]。

引用：
[1] 基本撰写和格式语法- GitHub 文档 https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
[2] progit/zh-tw/02-git-basics/01-chapter2.markdown at master - GitHub https://github.com/progit/progit/blob/master/zh-tw/02-git-basics/01-chapter2.markdown
[3] Markdown怎麼用？常見指令大集合 - Jasmine's BLOG https://jasminmin.com/2019-04-16-markdown-record/
[4] Markdown 基本语法 https://markdown.com.cn/basic-syntax/
[5] Markdown | GitBook 中文解說- 2.4 https://wastemobile.gitbooks.io/gitbook-chinese/content/format/markdown.html
[6] 推送提交到远程仓库- GitHub 文档 https://docs.github.com/zh/get-started/using-git/pushing-commits-to-a-remote-repository
[7] 技術筆記好工具：Markdown語法&編輯器 - HackMD https://hackmd.io/@howkii-studio/markdown_intro
[8] 2.5 Git 基础- 远程仓库的使用 https://git-scm.com/book/zh/v2/Git-%E5%9F%BA%E7%A1%80-%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E7%9A%84%E4%BD%BF%E7%94%A8
[9] Markdown 語法說明 https://markdown.tw
[10] 2.5 Git 基礎- 與遠端協同工作 https://git-scm.com/book/zh-tw/v2/Git-%E5%9F%BA%E7%A4%8E-%E8%88%87%E9%81%A0%E7%AB%AF%E5%8D%94%E5%90%8C%E5%B7%A5%E4%BD%9C
[11] 給新手：20 個Git 指令整理 - CodeLove 論壇 https://codelove.tw/@tony/post/gqv9Xa
[12] git远程仓库分支的各命令的具体解析(git remote add) 原创 - CSDN博客 https://blog.csdn.net/wq6ylg08/article/details/89028412
[13] 菜雞的Markdown 筆記| 伊果的沒人看筆記本 https://igouist.github.io/post/2020/10/markdown/
[14] git remote、pull、push、fetch等命令原创 - CSDN博客 https://blog.csdn.net/liuxiao723846/article/details/55193239
[15] Git基本指令和markdown语法 - CSDN博客 https://blog.csdn.net/m0_60920298/article/details/126902103
[16] git remote 命令| 菜鸟教程 https://www.runoob.com/git/git-remote.html
[17] 管理远程仓库- GitHub 文档 https://docs.github.com/zh/get-started/getting-started-with-git/managing-remote-repositories
[18] 添加远程库- Git教程- 廖雪峰的官方网站 https://liaoxuefeng.com/books/git/remote/add-remote/index.html
[19] 遠端分支- Git 分支- Pro Git 繁體中文版 https://iissnan.com/progit/html/zh-tw/ch3_5.html
