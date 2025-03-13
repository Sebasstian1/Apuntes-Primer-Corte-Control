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

![Circuito RLC](https://github.com/user-attachments/assets/rlc-circuit.png)

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

Esta ecuación describe la relación entre \( V_o(s) \) y \( V_i(s) \).

---

## Conclusión

Se resolvieron cuatro ejercicios aplicando la Transformada de Laplace para encontrar soluciones en el dominio de la frecuencia. Estos incluyen sistemas mecánicos y eléctricos, mostrando la analogía entre ambos.
