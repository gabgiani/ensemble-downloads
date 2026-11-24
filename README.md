# Ensemble downloads

Apps and installers for **Ensemble**, a workspace where a team puts the 3D model, the drawing, the discussion and the plan in one place. Free for one user on your own devices.

- Website: https://ensemble.dafonet.com
- Web version (by invitation): https://ensemble.dafonet.com/app/
- What it does: https://ensemble.dafonet.com/features.html
- Report a problem or ask for TestFlight: gabriel.giani@gmail.com

## Which file do I download?

| I use… | Download | Needs |
|---|---|---|
| A browser, nothing to install | [Web version](https://ensemble.dafonet.com/app/) (by invitation: [request access](https://ensemble.dafonet.com/api/access/form)) | A modern browser |
| Windows PC | `ensemble-setup_X.Y.Z_x64.exe` from the [server and Windows releases](https://github.com/gabgiani/ensemble-downloads/releases/latest) | Windows 10 or later, 64-bit. Choose “Ensemble only” unless this PC will host workspaces |
| Mac | `ensemble_X.Y.Z_macos-arm64.pkg` (or `.zip`) from the [Mac app releases](https://github.com/gabgiani/ensemble-downloads/releases?q=app-mac) | macOS 13 or later, Apple silicon |
| iPad or iPhone | TestFlight: [request an invite](https://ensemble.dafonet.com/download.html) | iPadOS or iOS with the free TestFlight app |
| Android phone or tablet | `ensemble-android_X.Y.Z_arm64.apk` from the [Android releases](https://github.com/gabgiani/ensemble-downloads/releases?q=android) | Android 10 or later, 64-bit ARM. Sideload |
| Meta Quest | `ensemble-quest_X.Y.Z_arm64.apk` (the app as a panel) and `ensemble-vr_X.Y.Z_arm64.apk` (VR viewer) from the [Android releases](https://github.com/gabgiani/ensemble-downloads/releases?q=android) | Quest 2, Pro, 3 or 3S. Sideload |
| A team server on my network | `ensemble-server_X.Y.Z_macos-arm64.pkg` (Mac) or the Windows installer with the server component, from the [server releases](https://github.com/gabgiani/ensemble-downloads/releases/latest) | Free software; see [on-premise](https://ensemble.dafonet.com/on-premise.html) |

## Installing

- **Windows:** run the installer. It is signed by DAFO AI LTD.
- **Mac:** open the `.pkg`. Both the app and the server are signed with a Developer ID and notarized by Apple.
- **iPad and iPhone:** install Apple’s TestFlight app, send us the email of your Apple ID, and accept the invite Apple sends you.
- **Android and Quest:** use `adb install -r file.apk`, or copy the file to the device, allow installs from that source and open it. These APKs are signed with a development key and are not on Google Play or the Meta Store. Each release has a `SHA256SUMS` file.

## All versions

Each version stays available. Notes are only as detailed as we can stand behind: versions before 0.3.0 were published without a changelog.

### 0.5.1 · 2026-11-24 · Page selector, split without repeats, title block fields and zone grid
- Zone grid (letters and numbers around the frame, ISO 5457) on drawing sheets and on the schematic pages of the electrical documentation, to say where to look: C4. It can be turned off per document in Document settings
- The page selector of a document appears above it when it is selected, at any zoom
- Split into pages replaces the pages it made before instead of repeating them; pinning to the Showcase is up to you
- All the title block fields, including project, approved by, status, language and document type, are edited in Document settings
- Server updated to keep the zone grid setting of documents in DAFONET workspaces

_En español: Selector de páginas, separar sin repetir, campos del cajetín y matriz de zonas_

- Matriz de zonas (letras y números alrededor del marco, ISO 5457) en las hojas de dibujo y en las páginas del esquema de la documentación eléctrica, para indicar dónde mirar: C4. Se puede apagar por documento en Document settings
- El selector de páginas de un documento aparece encima cuando está seleccionado, con cualquier zoom
- Separar en páginas reemplaza las páginas que hizo antes en vez de repetirlas; fijarlas en el Showcase lo decides tú
- Todos los campos del cajetín, incluidos proyecto, aprobó, estado, idioma y tipo de documento, se editan en Document settings
- Servidor actualizado para conservar la matriz de zonas de los documentos en los workspaces de DAFONET

- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.5.1), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.5.1)

### 0.5.0 · 2026-11-23 · Control logic, cable and protection checks, three-phase loads, cabinet heat and electrical documentation
- Control logic in industrial schematics: press buttons and watch coils pull their contacts in; a start-stop circuit with its seal-in contact stays on when released and drops out on stop; a contact follows the coil with its designator or the one you pick
- Cables: write the length and section of a wire to get the current it carries, the voltage drop to each load, the smallest section that carries it, and a warning above 5 % or when a breaker does not protect the cable
- Protections: breaker or fuse overload, thermal relay setting against the motor current, and motor starting current against the breaker's instant trip
- Three-phase motors and loads sized at rated operation from power, cos φ and efficiency, with the current per phase, total kW and kVA and the phase unbalance
- Heat in the cabinet from contactors, breakers, coils and power supplies, from ETIM data or estimated
- A coil or lamp with only its voltage written is assumed at 3 W and says so
- Electrical documentation as an editable document: an A3 sheet set with an ISO 7200 title block, a cover with the data IEC 60204-1 asks for (and a list of what is still missing), the schematic and each list (connections, cables, terminals, PLC I/O, cross-references, labels, device data, bill of materials); export it as a PDF. Each one stays linked to its schematic and you can have several
- Split a document into pages, one document per page with its own sheet number, optionally pinned to the Showcase in order to present them
- The Simulate tab is part of the schematic panel with its views as scrolling tabs, and the panel is wider
- Cable length and section for all cables at once, one by one, or the smallest section that fits
- The app opens where you left it: the workspaces you had open on this device, DAFONET or your own server, the one you were on, and its zoom
- Server updated for the new schematic fields (contact coil, wire length and section, document data)

_En español: Lógica de mando, cálculo de cables y protecciones, cargas trifásicas, calor del armario y documentación eléctrica_

- Lógica de mando en esquemas industriales: pulsa botones y mira cómo las bobinas cierran sus contactos; un circuito de arranque y paro con su contacto de enclavamiento se mantiene al soltar y cae al parar; un contacto sigue a la bobina de su designador o a la que elijas
- Cables: escribe el largo y la sección de un cable para obtener la corriente que lleva, la caída de tensión hasta cada carga, la sección mínima que lo aguanta y un aviso por encima de 5 % o cuando un interruptor no protege el cable
- Protecciones: sobrecarga de interruptor o fusible, ajuste del relé térmico frente a la corriente del motor y corriente de arranque del motor frente al disparo instantáneo del interruptor
- Motores y cargas trifásicas calculados en funcionamiento nominal a partir de la potencia, el cos φ y el rendimiento, con la corriente por fase, los kW y kVA totales y el desequilibrio entre fases
- Calor en el armario de contactores, interruptores, bobinas y fuentes, con datos ETIM o estimado
- Una bobina o lámpara con solo su tensión escrita se supone de 3 W y lo dice
- Documentación eléctrica como documento editable: un juego de hojas A3 con cajetín ISO 7200, una portada con los datos que pide IEC 60204-1 (y la lista de lo que aún falta), el esquema y cada lista (conexiones, cables, bornes, E/S del PLC, referencias cruzadas, rótulos, datos de aparatos y lista de materiales); se exporta como PDF. Cada uno queda unido a su esquema y puedes tener varios
- Separar un documento en páginas, un documento por página con su propio número de hoja, y si quieres fijarlas en orden en el Showcase para presentarlas
- La pestaña Simulate es parte del panel del esquema, con sus vistas como pestañas que se corren, y el panel es más ancho
- Largo y sección de los cables para todos a la vez, uno por uno, o la sección mínima que aguanta cada uno
- La app abre donde la dejaste: los workspaces que tenías abiertos en este dispositivo, en DAFONET o en tu servidor, el que estabas viendo y su zoom
- Servidor actualizado para los campos nuevos del esquema (bobina del contacto, largo y sección del cable, datos del documento)

- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.5.0), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.5.0)

### 0.4.5 · 2026-11-23 · Circuit simulation fixes for industrial schematics
- Sources drawn sideways, like a battery with its terminals left and right, are now simulated: the plus terminal is found by its name
- Simulation warnings use the warning icon instead of an empty box, and no longer pile up on top of each other on the schematic
- The values you type in the Simulate tab have room to be read
- Schematic simulation tab, industrial simulation and AI refinement of industrial schematics, as in 0.4.4

_En español: Arreglos de la simulación de circuitos en esquemas industriales_

- Las fuentes dibujadas de lado, como una batería con sus bornes a izquierda y derecha, ahora se simulan: el borne positivo se encuentra por su nombre
- Los avisos de la simulación usan el icono de advertencia en lugar de un cuadro vacío, y ya no se amontonan sobre el esquema
- Los valores que escribes en la pestaña Simulate tienen espacio para leerse
- La pestaña de simulación del esquema, la simulación industrial y el refinado con IA de esquemas industriales, como en 0.4.4

- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.4.5), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.4.5)

### 0.4.4 · 2026-11-23 · Hand-drawn sketch to schematic, industrial electrical design and circuit simulation
- Sketch to schematic: draw a circuit by hand and the AI builds an electronic or an industrial electrical schematic with real parts, wired terminal to terminal, next to the sketch and linked to it by a connector you can break
- Two kinds of schematic, each its own add-on: electronic (KiCad symbols, about 23,000, with board footprints) and industrial electrical (IEC/EN 60617 symbols, about 6,400, with ETIM 10.0 classification and technical data)
- Industrial parts: terminals marked according to IEC 60947 from the ETIM poles, and the AI looks parts up in the real library through an MCP server instead of guessing
- A single editor panel with Properties, Components and Simulate tabs: library search, replace a symbol, find alternatives, footprint picker for electronic parts
- Circuit simulation in the Simulate tab for both kinds: voltage drop and power, with editable supplies, loads and ratings, contacts you can open, and warnings for overloaded parts
- Bill of materials from a schematic with one line in the chat, with the footprint of each part; refine a schematic by chatting with the AI
- Add-ons area to turn features on and off, a single material picker, grouped object menus and new objects placed in free space
- The app follows the language of the device, with English as the fallback
- Fixed the schematic panel stretching when the zoom changes

_En español: De boceto a mano a esquema, diseño eléctrico industrial y simulación de circuitos_

- De boceto a esquema: dibuja un circuito a mano y la IA arma un esquema electrónico o eléctrico industrial con piezas reales, cableado terminal a terminal, junto al boceto y unido a él por un conector que puedes cortar
- Dos tipos de esquema, cada uno su propio add-on: electrónico (símbolos de KiCad, unos 23.000, con huellas de placa) y eléctrico industrial (símbolos IEC/EN 60617, unos 6.400, con clasificación y datos técnicos ETIM 10.0)
- Piezas industriales: bornes marcados según IEC 60947 a partir de los polos de ETIM, y la IA busca las piezas en la biblioteca real mediante un servidor MCP en lugar de adivinar
- Un único panel de edición con pestañas Properties, Components y Simulate: búsqueda en la biblioteca, reemplazar un símbolo, buscar alternativas, selector de huellas para piezas electrónicas
- Simulación de circuitos en la pestaña Simulate para los dos tipos: caída de tensión y potencia, con fuentes, cargas y valores nominales editables, contactos que se pueden abrir y avisos de piezas sobrecargadas
- Lista de materiales de un esquema con una línea en el chat, con la huella de cada pieza; refinar un esquema conversando con la IA
- Área de add-ons para activar y desactivar funciones, un selector de materiales único, menús de objeto agrupados y objetos nuevos en un espacio libre
- La app sigue el idioma del dispositivo, con inglés como alternativa
- Se arregló que el panel del esquema se estirara al cambiar el zoom

- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.4.4), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.4.4)

