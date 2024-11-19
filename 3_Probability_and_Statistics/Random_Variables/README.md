<ul>
  <li><b>Random Variable:</b> A random variable in statistics is a numerical value that represents the outcomes of a random phenomenon or experiment. 
    It is called "random" because the specific value it takes depends on the outcome of an event.<br>
    For example:<br>
    If you toss a coin, you can assign 1 for Heads and 0 for Tails.<br>
    If you roll a die, you can use the number that appears on the die as the random variable.</li><br>

  <li><b>Types of random variables:</b><br>
    <ol type=1>
  <li>Discrete Random Variable: Takes on countable values, such as whole numbers.<br>
  Example: The number of heads in 5 coin tosses (X=0,1,2,3,4,5).<br></li>
    
  <li>Continuous Random Variable: Takes on any value within a range or interval, typically measured quantities.<br>
  Example: The time it takes for a train to arrive (X∈[0,∞)).</li>
  </ol>
  </li>

  <b><h2>Note:</h2></b> If probability of a random variable is 0, it always mean it represents an empty set or an impossible event in case of discrete random variable but doesn't in case of continuous random variable.<br>

 <li><b>Probability Mass Function (PMF):</b> It is a function that gives the probability of a discrete random variable taking on specific values. It maps each possible value of the random variable to its probability, ensuring the following properties:<br>
1) Non-negativity: P(X=x)≥0 for all x.<br>
2) Sum of probabilities equals 1: ∑<sub>(x∈S)</sub> P(X=x)=1, where S is the set of all possible values the random variable can take.<br><br>
   Example: Consider a fair six-sided die. Let X be the number rolled. The PMF is:<br>
   P(X=x)=> 1/6, if x∈{1,2,3,4,5,6} and 0, otherwise
 </li><br>

 <li><b>Bernoulli Random Variable:</b> A Bernoulli random variable is a type of discrete random variable that represents only two possible outcomes: success (usually represented by 1) and failure (usually represented by 0).<br><br>
 P(X=x)=> p, if x=1 and 1−p, if x=0. {p:probability of success}<br>
 Alternatively, P(X=x)=p<sup>x</sup>(1-p)<sup>1-x</sup> 
</li><br>

<li><b>Bernoulli Trial:</b> A Bernoulli trial refers to the actual experiment or single event that results in one of two possible outcomes: success or failure.
It is the process or act of performing the random experiment.</li><br>

<li><b>Independent Bernoulli trials:</b> They are multiple repetitions of a Bernoulli trial where the outcome of one trial does not influence the outcomes of others.<br>
Example: Tossing a fair coin: Each flip is a Bernoulli trial.<br>
Probability of heads (p=0.5) and tails (1−p=0.5) remains constant. Outcomes are independent.<br><br>
  If two coins are tossed simultaneously with P(H)=0.7 (the probability of heads for each coin), we can identify the following independent Bernoulli trials and their probabilities.<br>

Coin 1 outcome: Tossing the first coin.<br>
Success (H): 𝑃(𝐻1)=0.7<br>
Failure (T): 𝑃(𝑇1)=1−𝑃(𝐻1)=0.3, same for coin 2<br><br>

Using the independence property, the probabilities of the combined outcomes can be calculated as: P(Outcome)=P(Coin 1 outcome)⋅P(Coin 2 outcome)<br>
Possible outcomes:
HH (Heads on both coins):P(HH)=P(H1)⋅P(H2)=0.7⋅0.7=0.49<br>
P(HT)=P(TH)=0.21<br>
P(TT)=0.09
</li><br>

<li><b>Geometric Random Variable:</b> It is a type of discrete random variable that models the number of trials needed to get the first success in a sequence of independent and identically distributed Bernoulli trials, where each trial has a constant probability of success p.<br>
Example: Flipping a coin until head appears {H, TH, TTTTTTH, ....} <br><br>
The probability of the first success occurring on the k-th trial is: P(X=k)=(1−p)<sup>k-1</sup>p, where (1−p)<sup>k-1</sup> is the probability of k−1 failures before the first success.
</li>

 <b><h2>Note:</h2></b> Sum of all values of PMF of geometric random variable is 1 i.e. {P(H) + P(TH) + P(TTH) + P(......)}=1.

 <li><b>Binomial Random Variable:</b> It is a type of discrete random variable that counts the number of successes in a fixed number of independent Bernoulli trials, where each trial has the same probability of success p.<br>
The probability of observing exactly k successes in n trials is given by: P(X = k) = (nCk) * p<sup>k</sup> * (1 - p)<sup>(n - k)</sup>
 </li><br><br>

 <table border="1" style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr>
      <th>Feature</th>
      <th>Bernoulli</th>
      <th>Binomial</th>
      <th>Geometric</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Definition</b></td>
      <td>A random variable that represents a single trial with two outcomes (success or failure).</td>
      <td>A random variable representing the number of successes in a fixed number of independent Bernoulli trials.</td>
      <td>A random variable representing the number of trials until the first success in independent Bernoulli trials.</td>
    </tr>
    <tr>
      <td><b>Range of Values</b></td>
      <td>{0, 1}</td>
      <td>{0, 1, 2, ..., n}</td>
      <td>{1, 2, 3, ...}</td>
    </tr>
    <tr>
      <td><b>Example</b></td>
      <td>Flipping a coin once (Head = 1, Tail = 0).</td>
      <td>Counting how many heads occur in 10 flips of a coin.</td>
      <td>Counting how many coin flips are needed to get the first head.</td>
    </tr>
  </tbody>
 </table>

 <li><b>Continuous Random Variable:</b> It is a type of random variable that can take any value within a continuous range of values, typically on an interval of the real number line. Continuous random variables are defined over an interval, such as [a,b], or [0,∞), or (−∞,∞).<br>
   <ul>
