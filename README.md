# Классификация музыкальных жанров на основе аудиопризнаков

## Описание проекта
Данный репозиторий содержит курсовую работу на тему *"Классификация музыкальных жанров на основе аудиопризнаков"*, выполненную студентом Хоменко Иваном Михайловичем (группа Э-2110) в рамках дисциплины "Методы и средства интеллектуального анализа данных в экономике" СПбГЭУ

Проект направлен на сравнение различных методов классификации (k-NN, SVM, Random Forest, XGBClassifier) для определения жанра музыкальных композиций.

## Построение моделей
В работе реализованы следующие модели:
- **Baseline модель**: k-ближайших соседей с настройками по умолчанию.
- **k-NN**: модель с оптимизацией гиперпараметров (количество соседей, тип расстояния, веса).
- **SVM**: метод опорных векторов с подбором гиперпараметров (C, kernel, gamma).
- **Random Forest**: случайный лес с подобором количества деревьев, максимальной глубины и минимального числа разбиений.
- **XGBClassifier**: градиентный бустинг с подбором гиперпараметров (число деревьев, темп обучения, максимальная глубина).

## Оценка моделей
Модели оценивались по следующим метрикам:
- **Accuracy** – доля правильно классифицированных наблюдений.
- **ROC-AUC** – площадь под ROC-кривой, рассчитанная по схеме One-vs-Rest для многоклассовой классификации.
- **Время обучения** – эффективность модели с точки затрат времени.

**Результаты:**
- **Baseline**: Accuracy ≈ 0.45, ROC-AUC ≈ 0.82.
- **k-NN**: Accuracy ≈ 0.54, ROC-AUC ≈ 0.90, время обучения ≈ 3.5 сек.
- **SVM**: Accuracy ≈ 0.58, ROC-AUC ≈ 0.93, время обучения ≈ 205.4 сек.
- **Random Forest**: Accuracy ≈ 0.59, ROC-AUC ≈ 0.93, время обучения ≈ 7.5 сек.
- **XGBClassifier**: Accuracy ≈ 0.66, ROC-AUC ≈ 0.95, время обучения ≈ 10.3 сек.

## Выводы
В ходе работы было проведено сравнение различных алгоритмов классификации музыкальных жанров. Наилучшие результаты показала модель XGBClassifier. Однако общая точность классификации остаётся на уровне 22%, что указывает на возможность дальнейших улучшений.
