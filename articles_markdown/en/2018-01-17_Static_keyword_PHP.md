## static keyword in PHP ##

Recently I stumbled upon the **static** keyword in way that I had forgotten existed so I'm doing a post on what can be done with it to keep a reference for later use.

### In a class ###

The **static** keyword can be used inside a class either on class members like this:

    class TestStatic
	{
	    static public staticVariable = 42;
	}

Then to access it, you can write:

    // First method
    $class = new TestStatic();
	echo $class::$staticVariable;
	
	// Second method
	echo TestStatic::$staticVariable;
	
Here we see clearly that **static** is used to create a member of the class, and not a member of an instance. It's a value that all instances of the class **TestStatic** will share.


Another use in classes is to apply the **static** keyword to a method, to make it also a method of the class, and not a method of instances of the class.

    class Math
	{
	    static public function square($x)
		{
		    return $x*$x;
		}
	}
	
Here you see the implementation of **square** does not depend on the internals of the class it is being defined in, so we can define it **static** to use it without instantiating the class.
It's a behavior often observed with the **Math** class, because all the function inside it are working with just their respective parameters. They are independant to the internal states of an instance.

To use it you would do:

    echo Math::square(3);
	//print 9

