# HW1_IT-servises
## Github information
Servers | Stars | Watching | Forks 
:---- | :-----: | :--------: | -----:
Caddy | 52.8k | 826 | 3.8k |
Nginx | 20k | 975 | 6.5k |
Apache | 23k | 946 | 12.9k |

## Top servers (2020, Yandex, Google)
![image](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/60129d87-e107-4af1-a365-c20467a8aa71) 
https://timeweb.com/ru/community/articles/nginx-apache-cloudflare-statistika-i-obzor-populyarnyh-veb-serverov
## Top servers (2024, Yandex)     
Top | Name                               
:--- | ----:
1 | Apache HTTP Server |
2 | Nginx Web Server |
3 | Lighttpd Web Server |
4 | Apache Tomcat |
5 | Caddy Web Server |
6 | OpenLiteSpeed Web Server |
7 | Hiawatha Web Server |
8 | NodeJS |

https://www.tecmint.com/best-open-source-web-servers/

## Top servers (2024, Google)
Top | Name
:--- | ----:
1 | Apache - 39.94% |
2 | Nginx - 28.68% |
3 | IIS - 10.07% |
4 | LiteSpeed - 2.79% |
5 | Apache Traffic Server - 0.51% |
6 | OpenGSE - 0.42% |
7 | Phusion Passenger - 0.35% |
8 | Apache Tomcat - 0.15% |
9 | Netlify - 0.13% |
10 | Tengine - 0.11% |

https://hostadvice.com/marketshare/server/

## Performance (Caddy, Nginx, Apache)
![image](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/3872f561-eb6b-4d64-83e7-6c71dbcddab4)

https://blog.logrocket.com/comparing-best-web-servers-caddy-apache-nginx/

![image](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/134c872f-70d2-4ec5-8a87-1aabe3eb8975)

https://operavps.com/blog/caddy-vs-nginx-vs-apache/

## Experimenting with server fault-tolerance
![10 клиентов рисунок](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/cbd97be9-dacd-4a99-8c5f-6ed62d8e469a)
![200 клиентов](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/ad5543c4-f4a3-4b8c-b597-2a2ffc8a1d94)
![500 клиентов](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/63c1b0a4-3dc9-4d2f-a569-45d95147066e)
![1000 клиентов](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/06ab95d3-14bc-4fd1-9f12-83e2ef549454)
![10000 клиентов](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/e17b2d54-7219-45e0-abe1-fc39c8d35a6f)

Выводы эксперимента: 
1) Nginx выйдет из строя из-за отказа или прерывания соединений, Caddy выйдет из строя из-за замедления работы всего. Одно лучше другого? Для определенных вариантов использования - почти наверняка. Некоторым людям захочется быстрого отказа, в то время как другие захотят продолжать принимать подключения любой ценой.
2) Caddy оплачивает сбор мусора, но это не подавляющая стоимость (по крайней мере, при “нормальном” уровне трафика). Nginx использует почти не требующий усилий объем памяти. Caddy достигла максимума в объеме почти 160 МБ реальной памяти, выделенной для тестов без взлома, что может быть значительным, а может и не быть значительным, в зависимости от того, какой объем общей памяти доступен операционной системе. Еще неизвестно, какой конкретный путь кода вызывает все это malloc/free, но мои тесты, похоже, указывают на какой-либо механизм, лежащий в основе reverse_proxy.
3) Конфигурация Caddy по умолчанию хороша. Мы разблокировали все наши ядра и задействовали все доступные ресурсы без каких-либо утечек памяти. Напомним, что мои конфигурации Caddy “по умолчанию” и “оптимизированная” идентичны. По умолчанию Nginx ограничен одним ядром (вы можете узнать об этом из документации, но мы наблюдали это непосредственно в отношении Caddy).

https://blog.tjll.net/reverse-proxy-hot-dog-eating-contest-caddy-vs-nginx/

## Google Trends
![Servers](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/a0d1e939-fb0c-488a-9b59-eb8f1d774ab7)
### Динамика по всему миру за последние 5 лет
![Динамика по всему миру за последние 5 лет](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/f18a68c7-d9f6-4dec-b1b8-7c4ef70d76c7)
### Динамика по всему миру за последний год
![Динамика по всему миру за последний год](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/d2e5b4a0-3fcb-4366-93f2-b8cd21dc777d)
### Динамика по России за последние 5 лет
![Динамика по России (5 лет)](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/25eaecad-b4b4-40d6-ab19-5072bc7f2f7c)
### Динамика по России за последний год
![Динамика по России (год)](https://github.com/valeevartur/HW1_IT-servises/assets/163173033/c8615c46-139e-4b29-8478-3e9cc510de13)

## Phind
Сравнивая Caddy, Nginx, и Apache, можно выделить следующие ключевые аспекты:
Caddy:
Прост в использовании и настройке благодаря автоматической поддержке HTTPS и минимальным конфигурационным файлам.
Поддерживает TLS 1.3, что является новейшим стандартом безопасности транспорта.
Хотя Caddy показывает конкурентоспособную производительность с Apache, он немного отстает от Nginx в плане обработки запросов в секунду и стабильности при высокой нагрузке 1.
Nginx:
Известен своей высокой производительностью и масштабируемостью, благодаря асинхронной, событийно-ориентированной и неблокирующей архитектуре.
Использует модель с несколькими процессами, что позволяет поддерживать тысячи одновременных сетевых соединений на каждый рабочий процесс.
Часто используется для оптимизации производительности и является выбором для более чем 40% из 10 000 самых популярных сайтов 1.
Apache:
Основан на модульной архитектуре, что позволяет гибко настраивать сервер для различных задач, от обслуживания динамического контента до работы в качестве балансировщика нагрузки.
Поддерживает различные модули Multi-Processing Modules (MPM), такие как mpm_prefork, mpm_worker, и mpm_event, что делает его подходящим для широкого спектра сценариев использования.
Хотя Apache может быть более настраиваемым, его производительность может ухудшаться при высокой нагрузке, особенно при использовании mpm_prefork 2.
Выбор лучшего веб-сервера зависит от конкретных требований к проекту. Если важно максимальное количество статического контента и высокая производительность, Nginx может быть лучшим выбором. Для гибкости и настройки, особенно в контексте динамического контента и сложных сценариев, Apache может быть предпочтительнее. Caddy представляет собой хороший выбор для тех, кто ценит простоту и безопасность, особенно в контексте автоматического обновления сертификатов SSL/TLS.
Важно отметить, что выбор веб-сервера также может зависеть от предпочтений команды разработки и специфики проекта. В некоторых случаях, комбинирование двух или более веб-серверов может быть оптимальным решением для достижения желаемых результатов
