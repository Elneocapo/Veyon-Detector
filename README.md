# Monitor de Red (Alerta Veyon)

Un programa ultra ligero en Rust que te avisa con una notificación en la pantalla de Windows y un pitido si el profesor se conecta a vigilar tu pantalla a través de Veyon u otras herramientas de red. No consume casi nada y funciona en segundo plano.
### NO REQUIERE DE PRIVILEGIOS DE ADMINISTRADOR.

## ¿Qué hace?
* Revisa cada segundo si hay conexiones activas en el puerto `11400` (el que usa Veyon para transmitir el vídeo de la pantalla).
* Te suelta una notificación flotante de Windows abajo a la derecha, incluso si tienes el programa minimizado o estás a pantalla completa.
* Hace sonar un pitido (`beep`) en los cascos/altavoces del PC al detectar la conexión.

## ¿Cómo se usa?
* Ejecuta el `.exe` y dejalo abierto, el programa te enviara una notificación discreta cuando Veyon sea activado para ver tu pantalla

## Requisitos para que funcionen las notificaciones del monitor
El programa utiliza PowerShell y las notificaciones de Windows (NotifyIcon / ShowBalloonTip). Si no aparecen los avisos, comprueba estos ajustes:
1. Activar las notificaciones de Windows
1. Abre Configuración de Windows.
2. Entra en Sistema > Notificaciones (en Windows 10 puede aparecer como Notificaciones y acciones).
3. Activa Notificaciones.
4. Permite que las notificaciones muestren banners y aparezcan en el centro de notificaciones, si esas opciones están disponibles.
2. Desactivar No molestar / Asistente de concentración
- Desactiva No molestar o Asistente de concentración.
- Comprueba que no haya reglas automáticas que lo activen durante el horario de clase o al usar una aplicación.
3. Comprobar permisos y bloqueos de PowerShell
- Ejecuta PowerShell normalmente; el programa no debería necesitar permisos de administrador para mostrar la notificación.
- Comprueba que el antivirus o las políticas del equipo no estén bloqueando PowerShell.
- Si el equipo está administrado por el centro, puede haber políticas que impidan mostrar notificaciones o ejecutar scripts.
4. Comprobar que Windows no esté en una sesión que las suprima
- Revisa si está activado el modo de pantalla completa, una sesión de presentación o alguna configuración que silencie avisos.
- Comprueba que el volumen y los sonidos de notificación no estén silenciados (esto afecta al sonido, no necesariamente al banner visual).
