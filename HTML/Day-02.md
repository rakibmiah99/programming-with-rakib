### Unordered Lists (`<ul>`)
Unordered list এমন একটি তালিকা যেখানে বিষয়বস্তু কোন নির্দিষ্ট অর্ডারে সাজানো হয় না।  অর্থাৎ কোন সিকুয়েন্স বা ক্রম আকারে দেখানো হয় না। 
```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

`By default, this renders as a list with bullet points.`

#### Common Attributes for `<ul>`:

- **`type`**:  লিস্ট এর বুলেট গুলো কোন ধরনের হবে সেটি type attribute এর মাধ্যমে বলে দেওয়া যায়। 
    - `disc` (default) 
    - `circle`
    - `square`

### Description Lists (`<dl>`)

যদি আপনার এমন কোন লিস্ট এর প্রয়োজন হয় যেখানে defination এবং Deitails থাকবে, সেখানে Description List এর ব্যবহার করতে পারেন।  

```html
<dl>
  <dt>Coffee</dt>
  <dd>A brewed drink prepared from roasted coffee beans.</dd>

  <dt>Tea</dt>
  <dd>An aromatic beverage commonly prepared by pouring hot water over cured tea leaves.</dd>

  <dt>Milk</dt>
  <dd>A nutrient-rich liquid food produced by mammals.</dd>
</dl>
```


---

### External এবং Internal Links

**External Links**
**External Links** হলো এমন লিঙ্ক, যা আপনাকে এক ওয়েবসাইট থেকে অন্য ওয়েবসাইটে নিয়ে যায়।  সাধারণত, এগুলো ওয়েব পেজের বাইরে অন্য ডোমেইনে নির্দেশ করে।
```html
`<a href="https://www.example.com">Visit Example.com</a>`
```

**Internal Links**
অভ্যন্তরীণ লিঙ্ক দ্বারা একই পেজের বিভিন্ন সেকশনে নিয়ে যাওয়া যায়, যাকে **Anchor Link** বলে।
```html
`<a href="/home.html">Home Page</a>`
`<a href="/about.html">About Page</a>`
```

### External vs. Internal Link Summary:

| Feature              | External Links                               | Internal Links                           |
| -------------------- | -------------------------------------------- | ---------------------------------------- |
| **Purpose**          | এক ওয়েবসাইট থেকে অন্য ওয়েবসাইটে নিয়ে যায় | একই ওয়েবসাইটের পেজ বা সেকশনে নিয়ে যায় |
| **URL Structure**    | Full URL (e.g., `https://example.com`)       | Relative URL (e.g., `/about-us.html`)    |
| **Target Attribute** | সাধারণত `target="_blank"` ব্যবহার হয়        | সাধারণত `target` প্রয়োজন হয় না         |
| **Example**          | `<a href="https://example.com">Link</a>`     | `<a href="/about-us.html">Link</a>`      |

### Email Links in HTML

ইমেইল লিংক ব্যবহারকারীদের তাদের ইমেইল সফটওয়্যার (যেমন Gmail, Outlook, ইত্যাদি) সরাসরি খোলার সুযোগ দেয়, যাতে তারা নির্দিষ্ট একটি ইমেইল ঠিকানায় মেইল পাঠাতে পারে।  ইমেইল লিংক তৈরি করতে, আপনি `<a>` ট্যাগের `href` এট্রিবিউট এর ভ্যলুতে  `mailto:` স্কিম ব্যবহার করতে হবে।   

```html
<a href="mailto:programmingwithrakib@gmail.com">Contact Us</a>
```

**Adding Subject, Body, CC, and BCC:**

```html
`<a href="mailto:someone@example.com?subject=Hello&body=I want to know more about your services.">Send Email</a>`
```

this link will open the email client with:

- **To**: `someone@example.com`
- **Subject**: "Hello"
- **Body**: "I want to know more about your services."

```html
<a href="mailto:someone@example.com?cc=ccperson@example.com&bcc=bccperson@example.com">Email with CC and BCC</a>
```

This will:
- **CC** (Carbon Copy) to `ccperson@example.com`
- **BCC** (Blind Carbon Copy) to `bccperson@example.com`

#### 
### Summary:

- **Basic Email Link**: `mailto:someone@example.com`
- **Add Subject**: `?subject=Your%20Subject`
- **Add Body**: `&body=Your%20Message`
- **Add CC and BCC**: `&cc=email@example.com&bcc=email@example.com`

#### Telephone Links in HTML

**Telephone Links** allow users to directly make a phone call from their device
```html
<a href="tel:+1234567890">Call Us</a>
```

---

### Images in **HTML**
HTML-এ ছবি যোগ করার জন্য **`<img>`** ট্যাগ ব্যবহার করা হয়।  এই ট্যাগটির কোনো ক্লোজিং ট্যাগের প্রয়োজন হয় না।

**Add Image**

```html
<img src="image.jpg"">
```

