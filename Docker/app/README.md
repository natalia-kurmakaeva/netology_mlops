## Домашняя работа к занятию “Docker и микросервисная архитектура”

## **Цель**: 

Закрепить полученные знания по технологии контейнеризации Docker путём написания dockerfile с последующей сборкой и подъёмом на его базе докер-контейнера.

## **Задание**:
Необходимо сделать dockerfile для получения рабочего контейнера.
1.	В качестве основы, берём образ continuumio/miniconda3:latest
2.	Добавляем и делаем рабочей папкой /app 
3.	Создаём простой sh файл с названием 1.sh, который должен выдавать надпись “Hello Netology”.
4.	Надо скопировать этот файл внутрь контейнера и выдать ему права на исполнение.
5.	Запустить установку пакетов python mlflow boto3 pymysql.
6.	В конце запустить на вывод файл 1.sh.
7.	После чего собрать через docker build контейнер с тегом netology-ml:netology-ml

Домашнее задание выполните в файле readme.md в github репозитории.

## **Результат**: 
В личном кабинете отправьте на проверку ссылку на .md-файл в вашем репозитории.Приложите:
- полученный dockerfile
- лог выполнения сборки

ЗЫ  - Не удаляйте images, он может понадобиться в следующих ДЗ.

Также вы можете выполнить задание в Google Docs и отправить в личном кабинете на проверку ссылку на ваш документ. Название файла Google Docs должно содержать номер лекции и фамилию студента. Пример названия: "1.2. Docker — Товаркин Мананаж" Перед тем как выслать ссылку, убедитесь, что ее содержимое не является приватным (открыто на комментирование всем, у кого есть ссылка). Если необходимо прикрепить дополнительные ссылки, просто добавьте их в свой Google Docs.

## **Инструменты**:

●	Репозиторий с домашним заданием https://github.com/Netology-DS/devops-mlops/tree/master/Docker   
●	Образ continuumio/miniconda3:latest


## Выполнение домашнего задания - командная строка:
● docker build -t netology-ml:netology-ml .
● docker run -d -p 80:80 netology-ml:netology-ml


## Выполнение домашнего задания - командная строка:
● docker build -t netology-ml:netology-ml .
● docker run -d -p 80:80 netology-ml:netology-ml

Лог выполнения сборки (при повторном запуске):
D:\git\devops-mlops\Docker\app>docker build -t netology-ml:netology-ml .
[+] Building 0.0s (0/0)  docker:default
[+] Building 2.3s (9/9) FINISHED                                                                                                                                             docker:default
 => [internal] load build definition from Dockerfile                                                                                                                                   0.0s
 => => transferring dockerfile: 226B                                                                                                                                                   0.0s
 => [internal] load metadata for docker.io/continuumio/miniconda3:latest                                                                                                               1.8s
 => [internal] load .dockerignore                                                                                                                                                      0.1s
 => => transferring context: 2B                                                                                                                                                        0.0s
 => [1/4] FROM docker.io/continuumio/miniconda3:latest@sha256:2016f249cdae34692a20d90fdb17432d07cf312992345d0e1e492bc36a12a35b                                                         0.0s
 => [internal] load build context                                                                                                                                                      0.2s
 => => transferring context: 81B                                                                                                                                                       0.0s
 => CACHED [2/4] RUN pip install pymysql  && pip install mlflow  && pip install boto3                                                                                                  0.0s
 => [3/4] COPY ./1.sh /1.sh                                                                                                                                                            0.0s
 => [4/4] COPY ./1.py /1.py                                                                                                                                                            0.0s
 => exporting to image                                                                                                                                                                 0.0s
 => => exporting layers                                                                                                                                                                0.0s
 => => writing image sha256:57b1644c7ed3e651c659009c87a2bd80d790919fe6bee7468801008ef1a7dd0e                                                                                           0.0s
 => => naming to docker.io/library/netology-ml:netology-ml                                                                                                                             0.0s

What's Next?
  View a summary of image vulnerabilities and recommendations → docker scout quickview

D:\git\devops-mlops\Docker\app>docker run -d -p 80:80 netology-ml:netology-ml
6b36bb475283d859e8e4f73a413b6264874cd46e4c9e8a162b2137ef1c8a9b72


