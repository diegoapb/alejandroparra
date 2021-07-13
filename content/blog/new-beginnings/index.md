---
title: Introduction Django Project
date: "2015-05-28T22:40:32.169Z"
description: This is a little project, based on instagram and devolped in django.
---
# Cimientos

## IMPORTANTE

## Resumen Cimientos

[Django Avanzado - Slides P1.pdf](Cimientos%204865b7486a354b89b1379cedbb49ff74/Django_Avanzado_-_Slides_P1.pdf)

.

Comandos iniciales

- Descargar Codigo

> `git clone https://github.com/pablotrinidad/cride-platzi.git`

- exec

> `cd cride`
`docker-compose -f local.yml build`

## 1 Introduccion

**Palabras Clave:**

- Historias de usuario
- Funcionalidades
- Temas iniciales

**Resumen:** 

**Documentacion:**

**Notas:**

- 5.00 Explicacion del proyecto final
- 5.48 ¿Como funciona? Historias Epicas de la aplicacion
- 6.40 Modelo de usuarios
- 7.37 Modelo de "Circulos" grupos de rides
- 8.20 Modelo de "Rides" o viajes compartidos.
- 9.00 Funcionalidades de Usuarios5
- 9.17 Funcionalidades de Circulos
- 9.40 Funcionalidades de Rides
- 9.57 Funcionalidades extras
    - Administracion de admins
    - Despliege en aws
- 11.14 Contenido

---

---

## [2 Arquitectura de una aplicación](https://platzi.com/clases/1461-django-avanzado/17209-arquitectura-de-una-aplicacion/)

**Palabras Clave:**

El **Backend** consiste en:

- Servidor
- Aplicación
- Base de Datos

- APIs
    - SOPA
    - REST
    - GraphQL x Facebook

**Resumen:** El objetivo de este curso es convertirte en un Backend profesional que usa Django como su herramienta profesional.

Un Backend developer es un diseñador, su trabajo consiste un 90% en leer, diseñar, analizar y planear. Un 10% en programar. Nuestro trabajo más importante es el diseño del sistema y las decisiones tomadas son más costosas y más difíciles de cambiar.

Web Services es la manera en que se implementan las arquitecturas orientadas a servicios, se crean bloques que son accesibles a través de la web, son independientes del lenguaje de programación.

**Documentacion:**

Lecturas Recomendadas:

