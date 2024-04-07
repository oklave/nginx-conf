Defend against attaks

#СДЕЛАТЬ РЕЗЕРВНУЮ КОПИЮ файла конфигурации

1. Обновить ngingx
    sudo apt update 
    sudo apt upgrade nginx

2. Проверить конфигурацию
    sudo nginx -t

3. Использовать готовую конфигурацию
    !!!!!

4. Внедрить безопасные заголовки


5. Контроль доступа

6. Отключить Directory Listing
    autoindex off

7. Alias Traversal Protection


8. Перенаправление с http на https
    listen 80;
    server-name site-name.com;
    return 301 https://$host$request_uri;

9. Конфигурация SSL
    listen 443 ssl;
    server-name site-name.com;
    ssl_certificate /path-to/certificate.crt;
    ssl_certificate_key /path-to/private.key;

10. Rate Limiting
    limit_zone $binary_remote_addr zone=one:10m rate=1r/s;
    server {
        location / {
            limit_zone=one burst=5;
            ...
        }
    }

11. Ограничение соединений
    events {
    worker_connections 1024;
}

12. Своя страница с ошибкой 
    error_page 404 /404.html;

13. Использования архивации
    gzip on;
    gzip_types text/plain text/css application/json application/javascript;


14. Кэширование
    location ~* \.(jpg|jpeg|png|gif|ico|css|js)$ {
        expires 7d;
    }

15. Поддержка HTTP2
    listen 443 ssl http2;

16. Безопасная настройка доступа к файлам
    chmod 644 /path-to/file

17. Использование ngfw

18. Мониторинг и логирование 
    access_log /var/log/nginx/access.log;
    error_log /var/log/nginx/error.log;

19. ssh hardering
    nano /etc/ssh/sshd_config

20. Настройка firewall
    sudo ufw allow 80
    sudo ufw allow 443
    sudo ufw enable

21. 2-х факторная аутентификация

22. Регулярные backups

23. Запретить скрытые файлы
    location ~ /\. {
    deny all;
    }

24. Белый список адресов
    allow 192.168.1.1;
    deny all;

25. Отключение неиспользованных модулей

26. Use Trailing Slash in Alias Directives

27. Regular Expression Matching:

28. Implement Strict Location Paths

