**Why Swift**
its a new programming language, compared to the rest
makes it hard to write unsafe code
supports all languages out of the box
swift is just a language, that's why swift ui is introduced, apple's framework. 

**About the course**
not gonna learn everything but gonna learn the core, what you gonna use all the time. 

=========== Following along ===========
use xcode. go to file >> playground. this is the best way to learn swift. not to create apps but to learn. 
once you open playground, on the left is your code and on the right is output for your code.

**Creating variables and constants**
var greeting = "Hello, playground"
'var' means variable, means that it can change over time. 
got no semi colon, but dont need to use it, its only used when you want to put two lines of code on the same line. 

var name = "Ted"
name = "Rebecca"

when you want to overwrite a value, you dont have to type in 'var' anymore

creating constants
use 'let'
let name = "Eloise"

when you try to change name here it wont work. 

'print' is how you log to console.
ues camel case, so 'playerName' for example. 

use constant compared to variable. couple of reasons: 
1) allows code to be compiled better cause its constant
2) prevents you from changing variables by mistake. 

**Creating strings**
Can only use double quotes. 
single quotes are use for characters. so e.g. let Fail = 'F'
if you wanna use double quotes use back slashes \ as an escape character. 

**Multi line strings**
Its actually a single string but you wanna make it look nice in your code you cause use triple line quotes.

var burns = """
The best laid schemes
O’ mice and men
Gang aft agley
"""

the code is actually a single line if you were to print it out

**Integer**
same rules apply for constants and variables. so make sure you use the right things. 

to make things easier to read, we use _ instead of commas. e.g 1_000 
swift will just ignore the lower score. 

you can use the basic arithemtic with the vairbles: 
e.g. totalScore / totalNumberOfStudents

there are methods associated with numbers as well. e.g. isMultiple: used to see if the numerb is a multiple of the input number. 

**Floating points or double**
this is for decimal place. 
aka doubles. 

doubles is not the same as integer. 
so if you try to add a double to a double, it wont work cause you cant mix it. 
swift decides if its an integer or a double, if you have a decimal point, it will become a double. 