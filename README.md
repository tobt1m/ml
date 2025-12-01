label 1
Весы стандартизируются перед свёрткой:
нормализация mean/std даёт более стабильное обучение.

label 2
Один сверточный блок сети:
Conv - BatchNorm - GELU - MaxPool - Dropout.

label 3
Модель

label 3.1
выбор устройства CPU или GPU

label 3.2
архитектура сети ConvBlock - GAP - Flatten - FC - GELU - Dropout - LayerNorm - FC

label 3.3
loss - optimizer - scheduler = CrossEntropy + Adam + ReduceLROnPlateau.

label 4
сохранение и загрузка весов

label 5
Аугментация

label 6
Препроцессинг + аугментации:
нормализация
флипы
random pad + crop
maskout
resize

label 7
Главный цикл обучения:
формируем батчи
считаем loss
делаем backward
считаем accuracy
считаем валидацию
сохраняем лучшую модель

label 8
Графики обучения

label 9
Предсказание одного изображения

label 10
Прогон всего датасета, считает accuracy

label 11
Рисует матрицу ошибок + classification_report
