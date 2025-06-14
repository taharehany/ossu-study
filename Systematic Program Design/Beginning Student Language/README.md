## Beginning Student Language

#### Overview of the Module

This module introduces Beginning Student Language (BSL), a simple and minimal programming language used throughout the course. It provides a foundation to focus on learning the design method rather than complex syntax. BSL also shares core features with most other programming languages, making it easier to transfer your skills in the future.

يقدم هذا الجزء لغة البرمجة BSL، وهي لغة بسيطة ومحدودة تُستخدم خلال الكورس. هدفها هو تسهيل التركيز على منهج التصميم بدلًا من الانشغال بتعقيدات الصياغة. وتتميز BSL بأنها تشترك في الأساسيات مع معظم لغات البرمجة الأخرى، مما يسهل نقل المهارات مستقبلًا.

---

#### Course Audience

This course is mainly designed for students with no prior programming experience. The videos in this module are paced accordingly and cover both the language and the tools used. Students are advised not to skip or skim the material.

الكورس موجه أساسًا للطلاب الذين لم يبرمجوا من قبل، لذا تم تنظيم الفيديوهات بما يناسب هذا المستوى. وتشمل الشرح لكل من اللغة والأدوات المستخدمة. يُنصح بعدم تجاوز هذا المحتوى أو التسرع فيه.

---

#### A Note for Experienced Programmers

If you’ve programmed before, this module may feel easy—but don’t underestimate it. While BSL is conceptually similar to many languages, it also differs in important ways. It's crucial to understand it fully.

إذا كنت قد برمجت من قبل، فقد يبدو هذا الجزء سهلًا—لكن لا تستهين به. على الرغم من أن BSL تشترك مفاهيميًا مع لغات كثيرة، إلا أن لها اختلافات مهمة يجب فهمها جيدًا.

---

#### Estimated Time

Working through the videos and practice materials in this module should take around 5 to 8 hours of focused effort.

من المتوقع أن يستغرق إتمام الفيديوهات والمواد التدريبية في هذا الجزء حوالي 5 إلى 8 ساعات من الجهد المركز.

---

#### Learning Goals

- Write expressions using primitive data types (numbers, strings, images, booleans).  
- Define constants and functions.  
- Trace step-by-step evaluation of simple expressions.  
- Use the stepper tool to automate evaluation tracing.  
- Use DrRacket’s help desk to discover new primitives.

<br>

- كتابة تعبيرات باستخدام أنواع البيانات الأولية مثل الأرقام، السلاسل النصية، الصور، والقيم المنطقية.  
- تعريف الثوابت والدوال.  
- تتبع خطوات تقييم التعبيرات البسيطة يدويًا.  
- استخدام أداة "Stepper" لتتبع التقييم تلقائيًا.  
- استخدام مركز المساعدة في DrRacket لاكتشاف الدوال الأولية الجديدة.



## Expressions and Primitives in BSL

#### Learning the Basics

Before building complex programs like games or web apps, we must learn the basic building blocks. This section introduces simple expressions and primitive operations using Beginning Student Language (BSL).

<br>
قبل ما نبدأ نصمم برامج معقدة زي الألعاب أو تطبيقات الويب، لازم نتعلم الأساسيات. الجزء ده بيقدم التعبيرات البسيطة والعمليات الأولية باستخدام لغة BSL.

---

#### Getting Started with DrRacket

* When you open DrRacket, ensure it's set to **Beginning Student Language** (BSL). If not, go to `Language > Choose Language`, expand `How to Design Programs`, and pick **Beginning Student**.
* DrRacket has two areas:

  * **Definitions Area** (top): where you write code.
  * **Interaction Area** (bottom): where results appear after running.

<br>

* عند فتح DrRacket، تأكد إن اللغة المحددة هي BSL. لو مش موجودة، اخترها من `Language > Choose Language` تحت قسم `How to Design Programs`.
* البرنامج فيه منطقتين:

  * **منطقة التعريفات** (أعلى): لكتابة الكود.
  * **منطقة التفاعل** (أسفل): لعرض النتائج.

---

#### Writing Expressions

In BSL, arithmetic expressions follow the format:

```scheme
(+ 3 4) ;; This adds 3 and 4, returns 7
(* 2 3) ;; Multiplies 2 and 3
(+ 3 (* 2 3)) ;; Nested expressions, returns 9
(/ 12 (* 2 3)) ;; Divides 12 by 6, returns 2
```

