# 30 days of coding
## Day 0
```csharp
using System;
using System.Collections.Generic;
using System.IO;

class Solution {
    static void Main(String[] args) {
        // Declare a variable named 'inputString' to hold our input.
        String inputString; 
        
        // Read a full line of input from stdin (cin) and save it to our variable, input_string.
        inputString = Console.ReadLine(); 
        
        // Print a string literal saying "Hello, World." to stdout using cout.
        Console.WriteLine("Hello, World.");
        
        // TODO: Write a line of code here that prints the contents of input_string to stdout.
        Console.WriteLine(inputString);
    }
}
```


## Day 1
```csharp
using System;
using System.Collections.Generic;
using System.IO;

class Solution {
    static void Main(String[] args) {
        int i = 4;
        double d = 4.0;
        string s = "HackerRank ";

        
        // Declare second integer, double, and String variables.
        int ii = Convert.ToInt32(Console.ReadLine());
        double dd = Convert.ToDouble(Console.ReadLine().ToString()); 
        string ss = Console.ReadLine();
        // Read and save an integer, double, and String to your variables.
       
        // Print the sum of both integer variables on a new line.
        Console.WriteLine(i + ii);
        // Print the sum of the double variables on a new line.
        Console.WriteLine("{0:.0}", d + dd);
        // Concatenate and print the String variables on a new line
        // The 's' variable above should be printed first.
        Console.WriteLine(s + ss);

    }
```
Obs: Formatação do output do writeline


## Day 2
```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {

    // Complete the solve function below.
    static void solve(double meal_cost, int tip_percent, int tax_percent) {
        double totalCost=0;
        totalCost = Math.Round( meal_cost + (meal_cost * tip_percent / 100) + (meal_cost * tax_percent/100));

        Console.WriteLine(totalCost);

    }

    static void Main(string[] args) {
        double meal_cost = Convert.ToDouble(Console.ReadLine());

        int tip_percent = Convert.ToInt32(Console.ReadLine());

        int tax_percent = Convert.ToInt32(Console.ReadLine());

        solve(meal_cost, tip_percent, tax_percent);
    }
}
```


## Day 3
```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {



    static void Main(string[] args) {
        int N = Convert.ToInt32(Console.ReadLine());

        if(N % 2 != 0){
            Console.WriteLine("Weird");
        }else{
            if(N >= 2 && N <= 5 ){
                Console.WriteLine("Not Weird");
            }else if(N >= 6 && N <= 20){
                Console.WriteLine("Weird");
            }else if(N > 20){
                Console.WriteLine("Not Weird");
            }else{
                throw new System.Exception();
            }
        }
    }
}
```


## Day 4
```csharp
using System;
using System.Collections.Generic;
using System.IO;

class Person {
    public int age;     
	public Person(int initialAge) {
        // Add some more code to run some checks on initialAge
        if(initialAge<0){
            Console.WriteLine("Age is not valid, setting age to 0.");
            initialAge = 0;
        }
        this.age = initialAge;
     }
     public void amIOld() {
     
        var age = this.age;
        if(age < 13){
            Console.WriteLine("You are young.");
        }else if(age >= 13 && age < 18){
             Console.WriteLine("You are a teenager.");
        }else{
             Console.WriteLine("You are old.");
        }
     }

     public void yearPasses() {
        // Increment the age of the person in here
        this.age +=1;
     }

static void Main(String[] args) {
        int T=int.Parse(Console.In.ReadLine());
        for (int i = 0; i < T; i++) {
            int age=int.Parse(Console.In.ReadLine());
            Person p=new Person(age);
             p.amIOld();
                for (int j = 0; j < 3; j++) {
                  p.yearPasses();
                }
                p.amIOld();
                Console.WriteLine();
        }
    }
}
```


## Day 5
```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {



    static void Main(string[] args) {
        int n = Convert.ToInt32(Console.ReadLine());
        string ns = n.ToString();
        for(int i = 1; i<=10;i++){
            
            Console.WriteLine(ns + " x " + i.ToString() + " = " + (n*i));
        }
    }
}

```


## Day 6
```csharp
using System;
using System.Collections.Generic;
using System.IO;
class Solution {

    static string ReadString(string word){
        
        int wordLength = word.Length;
        string oddChars ="";
        string evenChars="";

        if(wordLength>=2 && wordLength <=10000){
            char[] chars = word.ToCharArray();
            

            for(int i=0; i<wordLength;i++){
                if(i%2==0){
                    evenChars += chars[i];
                }else{
                    oddChars += chars[i];
                }
            }
        }

        return evenChars + " " + oddChars;
    }

    static void Main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution */
        int numberOfCases = Int32.Parse(Console.ReadLine());
        
       

        if(numberOfCases >= 1 && numberOfCases <= 10){
        
            for(int i = 0; i<numberOfCases;i++){
                Console.WriteLine(ReadString(Console.ReadLine()));
            }
           
           
        }
        
    }
}
```


