# GitHub Pages 部署步骤（手写版）

## 第一步：创建仓库

1. 打开 [github.com](https://github.com)，确认已登录
2. 右上角绿色按钮 **+** → **New repository**（新建仓库）
3. 填入以下信息：
   - **Repository name**（仓库名）：`fxjsai`（写这个）
   - **Description**（描述）：可填可不填
   - 勾选 **Public**（公开）
   - 勾选 **Add a README file**（添加 README 文件）
4. 点击底部绿色按钮 **Create repository**

---

## 第二步：上传网站文件

### 方法 A — 直接拖拽（最简单）

1. 仓库页面，点击 **Add file** → **Upload files**
2. 把 `wang-stone` 文件夹**里面的所有文件**拖进浏览器窗口：
   - `index.html`
   - `images` 文件夹（包含所有别墅照片）
3. 往下滚动，看到 **Commit changes**，点下面的绿色按钮
4. 等待上传完成

### 方法 B — 如果拖拽失败

1. 先把 `wang-stone` 文件夹压缩成 **fxjsai.zip**
2. 同上，拖进 GitHub 上传
3. 上传后点击文件名，看到右上角 **Raw** 或 **Download**，右键点击 **复制链接地址**
4. 用在线解压工具解压（可选）

---

## 第三步：开启 GitHub Pages

1. 仓库页面，点击上方菜单 **Settings**（设置）
2. 左侧菜单找到并点击 **Pages**（向下滚动才能看到）
3. **Branch**（分支）下拉框选择 **main**，点击 **Save**
4. 等待 1-2 分钟，页面会显示一个绿色提示：
   ```
   Your site is live at https://你的用户名.github.io/fxjsai
   ```
5. 点击这个链接，看看能否正常访问你的网站

---

## 第四步：绑定自定义域名 fxjsai.cn

### 在 GitHub 设置域名

1. 还是在 **Settings → Pages** 页面
2. 找到 **Custom domain**（自定义域名）输入框
3. 填入：`fxjsai.cn`
4. 点击 **Save**
5. 勾选下方的 **Enforce HTTPS**（强制 HTTPS）

### 在凡科网改 DNS 解析

1. 登录凡科网 → 找到 **域名管理** → **DNS 解析**
2. 找到类型为 **CNAME** 的记录，删除或修改
3. 新增一条 CNAME 记录：
   - **主机记录**：`@` 或留空
   - **记录类型**：`CNAME`
   - **记录值**：`你的用户名.github.io`（替换成你的真实用户名）
   - **TTL**：默认 10 分钟
4. 保存，等待生效（通常几分钟到几小时）

---

## 检查清单

完成以上步骤后，验证一下：

- [ ] 访问 `https://你的用户名.github.io/fxjsai` 能看到网站
- [ ] 访问 `https://fxjsai.cn` 也能看到网站（DNS 生效后）
- [ ] 手机访问正常
- [ ] 微信里打开能正常显示

---

## 如果卡住的地方

| 问题 | 解决方法 |
|------|----------|
| 找不到 Settings | 在仓库页面最上方，靠右边 |
| 找不到 Pages | 在 Settings 左边菜单，要向下滚动 |
| 上传文件失败 | 文件太大，一次少传几个，分批上传 |
| 网站打不开 | 检查是否上传了 index.html，文件名要对 |
| 域名不生效 | 等 2 小时，DNS 生效需要时间 |

---

## 后续维护

- **更新页面**：直接在 GitHub 仓库里修改 `index.html` 或替换图片
- **续费提醒**：GitHub 免费，但域名 fxjsai.cn 每年 98 元需要续费
- **备份**：GitHub 本身就是备份，换电脑也能下载
