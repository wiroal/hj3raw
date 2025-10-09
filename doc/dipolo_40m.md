# 📡 Dipolo de 40 m (7.1 MHz)

Este documento resume las medidas y configuraciones típicas de un dipolo para la banda de 40 m.

---

## 📊 Altura vs Ángulo de Radiación

| Altura del dipolo (sobre el suelo) | Relación con λ (λ=40 m) | Ángulo de radiación predominante | Cobertura típica | Longitud total del dipolo | Longitud de cada brazo |
|-----------------------------------|--------------------------|---------------------------------|------------------|----------------------------|------------------------|
| **5 m**                           | ~0.12 λ                 | 75°–90° (muy alto)              | **NVIS**: cobertura local/regional (100–800 km) | ~21.13 m | ~10.57 m |
| **8 m**                           | ~0.20 λ                 | 60°–80°                         | Nacional/regional con menos “burbuja” | ~21.13 m | ~10.57 m |
| **10 m**                          | ~0.25 λ                 | 45°–60°                         | Buen compromiso: regional + DX ocasional | ~21.13 m | ~10.57 m |
| **15 m**                          | ~0.37 λ                 | 30°–40°                         | Ideal para DX intercontinental | ~21.13 m | ~10.57 m |
| **20 m**                          | ~0.5 λ                  | 20°–30°                         | Excelente para DX, requiere torres altas | ~21.13 m | ~10.57 m |

---

## 📐 Esquema de instalación

### 1. Dipolo horizontal (Flat-top)
```
10.57 m  -------------------  10.57 m
         |
         |  Altura mínima recomendada: 10 m
         |
       [Alimentación coaxial]
```

- Necesita **dos puntos de anclaje**.  
- Patrón bidireccional con mayor ganancia lateral.  

### 2. Dipolo en V invertida (Inverted-V)
```
        8–12 m
          /\
         /  \
  10.5 m/    \10.5 m
       /      \
     2–3 m    2–3 m
```

- Solo requiere **un mástil central alto** y dos anclas laterales.  
- Ángulo recomendado entre brazos: **120°–140°**.  
- Mejor adaptación a 50 Ω, fácil de instalar en espacios reducidos.  

---

## 🔧 Notas de construcción
- Fórmula general: **L total (m) = 150 / f (MHz)**.  
- Para 7.1 MHz → **21.13 m total**, **10.57 m por brazo**.  
- Cortar cada hilo con **5–10 cm de sobra** y ajustar con medidor de ROE (SWR).  
- Usar **balun 1:1** para evitar corrientes de retorno en el coaxial.  

---

✍️ Autor: Preparado con fines prácticos para radioaficionados.
