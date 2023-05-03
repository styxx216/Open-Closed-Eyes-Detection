# Open/Closed Eyes Detection

### Задача
Построить и обучить модель, которая получает на вход черно-белое изображение глаза формата 24 x 24 пикселя и возвращает 1 в случае открытого глаза и 0 - в случае закрытого.

Модель состоит из CNN-энкодера из 3 сверточных слоев и классификатора

### Описание выбранного подхода:
В первом слое идет свертка с ядром 5 x 5 с функцией активации ReLu, слой MaxPooling.
Далее - 2 блока, включающие слой свертки с ядром 3 x 3.
Классификатор состоит из 2 слоев с функцией активации sigmoid.


### Возможные улучшения:
1. Протестировать различные варианты энкодеров и классификаторов
2. Дополнительно дообучить классификатор
3. Использовать кластеризацию неразмеченных данных на фичах из энкодера
4. Использовать трансферное обучение (например, на основе VGG)
5. Возможно, понижать размер output-а свертки не за счет MaxPooling-а, а через увеличение stirde.
