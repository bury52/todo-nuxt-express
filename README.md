### run 

```bash
git clone https://github.com/bury52/todo-nuxt-express.git
```
```bash
cd todo-nuxt-express/
```
```bash
git submodule init
```
```bash
git submodule update
```
```bash
docker-compose up -d
```

>api :3300

>nuxt :3000

### deleting from docker
 
> ```bash
> docker ps
> ```
> ```text
> CONTAINER ID   IMAGE                          COMMAND                  CREATED         STATUS         PORTS                                       NAMES
> a9201eef3dd5   todo-nuxt-express-todo-back    "docker-entrypoint.s…"   7 minutes ago   Up 7 minutes   0.0.0.0:3300->3300/tcp, :::3300->3300/tcp   api
> 200b026a56d7   todo-nuxt-express-todo-front   "docker-entrypoint.s…"   7 minutes ago   Up 7 minutes   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp   nuxt
> ```
> ```bash
> docker stop a920 200b
> ```
> ```bash
> docker rm a920 200b
> ```
> -------- If Containers Are Not Working -------- 
> ```bash
> docker ps -a
> ```
> ```text
> CONTAINER ID   IMAGE                          COMMAND                  CREATED         STATUS         PORTS                                       NAMES
> a9201eef3dd5   todo-nuxt-express-todo-back    "docker-entrypoint.s…"   7 minutes ago   Up 7 minutes   0.0.0.0:3300->3300/tcp, :::3300->3300/tcp   api
> 200b026a56d7   todo-nuxt-express-todo-front   "docker-entrypoint.s…"   7 minutes ago   Up 7 minutes   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp   nuxt
> ```
> ```bash
> docker rm a920 200b
> ```
```bash
docker images
```
```text
REPOSITORY                     TAG       IMAGE ID       CREATED             SIZE
todo-nuxt-express-todo-front   latest    d8b342912116   About an hour ago   1.37GB
todo-nuxt-express-todo-back    latest    cff448848c1a   About an hour ago   1.31GB
```
```bash
docker image rm d8b3 cff4
```