```Java

public class HelloWorld {
    public static void say(String message) {
        System.out.println(message);
    }

    public static void sayToPerson(String message, String name) {
        System.out.println(name + ", " + message);
    }
}


public aspect MannersAspect {
    pointcut callSayMessage() : call(public static void HelloWorld.say*(..));
    before() : callSayMessage() {
        System.out.println("Good day!");
    }
    after() : callSayMessage() {
        System.out.println("Thank you!");
    }
}

```

```C#

using System;

class Hello
{
    static void Main()
    {
        Console.WriteLine("Hello, World");
    }
}

```

```C++

#include <iostream>
using namespace std;

int main() 
{
    cout << "Hello, World!";
    return 0;
}
```


```php

<?php
	echo 'Hello, World!';
?>

```

```python
print('Hello, world!')
```

```javascript
  <script>
    alert( 'Hello, world!' );
  </script>

 ```

```ruby
puts 'Hello, world!'

```