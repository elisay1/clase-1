# Documentación de las Rutas Personalizadas en la APP

En la aplicación **App**, hemos creado un sistema de rutas personalizadas para gestionar la navegación entre las diferentes pantallas de la aplicación de forma clara y estructurada. Esto nos permite mantener una mayor organización y facilitar el mantenimiento del código.

> [!NOTE]
> Las rutas personalizadas ayudan a organizar la navegación, proporcionando una manera centralizada y coherente de definir cómo el usuario se mueve entre pantallas.

## Archivo `routes.dart`

En el archivo **`routes.dart`** se definen las rutas como constantes. Este enfoque ayuda a mantener la consistencia de los nombres de las rutas y evita errores tipográficos.

```dart
// lib/src/routes/routes.dart
// Creamos rutas personalizadas
class Routes {
  static const String splash = '/splash';
}
```

- **Clase Routes:** Esta clase contiene constantes estáticas para cada ruta de la aplicación.
- **static const String splash:** Define la ruta para la pantalla de bienvenida o "Splash".

> [!TIP] 
> Utilizar constantes para definir rutas permite que sea fácil referenciarlas en cualquier parte del proyecto y evita errores de escritura.

**Archivo app_routes.dart**
El archivo app_routes.dart contiene el mapa de rutas que asocia cada ruta a una pantalla específica. Este mapa se utiliza para registrar todas las rutas en el widget MaterialApp, facilitando la navegación.
```dart
// lib/src/routes/app_routes.dart
import 'package:bliss_app/src/routes/routes.dart';
import 'package:bliss_app/src/screens/splash_screen.dart';
import 'package:flutter/material.dart';

// Ahora creamos las rutas asi a donde nos van a dirigir
Map<String, Widget Function(BuildContext)> appRoutes = {
  Routes.splash: (_) => const SplashPage(),
};
```

- **Map<String, Widget Function(BuildContext)> appRoutes:** Este mapa contiene la asociación de cada ruta con su correspondiente widget (pantalla).

- **Routes.splash:** Hace referencia a la constante definida en routes.dart, apuntando a la pantalla de bienvenida (SplashPage).
> [!IMPORTANT] 
> Mantener las rutas en un solo lugar (como app_routes.dart) hace que sea más fácil actualizar, agregar o eliminar pantallas, sin necesidad de buscar código en diferentes partes del proyecto.

Uso de las Rutas en MaterialApp
En el archivo principal (main.dart), el mapa de rutas se registra en el widget MaterialApp usando la propiedad routes, lo cual permite gestionar la navegación entre pantallas de manera clara y eficiente.
```dart
MaterialApp(
  // Inicializa la ruta inicial y otras rutas si es necesario
            initialRoute: Routes.splash,
            routes: appRoutes,
  // otras configuraciones
)
```

- **initialRoute:** Define la ruta que se cargará inicialmente al abrir la aplicación.
- routes: Asocia las rutas definidas en el mapa appRoutes al MaterialApp, facilitando la navegación con Navigator.pushNamed().

> [!WARNING] 
> Asegúrate de que todas las rutas definidas en app_routes.dart tengan un widget correspondiente. De lo contrario, podrías encontrar errores durante la navegación.

**### Buenas Prácticas**

- **Organización:** Mantener las rutas en routes.dart y app_routes.dart ayuda a centralizar la configuración de la navegación, haciéndola más fácil de mantener.
- **Uso de Constantes:** Utilizar constantes para las rutas evita errores tipográficos y hace el código más legible.
- **Navegación Clara:** Al definir las rutas en MaterialApp, se permite un acceso fácil mediante Navigator.pushNamed(), mejorando la claridad del código.

> [!TIP] 
> Para agregar nuevas rutas, simplemente define una constante en routes.dart y agrégala al mapa appRoutes en app_routes.dart.
