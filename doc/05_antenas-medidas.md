# 📻 Guía Completa de Frecuencias y Modos de Radioafición

Este repositorio contiene una guía estructurada sobre las **frecuencias de llamada, modos de emisión y reglas de operación** utilizadas en la radioafición, alineadas con las recomendaciones de la **IARU (International Amateur Radio Union)**.

---

## 📌 Tabla de Contenidos
- [Estructura de Modos (LSB vs USB)](#-estructura-de-modos-lsb-vs-usb)
- [Tabla de Frecuencias de Llamada por Banda](#-tabla-de-frecuencias-de-llamada-por-banda)
- [Glosario de Términos y Código Q](#-glosario-de-términos-y-código-q)
- [Conceptos Fundamentales](#-conceptos-fundamentales)

---

## 📐 Estructura de Modos (LSB vs USB)

En las transmisiones de voz por **Banda Lateral Única (SSB)**, la elección entre LSB y USB sigue un convenio internacional basado en la frecuencia de operación:

```
                      PUNTO DE CORTE (10 MHz)
                                 │
    ◄── LSB (Lower Sideband) ────┼──── USB (Upper Sideband) ──►
                                 │
 160m    80m     40m             │   20m    17m    15m    12m    10m    6m    2m    70cm
(1.8m)  (3.5m)   (7m)            │  (14m)  (18m)  (21m)  (24m)  (28m)  (50m) (144m) (430m)
```

> ⚠️ **Excepción:** La banda de **60 metros** ($5.3\text{ MHz}$) utiliza **USB** por normativa internacional a pesar de estar por debajo de los $10\text{ MHz}$.

---

## 📊 Tabla de Frecuencias de Llamada por Banda

| Banda | Frecuencia | Modo | Uso / Propósito Principal |
| :--- | :--- | :--- | :--- |
| **160 m** *(1.8 MHz / MF)* | `1.836 MHz` | CW | QRP (Baja potencia $\le 5\text{W}$) |
| | `1.840 – 1.843 MHz` | Todos | Uso general y varios modos |
| **80 m** *(3.5 MHz / HF)* | `3.550 MHz` | CW | Llamada general |
| | `3.555 MHz` | CW | QRS (Telegrafía lenta / Principiantes) |
| | `3.560 MHz` | CW | QRP |
| | `3.690 MHz` | LSB | QRP Fonía |
| | `3.760 MHz` | LSB | Emergencias y tráfico de red |
| **40 m** *(7 MHz / HF)* | `7.030 MHz` | CW | QRP |
| | `7.090 MHz` | LSB | Llamada general en fonía |
| **30 m** *(10 MHz / HF)* | `10.116 MHz` | CW | Llamada telegrafía *(Exclusivo CW/Datos)* |
| **20 m** *(14 MHz / HF)* | `14.055 MHz` | CW | QRS (Telegrafía lenta) |
| | `14.060 MHz` | CW | QRP |
| | `14.285 MHz` | USB | QRP Fonía |
| | `14.300 MHz` | USB | Emergencias y Redes Marítimas |
| **17 m** *(18 MHz / HF)* | `18.086 MHz` | CW | QRP |
| | `18.160 MHz` | USB | Llamada general y emergencias |
| **15 m** *(21 MHz / HF)* | `21.055 MHz` | CW | QRS (Telegrafía lenta) |
| | `21.060 MHz` | CW | QRP |
| **12 m** *(24 MHz / HF)* | `24.910 MHz` | CW | QRP |
| | `24.950 MHz` | USB | Llamada general |
| **10 m** *(28 MHz / HF)* | `28.060 MHz` | CW | QRP |
| | `28.200 MHz` | CW | Red mundial de balizas (IBP) |
| | `28.360 MHz` | USB | QRP Fonía |
| | `28.500 MHz` | USB | Llamada general en fonía |
| | `29.600 MHz` | FM | Llamada directa (Simples) |
| **11 m** *(27 MHz / CB)* | `27.065 MHz` *(Ch 9)* | AM / FM | **Canal Oficial de Emergencias** |
| | `27.185 MHz` *(Ch 19)* | AM / FM / SSB | Carretera y llamada general |
| **6 m** *(50 MHz / VHF)* | `50.090 MHz` | CW | DX (Larga distancia) |
| | `50.110 MHz` | USB | Llamada intercontinental (DX) |
| | `51.500 MHz` | FM | Contactos directos (Simples) |
| **2 m** *(144 MHz / VHF)* | `144.000 MHz` | CW / SSB | Llamada en banda lateral y telegrafía |
| | `145.000 MHz` | FM | Llamada estándar internacional (IARU) |
| | `145.550 MHz` | FM | Encuentro habitual (España) |
| **70 cm** *(430 MHz / UHF)*| `432.200 MHz` | USB | Llamada en SSB |
| | `433.500 MHz` | FM | Llamada en simples (frecuencia base) |
| | `433.550 MHz` | FM | Frecuencia de encuentro alternativa |

---

## 💡 Conceptos Fundamentales

### **CW (Continuous Wave / Telegrafía)**
Transmisión mediante **Código Morse** realizada interrumpiendo manualmente la onda portadora.
- **Ancho de banda:** $\approx 500\text{ Hz}$ (vs. $2.700\text{ Hz}$ de la fonía).
- **Ventaja:** Elevada eficiencia energética y gran resistencia al ruido electromagnético.

```
       [TECLA PRESIONADA]          [LIBERADA]
Señal: ─────┐        ┌───────────┐    ┌──────
            └────────┘           └────┘
Audio:         Punto       Raya        Punto
```

### **SSB (Single Sideband / Banda Lateral Única)**
Modulación de amplitud (AM) a la que se le elimina la portadora y una de las bandas laterales para concentrar el $100\%$ de la potencia del transmisor en la señal de voz útil.

---

## 📖 Glosario de Términos y Código Q

| Término | Significado | Descripción |
| :--- | :--- | :--- |
| **QRP** | Baja potencia | Operación con potencias $\le 5\text{W}$ en CW o $\le 10\text{W}$ en SSB. |
| **QRS** | Transmitir despacio | Solicitud o indicación de emisión a baja velocidad en Morse. |
| **QRM** | Interferencia humana | Interferencia provocada por otras estaciones. |
| **QRN** | Interferencia natural | Ruido estático o atmosférico. |
| **DX** | Larga distancia | Contactos internacionales o entre continentes. |
| **Simples** | Transmisión directa | Comunicación punto a punto sin el uso de repetidores. |