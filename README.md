# Лабораторная работа №3.
# Изучение влияние параметра “темп обучения” на процесс обучения нейронной сети на примере решения задачи классификации Oregon Wildlife с использованием техники обучения Transfer Learning  #

В этой работе были проделаны попытки улучшить обучение нейронной сети, с помощью изменения темпов обучения. Конкретно в этой работе были опробованы методы фиксированного темпа обучения, пошагового затухания и экспоненциального затухания.


  **Теперь о нашей задаче**

  ***Случай фиксированных темпов обучения***
  
![фикс](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%84%D0%B8%D0%BA%D1%81.png)

График с коэффициентом 0.1 имеет точность выше, а потери меньше.
  
  ***график точности для фиксированного темпа обучения***
  
  
  ![график 1.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracyp.svg)
  
   ***график потерь для фиксированного темпа обучения***
  
  ![график 1.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_lossp.svg)
  
  **По графикам видно, что лучшие результаты были у фиксированного темпа с коэффициентом 0.01 .**
  
  
 ***Случай пошагового затухания***
  
  Функция для этого затухания:
  
   ![пошагa](https://github.com/YurchenokMaxim/lab3/blob/main/%D0%BF%D0%BE%D1%88%D0%B0%D0%B3%D1%84.png)
    
 ***график точности для пошагового обучения***
 
 ![пошаг](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%88%D0%B0%D0%B3.png)
      
  ![график 2.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracy_s.svg)
  
  ***график потерь для пошагового обучения***
  
  ![график 2.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_loss_s.svg)
  

***Случай экспоненциального затухания***

![эксп](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%8D%D0%BA%D1%81%D0%BF.png)
  
  Функция этого затухания выглядит так:

  ![экспф](https://github.com/YurchenokMaxim/lab3/blob/main/%D1%8D%D0%BA%D1%81%D0%BF%D1%84.png)

  ***график точности для экспоненциального затухания*******

  ![график 3.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracye.svg)
  
  ***график потерь для экспоненциального затухания*******
  
  ![график 3.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_losse.svg)
  

  
  ***Анализ данных.***
