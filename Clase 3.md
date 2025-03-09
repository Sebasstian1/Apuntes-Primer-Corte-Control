# Modelado de Sistemas y Análisis de Control

Este documento profundiza en los conceptos fundamentales para el análisis de sistemas de control, cubriendo desde la formulación de ecuaciones diferenciales hasta el análisis de polos y ceros en el dominio de Laplace. A continuación, se detallan cada uno de los temas esenciales, con ejemplos y explicaciones.

---

## 1. Ecuación Diferencial de un Modelo

### **Descripción del Modelo**

Las ecuaciones diferenciales se utilizan para modelar sistemas dinámicos, donde el comportamiento de un sistema se describe mediante una relación matemática entre las variables de entrada y salida. 

Consideremos un sistema mecánico de masa-resorte-amortiguador, un modelo clásico en física y control. La dinámica de este sistema se describe mediante la segunda ley de Newton.

### **Ecuación Diferencial**

La ecuación que gobierna el movimiento de la masa en este sistema es:

$$
m \cdot \frac{d^2 x(t)}{dt^2} + b \cdot \frac{dx(t)}{dt} + k \cdot x(t) = F(t)
$$

Donde:
- \(m\) es la masa del objeto, representando la inercia del sistema.
- \(b\) es el coeficiente de amortiguamiento, que describe la resistencia al movimiento debido a fricción u otras fuerzas disipativas.
- \(k\) es la constante del resorte, que describe la elasticidad del resorte.
- \(x(t)\) es el desplazamiento de la masa en el tiempo.
- \(\frac{dx(t)}{dt}\) es la velocidad (derivada de \(x(t)\)), y \(\frac{d^2 x(t)}{dt^2}\) es la aceleración (segunda derivada de \(x(t)\)).
- \(F(t)\) es la fuerza externa aplicada al sistema.

Esta ecuación describe cómo la masa se mueve en función de las fuerzas aplicadas, la resistencia al movimiento y la elasticidad del resorte.

---

## 2. Transformada Inversa de Laplace

### **Transformada de Laplace**

La transformada de Laplace se usa para convertir funciones del dominio del tiempo (señales temporales) en funciones del dominio de Laplace, que es más conveniente para el análisis de sistemas lineales.

La transformada de Laplace de una función \(f(t)\), denotada como \(F(s)\), se define como:

$$
F(s) = \int_{0}^{\infty} f(t) \cdot e^{-st} \, dt
$$

Donde:
- \(s\) es una variable compleja, \(s = \sigma + j\omega\), que se utiliza en el dominio de Laplace.
- \(e^{-st}\) es el factor de decaimiento exponencial.

### **Transformada Inversa de Laplace**

La transformada inversa de Laplace permite regresar del dominio de Laplace al dominio del tiempo. Un ejemplo práctico es el siguiente:

Si tenemos la función en el dominio de Laplace:

$$
F(s) = \frac{1}{s^2 + 2s + 5}
$$

La transformada inversa de esta función nos da la solución en el dominio del tiempo:

$$
f(t) = e^{-t} \cdot \sin(t)
$$

Este resultado se puede obtener mediante tablas de transformadas inversas de Laplace o usando fracciones parciales, y muestra cómo un sistema oscilatorio decae con el tiempo.

---

## 3. Función de Transferencia

### **Definición**

La función de transferencia de un sistema dinámico es una representación algebraica que relaciona la entrada y la salida del sistema en el dominio de Laplace, bajo la suposición de que las condiciones iniciales son nulas. Es útil para estudiar la respuesta del sistema sin necesidad de resolver las ecuaciones diferenciales directamente.

La función de transferencia \(H(s)\) se define como la relación entre la transformada de Laplace de la salida y la entrada:

$$
H(s) = \frac{Y(s)}{U(s)}
$$

Donde:
- \(Y(s)\) es la transformada de Laplace de la salida \(y(t)\).
- \(U(s)\) es la transformada de Laplace de la entrada \(u(t)\).

