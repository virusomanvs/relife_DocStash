📁 relife_DocStash.json (основной конфиг)
Описывает общие настройки, карты и список документов, которые могут запускать создание схронов.

Пример конфига
```json
{
  "attemptFailedSpawn": 10,
  "mapsSizeList": {
    "chernarusplus": 15360,
    "enoch": 12800
  },
  "listOfDocs": [
    {
      "className": "RLF_Secret_Docs_Base",
      "textInDocAfterRead": "Coordinates %1",
      "descriptionInConfig": "just text in json",
      "chanceToSpawn": 1.0,
      "addMarkerInModdedMap": 0,
      "minSpawnDistanceAtPlayer": 1000,
      "maxSpawnDistanceAtPlayer": 1100,
      "spawnInSelectRadius": 0,
      "stashPosition": [
        {
          "radiusCenterPos": [0.0, 0.0, 0.0],
          "radiusDistance": 200,
          "selectChance": 1.0
        }
      ],
      "stashVariousIDList": ["Stash666"]
    }
  ],
  "warning0": "WARNING! DO NOT EDIT BELLOW!",
  "allItemsList": [],
  "allStashVariation": []
}
```
| Параметр             | Тип    | Описание                                       |
| -------------------- | ------ | ---------------------------------------------- |
| `attemptFailedSpawn` | int    | Кол-во попыток при неудачном спавне схрона.    |
| `mapsSizeList`       | object | Список карт и их размеров.                     |
| `listOfDocs`         | array  | Список настроек документов.                    |
| `warning0`           | string | Системное предупреждение (не изменять).        |
| `allItemsList`       | array  | Автогенерируемый список всех предметов. Не трогать!        |
| `allStashVariation`  | array  | Автогенерируемый список всех вариаций схронов. Не трогать!|

Параметры объекта listOfDocs

| Параметр                   | Тип            | Описание                                                      |
| -------------------------- | -------------- | ------------------------------------------------------------- |
| `className`                | string         | Класс документа.                                              |
| `textInDocAfterRead`       | string         | Текст после чтения документа ( `%1` заменится на координаты, поэтому наличие обязательно!). |
| `descriptionInConfig`      | string         | Комментарий в конфиге.                                        |
| `chanceToSpawn`            | float          | Шанс спавна документа.                                        |
| `addMarkerInModdedMap`     | bool (0/1)      | Добавлять ли маркер на карту.                                 |
| `minSpawnDistanceAtPlayer` | float          | Минимальная дистанция от игрока.                              |
| `maxSpawnDistanceAtPlayer` | float          | Максимальная дистанция от игрока.                             |
| `spawnInSelectRadius`      | bool (0/1)      | Спавнить ли строго в выбранном радиусе из списка ниже stashPosition.                       |
| `stashPosition`            | array          | Список областей с радиусами для спавна.                       |
| `stashVariousIDList`       | array\[string] | ID вариаций схронов из папки `STASHES`.                          |

Параметры объекта stashPosition

| Параметр          | Тип           | Описание                       |
| ----------------- | ------------- | ------------------------------ |
| `radiusCenterPos` | vector | XYZ координаты центра области. |
| `radiusDistance`  | float         | Радиус области спавна.         |
| `selectChance`    | float         | Шанс выбрать эту область среди остальных областей из списка.      |

