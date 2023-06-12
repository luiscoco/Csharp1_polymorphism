# Csharp1_polymorphism

In C#, polymorphism refers to the ability of an object to take on many forms or types. It allows objects of different classes to be treated as objects of a common base class during runtime.

Polymorphism is achieved through two main mechanisms: inheritance and method overriding. Let's explore each of these in more detail:

Inheritance: In C#, you can define a class that inherits from another class, also known as the base class or parent class. The derived class can inherit the properties, methods, and behaviors of the base class. Polymorphism comes into play when you have a reference variable of the base class type that is actually referring to an object of the derived class.
Here's an example:

```csharp
class Animal
{
    public virtual void MakeSound()
    {
        Console.WriteLine("The animal makes a sound.");
    }
}

class Dog : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The dog barks.");
    }
}

class Cat : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The cat meows.");
    }
}

// Usage:
Animal animal1 = new Dog();
Animal animal2 = new Cat();

animal1.MakeSound(); // Output: "The dog barks."
animal2.MakeSound(); // Output: "The cat meows."
```

In the example above, both the Dog and Cat classes inherit from the Animal base class. The MakeSound method is overridden in each derived class to provide a specific implementation. When we create objects of the derived classes and assign them to variables of the base class type, we can call the MakeSound method on these variables, and the appropriate implementation based on the actual object type will be executed.

Method Overriding: In the previous example, the MakeSound method in the base class is marked as virtual, and the corresponding methods in the derived classes are marked as override. This combination enables method overriding, which allows a derived class to provide its own implementation of a method that is already defined in the base class.
By using method overriding, you can invoke a method on a base class reference variable, but the overridden method in the derived class will be called at runtime. This is another form of polymorphism.

It's important to note that polymorphism relies on the base class reference variable to access the overridden method in the derived class. If the method is not overridden, the base class's implementation will be executed.

Polymorphism is a fundamental concept in object-oriented programming that promotes code reusability, flexibility, and extensibility. It allows you to write more generic and flexible code that can work with objects of different types, as long as they share a common base class or interface.

