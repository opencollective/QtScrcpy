QtScrcpy
Ventanas Mac OS Ubuntu

licencia lanzamiento

中文 介绍

QtScrcpy se conecta a dispositivos Android a través de USB (o mediante TCP / IP) para visualización y control. NO requiere privilegios de root.

Una sola instancia admite hasta 16 conexiones de dispositivos Android al mismo tiempo.

Es compatible con tres plataformas principales: GNU / Linux, Windows y MacOS.

Se enfoca en:

luminosidad (nativo, muestra solo la pantalla del dispositivo)
rendimiento (30 ~ 60 fps)
calidad (1920 × 1080 o superior)
baja latencia ( 35 ~ 70ms )
tiempo de inicio bajo (~ 1 segundo para mostrar la primera imagen)
no intrusividad (no queda nada instalado en el dispositivo)
ganar

Mac

linux

Asignación de teclas personalizada (solo Windows)
Puede escribir su propio script para asignar las acciones del teclado y el mouse a los toques y clics del teléfono móvil de acuerdo con sus necesidades. Aquí están las reglas.

Se proporciona un script para el mapeo de "PUBG mobile" y TikTok de forma predeterminada. Una vez habilitado, puede jugar el juego con su teclado y mouse como la versión para PC. o puede usar las teclas de dirección arriba / abajo / izquierda / derecha para simular el deslizamiento hacia arriba / abajo / izquierda / derecha. También puede escribir sus propios archivos de mapeo para otros juegos de acuerdo con las reglas de escritura . La asignación de teclas predeterminada es la siguiente:

juego

Aquí hay una demostración en video de cómo jugar "PUBG mobile"

Aquí están las instrucciones para agregar nuevos archivos de mapeo personalizados.

Escribe un script personalizado y colócalo en el keymapdirectorio.
Haga clic refresh scriptpara comprobar si se puede encontrar
Seleccione su guión
Conecte su teléfono, inicie el servicio y haga clic en apply
Presione la ~tecla (lado izquierdo de la tecla numérica 1) para cambiar al modo de asignación personalizada (se puede cambiar en el script como switchkey)
Presione la tecla ~ de nuevo para volver al modo normal
(Para PUBG y juegos similares) Si desea conducir automóviles con WASD, debe verificar single rocker modeen la configuración del juego.
Gracias
QtScrcpy se basa en el proyecto scrcpy de Genymobile . Gracias

La diferencia entre QtScrcpy y scrcpy original es la siguiente:

llaves	scrcpy	QtScrcpy
ui	sdl	qt
codificar video	ffmpeg	ffmpeg
render de video	sdl	opengl
multiplataforma	auto implementado	proporcionado por Qt
idioma	C	C ++
estilo	sincronizar	asincrónico
controlar	solo toque	solo / multitáctil
construir	mesón + gradle	Creador de Qt
Es muy fácil personalizar su GUI con Qt
La programación asincrónica del mecanismo de ranura de señal basado en Qt mejora el rendimiento
Fácil de aprender
Agregue soporte para multitáctil
Aprender
Si está interesado en él y quiere aprender cómo funciona pero no sabe cómo empezar, puede optar por comprar mis lecciones en video grabadas. Detalla la arquitectura de desarrollo y el proceso de desarrollo de todo el software, y le ayuda a desarrollar QtScrcpy desde cero.

Introducción al curso: https://blog.csdn.net/rankun1/article/details/87970523

Puede unirse a mi grupo de QQ para QtScrcpy e intercambiar ideas con amigos de ideas afines.

Número de grupo QQ: 901736468

Requisitos
API de Android> = 21 (Android 5.0).

Asegúrese de haber habilitado la depuración de adb en su (s) dispositivo (s).

Descargar
Ventanas
Para Windows, por simplicidad, los archivos prediseñados con todas las dependencias (incluido adb) están disponibles:

QtScrcpy
o puedes construirlo tú mismo

Mac OS
Para Mac OS, por simplicidad, los archivos prediseñados con todas las dependencias (incluido adb) están disponibles:

