# Go Goroutine Sample

## Goroutine

## Code
```Go
// Function to generate prime numbers
func primeRoutine1() {
	i := 0
	for {
		i += 1
		if checkPrime(i) {
			fmt.Printf("PrimeRoutine1 ☆ : %d\n", i)
		}
	}
}

// Function to generate prime numbers
func primeRoutine2() {
	i := 0
	for {
		i += 1
		if checkPrime(i) {
			fmt.Printf("PrimeRoutine2 ◇ : %d\n", i)
		}
	}
}

// Function to generate prime numbers
func primeRoutine3() {
	i := 0
	for {
		i += 1
		if checkPrime(i) {
			fmt.Printf("PrimeRoutine3 ◯ : %d\n", i)
		}
	}
}

// Asynchronous generation of prime numbers
func main() {
	
	// Asynchronous processing in Goroutine
	go primeRoutine1()
	go primeRoutine2()
	go primeRoutine3()

	for {
		// Infinite loop to drive main
	}
}
```

## Output Sample
~/Go_Goroutine $ go build main.go  
~/Go_Goroutine $ ./main  
  
 ~ omission ~   
  
PrimeRoutine3 ◯ : 493211  
PrimeRoutine3 ◯ : 493217  
PrimeRoutine2 ◇ : 492799  
PrimeRoutine1 ☆ : 493211  
PrimeRoutine3 ◯ : 493219  
PrimeRoutine1 ☆ : 493217  
PrimeRoutine2 ◇ : 492839  
PrimeRoutine3 ◯ : 493231  
PrimeRoutine1 ☆ : 493219  
PrimeRoutine2 ◇ : 492853  
PrimeRoutine1 ☆ : 493231  
PrimeRoutine3 ◯ : 493243  
PrimeRoutine2 ◇ : 492871  
PrimeRoutine1 ☆ : 493243  
PrimeRoutine3 ◯ : 493249  
PrimeRoutine2 ◇ : 492883  
PrimeRoutine1 ☆ : 493249  
PrimeRoutine3 ◯ : 493277  
PrimeRoutine2 ◇ : 492893  
PrimeRoutine3 ◯ : 493279  
PrimeRoutine1 ☆ : 493277  
  
 ~ omission ~  
