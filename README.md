# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$
So for $n > 1$,

$$
\begin{align}
T(n) &= T(\frac{n}{13}) + 5\\
&= (T(\frac{n}{13^2}) + 5) + 5\\
&= T(\frac{n}{13^3}) + 3*5\\
&= \vdots \\
&= T(\frac{n}{13^i}) + i*5
\end{align}
$$


3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

4.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$
