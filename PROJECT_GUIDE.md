# 元核智算工作室网站 - 项目配置指南

> 本文档记录项目中所有可配置内容的位置和修改方法。每次优化后请同步更新此文档。

---

## 📁 项目结构

```
web/
├── css/
│   └── global.css          # 全局样式变量
├── assets/
│   ├── images/
│   │   ├── hero/           # 首页轮播背景图
│   │   ├── projects/       # 项目图片
│   │   ├── team/           # 团队成员照片
│   │   └── gallery/        # 影像实验室图片
│   └── videos/             # 视频文件
├── index.html              # 首页
├── robots.html             # 核心成果页
├── intelligence.html       # 智算控制台页
├── custom.html             # 二次开发定制页
├── archive.html            # 影像实验室页
├── about.html              # 关于我们页
├── contact.html            # 联系我们页
└── PROJECT_GUIDE.md        # 本文档
```

---

## 🖼️ 图片资源配置

### 1. 首页 (index.html)

#### Hero 轮播背景图（重要）
| 位置 | 文件路径 | 建议尺寸 | 用途说明 |
|------|----------|----------|----------|
| 轮播图1 | `/assets/images/hero/hero-1.jpg` | 1920×1080px | 首页背景轮播（建议：团队工作照/机器人实拍） |
| 轮播图2 | `/assets/images/hero/hero-2.jpg` | 1920×1080px | 首页背景轮播 |
| 轮播图3 | `/assets/images/hero/hero-3.jpg` | 1920×1080px | 首页背景轮播 |
| 轮播图4 | `/assets/images/hero/hero-4.jpg` | 1920×1080px | 首页背景轮播 |

**修改位置**: 搜索 `hero-slider`，修改 `background-image: url('...')` 中的路径

**轮播配置**:
- 自动轮播间隔：5秒
- 切换动画：1.5秒淡入淡出
- 半透明遮罩：已内置（渐变黑色遮罩）

#### 展示区图片
| 位置 | 文件路径 | 建议尺寸 | 用途说明 |
|------|----------|----------|----------|
| 展示区大图 | `/assets/images/projects/unitree-b2-hero.jpg` | 1920×800px | B2机器狗宽幅展示 |
| 展示区小图1 | `/assets/images/projects/custom-arm.jpg` | 800×600px | 机械臂抓取特写 |
| 展示区小图2 | `/assets/images/projects/bionic-butterfly.jpg` | 800×600px | 仿生蝴蝶飞行状态 |

**修改位置**: 搜索 `showcase-image` 类，替换占位符文本为 `<img src="路径">`

### 2. 核心成果页 (robots.html)

| 位置 | 文件路径 | 建议尺寸 | 用途说明 |
|------|----------|----------|----------|
| B2机器狗 | `/assets/images/projects/unitree-b2.jpg` | 1200×800px | 侧面动态视角 |
| Go2机器狗 | `/assets/images/projects/unitree-go2.jpg` | 800×600px | 跳跃姿态 |
| 自研机械臂 | `/assets/images/projects/custom-arm.jpg` | 1000×700px | 抓取动作特写 |
| 仿生蝴蝶 | `/assets/images/projects/bionic-butterfly.jpg` | 800×600px | 飞行状态 |
| 具身智能终端 | `/assets/images/projects/embodied-terminal.jpg` | 800×600px | 交互界面 |
| 移动操作平台 | `/assets/images/projects/mobile-platform.jpg` | 1000×700px | 整体系统 |

**视频资源**:
| 位置 | 文件路径 | 建议规格 |
|------|----------|----------|
| B2巡检视频 | `/assets/videos/b2-patrol.mp4` | 1920×1080, H.264 |
| 机械臂抓取 | `/assets/videos/arm-grasping.mp4` | 1920×1080, H.264 |
| 仿生蝴蝶集群 | `/assets/videos/butterfly-swarm.mp4` | 1920×1080, H.264 |
| 移动操作 | `/assets/videos/mobile-manipulation.mp4` | 1920×1080, H.264 |

