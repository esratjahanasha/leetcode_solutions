Problem Statement
একটি array nums এবং একটি সংখ্যা target দেওয়া থাকবে।
##Approach 1: Brute Force (সরাসরি পেয়ার চেক করা)

###ধারণা (Idea)
-প্রতিটি element এর সাথে বাকি সব element এর pair চেক করা।
-যদি যোগফল target-এর সমান হয় → সেই pair এর index return করা।

###Complexity (সময় ও স্থান খরচ)
Time Complexity: O(n²) → সব pair চেক করতে হচ্ছে
Space Complexity: O(1) → কোনো extra data structure লাগেনি

###নোটস
-খুব সহজে implement করা যায়
-ছোট array এর জন্য ঠিক আছে
-বড় array এর জন্য ধীর (slow)
Approach 2: Optimized Approach with Map (HashMap ব্যবহার করে)

###ধারণা (Idea)
-Map object ব্যবহার করা হবে, যাতে আগের element দ্রুত lookup করা যায়।
-প্রতিটি element nums[i] এর জন্য complement বের করা হবে
-যদি complement map-এ থাকে → solution পেয়েছি।
-না থাকলে → current number + index map-এ store করব।

###Complexity (সময় ও স্থান খরচ)
Time Complexity: O(n) → একবার array loop করা + map operations O(1)
Space Complexity: O(n) → worst case সব element map-এ store হবে

###নোটস
বড় array এর জন্য খুব efficient
Map ব্যবহার করে previous elements দ্রুত খুঁজে পাওয়া যায়
একটু extra memory লাগে, তবে speed অনেক বেশি

###শেখার মূল কথা (Key Takeaways)
প্রথমে problem ঠিকভাবে বুঝতে হবে।
ছোট input এর জন্য brute force ঠিক আছে।
বড় input বা speed চাইলে Map/HashMap ব্যবহার করা ভালো।
Map ব্যবহার করার intuition:
“আগের element track করতে হবে”
“fast lookup দরকার”