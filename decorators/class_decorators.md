1. **Setting up TypeScript Configuration:**

   - In the provided starting project, ensures that the `tsconfig.json` file has the target set to `es6` and includes the experimental decorators configuration.

     ```json
     {
       "compilerOptions": {
         "target": "es6",
         "experimentalDecorators": true
       }
     }
     ```

2. **Introduction to Decorators:**

   - Explains the role of decorators in TypeScript, highlighting that decorators are functions applied to classes, enhancing or modifying their behavior.

3. **Example Class with Decorator:**

   - Illustrates a basic class named `Person` with a decorator called `Logger` applied to it. The decorator is a function prefixed with the `@` symbol, and it logs a message.

     ```typescript
     @Logger
     class Person {
       name = "Max";

       constructor() {
         console.log("Creating person object");
       }
     }
     ```

4. **Decorator Implementation:**

   - Defines the `Logger` decorator function, emphasizing that decorators receive one argument, the constructor function of the class to which the decorator is applied.

     ```typescript
     function Logger(constructor: Function) {
       console.log("Logging");
       console.log(constructor);
     }
     ```

5. **Decorator Execution Timing:**
   - Emphasizes that decorators execute when the class is defined, not when an object is instantiated. Shows that the decorator logs its output before the class constructor logs its message, reinforcing the timing of decorator execution.

Understanding the decorator syntax, implementation, and execution timing provides a foundation for using decorators to enhance and customize class behavior in TypeScript.
