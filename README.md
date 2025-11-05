# Validación y Verificación del Proyecto SafeTransit

##  Objetivo General

Garantizar que la aplicación **SafeTransit** cumpla con los requerimientos funcionales y no funcionales, asegurando la confiabilidad, usabilidad y precisión del sistema antes, durante y después de su desarrollo.

---

## 1. Validación

La validación se enfoca en comprobar que el sistema cumple con las necesidades reales del usuario final y que la solución propuesta resuelve efectivamente el problema identificado.

### 1.1 Métodos de Validación

| Método | Descripción | Responsable |
|--------|--------------|-------------|
| Entrevistas a usuarios | Reuniones con ciudadanos y conductores para validar si las funciones (mapa, alertas, denuncias) satisfacen sus necesidades de información y seguridad. | Equipo de análisis |
| Encuestas digitales | Formularios en línea para conocer la percepción sobre los problemas de transporte (incertidumbre, retrasos, inseguridad). | Investigador principal |
| Prototipado temprano (mockups) | Presentación de interfaces simuladas de la app a usuarios para obtener retroalimentación sobre usabilidad y diseño. | Equipo UX/UI |
| Revisión de requerimientos | Validación conjunta entre desarrolladores, usuarios y autoridades para confirmar que los requerimientos son completos y coherentes. | Líder técnico |

### 1.2 Resultados Esperados

- Los usuarios confirman que la app resuelve un problema real.  
- Se identifican posibles mejoras antes del desarrollo (alertas más específicas, diseño de mapas, tipos de incidentes, etc.).  
- Los requerimientos funcionales quedan aprobados y validados antes de programar.

---

## 2. Verificación

### 2.1 Métodos de Verificación

| Método | Descripción | Etapa |
|--------|--------------|-------|
| Pruebas unitarias | Verificar que cada módulo (registro, denuncias, mapa, alertas) funcione correctamente por separado. | Desarrollo |
| Pruebas de integración | Confirmar que los módulos se comuniquen adecuadamente entre frontend, backend y base de datos. | Desarrollo |
| Pruebas funcionales | Verificar que las funciones coincidan con los casos de uso definidos. | Testing |
| Pruebas de usabilidad | Evaluar facilidad de uso, claridad de interfaz y tiempo de respuesta del usuario. | Validación final |
| Pruebas de rendimiento | Medir velocidad de carga, tiempo de respuesta de alertas en tiempo real y estabilidad bajo carga. | Etapa final |

---

## 3. Casos de Uso para Validación y Verificación

| # | Caso de Uso | Validación Previa | Verificación Durante el Desarrollo |
|---|--------------|-------------------|------------------------------------|
| 1 | Registro de denuncias | Se consulta si los usuarios realmente desean incluir foto/video y cómo prefieren describir los hechos. | Validar que el formulario no permita enviar datos vacíos y que los archivos se guarden correctamente. |
| 2 | Consulta de denuncias propias | Verificar si los ciudadanos desean filtros por fecha o estado. | Comprobar que solo se muestren denuncias del usuario autenticado. |
| 3 | Mapa de incidentes | Confirmar que los usuarios prefieren visualizar zonas peligrosas en mapas interactivos. | Asegurar que los marcadores y filtros funcionen y se actualicen en tiempo real. |
| 4 | Notificaciones de zonas de riesgo | Validar si los usuarios quieren alertas por correo o dentro de la app. | Probar que las notificaciones lleguen correctamente según las zonas configuradas. |
| 5 | Panel de administración | Confirmar con autoridades qué datos desean ver (tipos de incidentes, estados, zonas). | Verificar roles de usuario, permisos y actualización de estado en tiempo real. |
| 6 | Recuperación de contraseña | Revisar si los usuarios prefieren correo o SMS como método de recuperación. | Verificar envío correcto del enlace y validación de seguridad. |
| 7 | Calificación de zonas seguras/inseguras | Evaluar si los usuarios comprenden la escala de calificación (👍 / 👎). | Confirmar que el sistema registre solo una calificación por usuario y actualice el promedio. |

---

## 4. Validación de Requerimientos No Funcionales

| Requerimiento | Tipo | Método de Validación | Criterio de Aceptación |
|----------------|------|----------------------|-------------------------|
| Seguridad | No funcional | Pruebas de autenticación, cifrado de datos. | Los datos del usuario deben viajar cifrados y almacenarse de forma segura. |
| Disponibilidad | No funcional | Simulaciones de carga y tiempo de respuesta. | El sistema debe soportar al menos 100 conexiones simultáneas sin fallos. |
| Usabilidad | No funcional | Pruebas A/B con usuarios reales. | El 90% de los usuarios debe poder completar tareas sin ayuda externa. |
| Escalabilidad | No funcional | Pruebas en ambientes simulados de alta demanda. | El sistema debe permitir agregar más buses o zonas sin afectar rendimiento. |

---

## 5. Estrategia de Pruebas Futuras

- Testing automatizado con herramientas como **Jest (JavaScript)** o **PyTest (Python)**.  
- Pruebas de API con **Postman** o **Swagger**.  
- Pruebas de mapas y geolocalización simulando ubicaciones falsas para validar alertas.  
- Testing de UI con **Cypress** o **Selenium**.  
- Pruebas piloto en una ciudad específica antes del despliegue nacional.

---

## 6. Conclusión

La validación y verificación permitirán asegurar la **calidad, utilidad y confiabilidad** de la aplicación **SafeTransit** antes de su construcción definitiva.  
De esta forma, se garantiza que el desarrollo se base en requerimientos bien definidos, evitando reprocesos y asegurando que la aplicación aporte valor real a la comunidad.
