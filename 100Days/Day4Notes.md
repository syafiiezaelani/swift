**Loops**
* Your standard for loops. code looks like this: for number in numbers { your code here }
* you can also use for _ in numbers. the underscore tells swift that you dont care about the value that is being read. you only care about doing iteration for each value regardless of the vlaue. 



**While**
var number = 1

while number <= 20 {
    print(number)
    number += 1
}

as long as while loop iterates as true, it will continue running the code. 

**Repeat loop**
var number = 1

repeat {
    print(number)
    number += 1
} while number <= 20

print("Ready or not, here I come!")

* the condition check is at the end of the block of code. so this means that the code will run at least once and will continue to run if the condition is met. 

**Breaking the lopp**
* just use break. usually used with if condition. 

**Breaking nested loops**
* you wanna break the outer loop from the inner loop. first need to label the outer loop, then use break with the outer loop label in the inner loop to break. 

outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")

        if product == 50 {
            print("It's a bullseye!")
            break outerLoop
        }
    }
}

**Continue in loops**
* Continue is when you tell that you're done with the iteration of the for loop and you wanna go to the next one. 
* break on the other hand says that youre done ww the for loop entirely and you wanna continue with the rest of the code. 

**Infinite loop**
* Runs forever, use it quite often. e.g. iphone runs some code, waits for user input then redraw screen. then do it all over again. so when you play game...this happens the whole duration you're playing the game. 


