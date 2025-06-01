# Guía Rápida RTL-SDR Blog V3 para Banda Aérea, Radioaficionados y HF

Este documento resume los pasos que funcionaron para poner en marcha un RTL-SDR Blog V3 en Windows, orientado a la recepción de señales en la banda aérea VHF (118–137 MHz), así como en bandas de radioaficionados y HF. Incluye configuraciones de software, modulación, y medidas precisas para antenas dipolo.

---

## ✅ Instalación correcta en Windows

### 1. Conectar RTL-SDR
- Conecta el RTL-SDR Blog V3 directamente a un puerto USB.

### 2. Instalar driver con Zadig
- Ejecuta `zadig.exe` como administrador.
- En el menú `Options`, activa:
  - "List All Devices"
  - "Ignore Hubs or Composite Parents"
- Selecciona: **Bulk-In Interface (Interface 0)**
- Reemplaza el driver con: **WinUSB**

### 3. Abrir SDR#
- Ejecuta `SDRSharp.exe` o `SDRSharp.dotnet9.exe`
- En la lista desplegable, selecciona: `RTL-SDR (USB)`
- Presiona el botón ▶ para iniciar la recepción

---

## ✈️ Configuración para Banda Aérea (118 - 137 MHz)

### SDR#
- **Frecuencia**: 123.500.000 Hz (por ejemplo)
- **Modulación**: AM
- **Ancho de banda**: 8 a 12 kHz

### Antena Dipolo RTL-SDR Blog
- Frecuencia central: **127.5 MHz**
- Longitud de onda λ: `≈ 2.35 m`
- Longitud total del dipolo: `117.4 cm`
- Longitud por varilla: `58.7 cm`

---

## 📻 Frecuencias Aéreas Comunes

| Frecuencia (MHz) | Uso común                       | Observación                      |
|------------------|----------------------------------|----------------------------------|
| 118.1            | Torre / ATIS                    | Común en aeropuertos regionales  |
| 119.5            | Torre de control principal      | Muy activa en capitales          |
| 120.5            | Torre / Aproximación            | Frecuente en operaciones civiles |
| 121.5            | Emergencias aeronáuticas        | Siempre activa (frecuencia guardada) |
| 122.8            | Multicom / CTA sin torre        | Pilotos se comunican entre sí    |
| 123.5            | Frecuencia de prueba            | Ideal para calibrar antenas      |
| 127.5            | Punto medio de la banda         | Para centrado de antena dipolo   |
| 133.0–136.975    | Comunicaciones entre aeronaves  | Aerovías de gran altitud         |

---

## 📡 Bandas de Radioaficionados

| Banda    | Rango Frecuencia | Modulación | Longitud de onda | Largo por varilla | Notas |
|----------|------------------|------------|------------------|-------------------|-------|
| 2 m      | 144–148 MHz      | NFM        | 2.08 m           | 52 cm             | Activa en ciudades |
| 1.25 m   | 222–225 MHz      | NFM        | 1.35 m           | 34 cm             | Menos común        |
| 70 cm    | 420–450 MHz      | NFM        | 0.68 m           | 17 cm             | Muy usada          |

---

## 🌐 Bandas HF (requieren modo Direct Sampling)

| Banda | Rango (MHz) | Uso | Longitud onda | Varilla λ/4 | Antena recomendada |
|-------|-------------|-----|----------------|--------------|---------------------|
| 80 m  | 3.5–4.0     | Voz | 85.7 m         | 21.4 m       | Hilo largo o dipolo |
| 40 m  | 7.0–7.3     | Voz | 42.8 m         | 10.7 m       | Dipolo invertido    |
| 20 m  | 14.0–14.35  | DX  | 21.4 m         | 5.35 m       | Longwire            |
| 15 m  | 21.0–21.45  | Voz | 14.2 m         | 3.55 m       | Vertical            |
| 10 m  | 28.0–29.7   | Voz | 10.3 m         | 2.57 m       | Dipolo telescópico  |

> En SDR#: ir a configuración del dispositivo > activar **Direct Sampling (Q branch)** para usar HF.

---

## 🔍 Otras Frecuencias Útiles

| Frecuencia (MHz) | Uso                         | Modulación |
|------------------|------------------------------|------------|
| 88–108           | Radio FM comercial           | WFM        |
| 137              | Satélites meteorológicos     | QPSK / FM  |
| 433              | Sensores inalámbricos / IoT  | NFM        |
| 868              | Redes LoRa                   | NFM        |
| 1090             | ADS-B / Aviones              | —          |

---

## 📌 Recomendaciones Finales

- Coloca la antena cerca de una ventana o en el exterior.
- Ajusta la longitud de las varillas según la frecuencia.
- Escucha frecuencias aéreas en la mañana o en la tarde-noche.
- Usa polarización vertical si es posible.

---

## 📄 Autor

**William Rozo**  
Compilado con base en la experiencia práctica de configuración del RTL-SDR Blog V3 para bandas aeronáuticas, radioaficionados y HF.
