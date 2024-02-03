# Design-Oriented Programming (DOP)

Design-Oriented Programming (DOP) introduces a new paradigm that prioritizes the design and construction of programs using building blocks called blocks or bricks. In this article, we will delve into the specifics of Design-Oriented Programming and distinguish it from other programming paradigms.

Understanding Programming Paradigms
Before exploring Design-Oriented Programming, it is essential to grasp the concept of programming paradigms. A programming paradigm comprises a set of ideas and concepts that define the style of writing computer programs. It establishes an approach to programming that governs the organization and structure of a program.

Programming paradigms include Imperative programming, Declarative programming, and Object-Oriented programming.

# Imperative Programming
Imperative programming involves writing instructions (commands) directly into a program's source code. These instructions must be followed sequentially, and subsequent instructions can access data from previous instructions stored in memory. It adopts a step-by-step, sequential approach to programming.

# Declarative Programming
In contrast to imperative programming, declarative programming focuses on specifying the problem's solution rather than the step-by-step process to obtain it. Declarative languages such as HTML and SQL enable programmers to describe the desired result without providing detailed steps.

# Object-Oriented Programming (OOP)
Object-Oriented Programming is a widely adopted programming paradigm that revolves around objects encapsulating both data (fields) and code (procedures). Objects can be organized into classes, serving as blueprints for creating object instances. OOP facilitates encapsulation, inheritance, and polymorphism, promoting modular and reusable code.

# Design-Oriented Programming (DOP)
Introducing Design-Oriented Programming (DOP)
Design-Oriented Programming approaches programming differently compared to the mentioned paradigms. DOP focuses on constructing programs using building blocks or blocks. These blocks serve as program constructors and can be directly written into the source code.
The key aspects of Design-Oriented Programming are:

- Blocks are implemented in the program's source code.
- Blocks can be utilized to construct classes, functions, or entire programs.
- Blocks can contain other blocks, establishing a hierarchical structure.
- Blocks can be components of various structures like methods and loops.

In Design-Oriented Programming (DOP), a block is a building block or brick that serves as a program constructor. Blocks are implemented directly in the program's source code and can be utilized to construct classes, functions, or even entire programs. They can contain other blocks, establishing a hierarchical structure. Blocks can be components of various structures like methods and loops.

The roots of DOP can be traced back to the AsmX programming language. Let's explore an AsmX example to grasp the working of DOP:
```
@using method setType;
@using method getType;

@constructor __create__(self):
    @call print('Created animal');

@class Animal:
    @bind constructor  __create__;
    @bind method setType;

    @method setType(type):
        self.type type;

@class Dog extends Animal:
    @bind constructor  __create__;
    @bind method getType;

    @method getType():
        @call print(self.type)

@create class Dog dog; # Created Animal
@call class::dog();

@create class Dog siba; # Created Animal
@call class::siba();

@call dog->setType('Dog');
@call dog->getType(); # Dog

@call siba->setType('Siba Inu');
@call siba->getType(); # Siba Inu
```

In this example, methods are treated as blocks or bricks that can be bound within a class. Constructors, destructors, blocks, and classes themselves are all employed in DOP.

The Fundamental Principle of DOP
At the heart of Design-Oriented Programming lies the idea of constructing programs using building blocks. These blocks serve as the fundamental units of the program and can be combined and interconnected to create complex computational structures.

The specificity of DOP lies in its emphasis on program design and construction. Instead of solely focusing on the sequence of steps or the desired result, DOP encourages programmers to think in terms of building blocks and their connections. This approach promotes modularity, reusability, and a clear design hierarchy.

Specializing with DOP
Design-Oriented Programming enables specialization in various domains and problem spaces. Programmers can tailor the construction of programs to specific requirements and constraints by utilizing different blocks and organizing them differently.

