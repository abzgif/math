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

(খ) 1500 এর চেয়ে ক্ষুদ্রতর সকল সংখ্যা নির্ণয়ের Mathematica command লেখ যার Prime ও Fibonacci উভয়ই হয়। এরুপ সংখ্যা মোট কতটি তাও নির্ণয় কর।
___
    (*1.b*)
```
k=1; t1={};
While[Prime[k]<1500, t1 = Append[t1, Prime[k]];k++]
k=1; t2={};
While[Fibonacci[k]<1500, t2=Append[t2, Fibonacci[k]];k++]
result=Intersection[t1, t2]
```
Out:{2, 3, 5, 13, 89, 233}
```
    Length [result]
```
Out:6
