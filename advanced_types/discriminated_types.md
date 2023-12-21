1. **Discriminated Union Overview:**

   - Discriminated unions are a pattern used with union types to facilitate type guards when working with object types.
   - The pattern involves adding a common property (discriminator) with literal types to each object type within the union.
   - Available when dealing with interfaces or classes that make up the union.

2. **Example Setup with Interfaces:**

   - Illustration using two interfaces, `bird` and `horse`, each with a specific property (`flyingSpeed` and `runningSpeed`).
   - Creation of a union type `animal` representing either a bird or a horse.
   - A function `moveAnimal` takes an `animal` as input and performs operations based on the specific type.

     ```typescript
     interface bird {
       type: "bird";
       flyingSpeed: number;
     }
     interface horse {
       type: "horse";
       runningSpeed: number;
     }
     type animal = bird | horse;

     function moveAnimal(animal: animal): void {
       switch (animal.type) {
         case "bird":
           const speed = animal.flyingSpeed;
           console.log(`Moving at speed ${speed}`);
           break;
         case "horse":
           const speed = animal.runningSpeed;
           console.log(`Moving at speed ${speed}`);
           break;
       }
     }
     ```

3. **Discriminated Union Benefits:**

   - Enhances type safety by leveraging a common property (`type`) to differentiate between union types.
   - Eliminates the risk of mistyping and provides autocompletion support based on literal types.
   - Ensures 100% type safety when checking and accessing specific properties of the objects in the union.

4. **Literal Types as Discriminators:**

   - The `type` property in each interface is assigned a literal type (`'bird'` or `'horse'`).
   - This narrows down the possible values for the `type` property, providing a more precise type assignment.
   - The switch statement in the function leverages these literal types for effective type checking.

5. **Usage and Flexibility:**
   - Discriminated unions work seamlessly with interfaces, providing a clear and concise way to handle different object types.
   - The pattern ensures that every object within the union has a unique discriminator, making it an efficient and type-safe approach.
