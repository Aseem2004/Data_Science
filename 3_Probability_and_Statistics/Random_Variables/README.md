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
</ul>
