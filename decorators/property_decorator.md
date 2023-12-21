1. **Decorator on Class Property:**

   - Illustrates adding a decorator, named `log`, to a property within a class. The decorator function takes two arguments: `target` (prototype of the object or constructor function for static properties) and `property name`. In this example, it logs information about the property and its prototype.

     ```typescript
     class Product {
       @log
       title: string;

       constructor(title: string) {
         this.title = title;
       }

       // ... other class methods
     }
     ```

2. **Decorator Execution Timing:**

   - Emphasizes that property decorators execute when the class definition is registered by JavaScript. The `log` decorator, in this case, runs when the property is defined as part of the class. Since there is no instantiation of the `Product` class, the decorator executes during class definition.

3. **Decorator Output:**

   - Shows the console output of the `log` decorator, indicating the `target` (prototype of the object) and `property name` ("title"). Demonstrates that methods are registered on the prototype, and the decorator executes during class definition.

4. **Decorator on Method:**

   - Extends the use of decorators to class methods. Adds a `log` decorator to the `getPriceWithTax` method, showcasing that decorators can be applied to both properties and methods within a class.

     ```typescript
     class Product {
       @log
       title: string;

       @log
       getPriceWithTax(taxRate: number): number {
         // Method implementation
       }

       // ... other class methods
     }
     ```

5. **Understanding Decorator Arguments:**
   - Clarifies that the arguments received by a decorator function depend on where it is applied. For properties, the decorator gets `target` and `property name`. This flexibility highlights how decorators can be adapted to different use cases within a class, providing a powerful tool for metaprogramming.
