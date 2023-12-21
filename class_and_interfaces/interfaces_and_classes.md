1. **Interface vs Custom Type:**

   - Interfaces and custom types are similar but have differences.
   - Both can describe object structures, but custom types offer more flexibility, allowing union types and more.
   - Interfaces are clearer in intent, specifically designed for defining object structures.

     ```typescript
     // Using Interface
     interface Person {
       name: string;
       age: number;
     }

     // Using Custom Type
     type Person = {
       name: string;
       age: number;
     };
     ```

2. **Interface as a Contract:**

   - Interfaces can serve as contracts that classes implement.
   - Example: Creating a `Greetable` interface with `name` and `greet` method, which a class must adhere to if it implements the interface.

     ```typescript
     interface Greetable {
       name: string;
       greet(phrase: string): void;
     }
     ```

3. **Implementing an Interface:**

   - Classes can implement interfaces using the `implements` keyword.
   - The class must follow the structure defined by the interface.
   - Example: Implementing the `Greetable` interface in a `Person` class.

     ```typescript
     class Person implements Greetable {
       constructor(public name: string) {}
       greet(phrase: string) {
         console.log(phrase + " " + this.name);
       }
     }
     ```

4. **Using Interface as a Type:**

   - Interfaces can be used as types for variables or constants.
   - Example: Using `Greetable` as a type for the `user1` variable, allowing it to store a `Person` object.

     ```typescript
     let user1: Greetable = new Person("Max");
     console.log(user1); // Outputs: { name: "Max" }
     ```
