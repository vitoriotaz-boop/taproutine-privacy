---
layout: page
title: Política de Privacidad de TapRoutine
lang: es
permalink: /es/
description: Información de privacidad y uso de datos de TapRoutine para Android.
eyebrow: Privacidad y uso de datos
brand_label: Privacidad
home_label: Inicio de la política de privacidad de TapRoutine
footer_label: TapRoutine · Android
contact_label: Contacto
---

<p class="last-updated">Última actualización: 11 de noviembre de 2026</p>
<nav class="language-nav" aria-label="Selección de idioma"><a href="{{ '/' | relative_url }}" lang="pt-BR">Português (Brasil)</a><a href="{{ '/en/' | relative_url }}" lang="en">English</a><span aria-current="page">Español</span></nav>
## Sobre esta versión de la app

TapRoutine es una app de vista previa para Android que permite configurar una rutina para una app elegida, programarla en el dispositivo, ejecutar pasos definidos por el usuario y comprobar puntos de la pantalla mediante el color. El APK inspeccionado tiene el identificador de paquete `io.github.vitoriotaz.taproutine`, `minSdk` 24, `targetSdk` 36 y `android:allowBackup=true`. Las conclusiones de este aviso se refieren a ese APK de vista previa y podrían no aplicarse a versiones futuras.

## Datos que la app crea o consulta

- **Rutina y ajustes del usuario:** pueden incluir el nombre de la rutina; el nombre y el identificador de paquete de la app elegida; horarios, días y zona horaria; pasos y gestos (como toques, deslizamientos, esperas, Atrás o Inicio) y sus posiciones; el color, el punto y la tolerancia utilizados en las comprobaciones; y ajustes como la frecuencia de comprobación y si se debe volver a abrir la app de destino. Los ajustes también pueden incluir el Guardián y una pantalla alternativa, con otra secuencia preconfigurada.
- **Apps disponibles para elegir:** TapRoutine consulta Android para mostrar apps que tienen una actividad de inicio disponible. El usuario elige la app de destino; el nombre y el identificador de paquete seleccionados se guardan en la rutina local.
- **Información temporal de la ventana en primer plano:** mientras el servicio de accesibilidad de TapRoutine está activo, recibe eventos Android `TYPE_WINDOW_STATE_CHANGED` y mantiene en memoria el nombre del paquete que proporciona el sistema. El servicio no lee el árbol de interfaz, textos, campos ni otro contenido de la pantalla.
- **Datos y registros locales:** las rutinas y los registros pueden incluir horarios, el paquete de la app de destino, el progreso y resultado de pasos e intentos, detalles técnicos de errores, valores de color, puntos/posiciones de la pantalla y su resolución. `SharedPreferences` también guarda el consentimiento relacionado con la divulgación y los estados y horarios de las programaciones y del Guardián.
- **Captura temporal para comprobar el color:** al hacer una comprobación, la app obtiene en memoria la pantalla/display actual completa para calcular únicamente el color promedio de un área de 3×3 en el punto indicado. Puede haber capturas durante las comprobaciones de la rutina, la detección de una pantalla alternativa y el funcionamiento del Guardián; no están necesariamente limitadas a la ventana o a la app de destino. La app no guarda deliberadamente la captura en un archivo. Es temporal y, en el flujo normal, se liberan los recursos asociados.

## Cómo se usan los datos

Los datos se utilizan en el dispositivo para guardar y cargar la rutina, programar su ejecución, realizar los pasos definidos por el usuario, comparar el color en el punto configurado y registrar resultados. Según la configuración, el color detectado puede seleccionar una secuencia alternativa ya preconfigurada o activar la acción preconfigurada del Guardián. La app no inventa acciones ni interpreta texto o contenido de la pantalla para decidir qué hacer.

## Procesamiento, almacenamiento y transmisión

Las rutinas y los registros se guardan en el almacenamiento local privado de la app. `SharedPreferences` también conserva los datos descritos arriba, incluido el consentimiento relacionado con la divulgación y los estados y horarios de las programaciones y del Guardián. El servicio mantiene en memoria el paquete de la ventana observado. La captura de pantalla es temporal; la app no la guarda deliberadamente en un archivo y libera los recursos asociados en el flujo normal.

