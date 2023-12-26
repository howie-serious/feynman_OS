tags:: #p3-🪴budding-抽条, #⚙️费曼学习OS, #s5-★★★★★, #需要用户自定义的system-files,
exclude-from-graph-view:: true

- > home 页面是需要根据个人需求来优化的。本页面是 candobear 的 home 页面模板，提供了一个 home 页面的框架。请按需迭代。
  迭代后，请删除笔记名称中的`- candobear template`。这样，以后系统文件更新，直接用新`system files`覆盖时，经过定制的`home`页面不会被覆盖，而新的 home 页面模板可以作为参考。
- > 这是小能熊`费曼学习 OS` 的首页，也是你的知识管理系统的全局地图。请根据实际需求作出合理调整。不求完美，但求在实际使用中不断迭代。
  祝你学习快乐！ - @howie.serious
- ## 📥 inbox 收集箱
  collapsed:: true
	- > 顾名思义，就是一个 inbox。请定期清空，让知识流动起来，让学习走完闭环。流水不腐户枢不蠹……你懂的。
	- #000-📥inbox
- ## 🏗️ projects 项目
  collapsed:: true
	- > 对于有明确目标、明确截止期限的、**项目性质**比较重的，可以**单独建立logseq 知识库（graph）**。#🏗️projects-项目
	- {{query (page-property :tags "#🏗️projects-项目")}}
- ## 🌲 BoK 知识体系
  collapsed:: true
	- > 1、哪怕有 10000 条笔记，也自动构成一个有序的个人知识体系。
	  2、通过多个视图（perspective），再多的笔记也可以轻松驾驭（当然，最重要的是搜索功能）。
	  3、`知识树视图`：查看你当前的知识体系以及知识砖块；
	  4、`成熟度视图`和`重要性视图`是 wikipedia 的理念。我迁移过来，让费曼学习 OS 成为你的私人 wikipedia；
	  5、`GTD 视图`和`分类视图`这是小能熊古典时期（2016~2020，logseq 这类全新工具出现之前）的知识管理 OS 分类体系。
	- 知识树视图 bok perspective
		- #[[🌲BoK-知识树]]
			- {{query (page-property :tags "#🌲BoK-知识树")}}
		- #🧱bricks-知识砖块
			- #🧱bricks-知识砖块/facts-事实性知识
			- #🧱bricks-知识砖块/concepts-概念
			- #🧱bricks-知识砖块/mental-models-思维模型
	- 成熟度视图 maturity perspective
		- #p1-🫐seed-种子
		- #p2-🌱sprout-萌芽
		- #p3-🪴budding-抽条
		- #p4-🌸flowering-开花
		- #p5-🌲evergreen-长青
	- 重要性视图 importance perspective
		- #s5-★★★★★
		- #s4-★★★★☆
		- #s3-★★★☆☆
		- #s2-★★☆☆☆t'w
		- #s1-★☆☆☆☆
	- **示例**：重要性为 S5、成熟度为 P1 的笔记。
	  > 请参考案例，按需设计。
		- {{query (and (page-tags [[p1-🫐seed-种子]]) (page-property :tags "#s5-★★★★★"))}}
	- GTD 视图 GTD perspective
		- #000-📥inbox
		- #zzz-📦archive-归档库
			- #zzz-📤outbox-费曼输出
				- #zzz-📤outbox-费曼输出/卡片输出
				- #zzz-📤outbox-费曼输出/文章输出
				- #zzz-📤outbox-费曼输出/视频输出
				- #zzz-📤outbox-费曼输出/podcast输出
				- #zzz-📤outbox-费曼输出/直播输出
	- 分类视图 classification perspective
		- > 经典的杜威十进制分类，请参考《知识管理 OS》训练营的对应课程。
		- #100-👷Job-工作
		- #200-🧑‍🎓learning-学习
			- #💎resources-资源
			- #✅SOP-清单与流程
			- #📋template-内容模板
		- #300-🌈life-生活
			- #👫friends&people-人是社会动物
			- #🏃‍♂️health&activity-运动健康
			- #🤑finance-财务管理
			- #😂dad-jokes&小树jokes
		- #400-😝interest-兴趣
- ## ⚙️ 费曼学习OS
	- > 这里是`费曼学习 OS`的系统文件，当可以按需调整。分类标签：#⚙️费曼学习OS （凡是打这个标签的，都是系统文件，在`system files`文件夹中。更新时手动替换此文件夹即可）