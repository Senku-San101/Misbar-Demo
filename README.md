

<div align="center">
  <img src="icons/icon128.png" alt="Misbar Logo" width="128" />
  <h1>Misbar - مِسبَار</h1>
</div>

(اللغة العربية في أسقل الصفحة)





> **Disclamer : **
This is only the Free version. Paid version includes 25+ advanced features, including AI assisstant, Crawling, Interceptor Breakpoints, and much more...
To get it, get in touch with me through my links or the  website mail in here : https://abdulrahmankamal.netlify.app
> 

<br>

<br>

<br>
**Misbar** is a powerful, browser-native security testing extension designed for penetration testers, bug bounty hunters, and security researchers. Integrating directly into your browser's Developer Tools, Misbar provides a lightweight and immediate interface to intercept, modify, replay, and manipulate HTTP requests, removing the need to switch between external proxy tools like Burp Suite or ZAP during active testing.
## 🚀 Key Features
*   **Real-time Request Interception:** Pause inbound/outbound HTTP requests to inspect, modify, or drop them before they reach the server.
*   **Advanced Repeater:** Forward captured requests to a dedicated replay interface, allowing you to tweak headers, body, and methods and observe the raw server response.
*   **Integrated Payload Library:** Built-in collection of common attack vectors for XSS, SQLi, SSTI, and more. Quickly copy or send pre-loaded payloads.
*   **Custom Payload Management:** Create, edit, organize, and recategorize your own custom payloads dynamically within the UI.
*   **Inline Encoder/Decoder:** Instant encoding and decoding of text across multiple formats, including Base64, URL, Hex, HTML Entities, and JWT.
---
## 📸 Walkthrough & Feature Details
### 1. Traffic Interception & Flow Control

**Detailed Explanation:** Misbar operates as a MITM (Man-in-the-Middle) proxy within the browser. When the **"Intercept: ON"** switch is toggled, Misbar halts network requests, preventing resources (like images or API responses) from loading on the frontend. As shown in the screenshot, the UI indicates an active interception (`Debugger attached`), and the application's image fails to render because the `GET` request is paused for manual inspection.
### 2. Forwarding Requests & Resuming Load

**Detailed Explanation:** Once a security tester has inspected the paused request, they can simply **forward** it to the target server. The screenshot demonstrates the result: the previously blocked image successfully loads on the application interface, confirming that the interception process is non-destructive and completely reversible.
### 3. The Request Editor (Forward, Drop, Repeater)

**Detailed Explanation:** Clicking **"Edit & Send"** on an intercepted request opens a comprehensive editor. This window provides a complete breakdown of the HTTP request, including the Method (`POST`), Target URL, Request Headers, and Body. From here, you have three crucial actions:
*   **Forward:** Send the request exactly as it currently sits.
*   **Drop X:** Abandon the request completely so it never reaches the server.
*   **Repeater:** Forward the current request to the dedicated _Repeater_ tab for persistent testing and manipulation.
### 4. The Repeater Module (Response Analysis)

**Detailed Explanation:** The **Repeater** is one of the most critical tools for manual testing. It allows you to view the raw server response to your modified requests. As seen in the image, the system displays the `STATUS` code (e.g., 400 Bad Request), response `TIME`, payload `SIZE`, and the raw HTML body. Users can repeatedly tweak the body or headers on the left and hit `Send` to launch the request again, ideal for fuzzing, path traversal, or testing WAF bypasses.
### 5. Pre-built Payload Library

**Detailed Explanation:** Misbar ships with a built-in **Payload Library**, pre-categorized into common vulnerability types such as XSS (Basic Script, SVG Onload), SQLi (Basic OR, Union Select, Time-Based), and SSTI (Jinja2). Each card features quick-action buttons: **Copy** (to instantly clone the payload to your clipboard for use elsewhere), **Send** (to push the payload directly into the Repeater body), **Edit**, and **Delete**.
### 6. Creating Custom Payloads

**Detailed Explanation:** Recognizing that pre-built lists are rarely enough for complex engagements, Misbar features a **Custom Payload** creator. This modal allows users to assign a descriptive name to their payload, select an existing category (such as "XSS"), and paste custom code or exploitation strings.
### 7. Instant Library Integration

**Detailed Explanation:** Upon clicking **Save**, the custom payload is instantly generated and visually inserted into the selected category section of the Payload Library. It mimics the exact structure of the built-in payloads, ensuring it is immediately available for reuse with the same Copy, Send, Edit, and Delete controls.
### 8. Dynamic Payload Management & Re-categorization