El código del APK inspeccionado no implementa una cuenta, un servidor, sincronización, analítica, anuncios, pagos ni llamadas de red propias de la app. Esto no significa que no pueda salir ninguna copia del dispositivo: la copia de seguridad automática de Android/Google puede copiar datos como se explica a continuación. La app elegida como destino también puede tener sus propias conexiones y prácticas de datos, que TapRoutine no controla.

Si decides contactar con soporte por correo electrónico, tu mensaje y la dirección utilizada para enviarlo serán transmitidos por tu servicio de correo para que podamos recibirlo y responder. Es una acción externa que inicias tú, no una llamada de red propia de TapRoutine.

## Copia de seguridad automática de Android/Google

El APK de vista previa inspeccionado establece `android:allowBackup` en `true`. Si la copia de seguridad automática de Android está activa, Android puede copiar archivos privados de la app y datos de `SharedPreferences` —que pueden incluir rutinas, registros, consentimiento y estados/horarios de las programaciones y del Guardián— a la propia cuenta Google/Drive del usuario como parte del servicio de Android. El comportamiento depende de la configuración de las copias de seguridad, la versión de Android y el dispositivo.

Esta copia de seguridad es un servicio de Android/Google, no un envío de TapRoutine al servidor del desarrollador. La app y el desarrollador no tienen acceso a la copia de seguridad. Borrar los datos locales o desinstalar la app no debe entenderse como garantía de que se elimine una copia separada que pueda conservar el servicio de copia de seguridad.

## Conservación y opciones del usuario

La rutina y los registros permanecen en el almacenamiento de la app hasta que se sustituyan o eliminen. El botón **Limpiar** del prototipo borra el registro de ejecución. Si el registro crece mucho, el prototipo también puede eliminar entradas antiguas y conservar las más recientes. Al guardar una configuración modificada se sustituye la rutina local; cancelar la programación detiene la ejecución programada, pero no elimina por sí solo la configuración guardada. Para eliminar los datos locales de la app, utiliza los controles de almacenamiento de Android para borrar los datos de la app o desinstálala; esto no garantiza que se elimine una copia de seguridad separada, si existe. El sistema operativo puede mostrar otros nombres para estos controles.

## Servicios y permisos de Android

- **Servicio de accesibilidad de Android:** el usuario debe activarlo en los ajustes del sistema para ejecutar los gestos configurados y realizar comprobaciones. Recibe eventos `TYPE_WINDOW_STATE_CHANGED` y mantiene en memoria el paquete proporcionado por el sistema; no lee el árbol de interfaz, textos ni campos. La captura temporal de pantalla se utiliza para calcular el promedio de color descrito arriba.
- **`SCHEDULE_EXACT_ALARM`:** relacionada con la programación de alarmas exactas. Si Android no permite alarmas exactas, la programación puede ser menos precisa y retrasarse.
- **`RECEIVE_BOOT_COMPLETED`:** permite al módulo recibir el evento de reinicio del dispositivo para gestionar la reprogramación de las rutinas.
- **`WAKE_LOCK`:** permite mantener activo el dispositivo durante una ejecución que necesite continuar en segundo plano.
- **`KILL_BACKGROUND_PROCESSES`:** relacionada con la acción preconfigurada de cerrar el proceso de la app de destino en segundo plano cuando la rutina prevé volver a abrirla.
- **`POST_NOTIFICATIONS`:** relacionada con la visualización de notificaciones locales, por ejemplo, de resultados.

Android controla la disponibilidad, concesión y forma de autorización de estos permisos; pueden variar según los ajustes, la versión del sistema y el dispositivo. Este aviso no presupone que cada permiso genere un aviso de runtime concreto. Concede solo los permisos que consideres necesarios para las funciones que quieras utilizar.

## Edad prevista

Esta versión beta de TapRoutine está destinada a personas adultas de **18 años o más**; no está diseñada para niños ni adolescentes.

## Cambios futuros

Las funciones y prácticas descritas aquí corresponden al APK de vista previa inspeccionado y pueden cambiar. Si una versión futura recopila, transmite, comparte o conserva otros datos, o incorpora servicios, esta política deberá revisarse para reflejar esa versión antes de distribuirla. Consulta la versión de la política que acompañe a la versión aprobada.

## Contacto

Preguntas o solicitudes sobre esta política: [vitoriotaz@gmail.com](mailto:vitoriotaz@gmail.com).
