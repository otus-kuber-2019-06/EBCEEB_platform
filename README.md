# EBCEEB_platform

EBCEEB Platform repository

### Домашнее задание 1

* Установлены (скачаны) kubectl, minicube, kind
* Создан и опубликован контейнер с nginx
* Создан и протестирован pod с двумя контейнерами: вышеуказанный с nginx и init-контейнер

Восстановление сервисов:

* kube-apiserver, kube-scheduler и kube-controller-manager созданы с `restartPolicy: Always`
* kube-proxy создан как daemonSet - должен быть запущен на каждом узле
* coredns создан как replicaSet с `replicas: 2` - всегда должно быть доступно 2 экземпляра
