# 📡 Programación del Baofeng DM-32UV (DMR / Analógico)

**Autor:** William Rozo Alvarez (WIROAL)  
**Última actualización:** Octubre 2025  
**Equipo:** Baofeng DM-32UV (FCC ID: 2AJGM-DM32UV)  
**Fabricante:** Po Fung Electronic (HK) International Group Co. Ltd.

---

## 🧩 1. Qué necesitas

### 🖥️ Hardware
- Radio **Baofeng DM-32UV**
- **Cable de programación USB-K** (de dos pines tipo Kenwood)
  - Chip compatible: **CH340**, **Prolific PL2303**, o **FTDI**

### 💾 Software
1. **Driver USB (CH340)**  
   👉 [Descargar desde wch.cn (oficial)](https://www.wch.cn/download/CH341SER_EXE.html)
2. **CPS Baofeng DM-32UV (Customer Programming Software)**  
   👉 [Descargar desde baofengradio.com → sección Downloads](https://www.baofengradio.com/pages/download)
3. (Opcional) **Plantilla de canales y TG Colombia (VHF/UHF)**  
   👉 [Repositorio de ejemplo en GitHub (radioaficionados Colombia)](https://github.com/motocolombia/dmr-codeplug-colombia)

---

## ⚙️ 2. Instalar el driver del cable

1. Conecta el cable USB al PC (sin el radio).
2. Abre **Administrador de dispositivos** → **Puertos (COM y LPT)**.  
   Verás algo como:  
   - “USB-SERIAL CH340”  
   - “Prolific USB-to-Serial Comm Port”  
   - “FTDI USB Serial Port”
3. Anota el número de puerto (ejemplo: **COM3**).
4. Si aparece ⚠️ error, instala el driver correcto (usa el del enlace anterior).

---

## 🧭 3. Instalar y abrir el CPS

1. Descarga el CPS oficial (archivo .zip o .exe).  
2. Instálalo o ejecútalo directamente.  
3. Abre el programa y selecciona el **puerto COM** detectado.

---

## 🔄 4. Conectar el radio

1. Apaga el radio.  
2. Conecta el cable firmemente (dos pines).  
3. Enciende el radio.  
4. En el CPS:  
   - Menú → **Program → Read from Radio**  
   - Espera a que descargue tu configuración (codeplug).  
5. Guarda ese archivo como **respaldo original**.

---

## 🧱 5. Editar tu configuración

Configura lo siguiente:

| Sección | Qué puedes modificar | Ejemplo |
|----------|----------------------|----------|
| **General Settings** | Nombre de usuario, ID DMR, zona horaria | WIROAL / 730001 |
| **Channel Information** | Frecuencia, ancho de banda, potencia | VHF 145.500 MHz / High |
| **DMR Contacts** | TG, grupo, tipo de llamada | TG730 (Colombia), TG732 (Bogotá) |
| **Zone List** | Agrupa canales por región o uso | “Bogotá VHF”, “Emergencia UHF” |
| **Buttons & PTT ID** | Accesos rápidos | P1 = Scan On/Off |

Cuando termines → Menú → **Program → Write to Radio**

---

## 📻 6. Recomendaciones de uso

- Bandas válidas: **VHF 136-174 MHz**, **UHF 400-470 MHz**  
- No uses frecuencias asignadas a servicios oficiales.  
- Verifica tu **ID DMR** en [radioid.net](https://radioid.net).  
- TG nacionales más comunes:  
  - 730 → Colombia nacional  
  - 732 → Bogotá  
  - 73201 → Grupo regional  
- Guarda una copia del archivo `.dat` o `.rdt` que genera el CPS.

---

## 🔧 7. Solución de problemas

| Problema | Causa probable | Solución |
|-----------|----------------|-----------|
| ❌ “Read Failed” | Puerto COM incorrecto o cable flojo | Revisa el número COM y reconecta |
| ⚠️ “Driver no reconocido” | Falta driver CH340 | Instala driver oficial |
| 💾 “Write Failed” | Diferencia de firmware | Usa CPS para DM-32UV exacto |
| 🔇 No transmite DMR | ID no configurado | Coloca tu ID DMR válido |

---

## 🧠 8. Archivos recomendados

Estructura sugerida para tu paquete local:

DM32UV_Colombia/
├─ CPS_DM32UV/
│ └─ setup.exe
├─ Drivers/
│ └─ CH341SER.EXE
├─ Plantillas/
│ ├─ DM32UV_Codeplug_Bogota.rdt
│ └─ DM32UV_Codeplug_Colombia.rdt
└─ Instrucciones.md


---

## ⚠️ 9. Advertencias legales

- La modificación del radio para recibir señales celulares u otros servicios privados está prohibida bajo normas FCC y ANE Colombia.  
- Usa las frecuencias permitidas por la resolución vigente de la ANE.  
- Transmitir en DMR requiere un ID asignado y respeto por las redes TG nacionales.

---

## 📚 10. Créditos y recursos útiles

- [BaofengRadio – Descargas oficiales](https://www.baofengradio.com/pages/download)  
- [CH340 Driver Support (WCH)](https://www.wch.cn/download/CH341SER_EXE.html)  
- [RadioID.net – Registro DMR global](https://radioid.net)  
- [Grupo DMR Colombia (Comunidad)](https://www.facebook.com/groups/DMRColombia/)

---

<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/6f18e3ad-07f8-455e-abc6-38b13013f541" />



**Elaborado por:** WIROAL  
**Propósito:** Documentación técnica para programación del Baofeng DM-32UV  
**Licencia:** CC BY-NC-SA 4.0  


