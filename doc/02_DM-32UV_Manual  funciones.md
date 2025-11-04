# 📘 Manual Técnico del Radio Baofeng DM-32UV  
**Versión:** v2 — Estructura de Menús, Funciones y Diferencias de Modo  
**Autor:** HJ3RAW - William Rozo Álvarez  
**Licencia:** CC BY-NC-SA 4.0  
**Fecha:** 2025-11-03  

---

# 🌦️ Módulo: Other Func – Weather Alarm (Baofeng DM-32UV)

## 🎯 Propósito
La opción **Weather Alarm** activa la función de **alerta meteorológica automática (NOAA Weather Alert)**.  
Cuando está activada, el radio **escucha periódicamente las frecuencias NOAA preestablecidas** (entre 162.400 – 162.550 MHz en EE. UU. y Canadá) y **emite una alarma sonora** si detecta una señal de emergencia climática.

**Ruta en el menú:**  
`Settings → Radio Settings → Other Func → Weather Alarm`

---

## ⚙️ Descripción de opciones

| Opción  | Significado        | Comportamiento                                                                                                                                         |
| :------ | :----------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **OFF** | Alerta desactivada | El radio no monitorea ni reacciona ante transmisiones NOAA. (Recomendado fuera de EE. UU./Canadá).                                                     |
| **ON**  | Alerta activada    | El radio escanea las frecuencias meteorológicas y suena una alarma si se detecta una transmisión de alerta (tormentas, huracanes, inundaciones, etc.). |

---

## 🌍 Notas de uso internacional
- En **Colombia y la mayoría de países de Latinoamérica**, este sistema NOAA **no transmite** alertas, por lo tanto, dejarlo **en OFF** evita consumo innecesario de batería.  
- En **EE. UU., Canadá y parte del Caribe**, sí es funcional si el firmware incluye la tabla de frecuencias **NOAA WX1-WX7**.

---

## 🔋 Recomendaciones
- Activar solo si se utiliza en zonas con cobertura meteorológica NOAA.  
- Si el radio se queda “congelado” o suena sin motivo, desactiva **Weather Alarm = OFF**.  
- Esta función **no sustituye** el monitoreo por canales convencionales de emergencia o protección civil.

---
# 🔊 Módulo: Other Func – TBST Sel (Baofeng DM-32UV)

## 🎯 Propósito
La función **TBST Sel** (Tone Burst Select) permite emitir un **tono de acceso rápido a repetidores analógicos** que requieren una señal de audio corta (burst tone) al inicio de la transmisión.  
Este tono es diferente del **CTCSS/DCS** continuo; el burst es un **pulso breve de 1000 a 2100 Hz** que “despierta” o habilita algunos repetidores antiguos antes de transmitir voz.

**Ruta en el menú:**  
`Settings → Radio Settings → Other Func → TBST Sel`

---

## ⚙️ Descripción de opciones

| Opción | Frecuencia del tono | Uso típico |
|:--------|:--------------------|:------------|
| **1000 Hz** | Tono de baja frecuencia | Usado en algunos equipos comerciales antiguos. |
| **1450 Hz** | Tono europeo clásico | Compatible con ciertos repetidores PMR. |
| **1750 Hz** | **Estándar más común en Europa y Latinoamérica.** Ideal para la mayoría de repetidores VHF analógicos que usan “tone burst”. |
| **2100 Hz** | Tono de alta frecuencia | Raramente usado; reservado a algunos sistemas personalizados. |

---

## 🔧 Cómo funciona
Cuando se presiona **PTT**, el radio puede enviar automáticamente (según configuración) un pulso corto del tono seleccionado para abrir el repetidor.  
Este tono **no es audible por los usuarios** si el radio tiene filtrado activo, y **no afecta transmisiones digitales (DMR)**.

---

## 🌎 En Colombia y Latinoamérica
- La mayoría de **repetidores modernos usan CTCSS o DCS**, no TBST.  
- Sin embargo, algunos **repetidores analógicos de radioaficionados** (particularmente en VHF) **aún aceptan burst de 1750 Hz** para activarse.  
- Si tu repetidor no responde con CTCSS, puedes intentar **activar TBST Sel = 1750 Hz** y probar.

---

