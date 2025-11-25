# Clase 1 - Introducción a Containers y Docker

# Aplicación elegida: Apache HTTP Server (httpd)

## Objetivo
En esta práctica se desplegó un servidor web Apache usando Docker, exponiendo el servicio en el puerto 8081 y ejecutándolo en segundo plano.

## Desarrollo

### 1. Ejecutar el container

```bash
docker run -d -p 8081:80 --name mi-apache httpd

```
**Explicación:**

**docker run**
	Ejecuta un nuevo contenedor.
**-d**
	Ejecuta el contenedor en segundo plano (modo detached).
**-p 8081:80*
	Mapea el puerto 80 del contenedor al puerto 8081 de la máquina local**--name mi-apache**
	Asigna un nombre personalizado al contenedor.
**httpd**
	Imagen utilizada (servidor Apache).



**Screenshot:**

![ejecuta contenedor de apache](screenshots/Screenshot1.png)

**Explicación:** 





Este comando crea y ejecuta un container con nginx en segundo plano (-d), mapeando el puerto 8080 de mi máquina al puerto 80 del container.

**Salida:**
\`\`\`
a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6
\`\`\`

### 2. Verificar que está corriendo

\`\`\`bash
docker ps
\`\`\`

**Screenshot:**

![Container corriendo](screenshots/docker-ps.png)

### 3. Acceder desde el navegador

Accedí a `http://localhost:8080` y obtuve:

![Nginx funcionando](screenshots/nginx-browser.png)




## Conclusiones

Aprendí a desplegar aplicaciones rápidamente usando Docker.

Entendí cómo funcionan los mapeos de puertos y la ejecución en segundo plano.

Me familiaricé con comandos básicos como docker run, docker ps, docker logs, docker stop, docker rm.

La única dificultad fue la configuración inicial de Docker, que resolví revisando repos, limpiando configuraciones y arrancando el daemon correctamente.

