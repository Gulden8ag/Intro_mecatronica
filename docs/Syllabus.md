# Syllabus

## Horario del curso

**Sesiones**: 1 sesión / semana, 2 horas / sesión

- Viernes, 11:00 – 13:00
- Laboratorio de Electrónica

## Información general

| | |
| --- | --- |
| **Asignatura** | Introducción a la Mecatrónica · Sigla LIIT0401 |
| **Periodo** | Otoño 2026 |
| **Programa** | Ingeniería Mecatrónica · 1er semestre |
| **Docente** | Oliver Ochoa García |
| **Contacto** | oliver.ochoa2@iberopuebla.mx |
| **Prerrequisitos** | N/A |

## Qué necesitas traer

No hay prerrequisitos académicos (es tu primer semestre), pero sí logística:

- **Laptop** con permisos para instalar software: Arduino IDE, Python 3.10+, Git y VS Code (o tu editor favorito).
- **Cuenta de GitHub** (la creamos en la sesión 1 si no tienes).
- **Celular Android o PC con Bluetooth** para controlar tu carro (iPhone no soporta el Bluetooth serial que usamos — ve la nota del [Tema 2](M1_Eletronica/tema2.md)).
- Ganas de que las cosas fallen: en este curso los errores se documentan, no se esconden.

## Eje transversal y competencias

| | |
| --- | --- |
| **Eje transversal** | Sustentabilidad |
| **Nivel de logro** | Iniciación |
| **Competencia genérica priorizada** | Trabajo colaborativo |

**Competencias específicas del programa que toca la asignatura:** interacción humano-máquina con algoritmos e IA; sistemas de cómputo embebidos; control continuo y discreto; instrumentación electrónica; elementos mecánicos; integración de manufactura; y proyectos mecatrónicos con énfasis social.

## Fines de aprendizaje

**Generales (plan oficial):**

- Identificar las áreas específicas de desarrollo del ingeniero mecatrónico en los contextos nacional y regional, a través del estudio de los campos de acción profesional, para detectar las oportunidades de desarrollo e intervención.
- Plantear un proyecto de aplicación básica de la ingeniería mecatrónica, a través de la identificación de áreas de oportunidad profesional, para diferenciar el uso de equipo y componentes propios de la ingeniería en mecatrónica.

**Específicos de la asignatura:**

- Construir y medir circuitos electrónicos básicos, comparando resultados experimentales con cálculos teóricos.
- Programar un ESP32 integrando sensores, actuadores y comunicación inalámbrica.
- Desarrollar en equipo un vehículo RC por Bluetooth y demostrarlo en un torneo.
- Implementar un lazo PID y visión por computadora para dotar de autonomía al vehículo (reto tipo VSSS simplificado).
- Analizar mecanismos básicos de transmisión aplicados al tren motriz de un vehículo.
- Documentar el proceso en un portafolio web público (GitHub Pages) y defenderlo oralmente.

## Bibliografía

- Liou, Frank W. *Rapid Prototyping and Engineering Applications*. CRC Press, 2019.
- Alciatore, David. *Introduction to Mechatronics and Measurement Systems*. McGraw-Hill Education, 2018.
- Bolton, William. *Mecatrónica. Sistemas de control electrónico en la ingeniería mecánica y eléctrica*. Alfaomega, 2017.
- Jouaneh, Musa. *Fundamentos de mecatrónica*. Cengage Learning, 2016.

