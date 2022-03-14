# Тестовое задание 5 Роли #
Установка сервера баз данных

## Предварительные условия ##
* Запущена ВМ с Centos 7
* На ВМ добавлен SSH - ключ родительской машины
* В файл `deploy/inventory.yml` добавлены адрес и порт SSH целевой виртуальной машины
* На родительской машине (или на ВМ от которой будет происходить управление)
  * установлен Ansible

## Запуск ##
### Все роли ###
```console
ansible-playbook ./configuration/deploy.yml -i ./configuration/inventory.yml
```
### Только NGINX ###
```console
ansible-playbook ./configuration/deploy.yml -i ./configuration/inventory.yml -e "only_nginx=true"
```
### Только MariaDB ###
```console
ansible-playbook ./configuration/deploy.yml -i ./configuration/inventory.yml -e "only_maria=true"
```