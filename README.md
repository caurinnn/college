![image](https://github.com/user-attachments/assets/3948dd49-2f32-498d-98e3-85eae9e86151)



# ***Docker Compose**

1. На скриншоте показан процесс установки **VirtualBox Guest Additions (гостевых дополнений)** на ОС Linux. Этот процесс происходит в терминале, и на экране отображается информация о ходе установки.

![image](https://github.com/user-attachments/assets/17190e4a-1602-46b2-9545-cd686edbd61a)

2. Далее идет настройка общего буфера обмена. Настраиваем передачу файлов **из основной в гостевую ОС.**

![image](https://github.com/user-attachments/assets/42e41946-3353-48c8-8b83-a0c2555721f2)

3. `sudo yum install wget`

Команда, устанавливающая пакет `wget`.
Скриншот показывает успешное выполнение команды установки пакета `curl` с помощью `sudo`. Система сообщает, что пакет уже установлен, и все зависимости разрешены. Сообщение "Выполнено!" подтверждает, что операция завершена успешно.

![image](https://github.com/user-attachments/assets/017bd979-3abd-48e0-a34d-6b8e80565b7c)

![image](https://github.com/user-attachments/assets/765f5599-c4b6-4d5d-b318-8385d8b96e7c)

4. `sudo wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo`

Выполняет скачивание файла репозитория Docker CE и сохраняет его в указанную директорию.

![image](https://github.com/user-attachments/assets/011675f1-397e-4120-b6e2-b85e626efd8a)

5. `sudo yum install docker-ce docker-ce-cli containerd.io`

Команда устанавливает три основных пакета, необходимых для работы с Docker CE:
- **docker-ce**: основной пакет Docker.
- **docker-ce-cli**: утилита командной строки для управления Docker.
- **containerd.io**: управление контейнерами.

![image](https://github.com/user-attachments/assets/36097e53-6e1e-495b-b8de-b97ae6e7089f)

6. Скриншот показывает успешное завершение установки пакетов, необходимых для работы с Docker. Это означает, что система готова к использованию для контейнеризации приложений.

![image](https://github.com/user-attachments/assets/42907141-144b-4b10-ab06-80728442a826)

7. Запуск Docker и разрешение на его автозапуск.

![image](https://github.com/user-attachments/assets/1f9b55b4-315e-471f-b3ca-1c133a22989d)

8. `COMVER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep 'tag_name' | cut -d\" -f4)`

С помощью API GitHub получаем последнюю версию Docker Compose.

![image](https://github.com/user-attachments/assets/8704fe5e-2904-464b-8033-de1259cacfc6)

9. `sudo curl -L "https://github.com/docker/compose/releases/download/$COMVER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose`
   
Загрузка и установка последней версии Docker. По завершении загрузка выполнена успешно.

![image](https://github.com/user-attachments/assets/f7b00cef-9f27-4760-ad4a-8587d518395c)

10. `sudo chmod +x /usr/bin/docker-compose`

Команда изменяет права доступа к файлу `/usr/bin/docker-compose`, добавляя разрешение на выполнение этого файла. 

`chmod`: команда для изменения прав доступа к файлам и директориям
`+x`: добавляет разрешение на выполнение для всех пользователей 
`/usr/bin/docker-compose`: путь к файлу, права доступа к которому необходимо изменить. В данном случае это исполняемый файл `docker-compose`, расположенный в системной директории `/usr/bin`.

![image](https://github.com/user-attachments/assets/1b56ae8f-e6e5-4b26-a5ff-349417979b6a)

11. `ls -l /usr/bin/docker-compose`

С помощью этой команды видим, что файл стал исполняемым

![image](https://github.com/user-attachments/assets/f8b6570e-0d23-42cd-a94d-a7c795a70007)

12. `docker-compose –version`

Информация о том, какая версия Docker Compose у нас установлена.

![image](https://github.com/user-attachments/assets/dd3f5d12-09f0-41c9-bc8d-5d37ebbe939e)

13.  `git clone https://github.com/skl256/grafana_stack_for_docker.git`

Производим клонирование удаленного репозитория git, расположенного по ссылке.

![image](https://github.com/user-attachments/assets/0f03777d-5fa0-4e90-b62c-a04b0de59f20)

14. `cd grafana_stack_for_docker`

Смена текущей директории на указанную. Переход в директорию **grafana_stack_for_docker**.

![image](https://github.com/user-attachments/assets/7ec8ad7e-7fbc-40dd-af06-980eabc27287)

15. `sudo docker compose up -d` 

Создание и запуск контейнеров в фоновом режиме с помощью конфига из файла docker-compose.yaml.

![image](https://github.com/user-attachments/assets/c172b614-4f27-4ff1-b3ed-a1c683132476)

16. `sudo docker compose stop` 

Происходит остановка запущенных контейнеров, не удаляя их.

![image](https://github.com/user-attachments/assets/3c2a9849-4b6c-475b-bbfe-aa2e6f1718dd)

17. `sudo docker compose down`

Происходит остановка и удаление контейнеров и других элементов, созданных с помощью Docker Compose.

![image](https://github.com/user-attachments/assets/5dedfa96-4f27-4c9b-b462-b6639fa44cf7)

18. . `sudo docker compose ps`

Проверка состояния контейнеров, определенных в файле, с последующим выводом логов их запуска.

![image](https://github.com/user-attachments/assets/52dc2892-e636-4f32-8146-03f3d348e91f)

19.  `git clone https://github.com/caurinnn/college.git `

Клонирование репозитория **college** с GitHub.

![image](https://github.com/user-attachments/assets/2833f940-1923-4937-8579-0b77699dcaad)

20. `pwd`

Осуществляется вывод полного пути текущего каталога.

![image](https://github.com/user-attachments/assets/82c65efc-7a63-4111-beaa-929c74be29f6)

21. `sudo vi docker-compose.yaml`

Открытие файла `docker-compose.yaml` в текстовом редакторе `vi` с правами суперпользователя, что позволяет редактировать его содержимое.

![image](https://github.com/user-attachments/assets/2b38bd5a-541b-4ad4-b8e6-17353a31b57c)

![image](https://github.com/user-attachments/assets/018d83d8-a32c-4e6c-9813-8972dd152194)

22. `sudo vi prometheus.yaml`

Команда для открытия файла `prometheus.yaml` в текстовом редакторе `vi` с правами суперпользователя.

![image](https://github.com/user-attachments/assets/85e195e7-a805-499b-a1e1-0e3f2a79cd2e)

![image](https://github.com/user-attachments/assets/3c5c53cf-40ee-4033-9ee7-fe1ba7a2eec7)

# ***Grafana**

1. `localhost:3000` 

Совершаем переход на сайт, где нужно будет залогиниться.
Данные для входа:
Пользователь: admin
Пароль: admin.

![image](https://github.com/user-attachments/assets/98a0d668-0039-4b29-9a49-b7274d0dea93)

2. Начальный экран (интерфейс) Grafana.

![image](https://github.com/user-attachments/assets/33449e36-c186-42f4-a596-5bf11a0a19fc)

3. `dashboards`.

Переход в дашборды и создание нового.

![image](https://github.com/user-attachments/assets/b3bdd46a-07c0-4047-9884-015116ffda53)

4. Работа с созданным дашбордом и добавление визуализации.

![image](https://github.com/user-attachments/assets/26d35c9a-36ac-4c77-ba67-514350d63116)

5. Выбираем `Prometheus`.

![image](https://github.com/user-attachments/assets/c2899d4a-636d-4afd-bb8d-7b9df9d954e5)

6. Ссылка сервера - `http://prometheus:9090` и базовая аутентификация admin/admin.

![image](https://github.com/user-attachments/assets/7da49f1d-17e5-48d3-97dc-b8f693f95740)

7. Успешное сохранение

![image](https://github.com/user-attachments/assets/19ff18df-d3e9-4b8e-9ed4-82fefcd0e2d7)

8. Импорт dashboard 1860.

![image](https://github.com/user-attachments/assets/01105b09-4498-4eac-9a7c-99e7a09e1fd6)

![image](https://github.com/user-attachments/assets/ee078758-be05-4e2a-a442-486bbe0756e2)

9. Дашборд успешно производит мониторинг метрик.

![image](https://github.com/user-attachments/assets/f00ba0e6-4571-4e43-9ecf-fa0736e34d81)

Викториа метрикс

создаю новую визуализацию. меняю url

![image](https://github.com/user-attachments/assets/1e8d8c28-f645-4556-8cb1-c0181fa4e343)

Ставлю режим код и выставляю параметр OILCOINT_metric1
![image](https://github.com/user-attachments/assets/c2613b77-19e3-4ffd-a94b-80f6ac44afd4)

Ввожу команды в терминал
![image](https://github.com/user-attachments/assets/5e76b25e-66ea-46ff-a02c-5c840dbd672a)

всё ок
![image](https://github.com/user-attachments/assets/fa7dfae6-aa76-4ee2-8a23-aec378249169)

результат
![image](https://github.com/user-attachments/assets/e0d38eec-05c0-427a-ad6d-28927b63c4aa)

и в графане
![image](https://github.com/user-attachments/assets/6edf6648-f3ee-4911-be8a-907fd854b214)
