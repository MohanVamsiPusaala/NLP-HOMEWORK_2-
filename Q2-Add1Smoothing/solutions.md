# Q2 – Add-1 Smoothing

---

### Given:
- Priors: P(−) = 3/5, P(+) = 2/5  
- Vocabulary size = 20  
- For the negative class: total token count = 14  

---

## 1. Denominator for likelihood estimation

With add-1 smoothing, the denominator is:  

**Total tokens in class + Vocabulary size**  
= 14 + 20  
= **34**

So every probability in the negative class will be divided by 34.

---

## 2. P(predictable | −)

The word "predictable" occurs 2 times in negative documents.  
Formula with add-1 smoothing:  

**(count(word) + 1) / (total tokens + V)**  
= (2 + 1) / 34  
= 3 / 34  
≈ **0.088**

---

## 3. P(fun | −)

The word "fun" never appeared in negative docs (count = 0).  
Formula:  

**(0 + 1) / 34**  
= 1 / 34  
≈ **0.029**

---

### Final Notes
- Denominator (34) stays the same for all words in the negative class.  
- Add-1 smoothing makes sure even unseen words (like "fun") get a small non-zero probability.  
