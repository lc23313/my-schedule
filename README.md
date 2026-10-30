# 我的日程

单文件日程管理网页。打开 `index.html` 就能用，不需要服务器、不需要联网。

- 时间段 / 截止时间两类事项，时间轴、日历、倒计时三种视图
- 到点弹页面内提醒卡片 + 提示音（+ 震动，没有震动的设备用屏幕闪烁代替）
- 数据默认只存在本机浏览器（`localStorage`）；可选开启 Supabase 多设备同步
- 已做微信内置浏览器（X5 / iOS WKWebView）适配

线上地址：`https://lc23313.github.io/my-schedule/`

## 本次优化（v3.8）

- 桌面双栏布局、手机自适应卡片，保留单文件离线使用方式。
- 今日完成进度、未来七天日期筛选，支持再次点击取消和一键重置。
- 搜索可一键清空，日历可一键回到今天；筛选无结果时给出操作提示。
- 修复日历已完成筛选、倒计时全部筛选，以及午夜新增事项的默认时间。
- 备份先校验再替换，保留本机同步配置；清空和恢复时记录删除，避免同步重新带回旧事项。
- 支持页面缩放、弹窗焦点管理和减少动画偏好。

## 更新线上版本

改完 `index.html` 之后：

```bash
git add -A
git commit -m "update"
git push
```

推送后大约 1 分钟生效，用 `Ctrl/Cmd + Shift + R` 强制刷新能看到新版。

## 首次部署到 GitHub Pages

见仓库根目录的提交记录或对话记录，核心三步：

1. 在 GitHub 新建公开仓库 `my-schedule`（免费账号必须公开才能用 Pages）
2. 把本目录内容推上去
3. 仓库 `Settings → Pages` → Source 选 `Deploy from a branch` → 分支 `main`、目录 `/ (root)` → Save

之后访问 `https://lc23313.github.io/my-schedule/`。
