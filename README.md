# AI Daily Workspace

每日 AI 新闻早报和午后 Reddit 洞察自动生成系统。

## Structure

```
workspace/
├── morning/
│   ├── template.html          # 早报模板
│   ├── 2026-02-08.html       # 当日早报
│   └── old/
│       └── 2026-02/          # 历史归档（按月份）
├── afternoon/
│   ├── template.html         # 午后模板
│   ├── 2026-02-08.html       # 当日午后
│   └── old/
│       └── 2026-02/          # 历史归档（按月份）
├── backup_daily.sh           # 每日备份脚本
└── vercel.json              # Vercel 路由配置
```

## URLs

| Page | URL |
|------|-----|
| 📰 Morning | https://workspace-one-woad.vercel.app/ |
| 🌤️ Afternoon | https://workspace-one-woad.vercel.app/afternoon |

## Workflow

1. **每日运行**: `backup_daily.sh`
2. 自动归档昨日文件到 `old/YYYY-MM/`
3. 从模板生成当日文件
4. Git 自动提交推送
5. Vercel 自动部署

## Deploy

自动部署到 Vercel（连接 GitHub 私有仓库 `code-nailao/workspace`）。
