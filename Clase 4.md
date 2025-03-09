# **Sistemas de Primer Orden y Análisis de Control**

Este documento aborda los sistemas de primer orden, su formulación y análisis, incluyendo la ecuación diferencial correspondiente, la forma canónica, y su respuesta temporal ante entradas escalón, rampa e impulso. También se analiza la ubicación de los polos y cómo afecta a la respuesta del sistema.

---

## 1. **Sistemas de Primer Orden**

### **Descripción de un Sistema de Primer Orden**

Un sistema de primer orden es un sistema dinámico cuya ecuación diferencial tiene la forma más sencilla, es decir, una ecuación diferencial de primer orden. Estos sistemas son comunes en muchas aplicaciones de ingeniería, como los sistemas térmicos, eléctricos, y de control de procesos.

La ecuación general de un sistema de primer orden es:

$$
\tau \frac{d}{dt} y(t) + y(t) = K u(t)
$$

- $\tau$ es la constante de tiempo (en segundos), que caracteriza la velocidad de la respuesta del sistema.
- $K$ es la ganancia del sistema.
- $u(t)$ es la entrada del sistema.
- $y(t)$ es la salida del sistema.

---

## 2. **Ecuación Diferencial de Primer Orden**

### **Ecuación Diferencial Estándar**

La ecuación diferencial estándar de un sistema de primer orden es:

$$
\tau \frac{dy(t)}{dt} + y(t) = K u(t)
$$

Esta ecuación muestra cómo la salida $y(t)$ depende del tiempo y de la entrada $u(t)$, y cómo las variables del sistema se relacionan mediante la constante de tiempo $\tau$.

---

## 3. **Forma Canónica de los Sistemas de Primer Orden**

### **Forma Canónica Estándar**

La forma canónica de un sistema de primer orden en términos de su función de transferencia es:

$$
H(s) = \frac{K}{\tau s + 1}
$$

Donde:
- $s$ es la variable compleja del dominio de Laplace.
- $K$ es la ganancia del sistema.
- $\tau$ es la constante de tiempo del sistema.

Esta forma es útil porque nos da una idea clara de cómo los parámetros del sistema (como $\tau$ y $K$) afectan la respuesta del sistema.

---

## 4. **Respuesta Temporal de un Sistema de Primer Orden ante una Entrada Escalón**

### **Entrada Escalón**

La respuesta temporal de un sistema de primer orden ante una entrada escalón, que se representa como:

$$
u(t) = 1 \quad \text{para} \quad t \geq 0
$$

Es conocida por su comportamiento asintótico, donde la salida $y(t)$ tiende a un valor final. La respuesta del sistema es:

$$
y(t) = K \left(1 - e^{-t/\tau}\right)
$$

Donde:
- $K$ es la ganancia del sistema.
- $\tau$ es la constante de tiempo.
- $e^{-t/\tau}$ representa la decayencia exponencial de la respuesta.

La respuesta es una curva que comienza en cero y se aproxima a un valor final de $K$ a medida que $t$ aumenta.

---

## 5. **Análisis de la Ubicación de Polos**

### **Ubicación de Polos en el Dominio de Laplace**

Los polos de un sistema son los valores de $s$ para los cuales el denominador de su función de transferencia se hace cero. En el caso de un sistema de primer orden, el sistema tiene un único polo que se encuentra en:

$$
s = -\frac{1}{\tau}
$$

Este valor determina la rapidez con la que el sistema responde a las entradas. Cuanto más negativo es el valor de $s$, más rápido es el sistema en alcanzar su valor final. El análisis de la ubicación de polos es fundamental para entender el comportamiento de la respuesta temporal de un sistema.

---

## 6. **Respuestas del Sistema a Diferentes Entradas**

### **Entrada Escalón**

La respuesta de un sistema de primer orden ante una entrada escalón es:

$$
y(t) = K \left(1 - e^{-t/\tau}\right)
$$

### **Entrada Rampa**

Para una entrada rampa, que se representa como:

$$
u(t) = t \quad \text{para} \quad t \geq 0
$$

La respuesta del sistema es:

$$
y(t) = K \tau \left( 1 - e^{-t/\tau} \right) + K t
$$

### **Entrada Impulso**

Para una entrada impulso, que se representa como:

$$
u(t) = \delta(t)
$$

La respuesta del sistema es una función impulsiva que genera una variación instantánea en la salida, determinada por:

$$
y(t) = K e^{-t/\tau}
$$

---

## Ejemplos de Cálculo de Respuestas

### **Ejemplo 1: Respuesta a una Entrada Escalón**

Si un sistema tiene $\tau = 5$ segundos y $K = 2$, la respuesta a una entrada escalón es:

$$
y(t) = 2 \left(1 - e^{-t/5}\right)
$$

Para $t = 10$ segundos, la salida será:

$$
y(10) = 2 \left(1 - e^{-10/5}\right) \approx 2 \left(1 - e^{-2}\right) \approx 2 \left(1 - 0.1353\right) \approx 1.7294
$$

---

## Conclusión

Los sistemas de primer orden son fundamentales en muchas aplicaciones de ingeniería y control. A través de este análisis, hemos aprendido cómo caracterizar estos sistemas mediante su ecuación diferencial, forma canónica, y cómo predecir su comportamiento ante entradas comunes como escalón, rampa e impulso. Además, el análisis de los polos y su ubicación es esencial para comprender cómo el sistema responderá en términos de velocidad y estabilidad.

