##Отток клиентов
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

###Задачи:
Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Нам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.

Построим модель с предельно большим значением F1-меры. Доведем метрику до 0.59. Проверим F1-меру на тестовой выборке.

Дополнительно измерим AUC-ROC, сравним её значение с F1-мерой.

##Описание данных:

Признаки:

RowNumber — индекс строки в данных

CustomerId — уникальный идентификатор клиента

Surname — фамилия

CreditScore — кредитный рейтинг

Geography — страна проживания

Gender — пол

Age — возраст

Tenure — сколько лет человек является клиентом банка

Balance — баланс на счёте

NumOfProducts — количество продуктов банка, используемых клиентом

HasCrCard — наличие кредитной карты

IsActiveMember — активность клиента

EstimatedSalary — предполагаемая зарплата

Целевой признак

Exited — факт ухода клиента

##Выводы:


В ходе выполнения проекта разработана модель, имеющая достаточный уровень метрики f1. При этом в ходе подготовки данных были выявлены и заполнены пропуски в данных, исключены лишние столбцы, которые не имеют значения для обудения данных. Также проведена кодировка данных в целях исключения категориальных данных. Далее данные были разделены на тестовую, обучающую и валидационную выборки. При выполнении проекта были применены и сравнены модели "Случайный лес" и "Решающее дерево", как наиболее перспективные в рассматриваемом случае. Кроме того, выявлены значительный дисбалан данных.

В заключительной части проекта были применены методы увеличения выборки и уравновешивания по классам (по результатам был выбран уравновешанный "Случайный лес").

Результаты проверки модели "Случайный лес" на тестовой выборке показали, что модель обладает значением f1 0,61, которое превышается значение из условия задачи, что свидетельствует о выполнении поставленной задачи.

Дополнительно установлено, что метрика auc_roc, полученная по результатам проверки на тестовой выборке, значетельно НЕ отличается от значения, полученного на валидационных данных.