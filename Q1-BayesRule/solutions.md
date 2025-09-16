# Q1 – Bayes Rule Applied to Text

---

## 1. Meaning of terms

- **P(c):** This is the *prior probability* of a class.  
  It tells us how likely a document belongs to class `c` before looking at the actual words in the document.  
  Example: If 70% of training documents are "sports" and 30% are "politics", then P(sports) = 0.7 and P(politics) = 0.3.  

- **P(d|c):** This is the *likelihood*, meaning the probability of seeing the document `d` given that it comes from class `c`.  
  Example: If the class is "sports", words like "game", "team", "score" will appear more often, so a document containing those words has a high P(d|sports).  

- **P(c|d):** This is the *posterior probability*, meaning the probability that the document belongs to class `c` after observing its words.  
  This is the final quantity we care about when classifying a document (deciding its label).  

---

## 2. Why P(d) can be ignored when comparing classes

The denominator P(d) is the same for all classes because it just means “the overall probability of seeing this document.”  
When we compare classes (e.g., is this document sports or politics?), P(d) does not change across classes, so it does not affect which class has the higher probability.  
That’s why we can ignore P(d) and just compare the numerator P(c) × P(d|c).  
This simplification makes computation easier without changing the classification result.  
