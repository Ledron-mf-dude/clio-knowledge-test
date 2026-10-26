# clio-knowledge-ukrgaz

Приватне джерело знань (гайденсів) для clio / Creatio у проєктах UKRgaz. Структура за зразком [clio-knowledge](https://github.com/Advance-Technologies-Foundation/clio-knowledge).

```bash
clio add-knowledge-source --alias ukrgaz --library-id com.ukrgaz.creatio --type git --location <URL цього репозиторію> --branch main
clio enable-knowledge-source --alias ukrgaz
clio install-knowledge --source ukrgaz
```
