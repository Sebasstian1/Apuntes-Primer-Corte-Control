# Análisis de Sistemas Dinámicos y Control

Este documento aborda los conceptos fundamentales sobre ecuaciones diferenciales, transformadas de Laplace, funciones de transferencia, clasificación de funciones según su grado, y el análisis de polos y ceros en sistemas dinámicos.

---

## 1. Ecuación Diferencial de un Modelo

Las ecuaciones diferenciales son fundamentales para describir el comportamiento de sistemas dinámicos. A continuación, se presenta un ejemplo clásico con un sistema de masa-resorte-amortiguador, modelado por una ecuación diferencial de segundo orden.

### **Modelo de Sistema Masa-Resorte-Amortiguador**

La ecuación diferencial que describe este sistema es la siguiente:

$$
m \frac{d^2x(t)}{dt^2} + b \frac{dx(t)}{dt} + k x(t) = F(t)
$$

Donde:
- \( m \) es la masa del objeto.
- \( b \) es el coeficiente de amortiguamiento.
- \( k \) es la constante del resorte.
- \( x(t) \) es el desplazamiento de la masa en el tiempo.
- \( \frac{dx(t)}{dt} \) es la velocidad.
- \( \frac{d^2x(t)}{dt^2} \) es la aceleración.
- \( F(t) \) es la fuerza externa aplicada.

Esta ecuación diferencial describe cómo la masa responde a la fuerza aplicada, teniendo en cuenta las fuerzas de amortiguamiento y elasticidad.

---

## 2. Transformada Inversa de Laplace

### **Definición de Transformada de Laplace**

La transformada de Laplace es una técnica matemática utilizada para convertir funciones del tiempo en funciones del dominio de Laplace, lo cual facilita su análisis en sistemas lineales.

La transformada de Laplace de una función \( f(t) \) es:

$$
F(s) = \mathcal{L}\{f(t)\} = \int_0^\infty f(t) e^{-st} dt
$$

Donde \( s \) es una variable compleja \( s = \sigma + j\omega \).

### **Transformada Inversa de Laplace**

La transformada inversa de Laplace nos permite regresar del dominio de Laplace al dominio del tiempo. Por ejemplo, para la siguiente función en el dominio de Laplace:

$$
F(s) = \frac{1}{s^2 + 2s + 5}
$$

La transformada inversa de Laplace es:

$$
f(t) = e^{-t} \sin(t)
$$

Este resultado es obtenido a partir de tablas de transformadas inversas o fracciones parciales.

---

## 3. Función de Transferencia

### **Definición de Función de Transferencia**

La función de transferencia describe la relación entre la entrada y la salida de un sistema en el dominio de Laplace, bajo la suposición de que las condiciones iniciales son cero.

La función de transferencia \( H(s) \) se define como:

$$
H(s) = \frac{Y(s)}{U(s)}
$$

Donde:
- \( Y(s) \) es la transformada de Laplace de la salida \( y(t) \).
- \( U(s) \) es la transformada de Laplace de la entrada \( u(t) \).

### **Ejemplo de Sistema Masa-Resorte-Amortiguador**

La función de transferencia de un sistema masa-resorte-amortiguador es:

$$
H(s) = \frac{1}{ms^2 + bs + k}
$$

Esta función describe cómo la entrada (fuerza aplicada) afecta a la salida (desplazamiento de la masa) en el dominio de Laplace.

---

## 4. Funciones Propias, Impropias y Estrictamente Propias

### **Definición de Funciones Propias, Impropias y Estrictamente Propias**

Las funciones de transferencia se clasifican según la relación entre los grados del numerador y del denominador.

- **Función Propia:** El grado del numerador es menor o igual al grado del denominador.

  Ejemplo de **función propia**:

  $$ 
  H(s) = \frac{s + 1}{s^2 + 3s + 2}
  $$

  Aquí, el grado del numerador (1) es menor que el grado del denominador (2).

- **Función Impropia:** El grado del numerador es mayor que el grado del denominador.

  Ejemplo de **función impropia**:

  $$ 
  H(s) = \frac{s^2 + 2s + 1}{s + 3}
  $$

  El grado del numerador (2) es mayor que el grado del denominador (1).

- **Función Estrictamente Propia:** El grado del numerador es estrictamente menor que el grado del denominador.

  Ejemplo de **función estrictamente propia**:

  $$ 
  H(s) = \frac{1}{s^2 + 2s + 1}
  $$

  El grado del numerador (0) es estrictamente menor que el grado del denominador (2).

---

## 5. Polos y Ceros

### **Definición de Polos y Ceros**

Los **polos** son los valores de \( s \) que hacen que el denominador de la función de transferencia sea igual a cero. Los **ceros** son los valores de \( s \) que hacen que el numerador sea igual a cero.

### **Ejemplo de Análisis de Polos y Ceros**

Consideremos la función de transferencia:

$$
H(s) = \frac{s + 2}{s^2 + 3s + 2}
$$

- **Polos:** Son los valores de \( s \) que hacen que el denominador sea igual a cero. Resolviendo \( s^2 + 3s + 2 = 0 \), encontramos los polos en \( s = -1 \) y \( s = -2 \).
- **Ceros:** Son los valores de \( s \) que hacen que el numerador sea igual a cero. Resolviendo \( s + 2 = 0 \), encontramos un cero en \( s = -2 \).

### **Importancia de Polos y Ceros**

El análisis de polos y ceros es esencial para entender las propiedades dinámicas de un sistema. Los polos determinan la estabilidad del sistema, mientras que los ceros afectan su respuesta en frecuencia.

---

## Conclusión

El modelado y análisis de sistemas dinámicos mediante ecuaciones diferenciales y la transformada de Laplace es fundamental para el diseño de sistemas de control. Las funciones de transferencia, el análisis de funciones propias, impropias y estrictamente propias, y el estudio de polos y ceros proporcionan una comprensión profunda del comportamiento de los sistemas y son herramientas esenciales en la ingeniería de control.

---

## Referencias

- Ogata, K. "Ingeniería de Control Moderna".
- Dorf, R. "Sistemas de Control Automático".
