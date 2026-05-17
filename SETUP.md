```powershell
@"
# GitHub Pages[|个人静态网站|免费不用服务器支持静态网站|不支持 PHP / 数据库](https://wzf9.github.io)
1. 生成网页html:teleportHQ根据自然语言自动生成原型图和HTML代码 + 文件夹拖到cursor, codex, 甚至trae里面更个性化的定制
2. 整个文件夹拖到github上，给repository取名"username.github.io"
3. *回到仓库 Pages 设置，在 Custom domain 填你的域名，并且进行绑定，勾选Enforce HTTPS以增加安全性（不勾的话可能会被识别成恶意网站），等待一大段时间，大概20分钟
#或者
# Fork 并配置仓库：https://github.com/academicpages/academicpages.github.io
点击模板仓库页面绿色的 “Use this template” 按钮，创建一个属于你自己的新仓库。
关键：将新仓库命名为 [你的GitHub用户名].github.io，这将是你的个人网站域名。
在仓库的 Settings -> Pages 下，将Source设为 GitHub Actions，平台将自动开始构建你的网站。

# 本地克隆+修改
cd e:\mywork
git clone https://github.com/wzf9/wzf9.github.io
cd wzf9.github.io

#自定义网站内容：这是让网站真正属于你的关键步骤。通过修改 _config.yml 这一核心文件来配置网站标题等全局信息。你需要在根目录的该文件中，自定义以下个人信息：
code-insiders _config.yml

# 本地改动同步到GitHub远程仓库
# 查看修改状态
git status
# 添加修改的文件
git add _config.yml
# 提交（可写新的提交信息）
git commit -m "Update _config.yml with personnel info"
# 推送（分支可能是 main 或 master）
git push origin main
# 查看分支名
git branch
# 本地 master 重命名为 main（与 GitHub 默认保持一致）
git branch -m master main
git push -u origin main

# 个性化定制与建议
撰写个人简历(CV)：在_pages目录下找到cv.md，用Markdown格式撰写你的CV内容。你还可以通过_data/cv.yml文件，以更结构化的方式定义简历的各个板块（如教育背景、工作经历、发表论文等）。

添加研究项目和作品集：创建研究项目 (Research Projects)或作品集 (Portfolio)页面，详细介绍你的工作。你可以在Markdown文件中通过YAML Front Matter定义项目的标题、摘要、技术栈等元数据。

集成社交媒体和学术档案：在_config.yml文件的author部分，填写linkedin、googlescholar、twitter等字段。网站模板会自动识别并在你的个人资料区域显示相应的社交图标和链接。

集成第三方评论系统：如需开启博客文章的评论区，你可以集成Giscus或Disqus等第三方评论系统。选择一种你喜欢的服务，获取其通用代码片段，然后将代码添加到_layouts目录下的文章布局文件中，例如_layouts/single.html。
@" > SETUP.md

code-insiders SETUP.md

git status
git add SETUP.md
git commit -m "Initial commit with SETUP"
git push origin main

```