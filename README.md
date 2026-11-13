# Monitor de Red (Alerta Veyon)

Un programa ultra ligero en Rust que te avisa con una notificación en la pantalla de Windows y un pitido si el profesor se conecta a vigilar tu pantalla a través de Veyon u otras herramientas de red. No consume casi nada y funciona en segundo plano.
### NO REQUIERE DE PRIVILEGIOS DE ADMINISTRADOR.

## ¿Qué hace?
* Revisa cada segundo si hay conexiones activas en el puerto `11400` (el que usa Veyon para transmitir el vídeo de la pantalla).
* Te suelta una notificación flotante de Windows abajo a la derecha, incluso si tienes el programa minimizado o estás a pantalla completa.
* Hace sonar un pitido (`beep`) en los cascos/altavoces del PC al detectar la conexión.

## ¿Cómo se usa?
* Ejecuta el `.exe` y dejalo abierto, el programa te enviara una notificación discreta cuando Veyon sea activado para ver tu pantalla