QtScrcpy
o puedes construirlo tú mismo

Linux
puedes construirlo tú mismo (solo prueba de ubuntu)

correr
Conéctese a su dispositivo Android en su computadora, luego ejecute el programa y haga clic en el botón de abajo para conectarse al dispositivo Android.

correr

Pasos para la conexión inalámbrica (asegúrese de que el teléfono móvil y la PC estén en la misma LAN):
Habilite la depuración de USB en las opciones de desarrollador en el dispositivo Android
Conecte el dispositivo Android a la computadora a través de USB
Haga clic en actualizar dispositivo y verá que el número de dispositivo se actualiza
Haga clic en obtener IP del dispositivo
Haga clic en iniciar adbd
Haga clic en conexión inalámbrica
Haga clic en actualizar dispositivo nuevamente y se encontrará otro dispositivo con dirección IP. Seleccione este dispositivo.
Haga clic en iniciar servicio
​

Nota: no es necesario mantener su dispositivo Android conectado a través de USB después de iniciar adbd.

Introducción al botón de interfaz:
Start config: configuración de parámetros de función antes de iniciar el servicio

Puede establecer la velocidad de bits, la resolución, el formato de grabación y la ruta de guardado del video grabado localmente.

Registro de antecedentes: la pantalla del dispositivo Android no se muestra después de iniciar el servicio. Se registra en segundo plano.
Siempre en la parte superior: la ventana de video para el dispositivo Android se mantendrá en la parte superior
Cerrar pantalla: apaga automáticamente la pantalla del dispositivo Android para ahorrar energía después de iniciar el servicio
Conexión inversa: modo de inicio del servicio. Puede desmarcarlo si experimenta una falla de conexión con el mensajemore than one device
Actualizar dispositivos: actualice el dispositivo actualmente conectado

Iniciar servicio: conéctese al dispositivo Android

Detener el servicio: desconectarse del dispositivo Android

Detener todos los servicios: desconecte todos los dispositivos Android conectados

Obtener la IP del dispositivo: obtenga la dirección IP del dispositivo Android y actualícela en el área "Inalámbrico" para facilitar la configuración de la conexión inalámbrica.

Iniciar adbd: inicia el servicio adbd del dispositivo Android. Debe iniciarlo antes de la conexión inalámbrica.

Conexión inalámbrica: conéctese a dispositivos Android de forma inalámbrica

Desconexión inalámbrica: desconecte los dispositivos Android conectados de forma inalámbrica

comando adb: ejecute comandos adb personalizados (los comandos de bloqueo no son compatibles ahora, como el shell)

La función principal
Mostrar pantallas de dispositivos Android en tiempo real

Control de mouse y teclado en tiempo real de dispositivos Android

Grabación de pantalla

Captura de pantalla en png

Conexión inalámbrica

Admite hasta 16 conexiones de dispositivos (el número puede ser mayor si el rendimiento de su PC lo permite. Debe compilarlo usted mismo)

Visualización de pantalla completa

Mostrar en la parte superior

Instalar apk: arrastre y suelte apk en la ventana del video para instalar

Transferir archivos: arrastre archivos a la ventana de video para enviar archivos a dispositivos Android

Grabación en segundo plano: solo grabación, sin interfaz de pantalla

Copiar pegar

Es posible sincronizar portapapeles entre la computadora y el dispositivo, en ambas direcciones:

Ctrl+ ccopia el portapapeles del dispositivo al portapapeles de la computadora;
Ctrl+ Shift+ vcopia el portapapeles de la computadora al portapapeles del dispositivo;
Ctrl+ v pega el portapapeles de la computadora como una secuencia de eventos de texto (pero rompe los caracteres que no son ASCII).
Control de grupo

