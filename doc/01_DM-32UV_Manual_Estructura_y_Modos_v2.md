# 📘 Manual Técnico del Radio Baofeng DM-32UV  
**Versión:** v2 — Estructura de Menús, Funciones y Diferencias de Modo  
**Autor:** HJ3RAW - William Rozo Álvarez  
**Licencia:** CC BY-NC-SA 4.0  
**Fecha:** 2025-11-03  

---

## 📋 Introducción
El **Baofeng DM-32UV** es un transceptor **dual band (VHF/UHF)** con **modos analógico (ANA)** y **digital (DMR Tier II)**.  
Este documento detalla su estructura jerárquica de menús, la función de cada parámetro y las diferencias operativas según el modo activo.

---

## 🌳 Estructura general del menú

```
Settings
├── 1. Radio Settings
│   ├── Voice Func
│   ├── Key Func
│   ├── Display Func
│   └── Other Func
├── 2. Channel Set
│   ├── TX/RX Freq
│   ├── Bandwidth
│   ├── Power Level
│   ├── Freq Step
│   ├── TBST Sel
│   └── CTC/DCS
├── 3. Device Info
│   ├── Model
│   ├── Firmware
│   └── Serial No.
├── 4. DTMF
│   ├── Code Set
│   ├── Auto Resp
│   └── Delay Time
├── 5. BDC1200
│   ├── Encode/Decode
│   └── ANI ID
├── 6. Two-Tone
│   ├── Encode
│   └── Decode
└── 7. Five-Tone
    ├── Encode
    └── Decode
```

---

## 🟢 Diferencias entre modos ANA y DIG

| Característica | Modo ANA | Modo DIG |
|----------------|-----------|-----------|
| Tipo de modulación | FM análoga | DMR digital TDMA |
| Identificación | Sin ID, solo frecuencia | ID DMR (Radio ID, Color Code, Slot, TG) |
| Subtonos | CTCSS / DCS | Color Code / TG / Slot |
| Funciones exclusivas | TBST Sel, Freq Step amplio | Contactos, TalkGroups, Private Call |
| Calidad de voz | Sujeta a ruido | Nítida y comprimida (AMBE+2) |
| Escaneo | Banda abierta | Solo canales programados DMR |
| Interoperabilidad | Radios FM convencionales | Solo equipos DMR Tier II compatibles |

---

## ⚙️ Funciones explicadas

### 🔋 Power Save (Ahorro de Energía)
**Ruta:** `Settings → Radio Settings → Other Func → Power Save`  
Permite que el receptor entre en reposo periódico para extender la vida de la batería.

| Opción | Ciclo de trabajo | Efecto |
|:--------|:-----------------|:-------|
| Save Off | Desactivado | Máximo consumo, respuesta inmediata. |
| Save 1 : 1 | 30 ms activo / 30 ms reposo | Ahorro leve. |
| Save 1 : 2 | 30 ms activo / 60 ms reposo | Ahorro medio recomendado. |
| Save 1 : 4 | 30 ms activo / 120 ms reposo | Máximo ahorro, posible retardo RX. |

> 💡 Recomendado: **Save 1:2** para equilibrio entre autonomía y respuesta.  
> ⚠️ En modo DIG puede causar leve retardo al recibir.

---

### ⚙️ Freq Step (Incremento de frecuencia)
**Ruta:** `Settings → Channel Set → Freq Step`  
Determina el salto de frecuencia cuando se ajusta manualmente desde el VFO.

| Valor | Incremento | Aplicación sugerida |
|:------|:-----------|:--------------------|
| 2.5 kHz | Muy fino | Ajustes precisos o intermedios. |
| 5 kHz | Estándar | Uso general VHF/UHF. |
| 6.25 kHz | Digital | DMR / NXDN canal reducido. |
| 10 – 12.5 kHz | Medio | DMR (12.5 kHz típico). |
| 25 kHz | Amplio | Escaneo rápido o wide FM. |
| 50 – 100 kHz | Macro | Exploración o bandas aéreas. |

> 💡 Para **DMR**, usa **12.5 kHz**; para **FM**, 5 kHz.

---

### 🔊 TBST Sel (Tone Burst Selection)
**Ruta:** `Settings → Channel Set → TBST Sel`  
(Solo disponible en modo **ANA**)  
Envía un tono corto antes de transmitir para abrir repetidores analógicos que lo requieran.

| Frecuencia | Uso típico |
|:------------|:-----------|
| 1000 Hz | Repetidores antiguos |
| 1450 Hz | Algunos europeos |
| 1750 Hz | 🌎 Estándar mundial (recomendado) |
| 2100 Hz | Sistemas especiales |

> ⚠️ No sustituye CTCSS/DCS; algunos repetidores exigen ambos.

---

## 🧭 Consejos rápidos de operación

- **Modo dual (A/B):** permite escuchar dos frecuencias; el indicador rojo (▲) muestra el VFO activo para TX.  
- **Teclas P1 / P2:** se pueden asignar a funciones como *Monitor*, *Scan* o *Zone Change* desde el CPS.  
- **ANA ↔ DIG:** el conmutador del modo depende del tipo de canal programado; no se cambia desde VFO directo.  
- **Guardar canales:** utiliza “Menu → CH Save” para almacenar configuraciones temporales en memoria.  
- **Pantalla:** en DMR, la etiqueta muestra el *Contact* o *Talk Group*; en FM, el nombre del canal o frecuencia.

---

## 🧩 Ejemplo de configuración mixta (ANA + DIG)

| Canal | Modo | RX (MHz) | TX (MHz) | Color Code / CTCSS | TG / ID | Comentario |
|:------|:------|:---------|:---------|:-------------------|:--------|:------------|
| 1 | DIG | 462.56250 | 462.56250 | CC 1 | TG 91 | Repetidor HK-ASOREC |
| 2 | ANA | 462.65000 | 467.65000 | 123.0 Hz | — | Repetidor HS-Z3 |
| 3 | ANA | 433.55000 | 433.55000 | OFF | — | Frecuencia simplex local |

---

## 🧰 Información técnica básica

| Parámetro | Valor |
|:-----------|:------|
| Frecuencias | 136–174 MHz / 400–470 MHz |
| Modos | FM (ANA) / DMR Tier II (DIG) |
| Potencia | 1 W / 5 W |
| Canales | 1024 |
| Espaciado | 12.5 / 25 kHz |
| Batería | 2000 mAh Li-Ion |
| Conector de programación | Micro-USB |

---

## 🪪 Créditos y licencia

**Autor:** HJ3RAW - William Rozo Álvarez  
**Licencia:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)  
**Repositorio sugerido:**  
`https://github.com/HJ3RAW/DM32UV_Manual`

> Se permite copiar, adaptar y compartir con atribución y uso no comercial.  
