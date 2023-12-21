1. **Interface for Function Types:**

   - Interfaces can define the structure of functions, serving as an alternative to custom function types.
   - Function types define the parameters and return type of a function.
   - Example: Creating a function type `AddFn` using an interface.

     ```typescript
     interface AddFn {
       (a: number, b: number): number;
     }
     ```

2. **Anonymous Function in Interface:**

   - In the interface, use an anonymous function syntax to specify the function type.
   - Arguments and return type are defined within the parentheses and after the colon, respectively.
   - Example: Defining an `AddFn` interface with an anonymous function.

     ```typescript
     interface AddFn {
       (a: number, b: number): number;
     }
     ```

3. **Using Interface for Function:**

   - Use the interface `AddFn` to type-check functions.
   - Assign the function type to a variable or constant.
   - Example: Assigning an actual function to a variable with the `AddFn` interface.

     ```typescript
     const addFunction: AddFn = (a, b) => a + b;
     ```

4. **Alternative to Custom Types:**

   - While custom function types with `type` are common, interfaces offer an alternative syntax.
   - The interface syntax is useful to understand, especially when encountered in projects.
   - Example: Comparing the interface and custom type syntax for function types.

     ```typescript
     // Using Interface
     interface AddFn {
       (a: number, b: number): number;
     }

     // Using Custom Type
     type AddFn = (a: number, b: number) => number;
     ```
