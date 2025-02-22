# Modelado Matemático de Sistemas

Este documento aborda el proceso de obtención de modelos matemáticos para sistemas con amplificadores operacionales, sistemas de tanques y sistemas térmicos. Incluye ecuaciones diferenciales y sus aplicaciones prácticas.

---

## 1. Modelado Matemático de Circuitos con Amplificadores Operacionales

### **Descripción del Sistema**

Un amplificador operacional (Op-Amp) es un dispositivo fundamental en circuitos electrónicos. Se utiliza en configuraciones de amplificación, filtros, y control de señales. Un modelo básico involucra componentes como resistores y fuentes de voltaje.

### **Modelo Matemático**

Para un circuito con un amplificador operacional en configuración no inversora, la ecuación que describe el comportamiento es:

$$
V_o = \left( 1 + \frac{R_f}{R_{in}} \right) V_{in}
$$

Donde:
- $V_o$ es la salida del amplificador.
- $V_{in}$ es la entrada.
- $R_f$ es la resistencia de retroalimentación.
- $R_{in}$ es la resistencia de entrada.

#### Configuración Inversora:

La ecuación para la configuración inversora es:

$$
V_o = - \left( \frac{R_f}{R_{in}} \right) V_{in}
$$

### **Ejemplos y Aplicaciones**

- **Filtros activos:** Uso de amplificadores operacionales para crear filtros pasa-altos, pasa-bajos y pasa-banda.
- **Osciladores:** Amplificadores operacionales pueden ser utilizados para diseñar osciladores sinusoidales.
- **Circuitos de control:** Usados en sistemas de retroalimentación para mantener un valor de salida deseado.

---

## 2. Modelado Matemático de Sistemas de Tanques

### **Descripción del Sistema**

Un sistema de tanques es utilizado para modelar procesos de almacenamiento y transferencia de líquidos en diversas industrias. El sistema básico incluye:

- **Válvulas de entrada y salida**: Controlan el flujo de líquido en el sistema.
- **Tanques de almacenamiento**: Almacenan el líquido y mantienen el nivel dentro de los límites deseados.
- **Bomba de alimentación**: Ayuda a mantener el nivel de líquido en el tanque.

### **Ecuación Diferencial**

La dinámica del nivel de un tanque se puede modelar con la siguiente ecuación diferencial:

$$
\frac{dH}{dt} = \frac{Q_{in} - Q_{out}}{A}
$$

Donde:
- $H$ es el nivel de líquido en el tanque.
- $Q_{in}$ es el flujo de entrada.
- $Q_{out}$ es el flujo de salida.
- $A$ es el área de la base del tanque.

Si el flujo de salida es proporcional al nivel del líquido, entonces:

$$
Q_{out} = K H
$$

### **Tipos de Respuesta**

- **Respuesta a un paso:** Se analiza cómo cambia el nivel cuando se aplica un flujo constante.
- **Control de nivel:** Diseño de controladores para mantener el nivel dentro de los límites deseados.

### **Aplicaciones Prácticas**

- **Tratamiento de aguas residuales:** Sistemas de tanques para el almacenamiento y tratamiento de aguas.
- **Industria química:** Utilizados en el almacenamiento de productos líquidos y control de mezclas.

---

## 3. Modelado Matemático de Sistemas Térmicos

### **Descripción del Sistema**

Los sistemas térmicos se utilizan para modelar el comportamiento de la temperatura en diferentes entornos y procesos. Un modelo básico incluye:

- **Fuente de calor**: Suministra energía térmica al sistema.
- **Cuerpo térmico**: El objeto que recibe el calor, como una placa o un fluido.
- **Disipación de calor**: Pérdidas térmicas al ambiente.

### **Ecuación Diferencial**

La ecuación de un sistema térmico se puede describir mediante la ley de enfriamiento de Newton, que establece que la tasa de cambio de la temperatura de un cuerpo es proporcional a la diferencia entre su temperatura y la temperatura ambiente:

$$
m C \frac{dT}{dt} = Q - h A (T - T_{amb})
$$

Donde:
- $m$ es la masa del cuerpo térmico.
- $C$ es la capacidad calorífica del material.
- $T$ es la temperatura del cuerpo.
- $T_{amb}$ es la temperatura ambiente.
- $Q$ es el calor suministrado al sistema.
- $h$ es el coeficiente de transferencia de calor.
- $A$ es el área superficial del cuerpo.

### **Tipos de Respuesta**

- **Respuesta a una fuente de calor constante:** Análisis de la estabilización de la temperatura.
- **Enfriamiento natural:** Estudio de cómo un objeto pierde calor al ambiente.

### **Aplicaciones Prácticas**

- **Sistemas de climatización:** Control de temperatura en edificios y vehículos.
- **Procesos industriales:** Control de temperatura en hornos, reactores y equipos de procesamiento.

---

## Conclusión

Los sistemas descritos en este documento —circuitos con amplificadores operacionales, sistemas de tanques y sistemas térmicos— pueden modelarse mediante ecuaciones diferenciales. Estas ecuaciones proporcionan una descripción matemática del comportamiento dinámico de los sistemas, permitiendo su análisis y diseño de controladores adecuados. El uso de estos modelos es fundamental para optimizar el rendimiento y la estabilidad de diversos procesos industriales y tecnológicos.

---

## Referencias

- Dorf, R. C., & Bishop, R. H. (2017). **Modern Control Engineering**. Pearson.
- Ogata, K. (2010). **Modern Control Engineering**. Prentice Hall.
- Nise, N. S. (2011). **Control Systems Engineering**. Wiley.