## 💡 Recomendaciones
- Dejar **1750 Hz** como valor por defecto si usas bandas de radioaficionado.  
- Si transmites en DMR o canales comerciales, **desactiva la función TBST o ignórala**, ya que no tiene efecto en digital.  
- No confundir **TBST** con **CTCSS**: el primero es un pulso breve; el segundo es una señal continua.

---
# 🔈 Módulo: Other Func – Tail (Baofeng DM-32UV)

## 🎯 Propósito
La función **Tail** sirve para **eliminar o reducir el ruido de cola (squelch tail)** que aparece al final de una transmisión analógica, especialmente cuando se usan **repetidores** o **CTCSS/DCS**.  
Este ruido es causado por la pequeña diferencia de tiempo entre la apertura y el cierre del transmisor y el receptor del repetidor.

**Ruta en el menú:**  
`Settings → Radio Settings → Other Func → Tail`

---

## ⚙️ Descripción de opciones

| Opción | Descripción técnica | Uso recomendado |
|:--------|:--------------------|:----------------|
| **Off** | Desactiva la supresión de ruido de cola. Podrás oír un breve chasquido al final de cada transmisión. | Si deseas oír todo el audio, incluso el final de la portadora. |
| **55 Hz** | Inserta un tono subaudible de 55 Hz al finalizar la transmisión, usado para "enmudecer" receptores con tail eliminator. | Compatibilidad con algunos sistemas comerciales. |
| **120°** | Aplica una **fase de cierre retardada** (120°) para eliminar parcialmente el ruido de cola. | Uso general en repetidores VHF/UHF locales. |
| **180°** | **Modo más completo de cancelación de cola.** Introduce un retardo de fase de 180° en el tono de cierre para eliminar totalmente el chasquido. | Recomendado para repetidores modernos y redes analógicas de radioaficionados. |

---

## 📡 Explicación técnica
- En transmisiones analógicas con **CTCSS** o **DCS**, el receptor usa la presencia del tono para mantener abierto el audio.  
- Cuando el transmisor corta repentinamente el tono, se escucha un “pop” o chasquido.  
- La opción **Tail 120° o 180°** hace que el transmisor envíe una **señal de fase invertida al final de la transmisión**, permitiendo al receptor cerrarse suavemente sin ruido audible.

---

## 🌍 En Colombia y Latinoamérica
- La mayoría de los repetidores de radioaficionados que usan **CTCSS** funcionan mejor con **Tail = 180°**.  
- Si usas canales simplex (radio a radio) sin tonos, puedes dejar **Tail = Off**.  
- En entornos mixtos (comerciales y amateur), **Tail = 120°** es una opción equilibrada.

---

## 💡 Recomendaciones
- Si escuchas “chasquidos” después de cada transmisión, cambia **Tail = 180°**.  
- En comunicación directa sin repetidores, desactiva esta función.  
- Esta opción **no afecta transmisiones digitales (DMR)**.

---

# 💾 Módulo: Activar Modo Digital (DMR) en VFO y Canales – Baofeng DM-32UV

## 🎯 Propósito
Permitir al usuario cambiar entre **modo analógico (ANA)** y **modo digital (DMR)** en el **Baofeng DM-32UV**, tanto desde el teclado (VFO) como mediante el software **CPS**.

---

## ⚙️ Contexto técnico

El DM-32UV es un transceptor **mixto (analógico + DMR)**.  
Por defecto, cuando se enciende o se usa el **modo VFO**, el equipo **opera en modo analógico (ANA)**, incluso si tiene firmware digital.  
El cambio a digital debe hacerse manualmente o programando un canal.

---

## 🔹 Método 1 — Activar modo digital desde el equipo

**Ruta de menú:**
`Menu → Channel Set → Channel Type`

1. Selecciona **Channel Type → Digital**.  
2. Aparecerá en pantalla el indicador **DIG** (en rojo, arriba a la derecha).  
3. Configura los parámetros digitales:
   - **Color Code (CC):** entre 1 y 15 (por defecto 1).  
   - **Time Slot (TS):** 1 o 2 según la red o repetidor.  
   - **Contact:** TG (Talk Group) o contacto digital asignado.  
4. Guarda el canal o confirma con **OK**.

