# Auto Price Study
Анализ цен на автомобили: обработка данных и построение регрессионных моделей

Исследование выполнено с использованием Jupyter Notebook на языке программирования Python. В процессе анализа данных применялись следующие библиотеки: pandas, statsmodels.formula.api.

Задачи для Анализа:

1) Загрузить и предварительно обработать данные:
Загрузить данные и проверить их корректность. Проверить наличие пропущенных значений и определить типы данных.

2) Создать новый признак:
Ввести новый признак "марка автомобиля" (company). Идентифицировать производителей автомобилей, представленных в датасете. Внести необходимые коррективы в названия и проверить изменения.

3) Выбрать предикторы и проанализировать корреляцию:
Оставить только ключевые предикторы. Оценить корреляцию между ценой (price) и другими переменными.

4) Преобразовать категориальные переменные:
Использовать pd.get_dummies() для преобразования категориальных переменных.

5) Построить модели линейной регрессии:
Создать модель с одним предиктором - мощность двигателя (horsepower). Оценить процент изменчивости, объясненной данной моделью (R^2).

6) Сравнить модели:
Построить две модели: одну с использованием всех предикторов и вторую без учета марок машин. Сравнить изменения в (R^2), коэффициентах и их значимости. Принять решение о предпочтительной модели.

7) Обработать пропущенные значения:
Провести полный анализ:

Модель с одним предиктором (horsepower)

Модель со всеми предикторами

Модель со всеми предикторами, кроме марок машин

Выводы по Исследованию:

Был осуществлен анализ данных с целью подготовки и предварительной обработки информации. Создан новый признак "марка автомобиля" на основе столбца CarName, что привело к уменьшению количества уникальных производителей автомобилей. Далее были выбраны ключевые предикторы для прогнозирования цены, и оценена корреляция между ними.

Далее построены несколько моделей множественной линейной регрессии с одним предиктором (horsepower), также включая все предикторы и исключая марки машин. Модель с одним предиктором (horsepower), показала существенное влияние мощности двигателя на цену автомобилей, объясняя примерно 65% изменчивости. Модель, включающая все предикторы, продемонстрировала высокий R^2 примерно 95%, указывая на хорошее объяснение изменчивости цены. Даже при исключении марок машин, R^2 оставался на высоком уровне примерно 91%.

Таким образом, можно сделать вывод, что технические характеристики автомобилей, особенно мощность двигателя, существенно влияют на цену.
