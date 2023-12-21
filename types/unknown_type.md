- **Introduction to the Unknown Type:**

  - The `unknown` type in TypeScript is introduced for scenarios where the type of a variable is not known in advance.
  - Unlike `any`, which is the most flexible type allowing any value, `unknown` imposes some type checking restrictions.

- **Usage of Unknown Type:**

  - The `unknown` type is useful when the specific type of a variable is uncertain, but you want to impose type checks before performing certain operations.

- **Example Scenario:**

  - In the `app.ts` file, a variable named `userInput` is declared with the type `unknown`.
    ```typescript
    let userInput: unknown;
    ```

- **Assigning Values to Unknown Type:**

  - Any value can be assigned to a variable of type `unknown` without causing compilation errors.
    ```typescript
    userInput = 5; // No error
    userInput = "Hello"; // No error
    ```

- **Difference from Any Type:**

  - Unlike `any`, attempting to assign an `unknown` value to a variable with a specific type will result in a compilation error.
    ```typescript
    let userName: string;
    userName = userInput; // Error: Type 'unknown' is not assignable to type 'string'.
    ```

- **Type Check with Unknown Type:**

  - To use a value of type `unknown` in a context that expects a specific type, a type check is required.
    ```typescript
    if (typeof userInput === "string") {
      userName = userInput; // Type check allows assigning 'unknown' to 'string'.
    }
    ```

- **Advantages of Unknown over Any:**

  - The `unknown` type is more restrictive than `any`, requiring type checks before certain operations.
  - Provides a level of type safety by ensuring that the type is checked before performing actions specific to that type.

- **Best Practices:**

  - Use `unknown` when the type is not precisely known, but you want to enforce type checks before using the value.
  - Consider using more specific types or union types if the potential types of a variable can be defined.

- **Note:**

  - While `unknown` provides more type safety than `any`, it is preferable to use more precise types when possible.

- **Conclusion:**
  - The `unknown` type offers a middle ground between flexibility and type safety in situations where the type of a variable is uncertain. By introducing type checks, developers can safely use values of the `unknown` type in a controlled manner. While not suitable for all scenarios, `unknown` provides a balance between flexibility and type control in TypeScript.
