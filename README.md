# Laboratorio 02
Hoy utilizaremos docker compose para poder desplegar su trabajo. Servicio web y una
base de datos
## Stack
API
- Minimal API
- Debe retornar un mensaje incluyendo mi nombre
- Docker
- docker run -d --rm -p 3000:3000 nmatsui/hello-world-api

BD
- PostgreSQL
- $ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d
postgres
# Indicaciones
## Comandos
```bash
docker compose up -d
```
## Configuración por entorno
```
MESSAGE=<Colocar nombre>
```
# Creditos
- Angel Gabriel Culquichicon Vasquez

## Tipos de Redes en Docker

- bridge: Es la red por defecto. Crea un puente privado dentro de tu máquina para que los contenedores puedan hablar entre ellos usando sus nombres o IPs.
- host: Le quita el aislamiento al contenedor y hace que use directamente la red de tu computadora.
- none: Deja al contenedor totalmente aislado, sin ningún tipo de conexión a internet o a otros contenedores.
- overlay: Sirve para conectar contenedores que están en distintas máquinas físicas o servidores.
- macvlan: Le da una dirección MAC propia al contenedor para que tu router lo detecte como si fuera una computadora física real.

## Tipos de Volúmenes en Docker

- Volúmenes (Volumes): Es la forma oficial y recomendada. Docker guarda y maneja la información en una carpeta propia dentro del sistema sin que tengamos que preocuparnos por la ruta exacta.
- Bind Mounts: Es cuando vinculas una carpeta exacta de tu computadora con una del contenedor. Lo que cambias afuera se refleja inmediatamente adentro.
- tmpfs Mounts: Guarda los datos temporalmente en la memoria RAM. En cuanto apagas el contenedor, todo lo que estaba ahí se borra.

## Comandos para manejar el proyecto

- docker compose up -d --build
- docker compose ps
- docker compose logs -f
- docker compose down

# evidencias
