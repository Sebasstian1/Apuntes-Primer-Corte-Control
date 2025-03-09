# Apuntes sobre Sistemas de Control - Laboratorio

En esta clase de laboratorio, abordamos los mismos temas que discutimos en la **Clase 1**, pero con un enfoque más detallado en los **circuitos RLC** y su comportamiento. Repasamos los conceptos fundamentales de los sistemas de control, centrándonos especialmente en cómo los circuitos RLC pueden ser modelados y analizados mediante ecuaciones diferenciales.

## 1. Sistema Masa-Resorte-Amortiguador

**Descripción del Sistema:**  
Este sistema es clave en el estudio de sistemas mecánicos traslacionales y se utiliza en diversas aplicaciones como suspensiones de automóviles y control de vibraciones. Este sistema está compuesto por:

- Una **masa** \( m \) que puede moverse en una dirección sobre una superficie sin fricción.
- Un **resorte** con constante elástica \( k \) que genera una fuerza de restitución proporcional al desplazamiento.
- Un **amortiguador** con coeficiente de amortiguamiento \( b \) que disipa la energía del sistema reduciendo la velocidad.
- Una **fuerza externa** \( F(t) \) que actúa sobre la masa para excitar el sistema.

**Ecuación Diferencial:**  
Aplicando la Segunda Ley de Newton, la sumatoria de fuerzas en la dirección del movimiento es:

$$
F(t) - b \dot{x} - kx = mx''
$$

Reordenando:

$$
mx'' + b\dot{x} + kx = F(t)
$$

Donde:
- \( x \) es el desplazamiento de la masa.
- \( \dot{x} \) es la velocidad.
- \( x'' \) es la aceleración.

**Solución de la Ecuación:**  
La solución general depende de las condiciones iniciales y del tipo de excitación aplicada al sistema. Se pueden analizar tres casos:
- **Respuesta libre sin amortiguamiento** (\( b = 0 \)): Movimiento oscilatorio con frecuencia natural \( \omega_n = \frac{k}{m} \).
- **Respuesta libre con amortiguamiento** (\( b > 0 \)): Movimiento amortiguado con diferentes regímenes (subamortiguado, críticamente amortiguado, sobreamortiguado).
- **Respuesta forzada** (\( F(t) \neq 0 \)): Respuesta en régimen permanente dependiendo de la excitación externa.

**Aplicaciones Prácticas:**
- Diseño de suspensiones en automóviles.
- Amortiguadores en estructuras para mitigar efectos sísmicos.
- Control de vibraciones en maquinaria industrial.

## 2. Sistemas Rotacionales

**Descripción del Sistema:**  
Los sistemas rotacionales son equivalentes a los sistemas traslacionales, pero en términos de parámetros rotacionales. Se encuentran en aplicaciones como motores eléctricos, sistemas de transmisión mecánica y robots industriales. Los elementos principales del sistema son:
- **Momento de inercia** \( J \), que representa la resistencia del sistema al cambio en su velocidad angular.
- **Coeficiente de amortiguamiento rotacional** \( B \), que modela pérdidas de energía debido a fricción y resistencia del aire.
- **Constante de torsión del resorte** \( K \), que almacena energía en forma de deformación elástica.
- **Torque aplicado** \( T(t) \), que actúa como fuerza externa para inducir movimiento.

**Ecuación Diferencial:**  
Aplicando la ecuación de movimiento rotacional basada en la Segunda Ley de Newton para sistemas angulares:

$$
T(t) - B\dot{\theta} - K\theta = J\theta''
$$

Reordenando:

$$
J\theta'' + B\dot{\theta} + K\theta = T(t)
$$

Donde:
- \( \theta \) es el desplazamiento angular.
- \( \dot{\theta} \) es la velocidad angular.
- \( \theta'' \) es la aceleración angular.

**Ejemplos y Aplicaciones:**
- Motores eléctricos: El comportamiento de los motores de corriente continua puede modelarse con esta ecuación.
- Sistemas de control de velocidad: En robótica, se usa para diseñar servomecanismos.
- Péndulos físicos y giroscopios: Se modelan como sistemas rotacionales.

## 3. Circuitos RLC

**Descripción del Sistema:**  
En esta clase, nos enfocamos más a fondo en los **circuitos RLC**. Un **circuito RLC** es un sistema eléctrico compuesto por un **resistor**, un **inductor** y un **capacitor**. Se utiliza en aplicaciones como filtros, osciladores y acondicionadores de señales. Este tipo de circuito se utiliza frecuentemente en **comunicaciones**, **procesamiento de señales** y **generación de frecuencias**.

**Ecuación Diferencial:**  
Aplicando la Ley de Kirchhoff de voltajes, la suma de caídas de voltaje en los componentes es igual a la tensión aplicada:

$$
V(t) = L \frac{d^2i}{dt^2} + R \frac{di}{dt} + \frac{1}{C}i
$$

Reordenando:

$$
L \frac{d^2i}{dt^2} + R \frac{di}{dt} + \frac{1}{C}i = \frac{dV}{dt}
$$

Donde:
- \( i \) es la corriente en el circuito.
- \( \frac{di}{dt} \) es la tasa de cambio de la corriente.
- \( \frac{d^2i}{dt^2} \) es la derivada segunda de la corriente con respecto al tiempo.

**Tipos de Respuesta:**
- **Subamortiguado** (\( R \) pequeño): Oscilaciones con atenuación progresiva.
- **Críticamente amortiguado** (\( R \) óptimo): Respuesta más rápida sin oscilaciones.
- **Sobreamortiguado** (\( R \) grande): Respuesta lenta sin oscilaciones.

**Aplicaciones:**
- Filtros pasa-banda y pasa-bajos: Diseñados con circuitos RLC.
- Osciladores eléctricos: Utilizados en radios y telecomunicaciones.
- Sistemas de transmisión de energía: Estabilidad en líneas de alta tensión.

## Conclusión

Aunque en esta clase repasamos los mismos conceptos generales que en la **Clase 1**, nos centramos más en el análisis y comportamiento de los **circuitos RLC**, entendiendo cómo las ecuaciones diferenciales pueden modelar sistemas eléctricos y aplicarlas en el diseño de filtros, osciladores y otros componentes clave de sistemas de control.

La transformación de estas ecuaciones al dominio de **Laplace** y su posterior análisis es fundamental para comprender el comportamiento dinámico de los sistemas y diseñar controladores adecuados.
