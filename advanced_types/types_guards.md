1. **Type Guards Overview:**

   - Type guards are a feature used to narrow down types within union types during runtime.
   - Useful when dealing with flexibility provided by union types and needing to perform specific operations based on the exact type.
   - Commonly used scenarios include typeof checks, `in` keyword checks, and instanceof checks.

2. **Union Type Function Example:**

   - Example of a function `add` that takes two parameters of type `Combinable` (union type of string or number).
   - Uses a type guard to check the type of each parameter and performs different operations accordingly.

     ```typescript
     type Combinable = string | number;

     function add(a: Combinable, b: Combinable): Combinable {
       if (typeof a === "string" || typeof b === "string") {
         return a.toString() + b.toString();
       } else {
         return a + b;
       }
     }
     ```

3. **Object Type Type Guard:**

   - Example of an object type with type guard using the `in` keyword.
   - Two custom object types: `admin` and `employee`, with an `UnknownEmployee` union type.
   - Function `printEmployeeInformation` uses type guards to check for property existence.

     ```typescript
     type admin = { name: string; privileges: string[] };
     type employee = { name: string; startDate: Date };
     type UnknownEmployee = admin | employee;

     function printEmployeeInformation(emp: UnknownEmployee): void {
       console.log(emp.name);
       if ("privileges" in emp) {
         console.log(emp.privileges);
       }
       if ("startDate" in emp) {
         console.log(emp.startDate);
       }
     }
     ```

4. **Class Type Guard:**

   - Example using `instanceof` as a type guard for classes (`Car` and `Truck`).
   - Function `useVehicle` takes a parameter of type `Vehicle` (union of `Car` and `Truck`).
   - Uses `instanceof` to check the type and perform specific operations accordingly.

     ```typescript
     class Car {
       drive(): void {
         console.log("Driving");
       }
     }
     class Truck {
       drive(): void {
         console.log("Driving a truck");
       }
       loadCargo(amount: number): void {
         console.log(`Loading cargo: ${amount}`);
       }
     }
     type Vehicle = Car | Truck;

     function useVehicle(vehicle: Vehicle): void {
       vehicle.drive();
       if (vehicle instanceof Truck) {
         vehicle.loadCargo(1000);
       }
     }
     ```

5. **Considerations and Use Cases:**
   - Type guards provide a way to safely handle different types within a union type.
   - Useful in scenarios where runtime information about types is needed.
   - Choose the appropriate type guard (`typeof`, `in`, `instanceof`) based on the specific use case and the types involved.
