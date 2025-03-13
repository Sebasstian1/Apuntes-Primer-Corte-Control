# Sistema Masa-Resorte-Amortiguador

## Primer Ejercicio

![{CB832BCA-4C5A-4E80-B71C-86A5F331C72C}](https://github.com/user-attachments/assets/6145e663-4439-4619-9101-897f9cd01aa4)

## Planteamiento del Problema

El sistema consta de dos masas \( m_1 \) y \( m_2 \), conectadas mediante resortes de constantes \( k_1 \), \( k_2 \) y \( k_3 \), además de un amortiguador con coeficiente de amortiguamiento \( b \). La ecuación diferencial del sistema se obtiene aplicando la Segunda Ley de Newton a cada masa.

Para \( m_1 \):

$$ m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b (\dot{x}_1 - \dot{x}_2) + u $$

Para \( m_2 \):

$$ m_2 \ddot{x}_2 = -k_3 x_2 + k_2 (x_1 - x_2) + b (\dot{x}_1 - \dot{x}_2) $$

## Solución del Sistema

Resolviendo el sistema en términos de sus ecuaciones diferenciales:

Aplicando la transformada de Laplace:

$$ m_1 s^2 X_1(s) + (k_1 + k_2) X_1(s) - k_2 X_2(s) + b (s X_1(s) - s X_2(s)) = U(s) $$

$$ m_2 s^2 X_2(s) + (k_2 + k_3) X_2(s) - k_2 X_1(s) - b (s X_1(s) - s X_2(s)) = 0 $$

De donde podemos despejar \( X_1(s) \) y \( X_2(s) \) en función de \( U(s) \).

---

## Segundo Ejercicio

![image](https://github.com/user-attachments/assets/df54ad8b-cb30-4cf5-8c0e-32895fa7bf57)

## Planteamiento del Problema

El sistema consta de dos masas \( m_1 \) y \( m_2 \), conectadas mediante resortes de constantes \( k_1 \) y \( k_2 \), además de un amortiguador con coeficiente de amortiguamiento \( b_1 \). Se aplica una fuerza externa \( u \) a la masa \( m_1 \).

Para \( m_1 \):

$$ m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b_1 \dot{x}_1 + u $$

Para \( m_2 \):

$$ m_2 \ddot{x}_2 = -k_2 (x_2 - x_1) $$

## Solución del Sistema

Aplicando la transformada de Laplace:

$$ m_1 s^2 X_1(s) + (k_1 + k_2) X_1(s) - k_2 X_2(s) + b_1 s X_1(s) = U(s) $$

$$ m_2 s^2 X_2(s) + k_2 X_2(s) - k_2 X_1(s) = 0 $$

Resolviendo el sistema de ecuaciones, se obtiene la relación de \( X_1(s) \) y \( X_2(s) \) en función de \( U(s) \).

---

## Tercer Ejercicio: Circuito RLC en Serie

![{A27A323C-26A3-4764-BD1A-AB76FD8CA779}](https://github.com/user-attachments/assets/0541e843-295d-422b-be27-8675ba032f75)


## Planteamiento del Problema

El circuito consta de una resistencia \( R \), un inductor \( L \) y un capacitor \( C \) en serie. La corriente \( i(t) \) fluye a través del circuito, mientras que la tensión en el capacitor es \( v_C(t) \). Aplicando la Ley de Kirchhoff de Voltajes:

$$ v_i(t) = v_R(t) + v_L(t) + v_C(t) $$

Reemplazando las expresiones de voltaje en cada componente:

$$ v_i(t) = R i(t) + L \frac{d i(t)}{dt} + \frac{1}{C} \int i(t) dt $$

Derivando en ambos lados para obtener una ecuación diferencial de segundo orden:

$$ L \frac{d^2 i(t)}{dt^2} + R \frac{d i(t)}{dt} + \frac{1}{C} i(t) = \frac{d v_i(t)}{dt} $$

## Solución del Sistema

Aplicando la transformada de Laplace con condiciones iniciales nulas:

$$ L s^2 I(s) + R s I(s) + \frac{1}{C} I(s) = s V_i(s) $$

De donde podemos despejar \( I(s) \):

$$ I(s) = \frac{s V_i(s)}{L s^2 + R s + \frac{1}{C}} $$

Esta ecuación permite analizar la respuesta del circuito en el dominio de Laplace.

## Conclusión

Se han obtenido las ecuaciones diferenciales que describen el comportamiento del sistema masa-resorte-amortiguador y el circuito RLC en serie, planteando sus soluciones en el dominio de Laplace.
