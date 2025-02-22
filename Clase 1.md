# Sistemas de Control

Este documento contiene apuntes sobre Sistemas de Control, abordando la obtención de ecuaciones diferenciales a partir de modelos físicos en distintos dominios. Se incluyen ejemplos detallados y aplicaciones de cada sistema.

---

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

### **Solución de la Ecuación**

La solución general depende de las condiciones iniciales y del tipo de excitación aplicada al sistema. Se pueden analizar tres casos:

1. **Respuesta libre sin amortiguamiento ($b = 0$):** Movimiento oscilatorio con frecuencia natural $\omega_n = \sqrt{k/m}$.
2. **Respuesta libre con amortiguamiento ($b > 0$):** Movimiento amortiguado con diferentes regímenes (subamortiguado, críticamente amortiguado, sobreamortiguado).
3. **Respuesta forzada ($F(t) \neq 0$):** Respuesta en régimen permanente dependiendo de la excitación externa.

### **Aplicaciones Prácticas**

- Diseño de suspensiones en automóviles.
- Amortiguadores en estructuras para mitigar efectos sísmicos.
- Control de vibraciones en maquinaria industrial.

---

## 2. Sistemas Rotacionales

### **Descripción del Sistema**

Los sistemas rotacionales son equivalentes a los sistemas traslacionales, pero en términos de parámetros rotacionales. Se encuentran en aplicaciones como motores eléctricos, sistemas de transmisión mecánica y robots industriales. Los elementos principales del sistema son:

- **Momento de inercia $J$**, que representa la resistencia del sistema al cambio en su velocidad angular.
- **Coeficiente de amortiguamiento rotacional $B$**, que modela pérdidas de energía debido a fricción y resistencia del aire.
- **Constante de torsión del resorte $K$**, que almacena energía en forma de deformación elástica.
- **Torque aplicado $T(t)$**, que actúa como fuerza externa para inducir movimiento.

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

### **Ejemplos y Aplicaciones**

- **Motores eléctricos:** El comportamiento de los motores de corriente continua puede modelarse con esta ecuación.
- **Sistemas de control de velocidad:** En robótica, se usa para diseñar servomecanismos.
- **Péndulos físicos y giroscopios:** Se modelan como sistemas rotacionales.

---

## 3. Circuitos RLC

### **Descripción del Sistema**

Un circuito RLC es un sistema eléctrico que puede modelarse mediante una ecuación diferencial análoga a la de sistemas mecánicos. Se utiliza en filtros eléctricos, osciladores y circuitos de acondicionamiento de señales. Sus componentes son:

- **Resistor de resistencia $R$**, que disipa energía en forma de calor.
- **Inductor con inductancia $L$**, que almacena energía en un campo magnético y genera una fuerza electromotriz en respuesta a cambios de corriente.
- **Capacitor con capacitancia $C$**, que almacena energía en un campo eléctrico y afecta la distribución de voltaje.
- **Fuente de voltaje $V(t)$**, que excita el circuito.

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

### **Tipos de Respuesta**

- **Subamortiguado ($R$ pequeño):** Oscilaciones con atenuación progresiva.
- **Críticamente amortiguado ($R$ óptimo):** Retorno más rápido sin oscilaciones.
- **Sobreamortiguado ($R$ grande):** Respuesta lenta sin oscilaciones.

### **Aplicaciones**

- **Filtros pasa-banda y pasa-bajos:** Diseñados con circuitos RLC.
- **Osciladores eléctricos:** Utilizados en radios y telecomunicaciones.
- **Sistemas de transmisión de energía:** Estabilidad en líneas de alta tensión.

---

## Conclusión

Cada uno de estos sistemas puede ser representado mediante ecuaciones diferenciales de segundo orden. La solución de estas ecuaciones permite predecir el comportamiento dinámico del sistema y diseñar controladores adecuados para lograr respuestas deseadas. Además, las ecuaciones pueden transformarse al dominio de Laplace, lo que facilita su análisis y la obtención de funciones de transferencia. 

El estudio de estos sistemas es clave para el diseño de estrategias de control que optimicen la estabilidad y desempeño de diversos procesos físicos y tecnológicos.

---

## Referencias
- Ogata, K. "Ingeniería de Control Moderna".
- Dorf, R. "Sistemas de Control Automático".
