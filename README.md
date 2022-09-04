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





































































































