## Day 7

```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {



    static void Main(string[] args) {
        int n = Convert.ToInt32(Console.ReadLine());

        int[] arr = Array.ConvertAll(Console.ReadLine().Split(' '), arrTemp => Convert.ToInt32(arrTemp))
        ;

        string reversed="";
        if(n>=1 && n<=1000){
            Array.Reverse( arr, 0, n );
            for(int i = 0; i < arr.Length; i++){
                if(arr[i]>=1 && arr[i]<10000){
                    reversed += arr[i] + " ";
                }
            }
        }

        Console.WriteLine(reversed);
    }
}
```


## Day 8
```csharp
using System;
using System.Collections.Generic;
using System.IO;
class Solution {

    private Dictionary<string, string> phoneBook;

    public Solution(Dictionary<string, string> phoneBook){
        this.phoneBook = phoneBook;
    }

    public void saveDic(string name, string number){
        try{
          phoneBook.Add(name, number);
        }catch{
            Console.WriteLine("error adding");
        }
    }

    public string search(string s){
        if(phoneBook.ContainsKey(s)){
            return s + "=" + phoneBook[s];
        }
        else{
            return "Not found";
        }
    }

    
    static void Main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution */
        Dictionary<string, string> phoneBook = new Dictionary<string, string>();
        int n = Int32.Parse(Console.ReadLine());
        Solution S = new Solution(phoneBook);
        for(int i = 0; i < n; i++){
            string[] save = Console.ReadLine().Split(' ');
            S.saveDic(save[0], save[1]);
        }
        
        while(true){
            var query = Console.ReadLine();
            if(query==null) break;
            Console.WriteLine(S.search(query));
        }
    }
}
```


## Day 9
```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {

    // Complete the factorial function below.
    static int factorial(int n) {
        if(n==1)
            return 1;
        else
            return n*factorial(n-1);

    }

    static void Main(string[] args) {
        TextWriter textWriter = new StreamWriter(@System.Environment.GetEnvironmentVariable("OUTPUT_PATH"), true);

        int n = Convert.ToInt32(Console.ReadLine());
        if(n>=2 && n<=12){
            int result = factorial(n);

            textWriter.WriteLine(result);

            textWriter.Flush();
            textWriter.Close();
        }
    }
}
```

## Day 10
```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {

    static string converToBin(int num){
        var result = "";
        while (num > 1)
        {
            int remainder = num % 2;
            result = Convert.ToString(remainder) + result;
            num /= 2;
        }
        result = Convert.ToString(num) + result;
        return result;
    }

    static void Main(string[] args) {
        while(true){
            var q = Console.ReadLine();
            if(q==null) break;

            int n = Convert.ToInt32(q);
            
            var bin = Solution.converToBin(n);
           
            int max=0;
            int counter=0;
            if(n>=1 && n<=1000000){
                foreach(var b in bin){
                    if(b=='1'){
                        counter++;
                    }else{
                        
                        counter=0;

                    }

                    if(counter>max){
                        max = counter;
                    }
                }
                Console.WriteLine(max);
            }
            
        }
       
    }
}
```

## Day 11
```csharp
using System.CodeDom.Compiler;
using System.Collections.Generic;
using System.Collections;
using System.ComponentModel;
using System.Diagnostics.CodeAnalysis;
using System.Globalization;
using System.IO;
using System.Linq;
using System.Reflection;
using System.Runtime.Serialization;
using System.Text.RegularExpressions;
using System.Text;
using System;

class Solution {



    static void Main(string[] args) {
        int[][] arr = new int[6][];

        for (int i = 0; i < 6; i++) {
            arr[i] = Array.ConvertAll(Console.ReadLine().Split(' '), arrTemp => Convert.ToInt32(arrTemp));
        }

        int max = int.MinValue;
        
        for(int x=0; x < arr.Length; x++){
            for(int y = 0; y < arr[x].Length; y++){
                if(arr[x][y] > -10 && arr[x][y] < 10){
                    
                    try{
                        int hourglass = 
                                    arr[x][y]   + arr[x][y+1]   + arr[x][y+2]
                                                + arr[x+1][y+1]
                                  + arr[x+2][y] + arr[x+2][y+1] + arr[x+2][y+2];
                                  //Console.WriteLine(hourglass + " " + x + " " + y);
                        
                        if(hourglass > max){
                            max = hourglass;
                        }
                    }catch{

                    }
                }
            }
        }
        Console.WriteLine(max);

    }
}
```


