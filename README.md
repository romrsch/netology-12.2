### Домашнее задание к занятию "12.2 Команды для работы с Kubernetes"

#### Задание 1: Запуск пода из образа в деплойменте

Установил дополнительно kubelet и kubeadm,  kubectl уже был установлен 
```
romrsch@ubuntu:~/devops-projects/kuber$ minikube status
minikube
type: Control Plane
host: Running
kubelet: Running
apiserver: Running
kubeconfig: Configured
```
>Требуется запустить деплоймент на основе образа из hello world уже через deployment. Сразу стоит запустить 2 копии >приложения (replicas=2).

![Alt text](https://i.ibb.co/ct8LWdZ/Screenshot-3.jpg)

#### Задание 2: Просмотр логов для разработки
Конфиг пользователя:
![Alt text](https://i.ibb.co/dW5x52P/Screenshot-5.jpg)

#### Задание 3: Изменение количества реплик

