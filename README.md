¿# Sistema Masa-Resorte-Amortiguador

## Enunciado del Problema

_(Aquí se muestra el sistema de dos masas, resortes y amortiguador)_
  ![Uploading {3F4EC75F-67C2-4CCC-ADC7-939F8D65CF93}.png…]()


## Planteamiento del Problema

El sistema consta de dos masas \( m_1 \) y \( m_2 \), conectadas mediante resortes de constantes \( k_1 \), \( k_2 \) y \( k_3 \), además de un amortiguador con coeficiente de amortiguamiento \( b \). La ecuación diferencial del sistema se obtiene aplicando la Segunda Ley de Newton a cada masa.

Para \( m_1 \):

\[ m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b (\dot{x}_1 - \dot{x}_2) + u \]

Para \( m_2 \):

\[ m_2 \ddot{x}_2 = -k_3 x_2 + k_2 (x_1 - x_2) + b (\dot{x}_1 - \dot{x}_2) \]

## Ecuaciones Diferenciales en LaTeX

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

Las ecuaciones diferenciales que describen el sistema son:

\begin{equation}
    m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b (\dot{x}_1 - \dot{x}_2) + u
\end{equation}

\begin{equation}
    m_2 \ddot{x}_2 = -k_3 x_2 + k_2 (x_1 - x_2) + b (\dot{x}_1 - \dot{x}_2)
\end{equation}

\end{document}
```

## Conclusión

Se han obtenido las ecuaciones diferenciales que describen el movimiento del sistema masa-resorte-amortiguador de dos grados de libertad y se han representado en código LaTeX para su correcta documentación.


