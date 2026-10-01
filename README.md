# claude-skills

مهاراتي (Skills) الخاصة بـ Claude.

## المهارات

| المهارة | شتسوي |
|---|---|
| [`ponytail`](.claude/skills/ponytail/SKILL.md) | يخلي Claude يكتب أقل كود يشتغل: يتجنب الشي الزايد (YAGNI)، يستخدم المكتبة القياسية وميزات المنصة أولاً، وأقصر تعديل ممكن. المستويات: `lite` / `full` / `ultra` |
| [`ponytail-review`](.claude/skills/ponytail-review/SKILL.md) | يراجع التعديلات ويطلع قائمة بالأشياء اللي تنحذف أو تتبسط |
| [`ponytail-audit`](.claude/skills/ponytail-audit/SKILL.md) | يفحص المشروع كله ويدور على التعقيد الزايد ويرتبه من الأكبر للأصغر |
| [`systematic-debugging`](.claude/skills/systematic-debugging/SKILL.md) | تصليح الأخطاء بأربع مراحل: يلگى السبب الأصلي قبل أي تصليح، وإذا فشلت 3 محاولات يوگف ويراجع التصميم |
| [`verification-before-completion`](.claude/skills/verification-before-completion/SKILL.md) | ما يگول "خلص" أو "يشتغل" إلا بعد ما يشغّل الفحص ويشوف النتيجة بعينه |
| [`impeccable`](.claude/skills/impeccable/SKILL.md) | جودة تصميم الواجهات: 24 أمر (`/impeccable audit`، `critique`، `polish`، `typeset`...) وكاشف لأخطاء التصميم الشائعة. يشتغل بمهام الواجهات بس |
| [`webapp-testing`](.claude/skills/webapp-testing/SKILL.md) | يفتح موقعك بمتصفح حقيقي (Playwright)، يضغط ويجرب، ياخذ لقطات شاشة، ويقرا أخطاء الكونسول |
| [`grilling`](.claude/skills/grilling/SKILL.md) | قبل ما تبدي مشروع أو قرار: يسألك أسئلة على جولات، وكل سؤال وياه جوابه المقترح، لحد ما تتوضح الفكرة كاملة |
| [`teach`](.claude/skills/teach/SKILL.md) | `/teach <الموضوع>`: يسويلك كورس على مراحل بمجلد (دروس HTML، ملخصات، سجل تقدمك) ويكمل من وين ما وگفت |
| [`deepread`](.claude/skills/deepread/SKILL.md) | قراءة عميقة لكتاب أو محاضرة أو PDF: ملخص، خريطة أفكار، شرح فاينمان، وأسئلة مراجعة |
| [`statistical-analysis`](.claude/skills/statistical-analysis/SKILL.md) | تحليل نتائج التجارب: يختار الاختبار الإحصائي الصح (t-test، ANOVA، chi-square...)، يفحص الشروط، ويكتب النتيجة بصيغة علمية |
| [`experimental-design`](.claude/skills/experimental-design/SKILL.md) | تصميم التجربة قبل جمع البيانات: المجموعات، الكونترول، العشوائية، وعدد المكررات، حتى تطلع النتائج قابلة للتحليل |
| [`watch`](.claude/skills/watch/SKILL.md) | يشوف فيديو (رابط يوتيوب أو ملف): يطلع النص المكتوب ولقطات بتوقيتها، حتى تسأل عن محتواه أو تلخصه. يحتاج `ffmpeg` و`yt-dlp`، ومفتاح Gemini اختياري |

## الاستخدام

- **أضيف مهارة جديدة:** حطها بمجلد `.claude/skills/<اسم-المهارة>/SKILL.md`.
- **جلسات Claude Code السحابية:** افتح الجلسة على هذا المستودع، والمهارات وملف `CLAUDE.md` يشتغلون بروحهم.

