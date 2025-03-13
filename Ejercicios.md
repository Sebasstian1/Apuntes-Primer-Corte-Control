# Sistemas Dinámicos: Análisis y Solución

## Primer Ejercicio: Sistema Masa-Resorte-Amortiguador

![Sistema Masa-Resorte-Amortiguador](https://github.com/user-attachments/assets/6145e663-4439-4619-9101-897f9cd01aa4)

### Planteamiento del Problema

El sistema consta de dos masas \( m_1 \) y \( m_2 \), conectadas mediante resortes de constantes \( k_1 \), \( k_2 \) y \( k_3 \), además de un amortiguador con coeficiente de amortiguamiento \( b \). Aplicando la Segunda Ley de Newton:

Para \( m_1 \):

$$ m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b (\dot{x}_1 - \dot{x}_2) + u $$

Para \( m_2 \):

$$ m_2 \ddot{x}_2 = -k_3 x_2 + k_2 (x_1 - x_2) + b (\dot{x}_1 - \dot{x}_2) $$

### Solución

Aplicando la transformada de Laplace:

$$ m_1 s^2 X_1(s) + (k_1 + k_2) X_1(s) - k_2 X_2(s) + b (s X_1(s) - s X_2(s)) = U(s) $$

$$ m_2 s^2 X_2(s) + (k_2 + k_3) X_2(s) - k_2 X_1(s) - b (s X_1(s) - s X_2(s)) = 0 $$

---

## Segundo Ejercicio: Sistema Masa-Resorte-Amortiguador con Amortiguador Adicional

![Sistema Masa-Resorte-Amortiguador 2](https://github.com/user-attachments/assets/df54ad8b-cb30-4cf5-8c0e-32895fa7bf57)

### Planteamiento del Problema

El sistema consta de dos masas \( m_1 \) y \( m_2 \), conectadas mediante resortes de constantes \( k_1 \) y \( k_2 \), además de un amortiguador con coeficiente \( b_1 \). Se aplica una fuerza externa \( u \) a \( m_1 \).

Para \( m_1 \):

$$ m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b_1 \dot{x}_1 + u $$

Para \( m_2 \):

$$ m_2 \ddot{x}_2 = -k_2 (x_2 - x_1) $$

### Solución

Aplicando la transformada de Laplace:

$$ m_1 s^2 X_1(s) + (k_1 + k_2) X_1(s) - k_2 X_2(s) + b_1 s X_1(s) = U(s) $$

$$ m_2 s^2 X_2(s) + k_2 X_2(s) - k_2 X_1(s) = 0 $$

---

## Tercer Ejercicio: Circuito RLC en Serie

![{9C29B82A-A38B-4093-919A-C64FC479EFF0}](https://github.com/user-attachments/assets/f72b018c-92d5-4558-bafd-3e8927d86e7b)

### Planteamiento del Problema

El circuito consta de una resistencia \( R \), un inductor \( L \) y un capacitor \( C \) en serie. Aplicando la Ley de Kirchhoff:

$$ v_i(t) = R i(t) + L \frac{d i(t)}{dt} + \frac{1}{C} \int i(t) dt $$

Derivando:

$$ L \frac{d^2 i(t)}{dt^2} + R \frac{d i(t)}{dt} + \frac{1}{C} i(t) = \frac{d v_i(t)}{dt} $$

### Solución

Aplicando la transformada de Laplace:

$$ L s^2 I(s) + R s I(s) + \frac{1}{C} I(s) = s V_i(s) $$

Despejando \( I(s) \):

$$ I(s) = \frac{s V_i(s)}{L s^2 + R s + \frac{1}{C}} $$

---

## Cuarto Ejercicio: Circuito RC con Dos Resistencias y Dos Capacitores

![{7D6A757C-58BD-4137-A6E2-4E8D5C0A13F9}](https://github.com/user-attachments/assets/b9f5bc0b-01bb-43d8-83e9-7dd132f2a7c0)

### Planteamiento del Problema

El circuito consiste en:

- Resistencia \( R_1 \) en serie con capacitor \( C_1 \).
- Resistencia \( R_2 \) en serie con capacitor \( C_2 \), en paralelo con el primer conjunto.

Aplicando la Ley de Kirchhoff en la malla izquierda:

$$ v_i(t) = R_1 i_1(t) + v_{C_1}(t) $$

Para la malla derecha:

$$ v_{C_1}(t) = R_2 i_2(t) + v_o(t) $$

Las ecuaciones de corriente:

$$ i_1(t) = C_1 \frac{dv_{C_1}(t)}{dt} $$  
$$ i_2(t) = C_2 \frac{dv_o(t)}{dt} $$  

### Solución

Aplicando la transformada de Laplace:

$$ V_i(s) = R_1 I_1(s) + V_{C_1}(s) $$

$$ V_{C_1}(s) = R_2 I_2(s) + V_o(s) $$

Usando \( I_1(s) = C_1 s V_{C_1}(s) \) y \( I_2(s) = C_2 s V_o(s) \):

$$ V_i(s) = R_1 C_1 s V_{C_1}(s) + V_{C_1}(s) $$

$$ V_{C_1}(s) = R_2 C_2 s V_o(s) + V_o(s) $$

Resolviendo para \( V_o(s) \):

$$ V_o(s) = \frac{V_i(s)}{1 + R_1 C_1 s + R_2 C_2 s} $$

---

## Quinto Ejercicio: Sistema de Discos Acoplados con Resorte de Torsión

![{58622C7E-6912-43A3-8B4E-506A0F7C6FE7}](https://github.com/user-attachments/assets/c445e42e-0bd6-4d79-9800-776a5e5986c8)


### Planteamiento del Problema

El sistema consta de dos discos de inercia \( J_1 \) y \( J_2 \), acoplados mediante un resorte de torsión con constante \( K \). Cada disco tiene un amortiguamiento viscoso \( D_1 \) y \( D_2 \), y un torque externo \( T(t) \) aplicado a \( J_1 \).

Las ecuaciones de movimiento son:

$$ J_1 \ddot{\theta}_1 + D_1 \dot{\theta}_1 + K (\theta_1 - \theta_2) = T(t) $$

$$ J_2 \ddot{\theta}_2 + D_2 \dot{\theta}_2 + K (\theta_2 - \theta_1) = 0 $$

### Solución en el Dominio de Laplace

$$ J_1 s^2 \Theta_1(s) + D_1 s \Theta_1(s) + K (\Theta_1(s) - \Theta_2(s)) = T(s) $$

$$ J_2 s^2 \Theta_2(s) + D_2 s \Theta_2(s) + K (\Theta_2(s) - \Theta_1(s)) = 0 $$

---

## Conclusión

Se resolvieron cinco ejercicios aplicando la Transformada de Laplace para modelar sistemas mecánicos y eléctricos.

---

# Problemas Resueltos de Dinámica de Sistemas

Este documento contiene ejercicios resueltos de modelado y análisis de sistemas dinámicos utilizando la **Transformada de Laplace**.

---

## Sexto Ejercicio: Sistema de Tanques Interconectados  

![{A53632EF-FB34-492B-98BC-C1F7A9C147CF}](https://github.com/user-attachments/assets/25bebbec-bdb8-43f0-966c-88e24d9774ac)


### Planteamiento del Problema  

El sistema consta de **dos tanques interconectados** en serie:  

- \( q_i \) es el **caudal de entrada** al primer tanque, regulado por la válvula \( a_1 \).  
- \( q_m \) es el **caudal intermedio** entre los tanques.  
- \( q_o \) es el **caudal de salida** del segundo tanque, regulado por la válvula \( a_2 \).  
- \( h_1 \) y \( h_2 \) son las **alturas del líquido** en los tanques.  
- \( A_1 \) y \( A_2 \) son las **áreas transversales** de los tanques.  

Aplicamos **balance de masas** en cada tanque.  

Para el **primer tanque**:  

\[
A_1 \frac{dh_1}{dt} = q_i - q_m
\]

Para el **segundo tanque**:  

\[
A_2 \frac{dh_2}{dt} = q_m - q_o
\]

**Flujo a través de las válvulas** (Ecuación de Torricelli):  

\[
q_m = K_1 \sqrt{h_1}
\]

\[
q_o = K_2 \sqrt{h_2}
\]

Sustituyendo en las ecuaciones de balance:  

\[
A_1 \frac{dh_1}{dt} = q_i - K_1 \sqrt{h_1}
\]

\[
A_2 \frac{dh_2}{dt} = K_1 \sqrt{h_1} - K_2 \sqrt{h_2}
\]

---

### Solución en el Dominio de Laplace  

Aplicamos la **Transformada de Laplace** con condiciones iniciales nulas:  

\[
A_1 s H_1(s) = Q_i(s) - K_1 H_1(s)^{1/2}
\]

\[
A_2 s H_2(s) = K_1 H_1(s)^{1/2} - K_2 H_2(s)^{1/2}
\]

Estas ecuaciones pueden resolverse numéricamente o **linealizarse** alrededor de un punto de operación para obtener una solución analítica.

---

### Conclusión  

Se modeló el sistema de **tanques interconectados** aplicando **balance de masas** y la ecuación de **Torricelli**. Luego, se resolvió en el **dominio de Laplace** para su análisis dinámico.

---

## Otros Ejercicios  

Para más problemas resueltos, consulta los ejercicios anteriores en este mismo documento.