**Fallback Description**
**`alt`**: ছবিটি লোড না হলে বা অ্যাক্সেসিবিলিটির জন্য ছবি সম্পর্কে তথ্য দেয়।

```html
<img src="flower.jpg" alt="A beautiful flower" >
```

**Image Width & Height**
- **`width`**: ছবির প্রস্থ নির্ধারণ করে (পিক্সেলে বা শতাংশে)।
- **`height`**: ছবির উচ্চতা নির্ধারণ করে (পিক্সেলে বা শতাংশে)।

```html
<img src="flower.jpg" alt="A beautiful flower" width="300" height="200">
```


### 4. **Image Paths (Relative vs. Absolute)**

**Image paths** নির্ধারণ করে কোথায় থেকে ইমেজ ফাইলটি আসবে।  Image path মূলত দুই ধরনের হতে পারে: **Relative Path** এবং **Absolute Path**।

##### **Relative Path**:

Relative path বর্তমান পেজের লোকেশন অনুসারে ইমেজের লোকেশন নির্দেশ করে।  এটি সাধারণত একই সার্ভার বা ফোল্ডারের মধ্যে ব্যবহৃত হয়।

```html
<img src="images/photo.jpg" alt="Relative Path Image">
```
এখানে `images/` ফোল্ডারের মধ্যে থাকা `photo.jpg` ছবিটি লোড হবে।

##### **Absolute Path**:

Absolute path সম্পূর্ণ URL দিয়ে ছবির সঠিক অবস্থান নির্দেশ করে, যা অন্য সার্ভার থেকেও আসতে পারে।

```html
<img src="https://www.example.com/images/photo.jpg" alt="Absolute Path Image">

```

##### Summary:

- **Image Tag (`<img>`)**: HTML ইমেজ যোগ করার ট্যাগ।
- **Image Formats**: JPEG, PNG, GIF ফরম্যাটগুলির আলাদা ব্যবহার আছে (ফটোগ্রাফের জন্য JPEG, ট্রান্সপারেন্সির জন্য PNG, অ্যানিমেশনের জন্য GIF)।
- **`alt` Attribute**: ইমেজের বিকল্প টেক্সট যা অ্যাক্সেসিবিলিটি ও SEO-এর জন্য গুরুত্বপূর্ণ।
- **Image Paths**: Relative paths বর্তমান ফোল্ডারের নির্ভরশীল, আর Absolute paths সম্পূর্ণ URL ব্যবহার করে।



#### HTML-এ মাল্টিমিডিয়া
আমরা দেখব কিভাবে `<audio>` এবং `<video>` ট্যাগ ব্যবহার করে অডিও এবং ভিডিও ফাইল যুক্ত করা যায়। চলুন সহজভাবে বুঝে নিই:

**অডিও ইম্বেড করা**

HTML-এ অডিও যুক্ত করতে হলে আমরা `<audio>` ট্যাগ ব্যবহার করি। এই ট্যাগের মাধ্যমে ব্রাউজারে অডিও ফাইল প্লে করা যায়। উদাহরণ:

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  failed to play
</audio>
```

- `controls`: অডিও প্লেয়ারের প্লে, পজ ইত্যাদি কন্ট্রোল দেখাবে।
- `autoplay`: পেজ লোড হলে অডিও স্বয়ংক্রিয়ভাবে শুরু হবে।
- `loop`: অডিও শেষ হলে আবার শুরু হবে।

**ভিডিও ইম্বেড করা**
ভিডিও যুক্ত করতে আমরা `<video>` ট্যাগ ব্যবহার করি। এর মাধ্যমে পেজে ভিডিও যুক্ত করা যায়। উদাহরণ:

```html
<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4">
  failed to play
</video>
```

- `controls`: ভিডিও প্লেয়ারের কন্ট্রোল দেখাবে।
- `autoplay`: ভিডিও স্বয়ংক্রিয়ভাবে প্লে হবে।
- `loop`: ভিডিও শেষ হলে পুনরায় প্লে হবে।


**ইউটিউব ভিডিও ইম্বেড করা**

HTML-এ ইউটিউব ভিডিও ইম্বেড করতে হলে আমরা `iframe` ট্যাগ ব্যবহার করি। উদাহরণ:\

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/video-id" frameborder="0" allowfullscreen></iframe>
```

- `src`: ইউটিউব ভিডিওর লিঙ্ক।
- `allowfullscreen`: ভিডিও ফুলস্ক্রিনে দেখার সুবিধা দেয়।

In this video, we dive into the basics of HTML tables and how to use them effectively. Learn how to create a table using the `<table>`, `<tr>`, `<th>`, and `<td>` tags, as well as how to add headers, borders, and customize table styles with CSS. We'll also cover how to merge cells using `colspan` and `rowspan`. Whether you're a beginner or brushing up on HTML, this tutorial from Programming with Rakib will guide you step-by-step. Don't forget to subscribe for more web development tutorials!