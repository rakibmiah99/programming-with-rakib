CSS Flexbox দিয়ে কন্টেন্টের লে-আউট ডিজাইন করা অনেক সহজ এবং কার্যকর। Flexbox ব্যবহার করে আপনি উপাদানগুলোকে একটি লাইনে সাজাতে, সেগুলোর আকার নিয়ন্ত্রণ করতে এবং রেসপনসিভ ডিজাইন তৈরি করতে পারেন।

Flexbox-এ দুটি অংশ থাকে - একটিকে বলা হয় **Flex Container**, অন্যটিকে **Flex Items**। Flex Container-এর মধ্যে থাকা সবগুলো উপাদান Flex Items হিসেবে কাজ করে।

```css
display: flex;
flex-direction: row|column|row-reverse|column-reverse;
flex-wrap: wrap|no-wrap|wrap-reverse;
justify-content: center|flex-start|flex-end;

align-items: center|flex-start|flex-end|stretch|baseline;

align-content: space-between|space-around|stretch:default|center|flex-start|flex-end

/* Flex Item */
order: 1; /*The _order_ property can change the order of the flex items: */

flex-grow: 1/*আকারে কতটুকু বৃদ্ধি পাবে বা কমবে সেটি নির্দারন করতে পারবেন*/

flex-shrink: 0; /* যদি আপনি ০ ব্যবহার করেন তাহলে এটি সয়ংক্রিয় সংকোচন হবে না। */ 

flex-basis: 200px; /* flex item এর দৈর্ঘ্য দিয়ে দিতে পারেন*/ 






```