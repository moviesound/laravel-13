### Инструкция по Установке: 
1. Запустить контейнер командой:

       docker compose up -d

2. Зайти в терминал контейнера "app" через services в Phpstorm
или командой в терминале:

       docker exec -it app bash

3. Вы окажетесь в папке /var/www. Необходимо в 
контейнере перейти в каталог app командой 

       cd app

4. Установить ларавел командой:

       composer create-project "laravel/laravel:^13" .

5. Разрешить писать файлы в папку bootstrap/cache:

       chown -R www-data:www-data storage bootstrap/cache
       chmod -R 775 storage bootstrap/cache
