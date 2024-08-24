# Programming in Java

# Week 5 

# Programming Assignment 1

```bash
// write a function to check an integer as a parameter and throws an exception if the number is odd
public static void trynumber(int n){
  try {
      checkEvenNumber(n);
    } catch (IllegalArgumentException e) {
      System.out.print(e.getMessage());
    }
}
 
 
public static void checkEvenNumber(int number) throws IllegalArgumentException {
  if ( number % 2 == 1)
    throw new IllegalArgumentException("Error: " + number + " is odd.");
  else
    System.out.print(number + " is even.");
}
```

# Programming Assignment 2

```bash
// Declare the Document class and WebPage class, which implements the Searchable interface
class Document implements Searchable{
  public boolean search(String keyword){
    return true; // dummy statement
  }
}
 
class WebPage implements Searchable{
  
  String url;
  String title;
  
  WebPage(String url, String title){
    this.url = url;
    this.title = title;
  }
  public boolean search(String keyword){
    return title.contains(keyword);
  }
}
```

# Programming Assignment 3

```bash
// create a method that takes a string as input and throws an exception if the string does not contain vowels.
public static void checkVowels(String a) throws NoVowelsException {
  boolean flag = false;
  for ( int i = 0 ; i < a.length() ; i++){
        char c = a.charAt(i);
        if ( c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u' || 
            c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U')
          flag = true;
      }
  if ( flag == false )
    throw new NoVowelsException("String does not contain any vowels.");
}
```

# Programming Assignment 4

```bash
// Declare the Spacecraft class, Airplane class, Helicopter class which implements the Flyable interface
// Implement the "fly_obj" method required by the Flyable interface
class Spacecraft implements Flyable{
  public void fly_obj(){
    System.out.println("Spacecraft is flying");
  }
}
class Airplane implements Flyable{
  public void fly_obj(){
    System.out.println("Airplane is flying");
  }
}
class Helicopter implements Flyable{
  public void fly_obj(){
    System.out.println("Helicopter is flying");
  }
}
```

# Programming Assignment 5

```bash
// Declare the Volleyball, Basketball, Football class, which implements the Playable interface
class Volleyball implements Playable{
  public void play(){
    System.out.println("Playing volleyball");
  }
}
class Basketball implements Playable{
  public void play(){
    System.out.println("Playing basketball");
  }
}
class Football implements Playable{
  public void play(){
    System.out.println("Playing football");
  }
}
```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)