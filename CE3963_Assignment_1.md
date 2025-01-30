# CE3963 - Assignment 1

**Author:** Shahriar Kariman

**Due:** Jan 27th, 2025

## Problem 1 - Compounding Terms in Credit Card

So I know that the nominal interest rate is $r = 16.9\%$ and the effective interest rate is $i_e = 18.407\%$ and I have the formula for calculating $i_e$ given a number of periods($n$). I can easily calcualte $n$.

$$
\begin{split}
  i_e = (1+\frac{r}{n})^n - 1
  \\
  (i_e + 1) = (1+\frac{r}{n})^n
  \\
  \ln(1+i_e) = n \times \ln(1+\frac{r}{n})
  \\
  n = \frac{\ln(1+i_e)}{\ln(1+\frac{r}{n})}
\end{split}
$$

So I solved that using the fixed point iteration method on my calcualtor and got $\approx 337$ so this mean that we are pretty close to *compounding daily* but I can't say why we didn't just end up with $365$?

## Problem 2 - Annual Nominal and Effective Interest Rates of the Bank

So we know:

$$
\begin{split}
  P = \$ 20000 \rightarrow present \ value
  \\
  A = \$ 386 \rightarrow fixed \ periodic \ payment
  \\
  i = \ ? \rightarrow interest \ rate \ per \ period
  \\
  N = 12 \times 5 = 60 \rightarrow number \ of \ periods
  \end{split}
  \\
  (A/P, i, N) = \frac{i (1+i)^N}{(1+i)^N-1}
$$

We need to solve for $i$.

$$
  \begin{split}
  A = P \times \frac{i (1+i)^N}{(1+i)^N-1}
  \\
  386 = 20000 \times \frac{i (1+i)^{60}}{(1+i)^{60}-1}
\end{split}
$$

## Problem 3 - Monthly Payment for Financing Period

So we know:

$$
\begin{split}
  P = \$ 24999 - \$ 3000 \rightarrow present \ value
  \\
  r = 1.9 \% \rightarrow annual \ interest \ rate
  \\
  m = 365 \rightarrow compounded \ daily
  \\
  N = 48 \rightarrow loan \ term
  \\
  i_e = (1+i_s)^m-1
  \\
  i_s = \frac{r}{m}
\end{split}
$$

Since we are dealing with daily compunding we can caluclate the effective monthly interest rate with:

$$
\begin{split}
  i_{monthly} = (1+\frac{r}{m})^{\frac{m}{12}}-1
\end{split}
$$

And we calcualte the monthly payment with the capital interest rate formula.

$$
\begin{split}
  (A/P, i, N) = \frac{i (1+i)^N}{(1+i)^N-1}
\end{split}
$$

## Problem 4 - Total Monetary Loss During Construction

So we know:

$$
\begin{split}
A = \frac{4 \times 10^6}{2} \rightarrow annual \ revenue
\\
r = 4 \% \rightarrow annual \ interest \ rate
\end{split}
$$

We can calcualte the present worth of a prepetual income stream with the capitalized value formula.

$$
\begin{split}
CV = \frac{A}{i}
\\
CV = \frac{2 \times 10^6}{0.04} = 5 \times 10^7
\end{split}
$$

So thats $\$ 50$ million total monetary loss.

## Problem 5 - Potential for a Photovoltaic System

## Problem 6 - Viability of the Rollercoaster Project

## Problem 7 - Comparing Water Pumps
