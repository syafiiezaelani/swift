**Closure**

Now think about this: what if my app behaves badly, and takes 10 seconds to respond to Siri? Remember, the user doesn’t actually see my app, just Siri, so from their perspective it looks like Siri has completely frozen.

This would be a terrible user experience, so Apple uses closures instead: it launches our app in the background and passes in a closure that we can call when we’re done. Our app then can take as long as it wants to figure out what work needs to be done, and when we’re finished we call the closure to send back data to Siri. Using a closure to send back data rather than returning a value from the function means Siri doesn’t need to wait for the function to complete, so it can keep its user interface interactive – it won’t freeze up.

Another common example is making network requests. Your average iPhone can do several billion things a second, but connecting to a server in Japan takes half a second or more – it’s almost glacial compared to the speed things happen on your device. So, when we request data from the internet we do so with closures: “please fetch this data, and when you’re done run this closure.” Again, it means we don’t force our user interface to freeze while some slow work is happening.

Closure vs functions
Functions:

Independent: Functions are self-contained units of code with a defined name, parameters, and return type. They don't inherently capture variables from their surrounding scope.
Named: Functions always have a name that identifies them within your code.
Scope: Variables used within a function are local to that function and cannot be accessed directly from outside.

Closures:

Anonymous (Optional): Closures can be anonymous (without a name) or named.
Can Capture Values: Closures can access and potentially modify variables from their surrounding context (like the function or loop where they were created). This is called "capturing."
Flexibility: Closures can be passed around as arguments to functions, used as return values, and stored in variables, offering more flexibility in code design.

* Basic closure
    Treats a function like a variable. can pass that function or call said function. basic closure looks like this: 
        let driving = {
            print("I'm driving in my car")
        }

    can invoke said function liek this: driving()

* Passing params to closures: 
    let driving = { (place: String) in
        print("I'm going to \(place) in my car")
    }

    the params are in the braces, 'in' is where the main body of the closure starts. there are no param labels for closure. 

* Return values. closures can also return values. code looks like this: 

    let drivingWithReturn = { (place: String) -> String in
        return "I'm going to \(place) in my car"
    }
    you can see that the arrow before 'in' tells us the type to be returned. 
    to return a value where the closure doesnt take any params would be like this: 

    let payment = { () -> Bool in
        print("Paying an anonymous person…")
        return true
    }

* Using closures as parameter. 
    this is what your closure looks like. 
    let driving = {
        print("I'm driving in my car")
    }

    func travel(action: () -> Void) { // We are passing a closure to this function. 
        print("I'm getting ready to go.")
        action()
        print("I arrived!")
    }

to use: travel(driving)

* Trailing closure syntax. 
    This is a function using closure as a param: 

    func travel(action: () -> Void) {
        print("I'm getting ready to go.")
        action()
        print("I arrived!")
    }

    since its last param is a closure, we can pass the closure to the function using trailing closure syntax. it will look like this: 

    travel() { // The curly braces is an unnamed closure. you did not assign the closure to a variable and passing said variable into travel, you straight away pass the closure to travel like this. 
        print("I'm driving in my car")
    }

    Since no other params for that function, we can remove the parenthesis entire and just pass in the closure as such. 
    
    travel {
        print("I'm driving in my car")
    }

