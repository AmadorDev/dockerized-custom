
# 📌 Gestión de Contenedores
- docker ps                      # Listar contenedores en ejecución
- docker ps -a                   # Listar todos los contenedores (incluidos detenidos)
- docker start nombre_contenedor  # Iniciar un contenedor detenido
- docker stop nombre_contenedor   # Detener un contenedor
- docker restart nombre_contenedor  # Reiniciar un contenedor
- docker rm nombre_contenedor     # Eliminar un contenedor detenido
- docker rm $(docker ps -aq)      # Eliminar todos los contenedores detenidos


# 📌 Gestión de Imágenes
- docker images                   # Listar imágenes disponibles
- docker rmi nombre_imagen        # Eliminar una imagen
- docker rmi $(docker images -q)  # Eliminar todas las imágenes
- docker build -t nombre_imagen .  # Construir una imagen desde un Dockerfile


# 📌 Gestión de Docker Compose
- docker compose up -d --build         # Construir y levantar servicios en segundo plano
- docker compose down -v               # Detener y eliminar volúmenes
- docker compose up -d --build node    # Construir y levantar solo el servicio "node"
- docker compose up -d --no-deps --build mysql  # Reconstruir MySQL sin dependencias
- docker compose logs -f               # Ver logs de todos los servicios
- docker compose logs -f node_app       # Ver logs de un servicio específico
- docker compose ps                     # Listar contenedores administrados por Compose
- docker compose config                 # Ver configuración actual de Docker Compose


# 📌 Acceder a un Contenedor en Ejecución
- docker exec -it nombre_contenedor sh   # Ingresar al contenedor con shell
- docker exec -it nombre_contenedor bash # Ingresar con bash si está disponible
- docker logs -f nombre_contenedor       # Seguir logs en tiempo real


# 📌 Gestión de Redes
- docker network ls             # Listar redes de Docker
- docker network inspect nombre_red  # Ver detalles de una red
- docker network rm nombre_red  # Eliminar una red


# 📌 Gestión de Volúmenes
- docker system df                      # Ver tamaño de almacenamiento utilizado
- docker volume ls                       # Listar volúmenes
- docker volume inspect nombre_volumen   # Inspeccionar un volumen
- docker volume rm nombre_volumen        # Eliminar un volumen específico
- docker volume prune                     # Eliminar volúmenes no utilizados
- docker volume rm $(docker volume ls -q) # Eliminar todos los volúmenes


# 📌 Comandos Útiles de Depuración
- curl -i http://node:3001/socket.io/?EIO=4&transport=polling  # Probar conexión a Socket.IO
- docker stats            # Ver consumo de CPU/Memoria en tiempo real
- docker top nombre_contenedor  # Ver procesos en ejecución dentro de un contenedor
- docker inspect nombre_contenedor  # Ver detalles completos del contenedor




