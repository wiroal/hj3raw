# 📡 Dipolo de 15 m (f₀ ≈ 21.2 MHz)

Este documento resume las medidas y configuraciones típicas de un dipolo para la banda de 15 m.

---

## 📊 Altura vs Ángulo de Radiación

| Altura del dipolo (sobre el suelo) | Relación con λ (λ ≈ 14.15 m) | Ángulo de radiación predominante | Cobertura típica | Longitud total del dipolo | Longitud de cada brazo |
|-----------------------------------|--------------------------|---------------------------------|------------------|----------------------------|------------------------|
| **3 m**                           | ~0.21 λ  | 75°–90° (muy alto)              | **NVIS** / local-regional | ~7.08 m | ~3.54 m |
| **5 m**                           | ~0.35 λ  | 60°–80°                         | Regional | ~7.08 m | ~3.54 m |
| **7.5 m**                         | ~0.53 λ| 45°–60°                         | Compromiso: regional + DX ocasional | ~7.08 m | ~3.54 m |
| **10 m**                          | ~0.71 λ | 30°–40°                         | Mejor para DX | ~7.08 m | ~3.54 m |
| **12–15 m**                       | ~0.85–1.06 λ | 20°–30° | Excelente para DX | ~7.08 m | ~3.54 m |

> **Reglas prácticas:** Un dipolo comienza a rendir bien para DX alrededor de **¼ λ** de altura. Para trabajo local/NVIS puede instalarse más bajo.

---

## 📐 Esquema de instalación

### 1. Dipolo horizontal (Flat-top)
```
3.54 m  -------------------  3.54 m
         |
         |  Altura recomendada: ≥ ¼ λ
         |
       [Alimentación coaxial]
```

- Requiere **dos puntos de anclaje**.  
- Patrón bidireccional con mayor ganancia lateral.  

### 2. Dipolo en V invertida (Inverted-V)
```
       vértice alto (≥ ¼ λ)
          /\
         /  \
   3.54 m/    \3.54 m
       /      \
     2–3 m    2–3 m
```

- Solo requiere **un mástil central** y dos anclas laterales.  
- Ángulo recomendado entre brazos: **120°–140°**.  
- Mejor adaptación a 50 Ω; práctico en espacios reducidos.  

---

## 🔧 Notas de construcción
- Fórmula general: **L total (m) = 150 / f (MHz)**.  
- Para 21.2 MHz → **7.08 m total**, **3.54 m por brazo**.  
- Corta cada hilo con **5–10 cm extra** y ajusta con medidor de ROE (SWR).  
- Usa **balun 1:1** (o choke con 6–8 vueltas del coaxial en 10–12 cm de diámetro, según banda) para mitigar corrientes de retorno.  

---

✍️ Autor: Preparado con fines prácticos para radioaficionados.
