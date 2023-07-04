ES6_data_manipulation

This directory  contains JavaScript code for data manipulation tasks using ES6 features.
Task 0: Basic list of objects

File: 0-get_list_students.js

javascript

function getListStudents() {
  return [
    { id: 1, firstName: 'Guillaume', location: 'San Francisco' },
    { id: 2, firstName: 'James', location: 'Columbia' },
    { id: 5, firstName: 'Serena', location: 'San Francisco' },
  ];
}

export default getListStudents;

Task 1: More mapping

File: 1-get_list_student_ids.js

javascript

function getListStudentIds(students) {
  if (!Array.isArray(students)) {
    return [];
  }

  return students.map((student) => student.id);
}

export default getListStudentIds;

Task 2: Filter

File: 2-get_students_by_loc.js

javascript

function getStudentsByLocation(students, city) {
  return students.filter((student) => student.location === city);
}

export default getStudentsByLocation;

Task 3: Reduce

File: 3-get_ids_sum.js

javascript

function getStudentIdsSum(students) {
  return students.reduce((sum, student) => sum + student.id, 0);
}

export default getStudentIdsSum;

Task 4: Combine

File: 4-update_grade_by_city.js

javascript

function updateStudentGradeByCity(students, city, newGrades) {
  return students.map((student) => {
    const gradeObj = newGrades.find((grade) => grade.studentId === student.id);
    student.grade = gradeObj ? gradeObj.grade : 'N/A';
    return student;
  });
}

export default updateStudentGradeByCity;

Task 5: Typed Arrays

File: 5-typed_arrays.js

javascript

function createInt8TypedArray(length, position, value) {
  if (position >= length || position < 0) {
    throw new Error('Position outside range');
  }

  const buffer = new ArrayBuffer(length);
  const dataView = new DataView(buffer);
  dataView.setInt8(position, value);

  return dataView;
}

export default createInt8TypedArray;

Task 6: Set data structure

File: 6-set.js

javascript

function setFromArray(arr) {
  return new Set(arr);
}

export default setFromArray;

Task 7: More set data structure

File: 7-has_array_values.js

javascript

function hasValuesFromArray(set, arr) {
  return arr.every((value) => set.has(value));
}

export default hasValuesFromArray;

Task 8: Clean set

File: 8-clean_set.js

javascript

function cleanSet(set, startString) {
  const result = [];
  set.forEach((value) => {
    if (value.startsWith(startString)) {
      result.push(value.slice(startString.length));
    }
  });
  return result.join('-');
}

export default cleanSet;

Task 9: Map data structure

File: 9-groceries_list.js

javascript

function groceriesList() {
  const groceries = new Map();
  groceries.set('Apples', 10);
  groceries.set('Tomatoes', 10);
  groceries.set('Pasta', 1);
  groceries.set('Rice', .  groceries.set('Rice', 5);
  groceries.set('Bananas', 6);

  return groceries;
}

export default groceriesList;

Task 10: Update groceries

File: 10-update_groceries.js

javascript

function updateGroceries(groceriesMap, groceryItem, quantity) {
  if (groceriesMap.has(groceryItem)) {
    const currentQuantity = groceriesMap.get(groceryItem);
    groceriesMap.set(groceryItem, currentQuantity + quantity);
  } else {
    groceriesMap.set(groceryItem, quantity);
  }
}

export default updateGroceries;
