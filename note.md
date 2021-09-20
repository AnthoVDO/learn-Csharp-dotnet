# Csharp and dotnet note  
I followed the "Learn C# Basics 1/2/3 of 3 with Scott and Cherita on youtube  
channel: Scott Hannselman  
## Use console:  
Console.WriteLine("Hello, world!");  //to have a single line;  
Console.Write("Hello, world"); //with this one, if we add this console, there won't be any return line
## Build-in variables:  
- string => string myVariable = "John";  // it work with camelCase, PascalCase, kabbo-case, ...  
- interger => int myNumber = 17; 
- character => char c = 'C';  
- double => double j = 5.5d;  // for more info, check the difference between float, double, ... There is a memory space tricks for that;
- var => used when we don't know which kind of variable we will asign. Remark, after the first assignement, it won't be possible to change the kind of variable. So if we assign a string, it won't be possible to assign a int for exemple.
- bool => boolean  
- decimal => number with decimal. Need to add m or M after the number.  
- string [] arrayName = new string [3]; => create an array of 3 strings   
- string[] otherArr = {"hello", "test", "world"}; => initialize an array named otherArr with 3 strings
## concat string:  
Console.WriteLine("Hello " + aFriend); //  
## string interpolation( an other kind of concatenation):  
- Console.WriteLine($"Hello {aFriend}");  //a little like ECScript 2015 except that the dollar sign is before the string  
- @ before a string allow litteral. It will keep spacing, tab and avoid escaping character exemple : Console.WriteLine(@"   c:\source\repos   
      (this is where your code goes)");  
- we can also combine $@ before a string 
## comments  
- // => single line comment  
- /* */ => multiple line comment  
- '' => only one charactere  
- "" => a string  
- Console.WriteLine(12.3m); => use m after the number to tell C# that we want to use a decimal. Note: we can use m or M 
# Methods  
## String methods  
- .ToUpper() => change to upper case  // we can add culture inside because the letter aren't the same in all country ex: myString.ToUpper(new CultureInfo("en-US", false)
- .ToLower() => change to lower case  
- .ToReplace(wordToReplace, newWord) => to replace a word by an other one  
- .Contains(wordToSeachFor) => check the string who contain a word and return true or false  
- .Trim() => remove white space before and after a string  
- .TrimEnd() => remove white space after a string  
- .TrimStart() => remove white space before a string  
- .StartWith(Item to check) => check if the element start with a specified item.  
-  
## Array methods 
- .Length => length of the array. 
- foreach(int items in inventory){} => foreach method  
  
## Int methods  
int.Parse(elementToParse) => transform an element to a int  
# Operator  
- + - * /  
- += -= *= /=
- == >= <= != // there is no ===   
- > <  
- || &&  
- \ => escape character ex: \n add a line, \t add a tabulation

# Conditional  
- if is the same as javascript => if(){}  // curly bracket are optionnal if there is only one line
- ternary operator like in javascript => question ? answer A : answer B;  
- switch case is the same as javascript  
# Loop  
- For loop => same as javascript  
- foreach(var name in arrNames){console.WriteLine(name)};  
- while and while do => same as javascript  
  
# Function  
static int functionName(){} => to create a function, we use: static, value that the function return (int here), name, arguments, curly brackets
static myName = Antho => The word static is used to make a variable global. So I can use it in other function  
void => mean empty so the function is executed but return nothing. We can use it with a global variable  


# Library  
- using System => say that we are using the library named System. Allow use to use function like Console.WriteLine();


# Note :  
- All methods start with a Capital letter  
- In Vs code, the while tipping, the 3d square is a method => .ToUpper(),  .ToLower(), ...
- In Vs cide, the wrench is a property =>   .Length  
- Don't forget semicolon ;  
- use \\ for path file because only one \ is an escape character  
# Remark :  
- Learn more about float, integer and double  
- To show special character add this line before the console : Console.OutputEncoding = System.Text.Encoding.UTF8;   
- Better to use function which return value so try to avoid static void 
  
 # ShortCut Visual Studio  
 - cw tab tab => Console.WriteLine();
 - try/catch work barely like javascript except that we need to pay attention to the scope  
 - 