### 3. 智算控制台页 (intelligence.html)

| 位置 | 文件路径 | 建议尺寸 | 用途说明 |
|------|----------|----------|----------|
| 主展示区 | `/assets/images/projects/console-main.jpg` | 1920×800px | 控制台主界面截图 |
| 拓扑图生成 | `/assets/images/projects/topology-demo.jpg` | 600×450px | 拓扑图生成效果 |
| 代码生成 | `/assets/images/projects/code-gen.jpg` | 600×450px | 代码生成界面 |
| 模块配置 | `/assets/images/projects/module-config.jpg` | 600×450px | 模块配置界面 |

### 4. 影像实验室页 (archive.html)

| 位置 | 文件路径 | 建议尺寸 | 用途说明 |
|------|----------|----------|----------|
| B2室外测试(宽) | `/assets/images/gallery/b2-outdoor.jpg` | 1920×800px | 宽幅展示 |
| 团队合影(高) | `/assets/images/gallery/team-photo.jpg` | 600×900px | 竖版照片 |
| 机械臂调试 | `/assets/images/gallery/arm-debug.jpg` | 800×600px | 项目记录 |
| 获奖证书 | `/assets/images/gallery/award-1.jpg` | 800×600px | 获奖荣誉 |
| 仿生蝴蝶测试 | `/assets/images/gallery/butterfly-test.jpg` | 800×600px | 项目记录 |
| 技术分享会 | `/assets/images/gallery/tech-share.jpg` | 800×600px | 团队风采 |
| 专利证书 | `/assets/images/gallery/patent.jpg` | 800×600px | 获奖荣誉 |
| 导航系统测试 | `/assets/images/gallery/nav-test.jpg` | 800×600px | 项目记录 |

**分类说明**:
- `project`: 项目记录
- `team`: 团队风采
- `award`: 获奖荣誉

**修改位置**: 在 `gallery-item` div 上修改 `data-category` 属性

### 5. 关于我们页 (about.html)

| 位置 | 文件路径 | 建议尺寸 | 用途说明 |
|------|----------|----------|----------|
| 团队合照 | `/assets/images/team/group-photo.jpg` | 1200×600px | 团队合影 |
| 成员头像 | `/assets/images/members/member-*.jpg` | 400×400px | 个人头像，正方形 |

**修改位置**: 在 `<script>` 标签内的 `teamMembers` 数组中修改 `avatar` 字段

### 6. 二次开发定制页 (custom.html)

此页面无需图片资源，主要为表单和服务介绍。

### 7. 联系我们页 (contact.html)

| 位置 | 文件路径 | 建议尺寸 | 用途说明 |
|------|----------|----------|----------|
| 地图区域 | 可嵌入高德/百度地图iframe | - | 位置展示 |

---

## 👥 团队成员配置

### 修改位置: `about.html`

在 `<script>` 标签内的 `teamMembers` 数组中修改：

```javascript
const teamMembers = [
  {
    name: '张三',                    // 姓名
    role: '负责人',                  // 职位/角色
    avatar: '/assets/images/team/member-1.jpg',  // 头像路径
    skills: [                        // 技能标签
      { name: 'ROS2', level: 90 },
      { name: 'SLAM', level: 85 },
      { name: '深度学习', level: 80 }
    ],
    description: '负责整体技术架构设计与项目管理'  // 简介
  },
  // 添加更多成员...
];
```

### 技能等级说明
- `level`: 0-100 的数值，用于雷达图展示
- 技能数量建议: 3-5 个

---

## 📞 联系方式配置

### 修改位置: `contact.html`

在页面中搜索以下关键词进行修改：

