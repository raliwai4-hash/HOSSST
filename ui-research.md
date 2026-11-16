# بحث أنماط واجهات منصات VPS وCloud

## الخلاصة التصميمية
البحث في الواجهات الرسمية لـDigitalOcean وHetzner Cloud وVercel وRailway وRender وCoolify أظهر أن أفضل لوحات VPS لا تعتمد على صفحة تسويقية طويلة داخل المنتج. النمط المشترك هو Control Plane عملي يبدأ بمساحة العمل أو المشروع، ثم يعرض الموارد كـInstances/Services، ويفتح تفاصيل كل مورد في تبويبات تشغيلية مثل Overview وDeployments وLogs وTerminal وResources وSettings.

الألوان في هذه المنتجات دلالية: اللون الأخضر للحالة الصحية، الأحمر للخطأ أو التدمير، الكهرماني للتحذير، واللون الأساسي للفعل الحالي. الحالة لا تعتمد على اللون وحده؛ تُعرض أيضًا كنص وأيقونة وإجراء تالٍ واضح. الإجراءات غير القابلة للعكس تستخدم تأكيدًا متدرجًا، بينما العمليات غير المتزامنة تعرض مراحلها وسجلاتها.

الأنماط التي سيتم تكييفها أصليًا في GOO HOST:

- شريط جانبي قابل للطي يحمل Workspace وInstances وTerminal وResources وDocs، مع topbar يوضح السياق الحالي.
- بطاقات موارد تجمع الاسم، الحالة، المنطقة، uptime، CPU/RAM/disk، والإجراء التالي مثل Open Terminal أو Start.
- صفحة تشغيل المورد كـOperations Hub: Overview وDeployments وLogs وTerminal وFiles وSettings.
- خلفية شبكية متحركة وglow محدود، مع حركة وظيفية: hover واضح، shimmer أثناء الانتظار، live pulse للحالة، ودخول تدريجي للبطاقات.
- Command palette/quick actions ومسارات واضحة للإجراءات، مع إبقاء الأفعال الخطرة داخل Danger Zone وتأكيديًا.
- Terminal حي وسجلات قابلة للبحث والتصفية، مع `OUT` و`ERR` وعرض حالة العملية نصيًا.

## المصادر الرسمية

- DigitalOcean Droplets: https://www.digitalocean.com/products/droplets
- DigitalOcean Droplet creation: https://docs.digitalocean.com/products/droplets/how-to/create/
- DigitalOcean Console: https://docs.digitalocean.com/products/droplets/how-to/connect-with-console/
- Hetzner Cloud: https://www.hetzner.com/cloud/
- Hetzner Cloud docs: https://docs.hetzner.com/cloud/
- Hetzner VNC console: https://docs.hetzner.com/cloud/servers/getting-started/vnc-console/
- Vercel dashboard: https://vercel.com/dashboard
- Vercel deployments: https://vercel.com/docs/deployments
- Vercel runtime logs: https://vercel.com/docs/logs/runtime
- Railway: https://railway.com/
- Railway observability: https://docs.railway.com/observability
- Railway staged changes: https://docs.railway.com/deployments/staged-changes
- Render dashboard: https://render.com/docs/render-dashboard
- Render logging: https://render.com/docs/logging
- Render service metrics: https://render.com/docs/service-metrics
- Coolify: https://coolify.io/
- Coolify canvas views: https://coolify.io/docs/core/canvas-views
- Coolify web terminal: https://coolify.io/docs/core/infrastructure/servers/web-terminal
