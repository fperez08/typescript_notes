- **Execution during Class Definition:** Decorators run when you define a class, not during instantiation or runtime. This is a crucial distinction to grasp.

- **Metaprogramming Concept:** Decorators follow a metaprogramming paradigm, allowing you to perform behind-the-scenes setup work during class definition.

- **Not Event Listeners:** Unlike event listeners, decorators are not designed to respond during method or property calls. They are functions executed during class definition, allowing you to enhance or modify class behavior.

- **Adding Extra Functionality:** Decorators are primarily used to add extra functionality or metadata behind the scenes, offering a way to set up code that may run later when interacting with the class or method.

- **Example with Template Decorator:** The template decorator discussed earlier, which adds functionality during class definition, not instantiation, serves as an example. You might store the template internally and use it when needed, not necessarily when creating a new instance.
