# Modelado de Sistemas y Análisis de Control

Este documento cubre los conceptos fundamentales para el análisis de sistemas de control, incluyendo la formulación de ecuaciones diferenciales, la transformada inversa de Laplace, la función de transferencia, clasificación de funciones como propias, impropias o estrictamente propias, y el análisis de polos y ceros. Se presentan ejemplos y aplicaciones para facilitar la comprensión de cada tema.

---

## 1. Ecuación Diferencial de un Modelo

### **Descripción del Modelo**

Consideremos un sistema mecánico de masa-resorte-amortiguador. La ecuación diferencial que describe este sistema se obtiene a partir de la segunda ley de Newton.

### **Ecuación Diferencial**

La ecuación para el movimiento de la masa se puede escribir como:

$$
m \ddot{x} + b \dot{x} + k x = F(t)
$$

Donde:
- $m$ es la masa del objeto.
- $b$ es el coeficiente de amortiguamiento.
- $k$ es la constante del resorte.
- $x$ es el desplazamiento de la masa.
- $\dot{x}$ es la velocidad (derivada de $x$).
- $\ddot{x}$ es la aceleración (derivada de la velocidad).
- $F(t)$ es la fuerza externa aplicada al sistema.

---

## 2. Transformada Inversa de Laplace

La transformada inversa de Laplace se utiliza para convertir una función de Laplace en su representación en el dominio del tiempo.

### **Proceso de Transformada Inversa**

Dada una función $F(s)$ en el dominio de Laplace, la transformada inversa de Laplace, denotada como $\mathcal{L}^{-1}\{F(s)\}$, nos da la solución en el dominio del tiempo.

Por ejemplo, si tenemos:

$$
F(s) = \frac{1}{s^2 + 2s + 5}
$$

La transformada inversa se puede realizar utilizando tablas o métodos de fracciones parciales para obtener:

$$
f(t) = e^{-t} \sin(t)
$$

---

## 3. Función de Transferencia

### **Definición**

La función de transferencia $H(s)$ de un sistema es la relación entre la salida y la entrada de un sistema en el dominio de Laplace, con condiciones iniciales nulas.

Para el sistema masa-resorte-amortiguador, la función de transferencia se obtiene de la siguiente manera:

$$
H(s) = \frac{X(s)}{F(s)} = \frac{1}{ms^2 + bs + k}
$$

Donde:
- $X(s)$ es la transformada de Laplace de la salida $x(t)$.
- $F(s)$ es la transformada de Laplace de la entrada $F(t)$.
- $m$, $b$, y $k$ son los parámetros del sistema.

---

## 4. Funciones Propias, Impropias y Estrictamente Propias

### **Definición**

- **Función Propia:** Es aquella en la que el grado del numerador es menor o igual al grado del denominador.
- **Función Impropia:** Es aquella en la que el grado del numerador es mayor que el grado del denominador.
- **Función Estrictamente Propia:** Es aquella en la que el grado del numerador es estrictamente menor que el grado del denominador.

### **Ejemplos**

- **Función Propia:**

$$
H(s) = \frac{s + 1}{s^2 + 3s + 2}
$$

Aquí, el grado del numerador (1) es menor que el grado del denominador (2), por lo que es una función propia.

- **Función Impropia:**

$$
H(s) = \frac{s^2 + 2s + 1}{s + 3}
$$

En este caso, el grado del numerador (2) es mayor que el grado del denominador (1), por lo que es una función impropia.

- **Función Estrictamente Propia:**

$$
H(s) = \frac{1}{s^2 + 2s + 1}
$$

Aquí, el grado del numerador (0) es estrictamente menor que el grado del denominador (2), lo que la convierte en estrictamente propia.

---

## 5. Polos y Cerros

### **Definición**

- **Polos:** Son los valores de $s$ que hacen que el denominador de la función de transferencia sea cero.
- **Ceros:** Son los valores de $s$ que hacen que el numerador de la función de transferencia sea cero.

### **Ejemplos**

Para la función de transferencia:

$$
H(s) = \frac{s + 2}{s^2 + 3s + 2}
$$

- **Polos:** Son los valores de $s$ que satisfacen la ecuación $s^2 + 3s + 2 = 0$, que tiene como soluciones $s = -1$ y $s = -2$.
- **Ceros:** Son los valores de $s$ que satisfacen la ecuación $s + 2 = 0$, dando como solución $s = -2$.

---

## Conclusión

El análisis de sistemas de control requiere comprender cómo modelar sistemas con ecuaciones diferenciales, realizar transformaciones al dominio de Laplace, y analizar la función de transferencia para estudiar su comportamiento. El análisis de funciones propias, impropias y estrictamente propias, junto con los conceptos de polos y ceros, es esencial para entender la estabilidad y respuesta dinámica de los sistemas.

---

## Referencias

- Ogata, K. "Ingeniería de Control Moderna".
- Dorf, R. "Sistemas de Control Automático".

