# CE3963 - Assignment 1

**Author:** Shahriar Kariman

**Due:** Jan 27th, 2025

## Problem 1 - Compounding Terms in Credit Card

So I know that the nominal interest rate is $r = 16.9\%$ and the effective interest rate is $i_e = 18.407\%$ and I have the formula for calculating $i_e$ given a number of periods($n$). I can easily calculate $n$.

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

So I solved that using the fixed point iteration method on my calculator and got $\approx 337$ so this mean that we are pretty close to *compounding daily* but I can't say why we didn't just end up with $365$?

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

Since we are dealing with daily compounding we can calculate the effective monthly interest rate with:

$$
\begin{split}
  i_{monthly} = (1+\frac{r}{m})^{\frac{m}{12}}-1 = (1+i_d)^{\frac{m}{12}}-1
  \\
  i_{monthly} = (1+\frac{r}{m})^{\frac{m}{12}}-1 = (1+5.2 \times 10^{-5})^{30}-1
  \\
  i_{monthly} = 0.00156 = 0.156 \%
\end{split}
$$

And we calculate the monthly payment with the capital interest rate formula.

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

We can calculate the present worth of a perpetual income stream with the capitalized value formula.

$$
\begin{split}
  CV = \frac{A}{i}
  \\
  CV = \frac{2 \times 10^6}{0.04} = 5 \times 10^7
\end{split}
$$

So that's $\$ 50$ million total monetary loss.

## Problem 5 - Potential for a Photovoltaic System

It is hard to do a cash flow diagram in a markdown document which is what I am using so I am just going to use a table instead.

| Year        | Event                                      | Cash Flow ($)             |
|-------------|--------------------------------------------|---------------------------|
| 0           | Initial investment (solar cell + wiring)   | -3000 - 800 = -3800       |
| 1-20        | Annual Operating Cost                      | -100 per year             |
| 5,10,15,20  | Battery Replacement (every 5 years)        | -1000                     |
| 10,20       | Power Control Replacement (every 10 years) | -100                      |

That means:

$$
\begin{split}
  P_{initial} = 3000+1000+800+100
  \\
  i = 0.1 \rightarrow Annual \ interest \ rate
  \\
  E = 35 \times 365 (kWh/year) \rightarrow Annual \ energy \ output
  \\
  c_{electiricty} = 0.07 \rightarrow cost \ of \ electiricty
  \\
  S = 0 \rightarrow No \ salvage
  \\
  c_{Operating} = \$ 100/year \rightarrow Operating \ cost
\end{split}
$$

And I need the Annual Equivalent Cost:

$$
\begin{split}
  EAC_{Capital} = (P_{initial} - S) \times (A/P, i, N) + S \times i = P_{initial} \times (A/P, i, N) = 4900 \times \frac{0.10(1+0.10)^{20}}{(1+0.10)^{20} - 1} = 4900 \ times 0.117 = \$ 575.5
  \\
  EAC_{Batteries} = (P/A, i, N) = \frac{Battery \ Cost}{(P/A, i, N)} = \frac{Battery \ Cost}{\frac{(1 + 0.10)^5 - 1}{0.10(1 + 0.10)^5}} = \frac{1000}{3.79} = \$ 263.8
  \\
  EAC_{Power \ Control} = \frac{Power \ Control \ Cost}{(P/A, i, N)} = \frac{Power \ Control \ Cost}{(P/A, i, N)} = \frac{100}{\frac{(1.10)^{10} - 1}{0.10 \times (1.10)^{10}}} = \frac{100}{6.1445} = \$ 16.27
  \\
  EAC_{Operating} = \$ 100
  \\
  EAC = EAC_{Capital} + EAC_{Operating} + EAC_{Batteries} + EAC_{Power \ Control} = 575.5 + 263.8 + 16.27 + 100 = \$ 955.57
\end{split}
$$

And the benefit of the photovoltaic would be based on the energy it creates:

$$
\begin{split}
  b = c_{electiricty} \times 35 \times 365 = \$ 894.25
\end{split}
$$

Finally the total profit should be:

$$
\begin{split}
  \text{total profit} = 894.25 - 955.57 = -61.32
\end{split}
$$

So we actually lose money with the new system so it is *not beneficial* to have this new system in an economic sense which means NB power **should not** implement the system. But I would also consider environmental impact as well.

## Problem 6 - Viability of the Rollercoaster Project

Unfortunately I ran out of time.

## Problem 7 - Comparing Water Pumps

I think I just need to calculate the Equivalent Annual Cost for 12 years for each pump and compare them.

### Pump A

$$
\begin{split}
  cost = 12000
  \\
  P_{\text{Pump A}} = \text{cost} \ (1 + \frac{1}{(1+i)^N} + \frac{1}{(1+i)^{2N}}) = 12000 \times \left( 1 + \frac{1}{(1.08)^3} + \frac{1}{(1.08)^6} + \frac{1}{(1.08)^9} \right) = \$ 35091.01
\end{split}
$$

### Pump B

$$
\begin{split}
  cost = 15000
  \\
  P_{\text{Pump B}} = \text{cost} \ (1 + \frac{1}{(1+i)^N} + \frac{1}{(1+i)^{2N}}) = 15000 \times \left( 1 + \frac{1}{(1.08)^4} + \frac{1}{(1.08)^8}\right) = \$ 34129.48
\end{split}
$$

### Conclusion

So it is more advantageous to use pump B since the since the present cost is less than pump A.
