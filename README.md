# Car Detection Dataset
**Датасет для дипломного проекта: распознавание автомобилей на видео с GPS‑привязкой**

![GitHub repo size](https://img.shields.io/github/repo-size/admiralbanan/Car_detection?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/admiralbanan/Car_detection?style=flat-square)
![GitHub License](https://img.shields.io/github/license/admiralbanan/Car_detection?style=flat-square)
![Dataset size](https://img.shields.io/badge/dataset%20size-2.6%20GB-blue?style=flat-square)

---

## Сводка
| Параметр | Значение |
|---|---|
| Размер базы | 2.6 ГБ |
| Лицензия | Открытая |

---

## Цель
Создать и опубликовать открытый датасет изображений трёх моделей автомобилей для обучения и сравнения алгоритмов классификации/распознавания, а также для экспериментов с интеграцией в видеопайплайн с GPS‑привязкой.

## Общая информация
- Всего изображений: 6283
- Классы: `audi_a6_c4`, `shkoda_fabia`, `uaz_images`
- Формат: JPEG
- Разрешение: разное (оригинальное); при обучении возможно предварительное Resize(800)
- Разметка: ручная (сортировка по папкам классов)
- Структура: `train` / `val` / `test`
- Источник данных: открытые источники
  - https://www.avito.ru
  - https://www.drive2.ru
  - https://yandex.ru/images
  - Yotube
  - Google images
- Инструмент сбора: ShareX (скриншоты и кадры из видео)

## Структура датасета
```
dataset/
├── train/
│   ├── audi_a6_c4/
│   ├── shkoda_fabia/
│   └── uaz_images/
├── val/
│   ├── audi_a6_c4/
│   ├── shkoda_fabia/
│   └── uaz_images/
└── test/
    ├── audi_a6_c4/
    ├── shkoda_fabia/
    └── uaz_images/
```


## Примеры изображений
| Класс | Пример |
|---|---|
| Audi A6 C4 | ![audi](https://github.com/admiralbanan/Car_detection/raw/main/dataset/train/audi_a6_c4/2330.jpg) |
| Skoda Fabia | ![fabia](https://github.com/admiralbanan/Car_detection/raw/main/dataset/train/shkoda_fabia/3000.jpg) |
| UAZ Patriot | ![uaz](https://github.com/admiralbanan/Car_detection/raw/main/dataset/train/uaz_images/1284.jpg) |

## Статистика по классам
| Класс           | Train | Val  | Test | Всего  |
|-----------------|------:|-----:|-----:|-------:|
| `audi_a6_c4`    | 2467  | 171  | 42   | **2680** |
| `shkoda_fabia`  | 1172  | 143  | 74   | **1389** |
| `uaz_images`    | 1984  | 176  | 54   | **2214** |
| **Итого**       | **5623** | **490** | **170** | **6283** |

## Загрузка и LFS
- Репозиторий использует Git LFS для хранения изображений; перед клонированием установите LFS и выполните `git lfs install`, затем обычный `git clone`.  
- При прямых загрузках отдельных файлов используйте ссылки raw GitHub (см. примеры выше).

## Использование
- Классификация по папкам: каждая подпапка — это метка класса; используйте любой фреймворк, поддерживающий загрузку из папочной структуры (PyTorch ImageFolder, tf.keras utils и т. п.).  
- Рекомендуемые сплиты: использовать предоставлённые каталоги `train`/`val`/`test` для корректной оценки без утечек.

## Качество и очистка
- Выполнен ручной контроль качества; при необходимости можно повторно проверить данные перцептуальным хешированием (pHash) или SHA‑256.  
- Изображения получены из открытых источников.

## Лицензия
Данные распространяются на условиях открытой лицензии.

## Цитирование
Если используете датасет в работе, пожалуйста, дайте ссылку на репозиторий.