Atajos
Acción	Atajo (Windows)	Acceso directo (macOS)
Cambiar el modo de pantalla completa	Ctrl+f	Cmd+f
Cambiar el tamaño de la ventana a 1: 1 (píxel perfecto)	Ctrl+g	Cmd+g
Cambiar el tamaño de la ventana para eliminar los bordes negros	Ctrl+ x| Doble clic	Cmd+ x | Doble clic
Haga clic en HOME	Ctrl+ h| Clic medio	Ctrl+ h| Clic medio
Haga clic en BACK	Ctrl+ b| Clic derecho²	Cmd+ b | Clic derecho²
Haga clic en APP_SWITCH	Ctrl+s	Cmd+s
Haga clic en MENU	Ctrl+m	Ctrl+m
Haga clic en VOLUME_UP	Ctrl+ ↑ (arriba)	Cmd+ ↑ (arriba)
Haga clic en VOLUME_DOWN	Ctrl+ ↓ (abajo)	Cmd+ ↓ (abajo)
Haga clic en POWER	Ctrl+p	Cmd+p
Encendido	Clic derecho²	Clic derecho²
Apagar la pantalla del dispositivo (seguir duplicando)	Ctrl+o	Cmd+o
Expandir el panel de notificaciones	Ctrl+n	Cmd+n
Contraer panel de notificaciones	Ctrl+ Shift+n	Cmd+ Shift+n
Copiar el portapapeles del dispositivo a la computadora	Ctrl+c	Cmd+c
Pegar el portapapeles de la computadora en el dispositivo	Ctrl+v	Cmd+v
Copiar el portapapeles de la computadora al dispositivo	Ctrl+ Shift+v	Cmd+ Shift+v
¹ Haga doble clic en los bordes negros para eliminarlos.

² Hacer clic con el botón derecho enciende la pantalla si estaba apagada; de lo contrario, presiona ATRÁS.

QUE HACER
QUE HACER

Preguntas más frecuentes
Preguntas más frecuentes

DESARROLLAR
DESARROLLAR

¿Por qué desarrollar QtScrcpy?
Hay varias razones enumeradas a continuación según su importancia (de mayor a menor).

En el proceso de aprendizaje de Qt, necesito un proyecto real para probar
Tengo algunas habilidades básicas sobre audio y video y me interesan
Tengo algunas habilidades de desarrollo de Android. Pero lo he usado durante mucho tiempo. Quiero consolidarlo.
Encontré scrcpy y decidí rehacerlo con la nueva pila de tecnología (C ++ + Qt + Opengl + ffmpeg)
Cómo construir
Se proporcionan todas las dependencias y es fácil de compilar.

Cliente de PC
Configure el entorno de desarrollo de Qt en la plataforma de destino (Qt> = 5.12.0, vs> = 2017 (mingw no es compatible))
Clonar el proyecto
Abra el directorio raíz del proyecto all.pro con QtCreator
Compilar y ejecutar
Android (si no tiene requisitos especiales, puede usar directamente el scrcpy-server.jar incorporado)
Configurar un entorno de desarrollo de Android en la plataforma de destino
Abra el proyecto del servidor en la raíz del proyecto con Android Studio
La primera vez que lo abra, si no tiene la versión correspondiente de gradle, se le pedirá que busque gradle, si desea actualizar gradle y crearlo. Seleccione Cancelar. Después de cancelar, se le pedirá que seleccione la ubicación del gradle existente. También puede cancelarlo (se descargará automáticamente).
Edite el código según sea necesario, pero, por supuesto, no es necesario.
Después de compilar el apk, cámbiele el nombre a scrcpy-server y reemplace third_party / scrcpy-server.
Licencia
Dado que se basa en scrcpy, respete su Licencia

Copyright (C) 2018 Genymobile

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
Sobre el Autor
Barry CSDN

Un programador ordinario, que trabaja principalmente en C ++ para el desarrollo de clientes de escritorio, se graduó de Shandong durante más de un año en software educativo de simulación de acero, y luego se mudó a Shanghai para trabajar en seguridad, campos relacionados con la educación en línea, familiarizado con audio y video. Comprendo los campos de audio y video, como llamadas de voz, educación en vivo, videoconferencia y otras soluciones relacionadas. Al mismo tiempo, tenga Android, servidor Linux y otra experiencia de desarrollo.
