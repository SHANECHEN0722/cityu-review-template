<a id="readme-top"></a>
<p align="center">
    <a href="https://github.com/SHANECHEN0722/cityu-review-template/"><img src="https://img.shields.io/github/stars/SHANECHEN0722/cityu-review-template.svg?style=for-the-badge" alt="Stargazers"></a>
    <a href="https://github.com/SHANECHEN0722/cityu-review-template/network/members"><img src="https://img.shields.io/github/forks/SHANECHEN0722/cityu-review-template.svg?style=for-the-badge" alt="Forks"></a>
    <a href="https://github.com/SHANECHEN0722/cityu-review-template/graphs/contributors"><img src="https://img.shields.io/github/contributors/SHANECHEN0722/cityu-review-template.svg?style=for-the-badge" alt="Contributors"></a>
    <a href="https://github.com/SHANECHEN0722/cityu-review-template/issues"><img src="https://img.shields.io/github/issues/SHANECHEN0722/cityu-review-template.svg?style=for-the-badge" alt="Issues"></a>
    <a href="https://github.com/SHANECHEN0722/cityu-review-template/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License"></a>
    <a href="https://creativecommons.org/licenses/by-sa/4.0/deed.zh"><img src="https://img.shields.io/badge/License-CC_BY_4.0-lightblue.svg?style=for-the-badge&label=license" alt="CC BY-SA 4.0"></a>
    <a href="https://shanechen0722.github.io/cityu-review-template/"><img src="https://img.shields.io/badge/GitHub%20Pages-181717?style=for-the-badge&logo=github" alt="GitHub Pages"></a>
    <a href="mailto:dieael_chenxian@163.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
    <h1 align="center">For CityU Review Hub</h1>
    为香港城市大学学生设计的标准化复习资料仓库模板，快速开始建设你的专业资源库。

