# JAVA
## 08/23/2022 
### JAVA Escape Character:
**1. \t: Insert a tab in the text at this point.(you can add more than one \t to make them aligned)**

input: 
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("china\tjapan\tlebron");
    }
}
```
output: 
```
china	japan	lebron
```

**2. \n: change the line**

input:
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("china\njapan\nlebron");
    }
}
```
output: 
```
china
japan
lebron
```
**3. to output back slash: one for one, two for two**

**one back slash**

input:
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("china\\japan\\lebron");
    }
}
```
output:
```
china\japan\lebron
```

**two back slashes**

input:
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("china\\\\japan\\\\lebron");
    }
}
```
output:
```
china\\japan\\lebron
```

**4. to output double/single quote: add one bask slash before the 1st quote and another one before the second quote**

input: 
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("\"china\\japan\\lebron\"");
    }
}
```
output:
```
"china\japan\lebron"
```

**5. \r: Insert a carriage return in the text at this point.(content before it will be replaced by those after since it is at the same line by default)**

input:
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("china\rjapanlebron");
    }
}
```
output:clearly, "china" is replaced by japanlebron. 
```
japanlebron
```

**to solve it, add one \n after \r so it goes to the second line**

input:
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("china\r\njapanlebron"); 
    }
}
```
output: 
```
china
japanlebron
```

### Comment
**1. single line comment:**
```
//comment
```

**2. multiple line comment:(nested multiple line comment is not allowed)**
```
/* comment */
```

**3. if asterisk is also needed for each line of comment:**
```
/**the univerity is not around
 * 
 */
```

### Small tips to trim your code
**1.Select code and press "tab" key, move code to the right**

**2.Select code and press "tab" + "shift" keys, move the code to the left**

## 08/25/2022
### Relationship between JDK, JRE and JVM:
**1.JDK= JRE + JAVA Development Tools**

**2.JRE = JVM + Core Class Library**

### Variables
#### Rules about using variables in JAVA: 
**1.Variables can be defined in different classes**

input:
```
public class class082222 {
    public static void main(String[] args){
        int a = 1;
        System.out.println(a);
    }
}

class comeon {                                   //there could be more than one class in one program, but only one public class
    public static void main(String[] args) {
        int a = 250;
System.out.println(a);
    }
}
```
output (if run the first one)
```
1
```
output (if run the second one)
```
250
```

#### How "+" works in program
**1.When both sides are number(double or integer), then mathematical added up**

input:
```
public class class082222 {
    public static void main(String[] args){
        System.out.println(70+4);
    }
}
```
output:
```
74
```

**2.When either of sides is a string, generate string in the end, just put them together** 

input:
```
public class class082222 {
    public static void main(String[] args){
        System.out.println("100Nick"+4);
    }
}
```
output:
```
100Nick4
```

#### Sizes of primitive Data/Variables(in byte)(1 byte = 8 bit )
**1.Metric variables (for integers)**
```
int[4]
short[2]
long[8]
```

**2.Metric variables(for decimal)**
```
float[4]
double[8]
```

**3.Char**
```
char[2]：for single char like： 'a'
boolean[1]：only for true or false
```

#### Details of integer
**1."int" is set for integer by default in JAVA, and to claim a long type, we have to add an "l" or "L"**

input:
```
public class class082222 {
    public static void main(String[] args){
        long a = 114L;             //"L" is optional, but int a= 114L would be wrong.
        System.out.println(a);
    }
}
```
output:
```
114
```

#### Details of float
**1."double" is set default by JAVA, and to claim a float, we have to add a "f" or "F"**

input:
```
public class class082222 {
    public static void main(String[] args){
        float a = 1.1f;
        double b = 1.1f;
        System.out.println(a);
        System.out.println(b);
    }
}
```
output:
```
1.1
1.100000023841858               //double is more accurate that float
```
**2.directly compare two floats after operation may be risky**

input:
```
public class class082222 {
    public static void main(String[] args){
        double b = 8.1/3;
        double c = 2.7;
        if(b==c){
            System.out.println("you are from China");
        }else
        {
            System.out.println(b);
        }
    }
}
```
output:
```
2.6999999999999997
```

#### Details of Char
**1.char can only store one single char**

input:
```
public class class082222 {
    public static void main(String[] args){
        char a = 'a';
        char b = '\t';
        char c = '真';
        char d = '9';
        System.out.println(a);
        System.out.println(b);
        System.out.println(c);
        System.out.println(d);
    }
}
```
output:
```
a
	
