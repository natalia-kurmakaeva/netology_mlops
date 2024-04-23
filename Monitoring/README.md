## Домашняя работа к занятию “Мониторинг”
## **Цель задания**

Научиться пользоваться инструментами bugtrasing и мониторинга, чтобы понимать, каким образом можно мониторить ваши приложения и готовить логи.

## **Задание**:

Необходимо установить и настроить на базе образа Grafana + Prometheus + alertmanager:
1. Скачиваем образ из репозитория - https://github.com/stefanprodan/dockprom
2. Собираем
3. Поднимаем
4. Проверяем, что всё работает через docker ps
5. Логинимся в Prometheus и изучаем настроенные alerts, rules
	** alerts, rules:
	** containers:
	* jenkins_down 			Jenkins down 
	* jenkins_high_cpu 		Jenkins high CPU usage
	* jenkins_high_memory 	Jenkins high memory usage
	** host:
	* high_cpu_load			Server under high load
	* high_memory_load 		Server memory is almost full
	* high_storage_load 	Server storage is almost full
	** targets
	* monitor_service_down	Monitor service non-operational
	
6. Логинимся в Grafana
7. Смотрим, что настроено в дашбордах и explore
	** Дашборды:
	* Docker Containers  ПО Docker
	* Docker Host ПО Docker
	* Monitor Services ПО: alertmanager, caddy, cadvisor, grafana, nodeexporter, prometheus, pushgateway
	* Nginx ПО Nginx
	
	** Docker Containers метрики:
		* CPU Load, CPU Cores, Memory Load, Used Memory, Storage Load, Used Storage, Running containers, System Load, I/O Usage, Container CPU Usage, Container Memory Usage, Container Cached Memory Usage, Container Network Input, Container Network Output
Домашнее задание выполните в файле readme.md в github репозитории.

## **Результат**:
 
1.	В личном кабинете отправьте на проверку ссылку на .md-файл в вашем репозитории.
2.	Перечислите алерты, которые настроены в Prometheus alerts.
3.	Перечислите количество dashboards в Grafana, для какого ПО они?
4.	Сделайте скриншот работающего dashboards docker containers grafana, перечислите метрики, которые там есть.

Также вы можете выполнить задание в Google Docs и отправить в личном кабинете на проверку ссылку на ваш документ. Название файла Google Docs должно содержать номер лекции и фамилию студента. Пример названия: "1.2. Docker — Товаркин Мананаж" Перед тем как выслать ссылку, убедитесь, что ее содержимое не является приватным (открыто на комментирование всем, у кого есть ссылка). Если необходимо прикрепить дополнительные ссылки, просто добавьте их в свой Google Docs.

## **Инструменты**:

Образ для работы - https://github.com/stefanprodan/dockprom  

Любые вопросы по решению задач задавайте в чате Slack.
