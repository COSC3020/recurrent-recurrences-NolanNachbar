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
&= T(\frac{n}{13^3}) + 3 \cdot 5\\
&= \vdots\\
&= T(\frac{n}{13^i}) + 5\cdot i
\end{align} 
$$

So for $i = log_{13} n$,

$$
\begin{align}
T(n) &= T(\frac{n}{13^{log_{13} n}}) + 5 log_{13} n\\
&= T(1) + 5 log_{13} n\\
&\in \Theta(log n)\
\end{align}
$$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

So for $n > 1$,

$$
\begin{align}
T(n) &= 13 T(\frac{n}{13}) + 5\\
&=13^2 (T(\frac{n}{13^2}) + 5 \cdot 13) + 5\\
&= 13^3 T(\frac{n}{13^3}) + 13 \cdot 5 + 13 \cdot 5 + 5\\
&= \vdots\\
&= 13^i T(\frac{n}{13^i}) + 5^13^{(i - 1)} + 5  \cdot  13^{(i - 2)} + \cdots + 5
\end{align} 
$$

So for $i = log_{13} n$,

$$
\begin{align}
T(n) &= 13^{(log_{13} n)} T(\frac{n}{13^{(log_{13} n)}}) + 5^13^{(log_{13} n - 1)} + 5  \cdot  13^{(log_{13} n - 2)} + \cdots + 5\\
&= n T(1) + 5 + 5 \frac{n}{13} + 5 \frac{n}{13^2} + \cdots\\
&\in \Theta(n)\
\end{align}
$$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

So for $n > 1$,

$$
\begin{align}
T(n) &= 13 T(\frac{n}{13}) + 2n\\
&=13^2 T(\frac{n}{13^2})+ 2n \cdot 2\\
&=13^3 T(\frac{n}{13^3}) + 2n \cdot 3\\
&= \vdots\\
&=13^i T(\frac{n}{13^i}) + 2n \cdot i\\
\end{align} 
$$

So for $i = log_{13} n$,

$$
\begin{align}
T(n) &=13^{log_{13} n} T(\frac{n}{13^{log_{13} n}}) + 2n \cdot log_{13} n\\
&= n T(1) + 2n \cdot log_{13} n\\
&\in \Theta(n \log n)\
\end{align}
$$
