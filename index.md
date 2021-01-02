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



## Day 15

```csharp
using System;
class Node
{
	public int data;
	public Node next;
    public Node(int d){
        data=d;
        next=null;
    }
		
}
class Solution {

    public static Node GetLastNode(Node N) {  
        Node temp = N;
        while (temp.next != null) {  
            temp = temp.next;  
        }     
        return temp;
    }

	public static  Node insert(Node head,int data)
	{
        //Complete this method
        Node new_node = new Node(data);    
        if (head == null) {    
            head = new_node;    
            return head;    
        }    
        Node lastNode = GetLastNode(head);//GetLastNode(head);    
        lastNode.next = new_node;
        
        return head;
    }

	public static void display(Node head)
	{
		Node start=head;
		while(start!=null)
		{
			Console.Write(start.data+" ");
			start=start.next;
		}
	}
    static void Main(String[] args) {
	
		Node head=null;
        int T=Int32.Parse(Console.ReadLine());
        while(T-->0){
            int data=Int32.Parse(Console.ReadLine());
            head=insert(head,data);
        }
		display(head);
	}
}
```



## Day 16

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
class Solution {

    static void Main(String[] args) {
        string S = Console.ReadLine();
        try{
            int n = int.Parse(S);
            Console.WriteLine(n);
        }catch{
            Console.WriteLine("Bad String");
        }
    }
}

```



## Day 17

```csharp
using System;

//Write your code here
class Calculator{
    public int power(int n, int p){
        if(n<0 || p<0){
            throw new System.ArgumentException("n and p should be non-negative");
        }else{
            return Convert.ToInt32(Math.Pow(n,p));
        }
    }
}

class Solution{
    static void Main(String[] args){
        Calculator myCalculator=new  Calculator();
        int T=Int32.Parse(Console.ReadLine());
        while(T-->0){
            string[] num = Console.ReadLine().Split();
            int n = int.Parse(num[0]);
            int p = int.Parse(num[1]); 
            try{
                int ans=myCalculator.power(n,p);
                Console.WriteLine(ans);
            }
            catch(Exception e){
               Console.WriteLine(e.Message);

            }
        }
        
        
        
    }
}

```



## Day 18

``` csharp
using System;
using System.Collections.Generic;
using System.IO;


class Solution {
    //Write your code here
    Stack<char> st = new Stack<char>();
    Queue<char> q = new Queue<char>();

    void pushCharacter(char c){
        st.Push(c);
    }

    void enqueueCharacter(char c){
        q.Enqueue(c);
    }

    char popCharacter(){
        return st.Pop();
    }

    char dequeueCharacter(){
       return q.Dequeue();
        
    }

    static void Main(String[] args) {
        // read the string s.
        string s = Console.ReadLine();
        
        // create the Solution class object p.
        Solution obj = new Solution();
        
        // push/enqueue all the characters of string s to stack.
        foreach (char c in s) {
            obj.pushCharacter(c);
            obj.enqueueCharacter(c);
        }
        
        bool isPalindrome = true;
        
        // pop the top character from stack.
        // dequeue the first character from queue.
        // compare both the characters.
        for (int i = 0; i < s.Length / 2; i++) {
            if (obj.popCharacter() != obj.dequeueCharacter()) {
                isPalindrome = false;
                
                break;
            }
        }
        
        // finally print whether string s is palindrome or not.
        if (isPalindrome) {
            Console.Write("The word, {0}, is a palindrome.", s);
        } else {
            Console.Write("The word, {0}, is not a palindrome.", s);
        }
    }
}
```



## Day 19

```csharp
using System;
public interface AdvancedArithmetic{
    int divisorSum(int n);
}

public class Calculator : AdvancedArithmetic
{
    public int divisorSum(int n)
    {
        int sum = 0;
        if(n>=1 && n<=1000){
            for(int i = 1 ; i<=n; i++){
                if(n%i==0){
                    sum += i;
                }
            }
        }
        
        return sum;
    }
}

class Solution{
    static void Main(string[] args){
        int n = Int32.Parse(Console.ReadLine());
      	AdvancedArithmetic myCalculator = new Calculator();
        int sum = myCalculator.divisorSum(n);
        Console.WriteLine("I implemented: AdvancedArithmetic\n" + sum); 
    }
}
```



## Day 20

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
class Solution {

    static void Main(String[] args) {
        int n = Convert.ToInt32(Console.ReadLine());
        string[] a_temp = Console.ReadLine().Split(' ');
        int[] a = Array.ConvertAll(a_temp,Int32.Parse);
        // Write Your Code Here
        int temp;
        int swaps=0;
        for (int j = 0; j <= a.Length - 2; j++) {
            for (int i = 0; i <= a.Length - 2; i++) {
               if (a[i] > a[i + 1]) {
                  temp= a[i + 1];
                  a[i + 1] = a[i];
                  a[i] = temp;
                  swaps++;
               }
            }
         }
         Console.WriteLine("Array is sorted in "+swaps+" swaps.");
         Console.WriteLine("First Element: " + a[0]);
         Console.WriteLine("Last Element: " + a[n-1]);

    }
}

```



