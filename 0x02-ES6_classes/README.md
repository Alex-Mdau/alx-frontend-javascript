# JavaScript Classes Exercises

This directory contains solutions to JavaScript class exercises.

## Table of Contents

1. [ClassRoom](#classroom)
2. [Initialize Rooms](#initialize-rooms)
3. [HolbertonCourse](#holberton-course)
4. [Currency](#currency)
5. [Pricing](#pricing)
6. [Building](#building)
7. [SkyHighBuilding](#skyhigh-building)
8. [Airport](#airport)
9. [HolbertonClass](#holberton-class)
10. [Hoisting](#hoisting)
11. [Car](#car)

## ClassRoom

Implement a class named `ClassRoom` with a constructor that accepts one attribute `maxStudentsSize` and assigns it to the private attribute `_maxStudentsSize`. The class should have a method `getMaxStudentsSize()` that returns the value of `_maxStudentsSize`.

## Initialize Rooms

Implement a function named `initializeRooms` that returns an array of 3 `ClassRoom` objects with the sizes 19, 20, and 34 (in this order).

## HolbertonCourse

Implement a class named `HolbertonCourse` with a constructor that accepts three attributes `name`, `length`, and `students`. The constructor should store these attributes in private attributes `_name`, `_length`, and `_students`, respectively. The class should have getter and setter methods for each attribute.

## Currency

Implement a class named `Currency` with a constructor that accepts two attributes `code` and `name`. The constructor should store these attributes in private attributes `_code` and `_name`, respectively. The class should have getter and setter methods for each attribute. Additionally, implement a method named `displayFullCurrency` that returns the attributes in the format `name (code)`.

## Pricing

Implement a class named `Pricing` with a constructor that accepts two attributes `amount` and `currency`. The constructor should store these attributes in private attributes `_amount` and `_currency`, respectively. The class should have getter and setter methods for each attribute. Additionally, implement a method named `displayFullPrice` that returns the attributes in the format `amount currency_name (currency_code)`. The class should also have a static method named `convertPrice` that accepts two arguments `amount` and `conversionRate` and returns the result of multiplying the amount by the conversion rate.

## Building

Implement an abstract class named `Building` with a constructor that accepts one attribute `sqft` and assigns it to the private attribute `_sqft`. The class should have a getter method for `_sqft`. The class should also define an abstract method named `evacuationWarningMessage`. If a class that extends `Building` does not implement this method, an error should be thrown with the message "Class extending Building must override evacuationWarningMessage".

## SkyHighBuilding

Implement a class named `SkyHighBuilding` that extends the `Building` class. The constructor should accept two attributes `sqft` (which should be assigned to the parent class) and `floors`, and store them in private attributes `_sqft` and `_floors`, respectively. The class should have getter methods for `_sqft` and `_floors`. The class should also override the `evacuationWarningMessage` method and return the string "Evacuate slowly the NUMBER_OF_FLOORS floors", where `NUMBER_OF_FLOORS` is the value of `_floors`.

## Airport

Implement a class named `Airport` with a constructor that accepts two attributes `name` and `code`. The constructor should store these.attributes in private attributes `_name` and `_code`, respectively. The class should have getter and setter methods for each attribute.

## HolbertonClass

Implement a class named `HolbertonClass` with a constructor that accepts two attributes `size` and `location`. The constructor should store these attributes in private attributes `_size` and `_location`, respectively. The class should have getter and setter methods for each attribute. Additionally, implement a method named `displayClassInfo` that returns the attributes in the format `Holberton Class: size students - Location: location`.

## Hoisting

Implement a function named `hoisting` that demonstrates hoisting in JavaScript. The function should print the value of a variable `message` before and after its declaration. Make sure to explain the concept of hoisting in a comment within the function.

## Car

Implement a class named `Car` with a constructor that accepts three attributes `make`, `model`, and `year`. The constructor should store these attributes in private attributes `_make`, `_model`, and `_year`, respectively. The class should have getter and setter methods for each attribute. Additionally, implement a method named `displayCarInfo` that returns the attributes in the format `Year: year - Make: make - Model: model`.

## Usage

To run the exercises, follow these steps:

1. Clone the repository: `git clone <repository-url>`
2. Navigate to the cloned directory: `cd javascript-classes-exercises`
3. Open the files in your preferred code editor.
4. Implement the missing code for each exercise.
5. Run the code to test the functionality.

