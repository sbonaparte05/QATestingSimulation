// Calculator Functions
function add(a, b) {
  return a + b;
}

function subtract(a, b) {
  return a - b;
}

function multiply(a, b) {
  return a * b;
}

function divide(a, b) {
  if (b === 0) {
    throw new Error("Division by zero is not allowed."); // Correct error handling
  }
  return a / b;
}

// Test Cases
console.log("Addition Test 1:", add(5, 3) === 8 ? "Pass" : "Fail");
console.log("Subtraction Test 1:", subtract(10, 4) === 6 ? "Pass" : "Fail"); // Corrected expected value
console.log("Multiplication Test 1:", multiply(7, 6) === 42 ? "Pass" : "Fail");
console.log("Division Test 1:", divide(12, 4) === 3 ? "Pass" : "Fail");

// Add tests for edge cases
// Test for division by zero
try {
  divide(20, 0);
  console.log("Division by Zero Test: Fail (Error not thrown)");
} catch (e) {
  console.log("Division by Zero Test:", e.message === "Division by zero is not allowed." ? "Pass" : "Fail");
}

// Tests with negative numbers
console.log("Addition Test Negative:", add(-5, -3) === -8 ? "Pass" : "Fail");
console.log("Subtraction Test Negative:", subtract(-10, -7) === -6 ? "Pass" : "Fail");
console.log("Multiplication Test Negative:", multiply(-6, -9) === 42 ? "Pass" : "Fail");

Steps to fix the code:
Correct the expected value in the subtraction test case. The result of subtract(10, 4) is 6, not 5.