**Apoyos:** [documentación de OpenCV](https://docs.opencv.org) · [Arduino-ESP32 (Espressif)](https://docs.espressif.com/projects/arduino-esp32/) · [categoría IEEE Very Small Size Soccer](https://vsssleague.github.io/vss/) · [IEEE RAS](https://www.ieee-ras.org/publications/ram)

## Política de evaluación

**Componentes de la calificación:**

| Componente | Qué cubre | Evidencia | Peso |
| --- | --- | --- | --- |
| Portafolio de clase | Bitácora del semestre: evidencias de proceso, mediciones propias, historial de commits, defensas orales | Sitio web público con entradas fechadas | **20 %** |
| Proyecto 1 · Carro RC | Electrónica, MCU, actuadores, BT, mecanismos + torneo | Demo con rúbrica, repo, reporte, torneo — ver [brief](Proyectos/P1.md) | **25 %** |
| Proyecto Final · VSSS | Visión, control PID, autonomía + torneo inter-grupos | Demo por niveles con rúbrica, repo, reflexión — ver [brief](Proyectos/P2.md) | **25 %** |
| Prácticas y demos en vivo | Las 9 sesiones de práctica (S2–6, 8, 11–13) | Demo en clase (50 %) + entrada de bitácora (50 %) | **30 %** |
| **Total** | | | **100 %** |

**Escala de redondeo** (solo la calificación final se redondea):

| Promedio final | Calificación reportada |
| --- | --- |
| Hasta 5.9 | **5** |
| 6.0 – 6.5 | **6** |
| 6.6 – 7.5 | **7** |
| 7.6 – 8.5 | **8** |
| 8.6 – 9.5 | **9** |
| 9.6 – 10 | **10** |

**Entregas y revisiones:**

| Ítem | Política |
| --- | --- |
| Fecha de entrega | Todos los entregables se publican antes de la siguiente sesión. |
| Entrega tardía | Hasta 7 días naturales después, calificación máxima **8.0**; después no se acepta salvo justificación documentada. |
| Formato | PDF o el formato que indique la rúbrica, en Teams; formato/plataforma incorrecta = −1 punto. |
| Revisión de calificaciones | Por escrito, dentro de los **7 días hábiles** posteriores a su publicación. Se pierde el derecho con más de 5 faltas no justificadas. |
| Recuperación | Si el promedio final es < 6.0: evaluación integradora (demostración práctica + defensa oral) con asistencia ≥ 85 %; sustituye la calificación más baja entre los dos proyectos. |

**Uso de inteligencia artificial:**

| Ítem | Política |
| --- | --- |
| Como herramienta | Permitida (redacción, depuración, ideación) **declarando en cada entregable dónde y cómo se usó**. |
| Evidencias | Fotos, videos, mediciones y commits deben ser **propios del equipo**, con historial distribuido en el tiempo. |
| Defensa oral | Todo entregable debe poder explicarse en voz alta; no poder explicar el propio trabajo invalida la evidencia. |

**Faltas:**

| Ítem | Política |
| --- | --- |
| Justificación | Documentación (certificado médico, nota oficial) dentro de los 7 días hábiles posteriores a la falta. |
| Impacto | Las faltas no afectan directamente la calificación; más de 5 no justificadas → se pierde el derecho a revisiones. |
| Extensiones | Se solicitan por correo **antes** de la fecha límite, con motivo justificado. |

**Comunicación:**

| Ítem | Política |
| --- | --- |
| Canal oficial | **Microsoft Teams**: avisos, fechas, rúbricas y calificaciones. |
| Evidencias | Viven en tu **portafolio web**; en Teams se entrega la **URL de la entrada específica**, no la portada. |

## Módulos

| Módulo | Temas | Material |
| --- | --- | --- |
| M0 · Portafolio web | GitHub Pages, Markdown, Git, plantilla de bitácora | [Markdown](M0_Portafolio_web/comandos.md) · [Git](M0_Portafolio_web/gitcmds.md) · [Plantilla](M0_Portafolio_web/ejemplo.md) |
| M1 · Electrónica y MCU | Electrónica básica y 555; ESP32 (GPIO, BT); actuadores (TB6612, PWM, servos); sensores (ADC, LM35, MPU6050, filtros) | [T1](M1_Eletronica/tema1.md) · [T2](M1_Eletronica/tema2.md) · [T3](M1_Eletronica/tema3.md) · [T4](M1_Eletronica/tema4.md) |
| M2 · Control y Visión | Mecanismos; visión por computadora (OpenCV, HSV, centroides); control PID; cierre de lazo con ArUco | [T5](M2_Control/tema5.md) · [T6](M2_Control/tema6.md) · [T7](M2_Control/tema7.md) · [T8](M2_Control/tema8.md) |
| Proyectos | Carro RC por Bluetooth (medio semestre); fútbol de robots VSSS simplificado (final) | [P1](Proyectos/P1.md) · [P2](Proyectos/P2.md) |

## Calendario de sesiones

*Viernes 11:00–13:00. Fechas del calendario oficial de Licenciaturas 2026 (periodo: 17 ago. – 9 dic.); cualquier ajuste se avisa por Teams.*

| S | Módulo | Fecha | Tema | Entregable de bitácora |
| --- | --- | --- | --- | --- |
| 1 | M0 | 2026-08-21 | Introducción · portafolio en GitHub Pages · visión personal | Portafolio publicado + "sobre mí" |
| 2 | M1 | 2026-08-28 | Electrónica básica · 555 astable y monoestable · medición | Tablas medición vs. teoría + video ≤60 s |
| 3 | M1 | 2026-09-04 | ESP32: GPIO, botón con pull-up y antirrebote | Demo toggle + código en repo |
| 4 | M1 | 2026-09-11 | Actuadores: motor DC, TB6612, PWM | Video 2 sentidos / 3 velocidades + PWM mínimo |
| 5 | M1 | 2026-09-18 | Sensores: ADC, LM35 calibrado, MPU6050, promedio móvil | Curvas de calibración + captura Serial Plotter |
| 6 | M1 | 2026-09-25 | Bluetooth del ESP32 · protocolo de comandos | Tabla de protocolo + video de control desde celular |
| 7 | — | 2026-10-02 | **Kickoff Proyecto 1** · arquitectura, BOM, chasis con Proyectos 1 | Propuesta + BOM + riesgos |
| 8 | M2 | 2026-10-09 | Mecanismos · taller de estaciones con modelos impresos | Ficha de estaciones + hoja de ejercicios |
| 9 | — | 2026-10-16 | **Revisión de avance P1** + defensa de portafolio | Video de subsistemas + checklist R1–R8 |
| 10 | — | 2026-10-23 | **Entrega P1 + Torneo** de fútbol RC | Demo, reporte, velocidad real vs. teórica |
| 11 | M2 | 2026-10-30 | Control: lazo abierto vs. cerrado · PID · sintonía empírica | Secuencia en lazo abierto + tabla de sintonía + ganancias finales |
| 12 | M2 | 2026-11-06 | Visión I: HSV, centroide de la pelota · generación de marcadores ArUco | Detección de pelota + marcadores impresos |
| 13 | M2 | 2026-11-13 | Visión II: cierre de lazo (ArUco → PID → BT) | Video "llegar y detenerse" + FPS/latencia |
| 14 | — | 2026-11-20 | **Kickoff Proyecto Final** · VSSS simplificado, niveles N1–N4 | Propuesta con nivel objetivo + sprints |
| 15 | — | 2026-11-27 | **Revisión de avance PF** + defensa · sesión colchón | Video N1 + bitácora de sintonía |
| 16 | — | 2026-12-04 | **Entrega PF + Torneo VSSS inter-grupos** 🏆 | Demo por nivel + portafolio final + reflexión individual |


**Fechas administrativas que nos tocan** (del calendario oficial): registro de calificaciones intrasemestrales — 1er periodo del 17 al 22 sep (con las prácticas de las sesiones 1–4), 2º periodo del 19 al 23 oct (con la entrega del Proyecto 1); registro de calificaciones finales del 7 al 9 dic (justo después del torneo del 4 dic); último día para baja total: 20 nov.
