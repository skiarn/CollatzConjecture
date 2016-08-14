# CollatzConjecture

```
package main

import (
	"fmt"
	"math/big"
)

func main() {
	fmt.Println("CollatzConjecture")

	var n int64 = 71
	fmt.Printf("Number -------- prime \n")
	for n != 1 {
		n = CollatzConjecture(n)
  		i := big.NewInt(n)
		fmt.Printf("%v		%v \n",n, i.ProbablyPrime(4))
	}
}

func CollatzConjectureDoubleStep(n int64) int64 {
	if Odd(n) {
		return ((3*n) +1) / 2
	} else {
		return n / 2
	}
}

func CollatzConjecture(n int64) int64 {
	if Even(n) {
		return n / 2
	} else {
		return (n*3) + 1
	}
}


func Even(number int64) bool {
    return number%2 == 0
}

func Odd(number int64) bool {
    return !Even(number)
}
```
