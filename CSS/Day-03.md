## Border

**CSS `border`** প্রপার্টি ব্যবহার করে একটি এলিমেন্টের চারপাশে সীমারেখা (border) তৈরি করা যায়।  এটি এলিমেন্টের আকার ও শৈলীর ওপর প্রভাব ফেলে। `border` মূলত তিনটি বৈশিষ্ট্যের সমন্বয়ে তৈরি হয়:

**Border Width**: বর্ডারের পুরুত্ব বা প্রস্থ নির্ধারণ করে। এটি পিক্সেল বা কিওয়ার্ড (`thin`, `medium`, `thick`) দ্বারা সেট করা যায়।

```css
border-width: 2px;
```

**Border Style**: বর্ডারের শৈলী নির্ধারণ করে।  এখানে বিভিন্ন ধরণের শৈলী ব্যবহার করা যায়, যেমন:

- `solid`: একটানা সোজা রেখা।
- `dashed`: ড্যাশের মত বিন্দুবিন্দু রেখা।
- `dotted`: বিন্দু বিন্দু রেখা।
- `double`: দ্বিগুণ রেখা।
- `groove`, `ridge`, `inset`, `outset`: থ্রিডি প্রভাবযুক্ত বর্ডার।

```css
border-style: solid;
```

**Border Color**: বর্ডারের রঙ নির্ধারণ করে।  রঙের মান হতে পারে হেক্স কোড, RGB, বা রঙের নাম।
```css
border-color: #ff0000; /* লাল রঙ */
```


---
**shorthand border**
বর্ডার এর ৩ টি বৈশিষ্ট কে একসাথে `border` প্রপার্টি এর মধ্যে লিখা যায়। 
```css
border: 2px solid #0000ff; /* border width, style, color */
```

---

**চারপাশের বর্ডার আলাদাভাবে নির্ধারণ**
বর্ডারের প্রতিটি দিক (top, right, bottom, left) আলাদাভাবে সেট করা যায়:

- **border-top**: উপরের বর্ডার
- **border-right**: ডান দিকের বর্ডার
- **border-bottom**: নিচের বর্ডার
- **border-left**: বাম দিকের বর্ডার\

```css
div {
  border-top: 2px solid red;
  border-right: 3px dashed blue;
  border-bottom: 4px dotted green;
  border-left: 5px double black;
}

```

**Border Radius**
`border-radius` প্রপার্টি ব্যবহার করে বর্ডারের কোণ গোলাকার করা যায়।

```css
div {
  border: 2px solid black;
  border-radius: 10px; /* কোণগুলো গোলাকার */
}
```

---
## Padding


**CSS `padding`** প্রপার্টি ব্যবহার করে একটি এলিমেন্টের content-এর চারপাশে থাকা খালি জায়গার (space) আকার নির্ধারণ করা হয়। এটি মূলত content এবং border-এর মধ্যে থাকা অভ্যন্তরীণ স্থান তৈরি করে।  Padding-এর মান এলিমেন্টের চারপাশের চারটি দিকেই আলাদাভাবে বা একসাথে নির্ধারণ করা যায়।

যদি শুধুমাত্র একটি মান ব্যবহার করা হয়, এটি এলিমেন্টের সব দিকের জন্য একই padding সেট করে।

```css
div {
  padding: 20px; /* চারদিকে ২০ পিক্সেল padding */
}
```

#### 2. **দুটি মান**

যদি দুটি মান ব্যবহার করা হয়, প্রথমটি হবে উপরের ও নিচের দিকের padding, এবং দ্বিতীয়টি হবে বাম ও ডান দিকের padding।

```css
div {
  padding: 20px 10px; /* উপর-নিচে ২০px, বাম-ডানে ১০px */
}
```

#### 3. **তিনটি মান**

