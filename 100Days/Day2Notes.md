**Booleans**
Same as js, can set as constant and variable. 
can use ! to get opposite of current value. 

**String interpolation**

you can combine string using '+'...not the best cause if you have chain
e.g. "string1" + "string2" + "string3" 
its gonna do one by one, so first create "string1string2" string as a temp and use it to continue to combine. 

that's why string interpolation is there, similar to js `${}`. 
code looks like this " /(variableName)"

will cast the variables as string...if its possible ah. 

what about objects?
class Person {
  let name: String
  let age: Int

  init(name: String, age: Int) {
    self.name = name
    self.age = age
  }
}

let person = Person(name: "Alice", age: 30)
let message = "This person is \(person)"  // message will be "This person is Person(name: "Alice", age: 30)"
print(message)