## Day 12
inheritance
```csharp
using System;
using System.Linq;

class Person{
	protected string firstName;
	protected string lastName;
	protected int id;
	
	public Person(){}
	public Person(string firstName, string lastName, int identification){
			this.firstName = firstName;
			this.lastName = lastName;
			this.id = identification;
	}
	public void printPerson(){
		Console.WriteLine("Name: " + lastName + ", " + firstName + "\nID: " + id); 
	}
}

class Student : Person{
    private int[] testScores;  
  
    /*	
    *   Class Constructor
    *   
    *   Parameters: 
    *   firstName - A string denoting the Person's first name.
    *   lastName - A string denoting the Person's last name.
    *   id - An integer denoting the Person's ID number.
    *   scores - An array of integers denoting the Person's test scores.
    */
    protected int[] scores;
    // Write your constructor here
    public Student(string firstName, string lastName, int id, int[] scores){
        this.firstName = firstName;
        this.lastName = lastName;
        this.id = id;
        this.scores = scores;
    }
    /*	
    *   Method Name: Calculate
    *   Return: A character denoting the grade.
    */
    // Write your method here
    public char Calculate(){
         int sumScores = this.scores.Sum() / this.scores.Length;

         //Console.WriteLine(sumScores);

        char result;
        if(sumScores < 40){
            result='T';
        }else if(sumScores >= 40 && sumScores < 55){
            result = 'D';
        }else if(sumScores >= 55 && sumScores < 70){
            result = 'P';
        }else if(sumScores >= 70 && sumScores < 80){
            result = 'A';
        }else if(sumScores >= 80 && sumScores < 90){
            result = 'E';
        }else if(sumScores >= 90 && sumScores <= 100){
            result = 'O';
        }else{
            result = '\0';
        }

        return result;
    }
}

class Solution {
	static void Main() {
		string[] inputs = Console.ReadLine().Split();
		string firstName = inputs[0];
	  	string lastName = inputs[1];
		int id = Convert.ToInt32(inputs[2]);
		int numScores = Convert.ToInt32(Console.ReadLine());
		inputs = Console.ReadLine().Split();
	  	int[] scores = new int[numScores];
		for(int i = 0; i < numScores; i++){
			scores[i]= Convert.ToInt32(inputs[i]);
		} 
	  	
		Student s = new Student(firstName, lastName, id, scores);
		s.printPerson();
		Console.WriteLine("Grade: " + s.Calculate() + "\n");
	}
}
```


## Day 13
Abstract classes
```csharp
using System;
using System.Collections.Generic;
using System.IO;
abstract class Book
{
    
    protected String title;
    protected  String author;
    
    public Book(String t,String a){
        title=t;
        author=a;
    }
    public abstract void display();


}

//Write MyBook class
 class MyBook : Book {

    protected int price;
    public MyBook(string title, string author, int price) : base (title, author){
        this.price  = price;
    }  

    public override void display(){

        Console.WriteLine("Title: " + this.title );
        Console.WriteLine("Author: " + this.author);
        Console.WriteLine("Price: " + this.price);

    }
}

class Solution {
    static void Main(String[] args) {
      String title=Console.ReadLine();
      String author=Console.ReadLine();
      int price=Int32.Parse(Console.ReadLine());
      Book new_novel=new MyBook(title,author,price);
      new_novel.display();
    }
}
```


## Day 14
```csharp
using System;
using System.Linq;

class Difference {
    private int[] elements;
    public int maximumDifference;

	// Add your code here
    public Difference(int[] a){
        elements = a;
    }

    public void computeDifference(){
        int max = int.MinValue;
        var el  = elements;
        for(int i = 0; i<el.Length; i++ ){
            for( int k = 0; k < el.Length; k++ ){
                int diff = Math.Abs(el[i] - el[k] );

                if(diff > max){
                    max = diff;
                }
            }
        }

        maximumDifference = max;
    }

} // End of Difference Class

class Solution {
    static void Main(string[] args) {
        Convert.ToInt32(Console.ReadLine());
        
        int[] a = Console.ReadLine().Split(' ').Select(x=>Convert.ToInt32(x)).ToArray();
        
        Difference d = new Difference(a);
        
        d.computeDifference();
        
        Console.Write(d.maximumDifference);
    }
}
```