# Тестовое задание

Для выполнения задания был создан кластер k8s на kubeadm, состоящий из мастер ноды и 4 воркеров.    

Кластер разворачивается после команды terraform apply в папке nodes, дальше ansible настраивает ноды.    

После завершения работы terraform на мастер ноде требуется запустить flannel.sh для установки плагина.    

Содержимое созданного ансиблом файла init.output.txt нужно скопировать и поместить на хостовой машине в корневом каталоге проекта в плейбук join.yml

Затем деплоймент [deploy.yml](https://github.com/dimanbanan/testing-task/blob/main/files/deploy.yml) копируется на мастер ноду и запускается 

```
kubectl apply -f deploy.yml

```
