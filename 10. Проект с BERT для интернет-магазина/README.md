## Задача

**Проект для интернет-магазина (с BERT)**

Интернет-магазин запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.

Необходимо обучить модель классифицировать комментарии на позитивные и негативные. Для проекта предоставлен набор данных с разметкой о токсичности правок.

Необходимо построить модель со значением метрики качества F1 не меньше 0.75.

Краткий план проекта:
 - загрузить и подготовить данные.
 - обучить разные модели.
 - сделать выводы.

### Цель проекта
 - построить модель классификации комментариев на позитивные и негативные,
 - для оценки качества использовать метрику F1
 - значение метрики F1 не должно быть меньше 0.75

## Данные

Данные находятся в файле `toxic_comments.csv`. Столбец `text` в нём содержит текст комментария, а toxic — целевой признак.

## Используемые библиотеки
*pandas*, *sklearn*, *matplotlib*, *seaborn*, *optuna*, *xgboost*, *catboost*, *nltk*, *spacy*, *transformers*, *wordcloud*, *tqdm*, *torch*

## Результаты
В ходе выполнения проекта исходные текстовые данные были преобразованы в TF-IDF embeddings и BERT embeddings. На основе этих данных обучены и исследованы неколько моделей. Детальные результаты исследования приведены в тетрадке `online_store_project.ipynb`. По итогам проекта получена модель, значение метрики качества F1 которой не меньше 0.75.