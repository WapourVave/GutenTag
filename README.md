## GutenTag
GutenTag is a complex - yet underpowered and unusable - interpretted text parsing programming language!
Some methods are excluded from the built-in libraries, and additional methods can be defined that utilize the parser environment veriables, as well as the method's output.

## Simple Example
```java
import com.jagrosh.gutentag.*;
public class Example
{
  public static void main(String[] args)
  {
    Parser parser = GutenTag.newDefaultBuilder()
                .addMethod( new Method("exclaim", (env,in) -> in[0]+"!!!") )
                .build();
    String result = parser.parse("{exclaim:{if:this|=|that|then:Foo Bar|else:Hello World}}");
    System.out.println(result);
  }
}
```
Result: `Hello World!!!`

## Maven
To use Maven with GutenTag, simply add the following sections to your pom.xml
```xml
  <repository>
    <id>central</id>
    <name>bintray</name>
    <url>http://jcenter.bintray.com</url>
  </repository>
```
```xml
  <dependency>
    <groupId>com.jagrosh</groupId>
    <artifactId>GutenTag</artifactId>
    <version>0.5</version>
  </dependency>
```

## Current Projects
Here are some other projects that utilize GutenTag:
* [**Mee6 (Discord Bot)**](https://mee6.xyz/) - Mee6 uses GutenTag in its customizable "welcome" message (user-created greeting), and in leave message for server's.

## Other Libraries
Below are GutenTag-related libraries available for other languages or purposes:
* [**pat/gutentag**](https://github.com/pat/gutentag) - A good, simple, solid tagging extension for ActiveRecord.
* [**arrdem/guten-tag**](https://github.com/arrdem/guten-taarrdem/) - Good tags for a good day!
