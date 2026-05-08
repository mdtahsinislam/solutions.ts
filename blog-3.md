3 How do Generics allow you to build reusable components and functions that stay strictly typed regardless of the data structures passed in?        
        
Generics in programming (especially in TypeScript and similar languages) allow developers to create reusable components, functions, and classes that can work with different data types while still maintaining strict type safety.
Instead of writing separate functions for each data type (such as number, string, or object), generics let us define a “type placeholder” that gets determined when the function or component is used.
প্রোগ্রামিংয়ে Generics (বিশেষ করে TypeScript-এ) ব্যবহার করে আমরা এমন reusable component বা function তৈরি করতে পারি যা বিভিন্ন ধরনের ডাটা (number, string, object ইত্যাদি) এর সাথে কাজ করতে পারে, কিন্তু type safety বজায় রাখে।
Generics আসলে একটি “type placeholder” হিসেবে কাজ করে, যা পরে ব্যবহার করার সময় নির্ধারিত হয়।

How it works:
A generic type acts like a variable for types (e.g., T).
When the function is called, the actual type is provided.
The compiler ensures type consistency throughout the usage.
Benefits:
Code reusability (one function works for many types)
Strict type safety (prevents wrong type usage)
Better maintainability
Reduces code duplication

কিভাবে কাজ করে:
T এর মতো generic type একটি variable টাইপ হিসেবে কাজ করে
যখন function ব্যবহার করা হয় তখন আসল টাইপ দেওয়া হয়
Compiler নিশ্চিত করে যে সব জায়গায় একই টাইপ ব্যবহার হচ্ছে
সুবিধা:
কোড পুনরায় ব্যবহার করা যায় (reusable code)
Type safety নিশ্চিত থাকে
কোড সহজে maintain করা যায়
একই কাজের জন্য বারবার আলাদা function লিখতে হয় না

Example: 
A generic function: 

function identity<T>(value: T): T {
    return value;
}

