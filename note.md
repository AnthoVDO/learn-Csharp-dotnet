# Csharp and dotnet note  
I followed the "Learn C# Basics 1/2/3 of 3 with Scott and Cherita on youtube  
channel: Scott Hannselman  
## Use console:  
Console.WriteLine("Hello, world!");  
## Build-in variables:  
- string => string myVariable = "John";  // it work with camelCase, PascalCase, kabbo-case, ...  
- interger => int myNumber = 17; 
- character => char c = 'C';  
- double => double j = 5.5d;  // for more info, check the difference between float, double, ... There is a memory space tricks for that;
- var => used when we don't know which kind of variable we will asign. Remark, after the first assignement, it won't be possible to change the kind of variable. So if we assign a string, it won't be possible to assign a int for exemple.
- bool => boolean  
- 
## concat string:  
Console.WriteLine("Hello " + aFriend); //  
## string interpolation( an other kind of concatenation):  
Console.WriteLine($"Hello {aFriend}");  //a little like ECScript 2015 except that the dollar sign is before the string   
## comments  
- // => single line comment  
- /* */ => multiple line comment  
# Methods  
## String methods  
- .ToUpper() => change to upper case  // we can add culture inside because the letter aren't the same in all country ex: myString.ToUpper(new CultureInfo("en-US", false)
- .ToLower() => change to lower case  
- .ToReplace(wordToReplace, newWord) => to replace a word by an other one  
- .Contains(wordToSeachFor) => check the string who contain a word and return true or false  
- .Trim() => remove white space before and after a string  
- .TrimEnd() => remove white space after a string  
- .TrimStart() => remove white space before a string  
# Operator  
- + - * /  
- += -= *= /=
- == >= <= != // there is no ===   
- > <  

# Loops  
- if is the same as javascript => if(){}  // curly bracket are optionnal if there is only one line
- ternary operator like in javascript => question ? answer A : answer B;  
- 


# Note :  
- All methods start with a Capital letter  
- In Vs code, the while tipping, the 3d square is a method => .ToUpper(),  .ToLower(), ...
- In Vs cide, the wrench is a property =>   .Length  
- Don't forget semicolon ;  
-   
# Remark :  
- Learn more about float, integer and double  
- 

