tags:: #example-files, 


- #+BEGIN_NOTE
  这是我的一条笔记，不“整洁”但是真实，而且有用。
  - @howie.serious 
  #+END_NOTE
- ## todo
	- DONE 维护费曼日报仓库，把历史文件补齐，383期之前的内容
	- DONE 修改graph名称为 feynman_daily
	- DONE graph中，部分内容属于编辑流程，应该设置为不公开
	- DONE 制作首页：效法logseq help的首页
- ## what
	- 把logseq仓库公开为一个网页
	- DONE 整体思路
		- logseq graph：
			- 存在iCloud文件夹，便于多端同步
			- 同时设置为github仓库，便于publish
				- `cd /Users/howie.serious/Library/Mobile\ Documents/iCloud~com~logseq~logseq/Documents/feynman\ daily`
		- logseq publish-spa：一个github action
			- 把logseq graph做成一个网页+spa，以github pages的形式发布出来；
			- 需要修改logseq设置；
			- publish-spa这个action，是几个workflow，其中的依赖过期，需要根据github报错来手动修改；
			- workflow中的graph路径，需要根据实际情况修改
		- 设置完成后，logseq内容有更新，git同步之后，GitHub会自动更新网页；
		-
- ## how
	- DONE 把logseq 费曼日报仓库 用git同步到github
	- ### github action
		- DONE 开启git仓库的pages
	- ### logseq仓库
		- DONE 将git仓库的代码添加到logseq本地文件夹
		- DONE 在logseq仓库中添加文件 `.github/workflows/publish.yml`
		- DONE 修改logseq设置，把journals、whiteboard和flash cards关闭；同时打开页面publish设置；
	- ### github pages
		- 在github pages页面，选择 `gh-pages`作为页面内容；
		- 修改了`publish.yml`中的logseq文件夹路径；
		- 根据github仓库workflow页面的报错，来修改代码中的问题；主要是过时的依赖；
		- DONE 绑定域名
			- daily.candobear.com
			- 分别添加cname和txt记录
			- GitHub会自动发放tls、https证书
			- 设置强制https
			- 需要24小时生效
	- ### 日常维护
		- graph发生变化后，git push一下，自动更新页面
		-
- ## ref.
	- [logseq官方案例](https://docs.logseq.com/#/page/contents)
	- [logseq/publish-spa: A github action and CLI to publish logseq graphs as a SPA app](https://github.com/logseq/publish-spa)