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

#### Sizes of primitive Data/Variables(in byte)
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



























































































































