### 0.4.2 · 2026-11-10 · Drawing check against the 3D part, and a design simulator with a wind tunnel
- Drawing check: compare a PDF drawing with its STEP part. The AI reads each dimension off the drawing and Ensemble measures the real geometry; every dimension gets a verdict (OK, out of tolerance, review, not checked) and can be shown on the 3D part with its label and dimension line
- Design simulation (Analyze part, Simulate tab): static load and own weight with a safety factor, vibration modes, heat, impact against a rigid wall with permanent deformation, and a wind tunnel
- Results are painted on the part and the part is drawn deformed; vibration and impact are animated
- Wind tunnel: drag and lift, Cd and Cl, pressure on every face, and animated air particles that follow the real air speed; air or water, in any direction
- Impact is shown at real scale, steel hardens only up to a limit and then tears, and the result warns when the calculation ended before the part came to rest
- Thin sheets and open surfaces now block the air in the wind tunnel
- The 3D labels of a drawing check show only for the selected dimension

_En español: Chequeo del plano contra el 3D y un simulador de diseño con túnel de viento_

- Chequeo del plano: compara un plano PDF con su pieza STEP. La IA lee cada cota del plano y Ensemble mide la geometría real; cada cota recibe un veredicto (OK, fuera de tolerancia, revisar, sin comprobar) y se puede mostrar sobre la pieza 3D con su etiqueta y su línea de cota
- Simulación de diseño (Analizar pieza, pestaña Simular): carga estática y peso propio con factor de seguridad, modos de vibración, calor, impacto contra una pared rígida con deformación permanente y un túnel de viento
- Los resultados se pintan sobre la pieza y la pieza se dibuja deformada; la vibración y el impacto se animan
- Túnel de viento: arrastre y sustentación, Cd y Cl, presión en cada cara y partículas de aire animadas que siguen la velocidad real; aire o agua, en cualquier dirección
- El impacto se muestra a escala real, el acero se endurece solo hasta un límite y luego se desgarra, y el resultado avisa si el cálculo terminó antes de que la pieza se detuviera
- Las chapas finas y las superficies abiertas ahora frenan el aire en el túnel de viento
- Las etiquetas 3D del chequeo del plano se ven solo para la cota elegida

- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.4.2), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.4.2), [Android and Quest](https://github.com/gabgiani/ensemble-downloads/releases/tag/android-v0.4.2)

### 0.4.1 · 2026-11-10 · Merge 3D models into one scene, exploded view, material checks and a camera you place
- Merge models: drop one 3D card onto another (or use the Scene tab) to bring several STEP files into the same real 3D space, for example a board inside its enclosure
- Move each model on its own with 3 axis arrows and a free-move dot, plus exact position and rotation, and shortcuts to center inside, sit on top or place beside
- A camera you place in the scene, like in Unity: click a point, move it with its 3 axes, aim it with a handle or with turn and tilt, choose the field of view, and look through it to check the fit from inside
- Animated exploded view of assemblies (all directions or along X, Y or Z), shown in 3D on every platform including Meta Quest
- Material per part, mass and center of gravity, and quick strength checks (cantilever, tension, supported plate) painted on the part
- Right-click a part in 3D: hide, make transparent, show hidden parts or take it to another view
- Meta Quest: CAD analysis in VR with the exploded view, center of gravity, material and the cut shown in the headset
- Android: on-screen keyboard fix
- Web version: access request form with company and role required

_En español: Fusionar modelos 3D en una escena, despiece, comprobaciones de material y una cámara que tú colocas_

- Fusionar modelos: suelta una tarjeta 3D sobre otra (o usa la pestaña Escena) para traer varios STEP al mismo espacio 3D real, por ejemplo una placa dentro de su caja
- Mueve cada modelo por separado con 3 flechas de ejes y un punto de movimiento libre, con posición y giro exactos, y atajos para centrar adentro, apoyar encima o poner al lado
- Una cámara que colocas en la escena, como en Unity: haz clic en un punto, muévela con sus 3 ejes, apúntala con una manija o con giro e inclinación, elige el ángulo de visión y mira a través de ella para revisar el ajuste desde adentro
- Despiece animado de ensambles (en todas las direcciones o a lo largo de X, Y o Z), visible en 3D en todas las plataformas, incluido Meta Quest
- Material por pieza, masa y centro de gravedad, y comprobaciones rápidas de resistencia (voladizo, tracción, placa apoyada) pintadas sobre la pieza
- Clic derecho sobre una pieza en 3D: ocultar, hacer transparente, mostrar lo oculto o llevarla a otra vista
- Meta Quest: análisis CAD en VR con el despiece, el centro de gravedad, el material y el corte dentro del visor
- Android: arreglo del teclado en pantalla
- Versión web: formulario de solicitud de acceso con empresa y rol obligatorios

- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.4.1), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.4.1), [Android and Quest](https://github.com/gabgiani/ensemble-downloads/releases/tag/android-v0.4.1)

### 0.4.0 · 2026-11-09 · Workspace tabs, live Showcase, web version, wireframe mesh and a richer VR
- Workspace tabs: several workspaces open at once (this device, DAFONET or your own server), one tap to switch, each remembers its zoom and position
- Split screen (beta): two workspaces side by side on iPad and Mac
- Live Showcase: the presenter turns the 3D part in the air with no menus, and everyone sees the turn, color, cut, mode and analysis highlight in real time
- Live Showcase: a drawing bar for the presenter (pen, marker, eraser, arrow, text, pins and labels); at the end, save the presentation as a new dated Showcase, add the annotations to the workspace, or discard them
- Apple Pencil: only the pencil draws and the finger navigates; the annotation bar sits next to the toolbar; pen, marker and eraser stay active; smoother strokes
- 3D viewer: mesh mode like a wireframe (thin lines, no fill, see-through) with finer tessellation
- 3D viewer: section cuts can show the cut-away part as a mesh, with a color of your choice and line intensity
- 3D viewer: select parts of an assembly and send them to a new view or to another view, with a soft connection line between linked views; a Views submenu; A3 sheets respect the chosen “up” orientation of the part (STEP and SolidWorks)
- Groups: their own frame to scale a group of strokes proportionally; copying or moving to another workspace keeps the sketch and the frame contents
- A chip shows where a workspace lives (this device, DAFONET or my server); discreet tooltips on buttons (cursor, or press and hold on iPad); the inspector no longer opens by itself
- Meta Quest: keyboard with symbols and @, click with A/X as well as the trigger, a built-in controls guide (“?”), and move, bring closer, widen and curve the canvas around you
- Meta Quest: floating parts follow changes on the shared canvas; in a Showcase you see the 3D part in the air and walk around it (read-only); section cut with mesh in VR
- Web version in the browser, with nothing to install: access by invitation only (request it with a form; the administrator approves it)
- Android: phone and tablet (APK), Quest panel and VR viewer

_En español: Pestañas de workspaces, Showcase en vivo, versión web, malla tipo wireframe y una VR más completa_

- Pestañas de workspaces: varios abiertos a la vez (este dispositivo, DAFONET o un servidor propio), un toque para cambiar, cada uno recuerda su zoom y posición
- Pantalla dividida (beta): dos workspaces lado a lado en iPad y Mac
- Showcase en vivo: quien presenta rota la pieza 3D en el aire sin menús, y todos ven en tiempo real el giro, el color, el corte, el modo y el resaltado del análisis
- Showcase en vivo: barra de dibujo para el presentador (lápiz, marcador, goma, flecha, texto, pins y etiquetas); al terminar, guardar la presentación como un Showcase nuevo con la fecha, agregar lo anotado al workspace o descartarlo
- Apple Pencil: solo el lápiz dibuja y el dedo navega; la barra de anotación va pegada a la barra de herramientas; lápiz, marcador y goma se quedan activos; trazos más suaves
- Visor 3D: modo malla como un wireframe (líneas finas, sin relleno, se ve a través) con teselación más fina
- Visor 3D: el corte puede mostrar la parte cortada como malla, con el color que elijas e intensidad de línea
- Visor 3D: selección de piezas de un ensamble para enviarlas a una vista nueva o a otra vista, con una línea de conexión suave entre vistas enlazadas; submenú Views; las hojas A3 respetan la orientación «arriba» elegida de la pieza (STEP y SolidWorks)
- Grupos: marco propio para escalar proporcionalmente un grupo de trazos; copiar o mover a otro workspace conserva el boceto y el contenido del marco
- Un chip indica dónde vive el workspace (este dispositivo, DAFONET o mi servidor); etiquetas discretas por botón (cursor, o mantener pulsado en iPad); el inspector ya no se abre solo
- Meta Quest: teclado con símbolos y @, clic con A/X además del gatillo, guía de controles integrada («?») y poder mover, acercar, ensanchar y curvar el lienzo alrededor de ti
- Meta Quest: las piezas flotantes siguen los cambios del lienzo compartido; en un Showcase ves la pieza 3D en el aire y caminas a su alrededor (solo lectura); corte con malla en VR
- Versión web en el navegador, sin instalar nada: acceso solo por invitación (se pide con un formulario y el administrador lo aprueba)
- Android: teléfono y tablet (APK), panel Quest y visor VR

- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.4.0), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.4.0), [Android and Quest](https://github.com/gabgiani/ensemble-downloads/releases/tag/android-v0.4.0)

### 0.3.0 · 2026-11-08 · SolidWorks and AutoCAD files, free rotation, cleaner large models
- Opens SolidWorks parts (.SLDPRT) and complete assemblies (.SLDASM) straight from the file, with their structure and part names
- Opens AutoCAD DWG drawings (2013 format) as vector drawing cards, and the AI can propose a 3D model from them
- 3D viewer: you can now rotate all the way over and under a part, with no limit on the vertical turn
- 3D viewer: fixed the speckled, outlined patches that appeared on large assemblies when zoomed out (depth precision)
- Analysis works on SolidWorks parts and assemblies; interference check and exact comparison still need a STEP
- New builds: Meta Quest (VR viewer and the full app as a panel) and Android phones and tablets (sideloaded APK)
- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.3.0), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.3.0), [Android and Quest](https://github.com/gabgiani/ensemble-downloads/releases/tag/android-v0.3.0)

### 0.2.6 · 2026-11-07 · Server and Mac app update
- Ensemble Server 0.2.6 for macOS (Apple silicon) and Ensemble for Mac 0.2.6, signed and notarized
- Downloads: [Server](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.2.6), [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.2.6)

### 0.2.5 · 2026-11-07 · First release of the Mac app
- Ensemble for Mac 0.2.5 (Apple silicon, macOS 13 or later), signed with Developer ID and notarized
- Downloads: [Mac app](https://github.com/gabgiani/ensemble-downloads/releases/tag/app-mac-v0.2.5)

### 0.2.4 · 2026-11-06 · Server for macOS and Windows installer
- Ensemble Server 0.2.4 for macOS and the signed Windows installer
- Downloads: [Server and Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.2.4)

### 0.2.1 · 2026-11-06 · First signed Windows installer
- Ensemble by DAFO 0.2.1 for Windows (x64), signed installer
- Downloads: [Windows](https://github.com/gabgiani/ensemble-downloads/releases/tag/v0.2.1)

## Checking a download

Every file has a SHA-256 in its manifest (`*.json` in this repository) or in the release. On a Mac or Linux: `shasum -a 256 file`. On Windows: `Get-FileHash file`.
