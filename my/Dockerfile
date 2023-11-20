# исп. базового образ Ubuntu
FROM ubuntu:latest

# обновление списка пакетов и устновка необходимых инструменты
RUN apt-get update && apt-get install -y \
    x11-apps \    
    xauth \         
    openjdk-11-jre \ 
    && rm -rf /var/lib/apt/lists/*  

# коипрование приложение calc.jar внутрь контейнера
COPY calc.jar /new-app/

# установлние переменной окружения DISPLAY для работы графики
ENV DISPLAY=:0

# команда по умолчанию для запуска приложения calc.jar
CMD ["java", "-jar", "/new-app/calc.jar"]
