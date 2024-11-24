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
   </li><br>

  <li><b>Expectation of Transformed RV:</b> The expectation of a transformed random variable Y=g(X) is given by the formula:<br>
  E[Y]=E[g(X)]= ∑ g(x)P(X=x)</li><br>

  <li><b>Moments:</b> Moments are quantitative measures related to the shape of a probability distribution. Moments help describe various properties of a distribution, such as its location, spread, skewness, and kurtosis.<br>

  <ul>
    <li><b>Raw Moments:</b> Raw moments are calculated with respect to the origin (zero):<br>
      𝜇<sub>n</sub>′=E[X<sup>n</sup>]</li><br>

  <li><b>Central Moments:</b> Central moments are calculated with respect to the mean (μ):<br>
      𝜇<sub>n</sub>=E[(X−μ)<sup>n</sup>] where: μ<sub>n</sub>: n-th central moment and μ: Mean of the distribution.<br><br>
      
Key central moments:<br>
<ol type='1'>
<li>First moment(μ<sub>1</sub>): Always 0 (since it measures deviation from the mean).</li>
<li>Second moment(μ<sub>2</sub>): Variance (𝜎<sup>2</sup>).</li>
<li>Third moment (μ<sub>3</sub>): Measures skewness (asymmetry of the distribution).</li>
<li>Fourth moment (μ<sub>4</sub>): Measures kurtosis (tailedness of the distribution).</li></li></ol>
  </ul>
</li><br>

  <li><b>Variance:</b> Variance is a measure of how much the values in a data set deviate from the mean (average) of that set. It tells you the spread or dispersion of the data points around the mean. If the variance is high, it indicates that the data points are spread out over a large range of values.
If the variance is low, it means that the data points are closer to the mean.<br>
    
  ![image](https://github.com/user-attachments/assets/636852f9-24e1-4fb4-9559-7f071807d4e2)

Var(X)=E[X<sup>2</sup>] - (E[X])<sup>2</sup></li><br>

<li><b>Skewness:</b> Skewness is a statistical measure that describes the asymmetry of the distribution of values in a dataset or a probability distribution. It indicates whether the data is skewed (or lopsided) to the left or right.<br><br>
Types:
  <ol type='1'>
    <li><b>Positive Skew (Right Skew)</b>: The right tail of the distribution is longer or fatter than the left.<br>
Most of the data points are concentrated on the left side, with fewer but larger values on the right.<br>
For a positively skewed distribution, the mean is greater than the median.<br>
Example: Income distribution in a country, where most people earn below average, but a few earn extremely high amounts.</li><br>

   <li><b>Negative Skew (Left Skew):</b> The left tail of the distribution is longer or fatter than the right.</br>
Most of the data points are concentrated on the right side, with fewer but smaller values on the left.</br>
For a negatively skewed distribution, the mean is less than the median.</br>
Example: Age of retirement, where most people retire at around 60-70, but a few retire earlier.</li></br>

<li><b>Zero Skew (Symmetrical Distribution):</b> The distribution is symmetrical, meaning the left and right tails are mirror images of each other.</br>
For a perfectly symmetrical distribution, the mean equals the median.<br>
Example: A normal distribution has zero skew.</li>
  </ol><br>

![image](https://github.com/user-attachments/assets/8750ae3d-e1fb-4ce5-8561-868b87000ff2)

</li><br>

<li><b>Kurtosis:</b> Kurtosis is a statistical measure that describes the shape of a probability distribution's tails and the sharpness (peakedness) of its central peak. In simple terms, it gives us an idea of how outlier-prone a distribution is compared to a normal distribution.<br.<br>
Types:
<ol type='1'>
  <li><b>Leptokurtic:</b> Distributions with positive kurtosis are called leptokurtic. They have fatter tails and a higher peak compared to the normal distribution.<br>
Leptokurtic distributions tend to have more extreme values (outliers), indicating a higher likelihood of extreme events.</li><br>

<li><b>Platykurtic:</b>Distributions with negative kurtosis are called platykurtic. They have thin tails and a lower peak than a normal distribution.</br>
Platykurtic distributions have fewer outliers and are more spread out.</li><br>

<li><b>Mesokurtic:</b>A normal distribution has zero excess kurtosis and is called mesokurtic. It serves as a reference distribution.<br>
It has neither excessively fat tails nor overly thin tails.</li>
</ol><br>

![image](https://github.com/user-attachments/assets/fd46febc-1d4c-47d5-b2eb-cb8ea6a47593)

When calculating kurtosis directly from the formula, the result for a normal distribution is 3. To make the comparison more meaningful, we subtract 3 from the kurtosis value, which makes the kurtosis of the normal distribution equal to 0. This adjustment is known as the excess kurtosis. If we don't subtract 3, we have to take normal value as 3 and comparisons to be made with 3 and not 0.</li><br>

<li><b>Multiple Random Variables:</b> When dealing with multiple random variables, we study the relationships and interactions between two or more random variables.

<ul>
  <li><b>Joint Probability Distribution:</b> For two or more random variables, the joint probability distribution describes the probability that each of the variables takes on a specific value simultaneously.<br>
    
  ![image](https://github.com/user-attachments/assets/8b35d962-2b53-45d1-8009-8406fb3a75ac)
</li><br>

<li><b>Marginal Distribution:</b> The marginal distribution of one variable is obtained by summing (discrete) or integrating (continuous) over the other variable in the joint distribution.<br>

![image](https://github.com/user-attachments/assets/f53e5559-ecc8-4ac9-8f64-ab630d3bf8f3)
</li><br>

<li><b>Independence of Random Variables:</b> Two random variables X and Y are independent if:<br>
  P(X=x,Y=y)=P(X=x)⋅P(Y=y)  (Discrete)<br>
  f<sub>X,Y</sub>(x,y)=f<sub>X</sub>(x).f<sub>Y</sub>(y)  (Continuous)</li><br>

  <li><b>Covariance:</b> Covariance measures the degree to which two random variables vary together.<br>
    In simpler terms, it tells us:<br>
    How two variables are related: Whether an increase in one variable corresponds to an increase or decrease in the other.<br>
    Direction of relationship: Positive covariance indicates that the variables increase together, while negative covariance means one increases as the other decreases.<br><br>
  
  Let X and Y be two random variables. The covariance is given by:<br>
  Cov(X,Y) = E[(X−E[X])(Y−E[Y])] = E[XY] - E[X]E[Y] 
  </li><br>

  <li><b>Correlation:</b> </li>
</ul>
</li><br>

<li><b>Expectation for Multiple Random Variables:</b><br>
  1) Discrete RV:<br>
  
  ![image](https://github.com/user-attachments/assets/2813545d-da0d-4025-8736-edcf3cb5bc33)<br>

  2)Continuous RV:<br>

  ![image](https://github.com/user-attachments/assets/078731e3-7470-45ee-903a-e78fb949b68d)
</li><br>

<b><h2>Note:</h2></b> The expectation of the sum of multiple random variables is always linear, regardless of whether the random variables are independent or dependent.<br>

E[X<sub>1</sub> + X<sub>2</sub> + ... + X<sub>n</sub>] = E[X<sub>1</sub>] + E[X<sub>2</sub>] + .. + E[X<sub>n</sub>]<br><br>

<b><h2>Note:</h2></b> The expectation of the product of multiple random variables <b>if and only if random variables are independent:</b><br>

E[X<sub>1</sub>.X<sub>2</sub>....X<sub>n</sub>] = E[X<sub>1</sub>].E[X<sub>2</sub>]....E[X<sub>n</sub>]<br><br>

<li><b></b></li>

</ul>
