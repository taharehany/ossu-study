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
---

## Evaluation Rules in BSL

#### Why Evaluation Rules Matter

Even simple expressions like `(+ 1 2)` follow specific rules during evaluation. While that may seem excessive, it becomes essential when dealing with large, real-world programs like those with millions of lines of code. Understanding the evaluation rules helps us reason about and debug complex programs effectively.

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

<br>
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

<br>

* السلسلة النصية (String) هي أي مجموعة حروف بين علامتي اقتباس مزدوجة:
* السلاسل النصية قيم بحد ذاتها.
* نقدر نستخدم `string-append` لدمج سلاسل نصية:
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

<br>
غالبًا المبتدئين بيغلطوا في تحديد الحروف بسبب الترقيم من الصفر. عشان تتجنب الخطأ، ممكن تكتب سلسلة

وحطها تحت السلسلة الأصلية عشان تشوف أماكن الحروف.

---

#### Dealing with Errors

Making mistakes like mixing strings and numbers is normal. Racket provides error messages that show where the issue is. Use them to fix your code.

<br>
الخطأ جزء طبيعي من البرمجة، خصوصًا أثناء التعلم. Racket بيعرض رسالة الخطأ ويوضح مكانها، فاستفد منها لتصحيح الكود.

---


## Strings and Images in BSL

#### String Basics

In BSL, strings are sequences of characters enclosed in double quotes:

```scheme
"apple"
"Ada"
```

These are values, just like numbers. When run, they return themselves.

<br>
في BSL، السلاسل النصية (Strings) هي مجموعة من الحروف بين علامتي تنصيص مزدوجتين:

```scheme
"apple"
"Ada"
```

دي قيم زيها زي الأرقام. لما بتشغلها، بترجع نفسها.

---

#### String Operations

You can concatenate strings using `string-append`:

```scheme
(string-append "Ada" " " "Lovelace") ;; => "Ada Lovelace"
```

Note:

* Strings that contain digits (e.g., "123") are still strings, not numbers.
* You can't perform arithmetic on them unless converted.

```scheme
(+ 123 1) ;; => 124
(+ "123" 1) ;; Error: string used where number expected
```

<br>

تقدر تربط سلاسل نصية مع بعض باستخدام `string-append`:

```scheme
(string-append "Ada" " " "Lovelace") ;; الناتج "Ada Lovelace"
```

ملاحظات:

* السلاسل اللي فيها أرقام (زي "123") تفضل Strings مش أرقام.
* مينفعش تعمل عليهم عمليات حسابية.

---

#### String Utilities

* `string-length`: returns the number of characters in the string.
* `substring`: extracts part of a string based on **zero-based indexing**.

Example:

```scheme
(string-length "apple") ;; => 5
(substring "caribou" 2 4) ;; => "ri"
(substring "caribou" 0 3) ;; => "car"
```

<br>

* `string-length`: بيرجع عدد الحروف.
* `substring`: بيطلع جزء من السلسلة حسب الترقيم اللي بيبدأ من صفر.

مثال:

```scheme
(string-length "apple") ;; الناتج 5
(substring "caribou" 2 4) ;; الناتج "ri"
(substring "caribou" 0 3) ;; الناتج "car"
```

---

#### Image Basics

To use image functions, start your file with:

```scheme
(require 2htdp/image)
```

Common primitives to create images:

```scheme
(circle 30 "solid" "red")
(rectangle 50 100 "outline" "blue")
(text "Hello" 24 "orange")
```

---

#### Image Combinations

Use the following functions to combine images:

* `above`: stack images vertically.
* `beside`: place images side by side.
* `overlay`: place images on top of each other.

Example:

```scheme
(above
 (circle 10 "solid" "red")
 (circle 20 "solid" "green")
 (circle 30 "solid" "blue"))
```

<br>

الدمج بين الصور:

* `above`: يرص الصور فوق بعض.
* `beside`: يحط الصور جنب بعض.
* `overlay`: يحط الصور فوق بعض في نفس المكان.
---


## Constant Definitions in BSL

#### Introduction

In previous lessons, we learned how to use different types of values—numbers, strings, and images—and how to write expressions to manipulate them.

**بالعربي:**
في الدروس السابقة تعلمنا كيفية استخدام أنواع مختلفة من القيم مثل الأرقام والسلاسل النصية والصور، وكيفية كتابة تعبيرات لمعالجتها.

---

## Why Use Constant Definitions?

Constants give names to values, making code easier to read and change. These two features—**readability** and **changeability**—are among the most important traits of good code.

**بالعربي:**
الثوابت تمنح القيم أسماء، مما يجعل الكود أسهل في القراءة والتعديل. وهذان العاملان (قابلية القراءة وقابلية التعديل) من أهم خصائص الكود الجيد.

---

## Syntax of Constant Definition

```racket
(define WIDTH 400)
(define HEIGHT 600)
```

Constants do not immediately produce output but can be used in expressions. For example:

```racket
(* WIDTH HEIGHT)
```

This will evaluate to:

* First step: `WIDTH` → `400`
* Second step: `HEIGHT` → `600`
* Final result: `(* 400 600)` → `240000`

**بالعربي:**
الثوابت لا تنتج ناتجًا مباشرة، ولكن يمكن استخدامها داخل تعبيرات.

---

## Rules for Defining Constants

* Use `(define NAME value)` format.
* Names can contain letters, digits, and certain symbols like `!`, `?`, `=`.
* Cannot contain parentheses `(` `)` or quotes `"`.
* A constant can only be defined once. Attempting to redefine it causes an error.

---

## Example with Images

You can define constants for images:

```racket
(define CAT <inserted cat image>)
```

Then use expressions like:

```racket
(define RCAT (rotate -10 CAT))
(define LCAT (rotate 10 CAT))
```

This defines:

* `RCAT`: the cat rotated right
* `LCAT`: the cat rotated left

---

#### How to Define Constants

Use the `define` form:

```racket
(define CONSTANT-NAME value)
```

Example:

```racket
(define WIDTH 400)
(define HEIGHT 600)
(* WIDTH HEIGHT) ; => 240000
```

#### Rules and Naming

* Constant names are typically in UPPERCASE.
* Names can include letters, digits, `!`, `?`, `=`, etc.
* Cannot contain parentheses or quotes.

#### Example with Images

You can define a constant that stores an image value:

```racket
(define CAT (image "🐱")) ; using pasted image from editor
(define RCAT (rotate -10 CAT))
(define LCAT (rotate 10 CAT))
```

#### Final Note

Once defined, a constant's value cannot be changed. Attempting to redefine it will result in an error.

بمجرد تعريف الثابت، لا يمكن تغييره. إذا حاولت تعريفه مرة أخرى بنفس الاسم، سيظهر خطأ.

Constant definitions let us name values once and reuse them throughout the program. This improves clarity and maintainability.

تعريف الثوابت يسمح لنا بتسمية القيم مرة واحدة وإعادة استخدامها في أجزاء متعددة من البرنامج، مما يحسّن الوضوح وسهولة التعديل.