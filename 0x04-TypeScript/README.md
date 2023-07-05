Task 1: Let's build a Teacher interface
Instructions

    Create a directory named task_1 and copy the following configuration files into this folder: package.json, tsconfig.json, webpack.config.js.

    Implement the Teacher interface with the following attributes:
        firstName (string) and lastName (string): These two attributes should only be modifiable when a Teacher is first initialized.
        fullTimeEmployee (boolean): This attribute should always be defined.
        yearsOfExperience (number): This attribute is optional.
        location (string): This attribute should always be defined.
        Add the possibility to add any attribute to the Object like contract (boolean) without specifying the name of the attribute.

Example:

typescript

const teacher3: Teacher = {
  firstName: 'John',
  fullTimeEmployee: false,
  lastName: 'Doe',
  location: 'London',
  contract: false,
};

console.log(teacher3);

// should print
// Object
// contract: false
// firstName: "John"
// fullTimeEmployee: false
// lastName: "Doe"
// location: "London"

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    Files: task_1/js/main.ts, task_1/webpack.config.js, task_1/tsconfig.json, task_1/package.json

Task 2: Extending the Teacher class
Instructions

    Implement an interface named Directors that extends Teacher. It requires an attribute named numberOfReports (number).

Example:

typescript

const director1: Directors = {
  firstName: 'John',
  lastName: 'Doe',
  location: 'London',
  fullTimeEmployee: true,
  numberOfReports: 17,
};
console.log(director1);

// should print
// Object
// firstName: "John"
// fullTimeEmployee: true
// lastName: "Doe"
// location: "London"
// numberOfReports: 17

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    File: task_2/js/main.ts

Task 3: Printing teachers
Instructions

    Write a function printTeacher that accepts two arguments: firstName and lastName. It returns the first letter of the firstName and the full lastName.

Example: printTeacher("John", "Doe") -> J. Doe

    Write an interface for the function named printTeacherFunction.

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    File: task_1/js/main.ts

Task 4: Writing a class
Instructions

    Write a Class named StudentClass:
        The constructor accepts firstName (string) and lastName (string) arguments.
        The class has a method named workOnHomework that returns the string "Currently working".
        The class has a method named displayName that returns the `firstNameof the student.
        The constructor of the class should be described through an Interface.
        The class should be described through an Interface.

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    File: task_1/js/main.ts

Task 5: Advanced types Part 1
Instructions

    Create the DirectorInterface interface with the 3 expected methods:
        workFromHome() returning a string
        getCoffeeBreak() returning a string
        workDirectorTasks() returning a string

    Create the TeacherInterface interface with the 3 expected methods:
        workFromHome() returning a string
        getCoffeeBreak() returning a string
        workTeacherTasks() returning a string

    Create a class Director that will implement DirectorInterface:
        workFromHome() should return the string "Working from home"
        getToWork() should return the string "Getting a coffee break"
        workDirectorTasks() should return the string "Getting to director tasks"

    Create a class Teacher that will implement TeacherInterface:
        workFromHome() should return the string "Cannot work from home"
        getCoffeeBreak() should return the string "Cannot have a break"
        workTeacherTasks() should return the string "Getting to work"

    Create a function createEmployee with the following requirements:
        It can return either a Director or a Teacher instance
        It accepts 1 argument: salary (either number or string)
        If salary is a number and less than 500, it should return a new Teacher. Otherwise, it should return a Director.

Example:

typescript

console.log(createEmployee(200));
// Teacher

console.log(createEmployee(1000));
// Director

console.log(createEmployee('$500'));
// Director

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    File: task_2/js/main.ts, task_2/webpack.config.js, task_2/tsconfig.json, task_2/package.json

Task 6: Creating functions specific to employees
Instructions

    Write a function isDirector:
        It accepts employee as an argument.
        It will be used as a type predicate to check if the employee is a director.

    Write a function executeWork:
        It accepts employee as an argument.
        If the employee is a Director, it will call workDirectorTasks.
        If the employee is a Teacher, it will call workTeacherTasks.

Example:

typescript

executeWork(createEmployee(200));
// Getting to work

executeWork(createEmployee(1000));
// Getting to director tasks

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    File: task_2/js/main.ts

Task 7: String literal types
Instructions

    Write a String literal type named Subjects allowing a variable to have the value "Math" or "History" only.

    Write a function named teachClass:
    -It takes todayClass as an argument.
        It will return the string "Teaching Math" if todayClass is "Math".
        It will return the string "Teaching History" if todayClass is "History".

Example:

typescript

teachClass('Math');
// Teaching Math

teachClass('History');
// Teaching History

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    File: task_2/js/main.ts

Task 8: Ambient Namespaces
Instructions

    Create a directory called task_3 and copy the following configuration files into it: package.json, webpack.config.js, tsconfig.json.

    Inside a file named interface.ts, create the following:
        Create a type RowID and set it equal to number.
        Create an interface RowElement that contains these 3 fields:
            firstName: string
            lastName: string
            age?: number

    Download the crud.js library and copy the file into the task_3/js directory. The library provides the following functions:
        insertRow(row): Inserts a row and returns a random row ID.
        deleteRow(rowId): Deletes a row with the given row ID.
        updateRow(rowId, row): Updates a row with the given row ID and new data.

    Write an ambient file within task_3/js named crud.d.ts containing the type declarations for each crud function. Import RowID and RowElement from interface.ts.

    In main.ts, do the following:
        Include all the dependencies from crud.d.ts using a triple slash directive at the top of the file.
        Import the RowID type and RowElement from interface.ts.
        Import everything from crud.js as CRUD.
        Create an object called row with the type RowElement and set the fields to the provided values: firstName: "Guillaume", lastName: "Salva".
        Create a const variable named newRowID with the type RowID and assign the value of the insertRow command.
        Create a const variable named updatedRow with the type RowElement and update row with an age field set to 23.
        Finally, call the updateRow and deleteRow commands.

Example:

typescript

const obj = { firstName: "Guillaume", lastName: "Salva" };
CRUD.insertRow(obj);
// Insert row {firstName: "Guillaume", lastName: "Salva"}

const updatedRow: RowElement = { firstName: "Guillaume", lastName: "Salva", age: 23 };
CRUD.updateRow(newRowID, updatedRow);
// Update row 125 {firstName: "Guillaume", lastName: "Salva", age: 23}

CRUD.deleteRow(125);
// Delete row id 125

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript
    Files: task_3/js/main.ts, task_3/js/interface.ts, task_3/js/crud.d.ts

Task 9: Namespace & Declaration merging
Instructions1. Create a new directory named task_4 and copy the provided tsconfig.json file into it. Also, create a package.json file with the provided content.

json

{
  "name": "task_4",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "@typescript-eslint/eslint-plugin": "^2.4.0",
    "@typescript-eslint/parser": "^2.4.0",
    "typescript": "^3.6.4"
  }
}

    In the task_4/js/subjects directory, create a file named Teacher.ts and write a Teacher interface in a namespace named Subjects.

typescript

namespace Subjects {
  export interface Teacher {
    firstName: string;
    lastName: string;
  }
}

Repository Details

    GitHub repository: alx-frontend-javascript
    Directory: 0x04-TypeScript/task_4
    Files: tsconfig.json, package.json, js/subjects/Teacher.ts

