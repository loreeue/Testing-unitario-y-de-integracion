## Testing Unitario y de Integración

Este proyecto forma parte de la asignatura **Ampliación de Ingeniería del Software** del Grado en Ingeniería Informática. Su objetivo es implementar pruebas automáticas para asegurar la calidad de la aplicación **Nitflex**, que gestiona películas.

### Descripción del Proyecto

El objetivo de esta práctica es desarrollar y ejecutar **tests unitarios** e **integración** para las funcionalidades principales de la aplicación Nitflex, centrándose en la validación de URLs y la gestión de películas.

### Funcionalidades Probadas

#### Tests Unitarios: `FilmService`
- **Guardar películas con URL válida:**
  - Se asegura que la película se guarda en el repositorio y se lanza una notificación.
- **Guardar películas con URL inválida:**
  - La película **NO** se guarda en el repositorio ni se lanza una notificación.
- **Validación del título de la película:**
  - El título no debe ser vacío.
- **Uso obligatorio de Mocks:**
  - Todas las dependencias deben ser simuladas, evitando la dependencia de una base de datos real.

#### Tests de Integración: `UrlUtils`
- **URLs inválidas:**
  - URLs con formato incorrecto son marcadas como no válidas.
- **URLs inexistentes:**
  - Aunque tengan formato válido, si no existen, son marcadas como no válidas.

### Requisitos

- **Independencia de tests:**
  - Los tests no deben depender entre sí ni de recursos externos inicializados previamente.
- **Cobertura de errores:**
  - Comprobación de que se lanzan los errores adecuados con los mensajes esperados.
- **Modularización:**
  - Separar los tests en paquetes o clases según su naturaleza (unitarios o de integración).

### Tecnologías Utilizadas

- **Java** con soporte para **JUnit 5**.
- **Maven** para la gestión del proyecto y la ejecución de pruebas.
- Uso de **Mocks** (e.g., Mockito) para simular dependencias.

### Cómo Ejecutarlo

1. **Compilación y ejecución de tests:**
   Utiliza Maven para ejecutar todos los tests del proyecto:
   ```bash
   mvn test
   ```

2. **Estructura del Proyecto:**
   - `src/main/java`: Código principal de la aplicación.
   - `src/test/java`: Código de pruebas unitarias e integración.
