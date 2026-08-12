# Plantilla de entrada de bitácora

> Copia este archivo por cada sesión como `YYYY-MM-DD-sesion-N.md` en la carpeta `bitacora/` de tu portafolio.
> **Borra las secciones que no uses** (mejor eliminarlas que dejarlas vacías) y borra todas las notas en *cursiva*.
> Meta de tamaño: **1 a 2 pantallas**. Una buena entrada corta vale más que una larga de relleno.

---

```markdown
---
titulo: "Sesión N — Título corto"
fecha: YYYY-MM-DD
autor: "Nombre"
equipo: "Nombre del equipo (si aplica)"
estado: borrador   # borrador | completa
---

# Sesión N — Título corto

## Qué debía lograr hoy
*Copia los objetivos de la sesión y márcalos al final. Sé honesto: un ❌ explicado vale más que un ✅ falso.*

- [ ] Objetivo 1
- [ ] Objetivo 2

## Qué usé
*Lista corta: componentes y software. Si compraste algo, pon el costo.*

- ESP32 DevKit V1, TB6612, ...
- Arduino IDE 2.x / Python 3.12

## Qué hice y qué pasó (evidencia)
*2–4 fotos o capturas TUYAS, cada una con un pie de foto de una línea diciendo qué muestra.
Si mediste algo, va la tabla — la tabla ES la evidencia.*

![Pie de foto: qué muestra esta imagen](img/sesionN_1.jpg)

| Magnitud | Teórico | Medido | % error |
| --- | --- | --- | --- |
|  |  |  |  |

## Qué falló y cómo lo resolví
*Mínimo una. Si de verdad nada falló, escribe qué te sorprendió.
Formato: síntoma → cómo lo encontré → solución.*

- **Síntoma:** ...
- **Cómo lo encontré:** ...
- **Solución:** ...

## Qué aprendí
*3 a 5 líneas, con tus palabras. No es resumen del tema: es qué entendiste TÚ que antes no.*

## Siguiente paso
*Una línea: qué sigue antes de la próxima sesión.*
```

---

## Reglas de la bitácora

1. **Se publica antes de la siguiente sesión** (mismo plazo que la política de entregas del syllabus).
2. **Las fotos y videos son tuyos**, tomados por ti, del montaje real. Capturas de pantalla con fecha visible cuando aplique.
3. **El commit cuenta como fecha.** Una bitácora del semestre subida en un solo commit final no es una bitácora — el historial de Git es parte de la evidencia.
4. **Se permite IA como apoyo de redacción declarándolo**, pero la evidencia (fotos, tablas, mediciones, código) es tuya, y en las defensas orales explicas tu propia bitácora.
5. **Las tablas de medición se llenan con números reales**, aunque salgan feos. Un error de 40 % bien explicado califica mejor que un 2 % inventado.
