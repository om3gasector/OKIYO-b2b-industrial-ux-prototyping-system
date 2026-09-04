# OKIYO Automation: B2B Industrial UI/UX Redesign

> Концептуальный редизайн сайта промышленного оборудования. Трансформация устаревшего каталога в интерактивный цифровой продукт с фокусом на конверсию и техническую точность.

[![Figma Prototype](https://img.shields.io/badge/Figma-Prototype-F24E1E?style=for-the-badge&logo=figma)](https://www.figma.com/proto/c6KoufZFgjeI21E3nCquK5/OKIYO-industrial-project?node-id=41-821&p=f&t=tcNhYM9DUaD7rQZ9-0&scaling=scale-down-width&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=41%3A821&hide-ui=1)
[![Dribbble Shot](https://img.shields.io/badge/Dribbble-Shot-ea4c89?style=for-the-badge&logo=dribbble)](https://dribbble.com/shots/27510308-Avatar-Configurator-Gamified-UI-UX-Design-System)

# ВИДОС

## О проекте
Этот проект родился из простого инсайта: промышленный B2B-веб застрял в прошлом. Текстовые стены, отсутствие каталогов и путь до заявки в 5+ кликов убивают конверсию. OKIYO — это ответ на эту проблему. Интерфейс построен на модели **Three-Buyer Blueprint**, закрывая вопросы Инженера, Закупщика и Директора за 1-2 клика.

## Документация
| Документ | Описание |
| :--- | :--- |
| [01 - Бриф и контекст](./01%20-%20Бриф%20и%20контекст.md) | Задача, аудитория, бенчмаркинг конкурентов |
| [02 - Информационная архитектура](./02%20-%20Информационная%20архитектура.md) | Sitemap, User Flows, баланс каталога (25 карточек) |
| [03 - Design System & Logic](./03%20-%20Design%20System%20&%20Prototyping%20Logic.md) | Токены, логика прототипа, Engineering Challenges |
| [04 - Метрики и валидация](./04%20-%20Метрики%20и%20валидация.md) | Usability-тесты, гипотезы Maze, KPIs |

## Технические особенности прототипа
Прототип реализован в Figma с использованием продвинутых техник эмуляции фронтенда (0 строк кода):
- **Height-Collapse Grid:** Динамическая перестройка сетки через изменение высоты компонентов до `0px` вместо скрытия слоёв.
- **Text-Driven Map Logic:** Управление 24 вариантами маркеров карты через одну строковую переменную.
- **Manual Form Validation:** Эмуляция валидации полей формы через переменные состояния (`none` → `click` → `valid`).
- **Multi-Entry Navigation:** 3 точки входа в каталог, синхронизированные через глобальные переменные.

## Результаты валидации
| Метрика | Было (As-Is) | Стало (OKIYO) | Изменение |
| :--- | :--- | :--- | :--- |
| Клики до каталога | 3–5 | 1 | **-80%** |
| Клики до заявки (RFQ) | 5+ | 1-2 | **-60%** |
| Время до элементов доверия | Не сканируется | <5 сек | **Доступно** |
| Формат тех. данных | Только PDF | HTML Tabs + Download | **Мгновенно** |

## Стек инструментов
- **Design & Prototyping:** Figma (Variables/ Tokens, Component Based design, Properties, Auto Layout)
- **Validation:** Maze (Quantitative), Face-to-face Usability Testing (Qualitative)
- **Documentation:** Markdown / Obsidian
- **Benchmarking:** Chevron, AWS, Owen, Metran

## Лицензия
Этот проект является концептуальной работой для портфолио. Все торговые марки и изображения принадлежат их правообладателям. 3D-рендеры сгенерированы специально для проекта.

<img width="1600" height="1200" alt="1" src="https://github.com/user-attachments/assets/7b143908-3052-47a8-8950-7a64c1554d89" />
<img width="1600" height="1200" alt="3" src="https://github.com/user-attachments/assets/e0a58ace-78f3-4283-85ca-7cc84e92830d" />
<img width="1600" height="1200" alt="4" src="https://github.com/user-attachments/assets/154a8dfe-a233-4c15-9cfd-8735cffe4b18" />
<img width="1600" height="1200" alt="2" src="https://github.com/user-attachments/assets/4c2ccc21-84d5-4c3d-991c-5ccefc5c9871" />

<img width="1600" height="2860" alt="Slice 2" src="https://github.com/user-attachments/assets/4a028bf7-72e7-4999-ad7b-073acddf8b30" />
<img width="1600" height="3244" alt="Slice 2 (1)" src="https://github.com/user-attachments/assets/553af661-2afb-496f-800c-6a1f5e6f8dde" />



<img width="1600" height="1200" alt="6" src="https://github.com/user-attachments/assets/14777a4b-1a08-4d5f-90bc-82f20517ffe1" />
<img width="1600" height="1200" alt="7" src="https://github.com/user-attachments/assets/99c9afb5-8bc0-4325-b9b3-0905287280ff" />
<img width="1600" height="1200" alt="8" src="https://github.com/user-attachments/assets/cbe9ac89-0aa9-4d0d-967c-c189fcd42400" />
<img width="1600" height="1200" alt="9" src="https://github.com/user-attachments/assets/4cbfdb28-4fc2-4673-85e5-5872a51c0abc" />
<img width="1920" height="1080" alt="10" src="https://github.com/user-attachments/assets/2fc19af6-aa50-456f-aa51-f82a3522841a" />

---
**Автор:** [Валерий Попков](https://dribbble.com/om3gasector) • Проектировщик интерфейсов • Samara, Russia
