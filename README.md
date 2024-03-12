১। (ক) Mathematica-এর সাহায্যে Do lopp, For loop While loop ব্যবহার করে যোগফল নির্ণয় কর:
1+1+3/2!+1+3+3^2/3!+....50 পদ পর্যন্ত
___
    (*1.a*)
```
    \!\(\(sum = 0;\)\[IndentingNewLine]
  Do[sum = sum + 1\/\(n!\)*\(3^n - 1\)\/\(3 - 
    1\), {n, 1, 50}]\[IndentingNewLine]
  sum // N\)
```
Out:8.68363
```
    \!\(\(sum = 0;\)\[IndentingNewLine]
  Do[sum = sum + 1\/\(n!\)*\(3^n - 1\)\/\(3 - 
    1\), {n, 1, 50}]\[IndentingNewLine]
  sum // N\)
```
Out:8.68363
```
    \!\(While[n ≤ 50, sum = sum + 1\/\(n!\)*\(3^n - 
      1\)\/\(3 - 1\); n = n + 1]\[IndentingNewLine]
  sum // N\)
```
Out:8.68363
