# Прокидывание переменных в статику react

```bash
# для сборки через мультистейдж
docker build -t my-app:1 --no-cache -f Dockerfile-multistage .

# просто прикидывание результата локальной сборки (предварительно закоментировать dist в .dockerignore)
docker build -t my-app-only-nginx:1 --no-cahce .

# запуск контейнера с переменными
docker run -p 3000:80 -e changeme_VAR1="alpha" -e changeme_VAR2="beta"  my-app:1

docker run -p 3000:80 -e changeme_VAR1="alpha" -e changeme_VAR2="beta"  my-app-only-nginx:1

```

Результат смотрим http://127.0.0.1:3000
