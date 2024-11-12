<ul>
  <li><b>Probability: </b>Probability is the measure of how likely an event is to happen, expressed as a number between 0 and 1, where 0 means impossible and 1 means certain.</li><br>

  <li><b>Probability Law: </b>A probability law, or probability axiom, defines the rules that a probability function must follow when assigning probabilities to events, i.e. it goes from an event to a number.</li><br>

  <li><b>Axioms of probability: </b>
    <ol type='1'>
      <li><b>Non-negativity: </b>The probability of any event A must be a non-negative number: P(A)≥0</li> 
      <li><b>Normalization:</b> The probability of the entire sample space S is 1, meaning that something in the sample space is certain to happen: P(S)=1</li>
      <li><b>Additivity:</b> If A and B are mutually exclusive events, the probability of either A or B occurring is the sum of their individual probabilities: P(A∪B)=P(A)+P(B)</li>
    </ol>
  </li><br>
  <li><b>Some other results:</b>
  <ul>
    <li>P(Φ)=0</li>
    <li>General form: P(A∪B)=P(A)+P(B)-P(A∩B), no restriction on A and B being mutually exclusive.</li>
    <li>P(A)+P(A')=1</li>
  </ul>
  </li><br>

  <li><b>Continuous Probability Model:</b> Till now, we only talked about discrete probability model where probability of every outcome can be calculated. Like, upon rolling a die, we can calculate probabilities of getting each of 1,2,3,4,5 and 6.<br>But a continuous probability model describes scenarios where outcomes are not discrete but can take any value within a range. <b>In such models, probabilities are calculated over intervals instead of specific values, as there are infinitely many possible outcomes.</b></li><br>

  <li><b>Conditional Probability:</b> is the probability of an event occurring given that another event has already occurred. It provides a way to update the probability of an event based on new information. The conditional probability of event A given that event B has occurred is denoted as P(A|B).<br><br>
P(A|B)=P(A ∩ B)/P(B), given P(B)≠0
  </li><br>

  <li><b>Total Probability Theorem:</b> It provides a way to calculate the probability of an event based on a partition of the sample space.<br><br>
  If B1,B2,....,Bn are mutually exclusive events that form a partition of the sample space (i.e., they are non-overlapping and their union covers the entire sample space), and A is any event, then the probability of A can be expressed as:


P(A)=P(A∣B1)P(B1)+P(A∣B2)P(B2)+…+P(A∣Bn)P(Bn)<br>
OR simply as<br>
P(A)=P(A∩B1)+P(A∩B2)+....+P(A∩Bn)</li>

<li><b>Statistical Independence:</b> It refers to a relationship between two events where the occurrence of one event does not affect the probability of the other event occurring.<br>
P(A|B)=P(A) means A does not depend upon B. And A is independent of B also means B is independent of A i.e. P(B|A)=P(B).<br>
For two events, A and B, they are said to be independent if: P(A∩B)=P(A)⋅P(B).<br><br>
  For events A,B, and C to be mutually independent, they must satisfy:<br>
1) P(A∩B)=P(A)⋅P(B)<br>
2) P(A∩C)=P(A)⋅P(C)<br>
3) P(B∩C)=P(B)⋅P(C)<br>
4) P(A∩B∩C)=P(A)⋅P(B)⋅P(C)
</li><br>

<li><b>Conditional Independence:</b> It refers to a situation where two events are independent of each other given the knowledge of a third event. In other words, knowing the outcome of the conditioning event makes the two events behave as if they are independent, even if they might not be independent otherwise.<br>
P(A∩B∣C)=P(A∣C)⋅P(B∣C) or equivalently, P(A∣B∩C)=P(A∣C) and P(B∣A∩C)=P(B∣C)
</li><br>

<li><b>Bayes' Rule:</b>  It is a fundamental theorem in probability that allows us to update the probability of a hypothesis based on new evidence. It provides a way to calculate the conditional probability of an event, given prior knowledge about related events.<br>
For two events, A and B:<br>
P(A∣B)=P(B∣A)⋅P(A)/P(B), where:<br>
1) P(A∣B): The probability of A given that B has occurred (posterior probability).<br>
2) P(B∣A): The probability of B given that A is true (likelihood).<br>
3) P(A): The probability of A occurring (prior probability).<br>
4) P(B): The probability of B occurring (marginal probability).<br>
</li>
  
</ul>
