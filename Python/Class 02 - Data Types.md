ডেটা টাইপ হলো প্রোগ্রামিং ভাষায় ব্যবহৃত ডেটার ধরণ নির্ধারণের একটি উপায়।বা বলতে পারি ডাটার বিভিন্ন প্রকার বেধই ডাটা টাইপ।  পাইথনে বিভিন্ন ধরণের ডেটা টাইপ রয়েছে, যা বিভিন্ন ধরণের তথ্য সংরক্ষণ ও প্রক্রিয়াকরণের জন্য ব্যবহৃত হয়।

ডেটা টাইপের উপর নির্ভর করে বিভিন্ন অপারেশন করা যায়।  সঠিক ডেটা টাইপ ব্যবহার করলে অপারেশনগুলো দ্রুত সম্পন্ন হয়।

বাস্তব জীবনেও আমরা ডাটা টাইপ এর অপারেশন গুলো সঠিক ভাবেই সবসবই করি 
যেমন যখন আমরা গনিতে অংক করি তখন কিন্তু `five + 5 = 10 ` লিখি না অর্থ্যাৎ অক্ষরের সাথে সংখ্যার সংমিশ্রন ঘটিয়ে কিন্তু যোগ, বিয়োগ, গুন, ভাগ করি না।  নাম্বার এর সাথে নাম্বার এর অপারেশন গুলি করি ।  অক্ষরের সাথে অক্ষরের অপারেশন গুলি করি ।   

অর্থ্যাত সঠিক ডেটা টাইপ ব্যবহার করে কোডে ত্রুটি হ্রাস করা যায়।  এটি প্রোগ্রামের স্থায়িত্ব এবং নির্ভুলতা নিশ্চিত করে।

ডাটাটাইপ গুলো হল 
- ১. স্ট্রিং (String) - স্ট্রিং হলো টেক্সট ডেটা যা একাধিক অক্ষরের সমষ্টি ।                 `city = "Dhaka"`, `title = "Python Data Types`
-  সংখ্যা (Numbers) - 
	- ইনটিজার (Integer): পূর্ণ সংখ্যা `২৫, ৩০, ১০০, ৫০০`         `age = 25` , `year = 2024` , `total_student = 75`
	- ফ্লোট (Float): দশমিক সংখ্যা `22.11, 5.7, 9.8`                   `age = 25` , `height = 5.6` , `weight = 75`
-  বুলিয়ান (Boolean): বুলিয়ান হলো সত্য (True) বা মিথ্যা (False) মান নির্ধারণের জন্য ব্যবহৃত হয়।  `is_present = True` `is_active = False`
- তালিকা (List):  একাধিক মানকে একসাথে রাখা হয়।  যা স্কয়ার ব্রেকেট এর মধ্যে কমা দিয়ে দিয়ে লিখতে হয়।  
	`fruits = ["Apple", "Bannana", "mango"]`
    `numbers = [1,2,3,4,5]`
- টাপল (Tuple): এটিও একটি তালিকা ডাটা টাইপ।  কিন্তু এর ভ্যালু গুলো ফার্স্ট ব্রেকেট এর মধ্যে কমা দিয়ে দিয়ে আলাদা করতে হয়।  টাপল এ যদি একটি মাত্র ভ্যলু থাকে তাহলে শেষে কমা দিতে হবে অন্যথায় এরর দিবে। 
	- `coordinates = (23.2567, 90.4135)`
	- `colors = ("red", "green", "blue")`
	- 
- সেট (Set Data Type): এটিতেও একাধিক মান রাখা যায় কিন্তু একই মান যদি একের অধিক থাকে তাহলে সেগুলো থেকে একটি মান রাখবে।  অর্থাৎ সেট হচ্ছে ইউনিক বা একক মান গুলো ধারন করে ।  এটি ভিতর ডাটা রাখতে হলে সেকেন্ড ব্রেকেট এর মধ্যে লিখতে হয় এবং কমা দ্বারা আলাদা করা হয় ।  
	- `unique_numbers = {১, ২, ৩, ৪, ৫}`

- Dictionary ডাটা টাইপঃ এটিতেও একাধিক মান রাখা যায় কিন্তু মান গুলোকে সেকেন্ড ব্রেকেট এর মধ্যে `key:value` পেয়ার এ লিখতে হয় ।  এটি ডিকশনারির মতই প্রত্যেক্টি `key` অর্থ বহন করে। 

```python
students = {
	"name": "Alice",
    "age": 23,
    "major": "Computer Science"
}	
```