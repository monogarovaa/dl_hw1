# dl_hw1

Эксперимент 1
На тестовых данных получается минимальный loss = 0.1759
максимальный AUC = 0.9323
Оптимальное количество эпох 30-35, дальше модель начинает переобучаться
![experiment_1_combined](https://github.com/user-attachments/assets/716aae0a-a206-4eba-8434-991d80bf2a92)


Эксперимент 2
На тестовых данных минимальный loss = 0.1726 максимальный AUC = 0.9337
Видно, что переобучение начинается примерно на 27-й эпохе. Графики testloss и testauc стали более резкими, но в целом наблюдается значительное улучшение по сравнению с предыдущей моделью
![experiment_2_combined](https://github.com/user-attachments/assets/54674ee0-dcc3-4cac-88ec-8ff476158a68)


Эксперимент 3
На тестовых данных минимальный loss = 0.1764
максимальный AUC = 0.9318
Лучше не стало. Возможно, Skip Connections и Batch Norm делает модель более чувствительной к batch_size и learning_rate
Возможно, сработало бы с большим количеством слоёв.

![experiment_3_combined](https://github.com/user-attachments/assets/f4f81b79-d9e8-4867-9cc4-a35aac40a765)

Эксперимент 4
На тестовых данных минимальный loss = 0.1755
максимальный AUC = 0.9312
Стало лучше относительно 3 эксперимента, но хуже 2-го (возможно learning_rate неподходящий). Наилучшие результаты с dropout_rate = 0.5, при dropout_rate меньше 0.2 происходит переобучение
![compare_dropout](https://github.com/user-attachments/assets/9054261a-e755-40a1-9c88-af66b9fca975)



Эксперимент 5
Лучшие результаты при learning_rate=0.05 weight_decay=0.001
При больших их значениях график test_loss сильно колеблется
Стало лучше 2-го эксперимента, модель обучается быстрее
Test AUC = 0.9341
Test Loss = 0.1760
![experiment_5_lr_0 05_wd_0 001_combined](https://github.com/user-attachments/assets/782b868b-2b50-46b5-8518-f88c8c8d539d)
