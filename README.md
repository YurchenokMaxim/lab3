# Лабораторная работа #3.
# Изучение влияние параметра “темп обучения” на процесс обучения нейронной сети на примере решения задачи классификации Oregon Wildlife с использованием техники обучения Transfer Learning  #

 *** Описание архитектуры нейронной сети ***
В этой работе была попытка улучшить показатели нейронной сети с использованием *Transfer Learning*. Переносное обучение используется для ускорения обучения и повышения производительности модели глубокого обучения. Transfer Learning- это подход в глубоком обучении, при котором используются предварительно обученные модели,что позволяет сократить вычислительные и временные ресурсы для разработки нейронных сетей. Иными словами мы меняем классификатор, но при этом сохраняем ранее обученные модели.

  
  **Теперь о нашей задаче**


  ***Случай фиксированных темпов обучения***
  
  ![график 1.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracyp.svg)
  
  ![график 1.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_lossp.svg)
  
  
  ***Случай пошагового затухания ***
  
    
  ![график 2.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracystep.svg)
  
  ![график 2.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_lossstep.svg)
  

  
  ***Следующие графики были получены после изменения кода.***

  
  *Визуализация метрики качества.*
   
  ![график 2.1]()
  
  *Функция потерь*
   
  ![график 2.2]()
  
  
  
  ***Анализ данных.***