### **Ejemplo: Sistema Masa-Resorte-Amortiguador**

Para el sistema masa-resorte-amortiguador, la función de transferencia \(H(s)\) es:

$$
H(s) = \frac{1}{ms^2 + bs + k}
$$

Aquí, \(X(s)\) es la transformada de Laplace de la salida, que es el desplazamiento de la masa, y \(F(s)\) es la transformada de Laplace de la entrada, que es la fuerza aplicada. Esta función describe cómo la entrada afecta a la salida en el dominio de Laplace.

---

## 4. Funciones Propias, Impropias y Estrictamente Propias

### **Definición**

Las funciones de transferencia pueden clasificarse en tres tipos según la relación entre los grados del numerador y el denominador:

- **Función Propia:** El grado del numerador es menor o igual que el grado del denominador. Esto significa que el sistema es "estable" y su salida no crece más rápido que la entrada.

  Ejemplo de **función propia**:

  $$
  H(s) = \frac{s + 1}{s^2 + 3s + 2}
  $$

  En este caso, el grado del numerador (1) es menor que el grado del denominador (2), por lo que es una función **propia**.

- **Función Impropia:** El grado del numerador es mayor que el grado del denominador. Esto indica que el sistema tiene un comportamiento "inestable", y la salida puede crecer más rápido que la entrada.

  Ejemplo de **función impropia**:

  $$
  H(s) = \frac{s^2 + 2s + 1}{s + 3}
  $$

  El grado del numerador (2) es mayor que el grado del denominador (1), por lo que es una función **impropia**.

- **Función Estrictamente Propia:** El grado del numerador es estrictamente menor que el grado del denominador. Este tipo de función es "más estable" y es común en sistemas físicos reales.

  Ejemplo de **función estrictamente propia**:

  $$
  H(s) = \frac{1}{s^2 + 2s + 1}
  $$

  Aquí, el grado del numerador (0) es estrictamente menor que el grado del denominador (2), por lo que es estrictamente **propia**.

---

## 5. Polos y Cerros

### **Definición de Polos y Ceros**

- **Polos:** Son los valores de \(s\) que hacen que el denominador de la función de transferencia sea cero. Los polos indican los puntos donde la salida del sistema puede volverse infinita. Son esenciales para analizar la estabilidad de un sistema.
  
- **Ceros:** Son los valores de \(s\) que hacen que el numerador de la función de transferencia sea cero. Los ceros indican los puntos donde la salida es nula, incluso si la entrada no lo es.

### **Ejemplo: Sistema Masa-Resorte-Amortiguador**

Para la función de transferencia:

$$
H(s) = \frac{s + 2}{s^2 + 3s + 2}
$$

- **Polos:** Son los valores de \(s\) que satisfacen la ecuación del denominador \(s^2 + 3s + 2 = 0\). Resolviendo la ecuación cuadrática, encontramos los polos en \(s = -1\) y \(s = -2\).
- **Ceros:** Son los valores de \(s\) que satisfacen la ecuación del numerador \(s + 2 = 0\), dando como solución \(s = -2\).

### **Importancia de Polos y Ceros**

El análisis de polos y ceros es fundamental para determinar las propiedades dinámicas de un sistema, como su estabilidad, resonancia y respuesta a distintas frecuencias.

---

## Conclusión

El modelado de sistemas utilizando ecuaciones diferenciales y la posterior transformación al dominio de Laplace es esencial para analizar y diseñar sistemas dinámicos. La función de transferencia es una herramienta poderosa para estudiar cómo un sistema responde a diversas entradas. Además, el análisis de las funciones como propias, impropias o estrictamente propias, junto con el estudio de los polos y ceros, proporciona información clave sobre la estabilidad y el comportamiento dinámico del sistema.

---

## Referencias

- Ogata, K. "Ingeniería de Control Moderna".
- Dorf, R. "Sistemas de Control Automático".
