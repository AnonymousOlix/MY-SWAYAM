# Introduction To Haskell Programming

# Week 4

```
f1 :: [Int] -> [[Int]]
f1 l = [replicate i (l !! i) | i <- [0 .. length l - 1]]

f2 :: [Int] -> [[Int]]
f2 l = [if l !! i > 0 then replicate (l !! i) i else [] | i <- [0 .. length l - 1]]

f3 :: [Int] -> [Int]
f3 [] = []
f3 [_] = []
f3 l = [i | i <- [0 .. length l - 2], l !! i > l !! (i + 1)]

f4 :: [Int] -> [Int]
f4 [] = []
f4 (x:xs) = x : f4 (dropWhile (== x) xs)
```

# Week 7

```
import System.IO

main :: IO ()
main = do
    hSetBuffering stdout NoBuffering  -- Ensures immediate output
    processInput 0

processInput :: Int -> IO ()
processInput sumSoFar = do
    input <- getLine
    if null input
        then return ()  -- Exit on blank line
        else do
            let num = read input :: Int
                newSum = sumSoFar + num
            print newSum
            processInput newSum
```
