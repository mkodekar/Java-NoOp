Java - NoOp
===========
This is probably one of the simplest Java annotation processing libraries out there.

It generates [no-op implementations](https://en.wikipedia.org/wiki/NOP) of your interfaces. 

Usage
-----
* Simply annotate your interface with `@NoOp` like this:

```java
@NoOp
public interface TestInterface {

    byte aByte();

    short aShort();

    int anInt();

    long aLong();

    float aFloat();

    double aDouble();

    char aChar();

    boolean aBoolean();
    
    String aString();

    void aVoid();
}
```

* And it will generate the following no-op implementation at compile time:

```java
public class NoOpTestInterface implements TestInterface {

  @Override
  public byte aByte() {
    return (byte) 0;
  }

  @Override
  public short aShort() {
    return (short) 0;
  }

  @Override
  public int anInt() {
    return 0;
  }

  @Override
  public long aLong() {
    return 0L;
  }

  @Override
  public float aFloat() {
    return 0.0F;
  }

  @Override
  public double aDouble() {
    return 0.0D;
  }

  @Override
  public char aChar() {
    return ' ';
  }

  @Override
  public boolean aBoolean() {
    return false;
  }
  
  @Override
  public String aString() {
    return null;
  }

  @Override
  public void aVoid() {
  }
}
```

Download
--------

*- coming soon -*

License
-------
This project is licensed under the [MIT License](https://raw.githubusercontent.com/jenzz/Java-NoOp/master/LICENSE).