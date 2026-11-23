Лабораторная работа 7 (часть 1). ToDo backend в minikube

Задание 1: Кластер minikube
Скриншот 1(screenshots/lab7-1.png)
Узлов в кластере: 1 (minikube, статус Ready).
Компоненты control plane: kube-apiserver-minikube, etcd-minikube, kube-scheduler-minikube.

Задание 2: Pod без Deployment
Скриншот 2(screenshots/lab7-2.png)
Pod не появился снова, потому что создан напрямую, без контроллера (Deployment/ReplicaSet), который бы следил за количеством реплик.

 Задание 3: Backend: Deployment + Service
Скриншот 3(screenshots/lab7-3.png)
Скриншот 4(screenshots/lab7-4.png)

Задание 4: Самовосстановление
Скриншот 5(screenshots/lab7-5.png)
Имя нового Pod не совпадает со старым (другой суффикс).
Новый Pod создал Deployment через ReplicaSet, так как replicas: 2. В задании 2 Pod был без контроллера, поэтому не восстановился.
