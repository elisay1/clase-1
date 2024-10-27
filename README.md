# ESTRUCTURA DE PROYECTO

> [!NOTE]
> Esta estructura de proyecto facilita la organización de código y recursos, lo cual permite un desarrollo más limpio y mantenible.

## Estructura de Carpetas

![image](https://github.com/user-attachments/assets/8eeaed7a-2cce-4e12-8359-f342dfcbb2b9)


El proyecto está dividido en varias carpetas con diferentes responsabilidades. A continuación, se detalla cada una de ellas:

### 1. `assets/`
Contiene todos los recursos utilizados en la aplicación, como imágenes, fuentes, sonidos, y archivos adicionales. Se recomienda mantener los recursos organizados en subcarpetas según el tipo de archivo para facilitar el acceso y mantenimiento.

- `assets/images/`: Almacena las imágenes utilizadas en la interfaz de usuario (por ejemplo, iconos, fondos, etc.).
- `assets/fonts/`: Contiene las fuentes personalizadas utilizadas en la aplicación.
- `assets/sounds/`: Archivos de sonido para efectos sonoros, música, o notificaciones.
- `assets/files/`: Cualquier archivo adicional requerido por la aplicación (por ejemplo, PDFs).

> [!TIP]
> Mantener los recursos en subcarpetas organizadas mejora la eficiencia del desarrollo y la facilidad de uso en toda la aplicación.

### 2. `lib/src/screens/`
Esta carpeta contiene los archivos que definen las pantallas de la aplicación. Cada pantalla representa una vista o sección de la app y está organizada según el flujo de navegación.

- Ejemplos: `welcome_screen.dart`, `login_screen.dart`, `home_screen.dart`.

### 3. `lib/src/models/`
Define las clases utilizadas para manejar los datos de la aplicación. Los modelos representan las entidades del dominio, como usuarios, salones, reservas, etc.

> [!IMPORTANT]
> Los modelos ayudan a estructurar y gestionar los datos, separando la lógica de negocio del código de interfaz.

### 4. `lib/src/utils/`
Contiene clases y funciones auxiliares. En esta carpeta se encuentran los cálculos, conversiones y constantes que son comunes a toda la aplicación.

- Ejemplos: manipulación de fechas, validación de datos, constantes globales.

### 5. `lib/src/widgets/`
Esta carpeta incluye widgets reutilizables. Los widgets son componentes de interfaz que se pueden utilizar en varias pantallas para evitar duplicación de código y mejorar la consistencia.

- Ejemplos: `custom_button.dart`, `custom_input_field.dart`.

> [!TIP]
> La reutilización de widgets no solo ahorra tiempo, sino que también reduce la posibilidad de errores en el código.

### 6. `lib/src/services/`
En esta carpeta se encuentran las clases encargadas de la comunicación con servicios externos, como APIs, bases de datos en la nube o autenticación de usuarios.

- Ejemplos: `api_service.dart`, `auth_service.dart`.

> [!CAUTION]
> La comunicación con servicios externos debe estar correctamente gestionada para evitar problemas de seguridad y garantizar una buena experiencia de usuario.

### 7. `lib/main.dart`
Este es el punto de entrada de la aplicación, donde se define la función `main()` y la configuración inicial de la app. Incluye la configuración de temas y rutas principales, usando `MaterialApp` o `CupertinoApp`.

> [!WARNING]
> Asegúrate de que el archivo `main.dart` esté bien estructurado, con una configuración clara de las rutas y temas para evitar problemas durante la ejecución.

## Buenas Prácticas

- **Modularidad**: Mantener cada parte del código separada según su responsabilidad hace que el proyecto sea fácil de entender y modificar.
- **Reutilización de Código**: Usar widgets y funciones reutilizables facilita el mantenimiento y reduce errores.
- **Consistencia**: Definir constantes para los colores, estilos y otras propiedades permite mantener una apariencia uniforme en toda la aplicación.
- **Routes**: [Puedes trabajar con tus rutas personalizadas](href="https://github.com/elisay1/proyect_flutter/blob/main/Routes.md)

> [!NOTE]
> Estas buenas prácticas aseguran que el proyecto sea escalable, mantenible y fácil de entender por otros desarrolladores que trabajen en él en el futuro.

## Conclusión
La estructura de la App está diseñada para garantizar la organización y calidad del código, facilitando el desarrollo y escalabilidad del proyecto. La separación clara de responsabilidades, junto con el uso de widgets reutilizables y servicios bien definidos, asegura un proyecto bien mantenido y preparado para crecer.