Rules:

* Expressions start with an open parenthesis `(`.
* Then comes the operator: `+`, `-`, `*`, `/`.
* Followed by one or more operands (numbers or other expressions).
* Ends with a closing parenthesis `)`.

<br>
في BSL، التعبيرات الحسابية تتبع الصيغة:

```scheme
(+ 3 4) ;; جمع 3 و 4
(* 2 3) ;; ضرب 2 في 3
(+ 3 (* 2 3)) ;; تعبير متداخل، الناتج 9
(/ 12 (* 2 3)) ;; قسمة 12 على 6، الناتج 2
```

القواعد:

* تبدأ التعبيرات بـ `(`
* بعدها العامل `+` أو `*` أو غيره
* ثم المعاملات (أرقام أو تعبيرات أخرى)
* وتنتهي بـ `)`

---

#### Comments in DrRacket

* Use `;` to comment out a single line.
* To comment multiple lines: select them, right-click → Comment Out with Semicolons.
* You can also use **comment boxes** from `Insert > Comment Box`, even containing images.

<br>

* استخدم `;` للتعليق على سطر واحد.
* لتعليق عدة أسطر: حددها واختر "Comment Out with Semicolons".
* يمكن استخدام **مربعات التعليق** من قائمة Insert، وتقدر تضيف فيها صور.

---

#### More Numeric Operations

* `sqr`: squares a number
* `sqrt`: square root

Examples:

```scheme
(sqr 3)    ;; returns 9
(sqrt 16)  ;; returns 4
```

<br>

* `sqr`: تربيع الرقم
* `sqrt`: الجذر التربيعي

أمثلة:

```scheme
(sqr 3)    ;; الناتج 9
(sqrt 16)  ;; الناتج 4
```

---

#### Practice Exercise

Try writing some expressions in DrRacket using the primitives you've learned. Test them using the "Run" button and observe the results in the Interaction Area.

<br>
جرب تكتب تعبيرات بنفسك في DrRacket باستخدام العمليات اللي اتعلمتها. اضغط "Run" وشوف النتائج في منطقة التفاعل.

---

## Evaluation Rules in BSL

#### Why Evaluation Rules Matter

Even simple expressions like `(+ 1 2)` follow specific rules during evaluation. While that may seem excessive, it becomes essential when dealing with large, real-world programs like those with millions of lines of code. Understanding the evaluation rules helps us reason about and debug complex programs effectively.

<br>

حتى التعبيرات البسيطة مثل `(+ 1 2)` تتبع قواعد محددة أثناء التقييم. رغم إن ده ممكن يبدو مبالغ فيه، لكنه ضروري لما نتعامل مع برامج ضخمة. فهم القواعد دي بيساعدنا نفهم ونحل مشاكل البرامج المعقدة.

---

#### Primitive Calls: Terminology

An expression like `(+ 3 (* 3 4) (- (+ 1 2) 3))` is a **primitive call**:

* `+` is the **operator**.
* Everything after it (`3`, `(* 3 4)`, and `(- (+ 1 2) 3)`) are **operands**.

Each operand can itself be another primitive call.

<br>

تعبير زي `(+ 3 (* 3 4) (- (+ 1 2) 3))` اسمه **نداء أولي (primitive call)**:

* `+` هو **المُعامل**.
* والباقي (`3`, `(* 3 4)`, `(- (+ 1 2) 3)`) هما **المعاملات**.

وكل مُعامل ممكن يكون نداء أولي آخر.

---

#### Step-by-Step Evaluation Process

Evaluation follows a rule: **all operands must first be evaluated into values**.

For example:

```scheme
(+ 3 (* 3 4) (- (+ 1 2) 3))
```

Step-by-step:

1. `(* 3 4)` → `12`
2. `(+ 1 2)` → `3`
3. `(- 3 3)` → `0`
4. `(+ 3 12 0)` → `15`

So the entire expression evaluates to `15`.

<br>

عملية التقييم بتتبع قاعدة: **كل المعاملات لازم تتقيم (تتحول لقيم) قبل تنفيذ العملية**.

مثال:

```scheme
(+ 3 (* 3 4) (- (+ 1 2) 3))
```

خطوة بخطوة:

