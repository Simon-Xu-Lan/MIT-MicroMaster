# Elements of a Probabilistic Model

- The **sample space Ω**, which is the set of all possible outcomes of an
  experiment.
- The **probability law**, which assigns to a set A of possible outcomes (also called an event) a nonnegative number **P(A)** (called the **probability of A**) that encodes our knowledge or belief about the collective “likelihood” of the elements of A. The probability law must satisfy certain properties to be introduced shortly.

# Probability Axioms

1. (**Nonnegativity**) P(A) ≥ 0, for every event A.
2. (**Additivity**) If A and B are two disjoint events, then the probability of their union satisfies
   
   $P(A ∪ B) = {P(A) + P(B)}$
   $N = {1, 2, 3, 4, . . .}$

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
