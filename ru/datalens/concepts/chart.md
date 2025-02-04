# Чарт

_Чарт_ — это визуализация данных из датасета в виде таблицы или диаграммы.

Чарты создаются в [визарде](https://datalens.yandex.ru/wizard/) на основе данных из датасета.
На базе одного датасета может быть создано неограниченное количество чартов.

Рабочая область в интерфейсе визарда разделена на три основные панели:
1. Панель выбора, где отображаются поля датасета: **Измерения** и **Показатели**.
1. Панель настройки визуализации, где можно выбрать представление. Для каждого представления доступен свой набор секций (например, ось X, ось Y, фильтры и т.д.), куда можно перетаскивать измерения и показатели.
1. Панель превью, где отображается визуализация.

Чарт позволяет провести быстрый анализ и проверить гипотезу. Также чарты можно сохранять и выносить на дашборды в виде виджетов.

## Тип чарта {#chart-types}

В {{ datalens-full-name }} доступны следующие типы чартов:

 - [Таблица](#flat-table)
 - [Сводная таблица](#pivot-table)
 - [Линейная диаграмма](#line-chart)
 - [Диаграмма с областями](#area-chart)
 - [Круговая диаграмма](#pie-chart)
 - [Столбчатая диаграмма](#bar-chart)
 - [Древовидная диаграмма](#tree-chart)
 - [Точечная диаграмма](#scatter-chart)

### Простая таблица {#flat-table}

Отображает данные в табличном виде, где в первой строке определяются наименования полей, в остальных — их значения.

Секция | Описание
----- | ----
Столбцы  | Измерения и показатели, которые будут использованы в качестве столбцов. Имя поля используется для заголовка столбца
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Цвета  | Показатель. Влияет на заливку ячеек. Может содержать не более одного показателя
Сортировка  | Измерения и показатели, которые указаны в секции **Столбцы**.<br/>Вы можете использовать несколько измерений и показателей.<br/>Порядок полей в секции влияет на порядок сортировки полей таблицы

### Сводная таблица {#pivot-table}

Отображает данные в табличном виде, где в строках и столбцах могут быть значения измерений, а в ячейках на их пересечении — показатели.

Секция | Описание
----- | ----
Столбцы  | Измерения
Строки  | Измерения
Показатели | Показатели. При добавлении в секцию более одного показателя в секции Столбцы появится измерение **Measure Names**, которое определяет расположение заголовков показателей. **Measure Names** можно переносить в **Строки**
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Цвета  | Показатель. Влияет на заливку ячеек. Может содержать не более одного показателя
Сортировка  | Измерения и показатели, которые указаны в секциях **Столбцы** и **Строки**.<br/>Вы можете использовать несколько измерений и показателей.<br/>Порядок полей в секции влияет на порядок сортировки полей таблицы

### Линейная диаграмма {#line-chart}

Отображает изменение показателей по измерениям в виде горизонтальной линии.

Секция | Описание
----- | ----
X | Измерение. Может быть указано только одно поле
Y | Показатель.  Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции Цвета появится измерение **Measure Names**
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Цвета | Измерение или поле **Measure Names**. Влияет на цвет линий. **Measure Names** удаляется путем удаления показателей с оси Y
Сортировка | Измерение. Может использовать только одно измерение с оси Х. Влияет на сортировку оси X

### Диаграмма с областями {#area-chart}

Отображает изменение показателей по измерениям в виде областей, показывая вклад каждой линии в значение общей суммы.

Секция | Описание
----- | ----
X  | Измерение. Может быть указано только одно поле
Y  | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции Цвета появится измерение **Measure Names**
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Цвета  | Измерение или поле **Measure Names**. Влияет на цвет линий. **Measure Names** удаляется путем удаления показателей с оси Y
Сортировка  | Измерение. Может использовать только одно измерение с оси Х. Влияет на сортировку оси X

### Круговая диаграмма {#pie-chart}

Отображает размер элементов одного ряда данных относительно суммы элементов в виде круга.

Секция | Описание
----- | ----
Измерения  | Измерение. Может быть указано только одно поле
Показатели  | Показатель. Может быть указано только одно поле
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Сортировка  | Показатель или измерение. Одно измерение из секции Х или любой Показатель. Влияет на сортировку

### Столбчатая диаграмма {#bar-chart}

Отображает данные в виде плоских вертикальных столбцов.

Секция | Описание
----- | ----
X  | Измерения. Может быть указано одно или два измерения
Y  | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции Цвета появится измерение **Measure Names**. **Measure Names** можно перенести на ось Х
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Цвета  | Измерение или поле **Measure Names**. Влияет на цвет линий. **Measure Names** удаляется путем удаления показателей с оси Y
Сортировка  | Измерения и показатели. Влияет на сортировку столбцов

### Древовидная диаграмма {#tree-chart}

Отображается в виде набор прямоугольников. Диаграмма позволяет сравнить пропорции в иерархии.

Диаграмма позволяет сравнить пропорции в иерархии.

Секция | Описание
----- | ----
Измерения  | Измерения. Определяют дерево иерархии вложенности прямоугольников
Размер  | Показатель. Один показатель определяющий величину площади прямоугольника
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Цвета  | Показатель или Измерение. Влияет на заливку прямоугольников

### Точечная диаграмма {#scatter-chart}

Отображает точки данных для сравнения пар значений.

Секция | Описание
----- | ----
X  | Измерение или показатель по оси X
Y  | Измерение или показатель по оси Y
Точки | Точки - Измерение. Определяет количество точек на диаграмме
Фильтры | Измерения и показатели, которые используются в качестве фильтра
Цвета  | Измерение или показатель. Влияет на цвет точек
Сортировка  | Показатель. Влияет на сортировку столбцов


## Управление доступом {#access-management}

Вы можете настроить права доступа к чарту. Подробнее в разделе [{#T}](../security/index.md).

#### См. также {#see-also}
- [{#T}](../operations/chart/create-pivot-table.md)
- [{#T}](../operations/chart/create-table.md)
- [{#T}](../operations/chart/create-line-chart.md)
- [{#T}](../operations/chart/create-area-chart.md)
- [{#T}](../operations/chart/create-bar-chart.md)
- [{#T}](../operations/chart/create-pie-chart.md)



