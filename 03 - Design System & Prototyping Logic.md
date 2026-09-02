# Design System & Prototyping Logic

## Философия системы
Дизайн-система OKIYO построена по принципу **"Functional Prototyping"**.
В отличие от классических DS, ориентированных на передачу в верстку, эта система фокусируется на **логике взаимодействий и состояниях UI**. Токены здесь — это переменные управления поведением (валидация, фильтрация, навигация).
## 1. Типографика (Typography Tokens)
Шрифт: **Plus Jakarta Sans**. Размеры адаптированы под плотность B2B-интерфейсов.

| Token Name | Size (px) | Role / Usage |
| :--- | :--- | :--- |
| H1 | 42 | Главные заголовки страниц, Hero-секции |
| H2 | 32 | Заголовки секций, названия категорий |
| H3 | 26 | Подзаголовки, названия карточек продуктов |
| H4 | 22 | Метки, акцентный текст в списках |
| H5 | 20 | Текст кнопок, навигационные элементы |
| H6 | 18 | Основной body-текст, описания |
## 2. Цветовые токены (Color Tokens)
Финальная палитра «Industrial Clean». Строгая функциональная система без декоративного шума.

### Primary (Brand & Action)
| Token Name | Hex Value | Usage |
| :--- | :--- | :--- |
| **OKIYO Orange** | `#FF4E01` → `#FF8332` | Градиент. CTA Buttons, Active States, Focus Rings. Единственный яркий акцент конверсии. |
| **Deep Blue** | `#070911` → `#315182` | Градиент. Headers, Footer, Hero Backgrounds. Надежность и технологичность. |

### Neutral (Structure & Readability)
| Token Name | Hex Value | Usage |
| :--- | :--- | :--- |
| **Text Primary** | `#000000` | Основной текст, заголовки. Максимальный контраст (AAA). |
| **Gray Dark** | `#474B4D` | Второстепенный текст, подписи. |
| **Text Secondary** | `#999999` | Плейсхолдеры, disabled states, мета-информация. |
| **Border** | `#DCE1E6` | Рамки инпутов, разделители таблиц, границы карточек. |
| **Gray Light** | `#EEF2F7` | Фоны активных табов, hover-эффекты, информационные плашки. |
| **Background** | `#F7F8FB` | Общий фон страницы, поверхность под контентом. |
| **White** | `#FFFFFF` | Карточки товаров, поля ввода, модальные окна. |

### Secondary (Product Identity & UI States)
| Token Name | Hex Value | Usage |
| :--- | :--- | :--- |
| **Teal Medium** | `#002F6C` | Темные акценты продукта, иконки категорий. |
| **Teal Light** | `#004F9D` | Активные состояния ссылок, прогресс-бары. |
| **Teal** | `#3BA3A7` | Product Identity. Иллюстрации оборудования, теги, маркеры. |
| **Teal White** | `#BADEFE` | Фоновые подложки для Teal-элементов, selected tabs. |

## 3. Логические токены и Состояния (Logic & State Variables)
##### А. Валидация Форм (Form Validation)
*   `form_name`: Статус поля имени (`"none"` → `"click"` → `"valid"`)
*   `form_phone`: Статус поля телефона (`"none"` → `"click"` → `"valid"`)
*   `form_btn`: Состояние кнопки (`"disable"` ↔ `"enable"`)
    *   *Логика:* Active ONLY if `form_name == "valid" AND form_phone == "valid"`.
##### Б. Навигация и Контент
*   `Pages/[section]`: Флаги активности (`"disable"` / `"enable"`).
*   `overlay`: Управление модалками (`"none"` / `"active"`).
##### В. Интерактивные карты (Map Interactions)
*   `marker_text`: Название локации (ключ для переключения).
*   `marker`: Числовой ID (1-24).
*   *Логика:* При hover проверяется `marker_text`. Если совпадает → Change variant to ID.
##### Г. Отраслевые фильтры (Industry Filters)
*   `Отрасль_1` ... `Отрасль_6`: Статус (`[Name]_enable` / `[Name]_disable`).
*   *Логика:* Динамическая смена контента справа (картинка/кейс) без перезагрузки.
## 4. Компонентная база (Components)
*   **Input Field:** Меняет переменные `form_name`/`form_phone` при фокусе/вводе.
*   **Button (Primary):** Variant swap на `enable` только при валидации.
*   **Map Marker:** 24 варианта, переключаемых через строковую переменную.
*   **Product Card:** Поддержка Height-Collapse (501px ↔ 0px).
## 5. Универсальный шаблон страницы продукта (Content Template)
Единая структура описания для всех 25 карточек, обеспечивающая консистентность восприятия.

**Lead Text:**
> Advanced instrumentation for precise process control. Ensures optimization without interrupting production.

**Specifications List:**
*   **Installation:** Integrated mounting on existing infrastructure without production stoppage.
*   **Compatibility:** Seamless integration with current automation systems and regulatory compliance.
*   **Compliance:** Meets international safety standards (ISO/TR TS) for industrial use.
## 6. Engineering Challenges & Workarounds

1.  **Height-Collapse Grid:** Изменение высоты карточки до `0px` вместо `Visibility: Hidden`. Обеспечивает честную перестройку Auto Layout при фильтрации.
2.  **Text-Driven Map Logic:** Строковая переменная `marker_text` как ключ для 24 вариантов маркера. Заменяет 24 отдельных условия If/Else.
3.  **Manual Form Validation:** Эмуляция проверки полей через переменные состояния (`none` -> `click` -> `valid`).
4.  **Contextual Navigation:** Убрано глобальное меню в каталоге. Заменено на хлебные крошки и сайдбар для снижения когнитивной нагрузки.
## 7. Design Principles (Three-Buyer Blueprint)

| Роль | Главный вопрос | Решение в системе |
| :--- | :--- | :--- |
| Инженер | «Будет ли это работать?» | HTML-specs во вкладках, CAD-чертежи, фильтры по монтажу. |
| Закупщик | «Безопасен ли поставщик?» | Блок Certificates, Trust Logos, форма RFQ. |
| Директор | «Какой ROI?» | Блок Industries с метриками, кейсы, Executive Briefing. |

**Ключевые паттерны:**
*   **Industrial Clarity:** Контраст > Декор. Черный текст на белом фоне.
*   **Trust by Data:** Доверие через цифры и сертификаты, не лозунги.
*   **Action-Oriented UI:** Четкий следующий шаг на каждом экране. CTA всегда контрастный.