1. `(* 3 4)` → `12`
2. `(+ 1 2)` → `3`
3. `(- 3 3)` → `0`
4. `(+ 3 12 0)` → `15`

---

#### Evaluation Order Intuition

BSL uses **left-to-right** and **inside-out** evaluation:

* Left to right: `(* 3 4)` is evaluated before `(- (+ 1 2) 3)`.
* Inside to outside: `(+ 1 2)` happens before `(- ... 3)`.

<br>

BSL بتستخدم ترتيب تقييم:

* **من اليسار لليمين**: نبدأ بـ `(* 3 4)` قبل `(- (+ 1 2) 3)`.
* **من الداخل للخارج**: `(+ 1 2)` قبل `(- ... 3)`.

---

#### Summary

* A **primitive call** is an expression that starts with an operator and is followed by operands.
* **Evaluation rule**: evaluate all operands to values first, then apply the operator.
* Order: **left to right** and **inside to outside**.

We only need a few evaluation rules in BSL to handle complex programs. This simplicity lets us focus more on **design**, not just the language.

<br>


* **النداء الأولي** هو تعبير بيبدأ بمعامل، يليه معاملات.
* **قاعدة التقييم**: نقيم كل المعاملات الأول، ثم نطبق العملية.
* الترتيب: **من اليسار لليمين** و **من الداخل للخارج**.

بس شوية قواعد بسيطة كفاية عشان نبرمج برامج معقدة، وده بيسمح لينا نركز أكتر على **تصميم البرنامج** نفسه.


## Strings and Images in BSL

#### Introducing New Data Types

In addition to numbers, BSL supports other primitive data types like **strings** and **images**. These allow us to represent words, names, and pictures, expanding what we can build.

**بالعربي:**
بالإضافة للأرقام، لغة BSL تدعم أنواع بيانات أولية تانية زي **السلاسل النصية (Strings)** و**الصور (Images)**. الأنواع دي بتسمح لينا نمثل كلمات وأسماء وصور، وده بيوسع قدراتنا في البرمجة.

---

#### Strings in BSL

* A string is any sequence of characters wrapped in double quotes, like:

```scheme
"apple"
"Ada"
```

* Strings are **values** — running the expression returns the string itself.

* We can use `string-append` to combine multiple strings:

```scheme
(string-append "Ada" " " "Lovelace") ;; returns "Ada Lovelace"
```

**بالعربي:**

* السلسلة النصية (String) هي أي مجموعة حروف بين علامتي اقتباس مزدوجة:

```scheme
"apple"
"Ada"
```

* السلاسل النصية قيم بحد ذاتها.
* نقدر نستخدم `string-append` لدمج سلاسل نصية:

```scheme
(string-append "Ada" " " "Lovelace") ;; الناتج "Ada Lovelace"
```

---

#### Strings vs Numbers

Even if a string contains digits, it’s still not a number:

```scheme
"123" ;; a string
123   ;; a number
```

* You can add numbers:

```scheme
(+ 123 1) ;; returns 124
```

* But adding strings with numbers causes an error:

```scheme
(+ "123" 1) ;; ERROR
```

---

#### String Operations

* **string-length**: Returns number of characters in a string.

```scheme
(string-length "apple") ;; returns 5
```

* **substring**: Extracts part of a string using **zero-based indexing**.

```scheme
(substring "caribou" 2 4) ;; returns "ri"
```

Explanation:

* Indexing starts at 0.
* So index 2 = third character, and we stop **before** index 4.

---

#### Common Mistake: Off-by-One Errors

* Because of zero-based indexing, beginners often include or skip a wrong character.
* To avoid mistakes, try writing out a helper string like:

```scheme
"0123456"
```

Line it up with the actual string to visually see character positions.

**بالعربي:**
غالبًا المبتدئين بيغلطوا في تحديد الحروف بسبب الترقيم من الصفر. عشان تتجنب الخطأ، ممكن تكتب سلسلة زي:

```scheme
"0123456"
```

وحطها تحت السلسلة الأصلية عشان تشوف أماكن الحروف.

---

#### Dealing with Errors

Making mistakes like mixing strings and numbers is normal. Racket provides error messages that show where the issue is. Use them to fix your code.

**بالعربي:**
الخطأ جزء طبيعي من البرمجة، خصوصًا أثناء التعلم. Racket بيعرض رسالة الخطأ ويوضح مكانها، فاستفد منها لتصحيح الكود.

---
