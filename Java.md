# Java Standard Edition

###### JDK 11

## Working with Java data types



## Controlling Program Flow



## Java Object-Oriented Approach

### Immutable Class

- The class should be marked as `final` to suppress extensibility (other classes cannot extend this class; therefore, they cannot override methods)
- All fields should be declared `private` and `final` (they are not visible in other classes, and they are initialized only once in the constructor of this class)
- The class should contain a parameterized `public` constructor (or a `private` constructor and factory methods for creating instances) that initializes the fields
- The class should provide getters for fields
- The class should not expose setters

### Cloning

The `Object` class contains a method named `clone()`. This method is useful for creating shallow copies. In order to use it, a class should follow the given steps:

- Implement the `Cloneable` interface (if this interface is not implemented, then `CloneNotSupportedException` will be thrown).
- Override the `clone()` method (`Object.clone()` is `protected`).
- Call `super.clone()`.

>  `Object.clone()` doesn't rely on a constructor invocation, and so the developer cannot control the object construction.

### General contract associated with `equals()` method

For any non-null reference variables a, b and c

- `a.equals(a)` should always return `true`.
- `a.equals(b)` should return `true` if and only if `b.equals(a)` returns `true`.
- If `a.equals(b)` returns `true` and `b.equals(c)` returns `true` then `a.equals(c)` should return `true`.
- Multiple calling of `a.equals(b)` should consistently return `true` or consistently return `false` If the value of the object is not modified for either object.
- `a.equals(null)` should return `false`.



### General contract associated with `hashCode()` method

- The `hashCode()`method should return the same integer value for the same object for each calling of this method unless the value stored in the object is modified.
- If two objects are equal(according to `equals()` method) then the `hashCode()` method should return the same integer value for both the objects.
- But, it is not necessary that the `hashCode()` method will return the distinct result for the objects that are not equal (according to `equals()` method).

## Exception Handling



## Working with Arrays and Collections



## Working with Streams and Lambda expressions



## Java Platform Module System



## Concurrency



## Java I/O API



## Secure Coding in Java SE Application

### Designing Secure Object

#### Limiting accessibility

- Make the object `private` and write a method to provide the necessary functionality.

- Export the security packages to the specific modules that should have access.

  ```java
  exports animals.security to zoo.staff;
  ```

#### Restricting Extensibility

Make sensitive class as `final` prevents any subclasses.

#### Creating immutable objects

- Mark the class as `final`.
- Mark all the instance variables `private`.
- Don't define any setter methods and make fields final.
- Don't allow referenced mutable objects to be modified.
- Use a constructor to set all properties of the object, making a copy if needed.

#### Cloning objects

Implement `Cloneable` interface if you want classes to be able to call the `clone()`method on your object.

> *Defensive copy* is the copy being made in case other code does something unexpected.

#### Introducing Injection and Input Validation

> *Injection* is an attack where dangerous input runs in a program as part of a command.

> An *exploit* is an attack that takes advantage of weak security. 

## Database Applications with JDBC



## Localization



## Annotations



## Network

The default settings for `java.net.http.HttpClient` are as follows:

- HTTP/2
- No authenticator
- No connection timeout
- No cookie handler
- Default thread pool executor
- Redirection policy of NEVER
- Default proxy selector
- Default SSL context

## Notes

### String

#### Counting duplicate characters

```java
public Map<String, Long> countDuplicateCharacters(String str) {
  return str.codePoints()
      .mapToObj(c -> String.valueOf(Character.toChars(c)))
      .collect(Collectors.groupingBy(c -> c, Collectors.counting()));
}
```

#### Finding the first non-repeated character

```java
public String firstNonRepeatedCharacter(String str) {
  LinkedHashMap<Integer, Long> chs =
      str.codePoints()
          .boxed()
          .collect(
              Collectors.groupingBy(
                  Function.identity(), LinkedHashMap::new, Collectors.counting()));

  int codePoint =
      chs.entrySet().stream()
          .filter(e -> e.getValue() == 1L)
          .findFirst()
          .map(Map.Entry::getKey)
          .orElse((int) Character.MIN_VALUE);

  return String.valueOf(Character.toChars(codePoint));
}
```

#### Reversing letters and words

```java
private static final Pattern PATTERN = Pattern.compile(" +");

public String reverseWords(String str) {
  return PATTERN
      .splitAsStream(str)
      .map(w -> new StringBuilder(w).reverse())
      .collect(Collectors.joining(" "));
}
```

#### Counting vowels and consonants

```java
private static final Set<Character> VOWELS =
    new HashSet<>(Arrays.asList('a', 'e', 'i', 'o', 'u'));

public Pair<Long, Long> countVowelAndConsonants(String str) {
  Map<Boolean, Long> result =
      str.toLowerCase()
          .chars()
          .mapToObj(ch -> (char) ch)
          .filter(ch -> (ch >= 'a' && ch <= 'z'))
          .collect(Collectors.partitioningBy(ch -> VOWELS.contains(ch), Collectors.counting()));

  return Pair.of(result.get(true), result.get(false));
}
```

#### Joining multiple strings with a delimiter

```java
public String joinBy(char delimiter, String... args) {
  return Arrays.stream(args, 0, args.length)
      .collect(Collectors.joining(String.valueOf(delimiter)));
}
```

#### Generating all permutations

```java
  public void permutation(String prefix, String str) {
    int n = str.length();

    if (n == 0) {
      System.out.print(prefix + " ");
    } else {
      IntStream.range(0, n)
       // .parallel()
          .forEach(
              i ->
                  permutation(
                      prefix + str.charAt(i), str.substring(i + 1, n) + str.substring(0, i)));
    }
  }
```

#### Finding the character with the most appearances

```java
public Pair<Character, Long> maxOccurrenceCharacter(String str) {
  return str
      .toLowerCase()
      .codePoints()
      .filter(cp -> !Character.isWhitespace(cp))
      .mapToObj(ch -> (char) ch)
      .collect(Collectors.groupingBy(c -> c, Collectors.counting()))
      .entrySet()
      .stream()
      .max(comparingByValue())
      .map(p -> Pair.of(p.getKey(), p.getValue()))
      .orElse(Pair.of(Character.MIN_VALUE, -1L));
}
```

### Object

#### null references

```java
Objects.isNull(object);
Objects.nonNull(object);
Objects.requireNonNull(object, message);
Objects.requireNonNullElse(object, defaultValue);
Objects.requireNonNullElseGet(object, () -> defaultValue);
```

#### index

```java
Objects.checkIndex(n, N_UPPER_BOUND);
Objects.checkFromIndexSize(n, size, N_UPPER_BOUND);
Objects.checkFromToIndex(n, N_LOWER_BOUND, N_UPPER_BOUND);
```

