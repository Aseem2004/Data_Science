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

   <b><h2>Note:</h2></b> The area under the CDF curve is not necessarily 1.<br>

   <li><b>Expectations:</b> Expectation (or Expected Value) is a key concept in probability and statistics that represents the average or mean value of a random variable if the experiment were to be repeated many times.<br><br>
   1)For a discrete random variable X, the expected value is calculated as: E[X]= ∑ x<sub>i</sub>.P(x<sub>i</sub>), where x<sub>i</sub> are possible values of x and P(x<sub>i</sub>) is probability of x<sub>i</sub>.<br>
   Example: For a fair 6-sided die, the possible outcomes are 1, 2, 3, 4, 5, and 6. Since the die is fair, the probability of each outcome is 1/6<br>
The expected value is: E[X]= 1/6 (1+2+3+4+5+6)=3.5<br>
So, the expected value of a roll of a fair die is 3.5, even though it’s not possible to roll a 3.5. It represents the average outcome if you roll the die many times.<br><br>

2)For a continuous random variable, the expected value is calculated as: E[X]=∫(−∞ to ∞) f(x)dx where, f(x) is the probability density function (PDF) of the random variable X.<br>

Expectations of:<br>
<ol type='A'>
  <li>Bernoulli RV: The expectation of a Bernoulli random variable X is the probability of success of the Bernoulli trial.<br>
  E[X]=p<br>
  This makes sense intuitively, as p represents the probability of success, which is the average value of X over many trials.</li><br>

  <li>Geometric RV:The expectation of a Geometric random variable X, which represents the number of trials required to get the first success in a sequence of independent Bernoulli trials with success probability p, is given by: E[X] = 1/p<br>
    The mean of a Geometric random variable X depends inversely on p. If the probability of success p is high, fewer trials are needed on average to achieve the first success, and vice versa.</li><br>

  <li>Binomial RV: The expectation of a Binomial random variable X is given by the formula: E[X]=n⋅p<br>
  The expected number of successes in n independent trials is simply the number of trials n multiplied by the probability of success p for each trial.</li><br>

  <li>Uniform Distribution: The expectation of a Uniform random variable X is given by the formula: E[X] = (a+b)/2<br>
    Since the uniform distribution is symmetric and all outcomes are equally likely within the interval [a,b], the expected value (or the mean) is simply the midpoint of the interval [a,b].</li><br>

  <li>Exponential Distribution: The expectation of an Exponential random variable X with rate parameter λ (inverse scale parameter) is given by the formula: E[X] = 1/λ<br>
  If λ is small, events occur less frequently, and the expected time between events is larger.</li><br>

  <li>Gaussian Distribution: The expectation (mean) of a Gaussian random variable X with mean μ and standard deviation σ is: E[X]=μ<br>
   For a Gaussian random variable, the expectation is simply the mean μ, reflecting the symmetry of the distribution around this central point.</li>
</ol></li><br>

<li><b>Law of Large Numbers:</b> It is a fundamental theorem in probability theory that describes the result of performing the same experiment a large number of times. It essentially states that as the number of trials or observations increases, the sample average (or sample mean) will get closer to the expected value (or population mean / true mean) of the random variable.<br>
Example:<br>
If you flip a coin 10 times, you might get 6 heads and 4 tails. The sample mean would be 0.6.<br>
If you flip the coin 100 times, you might get 52 heads and 48 tails. The sample mean would be 0.52.<br>
If you flip the coin 10,000 times, you might get 5,000 heads and 5,000 tails. The sample mean would be very close to 0.5.<br><br>
It doesn't mean the sample mean will be exactly the expected value every time, but rather that it will get closer to the true average as the sample size grows larger.
</li><br>

   <li><b>Independent and Identically Distributed (i.i.d.) Random Variables:</b> Two or more random variables are said to be independent if the occurrence or outcome of one does not affect the occurrence or outcome of the other(s).Random variables are said to be identically distributed if they have the same probability distribution. This means that they share the same type of distribution (such as Normal, Binomial, Poisson, etc.), with identical parameters (mean, variance, etc.).<br>
   When random variables are both independent and identically distributed, they are referred to as i.i.d. random variables. This means that not only are the random variables independent of each other (no variable’s outcome influences another), but they also follow the same probability distribution (they all have the same type and parameters of distribution).</li><br>

   <li><b>Easy Comparison:</b><br><br>
   <table>
  <thead>
    <tr>
      <th>Random Variable</th>
      <th>Expectation (E[X])</th>
      <th>Range of X</th>
      <th>Range of Parameters</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bernoulli</td>
      <td>p</td>
      <td>{0, 1}</td>
      <td>0 ≤ p ≤ 1 (probability of success)</td>
    </tr>
    <tr>
      <td>Geometric</td>
      <td>1/p</td>
      <td>{1, 2, 3, ...}</td>
      <td>0 < p ≤ 1 (probability of success)</td>
    </tr>
    <tr>
      <td>Binomial</td>
      <td>n × p</td>
      <td>{0, 1, 2, ..., n}</td>
      <td>
        n: positive integer<br>
        0 ≤ p ≤ 1 (probability of success)
      </td>
    </tr>
    <tr>
      <td>Uniform (Continuous)</td>
      <td>(a + b) / 2</td>
      <td>[a, b]</td>
      <td>
        a < b<br>
        a, b: any real numbers
      </td>
    </tr>
    <tr>
      <td>Exponential</td>
      <td>1/λ</td>
      <td>[0, ∞)</td>
      <td>λ > 0 (rate parameter)</td>
    </tr>
    <tr>
      <td>Gaussian (Normal)</td>
      <td>μ</td>
      <td>(-∞, ∞)</td>
      <td>
        μ: any real number (mean)<br>
        σ > 0 (standard deviation)
      </td>
    </tr>
  </tbody>
</table>
   </li>
</ul>
