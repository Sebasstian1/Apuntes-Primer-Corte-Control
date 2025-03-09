# Clase 2: Circuitos RLC en el Laboratorio

En esta clase en el laboratorio, continuamos explorando las funciones de transferencia, pero nos enfocamos en un análisis más detallado de los **circuitos RLC** y su relación con los conceptos de funciones propias, bipropias e impropias. Los circuitos RLC son circuitos eléctricos que contienen resistores (R), inductores (L) y capacitores (C), y son esenciales en el estudio de sistemas dinámicos.

### Circuitos RLC
Un circuito RLC puede presentarse en varias configuraciones: **serie** o **paralelo**. Los circuitos RLC se usan comúnmente para modelar comportamientos resonantes, como oscilaciones y filtrado de señales. A continuación, veremos cómo los elementos del circuito afectan la función de transferencia.

---

## Circuito RLC Serie

En un circuito RLC en serie, la resistencia (R), el inductor (L) y el capacitor (C) están conectados de forma secuencial. La función de transferencia del circuito RLC en serie se puede obtener analizando la impedancia total del sistema.

### Impedancia en un circuito RLC Serie

La impedancia total de un circuito RLC serie se calcula como:

$$
Z(s) = R + sL + \frac{1}{sC}
$$

Donde:
- \(R\) es la resistencia.
- \(L\) es la inductancia.
- \(C\) es la capacitancia.
- \(s\) es la variable compleja de Laplace.

### Función de Transferencia

La función de transferencia \(H(s)\) de un circuito RLC serie es la relación entre la salida y la entrada del sistema en el dominio de Laplace:

$$
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = \frac{1}{R + sL + \frac{1}{sC}}
$$

Donde:
- \(V_{out}(s)\) es la salida en el dominio de Laplace.
- \(V_{in}(s)\) es la entrada en el dominio de Laplace.

Esta función de transferencia describe cómo las señales de entrada se afectan al pasar por el circuito.

---

## Circuito RLC Paralelo

En un circuito RLC paralelo, la resistencia (R), el inductor (L) y el capacitor (C) están conectados en paralelo. La impedancia total de un circuito RLC paralelo se calcula de manera diferente.

### Impedancia en un circuito RLC Paralelo

La impedancia total de un circuito RLC paralelo es:

$$
Z(s) = \left( \frac{1}{R} + \frac{1}{sL} + sC \right)^{-1}
$$

### Función de Transferencia

La función de transferencia en el caso de un circuito RLC paralelo se obtiene de la siguiente manera:

$$
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = \frac{1}{\left( \frac{1}{R} + \frac{1}{sL} + sC \right)}
$$

---

### Análisis de Estabilidad y Frecuencia de Resonancia

En ambos tipos de circuitos, el comportamiento de la función de transferencia depende de la frecuencia de operación. Cuando la frecuencia se acerca a la **frecuencia de resonancia**, que se define como:

$$
f_0 = \frac{1}{2\pi \sqrt{LC}}
$$

El circuito muestra un comportamiento resonante, lo que significa que puede amplificar o filtrar señales dependiendo de su configuración.

---

## Resumen de Funciones de Transferencia en Circuitos RLC

- **Circuito RLC Serie**: La función de transferencia está dada por:

  $$
  H(s) = \frac{1}{R + sL + \frac{1}{sC}}
  $$

- **Circuito RLC Paralelo**: La función de transferencia está dada por:

  $$
  H(s) = \frac{1}{\left( \frac{1}{R} + \frac{1}{sL} + sC \right)}
  $$

### Tipos de Funciones

Las funciones de transferencia para los circuitos RLC pueden clasificarse de manera similar a otros sistemas:

- **Función propia**: Cuando el grado del numerador es menor que el del denominador.
- **Función bipropia**: Cuando el grado del numerador es igual al del denominador.
- **Función impropia**: Cuando el grado del numerador es mayor que el del denominador.
- **Función estrictamente propia**: Cuando el grado del numerador es estrictamente menor que el del denominador.

Los circuitos RLC pueden tener funciones propias, bipropias o impropias dependiendo de la relación entre la inductancia, la capacitancia y la resistencia del circuito.

---

### **Conclusiones**
En esta clase, hemos profundizado en los circuitos RLC, observando cómo la impedancia y las funciones de transferencia determinan el comportamiento de estos sistemas. Además, hemos identificado cómo clasificar estas funciones según su comportamiento, y cómo la resonancia influye en la respuesta de los circuitos. Los circuitos RLC son fundamentales para comprender sistemas oscilatorios, y su análisis en términos de funciones de transferencia es clave para el diseño de filtros y otros sistemas electrónicos.

