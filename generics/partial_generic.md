1. **Introduction to Built-in Utility Types:**

   - Highlights the existence of built-in utility types in TypeScript, offering utility functionalities through generics to enhance type safety and flexibility.

2. **Example of Partial Type:**

   - Introduces the `partial` type, demonstrating its application in creating a function (`createCourseGoal`) that incrementally builds an object, temporarily allowing optional properties.

     ```typescript
     type CourseGoal = {
       title: string;
       description: string;
       completeUntil: Date;
     };
     function createCourseGoal(
       title: string,
       description: string,
       date: Date
     ): CourseGoal {
       const courseGoal: Partial<CourseGoal> = {};
       courseGoal.title = title;
       courseGoal.description = description;
       courseGoal.completeUntil = date;
       return courseGoal as CourseGoal;
     }
     ```

3. **Read-only Type for Arrays:**

   - Introduces the `read only` type and its application to enforce immutability on an array, preventing operations like push or pop. Illustrates how it can be used to enhance precision in code.

     ```typescript
     const names: Readonly<string[]> = ["Max", "Anna"];
     // names.push('Manu'); // Error: Cannot push to a read-only array
     ```

4. **Application of Utility Types to Objects:**

   - Mentions the versatility of utility types, not limited to arrays, as they can also be applied to objects for similar use cases. For example, using `read only` to prevent modifications to object properties.

5. **Overview of Utility Types and Resources:**

   - Emphasizes that utility types are powerful tools that aid in making code more precise and preventing undesired modifications. Encourages exploring the full list of built-in utility types in the TypeScript documentation for various scenarios.

   - Provides a reminder that utility types exist only during compilation, enhancing strictness and checks, and offers increased flexibility in certain scenarios.

Built-in utility types in TypeScript, such as `partial` and `read only`, enhance the expressive power of the language by providing tools for more robust and error-resistant code. Understanding these types allows developers to leverage TypeScript's features effectively.
