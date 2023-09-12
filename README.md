# Домашнее задание к занятию «Как работает сеть в K8s»

### Цель задания

Настроить сетевую политику доступа к подам.

----

### Задание 1. Создать сетевую политику или несколько политик для обеспечения доступа

1. Создать deployment'ы приложений frontend, backend и cache и соответсвующие сервисы.
2. В качестве образа использовать network-multitool.
3. Разместить поды в namespace App.
4. Создать политики, чтобы обеспечить доступ frontend -> backend -> cache. Другие виды подключений должны быть запрещены.
5. Продемонстрировать, что трафик разрешён и запрещён.

### Ответ:

1. Создать deployment'ы приложений frontend, backend и cache и соответсвующие сервисы.

   [backend.yaml](https://github.com/askarpoff/kuber_ex13/blob/main/manifests/main/backend.yaml)
   [frontend.yaml](https://github.com/askarpoff/kuber_ex13/blob/main/manifests/main/frontend.yaml)
   [cache.yaml](https://github.com/askarpoff/kuber_ex13/blob/main/manifests/main/cache.yaml)
   
2. В качестве образа использовать network-multitool.
   
   ![image](https://github.com/askarpoff/kuber_ex13/assets/108946489/535eca37-9dcc-46d3-803a-f8a561f62fd8)
   
4. Разместить поды в namespace App.
   
5. Создать политики, чтобы обеспечить доступ frontend -> backend -> cache. Другие виды подключений должны быть запрещены.
   
4. Продемонстрировать, что трафик разрешён и запрещён.