| 配置项 | 搜索关键词 | 说明 |
|--------|------------|------|
| B站链接 | `bilibili.com` | 替换为工作室B站主页URL |
| 邮箱地址 | `@example.com` | 替换为真实邮箱 |
| 地址信息 | `潍坊科技学院` | 修改详细地址 |
| 电话号码 | `phone` | 添加联系电话 |

### 具体修改示例

```html
<!-- B站链接 -->
<a href="https://space.bilibili.com/你的UID" target="_blank">

<!-- 邮箱 -->
<a href="mailto:your-email@example.com">

<!-- 地址 -->
<p>山东省潍坊市寿光市潍坊科技学院</p>
<p>具体楼栋/房间号</p>

<!-- 电话 -->
<a href="tel:+86-138-xxxx-xxxx">138-xxxx-xxxx</a>
```

---

## 🎨 全局样式配置

### 修改位置: `css/global.css`

在 `:root` 中修改CSS变量：

```css
:root {
  /* 主题色 */
  --color-accent: #0071E3;        /* 主色调（蓝色） */
  --color-accent-purple: #5E5CE6; /* 辅助色（紫色） */
  
  /* 背景色 */
  --color-bg: #FFFFFF;            /* 主背景 */
  --color-bg-secondary: #F5F5F7;  /* 次级背景 */
  
  /* 文字色 */
  --color-text: #1D1D1F;          /* 主文字 */
  --color-text-secondary: #86868B;/* 次级文字 */
  
  /* 圆角大小 */
  --border-radius-md: 18px;
  --border-radius-lg: 24px;
  --border-radius-xl: 32px;
  
  /* 间距 */
  --spacing-md: 16px;
  --spacing-lg: 24px;
  --spacing-xl: 32px;
}
```

---

## 📝 文案配置

### 首页文案 (index.html)

| 位置 | 搜索关键词 | 当前内容 |
|------|------------|----------|
| 标题 | `hero-title` | 元核智算工作室 |
| 副标题 | `hero-subtitle` | 致力于构建数字孪生驱动的下一代智能机器人系统... |
| 学校名称 | `潍坊科技学院` | 可修改为其他学校 |

### 统计数据 (index.html)

搜索 `stats-grid` 修改：

```html
<div class="stat-number">12+</div>  <!-- 项目数量 -->
<div class="stat-number">4</div>    <!-- 机器人平台数 -->
```

### 页脚信息

所有页面的页脚统一配置：

```html
<div class="footer-info">© 2024 元核智算工作室 · 潍坊科技学院</div>
```

---

## 🔗 导航链接配置

### 修改位置: 所有HTML文件的 `<nav>` 部分

```html
<ul class="nav-links">
  <li><a href="index.html">首页</a></li>
  <li><a href="robots.html">核心成果</a></li>
  <li><a href="intelligence.html">智算控制台</a></li>
  <li><a href="custom.html">二次开发</a></li>
  <li><a href="archive.html">影像实验室</a></li>
  <li><a href="about.html">关于我们</a></li>
  <li><a href="contact.html">联系我们</a></li>  <!-- 新增 -->
</ul>
```

---

## 📋 快速检查清单

### 上线前检查

- [ ] 所有图片占位符已替换为真实图片
- [ ] 团队成员信息已填写完整
- [ ] 联系方式（邮箱、B站、地址）已更新
- [ ] 统计数据已核实
- [ ] 页脚版权年份已更新
- [ ] 所有页面链接可正常跳转
- [ ] 移动端显示正常
- [ ] 图片已压缩优化

### 图片格式建议

| 类型 | 格式 | 说明 |
|------|------|------|
| 照片 | JPG/WebP | 压缩质量 80-90% |
| 图标/截图 | PNG | 保持清晰度 |
| 视频 | MP4 (H.264) | 兼容性最好 |

---

## 📅 更新日志

| 日期 | 更新内容 |
|------|----------|
| 2024-xx-xx | 初始版本创建 |
| | |

---

> **注意**: 每次修改项目内容后，请同步更新此文档中的相关信息。