- **تطبيق Claude:** المهارات محفوظة بالحساب، وتشتغل بروحها بأي مهمة برمجة.
- **Claude Code:** نصّب كل المهارات برسالتين منفصلتين:
  ```
  /plugin marketplace add ashurbio/claude-skills
  ```
  ```
  /plugin install ashur-skills@claude-skills
  ```
  وللتحديث بعد إضافة مهارات جديدة: `/plugin marketplace update claude-skills`
- **شريط الحالة [Claude HUD](https://github.com/jarrodwatts/claude-hud)** (يبين امتلاء المحادثة وحد الاستخدام تحت مربع الكتابة، للترمنل): نصّبه من مصدره، كل سطر برسالة منفصلة:
  ```
  /plugin marketplace add jarrodwatts/claude-hud
  ```
  ```
  /plugin install claude-hud@claude-hud
  ```
  ```
  /reload-plugins
  ```
  ```
  /claude-hud:setup
  ```
  بالويندوز يحتاج Node.js: `winget install OpenJS.NodeJS.LTS`
- **النسخة الكاملة من Ponytail** (مع الـ hooks اللي تخليه شغال دائماً): نصّبها من Claude Code برسالتين منفصلتين:
  ```
  /plugin marketplace add DietrichGebert/ponytail
  ```
  ```
  /plugin install ponytail@ponytail
  ```

## المصدر والرخصة

مهارات Ponytail منقولة من [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) (الإصدار 4.10.0) بدون تعديل، وتحت رخصة MIT. نص الرخصة موجود في [`.claude/skills/LICENSE-ponytail`](.claude/skills/LICENSE-ponytail).

مهارتا `systematic-debugging` و`verification-before-completion` منقولتان من [obra/superpowers](https://github.com/obra/superpowers) (الإصدار 6.4.2) بدون تعديل، وتحت رخصة MIT. نص الرخصة موجود في [`.claude/skills/LICENSE-superpowers`](.claude/skills/LICENSE-superpowers).

مهارة `impeccable` ووكلاؤها الفرعيون (`.claude/agents/impeccable-*`) منقولة من [pbakaus/impeccable](https://github.com/pbakaus/impeccable) (الإصدار 4.4.0) بدون تعديل، وتحت رخصة Apache 2.0. الرخصة والإشعارات في [`.claude/skills/LICENSE-impeccable`](.claude/skills/LICENSE-impeccable) و[`.claude/skills/NOTICE-impeccable.md`](.claude/skills/NOTICE-impeccable.md). الـ hooks التلقائية مالتها مو مضافة هنا؛ لتفعيلها نصّب الإضافة الأصلية.

مهارة `webapp-testing` منقولة من [anthropics/skills](https://github.com/anthropics/skills) بدون تعديل، وتحت رخصة Apache 2.0 (النص داخل مجلدها: `LICENSE.txt`).

مهارتا `grilling` و`teach` منقولتان من [mattpocock/skills](https://github.com/mattpocock/skills) بدون تعديل، وتحت رخصة MIT. نص الرخصة موجود في [`.claude/skills/LICENSE-mattpocock`](.claude/skills/LICENSE-mattpocock).

مهارة `deepread` منقولة من [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) بدون تعديل، وتحت رخصة MIT. نص الرخصة موجود في [`.claude/skills/LICENSE-alirezarezvani`](.claude/skills/LICENSE-alirezarezvani).

مهارتا `statistical-analysis` و`experimental-design` منقولتان من [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) (الإصدار 2.72.0)، وتحت رخصة MIT. التعديل الوحيد: حذفت قسم "Citing Scientific Agent Skills" اللي يطلب إضافة بحثهم لمراجع تقاريرك. نص الرخصة موجود في [`.claude/skills/LICENSE-kdense`](.claude/skills/LICENSE-kdense).

مهارة `watch` منقولة من [bradautomates/claude-video](https://github.com/bradautomates/claude-video) (الإصدار 0.3.2) بدون تعديل، وتحت رخصة MIT. نص الرخصة موجود في [`.claude/skills/LICENSE-claude-video`](.claude/skills/LICENSE-claude-video). الـ hook مالتها (يفحص التنصيب ببداية الجلسة) مو مضاف هنا.
