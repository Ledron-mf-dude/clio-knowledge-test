# UKRgaz: доступ до даних у Freedom UI

Angular-модулі Freedom UI читають і пишуть дані лише через `@creatio-devkit/common`.

## Робити
- `Model.create`, `model.load`, `model.insert`, `model.update`.
- Пагінація: `options.pagingConfig { rowsOffset, rowCount }`.
- Сортування: `options.sortingConfig.columns[{ columnName, direction }]`, де `direction` — рядок `'asc' | 'desc' | 'none'`.

## Не робити
- Не використовуйте OData.
- Не викликайте DataService напряму через HTTP.

Детальний чекліст — у reference `ukrgaz-entity-checklist`.
