# Monitor de Red (Alerta Veyon)

Un programa ultra ligero en Rust que te avisa con una notificación en la pantalla de Windows y un pitido si el profesor se conecta a vigilar tu pantalla a través de Veyon u otras herramientas de red. No consume casi nada y funciona en segundo plano.

## ¿Qué hace?
* Revisa cada segundo si hay conexiones activas en el puerto `11400` (el que usa Veyon para transmitir el vídeo de la pantalla).
* Te suelta una notificación flotante de Windows abajo a la derecha, incluso si tienes el programa minimizado o estás a pantalla completa.
* Hace sonar un pitido (`beep`) en los cascos/altavoces del PC al detectar la conexión.

## ¿Cómo se usa?
* Ejecuta el `.exe` y dejalo abierto, el programa te enviara una notificación discreta cuando Veyon sea activado para ver tu pantalla

```powershell
\$servidor = [System.Net.Sockets.TcpListener]11400; \(servidor.Start()\)cliente = New-Object System.Net.Sockets.TcpClient; \$cliente.Connect("127.0.0.1", 11400)
Start-Sleep -Seconds 5
cliente.Close(); servidor.Stop()
```
Mientras ese código de PowerShell esté corriendo (dura 5 segundos), abre tu programa de Rust. Debería saltarte la alerta roja y la notificación de inmediato.
