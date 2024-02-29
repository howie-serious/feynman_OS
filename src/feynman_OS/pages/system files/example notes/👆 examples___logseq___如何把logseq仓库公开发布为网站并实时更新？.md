tags:: logseq, #[[✅SOP 清单与流程]], #p3-🪴budding-抽条, #s4-★★★★☆, #[[👆 examples]],
iteration:: [[Dec 23rd, 2023]], [[Feb 28th, 2024]], [[Feb 29th, 2024]]
exclude-from-graph-view:: true

- #+BEGIN_NOTE
  这是我的一条笔记，不“整洁”但是真实，而且有用。
  - @howie.serious 
  #+END_NOTE
- ## what
	- 把logseq仓库发布出来，作为一个网站（效果与使用自己的 logseq 基本没区别）
- ## how
	- ### 整体思路
	  collapsed:: true
		- logseq graph
			- (可选)存在iCloud文件夹，便于多端同步
			- 设置为github仓库，便于publish
		- logseq publish-spa：logseq官方的发布方案，
			- 把logseq graph做成一个spa，通过github pages发布为网站；
				- 可以使用其他网站托管服务商，但是 github action在内容更新后自动刷新网站，很方便；
			- 需要修改logseq设置；
				- 隐藏私人性质的笔记；
			- publish-spa这个action，是几个workflow，其中的依赖过期，需要根据github报错来手动修改；
				- logseq 官方的代码有报错； README写的不清不楚；
				- `publish.yml`文件中的logseq graph路径，需要根据实际情况修改
		- 设置完成后，logseq内容有更新，git同步之后，GitHub会自动更新网页；
	- ### 建站SOP：更新最新实践来迭代
	  collapsed:: true
		- ### 目标
			- TODO
		- ### 本地文件夹同步至github
			- TODO 将`logseq/publish.spa`git仓库代码添加到logseq本地文件夹
				- [[logseq/github x logseq：用git同步 logseq 知识库]]
			- TODO 把本地logseq仓库用git同步到github
			- TODO 开启git仓库的pages
				- depoly from branch
		- ### 设置logseq仓库
			- TODO 在logseq仓库中添加文件 `.github/workflows/publish.yml`
				- 使用vs code 手动添加
				- `publish.yml`的代码在github 项目的 readme 中；
				- push 仓库之后，github 会自动运行，生成静态网站到github pages
			- TODO 修改logseq功能模块
				- 关闭journals、whiteboard和flash cards等与网站无关的功能；
			- TODO 打开页面publish设置
				- [[logseq/page properties 页面属性]]
			- TODO 修改`.gitignore`文件
				- ```
				  /node_modules
				  /.nbb
				  /.cpcache
				  .DS_Store
				  src/feynman_OS/logseq/bak/
				  src/feynman_OS/logseq/.recycle/
				  src/feynman_OS/logseq/pages/design files/
				  src/feynman_OS/logseq/pages/.DS_Store
				  src/feynman_OS/logseq/pages/system files/.DS_Store
				  # src/feynman_OS/journals/
				  # test/
				  ```
		- ### 设置 github pages
			- TODO 在github pages页面，选择 `gh-pages`作为页面内容；
			- 修改 `publish.yml`代码
				- TODO 修改`publish.yml`中的logseq文件夹路径；
				- 根据github仓库workflow页面的报错，来修改代码中的问题；
					- 唯一要修改的地方：`publish.yml`
					- 主要是过时的依赖（新版本代码已经没有问题）；
				- TODO bug：网站正常发布，github 没有报错，但是笔记没有显示出来；
					- `publish.yml` 中修改项目版本号为最新版 `uses: logseq/publish-spa@v0.3.1`
				- TODO bug：实际有 100 多条笔记，但是网站只显示两条。
					- logseq 的`config.edn`有两个：全局config，vault config。修改 vault config 的页面属性 ` :publishing/all-pages-public? true`
		- ### 自定义域名
			- TODO 绑定域名
				- xxx.candobear.com
				- [[在cloudflare上分别添加CNAME和TXT记录]]
			- TODO 设置强制https
				- 自定义域名 1 小时后，GitHub会自动发放tls、https证书。这是可以开启 HTTPS。
				- [Troubleshooting custom domains and GitHub Pages - GitHub Docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/troubleshooting-custom-domains-and-github-pages#https-errors)
		- ### 成功发布后的日常维护
			- 迭代github 项目
				- TODO 更新**README** [[费曼笔记系统/README]]
				- TODO 更新**ABOUT** [[费曼笔记系统/ABOUT]]
				- TODO 更新**RELEASES** [[费曼笔记系统/RELEASES]]
			- logseq 仓库的内容迭代后，git一下，网站自动更新！
	- ### logseq建站实践
		- DONE [费曼日报 daily.candobear.com](https://daily.candobear.com)
		- DONE [费曼笔记系统 notes.candobear.com](notes.candobear.com)
			- [[费曼笔记系统/把 logseq 仓库发布为网站]]
		- TODO 《费曼学习法》官方网站 feynman.candobear.com
		- TODO 知识体系实例：GPT 大法
		- TODO 知识体系实例：serious coding 大法
- ## todo
	- DONE 网站代码的版本升级 v0.3.1
	- DONE 维护费曼日报仓库，把历史文件补齐，383期之前的内容
	- DONE 修改graph名称为 feynman_daily
	- DONE graph中，部分内容属于编辑流程，应该设置为不公开
	- DONE 制作首页：效法logseq help的首页
- ## ref.
	- [[github projects]]
	- 工具
		- [logseq/publish-spa: A github action and CLI to publish logseq graphs as a SPA app](https://github.com/logseq/publish-spa)
	- 案例
		- [logseq官方案例](https://docs.logseq.com/#/page/contents)