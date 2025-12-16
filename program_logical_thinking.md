<div dir="rtl">

# ما هو البرنامج؟ 🧠

## المحتويات

- [المفهوم الأساسي](#المفهوم-الأساسي)
- [من ناحية التفكير المنطقي](#من-ناحية-التفكير-المنطقي)
- [من ناحية اللغة البرمجية](#من-ناحية-اللغة-البرمجية)
- [البرنامج في Android](#البرنامج-في-android)
- [أمثلة عملية](#أمثلة-عملية)
- [المشاكل الشائعة](#المشاكل-الشائعة)
- [الخلاصة](#الخلاصة)

---

## المفهوم الأساسي 🎯

### التعريف البسيط:

**البرنامج** هو مجموعة من **التعليمات المرتبة** التي تُنفّذ **بتسلسل محدد** لتحويل **مدخلات (Input)** إلى **مخرجات (Output)** من خلال **معالجة (Processing)**.

<div dir="ltr">

```
┌─────────────────────────────────────────┐
│         Program Execution Flow          │
├─────────────────────────────────────────┤
│                                         │
│  Input  ──→  Processing  ──→  Output   │
│                                         │
│  البيانات      المعالجة      النتائج   │
│                                         │
└─────────────────────────────────────────┘
```

</div>

---

## من ناحية التفكير المنطقي 🧩

### البرنامج = خوارزمية + بنية بيانات

<div dir="ltr">

```
Program = Algorithm + Data Structure
```

</div>

### 1️⃣ الخوارزمية (Algorithm)

**هي سلسلة خطوات منطقية واضحة لحل مشكلة معينة**

#### مثال تفكير منطقي: حساب مجموع الأعداد الزوجية

<div dir="ltr">

```
الخطوات المنطقية:
1. ابدأ من القائمة
2. لكل عنصر في القائمة:
   - هل العنصر زوجي؟
     ├─ نعم → أضفه للمجموع
     └─ لا → تجاهله
3. أرجع المجموع النهائي
```

</div>

#### العناصر الأساسية في التفكير المنطقي:

| العنصر        | الوصف                  | مثال من الحياة                |
| ------------- | ---------------------- | ----------------------------- |
| **Sequence**  | تنفيذ الخطوات بالترتيب | وصفة طبخ                      |
| **Selection** | اتخاذ قرار (if/else)   | إذا كان المطر نازلاً، خذ مظلة |
| **Iteration** | تكرار عملية            | عد من 1 إلى 10                |

### 2️⃣ بنية البيانات (Data Structure)

**هي طريقة تنظيم وتخزين البيانات لتسهيل الوصول والتعديل**

<div dir="ltr">

```
التفكير المنطقي في البيانات:
- كيف أخزن البيانات؟
- كيف أصل إليها بسرعة؟
- كيف أعدّلها بكفاءة؟
```

</div>

---

## من ناحية اللغة البرمجية 💻

### البرنامج = نص برمجي يُترجم إلى تعليمات الآلة

<div dir="ltr">

```
┌──────────────────────────────────────────────────┐
│          Program Compilation Pipeline            │
├──────────────────────────────────────────────────┤
│                                                  │
│  Source Code (Kotlin)                            │
│       ↓                                          │
│  Compiler (kotlinc)                              │
│       ↓                                          │
│  Bytecode (.class files)                         │
│       ↓                                          │
│  Dalvik Executable (.dex)                        │
│       ↓                                          │
│  ART (Android Runtime)                           │
│       ↓                                          │
│  Machine Code (Native CPU instructions)          │
│                                                  │
└──────────────────────────────────────────────────┘
```

</div>

### المكونات الأساسية في اللغة البرمجية:

#### 1. **Variables** - المتغيرات

مكان لتخزين البيانات في الذاكرة

<div dir="ltr">

```kotlin
// Declaration: حجز مساحة في الذاكرة
val username: String = "Ahmed"
var age: Int = 25

// في الذاكرة:
// Address: 0x1000 → Value: "Ahmed"
// Address: 0x1004 → Value: 25
```

</div>

#### 2. **Operators** - المعاملات

أدوات لمعالجة البيانات

<div dir="ltr">

```kotlin
val sum = 10 + 5        // Arithmetic
val isValid = age > 18   // Comparison
val result = true && false // Logical
```

</div>

#### 3. **Control Flow** - التحكم في التدفق

تحديد مسار التنفيذ

<div dir="ltr">

```kotlin
// Selection
if (age >= 18) {
    println("Adult")
} else {
    println("Minor")
}

// Iteration
for (i in 1..5) {
    println(i)
}
```

</div>

#### 4. **Functions** - الدوال

كتل برمجية قابلة لإعادة الاستخدام

<div dir="ltr">

```kotlin
fun calculateSum(numbers: List<Int>): Int {
    return numbers.sum()
}
```

</div>

#### 5. **Data Structures** - هياكل البيانات

طرق تنظيم البيانات

<div dir="ltr">

```kotlin
val list = listOf(1, 2, 3)           // Ordered collection
val map = mapOf("key" to "value")     // Key-Value pairs
```

</div>

---

## البرنامج في Android 📱

### البرنامج في Android = APK

<div dir="ltr">

```
APK Structure:
├── AndroidManifest.xml      (البيان: ما يحتويه التطبيق)
├── classes.dex              (Bytecode: التعليمات المترجمة)
├── resources.arsc           (الموارد: الصور، النصوص)
├── res/                     (ملفات الموارد)
├── lib/                     (المكتبات الأصلية)
└── META-INF/                (التوقيعات والشهادات)
```

</div>

### رحلة البرنامج من الكود إلى التنفيذ:

<div dir="ltr">

```kotlin
// 1. Source Code (ما تكتبه)
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val result = calculateSum(listOf(1, 2, 3))
        Log.d("Result", "Sum: $result")
    }

    private fun calculateSum(numbers: List<Int>): Int {
        return numbers.sum()
    }
}
```

</div>

<div dir="ltr">

```
2. Compilation (ما يحدث خلف الكواليس):

   Kotlin Compiler
        ↓
   .class files (Java Bytecode)
        ↓
   D8/R8 Compiler
        ↓
   .dex files (Dalvik Bytecode)
        ↓
   APK Package
```

</div>

<div dir="ltr">

```
3. Runtime Execution (على الجهاز):

   Android OS يُحمّل APK
        ↓
   ART يُجهّز البرنامج
        ↓
   Process يُنشأ للتطبيق
        ↓
   الكود يُنفّذ instruction by instruction
```

</div>

---

## أمثلة عملية 💡

### مثال 1: برنامج بسيط - حساب مجموع الأعداد الزوجية

#### التفكير المنطقي:

<div dir="ltr">

```
Input: [1, 2, 3, 4, 5, 6]
Processing:
  - فحص كل عنصر
  - إذا كان زوجي (n % 2 == 0)
  - أضفه للمجموع
Output: 12 (لأن 2 + 4 + 6 = 12)
```

</div>

#### الكود في Kotlin:

<div dir="ltr">

```kotlin
fun sumEvenNumbers(numbers: List<Int>): Int {
    var sum = 0  // State: حالة مؤقتة

    // Iteration: تكرار
    for (number in numbers) {
        // Selection: اتخاذ قرار
        if (number % 2 == 0) {
            sum += number  // Accumulation: تجميع
        }
    }

    return sum  // Output
}

// الاستخدام
fun main() {
    val numbers = listOf(1, 2, 3, 4, 5, 6)
    val result = sumEvenNumbers(numbers)
    println("Sum of even numbers: $result")  // Output: 12
}
```

</div>

#### ما يحدث في الذاكرة:

<div dir="ltr">

```
Memory State During Execution:

Iteration 1: number = 1
  ├─ 1 % 2 == 0? false
  └─ sum = 0 (no change)

Iteration 2: number = 2
  ├─ 2 % 2 == 0? true
  └─ sum = 2

Iteration 3: number = 3
  ├─ 3 % 2 == 0? false
  └─ sum = 2 (no change)

Iteration 4: number = 4
  ├─ 4 % 2 == 0? true
  └─ sum = 6

Iteration 5: number = 5
  ├─ 5 % 2 == 0? false
  └─ sum = 6 (no change)

Iteration 6: number = 6
  ├─ 6 % 2 == 0? true
  └─ sum = 12

Final: return 12
```

</div>

### مثال 2: برنامج Android - عرض قائمة مستخدمين

#### التفكير المنطقي:

<div dir="ltr">

```
Input: قائمة بيانات المستخدمين من API
Processing:
  1. جلب البيانات (Network Call)
  2. تحويل JSON إلى Objects
  3. تصفية المستخدمين النشطين
  4. ترتيبهم حسب الاسم
Output: عرض القائمة على الشاشة
```

</div>

#### الكود في Kotlin:

<div dir="ltr">

```kotlin
data class User(
    val id: Int,
    val name: String,
    val isActive: Boolean
)

class UserViewModel : ViewModel() {

    // State: الحالة التي يراقبها UI
    private val _users = MutableLiveData<List<User>>()
    val users: LiveData<List<User>> = _users

    fun loadUsers() {
        viewModelScope.launch {
            // Input: جلب البيانات
            val response = userRepository.fetchUsers()

            // Processing: معالجة البيانات
            val activeUsers = response
                .filter { it.isActive }      // تصفية النشطين فقط
                .sortedBy { it.name }        // ترتيب حسب الاسم

            // Output: تحديث الحالة
            _users.value = activeUsers
        }
    }
}
```

</div>

<div dir="ltr">

```kotlin
class UsersActivity : AppCompatActivity() {

    private val viewModel: UserViewModel by viewModels()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_users)

        // Observe: مراقبة التغييرات
        viewModel.users.observe(this) { users ->
            // UI Update: تحديث الواجهة
            updateRecyclerView(users)
        }

        // Trigger: بدء العملية
        viewModel.loadUsers()
    }
}
```

</div>

#### ما يحدث على مستوى النظام:

<div dir="ltr">

```
Android System Level:

1. Main Thread (UI Thread):
   └─ onCreate() executed
   └─ observe() registered
   └─ loadUsers() called

2. Background Thread (Coroutine):
   └─ Network request sent
   └─ Response received
   └─ Data processing (filter, sort)
   └─ Post result to Main Thread

3. Main Thread (UI Thread):
   └─ LiveData value changed
   └─ Observer triggered
   └─ RecyclerView updated
   └─ UI redrawn
```

</div>

---

## المشاكل الشائعة ⚠️

### ❌ مشكلة 1: عدم فهم الفرق بين Declaration و Execution

<div dir="ltr">

```kotlin
// Declaration: تعريف الدالة (لا يُنفّذ)
fun greet(name: String) {
    println("Hello, $name")
}

// Execution: تنفيذ الدالة
greet("Ahmed")  // هنا فقط يُطبع النص
```

</div>

**الخطأ الشائع:**

<div dir="ltr">

```kotlin
class MainActivity : AppCompatActivity() {

    // ❌ هذا مجرد تعريف، لن يُنفّذ تلقائيًا
    fun showMessage() {
        Toast.makeText(this, "Hello", Toast.LENGTH_SHORT).show()
    }

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        // ✅ يجب استدعاء الدالة لتنفيذها
        showMessage()
    }
}
```

</div>

### ❌ مشكلة 2: عدم فهم State Management

<div dir="ltr">

```kotlin
// ❌ الحالة المحلية تُفقد عند إعادة إنشاء Activity
class MainActivity : AppCompatActivity() {

    var counter = 0  // ستُفقد عند تدوير الشاشة

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        // counter سيعود إلى 0 بعد التدوير
    }
}
```

</div>

<div dir="ltr">

```kotlin
// ✅ الحل: استخدام ViewModel للحفاظ على الحالة
class CounterViewModel : ViewModel() {
    var counter = 0  // تبقى حية أثناء Configuration Changes
}
```

</div>

### ❌ مشكلة 3: Blocking Main Thread

<div dir="ltr">

```kotlin
// ❌ عملية طويلة على Main Thread
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        // هذا سيجمد التطبيق!
        val data = fetchDataFromNetwork()  // 5 seconds
        updateUI(data)
    }
}
```

</div>

<div dir="ltr">

```kotlin
// ✅ الحل: استخدام Coroutines
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        lifecycleScope.launch {
            // يعمل في Background Thread
            val data = withContext(Dispatchers.IO) {
                fetchDataFromNetwork()
            }
            // يعود إلى Main Thread
            updateUI(data)
        }
    }
}
```

</div>

---

## الربط بمبادئ Software Engineering 🏗️

### 1. Single Responsibility Principle

<div dir="ltr">

```kotlin
// ❌ دالة تفعل أكثر من شيء
fun processUser(userId: Int) {
    val user = fetchUser(userId)      // Network
    validateUser(user)                // Validation
    saveToDatabase(user)              // Database
    sendNotification(user)            // Notification
}

// ✅ فصل المسؤوليات
class UserRepository {
    fun fetchUser(id: Int): User { /*...*/ }
}

class UserValidator {
    fun validate(user: User): Boolean { /*...*/ }
}

class UserDatabase {
    fun save(user: User) { /*...*/ }
}

class NotificationService {
    fun notify(user: User) { /*...*/ }
}
```

</div>

### 2. DRY (Don't Repeat Yourself)

<div dir="ltr">

```kotlin
// ❌ تكرار الكود
fun calculateDiscountForStudent(price: Double): Double {
    return price * 0.8
}

fun calculateDiscountForEmployee(price: Double): Double {
    return price * 0.8
}

// ✅ استخراج الكود المشترك
fun calculateDiscount(price: Double, percentage: Double): Double {
    return price * (1 - percentage)
}

val studentPrice = calculateDiscount(100.0, 0.2)
val employeePrice = calculateDiscount(100.0, 0.2)
```

</div>

---

## الخلاصة 🎓

### النقاط الجوهرية:

| المنظور             | التعريف                           | المثال في Android                |
| ------------------- | --------------------------------- | -------------------------------- |
| **التفكير المنطقي** | خوارزمية + بنية بيانات            | تصفية قائمة، ترتيب بيانات        |
| **اللغة البرمجية**  | تعليمات تُترجم لكود الآلة         | Kotlin → Bytecode → Machine Code |
| **وقت التنفيذ**     | Process في الذاكرة يُنفّذ تعليمات | ART يُنفّذ APK على Android       |

### القاعدة الذهبية:

<div dir="ltr">

```
البرنامج ليس فقط "كود يعمل"
البرنامج هو:
  ✓ حل منطقي لمشكلة
  ✓ بيانات منظمة
  ✓ تعليمات قابلة للتنفيذ
  ✓ حالة (State) تتغير مع الوقت
  ✓ تفاعل مع النظام والمستخدم
```

</div>

### الفرق بين المبتدئ والمحترف:

| المبتدئ                  | المحترف                       |
| ------------------------ | ----------------------------- |
| يكتب كود "يعمل"          | يكتب كود يُفهم ويُصان         |
| يفكر في Features         | يفكر في Architecture          |
| يحل المشكلة مرة          | يبني حل قابل لإعادة الاستخدام |
| يكتب كل شيء في مكان واحد | يفصل المسؤوليات               |
| يختبر يدويًا             | يكتب Unit Tests               |

---

### الخطوة التالية:

الآن بعد فهم "ما هو البرنامج"، الأسئلة المنطقية التالية:

- كيف يُنفّذ البرنامج؟ (Execution Model)
- كيف تُدار الذاكرة؟ (Memory Management)
- كيف تتواصل الأجزاء؟ (Communication & IPC)
- كيف نتعامل مع الأخطاء؟ (Error Handling)

**جاهز للسؤال الثاني! 🚀**

</div>
