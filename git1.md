git status 狀態 untracked 未追蹤 tracked 已追蹤 staged 已暫存 committed 已提交
從未追蹤改成已追蹤 git add (檔案).md
把所有變更加入暫存區 git add . 。git commit -m "想改的名稱" 
看之前的提交 git log (--oneline)是git log 簡化版 (q(可退出))
新舊版的內容差異 git diff lD編號 (還原點)--檔名
如果想還原的話  git checkout ID --檔名檔名
一樣要提交 所以要快照  git add. git commit -m "想改的名稱"
還原一個點 刪除後面的點 不可逆 git reset --hard ID
如果被追蹤 刪除檔案 git add git.md。git add. git commit -m "想改的名稱" 
git remote add origin https://github.com/ya-ya-12/yaya.git 雲端 新增 遠端儲存庫名稱 遠端儲存庫網址
git branch -M main  分支管理 重新命名 新得分支名
git push -u origin main 推送 建立關聯 遠端名稱 本地名稱

git status 狀態 untracked 未追蹤 tracked 已追蹤 staged 已暫存 committed 已提交
從未追蹤改成已追蹤 git add (檔案).md
把所有變更加入暫存區 git add . 
建立提交 git commit -m "想改的名稱" 
看之前的提交 git log (--oneline) 是 git log 簡化版 (q 可退出)
新舊版的內容差異 git diff ID編號 (還原點)--檔名
如果想還原的話 git checkout ID --檔名
一樣要提交，所以要快照 git add . git commit -m "想改的名稱"
還原一個點，刪除後面的點（不可逆） git reset --hard ID
如果被追蹤，刪除檔案 git add git.md。git add . git commit -m "想改的名稱"
新增遠端儲存庫 git remote add origin https://github.com/ya-ya-12/yaya.git
檢查遠端儲存庫 git remote -v
更新遠端儲存庫 URL git remote set-url origin <新的遠端儲存庫網址>
重新命名分支 git branch -M main
推送到遠端儲存庫 git push -u origin main
2