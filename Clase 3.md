# Modelado de Sistemas y Análisis de Control

Este documento profundiza en los conceptos fundamentales para el análisis de sistemas de control, cubriendo desde la formulación de ecuaciones diferenciales hasta el análisis de polos y ceros en el dominio de Laplace. A continuación, se detallan cada uno de los temas esenciales, con ejemplos y explicaciones.

---

## 1. Ecuación Diferencial de un Modelo

### **Descripción del Modelo**

Las ecuaciones diferenciales son herramientas fundamentales en el modelado de sistemas dinámicos. Estas ecuaciones describen cómo una o más variables de salida cambian en función de una o más variables de entrada, bajo ciertas condiciones. En los sistemas mecánicos, por ejemplo, estas ecuaciones permiten analizar cómo fuerzas externas afectan a un objeto o estructura.

Uno de los ejemplos más comunes es el **sistema masa-resorte-amortiguador**, que es un modelo clásico en física y control, representando un sistema con fricción, elasticidad y una masa sometida a fuerzas externas.

### **Ecuación Diferencial**

Para este sistema, la ecuación que describe el movimiento de la masa es:

$$
m \ddot{x}(t) + b \dot{x}(t) + k x(t) = F(t)
$$

Donde:
- $m$ es la masa del objeto (en kg), que determina la inercia del sistema.
- $b$ es el coeficiente de amortiguamiento (en Ns/m), que describe la resistencia al movimiento debido a fricción u otras fuerzas disipativas.
- $k$ es la constante del resorte (en N/m), que describe la elasticidad del resorte.
- $x(t)$ es el desplazamiento de la masa con respecto a la posición de equilibrio (en metros).
- $\dot{x}(t)$ es la velocidad, que es la derivada de $x(t)$ con respecto al tiempo.
- $\ddot{x}(t)$ es la aceleración, que es la segunda derivada de $x(t)$ con respecto al tiempo.
- $F(t)$ es la fuerza externa aplicada al sistema (en Newtons).

Esta ecuación diferencial describe cómo la masa se desplaza en función de las fuerzas externas, la fricción y la elasticidad del resorte.

---

## 2. Transformada Inversa de Laplace

### **Transformada de Laplace**

La **Transformada de Laplace** es una herramienta matemática que convierte una función del tiempo $f(t)$, en el dominio del tiempo, en una función del complejo $s$ en el dominio de Laplace. Esto facilita el análisis y la resolución de ecuaciones diferenciales, ya que convierte las derivadas en términos algebraicos.

La transformada de Laplace de una función $f(t)$, denotada como $F(s)$, se define como:

$$
F(s) = \mathcal{L}\{f(t)\} = \int_{0}^{\infty} f(t) e^{-st} \, dt
$$

Donde:
- $s$ es una variable compleja, $s = \sigma + j\omega$, que permite analizar la estabilidad de los sistemas.
- $e^{-st}$ es el factor de decaimiento exponencial, que describe el comportamiento de las funciones en el dominio complejo.

### **Transformada Inversa de Laplace**

La transformada inversa de Laplace es el proceso inverso: permite convertir una función del dominio de Laplace de vuelta al dominio del tiempo.

Por ejemplo, si tenemos la función en el dominio de Laplace:

$$
F(s) = \frac{1}{s^2 + 2s + 5}
$$

La transformada inversa de Laplace nos da la solución en el dominio del tiempo:

$$
f(t) = e^{-t} \sin(t)
$$

Este resultado muestra cómo un sistema oscilatorio puede decaer con el tiempo, lo cual es característico en muchos sistemas físicos.

---

## 3. Función de Transferencia

### **Definición**

La **función de transferencia** de un sistema dinámico es una representación algebraica que relaciona la entrada y la salida del sistema en el dominio de Laplace, bajo la suposición de que las condiciones iniciales son cero. Esta función simplifica el análisis de sistemas lineales al eliminar la necesidad de resolver las ecuaciones diferenciales directamente.

La función de transferencia $H(s)$ se define como la relación entre la transformada de Laplace de la salida $Y(s)$ y la entrada $U(s)$:

$$
H(s) = \frac{Y(s)}{U(s)}
$$

