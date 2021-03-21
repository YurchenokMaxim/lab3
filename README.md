# Лабораторная работа #3.
# Изучение влияние параметра “темп обучения” на процесс обучения нейронной сети на примере решения задачи классификации Oregon Wildlife с использованием техники обучения Transfer Learning  #

 *** Описание архитектуры нейронной сети ***
В этой работе была попытка улучшить показатели нейронной сети с использованием *Transfer Learning*. Переносное обучение используется для ускорения обучения и повышения производительности модели глубокого обучения. Transfer Learning- это подход в глубоком обучении, при котором используются предварительно обученные модели,что позволяет сократить вычислительные и временные ресурсы для разработки нейронных сетей. Иными словами мы меняем классификатор, но при этом сохраняем ранее обученные модели.

  
  **Теперь о нашей задаче**


  ***Случай фиксированных темпов обучения***
  
  ![график 1.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracyp.svg)
  
  ![график 1.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_lossp.svg)
  
  
  ***Случай пошагового затухания ***
  
    
  ![график 2.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracy_s.svg)
  
  ![график 2.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_loss_s.svg)
  

***Случай экспоненциального затухания ***
    
  ![график 3.1](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_categorical_accuracye.svg)
  
  ![график 3.2](https://github.com/YurchenokMaxim/lab3/blob/main/epoch_losse.svg)
  


  
  
  
  ***Анализ данных.***
