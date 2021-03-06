# Csharp and dotnet note  
Followed the "Learn C# Basics 1/2/3 of 3 with Scott and Cherita on youtube  
channel: Scott Hannselman  
Followed Développeur C# | Formation complète 2021 on Udemy  
  

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
- string.IsNullOrEmpty => ((myString == "") || (myString == null ))  
- StringBuilder texte = new stringBuilder(); => used to create string quicker than concat. if we have a big string that we modify a lot, we need to use it   
- texte.Append(mytext); => With string builder, we need to append string because concatenation doens't work  
- texte.ToString(); => used to transfor a stringbuilder  
- texte.PadLeft(10, '0'); => will complet the string with char '0' to arrive to 10 character

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
- myList.Select(i=> function(i).ToList()); => use Linq and allow us to make modification without using foreach. Select will select each element and make the modification that we want
 
 
## Int methods  
- int.Parse(elementToParse) => transform an element to a int   
  
## Class/object methods  
- ClassName.OrderBy(e=>e.publicVariable).ToList(); //Linq method  
- use static in a class to create a variable that will stay the same and that we can use to increment number  
- public string name { get; private set; init;}; => variable with properties  
- public string name { get{function mode} set{function mode}} => variable with properties en function mode. If one is in function mode, the other should be in function mode  
- To create a class which inherit from an other one : class children : parent {}  
- To create a constructor from the parent constructor : children() : base(arg that we want from the parents){}
  
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
- using System; => say that we are using the library named System. Allow use to use function like Console.WriteLine();
- using System.IO; => IO mean input output, allow us to use file  
-  
# Files  
** REMARK ** If we want to use the file method inside a backend like mvc or razor pages, we need to use System.IO.File because the file methode already exist !!  
- File.WriteAllText(path, content that we want to add); => ex: File.WriteAllText("myText.txt", "Here is my content inside");  
- File.ReadAllText(path); => read the text from a file ex: String result = File.ReadAllText("myText.txt");  
- File.AppendAllText(filename/path, content to add);  
- File.WriteAllLines(filename/path, myList); => used to write text from a List  
- File.ReadAllLines(filename/path); => Read a file and transform it inside a list instead of a single text;  
- Environment.GetFolderPath(Environment.SpecialFolder.Personal); => Path to the document folder  
- Path.Combine(path, filename); => Linux, Windows and mac doesn't use the same methode for theirs path so this one is used to fit all. ex: string pathAndFile = Path.Combine(path, filename); // Used this methode to save a file in an other place and the programme folder  
- SpecialFolder reference: [Personal == document] [Desktop] []  
- Directory.CreateDirectory(path); => create a foler. Don't forget to used the previous elements if we want to used this directory  
- File.Exists(path/file); => return true if the file exist  
- Directory.Exists(path); => return true if the folder exist  
- File.Copy(fileToCopy, destination copy/new file); => Copy a file  
- File.Delete(path); => Delete a file  
- File.Move(); => used to rename or move a file  
- File.CreateText(path); => used to handle big data. It will directly write the text inside the file instead of allocating memory and then writing it to the file ex: var writeStream = File.CreateText(pathAndFile);  
- writeStream.WriteLine(string to write); => used to write inside the file  
Remark: While using stream methode, we need to delimit it with using because the stream take some memory space. Ex: using(var writeStream = File.CreateText(pathAndFile)){function to execute}  
- File.OpenText(path); => used to open a big file using stream  
- to used JSON, we need packets so rightClick on Dependency>package>package Nuget>search Json> Newtonsoft.Json

# JSON  
- JsonConvert.SerializeObject(myVariable); => Used to transform a variable into a json language. It can have string, int, list, ...  
- File.ReadAlltext(myJsonFile.json); => This can be used to read the data. Check below for more info  
- JsonConvert.DeserializeObject<Personne>(myVariable); => Convert JSON to C#. Use the class Personne as a model  
- Warning, if the Class have the variables in private, we need to have a constructor which is public. But it's better to use variables with Get and private Set with a constructor. The constructor will allow to set the values while using Deserialize and the get will allow to get the data while serialize
- Warning2, function won't be inside because it isn't data  
# Path  
While using path, we can have some issue according to the methode. It can try to access the computer path or the server path.  
If we want to refer the server path, we need to use [IWebHostEnvironment](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.hosting.iwebhostenvironment?view=aspnetcore-3.1) see also [StackOverFlow](https://stackoverflow.com/questions/49398965/what-is-the-equivalent-of-server-mappath-in-asp-net-core)
# WebClient  
** used to make API request **  
- using WebClient from using system.net  
- var webClient = new WebClient();  
- webClient.DownloadString(url); => http get  ex: .txt, .html, .json, ... The return will be a string
- webClient.UploadString(); => http post  
- webClient.DownloadFile(url, name that you want to give); => .jpg, ... The return will be void because it will download the file and that's all  
- webClient.UploadFile();  
- webClient.DownloadData();  
- webClient.UploadData();  
*There is also asyn methods !*  
  
## DateTime ##  
- DateTime date = DateTime.Now(); => Get the current date and hour  
- date.Year  
- date.Month  
- date.ToString("dd/MM/yyyy HH:mm:ss");  => use to string to format date
- date.ToString("dddd"); => Monday, Tuesday, ....  
- CultureInfo cultureFrancais = CultureInfo.GetCultureInfo("fr-FR");  Get the info from the viewer to optimise the date
- date.ToString("dd/MM/yyyy HH:mm:ss", cultureFrançais);  
- DateTime tomorrow = date.AddDays(1);  => Get tomorrow date  
- var diff = tomorrow-date;  => diff.TotalDays // to know how many days OR diff.TotalHours // to know how many hours OR ...  
## Generate vue from a model ##  
1) Create the folder where you want the vue (Create, Read, Delete, update)  
2) Compile the project (right click generate)  
3) Select the target folder> right click> create new automatic element generation> Razor page with Entity Framework (CRUD)> select class and context>add  
  
