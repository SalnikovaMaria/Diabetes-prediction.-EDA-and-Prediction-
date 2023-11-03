# Задача классификации: предсказание наличия у пациента сахарного диабета. 
Дипломный проект DST Skillfactory. 

## Оглавление  
1. Описание проекта
2. Задачи проекта
3. Выводы

### Описание проекта    
Набор данных для прогнозирования диабета представляет собой совокупность медицинских и демографических данных пациентов, а также их статуса диабета (положительного или отрицательного). 
Данные включают в себя такие характеристики, как возраст, пол, индекс массы тела (ИМТ), гипертония, болезни сердца, история курения, уровень HbA1c и уровень глюкозы в крови. 

Этот набор данных можно использовать для создания моделей машинного обучения для прогнозирования диабета у пациентов на основе их истории болезни и демографической информации. 

Это может быть полезно для медицинских работников при выявлении пациентов, которые подвержены риску развития диабета, для разработки индивидуальных планов лечения. Кроме того, набор данных может быть использован исследователями для изучения взаимосвязи между различными медицинскими и демографическими факторами и вероятностью развития диабета.

* Цель: Построить модель на основе алгоритмов машинного обучения, которая предсказывает наличие/отсутствие заболевания у пациента.


### Этапы проекта:

1. Первичная обработка данных

2. Разведывательный анализ данных (EDA)

3. Отбор и преобразование признаков

4. Решение задачи классификации: логистическая регрессия, решающие деревья, ансамбли моделей и построение прогноза.

5. Анализ наиболее важных признаков.

5. Выводы


### Выводы:  

* лучшая модель по метрике f1-score GradientBoosting с подобранными настройками параметров или CatBoost(со стандарными настройками)

* лучшая модель по распознаванию класса 1 - GradientBoosting (со стандартными настройками), однако выдает значительно большее количество FP. Подойдет, если есть цель и возможность дообследовать большее количество пациентов, при этом не упустив действительно больных.

* CatBoost работает значительно быстрее, а по результатам практически не уступает GradientBoosting. В случае необходимости уменьшить FN, это можно отрегулировать уменьшением порога вероятности. Следовательно, модель выбора - CatBoost
