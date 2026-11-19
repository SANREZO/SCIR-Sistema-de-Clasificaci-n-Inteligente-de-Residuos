Cómo usarlo

1. Abre `SCRI.html` en Edge o Chrome: con doble clic en el archivo o, en VS Code,
   con clic derecho → **Open with Live Server**.
2. Pulsa **Encender cámara** y acepta el permiso.
3. Muestra un objeto: el sistema dice en qué caneca va.

La primera vez la IA descarga unos 18 MB; el avance se ve en la fila **IA** del panel.
La cámara no funciona dentro de vistas previas (la del chat o la de VS Code): abre la página en el navegador.

Cómo funciona

- Todo está en un solo archivo: `SCRI.html`.
- La cámara y la IA son independientes: la cámara se enciende aunque la IA todavía esté cargando o haya fallado.
- Las librerías (versión fija) vienen de jsDelivr, con unpkg de respaldo, y se verifican con SRI.
- El modelo se descarga de Google; si falla, se usan copias del mismo modelo en jsDelivr o unpkg
  (paquete npm `node-red-contrib-tfjs-coco-ssd@1.0.6`).
- Usa la tarjeta gráfica (WebGL); si no está disponible o falla, usa el procesador.

Si algo falla

- Junto a "SCIR" debe decir **v4**. Si no lo dice, estás abriendo otro archivo.
- Los problemas de cámara o de IA se explican en la propia página; los errores de JavaScript aparecen en un aviso rojo arriba.
- Más detalle: F12 → pestaña Consola (mensajes que empiezan por `SCRI:`).

 Privacidad

El video se procesa únicamente en tu navegador; no se envía ni se guarda en ningún servidor.

Seguridad

- No hay claves, contraseñas ni servidor propio.
- Librerías con versión fija y SRI: si alguien las modifica en el CDN, el navegador no las ejecuta.
- Conexiones externas: Google Fonts, jsDelivr / unpkg (librerías y respaldo del modelo) y Google Cloud Storage (modelo).

Tecnologías

HTML, CSS, JavaScript, TensorFlow.js 4.22 y COCO-SSD 2.2.3.

Próximos pasos

Modelo MobileNetV2 entrenado específicamente para residuos (OpenCV + TensorFlow).

Licencias de terceros

TensorFlow.js, COCO-SSD y los pesos del modelo son © Google LLC, bajo licencia Apache 2.0.
La copia de respaldo del modelo viene del paquete `node-red-contrib-tfjs-coco-ssd` (Apache 2.0).

## Derechos de autor
© 2026 SANREZO. Todos los derechos reservados.

Las librerías y modelos de terceros (como TensorFlow.js y COCO-SSD) conservan sus respectivas licencias (Apache 2.0).
