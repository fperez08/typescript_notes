1. **Turning Name into a Private Property:**

   - To make the `name` property private, use the `private` access modifier in the constructor parameter.
   - This eliminates the need for separate field definitions and value assignments in the constructor.

2. **Access Modifiers in Constructor Parameters:**

   - Instead of initializing properties in the constructor body, use access modifiers in front of constructor parameters.
   - For public properties, add `public` before the parameter, and for private properties, add `private`.

3. **Simplified Initialization Code:**

   - The access modifiers serve as an explicit instruction to TypeScript to create properties with the same names.
   - The values passed as arguments to the constructor are automatically assigned to the corresponding properties.

4. **Example - Making Name Public:**

   ```typescript
   class Department {
     constructor(public id: string, public name: string) {}
   }
   ```

5. **Improved Code Readability:**
   - This approach streamlines property initialization, making the code more concise and readable.
   - The constructor's purpose is clearer, as it directly reflects the properties to be initialized.