📍 **Nota:**  
En modo **VFO**, algunos firmwares (como v1.45) **no permiten guardar el modo digital**.  
El cambio se pierde al apagar o cambiar de canal.  
Para que persista, es necesario **guardar el canal** en memoria.

---

## 🔹 Método 2 — Activar modo digital con el software CPS

1. Conecta el radio mediante el cable de programación USB.  
2. Abre el software **CPS V1.45 o V1.47**.  
3. En la pestaña **Channel Information**:
   - Configura **Channel Type = Digital**.  
   - Asigna **frecuencias RX/TX** (por ejemplo 438.1000 / 430.5000 MHz).  
   - Establece **Color Code**, **Slot (1 o 2)** y **Contact Name**.  
4. Haz clic en **Write Data to Radio**.  
5. Selecciona el canal desde el menú del radio: verás **DIGITAL** en pantalla.

---

## 🧩 Limitaciones del modo VFO

| Función | Analógico (ANA) | Digital (DMR) |
|:--------|:----------------|:---------------|
| Ingreso manual de frecuencia | ✅ Sí | ⚠️ Limitado |
| Transmisión directa | ✅ Sí | ❌ Requiere canal |
| Configurar TG/Contact | ❌ No aplica | ✅ Necesario |
| Cambio dinámico desde menú | ✅ Total | ⚠️ Parcial (según firmware) |

---

## 🔍 Verificación visual

| Indicador en pantalla | Significado |
|:-----------------------|:-------------|
| **ANA** (rojo) | Canal o VFO en modo analógico. |
| **DIG** (rojo) | Canal en modo digital DMR. |
| **Color Code y TG visibles** | Modo digital correctamente configurado. |

---

## 🧠 Recomendaciones prácticas

- Usa **CPS** para todos los canales digitales (más estable).  
- En **VFO**, puedes probar digital momentáneamente, pero no se guardará.  
- Configura **Radio ID** en CPS antes de transmitir en DMR.  
- Para redes **BrandMeister Colombia**, usa Color Code 1, Slot 1 o 2, y los TG regionales.

---
# 📘 Manual Técnico Avanzado – Baofeng DM-32UV
### Por **HJ3RAW – William Rozo Álvarez**
Licencia: CC BY-NC-SA 4.0 | Versión: 2025.11

---

## ⚙️ Módulo: Power Save
### Propósito
Reduce el consumo de batería controlando los ciclos de recepción.  
- **Save Off:** Desactiva ahorro de energía.  
- **Save 1:1 / 1:2 / 1:4:** Define cuántos ciclos de reposo ejecuta el receptor entre escaneos.  
  - `1:1` = ahorro mínimo, respuesta más rápida.  
  - `1:4` = ahorro máximo, pero respuesta más lenta.

💡 Recomendación: usar `Save 1:2` como balance entre autonomía y tiempo de respuesta.

---

## ⚙️ Módulo: Freq Step
### Propósito
Controla el incremento o salto de frecuencia en modo VFO.  
- **Valores:** 2.5 / 5 / 6.25 / 10 / 12.5 / 25 / 50 / 100 kHz  
- **Uso:** Si un repetidor trabaja en 146.520 y otro en 146.525, el paso de 5 kHz es el adecuado.  
  Para frecuencias comerciales o PMR, se usan pasos de 12.5 o 25 kHz.

---

## ⚙️ Módulo: TBST Sel (Tone Burst Select)
Permite enviar un tono de acceso (burst tone) para abrir repetidores analógicos antiguos.

| Opción | Frecuencia | Uso |
|---------|-------------|-----|
| 1000 Hz | Baja | Equipos antiguos |
| 1450 Hz | Estándar europeo | PMR |
| 1750 Hz | ✅ Más común en Latinoamérica | Repetidores VHF |
| 2100 Hz | Alta | Sistemas personalizados |

💡 En Colombia: usar 1750 Hz si el repetidor no responde a CTCSS.

---

## ⚙️ Módulo: Tail
Reduce o elimina el “chasquido” al final de una transmisión.

| Opción | Descripción | Uso |
|---------|--------------|-----|
| Off | No corrige ruido | Comunicación simplex |
| 55Hz | Inserta tono subaudible | Compatibilidad comercial |
| 120° | Fase parcial | Repetidores VHF locales |
| 180° | ✅ Cancelación total | Repetidores modernos |

