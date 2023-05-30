# Elements of a Probabilistic Model

- The **sample space Ω**, which is the set of all possible outcomes of an
  experiment.
- The **probability law**, which assigns to a set A of possible outcomes (also called an event) a nonnegative number **P(A)** (called the **probability of A**) that encodes our knowledge or belief about the collective “likelihood” of the elements of A. The probability law must satisfy certain properties to be introduced shortly.

# Probability Axioms

1. (**Nonnegativity**) P(A) ≥ 0, for every event A.
2. (**Additivity**) If A and B are two disjoint events, then the probability of their union satisfies
   
   $P(A ∪ B) = {P(A) + P(B)}$
   
   More generally, if the sample space has an infinite number of elements and A1 , A2 , . . . is a sequence of disjoint events, then the probability of their union satisfies

   $P(A1 ∪A2 ∪···) = {P(A1)+P(A2)+···}.$

3. (**Normalization**) The probability of the entire sample space Ω is equal to 1, that is, 
   
   $P(Ω) = 1.$

# Discrete Probability Law

If the sample space consists of a finite number of possible outcomes, then the probability law is specified by the probabilities of the events that consist of a single element. In particular, the probability of any event {s1, s2, . . . , sn} is the sum of the probabilities of its elements:

  $P({s1, s2, . . . , sn}) = {P(s1) + P(s2) + · · · + P(sn)}.$

# Discrete Uniform Probability Law

If the sample space consists of n possible outcomes which are equally likely (i.e., all single-element events have the same probability), then the proba- bility of any event A is given by

  $P(A) = {number\ of\ elements\ of\ A \over n}$

# Some Properties of Probability Laws

Consider a probability law, and let A, B, and C be events.

- (a) $IfA⊂B,thenP(A)≤P(B).$
- (b) $P(A∪B)=P(A)+P(B)−P(A∩B).$
- (c) $P(A∪B)≤P(A)+P(B).$
- (d) $P(A∪B∪C)=P(A)+P(Ac ∩B)+P(Ac ∩Bc ∩C).$

# Venn disgrams

![Venn Diagram](./images/Venn_diagram.jpeg)

### At least two of the events A, B, C occur.

- Regions: 2 4 5 6
- $(A \cap B) \cup (A \cap C) \cup (B \cap C)$

### At most two of the events A, B, C occur.

- Regions: 1 2 3 5 6 7 8
- $(A \cap B \cap C)^c$

### None of the events A, B, C occurs.

- Region: 8
- $A^c \cap B^c \cap C^c$

### All three events A, B, C occur:

- Region: 4
- $A \cup B \cup C$

### Exactly one of the events A, B, C occurs.

- Regions: 1 3 7
- $(A \cap B^c \cap C^c) \cup (A^c \cap B \cap C^c) \cup (A^c \cap B^c \cap C)$

### Events A and B occur, but C does not occur.

- Region: 2
- $ A \cap B \cap C^c $

### Either (i) event occurs, or (ii) neither or occurs.

- Regions: 1 2 3 4 6 8
- $B \cup (B^c \cap C^c)$

# Conditional Probabilites
$P(A|B) =$ "probability of A given that B occured"

$P(A|B) = {P(A \cap B) \over P(B)}$

Exercise
1. If Ω is finite and we have a discrete uniform probability law, and if $B \neq 0$, then the conditional probability law on B given that B occurred, is also discrete uniform.
        
   - **True**, because the outcomes inside B  maintain the same relative proportions as in the original probability law.

2. If Ω is finite and we have a discrete uniform probability law, and if $B \neq 0$, then the conditional probability law on Ω, given that B occurred, is also discrete uniform.
        
   - **False**. Outcomes in Ω that are outside B have zero conditional probability, so it cannot be the case that all outcomes in Ω have the same conditional probability.