[Web Tools APIs | USPS](https://www.usps.com/business/web-tools-apis/welcome.htm) Servicio postal de estados unidos

[Graph API - Documentation - Facebook for Developers](https://developers.facebook.com/docs/graph-api/) - Hablan de las buenas practicas para crear una graphql api

[GitHub GraphQL API v4 | GitHub Developer Guide](https://developer.github.com/v4/) - 

[GitHub - kamranahmedse/developer-roadmap: Roadmap to becoming a web developer in 2019](https://github.com/kamranahmedse/developer-roadmap)

[2.- Arquitectura de una aplicación - Google Slides](https://docs.google.com/presentation/d/1HlT7niPOISnHjk6ldbmCvZdiOeKqlzLNxfsGY5499_E/edit?usp=sharing)

**Notas:**

- 1.32 Roadmap → Carrera de un FullStack Developer
- 5.00 Arquitectura
    - Monolitica: Fuertemente acoplada a la base de datos y cualquier otro servicio que use, Todo esta **en un solo servidor.**
    - Distribuida: Los servicios estan distribuidos en la red, como la base de datos en otro lugar
    - Hibrida: el backend esta haciendo rendering en el frontend, el cliente se comunica directamente con el Bakend.
    - Orientada a Servicios:
        - Autocontenida
        - Caja negra
        - Representa una actividad de negocio especifica
- Estandares de Arquitectura SOA
    - SOAP → En desuso antiguo
    - RESTfulHTTP → Esta enfocada en el HTTP, Es en la que profundizaremos
    - GraphQL → Esta orientada por facebook, se enfoca en trabajar como un lenguaje de consulta para las APIs
    - Mas Informacion
        - SOAP ([https://www.usps.com/business/web-tools-apis/welcome.htm](https://www.usps.com/business/web-tools-apis/welcome.htm))
        - RESTful HTTP ([https://developers.facebook.com/docs/graph-api/](https://developers.facebook.com/docs/graph-api/))
        - GraphQL ([https://developer.github.com/v4/](https://developer.github.com/v4/))

---

---

## [3 The Twelve-Factor App](https://platzi.com/clases/1461-django-avanzado/17140-the-tlwelve-factor-app/)

**Palabras Clave:**

- SAAS
- Principios basicos
- 

- API
- HTTP
- Metodologia

**Resumen:** Algunos principios de Twelve Factor app
En el proyecto vamos a construir una API en la teoria estas aplicaciones construidas con apis son nombradas SAAS (Software as a Services) y **The Twelve-Factor App** Es una metodologia de desarrolla para aplicaciones SAAS. Esta metodologia ha sido formada por la contribuciones de muchas personas, mayoritariamente desarrolladores de Heroku.

**Documentacion:**

- [The Twelve-Factor App](https://12factor.net/) - Pagina oficial de la metodologia de desarrollo de SAAS

    Este documento sintetiza toda nuestra experiencia y observaciones sobre una amplia variedad de aplicaciones de software como servicio en la naturaleza. Es una triangulación de prácticas ideales para el desarrollo de aplicaciones, prestando especial atención a la dinámica del crecimiento orgánico de una aplicación a lo largo del tiempo, la dinámica de colaboración entre los desarrolladores que trabajan en el código base de la aplicación y evitando el costo de la erosión del software .

**Notas:**

- 0.30 Principios
    - Formas **declarativas** de configuracion: Minimizamos el tiempo que le toma a un desarrollador correr nuestro proyecto
    - Un **contrato claro** con el OS: Ofrecer maxima portabilidad.
    - Listas para **lanzar. El developer tiene que poder lanzar la aplicacion**
    - Minimizar la **diferencia** entre **entornos:** Generar un pipeland de continues deliver, consecuente a esto aumentamos la agilidad.
    - Facil de **escalar:** Evitaremos cambiar la arquitectura.
- 1.54 Los 12 Factores:

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_12.30.42_p._m..png](Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_12.30.42_p._m..png)

    [I. Código base (Codebase)](https://12factor.net/es/codebase)

    Un código base sobre el que hacer el control de versiones y multiples despliegues. 

    Solo hay un git con el codigo base.

    [II. Dependencias](https://12factor.net/es/dependencies)

    Declarar y aislar explícitamente las dependencias

    como el `package.json` de node.js.

    y **aislamos** usando un virtual env o docker

    [III. Configuraciones](https://12factor.net/es/config)

    Guardar la configuración en el entorno.

    Cada entorno debe llevar su configuracion, llaves usuarios etc

    [IV. Backing services](https://12factor.net/es/backing-services)

    Tratar a los “backing services” como recursos conectables.

    EJEMPLO :Servicios de emails → Debe ser muy facil de cambiar de servicio.

    [V. Construir, desplegar, ejecutar](https://12factor.net/es/build-release-run)

    Separar completamente la etapa de construcción de la etapa de ejecución.

    Build → es la parte donde compilamos nuestro codigo

    Relase→ Es la parte donde incluimos las variables de entorno dentro de nuestro paquete.

    Run → Donde corremos la aplicacion en el entorno que se va a ejecutar. 

    Es muy importante mantener esta etapas totalmente separadas, no escribir codigo de una etapa en otra.

    [VI. Procesos](https://12factor.net/es/processes)

    Ejecutar la aplicación como uno o más procesos sin estado.

    No requerimos el almacenamiento de estados en memoria, de ser asi debemos almacenarlo en el backend

    Procesos **Stateless**

    [VII. Asignación de puertos](https://12factor.net/es/port-binding)

    Publicar servicios mediante asignación de puertos.

    Se le debe asignar un puerto por el que la aplicacion escuchara las peticiones

    [VIII. Concurrencia](https://12factor.net/es/concurrency)

    Escalar mediante el modelo de procesos.

    Podemos escalar un solo proceso en varias cargas usando hilos para distribuir mejor la carga.

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/process-types.png](Cimientos%204865b7486a354b89b1379cedbb49ff74/process-types.png)

    [IX. Desechabilidad](https://12factor.net/es/disposability)

    Hacer el sistema más robusto intentando conseguir inicios rápidos y finalizaciones seguras.

    Los procesos pueden iniciarse o finalizarse en el momento que sea necesario. Esto permite un escalado rápido y flexible.

    [X. Paridad en desarrollo y producción](https://12factor.net/es/dev-prod-parity)

    Mantener desarrollo, preproducción y producción tan parecidos como sea posible.

    Reduccion de tiempos en deploys.

    [XI. Historiales](https://12factor.net/es/logs)

    Tratar los historiales como una transmisión de eventos.

    Nos permiten testear el comportamiento de la aplicacion durante su ejecucion.
