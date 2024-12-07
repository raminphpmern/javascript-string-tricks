# javascript-string-tricks
Javascript String Tricks 


Javascript has many useful built in methods available to simplify your coding tasks while handling JavaScript strings. Check out the below tricks to sharpen your skills

1. Reverse a string in single line

String Reversing can be done with a simple combination of methods:
Using this split, reverse and join built in methods

const reverseStr = str => str.split('').reverse().join('');
console.log(reverseStr("world")); // Output: "dlrow"

2. Check if a String Contains Another String
Using includes, you can quickly check for substrings:

const contains = str => str.includes("world");
console.log(contains("hello world")); // Output: true
3. Convert a String to Title Case
Capitalize the first letter of each word:

const toTitleCase = str => str.split(' ')
  .map(word => word.charAt(0).toUpperCase() + word.slice(1).toLowerCase())
  .join(' ');
console.log(toTitleCase("javascript string tricks")); // Output: "Javascript String Tricks"
4. Remove Whitespace from Both Ends
Trim spaces at the start and end with trim:

const trimmed = "   hello world   ".trim();
console.log(trimmed); // Output: "hello world"
5. Repeat a String Multiple Times
Easily repeat a string using repeat:

const repeated = "hello ".repeat(3);
console.log(repeated); // Output: "hello hello hello "
6. Find the Occurrence of a Substring
Count how many times a substring appears:

const countOccurrences = (str, sub) => str.split(sub).length - 1;
console.log(countOccurrences("hello world, hello JavaScript", "hello")); // Output: 2
7. Pad a String to a Specific Length
Use padStart or padEnd to add characters to a string:

const padded = "42".padStart(5, "0");
console.log(padded); // Output: "00042"
8. Replace All Occurrences of a Substring
Replace every occurrence with replaceAll:

const updatedString = "banana".replaceAll("a", "o");
console.log(updatedString); // Output: "bonono"
For environments without replaceAll, use a global regex:

const updated = "banana".replace(/a/g, "o");
9. Extract Only Letters or Numbers
Use regex to filter specific characters:

const onlyLetters = str => str.replace(/[^a-zA-Z]/g, '');
console.log(onlyLetters("a1b2c3")); // Output: "abc"
10. Convert a String to an Array of Characters
Split a string into its individual characters:

const chars = [..."hello"];
console.log(chars); // Output: ['h', 'e', 'l', 'l', 'o']
