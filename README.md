# 📌 Propuesta Proyecto de Grado – App de Alertas de Transporte Público

## 👤 Autor
- **Nombre:** Mateo hernandez diaz   
- **Carrera:** Tecnología en Desarrollo de Software  
- **Universidad:** Universidad Católica Luis Amigó  

---

## 🏷️ Nombre del proyecto
**SafeTransit – Alertas de Transporte Público en Tiempo Real**

---

## 🧩 Descripción del Problema
En muchas ciudades, los usuarios del transporte público no saben **cuándo pasará el bus**, si **ya pasó**, o si **viene lleno**.  
Esto genera **pérdida de tiempo**, **incertidumbre** y malas decisiones de ruta.

---

## 💡 Solución Propuesta
Desarrollar una **aplicación web/móvil** que muestre información confiable del transporte **sin depender de reportes del usuario**:

- 🚍 **Posición de buses en tiempo real** usando datos de GPS de empresas/autoridades (cuando exista API o datos abiertos).  
- ⏱️ **Tiempo estimado de llegada (ETA)** a cada parada mediante cálculo de distancia y velocidad histórica.  
- ⭐ **Reportes opcionales de ocupación** (vacío/medio/lleno). La app funciona igual sin ellos.  
- 🔔 **Alertas** si un bus presenta retrasos inusuales o desvíos.  
- 📍 **Paradas favoritas** y notificaciones cuando el bus esté cerca.  

> Primera versión: **mapa + ETA**; reportes ciudadanos como plus.  

---

## 🛠️ Tecnologías a Utilizar
- **Frontend móvil/web:** Flutter o React Native / React  
- **Mapas:** Google Maps Platform o Mapbox  
- **Backend:** Node.js (Express) o Python (FastAPI/Django)  
- **Base de datos:** PostgreSQL (PostGIS) o Firebase  
- **Tiempo real:** WebSockets (Socket.IO) o Firebase Realtime DB  
- **Control de Versiones:** Git & GitHub   


---

## 🔒 Privacidad y Fuentes de Datos
- Priorizar **datos oficiales** (APIs de empresas o datos abiertos).  
- Reportes ciudadanos **opcionales** y anónimos.  
- Cumplir Términos de Uso de mapas/APIs.

---

## Diagrama de Flujo
![Diagrama de Flujo](imagenes/bustracker_diagrama.png)

## Diagrama de ishikawa
![Diagrama de ishikawa](imagenes/Beige_and_Brown_Simple_Modern_Fishbone_Diagram_Graph.png)


---

# Historias de usuario
1. Registro de denuncias

Como ciudadano registrado, quiero registrar una denuncia sobre una situación de inseguridad en el transporte público, para que la autoridad competente pueda tomar medidas.

Criterios de aceptación:

- El formulario solicita ubicación, descripción del hecho y opción para adjuntar evidencia (foto/video).

- Validación de que todos los campos obligatorios estén diligenciados.

- La denuncia se guarda en la base de datos con fecha y hora.

- Se muestra mensaje de confirmación de registro exitoso.

---

2. Consulta de denuncias propias

Como ciudadano registrado, quiero consultar el historial de mis denuncias, para poder dar seguimiento a su estado.

Criterios de aceptación:

- El sistema muestra una lista de denuncias asociadas al usuario.

- Cada denuncia debe mostrar fecha, descripción y estado (pendiente, en revisión, resuelta).

- Debe existir opción de filtrar denuncias por estado o fecha.

- Acceso restringido solo al usuario propietario de la cuenta.

---

3. Visualización de mapa de incidentes

Como ciudadano, quiero visualizar en un mapa las zonas con más reportes de inseguridad, para evitar rutas peligrosas.

Criterios de aceptación:

- El mapa muestra marcadores en las ubicaciones reportadas.

- Los marcadores se agrupan por zonas con alta concentración de incidentes.

- Opción de filtrar por tipo de incidente o fecha.

- El mapa se actualiza automáticamente con las nuevas denuncias.

---

4. Notificaciones sobre zonas de riesgo

Como ciudadano, quiero recibir notificaciones sobre nuevas denuncias en mi zona habitual, para estar alerta en mis recorridos.

Criterios de aceptación:

- El sistema permite al usuario registrar zonas de interés (ej. barrio, estación).

- Notificación automática cuando se registre una denuncia en la zona configurada.

- Notificación enviada por correo electrónico o dentro de la app.

- Opción para activar o desactivar notificaciones.

---

5. Panel de administración (autoridad)

Como administrador, quiero acceder a un panel donde pueda visualizar todas las denuncias recibidas, para gestionar y darles respuesta.

Criterios de aceptación:

- El panel muestra lista de denuncias con opción de filtrado (fecha, zona, tipo de incidente).

- Cada denuncia debe tener opciones de actualizar su estado (pendiente, en revisión, resuelta).

- Acceso restringido a usuarios con rol de administrador.

- Los cambios en el estado de la denuncia se reflejan en el perfil del ciudadano denunciante.

---

6. Recuperación de contraseña

Como ciudadano registrado, quiero recuperar mi contraseña en caso de olvido, para poder acceder nuevamente a la plataforma.

Criterios de aceptación:

- El formulario de recuperación solicita el correo electrónico del usuario.

- Se valida que el correo exista en la base de datos.

- El sistema envía un enlace seguro de restablecimiento al correo registrado.

- El usuario puede definir una nueva contraseña cumpliendo las políticas de seguridad (mínimo 8 caracteres, letras y números).

- Mensaje de confirmación al finalizar el proceso.

---

7. Calificación de zonas seguras/inseguras

Como ciudadano, quiero calificar las zonas o rutas que frecuento como seguras o inseguras, para contribuir a la base de datos de la comunidad.

Criterios de aceptación:

- El sistema permite seleccionar una zona o ruta en el mapa.

- Se ofrece opción de calificación rápida (ej. 👍 Seguro / 👎 Inseguro).

- La calificación queda registrada con fecha y usuario.

- El promedio de calificaciones se refleja en el mapa general de la aplicación.

- Evitar duplicados por parte del mismo usuario en la misma ruta (una calificación por persona).



