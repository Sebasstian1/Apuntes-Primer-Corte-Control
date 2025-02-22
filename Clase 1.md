# Sistemas de Control

Este documento contiene apuntes sobre Sistemas de Control, abordando la obtención de ecuaciones diferenciales a partir de modelos físicos en distintos dominios.

## 1. Sistema Masa-Resorte-Amortiguador

### **Descripción del Sistema**

Un sistema masa-resorte-amortiguador es un modelo fundamental en el estudio de sistemas mecánicos traslacionales. Se encuentra en aplicaciones como la suspensión de automóviles, sistemas de absorción de vibraciones y estructuras sometidas a cargas dinámicas. Este sistema está compuesto por:

- Una masa $m$ que puede moverse en una dirección sobre una superficie sin fricción.
- Un resorte con constante elástica $k$ que genera una fuerza de restitución proporcional al desplazamiento.
- Un amortiguador con coeficiente de amortiguamiento $b$ que disipa la energía del sistema reduciendo la velocidad.
- Una fuerza externa $F(t)$ que actúa sobre la masa para excitar el sistema.

### **Ecuación Diferencial**

Aplicando la Segunda Ley de Newton, la sumatoria de fuerzas en la dirección del movimiento es:

$$
F(t) - b \dot{x} - kx = m \ddot{x}
$$

Reordenando:

$$
 m \ddot{x} + b \dot{x} + k x = F(t)
$$

Donde:
- $x$ es el desplazamiento de la masa.
- $\dot{x} = \frac{dx}{dt}$ es la velocidad.
- $\ddot{x} = \frac{d^2x}{dt^2}$ es la aceleración.

Esta ecuación diferencial de segundo orden describe la dinámica del sistema y se puede resolver mediante métodos analíticos o numéricos para obtener la respuesta temporal.

### **Ejemplo de Aplicación**

#### **Sistema con Dos Masas Acopladas**

Un sistema con dos masas acopladas mediante resortes y amortiguadores, como se muestra en la imagen adjunta, se describe mediante las siguientes ecuaciones:

Para la masa $m_1$:

$$
m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b_1 (\dot{x}_1 - \dot{x}_2) + u
$$

Para la masa $m_2$:

$$
m_2 \ddot{x}_2 = -k_2 (x_2 - x_1) + b_1 (\dot{x}_1 - \dot{x}_2)
$$

Donde:
- $x_1$ y $x_2$ son los desplazamientos de las masas.
- $b_1$ es el coeficiente de amortiguamiento asociado al resorte $k_2$.
- $u$ es una fuerza de entrada aplicada sobre $m_1$.

Este sistema representa un modelo útil para el análisis de vibraciones en estructuras y mecanismos acoplados.

---

## 2. Sistemas Rotacionales

### **Descripción del Sistema**

Los sistemas rotacionales son equivalentes a los sistemas traslacionales, pero en términos de parámetros rotacionales. Se encuentran en aplicaciones como motores eléctricos, sistemas de transmisión mecánica y robots industriales. Los elementos principales del sistema son:

- Momento de inercia $J$, que representa la resistencia del sistema al cambio en su velocidad angular.
- Coeficiente de amortiguamiento rotacional $B$, que modela pérdidas de energía debido a fricción y resistencia del aire.
- Constante de torsión del resorte $K$, que almacena energía en forma de deformación elástica.
- Torque aplicado $T(t)$, que actúa como fuerza externa para inducir movimiento.

### **Ecuación Diferencial**

Aplicando la ecuación de movimiento rotacional basada en la Segunda Ley de Newton para sistemas angulares:

$$
T(t) - B \dot{\theta} - K \theta = J \ddot{\theta}
$$

Reordenando:

$$
J \ddot{\theta} + B \dot{\theta} + K \theta = T(t)
$$

Donde:
- $\theta$ es el desplazamiento angular.
- $\dot{\theta} = \frac{d\theta}{dt}$ es la velocidad angular.
- $\ddot{\theta} = \frac{d^2\theta}{dt^2}$ es la aceleración angular.

Esta ecuación es fundamental para analizar la dinámica de sistemas de control rotacionales y diseñar mecanismos de regulación.

### **Ejemplo de Aplicación**

Un disco giratorio con un resorte de torsión y fricción rotacional tiene la ecuación:

$$
J \ddot{\theta} + B \dot{\theta} + K \theta = 0
$$

Este sistema es análogo a un oscilador armónico amortiguado.

---

## 3. Circuitos RLC

### **Descripción del Sistema**

Un circuito RLC es un sistema eléctrico que puede modelarse mediante una ecuación diferencial análoga a la de sistemas mecánicos. Se utiliza en filtros eléctricos, osciladores y circuitos de acondicionamiento de señales. Sus componentes son:

- Un resistor de resistencia $R$ que disipa energía en forma de calor.
- Un inductor con inductancia $L$, que almacena energía en un campo magnético y genera una fuerza electromotriz en respuesta a cambios de corriente.
- Un capacitor con capacitancia $C$, que almacena energía en un campo eléctrico y afecta la distribución de voltaje.
- Una fuente de voltaje $V(t)$ que excita el circuito.

### **Ecuación Diferencial**

Aplicando la Ley de Kirchhoff de voltajes, la suma de caídas de voltaje en los componentes es igual a la tensión aplicada:

$$
V(t) = L \frac{d^2 i}{dt^2} + R \frac{d i}{dt} + \frac{1}{C} i
$$

Reordenando:

$$
L \frac{d^2 i}{dt^2} + R \frac{d i}{dt} + \frac{1}{C} i = \frac{d V}{dt}
$$

Donde:
- $i$ es la corriente en el circuito.
- $\frac{d i}{dt}$ es la tasa de cambio de la corriente.
- $\frac{d^2 i}{dt^2}$ es la derivada segunda de la corriente con respecto al tiempo.

### **Ejemplo de Aplicación**

Un circuito serie con $R = 10\Omega$, $L = 1H$ y $C = 0.1F$ excitado por un voltaje $V(t) = 5\sin(2t)$ tiene la ecuación:

$$
\ddot{i} + 10 \dot{i} + 10 i = 10 \cos(2t)
$$

Este circuito puede analizarse en el dominio del tiempo o utilizando la Transformada de Laplace para obtener su respuesta en el dominio de la frecuencia.

---

## Conclusión

Cada uno de estos sistemas puede ser representado mediante ecuaciones diferenciales de segundo orden. La solución de estas ecuaciones permite predecir el comportamiento dinámico del sistema y diseñar controladores adecuados para lograr respuestas deseadas. Además, las ecuaciones pueden transformarse al dominio de Laplace, lo que facilita su análisis y la obtención de funciones de transferencia.

---

## Referencias
- Ogata, K. "Ingeniería de Control Moderna".
- Dorf, R. "Sistemas de Control Automático".
