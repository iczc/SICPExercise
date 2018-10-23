### Exercise 1.1:

Below is a sequence of expressions. What is the result printed by the interpreter in response to each  expression? Assume that the sequence is to be evaluated in the order in which it is presented.

```
1 ]=> 10
;Value: 10

1 ]=> (+ 5 3 4)
;Value: 12

1 ]=> (- 9 1)
;Value: 8

1 ]=> (/ 6 2)
;Value: 3

1 ]=> (+ (* 2 4) (- 4 6))
;Value: 6

1 ]=> (define a 3)
;Value: a

1 ]=> (define b (+ a 1))
;Value: b

1 ]=> (+ a b (* a b))
;Value: 19

1 ]=> (= a b)
;Value: #f

1 ]=> (if (and (> b a) (< b (* a b)))
    b
    a)
;Value: 4

1 ]=> (cond ((= a 4) 6)
      ((= b 4) (+ 6 7 a))
      (else 25))
;Value: 16

1 ]=> (+ 2 (if (> b a) b a))
;Value: 6

1 ]=> (* (cond ((> a b) a)
         ((< a b) b)
         (else -1))
    (+ a 1))
;Value: 16
```

### Exercise 1.2:

Translate the following expression into prefix form:

![\frac{5 + 4 + \left(2 - \left(3 - (6 + \frac{4}{5})\right)\right)}{3(6 - 2)(2 - 7)}`](https://latex.codecogs.com/gif.latex?%5Cfrac%7B5%20&plus;%204%20&plus;%20%5Cleft%282%20-%20%5Cleft%283%20-%20%286%20&plus;%20%5Cfrac%7B4%7D%7B5%7D%29%5Cright%29%5Cright%29%7D%7B3%286%20-%202%29%282%20-%207%29%7D%60)



```
1 ]=> ( / (+ 5 4 (- 2 (- 3 (+ 6 (/ 4 5)))))
    (* 3 (- 6 2) (- 2 7)))

;Value: -37/150
```