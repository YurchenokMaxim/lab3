# Лабораторная работа №3.
# Изучение влияние параметра “темп обучения” на процесс обучения нейронной сети на примере решения задачи классификации Oregon Wildlife с использованием техники обучения Transfer Learning  #

В этой работе были проделаны попытки улучшить обучение нейронной сети, с помощью изменения темпов обучения. Конкретно в этой работе были опробованы методы фиксированного темпа обучения, пошагового затухания и экспоненциального затухания.


  **Теперь о нашей задаче**

  ***Случай фиксированных темпов обучения***
  
![фикс](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%84%D0%B8%D0%BA%D1%81.png)

1. коэффициент 0.1 тренировка
2. коэффициент 0.1 валидация
3. коэффициент 0.01 тренировка
4. коэффициент 0.01 валидация
5. коэффициент 0.001 тренировка
6. коэффициент 0.001 валидация
7. коэффициент 0.0001 тренировка
8. коэффициент 0.0001 валидация

График с коэффициентом 0.1 имеет точность выше, а потери меньше, чем у 0.0001.
  
  ***график точности для фиксированного темпа обучения***
  
  
  ![график 1.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracyp.svg)
  
   ***график потерь для фиксированного темпа обучения***
  
  ![график 1.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_lossp.svg)
  
  **По графикам видно, что лучшие результаты были у фиксированного темпа с коэффициентом 0.01 .**
  
  
 ***Случай пошагового затухания***
  
  Функция для этого затухания:
  
   ![пошагф](https://github.com/YurchenokMaxim/lab3/blob/main/%D0%BF%D0%BE%D1%88%D0%B0%D0%B3%D1%84.png)
   
   ![пошаг](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%88%D0%B0%D0%B3.png)
   
  1. drop= 0.5 и epoch_ drops= 10 тренировка
  2. drop= 0.5 и epoch_ drops= 10 валидация
  3. drop= 0.2 и epoch_ drops= 2 тренировка
  4. drop= 0.2 и epoch_ drops= 2 валидация
  5. drop= 0.4 и epoch_ drops= 4 тренировка
  6. drop= 0.4 и epoch_ drops= 4 валидация
    
 ***график точности для пошагового обучения***
      
  ![график 2.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracy_s.svg)
  
  ***график потерь для пошагового обучения***
  
  ![график 2.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_loss_s.svg)
  
Среди данных опытов с разными коэффициентами наилучший результат показало пошаговое затухание с коэффициентами drop= 0.2 и epoch_ drops= 2. В отличии от ближайшего конкурента с параметрами drop=0.4 и epoch_ drops=4 , сходимость лучше на 14 эпох, а точность различна менее чем на 0.5 процента.

***Случай экспоненциального затухания***

![эксп](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%8D%D0%BA%D1%81%D0%BF.png)

1. k=0.4 обучение
2. k=0.4 валидация
3. k=0.1 обучение
4. k=0.1 валидация
5. k=0.9 обучение 
6. k=0.9 валидация
  
  Функция этого затухания выглядит так:

  ![экспф](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%8D%D0%BA%D1%81%D0%BF%D1%84.png)

  ***график точности для экспоненциального затухания*******

  ![график 3.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracye.svg)
  
  ***график потерь для экспоненциального затухания*******
  
  ![график 3.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_losse.svg)
  
Экспоненциальное затухание с параметром равным 0.4 показало наилучшую точность, но коэффициент 0.9 дал лучшую сходимость(сходимость с 0.9 произошла на 6ой эпохе, что на 7 эпох быстрее, чем у 0.4, при различии в точности на валидации между ними менее чем на 1 процент). В итоге лучшим в этом затухании оказалось затухание с параметром 0.9 .
  
  ***Анализ данных.***
 Итогом этой работы стало то, что наилучший метод изменения темпов обучения это экспоненциальный, потому что его абсолютная сходимость превышает пошаговый метод на 6 эпох, а по точности он обогнал фиксированное приближение на 2 процента. Пошаговый же метод уступает экспоненциальному еще и в точности на 0.5 процента.
