# 🔍 Módulo: Escaneo y Guardado de Frecuencias — Baofeng DM-32UV

**Autor:** HJ3RAW - William Rozo Álvarez  
**Fuente:** Manual oficial `dm32uv.pdf` (secciones Scan / VFO / Scan List / New Channel / CPS)  
**Fecha:** 2025-11-03  
**Licencia:** CC BY-NC-SA 4.0

---

## Resumen rápido
Este módulo explica cómo **escanear frecuencias (VFO/Channel)**, **crear/editar listas de escaneo (Scan Lists)**, **guardar frecuencias escaneadas como canales** y **programar listas de escaneo desde el PC (CPS)** en el Baofeng DM-32UV.

Las referencias clave del manual aparecen en las notas al final. Ejemplos paso a paso y rutas de menú incluidas.

---

## 1) Encender el escaneo (Scan)
Hay tres maneras de activar el escaneo en el DM-32UV:
- Pulsando la tecla preprogramada **[Scan]** (modo canal o VFO).  
- Si el canal tiene **Auto Scan** configurado y se cambia a ese canal, el radio empezará a escanear automáticamente.  
- Desde el menú: `Menu → Scan → Scan switch` para encender/apagar la función de escaneo. fileciteturn8file1L11-L15

Durante el escaneo puedes:
- Pulsar ▲ para avanzar por los incrementos del paso de frecuencia.
- Pulsar ▼ para retroceder por los incrementos del paso de frecuencia.
- Al detenerse en una frecuencia activa, mantén **PTT** para transmitir (si corresponde). fileciteturn8file0L14-L18

---

## 2) Escanear en modo VFO (frecuencias manuales)
1. Mantén presionada la tecla correspondiente para entrar en **VFO mode** y escribe la frecuencia inicial con el teclado numérico. fileciteturn8file0L9-L10  
2. Ajusta el **VFO Scan Range** para limitar la búsqueda (`Menu → Scan → VFO ScanRange (V)`), por ejemplo `144000000`–`146000000` para VHF. Introduce los dígitos tal como pide el menú. fileciteturn8file2L41-L44  
3. Selecciona el **VFO Scan Mode** (TO / CO / SE):  
   - **TO (Time Scan):** para detenerse en una señal y reanudar tras 5 s.  
   - **CO (Carrier Scan):** detenerse mientras haya señal; reanuda 2 s después de perderla.  
   - **SE (Search Scan):** detener el escaneo cuando detecta señal y terminar. fileciteturn8file2L21-L26

---

## 3) Escanear subtonos (CTCSS / DCS) y guardarlos
- Para buscar subtonos utilice `Menu → Scan → Scan CTCSS` o `Menu → Scan → Scan DCS`. El radio empezará a barrer los subtonos y avisará cuando encuentre un código válido. fileciteturn8file2L27-L37  
- Si deseas **guardar** el subtono detectado en el canal/frecuencia activa: `Menu → Scan → Scan Memory` y escoger si se almacena como **TX CTCSS/DCS**, **RX CTCSS/DCS** o **All (TX+RX)**. Solo funciona cuando el radio ha detectado y “se queda” en un código válido; entonces confirma con la tecla para memorizar. fileciteturn8file3L23-L33

**Atención:** guardar CTCSS/DCS reemplazará la configuración actual del canal con el nuevo subtono guardado. fileciteturn8file3L25-L30

---

## 4) Crear o editar una Scan List en el radio
1. `Menu → Scan → Scan List` → selecciona la lista que desees (el radio soporta varias listas). fileciteturn8file1L21-L26  
2. Dentro de la lista puedes: **Apply** (activar), **Edit/View List**, **Add Chan** (añadir canales desde la lista de canales existentes), **Edit Name** y **Set Priority Channel**. fileciteturn8file1L25-L33  
3. En **Edit/View List** puedes marcar canales para borrar o ajustar el orden. Puedes definir hasta **2 canales prioritarios** (P1 / P2) que recibirán un escaneo más frecuente. fileciteturn8file1L31-L35  
4. Para añadir un canal mientras estás viendo la lista: `Add Chan` → te llevará al listado de canales programados; selecciona y confirma para incluirlo. fileciteturn8file1L29-L31

