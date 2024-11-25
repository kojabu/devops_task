


# dev_ops_task

Проект для выполнения тестового задания по DevOps. Включает установку и настройку веб-сервера **Nginx** для отображения страницы на **localhost**.

## Установка Nginx

### Для Ubuntu/Debian:
1. Обновите пакеты:
   ```bash
   sudo apt update
   ```
2. Установите Nginx:
   ```bash
   sudo apt install nginx
   ```
3. Запустите Nginx:
   ```bash
   sudo systemctl start nginx
   ```

### Для macOS:
1. Установите Homebrew (если не установлен):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. Установите Nginx:
   ```bash
   brew install nginx
   ```
3. Запустите Nginx:
   ```bash
   brew services star nginx
   ```

## Конфигурация Nginx

1. Откройте конфигурационный файл:
   - Для Ubuntu: `/etc/nginx/sites-available/default`
   - Для macOS: `/usr/local/etc/nginx/nginx.conf`

2. Убедитесь, что строка с корнем указывает на ваш проект:
   ```nginx
   root /путь/к/проекту;
   index index.html;
   ```

3. Проверьте конфигурацию:
   ```bash
   sudo nginx -t
   ```

4. Перезапустите Nginx:
   ```bash
   sudo systemctl restart nginx
   ```

## Клонирование репозитория

1. Скопируйте HTTPS-ссылку репозитория:
   ```bash
   https://github.com/kojabu/devops_task   
```

2. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/kojabu/devops_task.git
   ```

3. Перейдите в директорию проекта:
   ```bash
   cd dev_ops_task
   ```

4. Поместите ваш проект в директорию, указанную в конфигурации Nginx (например, `/путь/к/проекту`).

5. Перезапустите Nginx:
   ```bash
   sudo systemctl restart nginx
   ```

6. Откройте браузер и перейдите на `http://localhost`. Вы должны увидеть вашу страницу.
## Настройка Docker-контейнера

Этот репозиторий содержит `Dockerfile` для создания контейнера, который запускает статический веб-сайт с использованием NGINX.

### Требования
- Установленный Docker

### Шаги для запуска контейнера

1. **Соберите Docker-образ**:
   ```bash
   docker build -t my_nginx_image .

    Запустите Docker-контейнер:

docker run -d -p 8080:80 --name my_nginx_container my_nginx_image

    Веб-сайт будет доступен по адресу http://localhost:8080.

Остановите контейнер:

docker stop my_nginx_container

Удалите контейнер:

docker rm my_nginx_container

Опционально: Удалите Docker-образ:

docker rmi my_nginx_image
## Контакты

- **Автор**: Abdulla Avdillayev
- **GitHub**: [https://github.com/kojabu/devops_task](https://github.com/kojabu/devops_task)





