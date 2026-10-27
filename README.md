# 台湾旅行网页 V2

打开 index.html 即可本地使用；也可将本文件夹发布到 GitHub Pages / Netlify / Cloudflare Pages。

## 已实现
- 9天详细行程，逐项修改时间、描述、备注、订票状态
- 每日嵌入 Google Maps 地图；每项一键打开 Google Maps 搜索
- 本机 localStorage 自动保存；最近100次修改快照、恢复、JSON 导入导出
- 可选 Supabase 云端同步接入界面

## 云端同步的安全限制（重要）
当前示例仅提供客户端接入流程，**没有部署数据库、没有配置用户登录或 RLS**。请不要把 `trip_documents` 表设为匿名可写并公开部署，这会允许未经授权修改数据。

正式上线推荐：Supabase Auth 邮箱登录 + 仅允许登录用户访问自己行程的 RLS 策略 + GitHub Pages 部署。需在 Supabase 控制台建立表和身份验证策略，完成后才可跨设备同步。不要在前端使用 service_role key。

## 资料来源
原始 docx 的日程表，少量风险注释另加；路线时间未全部实时验证。