## Day 21

```csharp
using System;

class Printer
{

	/**
	*    Name: PrintArray
	*    Print each element of the generic array on a new line. Do not return anything.
	*    @param A generic array
	**/
    // Write your code here
    
    static void PrintArray<T>(T[] arr)
    {
        foreach(T a in arr){
            Console.WriteLine(a);
        }
    }


    static void Main(string[] args)
	{
		int n = Convert.ToInt32(Console.ReadLine());
		int[] intArray = new int[n];
		for (int i = 0; i < n; i++)
		{
			intArray[i] = Convert.ToInt32(Console.ReadLine());
		}
		
		n = Convert.ToInt32(Console.ReadLine());
		string[] stringArray = new string[n];
		for (int i = 0; i < n; i++)
		{
			stringArray[i] = Console.ReadLine();
		}
		
		PrintArray<Int32>(intArray);
		PrintArray<String>(stringArray);
	}
}
```



## Day 22

```csharp
using System;
class Node{
    public Node left,right;
    public int data;
    public Node(int data){
        this.data=data;
        left=right=null;
    }
}
class Solution{

	static int getHeight(Node node){
      //Write your code here
        var result = -1;

        if(node != null)
        {
            result = Math.Max(getHeight(node.left), getHeight(node.right)) + 1;
        }

        return result;
    }

	static Node insert(Node root, int data){
        if(root==null){
            return new Node(data);
        }
        else{
            Node cur;
            if(data<=root.data){
                cur=insert(root.left,data);
                root.left=cur;
            }
            else{
                cur=insert(root.right,data);
                root.right=cur;
            }
            return root;
        }
    }
    static void Main(String[] args){
        Node root=null;
        int T=Int32.Parse(Console.ReadLine());
        while(T-->0){
            int data=Int32.Parse(Console.ReadLine());
            root=insert(root,data);            
        }
        int height=getHeight(root);
        Console.WriteLine(height);
        
    }
}
```



## Day 23

```csharp
using System;
using System.Collections;
using System.Collections.Generic;
using System.IO;
using System.Linq;
class Node{
    public Node left,right;
    public int data;
    public Node(int data){
        this.data=data;
        left=right=null;
    }
}
class Solution{

	static void levelOrder(Node root){
  		Queue<Node> q = new Queue<Node>();
        q.Enqueue(root);
        while (q.Count > 0)
        {
            Node n = q.Dequeue();
            Console.Write(n.data + " "); //Only write the value when you dequeue it
            if (n.left !=null)
            {
                q.Enqueue(n.left);//enqueue the left child
            }
            if (n.right !=null)
            {
                q.Enqueue(n.right);//enque the right child
            }
        }



    }

	static Node insert(Node root, int data){
        if(root==null){
            return new Node(data);
        }
        else{
            Node cur;
            if(data<=root.data){
                cur=insert(root.left,data);
                root.left=cur;
            }
            else{
                cur=insert(root.right,data);
                root.right=cur;
            }
            return root;
        }
    }
    static void Main(String[] args){
        Node root=null;
        int T=Int32.Parse(Console.ReadLine());
        while(T-->0){
            int data=Int32.Parse(Console.ReadLine());
            root=insert(root,data);            
        }
        levelOrder(root);
        
    }
}
```



## Day 24

```csharp
using System;
using System.Collections.Generic;
class Node
{
	public int data;
	public Node next;
    public Node(int d){
        data=d;
        next=null;
    }
		
}
class Solution {

  public static Node removeDuplicates(Node head){
    //Write your code here
        /*Another reference to head*/
       
        Node current = head; 
        /* Pointer to store the next  
        pointer of a node to be deleted*/
        Node next_next; 
  
        /* do nothing if the list is empty */
        if (head == null)  
            return null; 
  
        /* Traverse list till the last node */
        while (current.next != null)  
        { 
  
            /*Compare current node with the next node */
            if (current.data == current.next.data)  
            { 
                next_next = current.next.next; 
                current.next = null; 
                current.next = next_next; 
            } 
            else // advance if no deletion 
                current = current.next; 
        }
        return head; 
  }

	public static  Node insert(Node head,int data)
	{
        Node p=new Node(data);
		
		
		if(head==null)
			head=p;
		else if(head.next==null)
			head.next=p;
		else
		{
			Node start=head;
			while(start.next!=null)
				start=start.next;
			start.next=p;
			
		}
		return head;
    }
	public static void display(Node head)
	{
		Node start=head;
		while(start!=null)
		{
			Console.Write(start.data+" ");
			start=start.next;
		}
	}
    static void Main(String[] args) {
	
		Node head=null;
        int T=Int32.Parse(Console.ReadLine());
        while(T-->0){
            int data=Int32.Parse(Console.ReadLine());
            head=insert(head,data);
        }
      	head=removeDuplicates(head);
		display(head);
	}
}
	
```



