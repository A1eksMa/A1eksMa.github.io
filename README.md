# a1eksma.github.io

Личный сайт-портфолио — интерактивная карта компетенций специалиста по данным.

**Сайт:** https://a1eksma.github.io/

---

## Статус

Сайт-заглушка. Деплой настроен, скелет готов. В процессе наполнения контентом.

- [x] Hugo + Congo, деплой через GitHub Actions
- [x] Структура разделов: Blog, Skills, Education, Projects, Contact
- [ ] Наполнение контентом (Этап 1)
- [ ] Интерактивная фильтрация по навыкам и сферам
- [ ] Future Roadmap на таймлайне

---

## Стек

| Компонент | Решение                                                    |
|-----------|------------------------------------------------------------|
| Генератор | [Hugo](https://gohugo.io/) v0.148.0 Extended               |
| Тема      | [Congo](https://github.com/jpanther/congo) (git submodule) |
| Хостинг   | GitHub Pages (ветка `gh-pages`)                            |
| CI/CD     | GitHub Actions                                             |
| Языки     | Русский (основной) + English                               |

---

## Структура веток

| Ветка      | Содержимое                                                  |
|------------|-------------------------------------------------------------|
| `main`     | Контент сайта (`content/`)                                  |
| `hugo`     | Hugo-конфиг, тема, ассеты (`config/`, `themes/`, `assets/`) |
| `gh-pages` | Собранный сайт (создаётся автоматически Actions)            |

**Принцип:** ветки разделены, чтобы история контента и история конфига не смешивались. Actions при сборке объединяет обе ветки.

---

## Деплой

Триггер: `push` в `main` с изменениями в `content/**`.

```
checkout main                                          → контент
git checkout origin/hugo -- config/ themes/ assets/   → конфиг поверх
git submodule update                                   → тема Congo
hugo --minify                                          → ./public/
peaceiris/actions-gh-pages                             → ./public/ → gh-pages
```

> После изменений в ветке `hugo` (конфиг, тема) сайт не пересобирается автоматически —
> нужен ручной запуск через `workflow_dispatch` (Actions → Run workflow).

---

## Структура контента

```
content/
├── _index.md                    # Главная (profile layout)
├── blog/YYYY/MM/DD/slug/        # Статьи и заметки
├── skills/                      # Карточки навыков (🟢🟡🔴)
├── education/                   # Курсы, книги
├── projects/                    # Проекты
└── contact/                     # Контакты
```

Посты блога следуют конвенции `YYYY/MM/DD/slug/index.md` — это упрощает навигацию и перекрёстные ссылки.

Легенда навыков:
- 🟢 Уверенное практическое владение
- 🟡 Есть опыт, понимаю принципы
- 🔴 Зона ближайшего развития

---

## Локальная разработка

Для работы с контентом нужна только ветка `main` — Hugo и конфиг подтягиваются из `origin/hugo`.

```bash
# Клонировать репозиторий
git clone https://github.com/A1eksMa/A1eksMa.github.io.git
cd A1eksMa.github.io

# Получить конфиг и тему из ветки hugo
git fetch origin
git checkout origin/hugo -- config/ themes/ assets/
git submodule update --init

# Запустить локальный сервер
hugo server -D
# → http://localhost:1313/
```

---

## Документация

Предложения и планы лежат в `docs/proposals/`:

- [`001-site-structure.md`](docs/proposals/001-site-structure.md) — структура и концепция
- [`002-implementation-plan.md`](docs/proposals/002-implementation-plan.md) — план реализации по этапам
- [`003-technical-requirements.md`](docs/proposals/003-technical-requirements.md) — технические требования
- [`competency_map.md`](docs/proposals/competency_map.md) — карта компетенций
