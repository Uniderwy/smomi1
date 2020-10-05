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

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88ac.jpg)

Графики функции потерь

![alt text](https://github.com/Uniderwy/smomi1/blob/main/88loss.jpg)
