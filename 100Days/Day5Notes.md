**Functions**
* this is what a function would look like: 
func printHelp() {
    let message = """
Welcome to MyApp!

Run this app inside a directory of images and
MyApp will resize them all into thumbnails
"""

    print(message)
}

* Getting parameters into the function: 
func square(number: Int) {
    print(number * number)
}

* Calling functions with parameters. Have to name the parameter label then pass the value next to it like this: 
let result = square(number: 8)

* To avoid naming parameters when calling the function, need to use underscore when defining the function. when to use this? usually used when your function is a verb and the param is a noun. so greet('john') for example. 
e.g.: 
func greet(_ person: String) {
    print("Hello, \(person)!")
}

* Default values for params: use equal sign. if no value passed when the function called, then function would take the default value. 
func greet(_ person: String, nicely: Bool = true) {
    if nicely == true {
        print("Hello, \(person)!")
    } else {
        print("Oh no, it's \(person) again...")
    }
}

* Variadic functions. you can have none or multiple number of params passed in to the function. all these params will be converted to an array where you going do stuff with it.
e.g. func square(numbers: Int...) {
    for number in numbers {
        print("\(number) squared is \(number * number)")
    }
}

* Throwing errors. first must define enum with swift existing error type
enum PasswordError: Error {
    case obvious
}

your function would look like this: 
func checkPassword(_ password: String) throws -> Bool {
    if password == "password" {
        throw PasswordError.obvious
    }

    return true
}

* Running throwing functions
do {
    try checkPassword("password")
    print("That password is good!")
} catch {
    print("You can't use that password.")
}

need to use 'do'. then 'try' is for throwing function, if any error happens then it will go to catch block

* inout parameters. all parameters passed into a function are constants. using inout allows you to change these parameters, even outside of the function scope. 

this is how to define the code: 
func doubleInPlace(number: inout Int) { // Need inout when declaring the props
    number *= 2
}

this is how to use it: 
var myNum = 10 
doubleInPlace(number: &myNum) // To use variable as inout need to append '&' at the front. 



