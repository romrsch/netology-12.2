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
>Разработчикам крайне важно получать обратную связь от штатно работающего приложения и, еще важнее, об ошибках в его работе. >Требуется создать пользователя и выдать ему доступ на чтение конфигурации и логов подов в app-namespace.
>Требования:
>* создан новый токен доступа для пользователя
>* пользователь прописан в локальный конфиг (~/.kube/config, блок users)
>* пользователь может просматривать логи подов и их конфигурацию (kubectl logs pod <pod_id>, kubectl describe pod <pod_id>)

Сделал по инструкции:
[Как создать пользователя с правами администратора для доступа к Kubernetes Dashboard](https://itsecforu.ru/2020/01/30/%E2%98%B8%EF%B8%8F-%D0%BA%D0%B0%D0%BA-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D1%82%D1%8C-%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F-%D1%81-%D0%BF%D1%80%D0%B0%D0%B2%D0%B0%D0%BC/)

Создал админа: ```itsecforu-admin```
![Alt text](https://i.ibb.co/bBdkP5n/Screenshot-6.jpg)

![Alt text](https://i.ibb.co/9gsHKQ7/Screenshot-8.jpg)

Конфиг пользователя:
![Alt text](https://i.ibb.co/dW5x52P/Screenshot-5.jpg)

> пользователь может просматривать логи подов (правда логи были пустые) и их конфигурацию

![Alt text](https://i.ibb.co/q05nmfK/Screenshot-11.jpg)

![Alt text](https://i.ibb.co/HnMz6J2/Screenshot-12.jpg)
![Alt text](https://i.ibb.co/FHNf5Zc/Screenshot-13.jpg)

#### Задание 3: Изменение количества реплик
> в deployment из задания 1 изменено количество реплик на 5
![Alt text](https://i.ibb.co/pxKxHb4/Screenshot-14.jpg)

> проверить что все поды перешли в статус running (kubectl get pods)
![Alt text](https://i.ibb.co/KKVr1F6/Screenshot-15.jpg)
