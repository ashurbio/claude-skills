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
