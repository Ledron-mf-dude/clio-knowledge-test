# UKRgaz: порядок доставки змін у Creatio

Перед будь-якою операцією прочитайте `core-rules` і `routing`, потім цей гайд.

## Визначення режиму
Викличте `get-fsm-mode` для середовища. Результат `on` або `off` визначає подальші кроки.

## FSM увімкнено
- C# або Angular: `dotnet build MainSolution.slnx -c dev-n8`, потім `restart-by-environment-name`.
- Схема змінена через MCP: після виклику виконайте `pkg-to-file-system`.
- Схема змінена у файлах: виконайте `pkg-to-db`.
- Не використовуйте `push-workspace` і `compile-creatio`.

## FSM вимкнено
`push-workspace`, далі `compile-creatio` (лише якщо змінювався C#), далі `restart-by-environment-name`.

## Після рестарту
Сесія clio може завершитись. Плануйте зміни схем до рестарту або заново авторизуйтесь перед повторною спробою.

## Правила
- Очікувані бізнес-помилки не кидайте винятками — повертайте error-as-value.
- Для нового коду створюйте тести у проєктах, згенерованих через `clio unit-test`.
- Ведіть щоденник у `.codex/workspace-diary.md`.
