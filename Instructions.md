Work through the tasks below. Pay attention to the details. If a task doesn't specify if a variable/method should be public or private then decide for yourself based on the context.

## Creating Objects
In `main()`
1. Create a *Vehicle* **object** called `redCar`.
2. Create a *Vehicle* **object** called `blueBus` that has 8 wheels and can carry twelve passengers.
3. Create a **reference** to `blueBus` called `hospitalBus`.
4. Create a **reference** called `currentVehicle` that is not connected to a vehicle. We will use that later.

## Member Variables & Class Methods
1. Add a **member variable** to `Vehicle` called `driver` that will be used to store the driver's name. `driver` should not be accessible outside the class.
2. Add a **class method** to `Vehicle` called `setDriver(String firstName, String surname)`. This method should verify that both parameters are non-empty strings before setting the `driver` name.
3. Add a **class method** to `Vehicle` to return the driver's name.
4. Add a **class method** to `Vehicle` called `setDriver(string driver)` that verifies that the string isn't empty, that it contains two names, and then sets the drivers name if it is valid.

**In main()**

5. Use `setDriver(String firstName, String surname)` to set the driver of `redCar` to "James Bond".
6. Print out the `driver` of `redCar` to verify this was set correctly.
7. Use `setDriver(String driver)` to set the driver of `redCar` to "Felix".
8. Print out the `driver` of `redCar` to verify this was has not changed the name
9. Use `setDriver(String driver)` to set the driver of `blueBus` to "Keanu Reeves".
10. Print out the `driver` of `blueBus` to verify this was set correctly.

## Constructors
1. Add a **constructor** to `Vehicle` that takes two integers as parameters representing the number of wheels a vehicle has and the number of passengers it can carry.
2. In `main()` use your new constructor to create a vehicle called `forklift` that has four wheels and can carry no passengers.
3. Add a **class method** to `Vehicle` called `setPassengers` that takes an integer as a parameter and verifies that it is >= 0 and sets `passengers` if it is.
4. Add a **class method** to `Vehicle` called `setWheels` that takes an integer as a parameter and verifies it is a positive even integer before setting the `wheels` **member variable**.
5. Update the **constructors** so that they use `setPassengers` and `setWheels` (where appropriate).

## Creating A New Class
1. Create a new **class** called `Colour`. It should have three member variables that are integers called `red`, `blue` and `green`. 
2. Add a method `setColour` to `Colour` that takes three integers `red`, `green`, and `blue`. It should verify that the integers are in the range 0 to 255. Values outside that range should be capped to that range.
3. Add a **constructor** to `Colour` that takes three integers `red`, `green` and `blue` and uses `setColour` to set the values.
4. Add a method to `Colour` called `printColour()` that prints out the three integers that make up the colour.

## Object as Member Variables
1. Add a member variable to `Vehicle` that is a `Colour` **object** called `colour`.
2. Add a class method to `Vehicle` called `setColour(Colour colour)`.
3. Add a class method to `Vehicle` called `setColour(int red, int green, int blue)`.
4. Add a class method to `Vehicle` called `getColour()`
5. Test both versions of `setColour()`

## Inheritance

1. Create a new class called `IndustrialVehicle` that inherits from `Vehicle`. It should have a new member variable called `carryingCapacity` that stores the weight the vehicle can carry.
2. Create a constructor for `IndustrialVehicle` that has parameters for wheels, passengers and carrying capacity. It should set the carrying capacity itself but use its parent's constructor to set the other values.
3. Change where you create the `forklift` object so that it is now an `IndustrialVehicle`.
4. Industrial vehicles have special licensing and insurance requirements. These vary a great deal between different types of industrial vehicle. Add an abstract method `void licensingRequirements()` to `IndustrialVehicle`. Ensure the application compiles and runs after making this change.
5. Add a new class `HeavyGoodsVehicle` that **inherits** from `IndustrialVehicle`. Give it a constructor that calls its parent's constructor.