Donde:
- $Y(s)$ es la transformada de Laplace de la salida $y(t)$.
- $U(s)$ es la transformada de Laplace de la entrada $u(t)$.

### **Ejemplo: Sistema Masa-Resorte-Amortiguador**

En el caso del sistema masa-resorte-amortiguador, la función de transferencia $H(s)$ es:

$$
H(s) = \frac{X(s)}{F(s)} = \frac{1}{ms^2 + bs + k}
$$

Aquí:
- $X(s)$ es la transformada de Laplace del desplazamiento de la masa.
- $F(s)$ es la transformada de Laplace de la fuerza aplicada.

---

## 4. Funciones Propias, Impropias y Estrictamente Propias

Las funciones de transferencia se pueden clasificar en tres tipos según la relación entre los grados del numerador y el denominador:

### Función Propia
El grado del numerador es igual al grado del denominador. Los sistemas con funciones propias son generalmente estables y no tienden a generar oscilaciones no deseadas.

**Ejemplo de función propia:**

$$
H(s) = \frac{s^2 + 1}{s^2 + 3s + 2}
$$

Aquí, el grado del numerador (1) es igual que el grado del denominador (1), por lo que es una función propia.

### Función Impropia
El grado del numerador es mayor que el grado del denominador. Los sistemas con funciones impropias tienden a ser inestables o no realizables físicamente.

**Ejemplo de función impropia:**

$$
H(s) = \frac{s^2 + 2s + 1}{s + 3}
$$

En este caso, el grado del numerador (2) es mayor que el grado del denominador (1), lo que clasifica la función como impropia.

### Función Estrictamente Propia
El grado del numerador es estrictamente menor que el grado del denominador. Este tipo de función asegura que el sistema tiene una respuesta estable y controlable, siendo común en sistemas físicos reales.

**Ejemplo de función estrictamente propia:**

$$
H(s) = \frac{1}{s^2 + 2s + 1}
$$

En este caso, el grado del numerador (0) es estrictamente menor que el grado del denominador (2), lo que clasifica la función como estrictamente propia.


---

### **Resumen**

- **Función propia**: El grado del numerador es menor o igual que el del denominador.
- **Función estrictamente propia**: El grado del numerador es estrictamente menor que el del denominador.
- **Función impropia**: El grado del numerador es mayor que el del denominador.


---

## 5. Polos y Cerros

### **Definición de Polos y Ceros**

- **Polos:** Son los valores de $s$ que hacen que el denominador de la función de transferencia sea cero. Los polos son esenciales para determinar la estabilidad del sistema y su comportamiento en el tiempo.

- **Ceros:** Son los valores de $s$ que hacen que el numerador de la función de transferencia sea cero. Los ceros afectan la magnitud de la respuesta del sistema y pueden modificar su frecuencia de resonancia.

### **Ejemplo: Sistema Masa-Resorte-Amortiguador**

Consideremos la función de transferencia:

$$
H(s) = \frac{s + 2}{s^2 + 3s + 2}
$$

- **Polos:** Son los valores de $s$ que satisfacen la ecuación $s^2 + 3s + 2 = 0$. Resolviendo esta ecuación cuadrática, encontramos que los polos son $s = -1$ y $s = -2$.
  
- **Ceros:** Son los valores de $s$ que satisfacen $s + 2 = 0$, lo que da como resultado $s = -2$.

### **Importancia de Polos y Ceros**

El análisis de polos y ceros es crucial para comprender la estabilidad y la respuesta dinámica de un sistema. Los polos determinan la estabilidad (si están en el semiplano izquierdo, el sistema es estable), mientras que los ceros afectan la forma y la amplitud de la respuesta a las señales de entrada.

---

## Conclusión

El modelado de sistemas mediante ecuaciones diferenciales, transformadas de Laplace y funciones de transferencia es fundamental para el análisis y diseño de sistemas dinámicos. Además, el estudio de las funciones propias, impropias y estrictamente propias, junto con el análisis de polos y ceros, proporciona herramientas poderosas para caracterizar y controlar el comportamiento dinámico de los sistemas.

---

## Referencias

- Ogata, K. "Ingeniería de Control Moderna".
- Dorf, R. "Sistemas de Control Automático".
