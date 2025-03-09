# Sistemas de Control

Este documento contiene apuntes sobre **Sistemas de Control**, abordando la obtención de ecuaciones diferenciales a partir de modelos físicos en distintos dominios. Se incluyen ejemplos detallados y aplicaciones de cada sistema.

## 1. Sistema Masa-Resorte-Amortiguador

### Descripción del Sistema

Un sistema masa-resorte-amortiguador es un modelo fundamental en el estudio de sistemas mecánicos traslacionales. Este sistema está compuesto por:

- Una **masa** \( m \) que puede moverse en una dirección sobre una superficie sin fricción.
- Un **resorte** con constante elástica \( k \) que genera una fuerza de restitución proporcional al desplazamiento.
- Un **amortiguador** con coeficiente de amortiguamiento \( b \) que disipa la energía del sistema reduciendo la velocidad.
- Una **fuerza externa** \( F(t) \) que actúa sobre la masa para excitar el sistema.

### Ecuación Diferencial

Aplicando la Segunda Ley de Newton, la sumatoria de fuerzas en la dirección del movimiento es:

$$
F(t) - b \dot{x} - kx = m x''
$$

Reordenando:

$$
m x'' + b \dot{x} + kx = F(t)
$$

Donde:

- \( x \) es el desplazamiento de la masa.
- \dot{x} es la velocidad.
- \( x'' \) es la aceleración.

### Solución de la Ecuación

La solución general depende de las condiciones iniciales y del tipo de excitación aplicada al sistema. Se pueden analizar tres casos:

1. **Respuesta libre sin amortiguamiento** (\( b = 0 \)): Movimiento oscilatorio con frecuencia natural \( \omega_n = \frac{k}{m} \).
2. **Respuesta libre con amortiguamiento** (\( b > 0 \)): Movimiento amortiguado con diferentes regímenes (subamortiguado, críticamente amortiguado, sobreamortiguado).
3. **Respuesta forzada** (\( F(t) \neq 0 \)): Respuesta en régimen permanente dependiendo de la excitación externa.

### Aplicaciones Prácticas

- Diseño de **suspensiones en automóviles**.
- **Amortiguadores** en estructuras para mitigar efectos sísmicos.
- Control de **vibraciones en maquinaria industrial**.

---

## 2. Circuitos RLC

### Descripción del Sistema

Un **circuito RLC** es un sistema eléctrico que puede modelarse mediante una ecuación diferencial análoga a la de sistemas mecánicos. Sus componentes son:

- **Resistor** de resistencia \( R \), que disipa energía en forma de calor.
- **Inductor** con inductancia \( L \), que almacena energía en un campo magnético y genera una fuerza electromotriz en respuesta a cambios de corriente.
- **Capacitor** con capacitancia \( C \), que almacena energía en un campo eléctrico y afecta la distribución de voltaje.
- **Fuente de voltaje** \( V(t) \), que excita el circuito.

### Ecuación Diferencial

Aplicando la Ley de Kirchhoff de voltajes, la suma de caídas de voltaje en los componentes es igual a la tensión aplicada:

$$
V(t) = L \frac{d^2 i}{dt^2} + R \frac{di}{dt} + \frac{1}{C} i
$$

Reordenando:

$$
L \frac{d^2 i}{dt^2} + R \frac{di}{dt} + \frac{1}{C} i = \frac{dV}{dt}
$$

Donde:

- \( i \) es la corriente en el circuito.
- \frac{di}{dt} es la tasa de cambio de la corriente.
- \frac{d^2 i}{dt^2} es la segunda derivada de la corriente con respecto al tiempo.

---

## Conclusión

Cada uno de estos sistemas puede ser representado mediante **ecuaciones diferenciales de segundo orden**. La solución de estas ecuaciones permite predecir el comportamiento dinámico del sistema y diseñar controladores adecuados para lograr respuestas deseadas. Además, las ecuaciones pueden transformarse al **dominio de Laplace**, lo que facilita su análisis y la obtención de funciones de transferencia.

El estudio de estos sistemas es clave para el diseño de estrategias de control que optimicen la **estabilidad** y **desempeño** de diversos procesos físicos y tecnológicos.
