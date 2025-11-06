# 🧾 VALIDATION AND VERIFICATION PLAN  
## Proyecto: SafeCommunity – Plataforma de Denuncias Comunitarias  
**Autor:** Camilo García  
**Carrera:** Tecnología en Desarrollo de Software  
**Universidad:** Universidad Católica Luis Amigó  

---

## 1️⃣ Objetivo del documento
Definir los **procesos de validación y verificación** aplicables al proyecto **SafeCommunity**, con el fin de asegurar la calidad, funcionalidad y confiabilidad del sistema antes de su desarrollo e implementación.

---

## 2️⃣ Alcance
Este plan se centra en los casos de uso y pruebas conceptuales **previas al desarrollo**, que permitirán garantizar que el sistema responda a las necesidades de los ciudadanos y administradores comunitarios.

---

## 3️⃣ Validación (¿Estamos construyendo lo correcto?)
**Propósito:** Asegurar que el sistema cumpla con las expectativas y necesidades de los usuarios finales.

### Actividades de Validación:

| ID | Actividad | Descripción | Resultado Esperado |
|----|------------|--------------|--------------------|
| V1 | Revisión de requerimientos | Verificar que las historias de usuario reflejen las necesidades reales de los ciudadanos y administradores. | Lista de requerimientos validados por los interesados. |
| V2 | Entrevista con usuarios | Simular entrevistas con posibles ciudadanos o líderes comunitarios. | Ajustes a funcionalidades según feedback. |
| V3 | Validación de interfaz | Diseño de prototipos de formularios de denuncia y login. | Confirmación de que la interfaz es comprensible y accesible. |
| V4 | Validación de flujo de navegación | Revisión de cómo se pasa de una pantalla a otra (registro → denuncia → mapa → estadísticas). | Flujos lógicos y coherentes. |

---

## 4️⃣ Verificación (¿Estamos construyendo bien el sistema?)
**Propósito:** Comprobar que los módulos y funciones definidas cumplen los requerimientos técnicos.

### Actividades de Verificación:

| ID | Actividad | Descripción | Resultado Esperado |
|----|------------|--------------|--------------------|
| VE1 | Revisión de casos de uso | Comprobar consistencia y trazabilidad entre historias de usuario y casos de uso. | Diagrama de casos de uso aprobado. |
| VE2 | Verificación de reglas de validación | Revisar los criterios de validación de formularios (campos vacíos, correos válidos, contraseñas seguras). | Formulario cumple las reglas especificadas. |
| VE3 | Prueba de consistencia de datos | Evaluar si los datos se almacenan correctamente en la base de datos (denuncias, usuarios). | Integridad de los datos garantizada. |
| VE4 | Revisión de seguridad | Comprobar que las credenciales se manejan de forma segura (no se almacenan en texto plano). | Cumplimiento de buenas prácticas de seguridad. |

---

## 5️⃣ Casos de Uso Identificados

### Caso de Uso 1: Registro de Ciudadano
**Actor:** Ciudadano  
**Descripción:** El ciudadano crea una cuenta en la plataforma.  
**Precondiciones:** El ciudadano no debe tener una cuenta existente.  

**Flujo principal:**
1. El ciudadano ingresa nombre, correo y contraseña.  
2. El sistema valida los datos.  
3. El sistema guarda el registro.  
4. Se muestra mensaje de confirmación.  

**Validación esperada:**  
- Se evita el registro de correos duplicados.  
- El sistema confirma el registro exitoso.

---

### Caso de Uso 2: Inicio de Sesión
**Actor:** Ciudadano  
**Descripción:** Permite acceder al sistema mediante correo y contraseña.  

**Flujo principal:**
1. El ciudadano ingresa correo y contraseña.  
2. El sistema valida credenciales.  
3. Si son correctas, accede al panel principal.  

**Verificación esperada:**  
- Validación de credenciales correcta.  
- Error si los datos no coinciden.  

---

### Caso de Uso 3: Registrar Denuncia
**Actor:** Ciudadano  
**Descripción:** El ciudadano reporta un incidente.  

**Flujo principal:**
1. El ciudadano completa los campos: tipo, descripción, ubicación.  
2. El sistema valida los campos.  
3. Se guarda la denuncia en la base de datos.  
4. Se muestra mensaje de confirmación.  

**Validación esperada:**  
- Todos los campos requeridos están completos.  
- Mensaje de confirmación visible.  

---

### Caso de Uso 4: Visualizar Denuncias
**Actor:** Administrador Comunitario  
**Descripción:** Permite visualizar denuncias en lista o mapa.  

**Validación esperada:**  
- El mapa muestra correctamente los marcadores.  
- Filtros funcionales (por tipo, zona).  

---

### Caso de Uso 5: Generar Estadísticas
**Actor:** Administrador Comunitario  
**Descripción:** El administrador genera gráficos con estadísticas.  

**Verificación esperada:**  
- Datos mostrados correctamente según tipo y fecha.  
- Gráficos actualizados en tiempo real.  

---

## 6️⃣ Conclusión
La validación y verificación permiten garantizar que el sistema **SafeCommunity** cumpla tanto con los requerimientos funcionales como con las expectativas de los usuarios.  
Estos procesos serán aplicados de forma iterativa durante el desarrollo para asegurar un producto confiable, útil y de calidad.

---

## 🧩 Diagrama de Casos de Uso

A continuación se muestra el diagrama de casos de uso del proyecto **SafeCommunity**, que representa las interacciones principales entre los actores y el sistema.

![Use Case Diagram – SafeCommunity](DiagramaSafeComunity.png)

## ⚙️ Requisitos No Funcionales (ISO/IEC 25000 – SQuaRE)

Según el estándar **ISO/IEC 25000**, los requisitos no funcionales garantizan la calidad del sistema SafeCommunity en aspectos más allá de las funcionalidades básicas.

| Categoría | Descripción |
|------------|-------------|
| **Usabilidad** | La interfaz debe ser intuitiva y accesible para todo tipo de usuarios, incluyendo adultos mayores. |
| **Fiabilidad** | El sistema debe garantizar la integridad de la información reportada, evitando duplicados o pérdida de datos. |
| **Eficiencia de Desempeño** | Las consultas y registros deben realizarse en menos de 3 segundos bajo carga normal. |
| **Seguridad** | Las contraseñas deben almacenarse cifradas y el acceso debe requerir autenticación. |
| **Mantenibilidad** | El código debe estar documentado para permitir actualizaciones futuras. |
| **Portabilidad** | La plataforma debe poder ejecutarse en navegadores modernos y dispositivos móviles. |