Whether it involves building a todo list application or implementing a loop, DOP offers the flexibility and modularity necessary for creating specialized solutions. Let's see an example of a todo list and a loop in DOP:
```
# Define the first task
@task first:
    @call print('task 1');

# Define the second task
@task second:
    @call print('task 2');
    @set three i8 255;

# Define the third task
@task three:
    @call print('task 3');
    @call print(set::three);

# Define the First todolist
@todolist First:
    @bind task first;
    @bind task second;
    @bind task first;

# Define the Second todolist
@todolist Second:
    @bind task second;
    @bind task first;
    @bind task second;
    @bind task first;
    @bind task three;

# Create an instance of the First todolist with the first task
@create todolist First first;

# Run the first task in the First todolist
@call todolist::first::run(); # task 1
@call todolist::first::run(); # task 2

# View the contents of the First todolist
@call todolist::first::view();

# Create an instance of the Second todolist with the second task
@create todolist Second second;

# View the contents of the Second todolist
@call todolist::second::view();

# Run the tasks in the Second todolist in serial order
@call todolist::second::runSerial();

# View the contents of the Second todolist
@call todolist::second::view();
```

Loop example:
```
# Block for loop
@for name:
    @call print('text');

@execute for name 0x03;  # Execute the for loop 3 times
```

These examples illustrate how blocks can be employed in DOP to create specialized functionality and construct programs to meet specific requirements.

# Design-Oriented Programming (DOP) VS Object-Oriented Programming (OOP)
Design-Oriented Programming (DOP) is a programming paradigm that focuses on the design and construction of programs using building blocks called blocks or bricks. These blocks are implemented directly in the source code and can be used to construct classes, functions, or even entire programs. Blocks can also contain other blocks, establishing a hierarchical structure. DOP encourages programmers to think in terms of building blocks and their connections, promoting modularity, reusability, and a clear design hierarchy.

On the other hand, Object-Oriented Programming (OOP) is another widely adopted programming paradigm that revolves around objects encapsulating both data and code. Objects are organized into classes, serving as blueprints for creating object instances. OOP facilitates encapsulation, inheritance, and polymorphism, promoting modular and reusable code.

The main difference between DOP and OOP lies in their approach to programming. DOP prioritizes the design and construction of programs using building blocks, while OOP focuses on objects and their interaction. DOP views a program as a collection of interconnected blocks, creating complex computational structures. In contrast, OOP views a program as a collection of objects, with each object having its own data and behavior.

DOP is not OOP because it does not involve the use of objects and their interaction. Instead, DOP uses blocks as the fundamental units of a program, which can be combined and interconnected to create complex structures. While OOP promotes modularity and reusability through encapsulation and inheritance, DOP achieves these goals through the design and construction of programs using building blocks.

In conclusion, DOP and OOP are two distinct programming paradigms. DOP prioritizes the design and construction of programs using building blocks, while OOP revolves around objects encapsulating both data and code. Understanding the differences between these paradigms is essential for programmers to choose the most appropriate approach for their specific programming requirements.

# The difference between DOP and OOP
Unlike traditional class-based object-oriented programming, blocks in DOP do not encapsulate both data and code like objects do. Instead, blocks focus on the construction of programs and their design. They serve as fundamental units of the program and can be combined and interconnected to create complex computational structures. Blocks in DOP promote modularity, reusability, and a clear design hierarchy.

In summary, blocks in DOP are program constructors that can be implemented directly in the program's source code. They serve as fundamental units and can be combined and interconnected to create complex structures. Unlike objects in object-oriented programming, blocks in DOP do not encapsulate both data and code. Instead, they focus on the design and construction of programs.

# Conclusion
Design-Oriented Programming represents a unique paradigm that emphasizes the design and construction of programs using building blocks. By utilizing blocks as program constructors, DOP promotes modularity, reusability, and clear design hierarchies.

Originating from the AsmX programming language, DOP offers a flexible and specialized approach to programming. Whether constructing todo lists, implementing loops, or solving complex problems, DOP presents a fresh perspective on program development.

Incorporating Design-Oriented Programming principles into your development toolkit can expand your programming abilities and empower you to create well-designed, modular, and adaptable programs. Embrace the power of DOP and unlock new possibilities on your programming journey.