তিনটি মান ব্যবহার করলে প্রথমটি উপরের, দ্বিতীয়টি ডান-বাম, এবং তৃতীয়টি নিচের padding নির্ধারণ করে।
```css
div {
  padding: 20px 10px 5px; /* উপর ২০px, ডান-বাম ১০px, নিচ ৫px */
}
```

#### 4. **চারটি মান**

চারটি মান ব্যবহার করলে প্রতিটি দিকের জন্য আলাদা padding নির্ধারণ করা হয় (উপরে, ডানে, নিচে, এবং বামে)।

```css
div {
  padding: 20px 10px 5px 15px; /* উপর ২০px, ডান ১০px, নিচে ৫px, বামে ১৫px */
}
```

## প্রতিটি দিকের জন্য পৃথক Padding

**Padding-top**, **padding-right**, **padding-bottom**, এবং **padding-left** প্রপার্টি ব্যবহার করে প্রতিটি দিকের padding আলাদাভাবে নির্ধারণ করা যায়।

```css
div {
  padding-top: 20px;
  padding-right: 15px;
  padding-bottom: 10px;
  padding-left: 5px;
}
```


---
## Margin
**CSS `margin`** প্রপার্টি ব্যবহার করে একটি এলিমেন্টের চারপাশে থাকা বাহ্যিক ফাঁকা স্থান (space) নির্ধারণ করা হয়, যা এলিমেন্ট এবং এর চারপাশের অন্য এলিমেন্টগুলোর মধ্যে দূরত্ব তৈরি করে। এটি বর্ডারের বাইরের অংশে প্রভাব ফেলে এবং কোনো ব্যাকগ্রাউন্ড রঙ বহন করে না।

 **একটি মান**
যদি শুধুমাত্র একটি মান ব্যবহার করা হয়, এটি এলিমেন্টের সব দিকের জন্য একই margin সেট করে।
```css
div {
  margin: 20px; /* সব দিকেই ২০px margin */
}
```

#### 2. **দুটি মান**
যদি দুটি মান ব্যবহার করা হয়, প্রথমটি উপরের এবং নিচের জন্য এবং দ্বিতীয়টি বাম এবং ডান দিকের জন্য margin নির্ধারণ করে।

```css
div {
  margin: 20px 10px; /* উপর-নিচে ২০px, বাম-ডানে ১০px */
}
```


---

**CSS Box Model** হলো প্রতিটি HTML এলিমেন্টের চারপাশে থাকা চারটি প্রধান অংশের ধারণা, যা একটি এলিমেন্ট কিভাবে প্রদর্শিত হবে তা নিয়ন্ত্রণ করে। এই চারটি অংশ হল:

1. **Content**: এটি সেই এলাকা যেখানে আসল কন্টেন্ট প্রদর্শিত হয়, যেমন লেখা, ইমেজ ইত্যাদি। Content-এর আকার সাধারণত width এবং height দ্বারা নির্ধারিত হয়।
    
2. **Padding**: Content-এর চারপাশে থাকা খালি স্থান, যা কন্টেন্ট এবং বর্ডার-এর মধ্যে থাকে। Padding-এর আকারকে পরিবর্তন করা যায় `padding` প্রোপার্টি দিয়ে। এটি এলিমেন্টের ব্যাকগ্রাউন্ড রঙ বহন করে।
    
3. **Border**: Padding-এর বাইরে থাকা একটি রেখা, যা এলিমেন্টের আকার এবং শৈলী প্রদর্শন করে। `border` প্রোপার্টি দিয়ে এর আকার, রঙ, এবং শৈলী নিয়ন্ত্রণ করা যায়।
    
4. **Margin**: Border-এর বাইরের অংশ, যা এলিমেন্টের চারপাশে থাকা অন্য এলিমেন্টের সাথে দূরত্ব তৈরি করে। `margin` প্রোপার্টি দিয়ে এর আকার নির্ধারণ করা যায়। Margin কোনো ব্যাকগ্রাউন্ড রঙ বহন করে না, এটি সর্বদা স্বচ্ছ থাকে।