**Detailed Explanation:** Misbar's payload system is fully editable. By clicking the **Edit** button on a custom payload, users can not only modify the payload's code but also relocate it to a completely different category. The screenshot shows a payload (originally created in XSS) being edited and moved into the **SQL** category, showcasing the tool's adaptability to a user's evolving workflow.
### 9. Direct Payload Injection into Repeater

**Detailed Explanation:** This view demonstrates how the Payload Library interacts with the Repeater. The tester can push a `Payload content` variable or a specific XSS/SQL payload directly into the request body of an active test case. This automation saves time by allowing testers to cycle through various payload vectors without manually retyping them.
### 10. Integrated Encoder/Decoder Suite

**Detailed Explanation:** Misbar includes a robust cryptography and formatting utility panel. Testers can leverage this to quickly encode or decode strings for testing. The dropdown menu provides support for:
*   URL Encode / Decode
*   Base64 Encode / Decode
*   Hex Encode / Decode
*   HTML Entity Encode / Decode
*   JWT DecodeAs shown in the screenshot, entering "Hello" and selecting "Base64 Encode" instantly outputs `SGVsbG8=`, allowing for quick on-the-fly data manipulation.
---
## 📦 Installation (Chrome Extension)
Since Misbar runs as a Developer Tool extension, follow these steps to install it locally:
1.  Clone or download this repository to your local machine.
1.  Open your Chromium-based browser (Google Chrome, Brave, Microsoft Edge, etc.).
1.  Navigate to the Extensions management page: `chrome://extensions`.
1.  Toggle **Developer mode** on (usually located in the top right corner).
1.  Click the **Load unpacked** button.
1.  Select the folder containing the Misbar source code.
1.  Open your browser's Developer Tools (**F12** or **Right Click > Inspect**) and look for the newly added **Misbar** tab.
---
## 💻 Usage Guide
1.  **Starting a Test:** Navigate to your target web application and open the Developer Tools > **Misbar** tab.
1.  **Interception:** Toggle the `Intercept: ON` switch in the main dashboard.
1.  **Editing:** When a request is intercepted, click **Edit & Send** to view the raw HTTP data.
1.  **Replaying:** Forward a request to the **Repeater** to edit and resend it multiple times while viewing the server's specific response codes and bodies.
1.  **Expanding:** If you need a specific payload for a proprietary vulnerability, use the **Payloads** tab to add it to your library.
---
<br>
<br>
<br>
<br>
<br>

<br>
<br>


> **ملاحظة:** هذه هي النسخة **المجانية** فقط.  
> بينما تتضمن النسخة **المدفوعة** أكثر من **٢٥ ميزة متقدمة**، تشمل:
> - مساعد الذكاء الاصطناعي (AI Assistant)
> - الزحف الآلي (Crawling)
> - نقاط توقف الاعتراض المتقدمة (Interceptor Breakpoints)
> - وغيرها الكثير...

