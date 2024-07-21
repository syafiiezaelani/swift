**Arithmetic**
* standard sings +, -, *, /, %
* cant mix variable types when doing arithmetic, so cant multiply between integer and double. 

**Operator overloading**
* just a fancy of saying that operators do different things depending on data type. e.g. + does something different when comparing integer and string
* can actually change swift operators to suit your needs

**Compound overloading**
* shorthand for certain scenarios of using arithmetic
* its this: 
    var score = 95
    score -= 5  

**Comparison operator**
    firstScore == secondScore
    firstScore != secondScore
* the standard comparisons similar to js. return true or false

* can compare dates if you use the correct types when comparing
* can also do this for enums: 
    enum Sizes: Comparable {
        case small
        case medium
        case large
    }

    let first = Sizes.small
    let second = Sizes.large
    print(first < second) 

* you'll get true cause small comes before large in the enum list. this would also mean that the position of the enums matter...but i guess since you'd rarely use it in such a manner but its good to know that a functionality like this exists. 

**Conditions**
* This is your if else. ww if you just check the condition in the parenthesis which would run the code in curly braces if it returns true. when you have 'else' it would just run the code if 'if' condition return false. 

* can also combine conditions. similar to js. stuff liek && or || hold true. 

**Itenary operator**
*shorthand for if else. same as js.

**Switch cases**
    switch weather {
    case "rain":
        print("Bring an umbrella")
    case "snow":
        print("Wrap up warm")
    case "sunny":
        print("Wear sunscreen")
        fallthrough
    default:
        print("Enjoy your day!")
    }

fallthrough is a keyword where it will run the code of the next cases without even checking the cases. 

**Ranges**
* Look at this switch statement
    let score = 85

    switch score {
    case 0..<50:
        print("You failed badly.")
    case 50..<85:
        print("You did OK.")
    default:
        print("You did great!")
    }
its to evaluate. the arrow means less than so 1 < 50 means that the values is 1 to 49 inclusive of 49. 





