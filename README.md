# JAVA
## 08/23/22 
### JAVA Escape Character:
**1. \t: Insert a tab in the text at this point.**

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
output:// clearly
```
japanlebron
```

























