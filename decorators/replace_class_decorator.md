- **Decorator's Advanced Capabilities:**

  - Decorators, like class decorators and method decorators, can return values inside the decorator function.
  - This return value depends on the type of decorator you're working with.
  - For class decorators, you can return a new constructor function or a new class, effectively replacing the original one.
  - The returned class can extend the original class, preserving its properties.
  - This capability enables the addition of extra logic that runs when an instance of the class is instantiated, not just when the class is defined.

- **Example: Class Replacement with Decorator:**

  - The WithTemplate decorator is enhanced to return a new constructor function, effectively creating a new class.
  - This new class extends the original class and adds custom logic, allowing extra actions during instantiation.
  - The original class properties are preserved by calling `super()` inside the new constructor.
  - Now, the decorator's logic executes only when an instance of the class is created, not when the class is defined.

- **TypeScript Generic Decorator:**

  - To handle dynamic arguments for the constructor, the decorator function is turned into a generic function using TypeScript generics.
  - The generic type T represents the original constructor, ensuring the decorator is type-safe and compatible with various classes.

- **Enhanced Decorator Execution:**

  - The decorator execution order is during class definition, not instantiation.
  - By returning a new class, the decorator allows the addition of metaprogramming features, executing logic when an object is instantiated, not just when the class is defined.

- **Dynamic Rendering Example:**
  - The enhanced decorator ensures that template rendering now occurs only when an instance of the class is created.
  - When the class is defined but not instantiated, the template rendering logic is not triggered, showcasing the decorator's runtime flexibility.
