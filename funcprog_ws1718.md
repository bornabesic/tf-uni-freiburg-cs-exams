# Functional Programming
Winter Semester 2017 / 2018  
Prof. Dr. Peter Thiemann  
[Course website](https://proglang.informatik.uni-freiburg.de/teaching/functional-programming/2017/)


## 1. Types

Write the most general type of the expression or describe why the type checking fails.

1) `True`  
    `42`

2)  `(True ||)`  
    `(42 ||)`

3)  `(True, 42)`

4)  `map $ map filter [even, odd]`

## 2. Data types

```hs
data Avengers = Hulk |
                Thor Int |
                Assemble Avengers Avengers
```

1) Write a function `hulk` which returns the number of Hulks in the Avengers assemble.
2) Implement `foldAvengers` (same as `fold` for lists).

Parameters:
```hs
hulk :: r
thor :: Int -> r
assemble :: r -> r -> r
avengers :: Avengers
```

```hs
foldAvengers :: r -> (Int -> r) -> (r -> r -> r) -> Avengers -> r
foldAvengers hulk thor assemble avengers = ?
```

__HINT__:
```hs
data List a = Nil |
              Cons a (List a)

foldList :: r -> (a -> r -> r) -> List a -> r
foldList nil cons list =
    case list of
        Nil -> nil
        (Cons x xs) -> cons x (foldList nil cons xs)
```

3) Rewrite the function `hulk` using `foldAvengers`.

## 3. Laziness

1) What is the return value of the following piece of code?
```hs
let x = 42 `div` 0 in tail [x, 27]
```

2) What is the most general type of the function `iterate`?
```hs
iterate f r = r : iterate (f r)
```

3) What is the value of `result`?
```hs
result = iterate ('x':) "" !! 10
```

## 4. Monads

```hs
test gen f = do
    x <- gen
    y <- gen
    if f x y then return (x, y) else fail ""
```

1) What is the most general type for the function `test`?
2) What are the results of `test [True, False] (&&)` and `test [1..10] (==)`?
3) What monad is used in these examples?
4) Make your own example using some other monad. Describe the result and the type.

## 5. Reader monad

```hs
Reader env a = Reader (env -> a)
```

1) What are the types of `return` and `(>>=)`?
2) Implement these operations.

## 6. Typeclasses

```hs
class Monoid m where
    mempty :: m
    (<>) :: m -> m -> m
```

1) Write the instance of `Monoid` typeclass for `Integer` with the respect to `(+)`
2) Write the instance of `Monoid` typeclass for pair in which both elements have `Monoid` instance
3) `Integer` is also a `Monoid` with respect to `(*)`. How would you combine both of these instances in a single program?

## 7. GADTs: Specialized binary tree

```hs
data Z = Z
data S n = S n

data GTree a n where
    EG :: GTree a Z
    NG :: GTree a n -> a -> GTree a n -> GTree a (S n)
```

1) Give examples for `GTree () Z`, `GTree () (S Z)` and `GTree () (S (S Z))` without using `undefined` :)
2) How many trees are available in `GTree () (S^i (Z))` for every `i`?
3) What is the shape of the trees given by `GTree a (S^i (Z))`?
4) Implement `depth :: GTree a n`
5) ?

## 8. Random regex generator
?