<li> Probability: The probability of a continuous random variable taking any exact value is 0 (P(X=x)=0, if we take any positive value, sum of all exceeds 1, violating main axiom of probability). Instead, probabilities are calculated over intervals, such as P(a≤X≤b).</li></ul>
 </li><br>

 <li><b>A Probability Density Function (PDF):</b> It is a mathematical function that describes the likelihood of a continuous random variable taking on a particular value. While the probability of a continuous random variable at an exact point is 0, the PDF provides a way to calculate the probability of the variable falling within an interval.<br><br>
 Properties:<br>
   1) Non-Negativity: The PDF is always non-negative for all values of x: f(x)≥0 for all x<br>
   2) Total Probability Equals 1: The area under the curve of the PDF over the entire range is 1: &#8747;(-∞ to ∞)f(x)dx=1<br>
   3) Interval Probability: The probability that the random variable X falls within an interval [a,b] is given by the area under the PDF curve within that interval: P(a≤X≤b)=∫ (a to b)f(x)dx
 </li><br>

 <li><b>Uniform Distribution/ Uniform Random Variable:</b> It is a probability distribution where all outcomes are equally likely within a specific range. It can be categorized into two types:<br>
1) Discrete Uniform Distribution: Each value in a finite set has an equal probability.<br>
   A random variable X is discrete uniform if it can take on n values, each with equal probability: P(X=x)= 1/n<br><br>
​
2) Continuous Uniform Distribution: Any value within a given interval is equally likely.<br>
   The Probability Density Function (PDF) is: f(x)=> 1/(b−a) if a≤x≤b, and 0 otherwise
 </li><br><br>

 <li><b>Exponential Distribution:</b> It is a continuous probability distribution used to model the time until an event occurs, assuming the events happen at a constant rate.<br>
 Example: Models the time until a machine breaks down or models the time between customer arrivals at a service point.<br><br>

 The PDF of an exponential random variable X with rate parameter λ>0 is given by:<br>
 f(x)=> λe<sup>−λx</sup> for x≥0, 0 otherwise, where λ is the rate parameter (events per unit time)
 </li>

 <li><b>Normal/Gaussian Distribution:</b> It describes a continuous random variable where most of the data points cluster around the mean, and the probabilities for values further away from the mean decrease symmetrically. Example: Analyzing exam scores or height of individuals.<br>
  The PDF of a normal distribution with mean μ and standard deviation σ is:<br>
  
   ![image](https://github.com/user-attachments/assets/4a3d2de1-5f16-49e0-9f8e-c7197fde6624)<br>

   μ: Mean (center of the distribution), highest peak will be at x=μ and −∞<μ<∞.<br>
   σ: Standard deviation (controls the spread), higher the value slower will be decay and vice versa and σ>0.<br><br>
   It is a Bell-shaped and symmetric curve about the mean μ.
 </li><br>

 <li><b>Transformation of Random Variables:</b> It involves mapping a random variable X to another random variable Y using a function g(X).<br><br>
 1)For Discrete RV: PMF of Y can be found by summing over all x that map to the same y:<br>
   
   ![image](https://github.com/user-attachments/assets/534e888a-1d72-4f46-b406-9123639cc661) <br>
   
   Let X be a random variable representing the outcome of a fair 6-sided die roll and Y=X%3.<br>
   Possible values of X={1,2,3,4,5,6} and Y={0,1,2,0,1,2}. So P(Y=y)=2/6=1/3.<br>

2)For Continuous RV: If X is a continuous random variable with a probability density function (PDF) f<sub>X</sub>(x), the PDF of Y is determined using:<br>
  ![image](https://github.com/user-attachments/assets/6274802b-151e-416f-85a0-10018130c37e)
 </li><br>

 <li><b>Cumulative Distribution Function (CDF):</b> It tells us the probability that a random variable X is less than or equal to a certain value x. It tells you the probability up to any point x.<br>
   1)For Discrete RV: The CDF is the cumulative sum of probabilities.<br>
Example: Tossing a fair die: P(X≤3)=P(X=1)+P(X=2)+P(X=3)= 1/6 + 1/6 +1/6 = 1/2/<br>

   2)For Continuous RV: Here, you integrate the Probability Density Function (PDF) over all values up to x.<br>
   P(X≤x)=∫(−∞ to x) f(t)dt </li>

   <b><h2>Note:</h2></b> The area under the CDF curve is not necessarily 1.
</ul>
