# 📡 Plano Conceptual — Dipolo en Abanico Multibanda (40/20/10 m)

## 🎯 Descripción
Un **dipolo en abanico (fan dipole)** es una antena multibanda formada por varios dipolos de media onda conectados en paralelo en el **centro**.  
Se alimenta mediante un **balun 1:1** al centro, y cada banda tiene sus propios brazos.

---

## 📏 Medidas iniciales (por brazo)
- 🟧 **40 m (7,1 MHz):** ~10,5 m  
- 🔵 **20 m (14,2 MHz):** ~5,1 m  
- 🟢 **10 m (28,4 MHz):** ~2,55 m  

👉 Cortar un poco más largo (2–3%) y ajustar recortando para centrar la ROE.

---

## ⚙️ Lista de Materiales
- 🎛️ **Balun 1:1 de corriente** (ya lo tienes)  
- 🧵 **Alambre de cobre aislado** (AWG 14–18, 1,5–2,5 mm²)  
- 🔗 **Separadores plásticos** (10–15 cm de ancho, cada 50–70 cm en los primeros 2–3 m)  
- 🟤 **Aisladores de extremos**  
- 🪢 **Cuerda sintética trenzada** (resistente a UV)  
- 📡 **Cable coaxial RG-213** (o RG-58 si el tramo es corto)  
- ⚡ **Descargador a tierra** + **puesta a tierra de estación**

---

## 🏗️ Instalación
- **Altura del mástil (apex):** 8–12 m  
- **Ángulo entre brazos (inverted-V):** 120–140°  
- **Altura de extremos:** ≥2,5 m sobre el suelo  
- **Separadores:** primer separador a 30 cm del balun, luego cada 50–70 cm

---

## 📐 Esquema conceptual
```
               Balun 1:1
                  |
          ┌───────┼───────┐
          |       |       |
       🟧40m   🔵20m   🟢10m
          |       |       |
         ...    ...     ...
       aisl.   aisl.   aisl.
```
---

## ✅ Notas
- Ajustar primero la banda de **40 m**, luego **20 m**, y por último **10 m**.  
- Mantener simetría: recortar los dos brazos de cada banda por igual.  
- Mantener distancia de objetos metálicos y líneas eléctricas ⚠️
