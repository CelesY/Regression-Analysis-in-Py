# Direction in 2-Risky-Assets-Portfolio
The data comes from yahoo finance, which is an open source, so everyone can access the data for free. I got this data from the "Historical Data" column (CSV file, as shown in the code). 

The data contains 5 years of closing stock prices (unadjusted) for Walmart and Amazon, two well-known companies. There might be some more efficient ways to clean and use this data, but I'm still learning them. And this repository will be continuously updated, and will be expanded to N risky assets in the future.

Calculations are based on Portfolio Theory, formula are as follows:
## For Individual Asset:
          E(R)=ΣR(i)*P(i)
          σ^2=Σ[Ri-E(Ri)]^2*Pi
          std(σ)=sqrt(σ^2)

## For Two Risky Assets:
          E(Rp)=α*E(Ra)+β*E(Rb)
    while α and β are weights on assets of A and B separately
          σp^2=α^2*σa^2+β^2*σb^2+2*α*β*cov(Ra,Rb)
    or:   σp^2=α^2*σa^2+β^2*σb^2+2*α*β*corr(Ra,Rb)
     
## For N Risky Assets:
          E(Rp)=Σ[w(i)*E(Ri)]
          σ(port)^2=Σw(i)^2*σ(i)^2+ΣΣx(i)*x(j)cov(i,j)
    or:   σ(port)^2=[1/N]*var+[1-1/N]*cov
  
**It has to mention that the fomuler is under three assumptions:**
   1. All securities possess the same variance;
   2. All co-variance are the same;
   3. All securities are equally weighted in the portfolio.
   
After listing each possible weight on assets, we can create an efficient frontier.

## When Adding Risk-free Asset into the Portfolio:
          E(Rport)=w(rf)*E(Rf)+(1-w(rf))*E(Rm)
          σ(port)^2=w(rf)^2*σ(rf)^2+(1-w(rf))^2*σm^2+2*w(rf)*(1-w(rf))*cov(Rf,Rm)
          cov(Rf,Rm)=Σ[Rf-E(Rf)][Ri-E(Ri)]/n 
    Because the returns for the risk-free asset are certain,Rf-E(Rf)=0:
          cov(Rf,Rm)=0
        
Then we can get Tangency/Market Portfolio as well as CML & CAL, which I'll try to realize in a later update.