**Nota:** No se puede borrar el primer canal (posición 1) de una lista desde el menú. fileciteturn8file1L36-L37

---

## 5) Guardar una frecuencia encontrada como **Nuevo Canal** (desde VFO → Channel)
Si durante el escaneo o en VFO detectas una frecuencia que quieres conservar como canal programado, sigue estos pasos **en el radio**:

1. Cambia a **VFO mode** (mantén la tecla indicada) e introduce la **RX frequency** encontrada. fileciteturn8file0L9-L10  
2. `Menu → New Chan` (o `Menu → Channel → New Chan`) → selecciona el **Channel Type** (Analog / Digital / A+D TX A / D+A TX D). fileciteturn9file4L3-L9  
3. Edita el **Channel Name** si lo deseas (usa `#` para cambiar método de entrada). fileciteturn9file4L6-L9  
4. Introduce la **TX frequency** si procede y confirma para **Guardar** (la opción guarda el canal añadido). fileciteturn9file4L8-L9  
5. Para añadir ese canal a una **Zone**: `Menu → Zone → Select a Zone` → `Add Channel` → seleccionar el nuevo canal → confirmar → aparecerá “Add Success”. fileciteturn9file0L10-L13

> Consejo práctico: después de crear el nuevo canal, entra a `Settings → Channel Set` para configurar parámetros adicionales (Color Code, Time Slot, Contact, CTCSS/DCS, VOX, Power, Step, etc.). fileciteturn9file0L15-L20

---

## 6) Crear y gestionar Scan Lists desde el PC (CPS)
- En el **CPS (programming software)** puedes crear hasta **32 scan lists** y programarlas en el radio. Esto resulta más rápido cuando tienes muchas listas o deseas replicar configuraciones entre radios. Una vez terminada la edición en CPS, **Write** la configuración al radio. fileciteturn8file1L9-L10
- Ruta típica en CPS: `Public → Scan list` (crear/editar) → luego `Write` al equipo. fileciteturn8file1L9-L10
- Al leer el radio con CPS, guarda el código (Codeplug) en tu disco antes de editar; cuando termines, escribe el archivo al equipo. fileciteturn9file4L27-L34

---

## 7) Flujo recomendado de trabajo (paso a paso ideal)
1. **Leer** el radio con CPS y guardar el codeplug. fileciteturn9file4L27-L34  
2. Crear/editar **Scan Lists** en CPS (Public → Scan List) y asignar canales. fileciteturn8file1L9-L10  
3. Escribir (Write) el codeplug al radio. fileciteturn9file4L33-L34  
4. En el campo: si detectas frecuencias útiles con **VFO Scan**, crea el canal nuevo (`Menu → New Chan`) y añádelo a la zona/scan list, o guárdalo en CPS luego de leer el radio. fileciteturn8file0L9-L11fileciteturn9file4L3-L9

---

## 8) Casos especiales y advertencias
- **Auto Scan vs. Scan List:** Auto Scan en canal activará escaneo automáticamente cuando entres en ese canal; la funcionalidad de Scan List solo funciona en *Channel Mode* (no en VFO) y depende de los canales programados en la memoria. fileciteturn8file1L9-L15
- **CTCSS/DCS guardado:** si guardas un subtono detectado, reemplazarás el ajuste anterior del canal; haz copia antes en CPS si es importante. fileciteturn8file3L23-L33
- **VFO Scan Range:** asegúrate de limitar el rango para evitar barridos muy amplios que tarden demasiado. fileciteturn8file2L41-L44
- **Scan list limit:** el CPS soporta hasta 32 Scan Lists; organiza por prioridad. fileciteturn8file1L9-L10

---

### Referencias (manual)
- Guía de Scan y Scan List — `dm32uv.pdf` (sección 7.2 / 7.3). fileciteturn8file1L21-L31  
- VFO Scan Range / VFO Scan Modes — `dm32uv.pdf`. fileciteturn8file2L21-L26  
- Scan CTCSS / Scan DCS / Scan Memory — `dm32uv.pdf`. fileciteturn8file3L27-L33  
- New Channel & Channel Set — `dm32uv.pdf`. fileciteturn9file4L3-L9  
- Zone / Add Channel — `dm32uv.pdf`. fileciteturn9file0L10-L13

---

