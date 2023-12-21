1. **Accessor Decorator Example:**

   - Introduces the ability to add decorators to accessors (getter/setter) within a class. Creates a new decorator function `log2` that receives three arguments: `target` (prototype or constructor function), `property name` (name of the accessor), and `property descriptor` (with information like whether it has a setter and getter).

     ```typescript
     class Product {
       @log2
       set price(value: number) {
         // Setter implementation
       }

       // ... other class properties and methods
     }
     ```

2. **Method Decorator Example:**

   - Demonstrates the use of decorators on methods within a class. Adds a `log3` decorator to the `getPriceWithTax` method, showcasing that method decorators receive the same three arguments as accessor decorators: `target`, `method name`, and `property descriptor`.

     ```typescript
     class Product {
       @log3
       getPriceWithTax(taxRate: number): number {
         // Method implementation
       }

       // ... other class properties and methods
     }
     ```

3. **Parameter Decorator Example:**

   - Introduces the ability to add decorators to method parameters. Defines a new decorator function `log4` and applies it to the `tax` parameter within the `getPriceWithTax` method. Parameter decorators receive three arguments: `target` (prototype or constructor function), `method name`, and `parameter index`.

     ```typescript
     class Product {
       getPriceWithTax(@log4 taxRate: number): number {
         // Method implementation
       }

       // ... other class properties and methods
     }
     ```

4. **Decorator Execution Order:**

   - Highlights that decorators can be applied to various parts of a class, including properties, accessors, methods, and parameters. Shows the execution order of decorators, emphasizing that they execute bottom-up, meaning decorators at lower levels are executed first, followed by decorators at higher levels.

5. **Decorator Output:**
   - Illustrates the console output of the decorator functions (`log2`, `log3`, `log4`) when applied to different parts of the class. The output includes information such as the `target` (prototype or constructor), `property name`, `property descriptor` for accessors and methods, and `parameter index` for parameter decorators.
