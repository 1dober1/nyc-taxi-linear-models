# NYC Taxi Trip Duration (Kaggle) — линейная модель + feature engineering

Решение для соревнования **New York City Taxi Trip Duration**: предсказание длительности поездки на такси в Нью-Йорке.  
Модель: **Ridge/Lasso Regression** с инженерией признаков. Метрика: **RMSLE**.

## Что сделано

- EDA по времени и пространству
- Признаки по времени: день недели, месяц, час, день года + индикатор аномального периода
- Признаки расстояния: haversine + `log_haversine`
- Признаки трафика: rush hour / free flow
- Признаки локаций: близость к аэропортам JFK/LGA, попадание в район Манхэттен
- Дискретизация координат: `pickup_cell` / `dropoff_cell` (grid)
- Feature interaction: `route_id` как (pickup_cell, dropoff_cell) для топ-маршрутов
- Формирование `submission.csv` для Kaggle (последняя часть ноутбука)
