1. **Multiple Decorators on a Class:**

   - Demonstrates the ability to apply multiple decorators to a class. In this example, both `Logger` and `WithTemplate` decorators are applied to the `Person` class.

     ```typescript
     @WithTemplate("<h1>My Person Object</h1>", "app")
     @Logger
     class Person {
       // Class definition
     }
     ```

2. **Execution Order of Decorators:**

   - Explains the order in which decorators execute. Shows that decorator functions execute in a bottom-up fashion, with the bottom-most decorator executing first and decorators above it following. The order is crucial in understanding how decorators affect the class.

3. **Decorator Factories Order:**

   - Clarifies that the order of decorator factories matters in terms of when they are executed. The creation of decorator functions (factories) follows the order in which they are specified. Demonstrates this concept with a `Logger Factory` and a `Template Factory`.

     ```typescript
     @LoggerFactory
     @WithTemplateFactory("<h1>My Person Object</h1>", "app")
     class Person {
       // Class definition
     }
     ```

4. **Execution Timing of Decorator Factories:**

   - Emphasizes that decorator factories run earlier than decorator functions. While the creation of decorator functions follows the order of decorator factories, the actual execution of decorator functions occurs in a bottom-up order.

5. **Application Beyond Classes:**
   - Concludes by hinting at the broader application of decorators. Encourages exploration into other places, besides classes, where decorators can be applied and how they can enhance functionality.

Understanding the order of decorator execution, both for decorator functions and factories, is essential for using decorators effectively. The example showcases the versatility of decorators by applying them to classes and hints at the possibility of exploring other use cases beyond classes.
