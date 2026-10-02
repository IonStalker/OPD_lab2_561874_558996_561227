# OPD Lab 2: Unity + Git

Учебный проект: 2D-платформер на Unity (шаблон Simple 2D Template).
Лабораторная работа №2 «Основы работы с Git в движке Unity».

## Команда
| Рыцев Арсений | Сеньор |
| Руфов Илья | Джуниор |
| Остафичук Кирилл | Девопс |

## Требования
- Unity **6000.6.3f1** (версия должна совпадать у всех, иначе возможны конфликты в сценах)
- Git

## Как запустить
1. Клонировать репозиторий:
   `https://github.com/IonStalker/OPD_lab2_561874_558996_561227.git`
2. Открыть папку проекта в Unity Hub (Add → Add project from disk).
3. Дождаться импорта ассетов (первый запуск долгий).
4. Открыть сцену `Assets/IndieMarc/PlatformerDemo/PlatformerDemo.unity`.
5. Нажать Play.

## Документация
- [Структура проекта](docs/structure.md)
- [Геймплей и физика](docs/gameplay.md)
- [Сборка и состав проекта](docs/build.md)
- [Список изменений уровня](docs/changelog.md)

## CI/CD
При каждом пуше GitHub Actions (`.github/workflows/main.yml`) запускает тесты Unity
в режимах EditMode и PlayMode, а затем собирает игру под Windows.
Результаты видны на вкладке Actions.
