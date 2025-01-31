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
  \\
  i = \frac{386}{20000}\times\frac{(1+i)^{60}-1}{(1+i)^{60}} \rightarrow i = 0.0049 \approx 0.5 \%
\end{split}
$$

And finally:

$$
\begin{split}
  Annual \ Nominal \ Rate = i \times 12 = 5.93 \%
  \\
  Annual \ Effective \ Rate = (1 + i)^{12} - 1 = 6.09 \%
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
  i_e = (1+i_d)^m-1
  \\
  i_d = \frac{r}{m} = \frac{0.019}{365} = 5.2 \times 10^{-5}
\end{split}
$$

Since we are dealing with daily compunding we can caluclate the effective monthly interest rate with:

$$
\begin{split}
  i_{monthly} = (1+\frac{r}{m})^{\frac{m}{12}}-1 = (1+i_d)^{\frac{m}{12}}-1
  \\
  i_{monthly} = (1+\frac{r}{m})^{\frac{m}{12}}-1 = (1+5.2 \times 10^{-5})^{30}-1
  \\
  i_{monthly} = 0.00156 = 0.156 \%
\end{split}
$$

And we calcualte the monthly payment with the capital interest rate formula.

$$
\begin{split}
  (A/P, i, N) = \frac{i (1+i)^N}{(1+i)^N-1}
  \\
  A = P \times \frac{i (1+i)^N}{(1+i)^N-1}
  \\
  A = 21999 \times \frac{0.00156 \times 1.00156^{48}}{1.00156^{48}-1} = \$ 476
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

It is hard to do a cash flow diagram in a markdown document which is what I am using so I am just going to use a table instead.

| Year        | Event                                      | Cash Flow ($)             |
|-------------|--------------------------------------------|---------------------------|
| 0           | Initial investment (solar cell + wiring)   | -3000 - 800 = -3800       |
| 1-20        | Annual Operating Cost                      | -100 per year             |
| 5,10,15,20  | Battery Replacement (every 5 years)        | -1000                     |
| 10,20       | Power Control Replacement (every 10 years) | -100                      |

I am just going to use the capital recovery formula for the colar cell and wiring since those are a one time costs.

$$
\begin{split}
  (A/P, i, N) = \frac{i(1+i)^N}{(1+i)^N-1}
  \\
  A = P \times \frac{i(1+i)^N}{(1+i)^N-1}
\end{split}
$$

For battery and power control I can use the present worth using series present worth forumula.

$$
\begin{split}
  (P/A, i, N) = \frac{(1+i)^N-1}{i(1+i)^N}
\end{split}
$$

Then convert that into an equvalent annual cost using capital Recovery:

$$
\begin{split}
  To \ Be \ Continude...
\end{split}
$$

Then I can compute total equivalent annual cost:

$$
\begin{split}
  EAC = Annualized \ Capital \ Cost + Annualized \ Recurring \ Costs + Operating \ Costs
\end{split}
$$

Then the total cost per $kWh$ is:

$$
\begin{split}
  Cost \ per \ kWh = \frac{EAC}{Annual \ energy \ Output}
\end{split}
$$

## Problem 6 - Viability of the Rollercoaster Project

To be continude...

## Problem 7 - Comparing Water Pumps

To be continude...