## Day 25

```
using System;
using System.Collections.Generic;
using System.IO;
class Solution {
    
    static bool IsPrime(int number)
    {
        if(number<2)
            return false;
        if(number==2)
            return true;
        if(number%2==0)
            return false;
        for(int i=3;i<=Math.Sqrt(number);i += 2)
        {
            if(number%i==0)
                return false;
        }
        return true;
    }
    
    static void Main(String[] args) {
       
        int T=int.Parse(Console.ReadLine());
        while(T-->0){
            int data=int.Parse(Console.ReadLine());
            if(IsPrime(data)) Console.WriteLine("Prime");
            else Console.WriteLine("Not prime");
        }
       
    }
}

```



## Day 26

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

class Solution {
    static void Main(String[] args) {
        
        double fine = 0;
        
        int[] returnedDate = Console.ReadLine().Split(' ').Select(x=>Convert.ToInt32(x)).ToArray();
        int[] dueDate = Console.ReadLine().Split(' ').Select(x=>Convert.ToInt32(x)).ToArray();
       
      
        DateTime returned = new DateTime(returnedDate[2],returnedDate[1],returnedDate[0]);
        DateTime due = new DateTime(dueDate[2],dueDate[1],dueDate[0]);
        
               
        double diffDays = (returned-due).TotalDays;
        
        
        if(returned > due){
           
            fine = 10000;
            
            if(returned.Month == due.Month && returned.Year == due.Year){
                fine = diffDays * 15;
            }
            
            if(returned.Month > due.Month && returned.Year == due.Year){
                //Console.WriteLine(diffDays);
                fine = Math.Round(diffDays/30) * 500;
            }
        }
       
       Console.WriteLine(fine.ToString());
             
    }
}

```



## Day 27

```python
def minimum_index(seq):
    if len(seq) == 0:
        raise ValueError("Cannot get the minimum value index from an empty sequence")
    min_idx = 0
    for i in range(1, len(seq)):
        if seq[i] < seq[min_idx]:
            min_idx = i
    return min_idx

class TestDataEmptyArray(object):

    @staticmethod
    def get_array():
        return []
        # complete this function


class TestDataUniqueValues(object):
    data = []
    for i in range(5):
        data.append(i)
    data[::-1]

    @staticmethod
    def get_array():
        return TestDataUniqueValues.data

    @staticmethod
    def get_expected_result():
        data = TestDataUniqueValues.get_array()
        return data.index(min(data))
        # complete this function


class TestDataExactlyTwoDifferentMinimums(object):
    data = []
    for i in range(5):
        data.append(i)
    data[::-1]
    data.insert(0, 0)

    @staticmethod
    def get_array():
        return TestDataExactlyTwoDifferentMinimums.data

    @staticmethod
    def get_expected_result():
        data = TestDataExactlyTwoDifferentMinimums.get_array()
        return data.index(min(data))

```



## Day 28

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

    private List<string> userList {get;set;}
    
    public Solution(List<string> userList){
        this.userList = userList;
    }
    
    public void addUser(string name, string email){
        string theEmailPattern = @"^[\w!#$%&'*+\-/=?\^_`{|}~]+(\.[\w!#$%&'*+\-/=?\^_`{|}~]+)*"
                                   + "@"
                                   + @"gmail.com";
        string namePattern = @"[a-z]";
        
        var isName=Regex.IsMatch(name, namePattern);
        var isEmail=Regex.IsMatch(email, theEmailPattern);
        
        if(isName && isEmail && name.Length<=20 && email.Length<=50){
            userList.Add(name);
        }
        
    }

    static void Main(string[] args) {
        List<string> userList = new List<string>();
        Solution s = new Solution(userList);
         
        int N = Convert.ToInt32(Console.ReadLine());

        for (int NItr = 0; NItr < N; NItr++) {
            string[] firstNameEmailID = Console.ReadLine().Split(' ');

            string firstName = firstNameEmailID[0];

            string emailID = firstNameEmailID[1];
            
            s.addUser(firstName, emailID);
        }
        
        s.userList.Sort();
        foreach(string name in s.userList){
            Console.WriteLine(name);
        }
    }
}

```



## Day 29

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
        int t = Convert.ToInt32(Console.ReadLine());

        for (int tItr = 0; tItr < t; tItr++) {
            string[] nk = Console.ReadLine().Split(' ');

            int N = Convert.ToInt32(nk[0]);

            int K = Convert.ToInt32(nk[1]);
            
            int max = 0;

            for (int j = 1; j < N; j++)
            {
                for (int k = j + 1; k <= N; k++)
                {
                    int h = j & k;
                    if (h < K && max < h) max = h;
                }
            }

            Console.WriteLine(max);
        }
    }
}

```

