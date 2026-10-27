# 台湾旅行网页 V3 · Supabase 云端版

将 `index.html` 与 `data.json` 上传到 GitHub 仓库根目录；GitHub Pages 发布。

- 公共行程保存在 Supabase `trip_itinerary` 的 `id=main` 行；访客只读。
- 管理员通过 Supabase Auth 邮箱密码登录，UID 与数据库 RLS 匹配。
- 管理员首次登录后，在「账号 / 备份」点击「首次导入」，只允许空表导入。
- 修改触发 `trip_history` 的数据库记录，历史恢复会生成新记录。
- 行程及备注是公开数据，请勿填写订单号或个人隐私。
- Google Maps 嵌入仅显示当日酒店位置；逐站可点击打开地图搜索。
- 不要将 Supabase secret/service_role key 放进网页。
- 之前版本的本地浏览器修改不会自动迁移；首次导入使用内嵌原始行程。
- 原始路线尚有未核实交通和景点时间，不能当作实时道路开放证明。
