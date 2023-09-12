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
   
3. Разместить поды в namespace App.

   ![image](https://github.com/askarpoff/kuber_ex13/assets/108946489/6edcb94f-6721-416a-9d4b-09ca399a1ff6)

4. Создать политики, чтобы обеспечить доступ frontend -> backend -> cache. Другие виды подключений должны быть запрещены.

   Политика по-умолчанию запрещает всё
   [default.yaml](https://github.com/askarpoff/kuber_ex13/blob/main/manifests/network-policy/default.yaml)

   Политика бэкенда разрешает доступ от фронтенда
   [backend.yaml](https://github.com/askarpoff/kuber_ex13/blob/main/manifests/network-policy/backend.yaml)

   Политика кэша разрешает доступ от бэкенда
   [cache.yaml](https://github.com/askarpoff/kuber_ex13/blob/main/manifests/network-policy/cache.yaml)
   
5. Продемонстрировать, что трафик разрешён и запрещён.

   ![image](https://github.com/askarpoff/kuber_ex13/assets/108946489/22f74c99-0350-4f5e-b8fa-7001d56aced6)

