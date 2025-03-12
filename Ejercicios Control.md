# Análisis de un Sistema de Dos Masas Acopladas

## Descripción del Problema
Se analiza un sistema mecánico compuesto por dos masas \( m_1 \) y \( m_2 \), conectadas mediante resortes y un amortiguador. Se desea obtener las ecuaciones de movimiento y resolver el sistema.

## Ecuaciones de Movimiento
Aplicando la Segunda Ley de Newton a cada masa:

\[
 m_1 \ddot{x}_1 + (k_1 + k_2)x_1 - k_2 x_2 + b(\dot{x}_1 - \dot{x}_2) = u
\]

\[
 m_2 \ddot{x}_2 + (k_2 + k_3)x_2 - k_2 x_1 + b(\dot{x}_2 - \dot{x}_1) = 0
\]

## Representación en Espacio de Estados
Definiendo el estado como:
\[
 X = \begin{bmatrix} x_1 \\ \dot{x}_1 \\ x_2 \\ \dot{x}_2 \end{bmatrix}
\]
El sistema se puede escribir en forma matricial:

\[
\dot{X} = A X + B U
\]

Donde:

\[
A = \begin{bmatrix}
0 & 1 & 0 & 0 \\
-(k_1+k_2)/m_1 & -b/m_1 & k_2/m_1 & b/m_1 \\
0 & 0 & 0 & 1 \\
k_2/m_2 & b/m_2 & -(k_2+k_3)/m_2 & -b/m_2
\end{bmatrix}
\]

\[
B = \begin{bmatrix} 0 \\ 1/m_1 \\ 0 \\ 0 \end{bmatrix}
\]

## Solución del Sistema
Para resolver el sistema, aplicamos la Transformada de Laplace a las ecuaciones de movimiento:

\[
 m_1 s^2 X_1(s) + (k_1 + k_2)X_1(s) - k_2 X_2(s) + b s (X_1(s) - X_2(s)) = U(s)
\]

\[
 m_2 s^2 X_2(s) + (k_2 + k_3)X_2(s) - k_2 X_1(s) + b s (X_2(s) - X_1(s)) = 0
\]

Reescribimos en notación matricial:

\[
\begin{bmatrix} m_1 s^2 + k_1 + k_2 + bs & -k_2 - bs \\ -k_2 - bs & m_2 s^2 + k_2 + k_3 + bs \end{bmatrix}
\begin{bmatrix} X_1(s) \\ X_2(s) \end{bmatrix} = 
\begin{bmatrix} U(s) \\ 0 \end{bmatrix}
\]

Despejamos \( X_1(s) \) y \( X_2(s) \) usando la regla de Cramer:

\[
X_1(s) = \frac{ \text{Det}([B_1 | A_2]) }{\text{Det}(A)}
\]

\[
X_2(s) = \frac{ \text{Det}([A_1 | B_2]) }{\text{Det}(A)}
\]

Finalmente, aplicamos la Transformada Inversa de Laplace para obtener \( x_1(t) \) y \( x_2(t) \) en el dominio del tiempo.

## Conclusión
Se ha obtenido la representación del sistema en espacio de estados y se ha resuelto en el dominio de Laplace. Esta solución permite analizar el comportamiento dinámico del sistema y diseñar estrategias de control si es necesario.

