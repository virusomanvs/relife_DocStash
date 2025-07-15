## 📁 Stash.json
Содержит список возможных **вариаций тайников**. Можно создать разными файлами json в папке profile/RELIFE/DOCSTASH/STASHES

Пример конфига
```json
[
  {
    "variationID": "Stash666",
    "selectChance": 1.0,
    "containerClassname": "SeaChest_Stash",
    "descriptionText": "Описание",
    "particleCreate": 0,
    "stashLifetimeOverride": 36600,
    "createInUnderground": 1,
    "itemsIDList": [0]
  }
]
```
| Параметр                | Тип         | Описание                                                                  |
| ----------------------- | ----------- | ------------------------------------------------------------------------- |
| `variationID`           | `string`      | Уникальный ID вариации схрона. Используется для ссылок в других конфигах. |
| `selectChance`          | `float`       | Шанс выбора этой вариации при создании схрона (0.0 - 1.0).                |
| `containerClassname`    | `string`      | Класс контейнера (например `SeaChest_Stash`).                             |
| `descriptionText`       | `string`      | Описание для отладки или справки.                                         |
| `particleCreate`        | `int (0/1)`   | Создавать ли визуальные эффекты при спавне ящика (не работает если он закапывается).                               |
| `stashLifetimeOverride` | `int`         | Время жизни схрона в секундах.                                            |
| `createInUnderground`   | `int (0/1)`   | Закапывать ли схрон в землю.                                          |
| `itemsIDList`           | `array\[int]` | Список ID предметов из папки profile/RELIFE/DOCSTASH/ITEMS.                                |
