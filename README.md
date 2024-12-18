# Challenge Técnico: Junior en Soporte IT

## Objetivo General

Evaluar habilidades prácticas en la configuración y administración de entornos virtualizados, Active Directory, servidores web, bases de datos y redes.

**Nota importante:** Si bien el objetivo del challenge es completar todos los puntos descritos, **lo que estamos evaluando es la manera en que resuelves los problemas y enfrentas los desafíos técnicos.**

---

## Detalles del Challenge

### Plazo de Entrega
Tienes **1 semana** desde el momento en que recibas este desafío para completarlo.

### Entrega Final
Para entregar el challenge, debes:

1. Crear un **repositorio público** en GitHub.
2. Documentar el proceso completo en el archivo `README.md` de tu repositorio, incluyendo:
   - Qué hiciste, cómo lo hiciste y para qué.
   - Capturas de pantalla de cada paso realizado.
   - Descripciones claras y organizadas de cada sección del trabajo.
3. Cada desafío debe estar organizado en su propia carpeta dentro del repositorio, con todos los archivos relevantes.

---

## Tareas

### Tarea 1: Configuración Inicial de una Infraestructura Básica

1. **Crear una máquina virtual (VM):**  
   Utilizando el virtualizador de tu preferencia (VirtualBox, VMware, Hyper-V, etc.), instala **Windows Server 2019**.
   
2. **Configurar un Active Directory (AD):**  
   - Promocionar el servidor a controlador de dominio.  
   - Crear un dominio, por ejemplo: `empresa.local`.  

3. **Gestión de usuarios en el AD:**  
   - Crear tres tipos de usuarios con roles y permisos específicos:  
     - **Usuario Administrador:** Permisos de administración total sobre el dominio.  
     - **Usuario Técnico:** Permisos limitados para gestionar recursos específicos (como crear grupos o modificar usuarios).  
     - **Usuario Estándar:** Permisos básicos de uso (inicio de sesión y acceso limitado).  

4. **Crear y unir un workstation:**  
   - Crear una nueva VM con Windows 10 o Windows 11 como estación de trabajo.  
   - Unir la estación de trabajo al dominio configurado en el AD.  

5. **Configurar y levantar un sitio web estático:**  
   - Instalar y configurar **IIS** en el servidor.  
   - Crear un sitio web que muestre la página estática "Hola Mundo".  
   - Configurar el sitio para que sea accesible desde la **LAN**.  

---

### Tarea 2: Configuración de SQL Server y Base de Datos

1. **Instalar SQL Server:**  
   - Instalar y configurar **SQL Server** en la VM con Windows Server 2019.  
   - Habilitar el inicio de sesión con el usuario `sa`.  

2. **Crear una base de datos con relaciones:**  
   Diseñar una base de datos que represente un pequeño videojuego de rol (RPG). Las tablas deben incluir datos ficticios, relaciones lógicas, y pueden ser las siguientes:  
   - **Jugadores:** Información básica de los jugadores (ID, Nombre, Nivel).  
   - **Personajes:** Detalles de los personajes (ID, Nombre, Clase, Nivel, ID del jugador).  
   - **Habilidades:** Habilidades disponibles en el juego (ID, Nombre, Tipo, Nivel requerido).  
   - **Equipamiento:** Equipamiento que pueden usar los personajes (ID, Tipo, Bonificación, Nivel requerido, ID del personaje).  

3. **Crear un Stored Procedure (SP):**  
   - Desarrollar un SP para realizar una acción sobre las tablas. Por ejemplo:  
     - Subir de nivel a un personaje, incrementando su nivel y actualizando el nivel de las habilidades o equipamiento asociado.  
     - Validar los cambios en las tablas mediante el SP.  

---

### Tarea 3: Interconexión y Gestión Avanzada

1. **Crear una nueva VM:**  
   - Configurar una nueva VM con **Windows Server 2022**.  
   - Unirla al mismo segmento de red que la primera VM.  
   - Unir la nueva VM al dominio configurado en el AD del primer servidor.  

2. **Acceso al sitio web:**  
   - Desde la VM con Windows Server 2022, acceder al sitio estático "Hola Mundo" alojado en la VM con Windows Server 2019.  

3. **Carpeta compartida y permisos:**  
   - Crear una carpeta compartida en la VM con Windows Server 2022.  
   - Configurar permisos diferenciados para los tres usuarios creados en el AD:  
     - **Administrador:** Permiso total (lectura, escritura y eliminación).  
     - **Técnico:** Permiso de lectura y escritura, sin posibilidad de eliminar archivos.  
     - **Estándar:** Permiso de solo lectura.  

4. **Simulación de permisos:**  
   - Desde la VM con Windows Server 2019, conectarse a la carpeta compartida utilizando los tres usuarios y simular sus permisos sobre un archivo.  
   - Documentar el comportamiento esperado de cada usuario según sus permisos.  

---

## Criterios de Evaluación

- Capacidad para seguir instrucciones detalladas.  
- Resolución de problemas técnicos de configuración.  
- Documentación clara y detallada de los pasos realizados.  
- Funcionamiento correcto de cada tarea según los objetivos planteados.  
- Organización y claridad en el repositorio público de GitHub.  

---

## Nota Final

¡Éxitos en este desafío! Recuerda que lo más importante no es solo completar cada tarea, sino demostrar tu capacidad para resolver problemas y documentar adecuadamente el proceso. Si tienes alguna duda, no dudes en aclararla con quien te envió este challenge.