真
9
```

**2.Char can participate in operation, each char has its corresponding value in ASCII chart**

**operation between char and char**

input:
```
public class class082222 {
    public static void main(String[] args){
        char c1 = 'l';
        char c2 = 'K';
        System.out.println(c1+c2);
        }
    }
```
output:
```
183
```

**operation between char and other data/variables**

input:
```
public class class082222 {
    public static void main(String[] args){
        char a = 'a';                          // char is different from a string
        int b = 1;
        System.out.println(a+b);
    }
}
```
output:
```
98                 //This shows the ASCII value of 'a' is 97
```

#### Details of Boolean
**1.Boolean only allows "true" and "false"**

input:
```
public class class082222 {
    public static void main(String[] args){
        boolean result = true;
        if(result!=false){      //!= false equivalent to = true
            System.out.println("congratulations! ");
        }
    }
}
```
output:
```
congratulations!
```

#### Automatic data/variable conversion
**1.Accuracy increases from left to right(backward compatibility)**

**char-int-long-float-double**


**byte-short-int-long-float-double**


input:
```
public class class082222 {
    public static void main(String[] args){
        int a= 'c';                           //this will convert 'c' to the corresponding value in ASCII
            System.out.println(a);
        }
    }
```
output:
```
99
```

**2.no automatic conversion between byte, short and char**

**3. Boolean never participates in conversion**

#### Forced data/variable conversion (anti-backward compatbility)
**1.take the risk of losing accuracy**

input:
```
public class class082222 {
    public static void main(String[] args){
        int a = (int)1.9;                         //(int) means force to int
        System.out.println("a is" +" "+ a);       // in JAVA we use "+" to link, instead of "," in Python
        }
    }
```
output:
```
a is 1
```

#### Conversion between data/variable and string
**1.Add "" after the data/variable can make it converted to a String**

input:
```
public class class082222 {
    public static void main(String[] args){
        int a = 6;
        String b = a+"";
        System.out.println(b);
        }
    }
```
output:
```
6                      //this 6 is a string, this conversion essentially is from "how '+' works". when a string + a data, the final result is a string
```

**2. Use parse to convert a String(except a char)**

input:
```
public class class082222 {
    public static void main(String[] args){
        String a= "125";
                int b = Integer.parseInt(a);
                double c = Double.parseDouble(a);
                float d = Float.parseFloat(a);
                long e = Long.parseLong(a);
                byte f = Byte.parseByte(a);
                boolean g = Boolean.parseBoolean(a);
                short h = Short.parseShort(a);
        System.out.println(b);
        System.out.println(c);
        System.out.println(d);
        System.out.println(e);
        System.out.println(f);
        System.out.println(g);
        System.out.println(h);
        }
    }
```
output:
```
125
125.0
125.0
125
125
false
125
```

**Even in parse, we can still modify the string we're gonna convert**

input:
```
public class class082222 {
    public static void main(String[] args){
        String a= "125";
              double c = Double.parseDouble(a+1);            //the operation in bracket goes first
              System.out.println(c);
        }
    }
