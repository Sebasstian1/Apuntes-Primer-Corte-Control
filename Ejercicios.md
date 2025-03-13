# Sistema Masa-Resorte-Amortiguador

## Enunciado del Problema

_(Aquí se muestra el sistema de dos masas, resortes y amortiguador)_

![{CB832BCA-4C5A-4E80-B71C-86A5F331C72C}](https://github.com/user-attachments/assets/6145e663-4439-4619-9101-897f9cd01aa4)


## Planteamiento del Problema

El sistema consta de dos masas \( m_1 \) y \( m_2 \), conectadas mediante resortes de constantes \( k_1 \), \( k_2 \) y \( k_3 \), además de un amortiguador con coeficiente de amortiguamiento \( b \). La ecuación diferencial del sistema se obtiene aplicando la Segunda Ley de Newton a cada masa.

Para \( m_1 \):

$$ m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b (\dot{x}_1 - \dot{x}_2) + u $$

Para \( m_2 \):

$$ m_2 \ddot{x}_2 = -k_3 x_2 + k_2 (x_1 - x_2) + b (\dot{x}_1 - \dot{x}_2) $$

## Ecuaciones Diferenciales en Markdown

```markdown
$$
m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1) - b (\dot{x}_1 - \dot{x}_2) + u
$$

$$
m_2 \ddot{x}_2 = -k_3 x_2 + k_2 (x_1 - x_2) + b (\dot{x}_1 - \dot{x}_2)
$$
```

## Conclusión

Se han obtenido las ecuaciones diferenciales que describen el movimiento del sistema masa-resorte-amortiguador de dos grados de libertad y se han representado en formato Markdown con soporte para LaTeX, adecuado para visualizarse en GitHub.

## Referencias


