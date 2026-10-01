# claude-skills

مهاراتي (Skills) الخاصة بـ Claude.

## المهارات

| المهارة | شتسوي |
|---|---|
| [`ponytail`](skills/ponytail/SKILL.md) | يخلي Claude يكتب أقل كود يشتغل: يتجنب الشي الزايد (YAGNI)، يستخدم المكتبة القياسية وميزات المنصة أولاً، وأقصر تعديل ممكن. المستويات: `lite` / `full` / `ultra` |
| [`ponytail-review`](skills/ponytail-review/SKILL.md) | يراجع التعديلات ويطلع قائمة بالأشياء اللي تنحذف أو تتبسط |
| [`ponytail-audit`](skills/ponytail-audit/SKILL.md) | يفحص المشروع كله ويدور على التعقيد الزايد ويرتبه من الأكبر للأصغر |

## الاستخدام

- **تطبيق Claude:** المهارات محفوظة بالحساب، وتشتغل بروحها بأي مهمة برمجة.
- **Claude Code:** انسخ مجلد المهارة إلى `~/.claude/skills/` (لكل المشاريع) أو إلى `.claude/skills/` داخل المشروع.
- **النسخة الكاملة من Ponytail** (مع الـ hooks اللي تخليه شغال دائماً): نصّبها من Claude Code برسالتين منفصلتين:
  ```
  /plugin marketplace add DietrichGebert/ponytail
  ```
  ```
  /plugin install ponytail@ponytail
  ```

## المصدر والرخصة

مهارات Ponytail منقولة من [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) (الإصدار 4.10.0) بدون تعديل، وتحت رخصة MIT. نص الرخصة موجود في [`skills/LICENSE-ponytail`](skills/LICENSE-ponytail).