```
output:
```
1251.0
```

## 09/03/22
### JAVA Operators
#### "++" in JAVA**
**1.a++, assign value first then execute operation**

input:
```
public class ForExample {
    public static void main(String[] hell){
       int a =4;
       int b =a++;
       System.out.println(a);
        System.out.println(b);
    }
}
```
output:
```
5
4
```

**2.++a, execute operation first then assign value**

input:
```
public class ForExample {
    public static void main(String[] hell){
       int a =4;
       int b =++a;
       System.out.println(a);
        System.out.println(b);
    }
}
```
output:
```
5
5
```

#### Relational operator
**1.Relational operators work like boolean when printing out**

input:
```
public class ForExample {
    public static void main(String[] hell){
       int a=8;
       int b=9;
       System.out.println(a>b);
        System.out.println(a==b);
        System.out.println(a!=b);
        boolean flag = a>b;       //declare a boolean to help understand
        System.out.println(flag);  
    }
}
```
output:
```
false
false
true
false
```

#### Logic Operators
**1. &&(与): if both true, then true logic operator. If the first one is false, then the second condition won't be tested, higher efficiency**

**2. &:if both true, then true logic operator. Even if the first one is false, the second condition will still be tested, lower efficiency** 

**3. Most of the time we use "&&"**

**4. ||(或): if the first condition is true, then true. The second addition will not be tested, higher efficiency**

**5. |: Even if the first one is true, the second condition will still be tested, lower efficiency**

**6. Most of the time we use "||"**

#### Inverse Operators:
**1.!**

input:
```
public class ForExample {
    public static void main(String[] hell){
      System.out.println(60==50);
      System.out.println(!(60==50));
    }
}
```
output:
```
false
true
```

**2.^: when a and b are different(not both true, not both false), output "true", or we have a "false"**

input:
```
public class ForExample {
    public static void main(String[] hell){
      System.out.println((10>5)^(5<3));      //Or you can declare a boolean: boolean b = (10>5)^(5<3);
    }
}
```
output:
```
true
```

#### Assignment Operators
**1. +=, -=, *=, /=, %=**

For example:
```
a+=b equal to a=a+b 
```

#### Ternary Operation (三元运算符)
**1.condition?operation if true; operation if false;**

input:
```
public static void main(String[] hell){
        int a=9;
        int b=19;
        int c=a==b? a+=9: b++;      //ternary operation consists of condition(ends with ?), Operation when true, Operation when false
        System.out.print(c);
    }
}
```
output:
```
19
```
**2. In Ternary Operation, still pay attention to the difference between a++ and ++a**

input:
```
public class ForExample {
    public static void main(String[] hell){
        double a=9;
        double b=19;
        double c= a==b?--b:a++;         // in this case, condition should be false, output equal to c=a++ 
        System.out.println(c);          // Thus, c=a++, assign value then ++
        System.out.print(a);            // print a after ++
    }
}
```
output:
```
9.0
10.0
```

**3.Use Ternary operation to find the biggest number from three number**

input: 
```
public class ForExample {
    public static void main(String[] hell){
       int a= 55;
       int b = 33;
       int c= 147;
       int first = a>b?a:b;          //find the bigger one between a and b. 
       int second =  first>c?first:c;     // after getting the bigger one from a and b, we try to find the biggest one among a, b and c.
       System.out.print(second);
    }
}
```
output:
```
147
```

## 09/05/22
### Interaction with customers
#### Scanner
**1. How to use scanner to interact with customers**

Input:
```
import java.util.Scanner;                                                        //introduce Scanner
public class ForExample {
    public static void main(String[] hell){
        Scanner myScanner = new Scanner(System.in);                              //declare a scanner and build it in the system
        System.out.println("number of floors you want to build for pyramid");    //print indication
        int number = myScanner.nextInt();                                        //declare variable provided for scanner
        for(int i=1;i<=number;i++){
            for (int j=1;j<=number-i;j++){
                System.out.print(" ");
            }
            for (int k=1;k<=2*i-1;k++){
                System.out.print("*");
            }
            System.out.println();
        }
    }

```
Output:
```
number of floors you want to build for pyramid
7
      *
     ***
    *****
   *******
  *********
 ***********
*************

```

**2. Another example for Scanner**

Input:
```
import  java.util.Scanner;                               //really important keep in mind
public class ForExample {
    public static void main(String[] hell){              
        Scanner myScanner = new Scanner(System.in);      //build the value in, also important
        System.out.println("Name");
        String name = myScanner.next();                  //for string, directly next()
        System.out.println("Age");  
        int age = myScanner.nextInt();                   //for integer, use nextInt(). Similarly, for double, we use nextDouble()
        System.out.println("Gender");
        String gender = myScanner.next();
        if(age>25){
            System.out.println("you are dead meat");
        }else System.out.println("I'll let you go");
    }
    }

```
Output:
```
Name
Nick
Age
25
Gender
male
I'll let you go
```

## 09/07/22
### Binary fundamental:
#### Signed magnitude representation(原码), 1's complement(反码) and two's complement(补码):
**1.Signed magnitude representation(原码)**

正数三码合一，负数按绝对值转化为binary,最高位补1(这是符号位)

**2.1's complement(反码)**

正数三码合一，负数的反码对该数的原码除了符号位外各位取反

**3.two's complement(补码)**

正数三码合一，负数的补码为反码+1

**4.计算机运算过程中都是用二进制的补码进行操作！！！！！！(to unify negative number and positive number)**

input:
```
class bitewise{
    public static void main(String[] tired){
        int a=10;
        System.out.println(Integer.toBinaryString(a));
        System.out.println(-a);
        System.out.println(Integer.toBinaryString(-a));
    }
}
```
output:
```
1010
-10
11111111111111111111111111110110              //这里输出的是-10的补码
```


### Bitewise Operation(同样的都通过补码来运算)
#### 7 operation symbols:
**1. &: 同位全为1，结果为1，否则为0**

input:
```
class bitewise{
    public static void main(String[] tired){
        int a=0B100;
        int b= 0B0110;
        System.out.println("results before positional operation:"+a+"\n"+b);
        System.out.println("Decimal result after operation:"+(a&b));
        System.out.println("Binary result after operation:"+Integer.toBinaryString(a&b));    //Integer.toBinaryString() is the way to keep binary 
    }
}
```
output:
```
results before positional operation:4
6
Decimal result after operation:4
Binary result after operation:100
```

**2. |:同位有一个为1，结果为1**

input:
```
class bitewise{
    public static void main(String[] tired){
        int a=0B100;
        int b= 0B0110;
        System.out.println("results before positional operation:"+a+"\n"+b);
        System.out.println("Decimal result after operation:"+(a|b));
        System.out.println("Binary result after operation:"+Integer.toBinaryString(a|b));
    }
}
```
output:
```
results before positional operation:4
6
Decimal result after operation:6
Binary result after operation:110
```

**3. ^:异或，同位不同则为1，相同则为0**

input:
```
class bitewise{
    public static void main(String[] tired){
        int a=0B100;
        int b= 0B110;
        System.out.println("results before positional operation:"+a+"\n"+b);
        System.out.println("Decimal result after operation:"+(a^b));
        System.out.println("Binary result after operation:"+Integer.toBinaryString(a^b));
    }
}
```
output:
```
results before positional operation:4
6
Decimal result after operation:2
Binary result after operation:10
```

**4. ~:0转为1，1转为0(符号位也会转)**
input:
```
class bitewise{
    public static void main(String[] tired){
        int a=10;
        System.out.println(Integer.toBinaryString(a));
        System.out.println(Integer.toBinaryString(~a));
    }
}
```
output:
```
1010
11111111111111111111111111110101        
```

**5. >>:本质等于除以n个2**

input:
```
class bitewise{
    public static void main(String[] tired){
        int a=7;
        System.out.println(a>>3); //7/2/2/2=0 (向下取整)
    }
}
```
output:
```
0
```

**6. <<:本质等于乘以n个2**

input:
```
class bitewise{
    public static void main(String[] tired){
        int a=7;
        System.out.println(a<<3); //7*2*2*2=56 
    }
}
```
output:
```
56
```

**7.>>>:无符号右移，低位溢出，高位补0(用的比较少)**

input:
```
class bitewise{
    public static void main(String[] tired){
        int a=-128;
        System.out.println(a>>4);
        System.out.println(a>>>4);
    }
}
```
output:
```
-8
268435448
```

## 09/15/22
### Control Structure
#### if-else(curl brackets for if-else should be applied to show clear structure. If there is only one operation commanding, it could be omitted)
input:
```
import java.util.Scanner;
class stupid{
    public static void main(String[] args){
      Scanner input = new Scanner(System.in);
      System.out.println("input your age");
      int age = input.nextInt();
      if(age>=18){
          System.out.println("You are liable");
      }
      else
      {
          System.out.println("You are free of being charged");
      }
    }
}
```
output:
```
input your age
69
You are liable
```

#### if-else if-....-else(else could be non-existed)
input:
```
import java.util.Scanner;
class stupid{
    public static void main(String[] args){
      Scanner input = new Scanner(System.in);
      System.out.println("input your age");
      int age = input.nextInt();
      if(age>=65){
          System.out.println("You are free");
      }
      else if(age<=65&&age>=18)
      {
          System.out.println("You are dead meat");
      }
      else System.out.println("Anyway, you are so young");
    }
}
```
output:
```
input your age
4
Anyway, you are so young
```

#### nested if-else structure
input:
```
import java.util.Scanner;
class stupid{
    public static void main(String[] args){
      Scanner myScanner = new Scanner (System.in);
      System.out.println("Contestor's score");
      Double score = myScanner.nextDouble();
        if(score>8.0){
            System.out.println("Contestor's gender");
            String gender = myScanner.next();
            if(gender.equals("male")){                    //index.equals("") 用于判断字符串
                System.out.println("In men group");
            }else if(gender.equals("female")){
                System.out.println("In women group");
            }
            else System.out.println("please enter male or female");
        }else System.out.println("you are out");
    }
}
```
output:
```
Contestor's score
9
Contestor's gender
female 
In women group
```
**判断字符串：index.equals("")**

input:
```
class wonderland{
    public static void main(String[] argy){
        boolean c= ("comeon").equals("love");
        System.out.println(c);
    }
}
```
output:
```
false
```

**multiple nested structure**

input:
```
import  java.util.Scanner;
class nested{
    public static void main(String[] never){
        Scanner myscanner = new Scanner(System.in);              //for each class, Scanner only have to be declared once
        System.out.println("enter the month");
        int month = myscanner.nextInt();
        if(month>=4 && month<=10){
            System.out.println("enter age");
            int age = myscanner.nextInt();                       // here, the age is local variable, can be re-declared later. 
            if(age<18){
                System.out.println("half price");
            }
            else if(age>=18 && age<=60){
                System.out.println("60");
            }
            else if(age>60){
                System.out.println("1/3");
            }
        }else if((month>=1&& month<4) || (month>10 && month<=12 )){
            System.out.println("age");
            int age = myscanner.nextInt();                       //here, age is declared again as another local variable
            if(age>=18 && age<=60){
                System.out.println("40");
            }else System.out.println("20");;
        }
    }
}
```
output:
```
enter the month
2
age
56
40
```

#### switch structure
**1. example to show how switch works**

input:
```
import  java.util.Scanner;
class learntouseswitch{
    public static void main(String[] no){
        Scanner lookfor = new Scanner(System.in);
        System.out.println("enter a char");
        char c1= lookfor.next().charAt(0);                 //declare the variable which is a char in Scanner
        switch(c1){                                        //c1 is the one you wanna test with switch
            case 'a':System.out.println("this is a");      //testd by case, (notice there is ":")
            break;                                         //break helps to jump out of structure when getting desired results, 
	                                                     if no break, then another print will be processsed 
	                                                     each case can have more than one operation, with semi-colon to separate 
            case 'b':System.out.println("this is b");
            break;
            default:
                System.out.println("anyway, I got the char");  //default helpes to set default result and break the structure
        }
    }
}
```
output:
```
enter a char
a
this is a
```

**2. Another example**

input:
```
class learntouseswitch{
    public static void main(String[] no){
        Scanner lookfor = new Scanner(System.in);
        System.out.println("enter your name");
        String name= lookfor.next();
        switch(name){
            case "tom":System.out.println("this is a lame name");
            break;
            case "jeremy":System.out.println("this is a bastard");
            break;
            case "Nick":System.out.println("he is doomed to success");
                break;
            default:
                System.out.println("Anyway, life has to move forward and move on");
        }
    }
}

```
output:
```
enter your name
Nick 
he is doomed to success
```

**3.in switch, we can only use (byte, short, int, char, enumerate and string)**

input:
```
class whatsup{
    public static void main(String[] layback){
        int a = 3;                                        //double is forbidden in switch, int is allowed
        switch(a){
            case 1:                                       //case condition should be a constant, can not be a variable 
	    System.out.println("yes it is what it is");
            default:                                      // default is also optional
                System.out.println("not at all");
        }
    }
}
```
output:
```
not at all
```

**4.break in switch is important**

input:
```
import java.util.Scanner;
class breakyou{
    public static void main(String[] args){
        Scanner iamback = new Scanner(System.in);
        System.out.println("lets choose a new number");
        int number=iamback.nextInt();
        switch(number){
            case 1:System.out.println("monday");
            case 2:System.out.println("tuesday");
            case 3:System.out.println("wednesday");                      // since there is no break, the switch will start from case 3, and print all 
	                                                                    operations after that. (if we input number 1, then starts from "monday" to
									    "aftermath") 
            case 4:System.out.println("thursday");
            default:System.out.println("aftermath");
        }
        }
}
```
output:
```
lets choose a new number
3
wednesday
thursday
aftermath
```








































































































