##Datbase  
To Use the database, there is the ORM EntityFrameWork to help us  
###Link in database  
- many-to-one => exemple a book have one author: ```class book { public Author Author {get; set;}}```  
- one-to-many => exemple an author have multiple book: ```class Author{public ICollection<Book> Books{get; set;}}```  
- ```await _context.Books.Include(b=>b.Author).ToListAsync());``` => Include the Author from the book to the data, it's a join. On the html side ```item.Author.Name```  
###Migration  
- ```add-migration <name>```  
- ```update-database```  
- ```update-database <name of the migration>``` => To roll back add the name of the migration  
- ```remove-migration <name>```=> To remove a migration but won't change the database  
- ```migrationBuilder.RenameColumn("Genre", "Books", "StyleOfBook");``` => ```migrationBuilder.RenameColumn(<column name to change>, <table>, <new column name>);``` == Inside the migraiton, note inside the command line ! REMARK: we need to make it like this because the migration doesn't know when we change the name  
!! REMARK !! We need always to write inside the up and down but reverse to roll back exemple: I want to change a column name:  
```
protected override void up(MigrationBuilder migrationBuilder{ 
  migrationBuilder.RenameColumn("Genre", "Books", "StyleOfBook"); 
  } 
  
protected override void Down(MigrationBuilder migrationBuilder{ 
  migrationBuilder.RenameColumn("StyleOfBook", "Books", "Genre"); 
  }
```
# Note :  
- All methods start with a Capital letter  
- In Vs code, the while tipping, the 3d square is a method => .ToUpper(),  .ToLower(), ...
- In Vs cide, the wrench is a property =>   .Length  
- Don't forget semicolon ;  
- use \\ for path file because only one \ is an escape character  
- delegate => used to add function as argument inside an other function
  

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
 - ctrl+k + c to comment code and ctrl+k+u to uncomment

# Asp.net core  
## How to take info from a data base and return it as a json for exemple
* Like for all database related, we need to have a model *  
1) create create a variable named _context with private readonly ProjectName.FolderName.FileName => ex:  
    private readonly Pizza_Pito.Data.DataContext _context;  
2) create a constructor wich take the above dataContext as a variable and assign it inside => ex:  
  ```
    public ApiController(Pizza_Pito.Data.DataContext context)
    {
    _context = context;
    }  
  ```
3) create a list from the class => ex:  
  ```
    public IList<Pizza> Pizza { get; set; }  
  ```
4) make a function to assign the data to the created list => ex:  
  ```
    public async Task OnGetAsync()
        {
            Pizza = await _context.Pizzas.ToListAsync();
        }  
```
# Make new project  
- Create a folder named models  
- Create a class file for the models  
- Add properties to the class  
__  
- Create a data folder  
- Create the datacontext file class in the data folder to link the models to the database with entity framework  
- Inside the: dataContext is just a name. The main part is that it is a child from DbContext  (from entityFrameworkCore)  
- Define a constructor that take options parameter => see documentation  
- Declare which model to use  
__  
- initiate the dataContext inside Startup.cs>ConfigureServices> service.AddDbContext.....  
__  
- Add the connection string inside appsettings.json "ConnectionStrings":{"DefaultConnection": "Data Source = fileName.db"},  
__  
- If we want to use make a link to the database while clicking a page, we need to:  
1) create a variable with a DataContext type.  
2) add it to the constructor  
3) asign it with the constructor.  
For more info, check Dotnet core Dependency injection  
```
  public class IndexModel : PageModel
    {
        private readonly ILogger<IndexModel> _logger;

        DataContext dataContext;

        public IndexModel(ILogger<IndexModel> logger, DataContext dataContext)
        {
            _logger = logger;
            this.dataContext = dataContext;
        }

        public void OnGet()
        {
            var user = new User() {firstName = "test de la data base" };
            dataContext.Users.Add(user);
            dataContext.SaveChanges();

        }
    }
```
After that, we can create a new object. But before having the possibility to add this object to the database, we need to update the Program.cs to create the table before host.Run  
__  
- Change the program.cs file to create the table  
*To create db if not exist*
```  
  //CreateHostBuilder(args).Build().Run();
  var host = CreateHostBuilder(args).Build();
  CreateDbIfNotExists(host);
  host.Run();  
```  
*The function*  
 ```
  private static void CreateDbIfNotExists(IHost host)
        {
            using (var scope = host.Services.CreateScope())
            {
                var services = scope.ServiceProvider;
                try
                {
                    var context = services.GetRequiredService<DataContext>();
                    context.Database.EnsureCreated();
                }
                catch (Exception ex)
                {
                    var logger = services.GetRequiredService<ILogger<Program>>();
                    logger.LogError(ex, "An error occurred creating the DB.");
                }
            }
        }
 ``` 
