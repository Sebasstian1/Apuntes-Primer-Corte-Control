# Clase de Laboratorio: Sistemas de Control

En esta clase de laboratorio se abordaron los mismos temas tratados en la **Clase 1**, específicamente el estudio de **Sistemas Masa-Resorte-Amortiguador**, **Sistemas Rotacionales**, y **Circuitos RLC**. Sin embargo, se dedicó más tiempo a profundizar en el estudio de los circuitos RLC, ya que estos presentan una amplia variedad de aplicaciones en el mundo real y su análisis es crucial en muchos sistemas de control.

---

## 1. Sistemas Masa-Resorte-Amortiguador

En el laboratorio se revisaron brevemente los conceptos presentados en la **Clase 1** acerca del sistema masa-resorte-amortiguador. Se realizaron demostraciones físicas usando modelos de masa y resorte, así como ejemplos donde se observó la amortiguación de sistemas reales. 

**Ejemplo:**
En un experimento práctico, se utilizó un sistema masa-resorte con una masa de 1 kg, un resorte con constante elástica de 100 N/m y un amortiguador con un coeficiente de amortiguamiento de 5 Ns/m. El sistema se dejó oscilar libremente y se observó cómo la amplitud de las oscilaciones disminuía con el tiempo debido al amortiguamiento.

---

## 2. Sistemas Rotacionales

Similar a la **Clase 1**, en el laboratorio se discutieron los sistemas rotacionales, destacando su importancia en aplicaciones como los motores eléctricos y sistemas de control de velocidad en robótica. Se utilizaron simulaciones para modelar el comportamiento de estos sistemas bajo diferentes condiciones de amortiguamiento y torque aplicado.

**Ejemplo:**
Se simuló un sistema rotacional que modela un motor eléctrico con un momento de inercia de 0.01 kg·m², un coeficiente de amortiguamiento de 0.1 N·m·s/rad y una constante de torsión de 10 N·m·rad. Se aplicó un torque de 5 N·m en el sistema y se analizó la velocidad angular en función del tiempo para observar los efectos del amortiguamiento.

---

## 3. Circuitos RLC: Profundización

En esta clase de laboratorio, se dedicó un enfoque más extenso a los **Circuitos RLC**, debido a su relevancia en el diseño de filtros eléctricos y osciladores. Se profundizó en los siguientes aspectos:

### **Comportamiento Oscilatorio y Transitorio**

Los circuitos RLC pueden mostrar diferentes tipos de comportamientos en función de los valores de sus componentes (resistor, inductor y capacitor). Se mostró cómo los **circuitos subamortiguados** producen oscilaciones, mientras que los **sobreamortiguados** resultan en respuestas más lentas y suaves. Se discutieron las implicaciones de cada tipo de amortiguamiento en el diseño de sistemas de comunicación y filtros de señal.

**Ejemplo 1: Circuito Subamortiguado**
En un circuito RLC con $R = 10 \, \Omega$, $L = 1 \, H$ y $C = 0.01 \, F$, se observó un comportamiento subamortiguado, con oscilaciones a medida que el sistema regresaba al estado de equilibrio. La frecuencia de las oscilaciones fue calculada con la fórmula:

$$
\omega_d = \sqrt{\frac{1}{LC} - \left(\frac{R}{2L}\right)^2}
$$

**Ejemplo 2: Circuito Sobreamortiguado**
En un circuito RLC con $R = 100 \, \Omega$, $L = 1 \, H$ y $C = 0.01 \, F$, se observó un comportamiento sobreamortiguado. La respuesta se estabilizó sin oscilar, alcanzando el estado de equilibrio de forma más lenta.

### **Respuesta en el Dominio de la Frecuencia**

Además de las respuestas transitorias, se exploró cómo los circuitos RLC pueden analizarse en el **dominio de la frecuencia**. Los filtros diseñados con componentes RLC son capaces de filtrar señales según su frecuencia, lo cual es esencial en comunicaciones, análisis de señales y otros sistemas de procesamiento de señales.

**Ejemplo: Filtro Pasa-Banda**
Se diseñó un filtro pasa-banda utilizando un circuito RLC con $R = 10 \, \Omega$, $L = 0.5 \, H$ y $C = 0.01 \, F$. Este filtro dejó pasar señales con frecuencias cercanas a la frecuencia resonante, mientras que atenuó señales fuera de este rango.

### **Simulaciones y Experimentos**

En el laboratorio, los estudiantes realizaron experimentos prácticos con **circuitos RLC** reales, midiendo las señales de voltaje y corriente en el tiempo. Estas mediciones permitieron observar cómo las ecuaciones diferenciales se traducen en resultados experimentales y cómo la teoría del amortiguamiento se ajusta a las observaciones prácticas. Se utilizaron **osciloscopios** y **fuentes de señal** para generar las excitaciones y observar las respuestas del circuito.

**Ejemplo:**
Se conectó un circuito RLC en serie y se aplicó una señal de voltaje sinusoidal de 10 V a diferentes frecuencias. Los estudiantes midieron la corriente a través del circuito y observaron cómo la amplitud de la corriente cambiaba con la frecuencia de la señal, lo que confirmaba la resonancia a la frecuencia natural del circuito.

### **Ajuste de Componentes**

Los estudiantes también realizaron ejercicios prácticos donde modificaron valores de los componentes $R$, $L$ y $C$ para observar cómo estos afectan el comportamiento del sistema. Este enfoque les permitió entender mejor cómo diseñar un circuito RLC que cumpla con requisitos específicos, como la eliminación de ruido o la creación de un filtro de paso bajo o paso alto.

**Ejemplo: Ajuste de la Frecuencia de Resonancia**
Se modificaron los valores de $L$ y $C$ en un circuito RLC para cambiar la frecuencia de resonancia. Con un **inductor** de 0.5 H y un **condensador** de 0.01 F, la frecuencia de resonancia se calculó como:

$$
f_0 = \frac{1}{2\pi \sqrt{LC}}
$$

---

## Conclusión

La clase de laboratorio complementó lo aprendido en la **Clase 1** proporcionando una comprensión más profunda de los **Circuitos RLC**. A través de simulaciones y experimentos prácticos, los estudiantes pudieron visualizar cómo los sistemas de segundo orden reaccionan a diferentes condiciones, lo que facilita el diseño de sistemas de control más eficientes. Además, las aplicaciones de estos circuitos en filtros eléctricos, osciladores y comunicaciones se hicieron más claras, subrayando la importancia de comprender su comportamiento dinámico para aplicaciones tecnológicas.

---

## Referencias

- Ogata, K. "Ingeniería de Control Moderna".
- Dorf, R. "Sistemas de Control Automático".
