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

### Домашнее задание 2

* Созданы пространства имён
* Созданы служебные учётные записи
* Созданы и назначены роли, как глобальные, так и локальные для пространства имён

### Домашнее задание 3

* Создан деплоймент с 3 экземплярами пода web (ReplicaSet) c heathcheck
* Создан сервис ClusterIP для подов созданных деплойментом
* kube-proxy переключен в режим балансировки через IPVS
* Установлен MetalLB, настроен пул адресов
* Создан сервис LoadBalancer для подов созданных деплойментом
* Созданы сервисы (TCP и UDP) LoadBalancer для CoreDNS
* Установлен ingress-nginx
* Создан сервис LoadBalancer для ingress-nginx
* Создан headless сервис для подов созданных деплойментом
* Создан ingress-proxy (на URL /web) для подов созданных деплойментом