4. [die roll example](https://learning.edx.org/course/course-v1:MITx+6.431x+2T2023/block-v1:MITx+6.431x+2T2023+type@sequential+block@Lec__2_Conditioning_and_Bayes_rule/block-v1:MITx+6.431x+2T2023+type@vertical+block@ch4-s2-tab4)
5. $IF A \cap C = \phi, then P(A \cup C | B) = P(A | B) + P(C | B)$

### 7. A radar example: models based on conditional probabilities and three basic tools
![image](https://github.com/Simon-Xu-Lan/MIT-MicroMaster/assets/60492659/26653816-6816-4c60-af79-eb0b2cadf799)

### The Multiplication Rule

$P(A|B) = {P(A \cap B) \over P(B)}$

#### The probability that two events occur is equal to the probability that a first event occurs, event B in this case, times the conditional probability that the second event, event A, occurs, given that event B has occurred.
We are free to choose which one (A or B) as the first event.

$P(A \cap B) = P(B)P(A|B) = P(A)P(B|A)$

In other words, we can calculate the probability of a leaf by just multiplying the probabilities of the different branches involved and where we use conditional probabilities for the intermediate branches.

$P(A \cap B \cap C) = P(A)P(A|B)P(A|A \cap B)$

![image](https://github.com/Simon-Xu-Lan/MIT-MicroMaster/assets/60492659/fd4ae164-14b2-4ba6-b543-d4c5a0df984e)

#### Total probability theorem
In words, the probability that an event occurs is a weighted average of the probability that it has under each possible scenario, where the weights are the probabilities of the different scenarios.

![image](https://github.com/Simon-Xu-Lan/MIT-MicroMaster/assets/60492659/fb146d01-ae45-4121-b171-ac7cdf68d5dd)

### Bayes' Rule

![image](https://github.com/Simon-Xu-Lan/MIT-MicroMaster/assets/60492659/7389f534-86a1-4f7c-9751-96c78c51f47c)

### 13. Exercise: Bayes' rule and the false-positive puzzle
A test for a certain rare disease is assumed to be correct  of the time: if a person has the disease, the test result is positive with probability , and if the person does not have the disease, the test result is negative with probability . A person drawn at random from a certain population has probability  of having the disease.
1. Find the probability that a random person tests positive. 
2. Given that the person just tested positive, what is the probability he actually has the disease?
Let A be the event that the person has the desease, and B the event that the test result is positive.
- The probability taht a random person tests positive is
  
  $P(B) = P(A)(P(B|A) + P(A^c)P(B|A^c) = 0.001 * 0.95 + 0.999 * 0.05 = 0.0509$
  
- Given that the person just tested positive, what is the probability he actually has the disease

  $P(A|B) = {P(A)P(B|A) \over P(B)} = {0.001 * 0..95 \over 0.0509} = 0.01866$

# Independence
But if the conditional probability turns out to be the same as the unconditional probability, then the occurrence of event A does not carry any useful information on whether event B will occur. **In such a case, we say that events A and B are independent.**

### 2. A coin tossing example
- Each particular branch corresponds to a sequence of possible results in the different stages, 
- and the leaves of this tree correspond to the possible outcomes.

![image](https://github.com/Simon-Xu-Lan/MIT-MicroMaster/assets/60492659/a2b44d7d-d8b0-49c2-a8a7-11a99080a59f)

**The intuitive meaning of Independence**: 
- Intuitive "defination": $P(B|A) = P(B)$
        - The occurrence of A provides no new information about B.
        - In such case, we may say taht event B is independent from event A.
- Formal Definition of Independence: $P(A \cap B) = P(A)P(B)$
        - The formal definition is symmetric with respect to the roles of A and B. So instead of saying that B is independent from A, we can also say A is independent from B.
        - A and B are independent of each other.
        - Namely, that the conditional probability of A given B is the same as the unconditional probability of A.
        - In contrast, this new definition makes sense even when we're dealing with zero probability events.
#### Disjoint vs Independence
![image](https://github.com/Simon-Xu-Lan/MIT-MicroMaster/assets/60492659/e365aff1-71ff-4e1b-b7b1-8d4031cf89db)
- two events, A and B, both of which have positive probability.
- two events are disjoint.
- They do not have any common elements. **Are these two events independent?**
- The probability that both A and B occur is zero because the two events are disjoint. They cannot happen together.
- The following two expressions are different from each other
  - $P(A \cap B) = 0$
  - $P(A)P(B) > 0$
  - **Conclusion: two events are not independent**
- In fact, intuitively, these two events are as dependent as Siamese twins. If you know that A occurred, then you are sure that B did not occur.
- So the occurrence of A tells you a lot about the occurrence or non-occurrence of B.
**Being independent is somthing completely different from being disjoint.**
- Independence is a relation about information. It is important to always keep in mind the intuitive meaning of independence.
  - **Two events are independent if the occurrence of one event does not change our beliefs about the other.**
  - **It does not affect the probability that the other event also occurs.**
- When do we have independence in the real world?
        - The typical case is when the occurrence or non-occurrence of each of the two events A and B is determined by two physically distinct and non-interacting processes.
        - For example, whether my coin results in heads and whether it will be snowing on New Year's Day are two events that should be modeled as independent.
#### 4. Exercise: Independence of two events - I
 
We have a peculiar coin. When tossed twice, the first toss results in Heads with probability . However, the second toss always yields the same result as the first toss. Thus, the only possible outcomes for a sequence of 2 tosses are  and , and both have equal probabilities. Are the two events $A = \left\{Heads in the first toss\right\}$  and $B = \{Heads in the second toss\}$ independent?
- 