[📚 查看使用说明](#-快速开始) · [🤝 参与贡献](#-参与贡献) · [💡 获取帮助](https://github.com/SHANECHEN0722/cityu-review-template/issues) · [😊 实际案例仓库](https://github.com/SHANECHEN0722/cityu-CS-review)
</p>

## 📖 项目简介

这是一个为 [CityU Review Hub](https://github.com/SHANECHEN0722/Cityu-Review) 准备的标准化模板仓库，帮助CityU学生快速创建和维护自己专业的复习资料库：

- 🎯 **快速开始** - 使用"Use this template"按钮一键创建
- 📁 **标准结构** - 提供经过验证的文件组织方案
- 📝 **详细指南** - 清晰的自定义说明和内容建议
- 🤝 **社区集成** - 轻松集成到CityU Review Hub导航平台

## ✨ 为什么使用这个模板？

- ✅ 省时间 - 无需从零开始设计目录结构
- ✅ 保持一致 - 与其他贡献者保持风格统一
- ✅ 易维护 - 清晰的组织方式便于长期管理
- ✅ 更专业 - 提升仓库整体质量和可用性

## 🎯 快速开始

### 步骤 1️⃣：使用模板创建仓库

最简单的方式 - 只需一键：

1. 点击本仓库右上角的 **"Use this template"** 按钮
2. 选择 **"Create a new repository"**
3. 输入仓库名称，建议格式：`cityu-[专业简称]-review`
   - 例如：`cityu-cs-review`, `cityu-bba-review`, `cityu-fin-review`
4. 选择 **Public** (方便集成到导航)
5. 点击 **"Create repository from template"**
6. 点击Settings,再点击pages，部署仓库页面（GitHub pages）

✨ 完成！你已经有了自己的专业复习资料仓库

### 步骤 2️⃣：自定义仓库内容

将模板改成你专业的内容：

1. **克隆到本地**
   ```bash
   git clone https://github.com/你的用户名/cityu-xxx-review.git
   cd cityu-xxx-review
   ```

2. **自定义主README**
   - 编辑 `README.md` 文件
   - 更新课程列表和专业信息等相关信息

3. **整理文件夹结构**
   - 参考下方的 [模板结构](#-模板结构说明)
   - 删除不需要的模块
   - 为你的核心课程创建文件夹添加资料
   - 从courses里面获取对应课程的html文件，存放在src/core_course/<专业课>/里面

4. **修改GitHub pages信息**
   - 在index.html里修改下载仓库的超链接为你的仓库链接
   - 执行./run.sh或者执行python3 tool/generate_courses_data.py更新课程资料信息

5. **提交你的改动**
   ```bash
   (git add remote 仓库url)
   git add .
   git commit -m "Customize for [Your Major]"
   git push origin main
   ```

### 步骤 3️⃣：添加到 CityU Review Hub

让更多学生发现你的资料！

1. **Fork [CityU Review Hub](https://github.com/SHANECHEN0722/Cityu-Review)**

2. **找到你的专业**
   - 打开 `data.js` 文件
   - 找到对应的专业

3. **更新链接**
   ```javascript
   {
       name: 'BSc Computer Science',
       type: 'ug',
       description: '计算机科学理学士',
       githubRepo: 'https://github.com/shane/cityu-cs-review', // 改成你的仓库或者你部署好的pages
       color: '#0A84FF'
   }
   ```

4. **提交 Pull Request**
   - 描述你的改动：更新了 XX 专业的复习资料仓库链接
   - 等待审核和合并

## 📁 模板结构说明

这个模板提供了一个清晰、可扩展的目录结构。你可以按需调整：

```
cityu-[专业简称]-review/
│
├── README.md                             # 🚀 从这里开始自定义
│
├── 📋 专业信息/ (可选)
│   ├── course-selection-guide.md        # 选课指南和建议
│   ├── professor-reviews.md             # 教授评价和推荐
│   └── program-overview.md              # 专业概览
│
├───src/                         
│   └── core_cources/
│            └── [课程代码]-[课程名]/
│                  ├── cources.html              # 课程描述
│                  ├── homework/                 # 作业和解答
│                  ├── course_files/             # lecture & tutorial
│                  └── review/                   # 复习总结
│
├── 🏢 实习求职/ (可选)
│   ├── internship-guide.md              # 实习申请指南
│   ├── resume-templates/                # 简历模板
│   └── interview-prep.md                # 面试准备
│
└── 🛠️ 资源工具/ (可选)
    ├── recommended-tools.md             # 推荐软件工具
    └── learning-resources.md            # 在线学习平台
```
<p align="right"><a href="#readme-top">回到顶部</a></p>

## 🎨 自定义指南

###  保持更新

- 定期添加新的课程资料
- 更新教授信息和选课建议
- 收集学生的经验分享

## 📚 内容贡献建议

这个仓库可以包含哪些内容？

### ✅ 推荐的内容

- 📖 **课程笔记** - 个人整理的学习笔记、总结
- 📋 **作业和解答** - 作业题目和参考解答（注意版权）
- 📚 **教材资源** - 教科书推荐和补充资料
- 💡 **学习心得** - 个人经验和学习技巧
- 🎯 **往年试题** - 历年考试真题和解析
- 👨‍🏫 **教授评价** - 课程难度和教授评价
- 💼 **求职经验** - 实习、工作机会和面试经验
- 🛠️ **工具推荐** - 学习和工作相关的软件工具
<p align="right"><a href="#readme-top">回到顶部</a></p>

## 🤝 参与贡献

你有更好的资料？欢迎其他学生为你的仓库做贡献！

### 接受贡献的步骤

1. **启用 Pull Request** - 确保仓库允许fork和PR
2. **添加贡献指南** - 在 `CONTRIBUTING.md` 中说明：
   ```markdown
   # 如何贡献

   感谢你的兴趣！这是我们一起完善资料的方式。

   ## 贡献步骤

   1. Fork 这个仓库
   2. 创建一个新分支：`git checkout -b add-notes`
   3. 提交你的改动：`git commit -m "Add CS2000 lecture notes"`
   4. 推送到分支：`git push origin add-notes`
   5. 创建 Pull Request

   ## 内容指南

   - 确保内容准确和有用
   - 遵守上面的 [内容建议](#-内容贡献建议)
   - 使用清晰的文件命名
   ```

3. **审核贡献** - 在合并前检查质量和相关性
<p align="right"><a href="#readme-top">回到顶部</a></p>

## ❓ 常见问题

**Q: 我可以修改这个模板的结构吗？**
A: 完全可以！这只是一个建议的结构。根据你的需求自由调整。

**Q: 一定要把仓库添加到 CityU Review Hub 吗？**
A: 不一定。但这样可以让更多同学发现你的资料！

**Q: 可以在仓库中添加视频或大文件吗？**
A: 可以，但建议用 Git LFS 或上传到云盘提供链接。
<p align="right"><a href="#readme-top">回到顶部</a></p>

## 📞 获取帮助

遇到问题？

- 📖 查看 [查看模板网页](https://shanechen0722.github.io/cityu-review-template/)
- 💬 在 [Issues](https://github.com/SHANECHEN0722/cityu-review-template/issues) 提问
- 🌐 访问 [导航网站](https://shanechen0722.github.io/Cityu-Review/)
<p align="right"><a href="#readme-top">回到顶部</a></p>

## 📄 许可证

本模板采用 [MIT License](LICENSE) 开源协议。

## 🤝 参与贡献

我们欢迎所有形式的贡献！请查看 [参与贡献](#-参与贡献) 了解详情。

## Contributors

<a href="https://github.com/SHANECHEN0722/cityu-review-template/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=SHANECHEN0722/cityu-review-template" />
</a>

## Maintainers

[Xian Chen](https://github.com/SHANECHEN0722)

## 📜 许可证

本项目的代码基于 [MIT License](LICENSE) 许可协议，内容部分遵循 [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.zh) 许可协议。

### 📝 代码许可 - MIT License

本项目所有**代码**部分（包括 HTML、CSS、JavaScript 等）遵循 [MIT License](LICENSE)。

根据 MIT License，您可以：
- ✅ 自由使用、修改和分发代码
- ✅ 在商业项目中使用
- ✅ 在专有软件中使用

**条件**：保留原始版权声明和许可证文本

### 📚 内容许可 - CC-BY-SA 4.0

本项目所有**正文内容**（包括课程资料、学习指南等）遵循 [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.zh) 许可协议。

根据 CC-BY-SA 4.0，您可以：
- ✅ 自由复制、修改和分发内容
- ✅ 用于任何目的（包括商业用途）

**条件**：
- 📌 必须提供署名（标注本项目："CityU Review Hub"）
- 🔗 保留原作品链接和原出处作者版权信息
- 🔄 衍生作品必须使用相同的许可证 (CC-BY-SA 4.0)

<p align="right"><a href="#readme-top">回到顶部</a></p>

## 🙏 致谢

- 感谢香港城市大学提供的教育资源
- 感谢所有贡献学习资料的同学们

<div align="center">

**准备好了吗？[点击这里开始你的复习资料库！](../../generate)**

made with ❤️ for CityU students

</div>