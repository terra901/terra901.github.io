# 个人主页信息填写指南

这个文件告诉你应该去 `index.html` 的哪里替换个人信息。你可以直接搜索下面的英文占位符，然后把它们改成你的真实内容。

## 1. 基本信息

在 `index.html` 顶部和首屏 header 中修改：

- `YOUR NAME`：你的英文名或拼音名，例如 `Jinyu Chen`
- `中文名`：你的中文名；如果不想显示中文名，可以删除 `<span class="native-name">中文名</span>`
- `YOUR CURRENT ROLE, YOUR SCHOOL / ORGANIZATION`：你现在的身份，例如 `Undergraduate Student, XXX University`
- `your.email@example.com`：你的邮箱
- `YOUR_GITHUB`：你的 GitHub 用户名
- `Google Scholar` 链接：如果没有 Google Scholar，可以改成 LinkedIn、个人博客、知乎、CSDN，或直接删除这一项
- `assets/cv.pdf`：如果你有简历，把 PDF 放到 `assets/cv.pdf`；如果暂时没有，可以删除 CV 链接

页面标题也要改：

```html
<title>YOUR NAME | Personal Homepage</title>
<meta name="description" content="Personal academic homepage for YOUR NAME.">
```

## 2. 头像

现在头像使用的是：

```html
<img class="profile-photo" src="assets/profile-placeholder.svg" alt="YOUR NAME profile photo">
```

你可以把自己的照片放进 `assets/` 文件夹，例如 `assets/profile.jpg`，然后改成：

```html
<img class="profile-photo" src="assets/profile.jpg" alt="你的名字 profile photo">
```

建议使用正方形照片，比例 1:1，大小 500px 到 1200px 都可以。

## 3. Biography

找到：

```html
<section class="section" id="biography">
```

把里面两段中文提示替换成你的简介。建议包含：

- 学校、专业、年级
- 导师或实验室，如果有
- 研究方向或技术方向
- 当前关注的项目
- 未来希望申请/求职/研究的方向

如果你希望页面更像国际学术主页，建议 Biography 用英文。

## 4. Competitions

找到：

```html
<section class="section" id="competitions">
```

每一个比赛是一段：

```html
<li class="timeline-item">
  ...
</li>
```

需要填写：

- `YEAR`：比赛年份，例如 `2025`
- `Competition Name`：比赛名称
- `Award / Ranking, Team Role`：奖项、排名、你的角色，例如 `National Second Prize, Team Leader`
- 描述段落：写比赛任务、你负责的部分、技术方案、结果
- `Project` / `Certificate`：如果有项目链接或证书链接，把 `href="#"` 改成真实链接；没有就删掉对应 `<a>`

要添加更多比赛，复制一个完整的 `<li class="timeline-item">...</li>`。

## 5. Publications

找到：

```html
<section class="section" id="publications">
```

每一篇论文是一段：

```html
<li class="publication-item">
  ...
</li>
```

需要填写：

- `Paper Title`：论文标题
- 作者列表：把你的名字用 `<strong>你的名字</strong>` 包起来
- `Conference / Journal Name, YEAR`：会议/期刊/预印本状态和年份
- `summary` 段落：一句话写论文贡献
- `PDF` / `Code` / `Project Page`：把 `href="#"` 改成真实链接；没有的链接可以删除

如果暂时没有论文，可以把标题改成 `Selected Projects` 或 `Manuscripts`，内容写课程项目、研究项目或在投论文。

如果你想像参考主页一样给每篇论文放缩略图，可以把：

```html
<div class="paper-thumb" aria-hidden="true">Paper</div>
```

替换成：

```html
<img class="publication-image" src="assets/paper-name.png" alt="论文标题 thumbnail">
```

然后把图片文件放到 `assets/` 文件夹。

## 6. Internships

找到：

```html
<section class="section" id="internships">
```

每段实习经历是一段：

```html
<li class="timeline-item">
  ...
</li>
```

需要填写：

- `START - END`：起止时间，例如 `2025.06 - 2025.09`
- `Company / Lab Name`：公司、实验室或机构名称
- `Internship Title, City / Remote`：岗位名称和地点，例如 `Algorithm Intern, Shanghai`
- 描述段落：写你负责什么、用了什么技术、有什么产出

建议每段实习写 1-3 句话。能量化的结果尽量量化，例如准确率提升、处理速度提升、数据规模、上线模块数量。

## 7. 部署到 GitHub Pages

最简单的做法：

1. 创建一个名为 `你的GitHub用户名.github.io` 的 GitHub 仓库。
2. 把 `personal-homepage` 文件夹里的 `index.html`、`style.css`、`assets/` 上传到仓库根目录。
3. 打开 `https://你的GitHub用户名.github.io/` 查看页面。

如果你使用普通仓库，也可以在仓库 Settings -> Pages 中选择 `main` 分支和 `/root` 目录发布。
