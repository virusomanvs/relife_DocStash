📁 ItemConfig.json (конфиг предметов)
Определяет предметы, которые будут помещены в схроны.

Пример конфига
```json
[
  {
    "itemID": 0,
    "classNamesList": ["Apple", "Pear"],
    "className": "Apple",
    "chanceToSpawn": 1.0,
    "itemCount": 2,
    "itemHealth": [1.0, -1.0, -1.0],
    "isStackable": 0,
    "itemQuantity": [1.0, -1.0, -1.0]
  },
  {
    "itemID": 1,
    "classNamesList": ["Apple", "Pear"],
    "className": "Apple",
    "chanceToSpawn": 1.0,
    "itemCount": 2,
    "itemHealth": [1.0, -1.0, -1.0],
    "isStackable": 0,
    "itemQuantity": [1.0, -1.0, -1.0]
  }
]
```
| Параметр         | Тип            | Описание                                                |
| ---------------- | -------------- | ------------------------------------------------------- |
| `itemID`         | `int`            | Уникальный ID для связи с `itemsIDList` в `Stash.json`. |
| `classNamesList` | `array\[string]`| Список возможных классов предмета. Выбираются просто случайно                  |
| `chanceToSpawn`  | `float`          | Шанс спавна предмета.                                   |
| `itemCount`      | `int `           | Количество предметов в контейнере.                      |
| `itemHealth`     | `array\[float]`  | Состояние предмета по здоровью от 0 до 1: \[fix, min, max]. Если первый параметр не -1, то будет браться он, иначе рандом от 2 параметра до 3                 |
| `isStackable`    | `int (0/1) `     | Стакуемый ли предмет.                                   |
| `itemQuantity`   | `array\[float]`  | Количество в стаке от 0 до 1: \[fix, min, max]. Если первый параметр не -1, то будет браться он, иначе рандом от 2 параметра до 3                  |


