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
- float number = 1.75f; => float number  
- double number = 1.75d; => double number. It's like float but more precise. So better check before use it  
- string [] arrayName = new string [3]; => create an array of 3 strings   
- string[] otherArr = {"hello", "test", "world"}; => initialize an array named otherArr with 3 strings  
- const int NUMBER_MIN = 0 ; => to make a const variable  
- enum => a kind of variable that store value more or less like an object in javascript. Need to look further  
- **Class**  
- class MyClass {  
 *variables*  
 *constructor*  
 *method*  
 }
- 
## Variable from module:  
- List<int> liste = new List<int>();
- var liste = new List<int>();
- var liste = new List<int>(){"item1", "item2", "item3"};
- ArrayList a = new ArrayList(); // It isn't possible to use differents types inside an array or a list. But we can with an arraylist so not strictly typed => like javascript array but mixed type isn't a good practice
- var a = new ArrayList();
- var d = new Dictionary<string, string>(); create a new dictionary that will work with key value. it work like an object in javascript.
 exemple: d.Add("John", "0032492123456");
- 
  
## Concat string:  
Console.WriteLine("Hello " + aFriend); //  
  

## String interpolation( an other kind of concatenation):  
- Console.WriteLine($"Hello {aFriend}");  //a little like ECScript 2015 except that the dollar sign is before the string  
- @ before a string allow litteral. It will keep spacing, tab and avoid escaping character exemple : Console.WriteLine(@"   c:\source\repos   
      (this is where your code goes)");  
- we can also combine $@ before a string   
  
## Comments  
- // => single line comment  
- /* */ => multiple line comment  
- '' => only one charactere  => char a string with one character doesn't exist
- "" => a string  
- Console.WriteLine(12.3m); => use m after the number to tell C# that we want to use a decimal. Note: we can use m or M   
  
# Methods  
*Need to know Tris and Linq*  
*Good to know Passing Reference*
## String methods  
- .ToUpper() => change to upper case  // we can add culture inside because the letter aren't the same in all country ex: myString.ToUpper(new CultureInfo("en-US", false)
- .ToLower() => change to lower case  
- .ToReplace(wordToReplace, newWord) => to replace a word by an other one  
- .Contains(wordToSeachFor) => check the string who contain a word and return true or false  
- .Trim() => remove white space before and after a string  
- .TrimEnd() => remove white space after a string  
- .TrimStart() => remove white space before a string  
- .StartWith(Item to check) => check if the element start with a specified item.  
- we can use [] to select a character like in javascript
- we can use \n to return line  
  

## Array methods 
- .Length => length of the array. 
- foreach(int items in inventory){} => foreach method  
- Array.Sort(myArr);
## Listes methods  
- myList.Add(itemToAdd); => add an item to the list  
- myList.Count => it's the same as length method for string or array  
- myList.Remove(number or string to match) => will delete the first item that match the argument  
- myList.RemoveAt(item position) => will delete the item at a determined position  
- myList.Contains(item to match); => check if the list contain a value and return a bool  
- myList.GetRange(0, 3); => return 3 items in the list starting at position 0 
- myList.Sort();  => sort in the alphabetic ascendant order.  
- myList.OrderBy(e=> effect to give); => using Linq to add feature to the sort method (shallow copy)
 
 
## Int methods  
- int.Parse(elementToParse) => transform an element to a int   
  
## Class/object methods  
- ClassName.OrderBy(e=>e.publicVariable).ToList(); //Linq method  
- use static in a class to create a variable that will stay the same and that we can use to increment number  
- public string name { get; private set; init;}; => variable with properties  
- public string name { get{function mode} set{function mode}} => variable with properties en function mode. If one is in function mode, the other should be in function mode  
- 
  
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
static int functionName(string parametreName) {} => function returning int taking string parametre


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
- an array have a defined number of content. if we don't know it, we need to use the Lists  
- if we remove an item from a list while using a loop, we need to start from the end because the list length change.  
- Don't put too much stuff in public. If we need to access a name or something, use as much as possible function(accessor) to avoid erasing the values OR properties  
- For more info about properties and accessor check section 10 (105 and 106)  
- Check string builder  
- Private: access only within the function or class / Public: access everywhere / protected: it's private but the childrens can access them with inheritance  
- 

 # ShortCut Visual Studio  
 - cw tab tab => Console.WriteLine();
 - try/catch work barely like javascript except that we need to pay attention to the scope  
 - 