---

## ⚙️ Módulo: Dual Watch
Permite escuchar o alternar entre dos canales o frecuencias.

| Modo | Descripción | Comportamiento |
|------|--------------|----------------|
| Single Mode | Solo canal activo | Ahorra batería |
| Double Wait | Escucha ambos canales | Puede perder breves llamadas |
| Single Wait | ✅ Recomendado | Monitorea dos, transmite en A |

---

## ⚙️ Módulo: Weather Alarm
Función NOAA para recibir alertas meteorológicas (solo en EE. UU. / Canadá).  
En Colombia y la mayoría de países latinoamericanos **no funciona**, pues IDEAM y UNGRD no usan este sistema.

🔧 Recomendado: **OFF** (evita consumo innecesario).

---

## ⚙️ Módulo: Activar Modo Digital (DMR)
Permite cambiar entre modo analógico y digital.

### Método 1 — Desde el radio
1. `Menu → Channel Set → Channel Type → Digital`
2. Aparecerá “DIG” en pantalla.  
3. Configurar: **Color Code**, **Slot**, **Contact**.

### Método 2 — Desde CPS
1. Abrir **CPS V1.45/V1.47**  
2. Configurar **Channel Type = Digital**  
3. Asignar **frecuencia RX/TX**, **Color Code**, **Slot**, **Contact Name**  
4. Grabar en el radio con **Write Data**.

💡 En VFO no se puede guardar modo digital; usar canales programados.

---

## ⚙️ Módulo: Escaneo y Guardado de Frecuencias
### Escaneo manual
1. Desde la pantalla principal presionar **[SCAN]** o asignar función P1/P2.  
2. El radio buscará actividad en el rango activo.  
3. Al encontrar señal, detener el escaneo con **OK**.

### Guardar frecuencia
1. Con el escaneo detenido, mantener presionado **Menu → Save → Channel Number**.  
2. Confirmar con **OK** para almacenar.

### Tipos de escaneo
- **VFO Scan:** Escanea un rango de frecuencias libre.  
- **Channel Scan:** Escanea canales guardados.  
- **CTCSS/DCS Scan:** Detecta tonos de subaudio de una señal recibida.

---
# 🔍 Módulo: VFO Scan Mode – (TO / CO / SE)
### Ruta: `Menu → Radio Settings → VFO Scan Mode`

## 🎯 Propósito
Determina cómo actúa el escáner del radio cuando encuentra una señal activa durante el escaneo de frecuencias o canales.

---

## ⚙️ Descripción de modos

| Modo | Nombre completo | Comportamiento | Uso recomendado |
|------|------------------|----------------|-----------------|
| **TO** | *Time Operation* | El escaneo **se detiene temporalmente** cuando se detecta una señal y, tras unos segundos (≈5 s), continúa automáticamente. | Ideal para buscar actividad general sin intervención manual. |
| **CO** | *Carrier Operation* | El escaneo **se detiene mientras la portadora (señal)** esté activa y **reanuda cuando desaparece**. | ✅ Recomendado para monitoreo continuo de frecuencias activas. |
| **SE** | *Search Operation* | El escaneo **se detiene permanentemente** cuando detecta una señal, hasta que el usuario pulse **SCAN o EXIT** para continuar. | Útil para identificar frecuencias específicas y analizarlas. |

---

## 💡 Ejemplo práctico

- Si estás explorando bandas locales (VHF/UHF) y solo quieres detectar actividad: usa **TO**.  
- Si deseas permanecer escuchando mientras haya conversación: usa **CO**.  
- Si buscas una frecuencia desconocida y quieres anotar su valor exacto: usa **SE**.

---

## ⚙️ Recomendación general
Para radioaficionados y servicios locales, el modo **CO** ofrece el mejor equilibrio entre control y autonomía.  
Si escaneas frecuencias muy activas (por ejemplo, PMR o seguridad privada), **TO** evita bloqueos innecesarios.


---

## 🪪 Créditos y licencia

**Autor:** HJ3RAW - William Rozo Álvarez  
**Licencia:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)  
**Repositorio sugerido:**  
`https://github.com/HJ3RAW/DM32UV_Manual`

> Se permite copiar, adaptar y compartir con atribución y uso no comercial.  2025

---

