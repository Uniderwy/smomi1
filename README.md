# smomi1
По умолчанию `BATCH_SIZE = 64` `lr=0.000001`.

1. В данной модели 2 сверточных слоя, каждый по 8 фильтров.
```
def build_model():
    return tf.keras.models.Sequential([
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    ])
```
Графики точности
оранжевый - train
синий - validation

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88loss.jpg)

2. В данной модели 3 сверточных слоя, каждый по 8 фильтров.
```
def build_model():
    return tf.keras.models.Sequential([
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    ])
```
Графики точности
оранжевый - train
синий - validation

![alt text](https://github.com/Uniderwy/smomi1/blob/main/888ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/888loss.jpg)

3. В данной модели 3 сверточных слоя, первые два по 8 фильтров, третий - 16.
```
def build_model():
    return tf.keras.models.Sequential([
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    ])
```
Графики точности
оранжевый - train
синий - validation

![alt text](https://github.com/Uniderwy/smomi1/blob/main/8816ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/8816loss.jpg)

4. В данной модели 4 сверточных слоя, первые два по 8 фильтров, третий и четвертый - по 16.
```
def build_model():
    return tf.keras.models.Sequential([
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    ])
```
Графики точности
розовый - train
зеленый - validation

![alt text](https://github.com/Uniderwy/smomi1/blob/main/881616ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/881616loss.jpg)


5. В данной модели 4 сверточных слоя, первые два по 8 фильтров, третий - 16, четвертый - 32.
```
def build_model():
    return tf.keras.models.Sequential([
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    ])
```
Графики точности
красный - train
голубой - validation

![alt text](https://github.com/Uniderwy/smomi1/blob/main/881632ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/881632loss.jpg)

6. В данной модели 5 сверточных слоев, первые два по 8 фильтров, третий - 16, четвертый и пятый - 32.
```
def build_model():
    return tf.keras.models.Sequential([
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    ])
```
Графики точности
красный - train
голубой - validation

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88163232ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88163232loss.jpg)

7. В данной модели 5 сверточных слоев, первые два по 8 фильтров, третий - 16, четвертый - 32, пятый - 64.
```
def build_model():
    return tf.keras.models.Sequential([
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=64, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
    ])
```
Графики точности
розовый - train
зеленый - validation

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88163264ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88163264loss.jpg)
