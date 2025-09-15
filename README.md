# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
import numpy as np
import math

L = 0
hs = 0
p = []
lk = []

n = int(input("Enter the number of Samples : "))
for i in range(n):
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))
    p.append(pr)

for j in range(n):
    l = float(input(f"Enter the length of the sample values {j + 1}: "))
    lk.append(l)

for k in range(n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1

for k in range(n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs, 3)

eff = hs / L
eff = round(eff, 3)

red = round(1 - eff, 3)

var = 0
for k in range(n):
    var1 = p[k] * (lk[k] - L) ** 2
    var = var + var1
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")

```
# Calculation:

![WhatsApp Image 2025-09-15 at 20 25 19_118a322e](https://github.com/user-attachments/assets/3798d058-a357-4888-ba82-4ebb3820e6bf)

![WhatsApp Image 2025-09-15 at 20 25 19_379ad242](https://github.com/user-attachments/assets/df3cc00c-9771-4428-86b1-27bdb807c581)

![WhatsApp Image 2025-09-15 at 20 25 12_ee07f076](https://github.com/user-attachments/assets/68b1f4a4-4684-4709-9dcd-a186198c0fb4)




# Output

<img width="740" height="454" alt="image" src="https://github.com/user-attachments/assets/9c58b271-f4ed-4f7c-9b43-a93af8863ecd" />
 
# Results:
```
Huffman and Shannon-Fano coding methods were implemented on the provided source. Calculations for average codeword length, entropy, variance, redundancy, and coding efficiency have been carried out successfully.
```
