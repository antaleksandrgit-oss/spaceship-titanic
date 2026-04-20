Spaceship Titanic: Предсказание эвакуации пассажиров

Бизнес-задача
Космический корабль «Титаник» терпит крушение. Нужно предсказать, каких пассажиров удастся эвакуировать на спасательных шлюпках, чтобы оптимизировать распределение ресурсов и спасти максимум людей.

Цель: Построить модель классификации, которая по характеристикам пассажира (домашняя планета, возраст, траты на сервисы и т.д.) определит, будет ли он эвакуирован (Transported = True/False).

Технологический стек
- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn (RandomForestClassifier, LogisticRegression)
- Google Colab + GitHub

Краткий анализ данных (EDA)
- В датасете 8693 пассажира, 14 признаков.
- Есть пропуски в возрасте, каютах, информации о криосне.
- Пассажиры в режиме `CryoSleep` не тратили деньги на удобства (`RoomService`, `FoodCourt` = 0)

Подход к решению
1. Feature engineering: Создал признаки `FamilySize`, `IsAlone`, `TotalSpent`, извлёк номер каюты.
2. Обработка пропусков: Заполнение с учётом логических связей.
3. Модели: Сравнил RandomForest и LogisticRegression. Лучший результат дал RandomForest.

Результаты
- Метрика: Accuracy на валидации — **0.81**
- Важность признаков: Самые важные — `CryoSleep`, `TotalSpent`, `Age`.

Ссылки
- [Соревнование на Kaggle](https://www.kaggle.com/competitions/spaceship-titanic)
- [Ноутбук в Google Colab](https://colab.research.google.com/ваша-ссылка-пока-пустая)  <!-- добавите позже -->
- [Мой профиль Kaggle](https://www.kaggle.com/ваш-никнейм)

Контакты
- Telegram: @antaleksandr
- Email: AntAleksandrGit@gmail.com

---

Статус: Проект завершён, но планирую улучшить feature engineering и попробовать XGBoost.
