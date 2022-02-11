# Git 使用技巧

1. Git 中的自动纠错

   ```bash
   git config --global help.autocorrect 1
   ```

2. 仓库优化

   ```bash
   git gc --prune=now --aggressive
   ```

3. 给未追踪的文件来个备份
   
   ```bash
   git ls-files --others --exclude-standard -z |\
   xargs -0 tar rvf ~/backup-untracked.zip
   ```
   
4. 浏览另一个分支的文件
	```bash
	git show [branch]:README.md
	```
	
5. Git中搜索

   ```bash
   git rev-list --all | xargs git grep -F ''
   ```

   

