# OKIYO Automation: B2B Industrial UI/UX Redesign

> Концептуальный редизайн сайта промышленного оборудования. Трансформация устаревшего каталога в интерактивный цифровой продукт с фокусом на конверсию и техническую точность.

[![Figma Prototype](https://img.shields.io/badge/Figma-Prototype-F24E1E?style=for-the-badge&logo=figma)](https://www.figma.com/proto/c6KoufZFgjeI21E3nCquK5/OKIYO-industrial-project?node-id=41-821&p=f&t=tcNhYM9DUaD7rQZ9-0&scaling=scale-down-width&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=41%3A821&hide-ui=1)
[![Dribbble Shot](https://img.shields.io/badge/Dribbble-Shot-ea4c89?style=for-the-badge&logo=dribbble)](https://dribbble.com/shots/27510308-Avatar-Configurator-Gamified-UI-UX-Design-System)


<img width="1600" height="1200" alt="1" src="https://github.com/user-attachments/assets/7b143908-3052-47a8-8950-7a64c1554d89" />


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
- **Design & Prototyping:** Figma (Variables, Component Properties, Auto Layout)
- **Validation:** Maze (Quantitative), Face-to-face Usability Testing (Qualitative)
- **Documentation:** Markdown / Obsidian
- **Benchmarking:** Chevron, AWS, Owen, Metran

## Лицензия
Этот проект является концептуальной работой для портфолио. Все торговые марки и изображения принадлежат их правообладателям. 3D-рендеры сгенерированы специально для проекта.

---
**Автор:** [Валерий Попков](https://dribbble.com/om3gasector) • Проектировщик интерфейсов • Samara, Russia
