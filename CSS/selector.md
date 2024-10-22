একটি html page এর কোন একটি ইলিমেন্ট কে ৩ টি উপায়ে সিলেক্ট করতে পারবেন । 
১।  সরাসরি কোন ইলিমেন্ট এর নাম ধরে 
২।  id  attribute ধরে 
৩।  class arrtibue dore 

সরাসরি element ধরে যদি স্টাইল করতে চান তাহলে আপনাকে সেই ট্যগ এর নাম ধরে স্টাইল করতে হবে । 

```html
<h1> Welcome to our page</h1>
<h1> Subscribe us</h1>

h1{
	color: red;
}
```

ID attribute ব্যবহার করেও আপনি স্টাইল করতে পারবেন সেক্ষেত্রে আপনি যেই ইলিমেন্ট এর স্টাইল করতে চাচ্ছেন সেই ইলিমেন্ট এর একটি id attribute থাকতে হবে।  

```html
<h3 id="my-id"> Hello Bangladesh</h3>

#my-id{
	color: green;
}
```

আপনার একটি ওয়েব পেজ এ একই নামে একটি id থাকতে পারবে।  
একই নামে একাধিক id ব্যবহার করলে ভবিষ্যতে কোড এ error আসবে ।  তাই লক্ষ রাখবেন একটি পেজ এ একই নামে একাধিক id যেন না থাকে।  




id is unique

priority

overwrite 

inheritence 



