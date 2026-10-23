https://easyosinstall.wordpress.com/2026/10/23/easy-appimage-manager/

Spanish and English Version

App image installer

Hello everyone:

Browsing my EasyOS, I have visited MENU, SETUP, APPIMAGE INSTALLER, and I liked what I have seen, but I have thought that it could be improved to satisfy new users and developers who use tests and improvements and we want to be able to go back.

It would become a small application center: easy to install, transparent to understand its operation and easy to maintain for developers. It would retain the lightness of EasyOS.

La captura de pantalla muestra una base clara, pero surge un problema inmediato: "Instalar/Actualizar/Eliminar" agrupa tres acciones muy diferentes en un solo botón. Además, es difícil saber qué está instalado, qué versión se tiene y qué sucederá al pulsarlo.

Requiere Python 3 con Tkinter. EASYOS NO ES EL CASO, ASÍ QUE TENDRÁN QUE INSTALARLO. python3-tk

Estas serían mis mejoras:

ElementoCómo lo dejaríaPermanent search engineBuscar por nombre y función: "editar audio", "video", "programa"...NavegaciónExplorar · Instaladas · Actualizaciones , con categorías como filtroLista de aplicacionesIcono, nombre, descripción breve, versión, tamaño y estadoBotón principalInstalar , abrir o actualizar , según corresponda.DesinstalaciónIndependent action, indicating whether you will keep the adjustments.Hoja de solicitudCaptura, sitio web oficial, licencia, origen comprobado y compatibilidadProgresoDescarga, comprueba e integra en el menú, con opción de cancelar.Archivo localAgregar AppImage Botón ... y posibilidad de arrastrarlo a la ventana.

De qué se enamorará un nuevo usuario

La experiencia debería ser: buscar → pulsar Instalar → tocar . The installer would take care of the file, permissions and menu entry with its icon.

Yo añadiría tres funciones especialmente útiles:

Regresa a la versión anterior. Al actualizar, conserva temporalmente la versión que funcionaba.

Errores que ofrecen una solución. En lugar de “la instalación falló”, explique “No se pudo descargar” y ofrezca Reintentar ; si no arranca, muestre Ver diagnóstico .

Desinstalar conservando las preferencias. Una opción adicional permitiría eliminar los datos identificados de la aplicación, especificando cuáles.

La compatibilidad tendría etiquetas concretas: «Probada en EasyOS [versión]» , «Sin comprobar» o «Problema conocido» . No pondría un sello genérico de «segura» o «compatible» sin evidencias.

Lo que enamoraría a los developers

La mejora fundamental estaría detrás de la interfaz: separar el catálogo, el motor de instalación y la ventana gráfica .

Technical proposalAdvantageUna ficha declarativa por aplicaciónAñadir programas sin modificar el instaladorCampos de versión, arquitectura, origen, licencia y verificaciónRevisiones más fáciles y comportamiento previsibleMotor compartido por interfaz y terminalAutomatizar instalaciones y reproducir erroresValidador de catálogoDetectar fichas incompletas, arquitecturas incorrectas y enlaces rotosRegistro de diagnóstico exportableFacilitar el soporte sin pedir al usuario diez comandosActualización preparada antes de sustituir la anteriorEvitar perder una instalación funcional por una descarga fallida

Los datos del catálogo deben tratarse como datos, sin ejecutar instrucciones de shell incluidas en las fichas. It would also check for downloads using hashes or signatures when there is a reliable reference; a hash downloaded next to the file alone does not prove who published it.

Para los colaboradores, añadir una aplicación debería consistir en rellenar una ficha, validarla y proponerla para revisión .

El detalle especial para EasyOS

Incluiría «Probar sin integrar en el menú» para un AppImage descargado por el usuario. Si le convence, después podría pulsar «Añadir a mis aplicaciones» .

Y, cuando exista una forma de aislamiento compatible y comprobada, ofrecería «Ejecutar aislada» , explicando qué carpetas y recursos podrá utilizar. Ser AppImage, por sí mismo, no debe presentarse como aislamiento.

My first version would have five priorities: search engine, separate buttons, local installation, useful diagnostics and updating with back. That would change the experience a lot; then it would incorporate the collaborative catalog and advanced features.

Visually I would bet on a compact list with good icons, enough space and a side token. Attractive, fast and comfortable also in the old equipment where you use EasyOS.

Así que estoy desarrollando un programa easy-appimage-manager-0.1.pet

Includes search engine, installation from file or URL, menu launchers, manual update, previous version recovery and error diagnosis. It also supports JSON catalogs for developers.

Instalación: pulsa el .pet y acepta. Después busca Easy AppImage Manager en Menú → Configuración . También puedes abrirlo con:

easy-appimage-manager

Requires Python 3 with Tkinter. EASYOS IS NOT THE CASE SO THEY WILL HAVE TO INSTALL IT. python3-tk

It’s a 0.1 trial version: I checked the engine and package, but not yet the interface or installation in EasyOS real. It works as a stand-alone application; the online catalog maintained and the isolation are pending.

Todas colaboraciones serán bienvenidas.