للحصول على النسخة المدفوعة، يمكنك التواصل معي عبر روابط التواصل الخاصة بي، أو عبر بريد الموقع الرسمي هنا:  
[https://abdulrahmankamal.netlify.app](https://abdulrahmankamal.netlify.app)



<br>

<br>

<br>

**مِسبَار** هي أداة قوية ومدمجة لاختبار الأمان داخل المتصفح، مصممة خصيصاً لمختبرين الاختراق، وصائدي الثغرات، والباحثين في مجال الأمن السيبراني. من خلال التكامل المباشر مع أدوات المطور (Developer Tools) في المتصفح، توفر مِسبَار واجهة خفيفة وفورية لاعتراض، وتعديل، وإعادة إرسال، ومعالجة طلبات HTTP، مما يلغي الحاجة إلى التبديل بين أدوات البروكسي الخارجية مثل Burp Suite أو ZAP أثناء الاختبارات النشطة.

## 🚀 الميزات الرئيسية
-   **اعتراض الطلبات في الوقت الحقيقي:** إيقاف طلبات HTTP الواردة والصادرة مؤقتاً لفحصها، أو تعديلها، أو إسقاطها قبل وصولها إلى الخادم.
-   **أداة التكرار المتقدمة (Advanced Repeater):** إعادة توجيه الطلبات المحتجزة إلى واجهة تكرار مخصصة، مما يتيح لك تعديل الرؤوس (Headers)، ومحتوى الجسم (Body)، وطرق الإرسال، ومشاهدة استجابة الخادم الأولية.
-   **مكتبة الحمولات المدمجة (Integrated Payload Library):** مجموعة جاهزة من نواقل الهجوم الشائعة لاختبارات XSS، وSQLi، وSSTI، وغيرها. إمكانية نسخ أو إرسال الحمولات المُعدّة مسبقاً بسرعة.
-   **إدارة الحمولات المخصصة:** إنشاء، وتعديل، وتنظيم، وإعادة تصنيف الحمولات المخصصة الخاصة بك ديناميكياً من خلال واجهة المستخدم.
-   **أداة التشفير وفك التشفير المضمنة (Encoder/Decoder):** تشفير وفك تشفير النصوص بشكل فوري عبر صيغ متعددة، تتضمن Base64، وURL، وHex، وHTML Entities، وJWT.

---
## 📸 شرح تفصيلي للميزات والوظائف

### 1. اعتراض حركة المرور والتحكم في التدفق

**الشرح التفصيلي:** تعمل أداة مِسبَار كبروكسي وسيط (MITM) داخل المتصفح. عند تفعيل مفتاح **"Intercept: ON"**، تقوم مِسبَار بإيقاف طلبات الشبكة مؤقتاً، مما يمنع تحميل الموارد (مثل الصور أو استجابات واجهات برمجة التطبيقات) في الواجهة الأمامية. كما هو موضح في لقطة الشاشة، تشير الواجهة إلى وجود اعتراض نشط (`Debugger attached`)، وتفشل صورة التطبيق في الظهور لأنه تم إيقاف طلب `GET` مؤقتاً للفحص اليدوي.

### 2. إعادة توجيه الطلبات واستئناف التحميل

**الشرح التفصيلي:** بمجرد أن يقوم مختبر الأمن بفحص الطلب المتوقف، يمكنه ببساطة **إعادة توجيهه (Forward)** إلى الخادم المستهدف. توضح لقطة الشاشة النتيجة: حيث يتم تحميل الصورة التي تم حظرها سابقاً بنجاح على واجهة التطبيق، مما يؤكد أن عملية الاعتراض غير تدميرية وقابلة للعكس تماماً.

### 3. محرر الطلبات (إعادة توجيه، إسقاط، تكرار)

**الشرح التفصيلي:** يؤدي الضغط على **"Edit & Send"** على طلب معترض إلى فتح محرر شامل. توفر هذه النافذة تحليلاً كاملاً لطلب HTTP، بما في ذلك الطريقة (`POST`)، وعنوان URL المستهدف، ورؤوس الطلبات، ومحتوى الجسم. من هنا، تتوفر لديك ثلاثة إجراءات حاسمة:
-   **Forward (إعادة التوجيه):** إرسال الطلب كما هو تماماً في حالته الحالية.
-   **Drop X (الإسقاط):** التخلي عن الطلب تماماً بحيث لا يصل إلى الخادم مطلقاً.
-   **Repeater (التكرار):** إعادة توجيه الطلب الحالي إلى علامة التبويب المخصصة _للتكرار (Repeater)_ لاختبار ومعالجة مستمرة.

### 4. وحدة التكرار (تحليل الاستجابة)

**الشرح التفصيلي:** تعتبر أداة **التكرار (Repeater)** واحدة من أهم الأدوات للاختبار اليدوي. فهي تتيح لك رؤية استجابة الخادم الأولية لطلباتك المعدلة. كما يظهر في الصورة، يعرض النظام رمز `STATUS` الحالة (مثل 400 طلب غير صحيح)، وزمن الاستجابة `TIME`، وحجم الحمولة `SIZE`، ونص HTML الخام. يمكن للمستخدمين تعديل المحتوى أو الرؤوس في الجانب الأيسر بشكل متكرر والضغط على `Send` لإطلاق الطلب مرة أخرى، وهو أمر مثالي لاختبارات التزوير (Fuzzing)، أو اجتياز المسار (Path Traversal)، أو اختبار تجاوز جدار الحماية (WAF bypass).

### 5. مكتبة الحمولات الجاهزة (Pre-built Payload Library)

**الشرح التفصيلي:** تأتي مِسبَار مزودة بـ **مكتبة حمولات (Payload Library)** مضمنة، مصنفة مسبقاً حسب أنواع الثغرات الشائعة مثل XSS (نصوص أساسية، تحميل SVG)، و SQLi (OR أساسي، Union Select، استناد للزمن)، و SSTI (Jinja2). تحتوي كل بطاقة على أزرار إجراءات سريعة: **Copy (نسخ)** (لاستنساخ الحمولة إلى الحافظة لاستخدامها في مكان آخر)، و**Send (إرسال)** (لدفع الحمولة مباشرة إلى جسم أداة التكرار)، و**Edit (تعديل)**، و**Delete (حذف)**.

### 6. إنشاء حمولات مخصصة

**الشرح التفصيلي:** إدراكاً من الأداة بأن القوائم الجاهزة نادراً ما تكون كافية للاختبارات المعقدة، توفر مِسبَار أداة إنشاء **حمولات مخصصة (Custom Payload)**. تسمح هذه النافذة المنبثقة للمستخدمين بإعطاء اسم وصفي للحمولة الخاصة بهم، واختيار فئة موجودة (مثل "XSS")، ولصق الأكواد أو سلاسل الاستغلال المخصصة.

### 7. الدمج الفوري مع المكتبة

**الشرح التفصيلي:** عند الضغط على **Save (حفظ)**، يتم إنشاء الحمولة المخصصة فورياً وإدراجها بصرياً داخل قسم الفئة المحددة في مكتبة الحمولات. وهي تحاكي البنية الدقيقة للحمولات المدمجة، مما يضمن إتاحتها للاستخدام الفوري مع نفس أدوات التحكم (نسخ، إرسال، تعديل، حذف).

### 8. الإدارة الديناميكية وإعادة تصنيف الحمولات

**الشرح التفصيلي:** نظام الحمولات في مِسبَار قابل للتعديل بالكامل. من خلال الضغط على زر **Edit (تعديل)** في حمولة مخصصة، لا يمكن للمستخدمين تعديل كود الحمولة فقط، بل يمكنهم أيضاً نقلها إلى فئة مختلفة تماماً. توضح لقطة الشاشة حمولة (تم إنشاؤها أصلاً ضمن XSS) يتم تعديلها ونقلها إلى فئة **SQL**، مما يبرز قدرة الأداة على التكيف مع سير عمل المستخدم المتطور.

### 9. إدخال الحمولة مباشرة في أداة التكرار

**الشرح التفصيلي:** يوضح هذا العرض كيفية تفاعل مكتبة الحمولات مع أداة التكرار (Repeater). يمكن للمختبر دفع متغير `Payload content` أو حمولة XSS/SQL محددة مباشرة إلى محتوى جسم الطلب لحالة اختبار نشطة. توفر هذه الأتمتة الوقت من خلال السماح للمختبرين بالتدرج عبر ناقلات الحمولات المختلفة دون الحاجة إلى إعادة كتابتها يدوياً.

### 10. مجموعة التشفير وفك التشفير المدمجة

**الشرح التفصيلي:** تتضمن مِسبَار لوحة أدوات قوية للتشفير الصريح وتنسيق البيانات. يمكن للمختبرين الاستفادة منها لتشفير أو فك تشفير السلاسل بسرعة لاختبارها. توفر القائمة المنسدلة دعماً لـ:
-   تشفير / فك تشفير URL
-   تشفير / فك تشفير Base64
-   تشفير / فك تشفير Hex
-   تشفير / فك تشفير كيانات HTML (HTML Entity)
-   فك تشفير JWT
كما هو مبين في لقطة الشاشة، إدخال كلمة "Hello" واختيار "Base64 Encode" ينتج عنه فوراً `SGVsbG8=`، مما يتيح إجراء معالجة سريعة للبيانات أثناء التنقل.

---
## 📦 التثبيت (إضافة لمتصفح كروم)
بما أن مِسبَار تعمل كإضافة لأدوات المطور، اتبع هذه الخطوات لتثبيتها محلياً:
1.  استنساخ (Clone) أو تحميل هذا المستودع إلى جهازك المحلي.
2.  افتح المتصفح المبني على كروميوم (Google Chrome، Brave، Microsoft Edge، وغيرها).
3.  انتقل إلى صفحة إدارة الإضافات: `chrome://extensions`.
4.  قم بتفعيل **وضع المطور (Developer mode)** (يوجد عادةً في الزاوية العلوية اليمنى).
5.  انقر على زر **Load unpacked** (تحميل حزمة غير مضغوطة).
6.  اختر المجلد الذي يحتوي على الكود المصدري لـ مِسبَار.
7.  افتح أدوات المطور في متصفحك (**F12** أو **زر الفأرة الأيمن > فحص**) وابحث عن علامة التبويب الجديدة **Misbar**.

---
## 💻 دليل الاستخدام
1.  **بدء الاختبار:** انتقل إلى تطبيق الويب المستهدف وافتح أدوات المطور > علامة التبويب **Misbar**.
2.  **الاعتراض:** قم بتفعيل مفتاح `Intercept: ON` في لوحة التحكم الرئيسية.
3.  **التعديل:** عند اعتراض طلب، انقر على **Edit & Send** لعرض بيانات HTTP الخام.
4.  **إعادة الإرسال (Replaying):** أعد توجيه طلب إلى أداة **Repeater** لتعديله وإعادة إرساله عدة مرات مع مراقبة رموز استجابة الخادم ومحتوياته المحددة.
5.  **التوسع:** إذا كنت بحاجة إلى حمولة معينة لثغرة خاصة، استخدم علامة التبويب **Payloads** لإضافتها إلى مكتبتك.
---
