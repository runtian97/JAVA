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
### 




























































