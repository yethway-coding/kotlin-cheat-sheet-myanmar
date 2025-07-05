# Kotlin Cheatsheet (မြန်မာဘာသာပြန်)  

Kotlin Cheatsheet ဆိုတာက Kotlin programming language ရဲ့ အရေးကြီးဆုံး syntax တွေနဲ့ features တွေကို အချက်လိုက် မြန်မြန်ဆန်ဆန် လေ့လာနိုင်အောင် စုစည်းထားတဲ့ လမ်းညွှန်တစ်ခုဖြစ်ပါတယ်။ ဒီ cheatsheet ထဲက အကြောင်းအရာအများစုကို Kotlin ရဲ့ တရားဝင် မှတ်တမ်းကနေ ရယူထားပြီး အသေးစိတ်ရှင်းလင်းချက်တွေကို ရှောင်ရှားထားပါတယ်။ ဒီ cheatsheet က အမြန်ပြန်လှန်ကြည့်ဖို့အတွက်သာ ရည်ရွယ်ပါတယ်။ အသေးစိတ်သိချင်ရင် တရားဝင် [Kotlin documentation](https://kotlinlang.org/docs/home.html) ကို ဖတ်ဖို့ အကြံပြုပါတယ်။  

တကယ်လို့ ပြဿနာတစ်ခုခုတွေ့ရင် issue တစ်ခုဖွင့်ပြောပါ (ဒါမှမဟုတ်) ဒီ repository ကို contribute လုပ်ဖို့လည်း ဝမ်းသာပါတယ်။ ကျွန်တော့်ကို အားပေးချင်ရင် repository ကို star ပေးလို့ရပါတယ်။⭐  

![Kotlin လိုဂို](https://github.com/alidehkhodaei/kotlin-cheatsheet/raw/main/images/kotlin_logotype.jpg)  

## အကြောင်းအရာများစုစည်းမှု  

- [မိတ်ဆက်](#introduction)  
  - [ပထမဆုံး Kotlin program](#first-kotlin-program)  
  - [အသုံးပြုသူထံမှ input ရယူခြင်း](#get-input-from-user)  
  - [မှတ်ချက်များ](#comments)  
  - [KDoc](#kdoc)  
  - [Variables](#variables)  
  - [Data အမျိုးအစားများ](#data-types)  
  - [Type Inference](#type-inference)  
  - [Type Conversion](#type-conversion)  
  - [String templates](#string-templates)  
  - [Character escape](#character-escape)  
  - [Operators](#operators)  
- [Control Flow](#control-flow)  
  - [If-else](#if-else)  
  - [When](#when)  
  - [Conditional Expression](#conditional-expression)  
  - [For loop](#for-loop)  
  - [Ranges](#ranges)  
  - [While](#while)  
  - [Do while](#do-while)  
  - [Break and Continue](#break-and-continue)  
  - [Exceptions](#exceptions)  
- [Functions](#functions)  
  - [Function Declaration](#function-declaration)  
  - [Default arguments and named arguments](#default-arguments-and-named-arguments)  
  - [Function Return Types](#function-return-type)  
  - [Local functions](#local-functions)  
  - [Member functions](#member-functions)  
  - [Generic functions](#generic-functions)  
  - [Lambda Expressions](#lambda-expressions)  
  - [Extension Functions and Properties](#extension-functions-and-Properties)  
  - [Higher-Order Functions](#higher-order-functions)  
  - [Operator overloading](#operator-overloading)  
  - [Variable number of arguments (varargs)](#varargs)  
  - [Infix notation](#infix-notation)  
  - [Scope Functions](#scope-functions)  
- [Collections](#collections)  
  - [Array](#array)  
  - [List](#list)  
  - [Map](#map)  
  - [Set](#set)  
- [Classes and objects](#class-and-object)  
  - [Classes](#classes)  
  - [Property and methods](#property-and-methods)  
  - [Getters and setters](#getters-and-setters)  
  - [Visibility modifiers](#visibility-modifiers)  
  - [Late-initialized properties and variables](#late-initialized-properties-and-variables)  
  - [Inheritance](#inheritance)  
  - [Interface and Abstract Class](#interface-and-abstract-class)  
  - [Abstraction](#abstraction)  
  - [Polymorphism](#polymorphism)  
  - [Object Expression and Declaration](#object-expression-and-declaration)  
  - [Data class](#data-class)  
  - [Nested and Inner class](#nested-and-inner-class)  
  - [Type aliases](#type-aliases)  
  - [Enum](#enum)  
  - [Sealed class and interface](#sealed-class-and-interface)  
  - [Generics](#generics)  
  - [Delegation Pattern](#delegation-pattern)  
  - [Delegated properties](#delegated-properties)  
- [အခြားခေါင်းစဉ်များ](#other-topics)  
  - [Destructuring declarations](#destructuring-declarations)  
  - [Reflection](#reflection)  
  - [Annotations](#annotations)  
  - [Packages and imports](#packages-and-imports)  
  - [Null safety](#null-safety)  
  - [Equality](#equality)  
  - [Comparable](#comparable)  
  - [Regex](#regex)  
- <a href="https://kotlinlang.org/docs/keyword-reference.html">Kotlin Keywords and operators (Document link)</a>  

## မိတ်ဆက် <a name="introduction"></a>  
Kotlin ဆိုတာက ခေတ်သစ်၊ open-source programming language တစ်ခုဖြစ်ပြီး multi-platform applications တွေ ဆောက်ဖို့အတွက် အသုံးပြုပါတယ်။ ဒီ language က concise (အတိုချုံး)၊ expressive (ထင်ဟပ်မှုရှိ)၊ powerful (အားကောင်း) ပြီး null safety၊ extension functions၊ lambdas စတဲ့ features တွေပါဝင်ပါတယ်။  
ဒီ cheatsheet မှာ Kotlin ရဲ့ အခြေခံအကျဆုံး concepts တချို့ကို ဖော်ပြထားပါတယ်။  

### ပထမဆုံး Kotlin program <a name="first-kotlin-program"></a>  

Kotlin မှာ "Hello world" ကို ရိုက်ထုတ်တဲ့ ဥပမာ:  
```kotlin
fun main() {
    println("Hello world")
}
```  

### အသုံးပြုသူထံမှ input ရယူခြင်း <a name="get-input-from-user"></a>  
Kotlin မှာ အသုံးပြုသူထံမှ input ရယူဖို့ `readLine()` function ကို အသုံးပြုနိုင်ပါတယ်။  
ဥပမာ:  
```kotlin
fun main() {
    print("Enter your name: ")
    val name = readLine()
    println("Hello, $name!")
}
```  

### မှတ်ချက်များ <a name="comments"></a>  

```kotlin
// ဒါက end-of-line မှတ်ချက်ဖြစ်ပါတယ်  

/* ဒါက block မှတ်ချက်ဖြစ်ပါတယ်  
   multiple lines တွေမှာ ရေးနိုင်ပါတယ် */  
```  

Kotlin မှာ block comments တွေကို အထပ်ထပ်လုပ်နိုင်ပါတယ်။  
```kotlin
/* မှတ်ချက်က ဒီမှာစပါတယ်  
/* nested မှတ်ချက်ပါတယ် *⁠/  
ဒီမှာပြီးပါတယ် */  
```  

### KDoc <a name="kdoc"></a>  
KDoc ဆိုတာက Kotlin အတွက် documentation format တစ်ခုဖြစ်ပြီး Java အတွက် Javadoc နဲ့ ဆင်တူပါတယ်။ KDoc ကို Kotlin classes၊ functions၊ properties တွေအတွက် documentation ထုတ်ဖို့ အသုံးပြုပါတယ်။ KDoc comments တွေက `/**` နဲ့စပြီး `*/` နဲ့ ဆုံးပါတယ်။  
ဥပမာ:  
```kotlin
/**
 * ကိန်းပြည့်နှစ်ခုကို ပေါင်းခြင်း။  
 * 
 * @param a ပေါင်းမယ့် ပထမ ကိန်းပြည့်။  
 * @param b ပေါင်းမယ့် ဒုတိယ ကိန်းပြည့်။  
 * @return ကိန်းပြည့်နှစ်ခု ပေါင်းခြင်း။  
 */  
fun sum(a: Int, b: Int): Int {  
    return a + b  
}  
```  

### Variables <a name="variables"></a>  
Kotlin မှာ variables တွေကို `var` သို့မဟုတ် `val` keyword တွေသုံးပြီး ကြေငြာနိုင်ပါတယ်။  

`var` variables တွေက mutable ဖြစ်ပြီး initialization လုပ်ပြီးရင် တန်ဖိုးပြောင်းလို့ရပါတယ်။  

```kotlin
var x = 5  
x = 10  
```  

`val` variables တွေကတော့ immutable ဖြစ်ပြီး initialization လုပ်ပြီးရင် တန်ဖိုးပြောင်းလို့မရပါဘူး။  

```kotlin
val y = 5  
y = 10 // ဒါက compilation error ဖြစ်စေပါတယ်  
```  

### Data အမျိုးအစားများ <a name="data-types"></a>  
အသုံးများဆုံး data အမျိုးအစားတွေရဲ့ အကျဉ်းချုပ်:  

```kotlin  
    val booleanVar: Boolean = true  
    val byteVar: Byte = 127  
    val shortVar: Short = 32767  
    val intVar: Int = 2147483647  
    val longVar: Long = 9223372036854775807L  
    val floatVar: Float = 3.14f  
    val doubleVar: Double = 3.14159265358979323846  
    val charVar: Char = 'A'  
    val stringVar: String = "Hello, world!"  
```  

### Type Inference <a name="type-inference"></a>  

Kotlin က type inference ကို ပံ့ပိုးပေးပါတယ်။ ဆိုလိုတာက compiler က variable တစ်ခုရဲ့ type ကို initial value ကနေ အလိုအလျောက် ခန့်မှန်းနိုင်ပါတယ်။  

```kotlin
val x = 5 // x ရဲ့ type က Int လို့ အလိုအလျောက် ခန့်မှန်းပါတယ်  
val y = "hello" // y ရဲ့ type က String လို့ အလိုအလျောက် ခန့်မှန်းပါတယ်  
```  

Kotlin မှာ variables တွေကို initial value မထည့်ဘဲလည်း ကြေငြာနိုင်ပါတယ်။ ဒါပေမယ့် အဲ့ဒီအခါမှာတော့ type ကို ရှင်းရှင်းလင်းလင်း ဖော်ပြပေးဖို့လိုပါတယ်:  

```kotlin
var z: Double // Valid, z မှာ initial value မရှိဘူး  
// println(z) // Invalid, z ကို initialize မလုပ်ရသေးတဲ့အတွက် တန်ဖိုးမရှိဘူး  
z = 3.14 // Valid, z ကို တန်ဖိုးနဲ့ initialize လုပ်လိုက်ပြီ  
```  

### Type Conversion <a name="type-conversion"></a>  

Kotlin မှာ data အမျိုးအစားတွေ အချင်းချင်း ပြောင်းလဲဖို့ methods အမျိုးမျိုးရှိပါတယ်။  
အောက်မှာ Kotlin မှာ type conversion လုပ်တဲ့ နည်းလမ်းအမျိုးမျိုးကို ဥပမာနဲ့ ပြထားပါတယ်။  

```kotlin
    val str: String = "123"  
    val num: Int = str.toInt() // String ကနေ Int ကို ပြောင်းမယ်  

    val dbl: Double = 123.45  
    val int: Int = dbl.toInt() // Double ကနေ Int ကို ပြောင်းမယ်  

    val lng: Long = 9876543210  
    val flt: Float = lng.toFloat() // Long ကနေ Float ကို ပြောင်းမယ်  

    val bol: Boolean = true  
    val strBol: String = bol.toString() // Boolean ကနေ String ကို ပြောင်းမယ်  

    val char: Char = 'A'  
    val intChar: Int = char.toInt() // Char ကနေ Int ကို ပြောင်းမယ် // Char ကနေ Number ကို ပြောင်းတာက deprecated ဖြစ်နေပါပြီ။ Char.code property ကို အစားသုံးပါ။  

    val byte: Byte = 127  
    val short: Short = byte.toShort() // Byte ကနေ Short ကို ပြောင်းမယ်  
```  

### String templates <a name="string-templates"></a>  

```kotlin
val name= "Ali"  
val result= "My name is $name"   
```  

### Character escape <a name="character-escape"></a>  

```kotlin
\n စာကြောင်းအသစ်ထည့်မယ်  
\t tab ထည့်မယ်  
\r carriage return ထည့်မယ်  
```  

### Operators <a name="operators"></a>  

Arithmetic operators (သင်္ချာ operator များ)  

```kotlin
  val a = 10  
  val b = 5  
  println(a + b) // 15  
  println(a - b) // 5  
  println(a * b) // 50  
  println(a / b) // 2  
  println(a % b) // 0  
```  

Comparison operators (နှိုင်းယှဉ်ခြင်း operator များ)  
```kotlin
  val c = 10  
  val d = 5  
  println(c > d) // true  
  println(c >= d) // true  
  println(c < d) // false  
  println(c <= d) // false  
  println(c == d) // false  
  println(c != d) // true  
```  

Assignment operators (တန်ဖိုးထည့်သွင်းခြင်း operator များ)  

```kotlin
  var h = 10  
  h += 5  
  println(h) // 15  
  h -= 5  
  println(h) // 10  
  h *= 2  
  println(h) // 20  
  h /= 4  
  println(h) // 5  
  h %= 3  
  println(h) // 1  
```  

Logical operators (လော်ဂျစ် operator များ)    
```kotlin  
  val i = true  
  val j = false  
  println(i && j) // false  
  println(i || j) // true  
  println(!i) // false  
```  

Bitwise operators (ဘစ်ဝေး operator များ)  

```kotlin
  val k = 0b1010  
  val l = 0b1100  
  println(k and l) // "8" (0b1000) ကို ရိုက်ထုတ်မယ်  
  println(k or l) // "14" (0b1110) ကို ရိုက်ထုတ်မယ်  
  println(k xor l) // "6" (0b0110) ကို ရိုက်ထုတ်မယ်  
```  

Range operator (အကွာအဝေး operator)  

```kotlin
  val o = 1..10  
  println(o.contains(5)) // "true" ကို ရိုက်ထုတ်မယ်  
  println(o.contains(11)) // "false" ကို ရိုက်ထုတ်မယ်  
```  

## Control flow <a name="control-flow"></a>  

### If-else <a name="if-else"></a>  

```kotlin
if (condition) {  
    // condition မှန်ရင် execute လုပ်မယ့် code  
} else {  
    // condition မှားရင် execute လုပ်မယ့် code  
}  
```  

### When <a name="when"></a>  

```kotlin
when (value) {  
    condition1 -> // value က condition1 နဲ့ ကိုက်ညီရင် execute လုပ်မယ့် code  
    condition2 -> // value က condition2 နဲ့ ကိုက်ညီရင် execute လုပ်မယ့် code  
    else -> // value က ဘယ် condition နဲ့မှ မကိုက်ညီရင် execute လုပ်မယ့် code  
}  
```  

### Conditional Expression <a name="conditional-expression"></a>  
if နဲ့ when တွေက expressions တွေဖြစ်တဲ့အတွက် တိုက်ရိုက် variables တွေဆီ assign လုပ်နိုင်ပါတယ်။  

```kotlin
val seasonFirstMonth = when(season) {  
    "summer" -> 6,  
    "winter" -> 12,  
    "automn" -> 9,  
    "spring" -> 3,  
    else -> error("There is only 4 seasons")  
}  
```  

ဒါကြောင့် regular if သုံးပြီး ternary operator နဲ့ တူတဲ့ အလားအလာရှိပါတယ်။  

```kotlin
val max = if (a > b) a else b         
```  

### For loop <a name="for-loop"></a>  
```kotlin
for (item in collection) {  
    // collection ထဲက item တစ်ခုချင်းစီအတွက် execute လုပ်မယ့် code  
}  
```  

### Ranges <a name="ranges"></a>  
Kotlin မှာ ranges တွေသတ်မှတ်ဖို့ tools တစ်စုံရှိပါတယ်။  
```kotlin

for(i in 0..3) {              
    print(i)  
}  

for(i in 0 until 3) {       
    print(i)  
}  

for(i in 2..8 step 2) {     
    print(i)  
}  

for (i in 3 downTo 0) {     
    print(i)  
}  
```  
Char ranges တွေလည်း support လုပ်ပါတယ်။  
```kotlin
for (c in 'a'..'d') {   
    print(c)  
}  
```  
Ranges တွေက if statements တွေမှာလည်း အသုံးဝင်ပါတယ်။  

```kotlin
if (x in 1..5) {           
    print("x is in range from 1 to 5")  
}  
```  

### While <a name="while"></a>  
```kotlin  
while (condition) {  
    // condition မှန်နေသရွေ့ execute လုပ်မယ့် code  
}  
```  

### Do While <a name="do-while"></a>  

```kotlin
do {  
    // အနည်းဆုံး တစ်ကြိမ် execute လုပ်မယ့် code  
} while (condition)  
```  

### Break and Continue <a name="break-and-continue"></a>  

```kotlin
for (i in 1..10) {  
    if (i == 5) {  
        break // i က 5 နဲ့ ညီတဲ့အခါ loop ကနေ ထွက်မယ်  
    }  
    if (i % 2 == 0) {  
        continue // ဂဏန်းစုံတွေကို ကျော်ပြီး နောက် iteration ကို ဆက်သွားမယ်  
    }  
    // 1 ကနေ 10 အထိ ဂဏန်းမကိန်းတွေအတွက် execute လုပ်မယ့် code  
}  
```  

### Exceptions <a name="exceptions"></a>  

Exception object တစ်ခုကို လွှင့်ဖို့ throw expression ကို အသုံးပြုပါ:  

```kotlin
throw Exception("Exception...")  
```  
Exception တစ်ခုကို ဖမ်းဖို့ try...catch expression ကို အသုံးပြုပါ:  

```kotlin
try {  
    // some code  
} catch (e: SomeException) {  
    // handler  
} finally {  
    // optional finally block  
}  
```  
Nothing type: ဒီ type မှာ တန်ဖိုးမရှိပါဘူး။ ဘယ်တော့မှ မရောက်နိုင်တဲ့ code တွေကို မှတ်သားဖို့အတွက် အသုံးပြုပါတယ်။ ကိုယ့် code ထဲမှာ Nothing ကို return မပြန်တဲ့ function တစ်ခုကို မှတ်သားဖို့ အသုံးပြုနိုင်ပါတယ်။  
```kotlin
fun fail(message: String): Nothing {  
    throw IllegalArgumentException(message)  
}  
```  

## Functions <a name="functions"></a>  

### Function Declaration <a name="function-declaration"></a>  

```kotlin
fun sayHello() {  
    println("Hello!")  
}  

fun greet(name: String) {  
    println("Hello, $name!")  
}  
```  

### Default arguments and named arguments <a name="default-arguments-and-named-arguments"></a>  

```kotlin
fun greet(name: String = "World", greeting: String = "Hello") {  
    println("$greeting, $name!")  
}  

fun main() {  
    // default arguments တွေနဲ့ function ကို ခေါ်မယ်  
    greet() // output: Hello, World!  

    // named arguments တွေနဲ့ function ကို ခေါ်မယ်  
    greet(greeting = "Hi", name = "Ali") // output: Hi, Ali!  

    // named arguments တချို့နဲ့ function ကို ခေါ်မယ်  
    greet(name = "Reza") // output: Hello, Reza!  
}  
```  

### Function Return Types <a name="function-return-type"></a>  

```kotlin
fun add(a: Int, b: Int): Int {  
    return a + b  
}  

fun multiply(a: Int, b: Int) = a * b  
```  

Unit-returning functions  
Function တစ်ခုက တန်ဖိုးမပြန်ဘူးဆိုရင် return type က Unit ဖြစ်ပါတယ်။  

```kotlin
fun printHello(): Unit {  
  print("Hello")  
}  
```  
ဒါမှမဟုတ်  
```kotlin
fun printHello() {  
   print("Hello")  
}  
```  

### Local functions <a name="local-functions"></a>  

Kotlin က local functions တွေကို support လုပ်ပါတယ်။ local functions တွေဆိုတာ အခြား functions တွေရဲ့အတွင်းမှာ သတ်မှတ်ထားတဲ့ functions တွေဖြစ်ပါတယ်။  
printMessage() ဆိုတာ main() function အတွင်းမှာ သတ်မှတ်ထားတဲ့ local function တစ်ခုဖြစ်ပါတယ်။  
```kotlin
fun main() {  
    fun printMessage(message: String) {  
        println("Message: $message")  
    }  

    printMessage("Hello, world!")  
}  
```  

### Member functions <a name="member-functions"></a>  

Member function ဆိုတာ class သို့မဟုတ် object အတွင်းမှာ သတ်မှတ်ထားတဲ့ function တစ်ခုဖြစ်ပါတယ်။  

```kotlin
class Sample {  
    fun foo() {//...}  
}  
```  

### Generic functions <a name="generic-functions"></a>  

Functions တွေမှာ generic parameters တွေပါနိုင်ပါတယ်။ angle brackets တွေကို function name ရဲ့အရှေ့မှာ ထားပြီး သတ်မှတ်ပါတယ်။  

```kotlin
fun <T> function(item: T){  
 //Code  
}  
```  

### Lambda Expressions <a name="lambda-expressions"></a>  

```kotlin
val sum = { a: Int, b: Int -> a + b }  

val square: (Int) -> Int = { it * it }  
```  

### Extension Functions and Properties <a name="extension-functions-and-Properties"></a>  
Extension Functions and Properties တွေက Kotlin မှာ existing classes တွေကို source code မပြင်ဘဲ အသစ်ထပ်ဖြည့်နိုင်တဲ့ functionality တွေ (သို့) properties တွေ ထည့်ဖို့ ခွင့်ပြုပါတယ်။  
```kotlin
// Extension function  
fun String.reverse(): String {  
    return this.reversed()  
}  

// Extension property  
val String.firstChar: Char  
    get() = this[0]  
```  
```kotlin
fun main() {  
    val str = "Ali"  
    println(str.reverse())  // "ilA" ကို ရိုက်ထုတ်မယ်  
    println(str.firstChar)  // "A" ကို ရိုက်ထုတ်မယ်  
}  
```  

### Higher-Order Functions <a name="higher-order-functions"></a>  

Higher-order function ဆိုတာ အခြား function တစ်ခုကို parameter အဖြစ်လက်ခံတဲ့ (သို့) function တစ်ခုကို return ပြန်တဲ့ function တစ်ခုဖြစ်ပါတယ်။  

- Functions တွေကို Parameters အဖြစ်လက်ခံခြင်း  

```kotlin
fun calculate(x: Int, y: Int, operation: (Int, Int) -> Int): Int {  
    return operation(x, y)                                          
}  

fun sum(x: Int, y: Int) = x + y                                 
```  

```kotlin
fun main() {  
    val sumResult = calculate(1, 7, ::sum)                          
    val mulResult = calculate(1, 7) { a, b -> a * b }              
}  
```  

- Functions တွေကို Return ပြန်ခြင်း  

```kotlin
fun operation(): (Int) -> Int {                                      
    return ::square  
}  

fun square(x: Int) = x * x                                          
```  

```kotlin
fun main() {  
    val func = operation()                                          
    println(func(7))                                                
}  
```  

### Operator overloading <a name="operator-overloading"></a>  
Kotlin မှာ operator overloading က သင့်ရဲ့ classes တွေနဲ့ types တွေအတွက် custom operators တွေကို သတ်မှတ်ဖို့နဲ့ အသုံးပြုဖို့ ခွင့်ပြုပါတယ်။  

```kotlin
data class Point(val x: Int, val y: Int) {  
    operator fun plus(other: Point): Point {  
        return Point(x + other.x, y + other.y)  
    }  
}  
```  

```kotlin
fun main() {  
    val p1 = Point(1, 2)  
    val p2 = Point(3, 4)  
    val p3 = p1 + p2 // overloaded '+' operator ကို အသုံးပြုမယ်  
    println(p3) // Output: Point(x=4, y=6)  
}  
```  

### Variable number of arguments (varargs) <a name="varargs"></a>  

Varargs ဆိုတာ function တစ်ခုကို အမျိုးအစားတူ argument တွေ အများကြီး ပို့နိုင်တဲ့ feature တစ်ခုဖြစ်ပါတယ်။  

```kotlin
fun printNumbers(vararg numbers: Int) {  
    for (number in numbers) {  
        println(number)  
    }  
}  

fun main() {  
    printNumbers(1, 2, 3) // 1, 2, 3 ကို ရိုက်ထုတ်မယ်  
    printNumbers(4, 5, 6, 7, 8) // 4, 5, 6, 7, 8 ကို ရိုက်ထုတ်မယ်  
}  
```  

### Infix notation <a name="infix-notation"></a>  

Kotlin မှာ infix က function တွေကို infix notation (ဆိုလိုတာက parentheses တွေနဲ့ dot notation မသုံးဘဲ) နဲ့ ခေါ်နိုင်အောင် သတ်မှတ်ခွင့်ပြုပါတယ်။  

```kotlin
infix fun Int.times(str: String) = str.repeat(this)  

fun main() {  
    val str = 5 times "Hello "  
    println(str) // Output: "Hello Hello Hello Hello Hello "  
}  
```  

### Scope Functions <a name="scope-functions"></a>  

- let  

let ကို scoping နဲ့ null-checks တွေအတွက် အသုံးပြုနိုင်ပါတယ်။ object တစ်ခုပေါ်မှာ let ကို ခေါ်တဲ့အခါ၊ code block တစ်ခုကို execute လုပ်ပြီး နောက်ဆုံး expression ရဲ့ result ကို return ပြန်ပါတယ်။ object ကို block အတွင်းမှာ it (default) (သို့) custom name တစ်ခုနဲ့ access လုပ်နိုင်ပါတယ်။  

```kotlin
val message: String? = "Hello"  
message?.let {  
    print(it.toUpperCase()) // Output: "HELLO"  
}  
```  

- run  

let လိုပါပဲ၊ run ကလည်း standard library က scoping function တစ်ခုဖြစ်ပါတယ်။ အခြေခံအားဖြင့် အလုပ်လုပ်ပုံက တူပါတယ်: code block တစ်ခုကို execute လုပ်ပြီး နောက်ဆုံး expression ရဲ့ result ကို return ပြန်ပါတယ်။ ကွာခြားချက်က run ထဲမှာ object ကို this နဲ့ access လုပ်ပါတယ်။ object ရဲ့ methods တွေကို argument အဖြစ်ပို့မယ့်အစား တိုက်ရိုက်ခေါ်ချင်တဲ့အခါမှာ ဒါက အသုံးဝင်ပါတယ်။  

```kotlin
val message: String? = "Hello"  
message?.run {  
    print(this.toUpperCase()) // Output: "HELLO"  
}  
```  

- with  

with က non-extension function တစ်ခုဖြစ်ပြီး argument ရဲ့ members တွေကို concise ဖြစ်အောင် access လုပ်နိုင်ပါတယ်: instance name ကို ထည့်မပြောဘဲ members တွေကို ရည်ညွှန်းနိုင်ပါတယ်။  

```kotlin
val person = Person("Ali", 24)  
val message = with(person) {  
    "My name is $name and I'm $age years old."  
}  
```  

- apply  

apply က object တစ်ခုပေါ်မှာ code block တစ်ခုကို execute လုပ်ပြီး object ကိုယ်တိုင်ကို return ပြန်ပါတယ်။ block အတွင်းမှာ object ကို this နဲ့ ရည်ညွှန်းပါတယ်။ ဒီ function က objects တွေကို initialize လုပ်ဖို့ အဆင်ပြေပါတယ်။  

```kotlin
val person = Person("Ali", 24)  
person.apply {  
    name = "Ali"  
    age = 24  
}  
```  

- also  

also က apply လိုပါပဲ: ပေးထားတဲ့ block ကို execute လုပ်ပြီး ခေါ်ထားတဲ့ object ကိုယ်တိုင်ကို return ပြန်ပါတယ်။ block အတွင်းမှာ object ကို it နဲ့ ရည်ညွှန်းတဲ့အတွက် argument အဖြစ်ပို့ရတာ ပိုလွယ်ပါတယ်။ ဒီ function က call chains တွေထဲမှာ logging လိုမျိုး အပိုလုပ်ဆောင်ချက်တွေ ထည့်ဖို့ အဆင်ပြေပါတယ်။  

```kotlin
val message: String? = "Hello"  
message?.also {  
    print(it.toUpperCase()) // Output: "HELLO"  
}  
```  

## Collections <a name="collections"></a>  

### Array <a name="array"></a>  

Array ဆိုတာ အမျိုးအစားတူ element တွေရဲ့ fixed-size collection တစ်ခုဖြစ်ပါတယ်။  

- Arrays တွေကို ကြေငြာခြင်းနှင့် အစပြုခြင်း  

```kotlin

// ကိန်းပြည့် array တစ်ခု ကြေငြာမယ်  
val numbers = arrayOf(1, 2, 3, 4, 5)  

// string array တစ်ခု ကြေငြာမယ်  
val names = arrayOf("Alice", "Bob", "Charlie", "Dave")  

// အရွယ်အစားတစ်ခုနဲ့ array တစ်ခု ကြေငြာမယ်  
val array = arrayOfNulls<Int>(10)  

// အရွယ်အစားနဲ့ initial value တစ်ခုနဲ့ ကိန်းပြည့် array တစ်ခု ကြေငြာမယ်  
val array = Array<Int>(7) { i -> i*i }  
val filledArray = IntArray(5) { index -> index * 2 } // အခြား အမျိုးအစားများ: BooleanArray, ShortArray, DoubleArray စသည်  

```  

- Array Elements တွေကို Access လုပ်ခြင်း  

```kotlin
// အထူး index တစ်ခုမှာ element တစ်ခုကို access လုပ်မယ်  
val firstNumber = numbers[0]  

// Array ရဲ့ နောက်ဆုံး element ကို access လုပ်မယ်  
val lastNumber = numbers[numbers.size - 1]  
```  

- Array Elements တွေကို ပြုပြင်ခြင်း  

```kotlin
// အထူး index တစ်ခုမှာ element တစ်ခုကို ပြုပြင်မယ်  
numbers[0] = 10  

// Array တစ်ခုကို အထူး value တစ်ခုနဲ့ ဖြည့်မယ်  
Arrays.fill(numbers, 0)  
```  

- Arrays တွေပေါ်မှာ Iterate လုပ်ခြင်း  

```kotlin

// for loop သုံးပြီး array တစ်ခုပေါ်မှာ iterate လုပ်မယ်  
for (number in numbers) {  
    println(number)  
}  

// index နဲ့တကွ for loop သုံးပြီး array တစ်ခုပေါ်မှာ iterate လုပ်မယ်  
for (i in names.indices) {  
    println("${i}: ${names[i]}")  
}  

// forEach loop သုံးပြီး array တစ်ခုပေါ်မှာ iterate လုပ်မယ်  
names.forEach { name ->  
    println(name)  
}  
```  

- အခြေခံ methods များ  

```kotlin
val index = numbers.indexOf(3)  

numbers.sort()  

names.reverse()  
```  

### List <a name="list"></a>  

- သတ်မှတ်ထားတဲ့ အစဉ်လိုက် element တွေရဲ့ collection တစ်ခု  
- Duplicates တွေပါနိုင်တယ်  
- Immutable: listOf(), or mutable: mutableListOf()  
- List: ဒါက element တွေရဲ့ read-only list တစ်ခုအတွက် အခြေခံ interface ဖြစ်တယ်။  
- MutableList: ဒါက List ရဲ့ subinterface တစ်ခုဖြစ်ပြီး element တွေထည့်ခြင်း၊ ဖယ်ရှားခြင်းလိုမျိုး mutable operations တွေကို ခွင့်ပြုတယ်။  
- ArrayList: ဒါက MutableList ရဲ့ implementation တစ်ခုဖြစ်ပြီး element တွေသိမ်းဖို့ array တစ်ခုကို အသုံးပြုတယ်။  
- LinkedList: ဒါက MutableList ရဲ့ implementation တစ်ခုဖြစ်ပြီး element တွေသိမ်းဖို့ linked list တစ်ခုကို အသုံးပြုတယ်။  

```kotlin
val list = listOf(1, 2, 3, 4, 5)  
val list2=mutableListOf(1, 2, 3, 4, 5)  
```  

အခြေခံ methods များ:  
```kotlin
    val numbers = mutableListOf(1, 2, 3)  
    numbers.add(4) // သတ်မှတ်ထားတဲ့ element ကို list ရဲ့ အဆုံးမှာ ထည့်မယ်  
    numbers.remove(3) // list ထဲက သတ်မှတ်ထားတဲ့ element ရဲ့ ပထမဆုံး အကြိမ်ကို ဖယ်ရှားမယ်  
    numbers[1] // list ထဲက သတ်မှတ်ထားတဲ့ index မှာ ရှိတဲ့ element ကို return ပြန်မယ်  
```  

### Map <a name="map"></a>  

- key-value pairs တွေရဲ့ collection တစ်ခု  
- Keys တွေက unique ဖြစ်ရမယ်  
- Immutable: mapOf(), or mutable: mutableMapOf()  
- Map: ဒါက key-value pairs တွေရဲ့ read-only map တစ်ခုအတွက် အခြေခံ interface ဖြစ်တယ်။  
- MutableMap: ဒါက Map ရဲ့ subinterface တစ်ခုဖြစ်ပြီး key-value pairs တွေထည့်ခြင်း၊ ဖယ်ရှားခြင်းလိုမျိုး mutable operations တွေကို ခွင့်ပြုတယ်။  
- HashMap: ဒါက MutableMap ရဲ့ implementation တစ်ခုဖြစ်ပြီး key-value pairs တွေသိမ်းဖို့ hash table တစ်ခုကို အသုံးပြုတယ်။  
- LinkedHashMap: ဒါက MutableMap ရဲ့ implementation တစ်ခုဖြစ်ပြီး key-value pairs တွေရဲ့ ထည့်သွင်းမှုအစဉ်ကို ထိန်းသိမ်းထားတယ်။  
- SortedMap: ဒါက key-value pairs တွေကို အစဉ်လိုက်ထိန်းသိမ်းထားတဲ့ map တစ်ခုအတွက် interface ဖြစ်တယ်။  
- TreeMap: ဒါက SortedMap ရဲ့ implementation တစ်ခုဖြစ်တယ်။  

```kotlin
val map = mapOf(1 to "one", 2 to "two", 3 to "three")  
val map2= mutableListOf(1 to "one", 2 to "two", 3 to "three")  
```  

အခြေခံ methods များ:  
```kotlin
    val numbers =  mutableMapOf("one" to 1, "two" to 2, "three" to 3)  
    numbers.put("four", 4) // သတ်မှတ်ထားတဲ့ value ကို သတ်မှတ်ထားတဲ့ key နဲ့ map ထဲမှာ ဆက်စပ်ပေးမယ်  
    numbers.remove("two") // map ထဲက သတ်မှတ်ထားတဲ့ key အတွက် mapping ကို ဖယ်ရှားမယ် (အကယ်၍ ရှိခဲ့ရင်)  
    numbers.containsKey("two") // map ထဲမှာ သတ်မှတ်ထားတဲ့ key ပါရင် true ပြန်မယ်  
```  

### Set <a name="set"></a>  

- Duplicates မရှိတဲ့ element တွေရဲ့ collection တစ်ခု  
- Elements တွေက သတ်မှတ်ထားတဲ့ အစဉ်လိုက်မဟုတ်ဘူး  
- Immutable: setOf(), or mutable: mutableSetOf  
- Set: ဒါက element တွေရဲ့ read-only set တစ်ခုအတွက် အခြေခံ interface ဖြစ်တယ်။  
- MutableSet: ဒါက Set ရဲ့ subinterface တစ်ခုဖြစ်ပြီး element တွေထည့်ခြင်း၊ ဖယ်ရှားခြင်းလိုမျိုး mutable operations တွေကို ခွင့်ပြုတယ်။  
- HashSet: ဒါက MutableSet ရဲ့ implementation တစ်ခုဖြစ်ပြီး element တွေသိမ်းဖို့ hash table တစ်ခုကို အသုံးပြုတယ်။  
- LinkedHashSet: ဒါက MutableSet ရဲ့ implementation တစ်ခုဖြစ်ပြီး element တွေရဲ့ ထည့်သွင်းမှုအစဉ်ကို ထိန်းသိမ်းထားတယ်။  
- SortedSet: ဒါက element တွေကို အစဉ်လိုက်ထိန်းသိမ်းထားတဲ့ set တစ်ခုအတွက် interface ဖြစ်တယ်။  
- TreeSet: ဒါက SortedSet ရဲ့ implementation တစ်ခုဖြစ်တယ်။  

```kotlin
val set = setOf(1, 2, 3, 4, 5)  
val set2=mutableSetOf(1, 2, 3, 4, 5)  
```  

အခြေခံ methods များ:  
```kotlin
    val numbers =  mutableSetOf(1, 2, 3)  
    numbers.add(4) // သတ်မှတ်ထားတဲ့ element ကို set ထဲမှာ ထည့်မယ် (အကယ်၍ မရှိသေးရင်)  
    numbers.remove(3) // set ထဲက သတ်မှတ်ထားတဲ့ element ကို ဖယ်ရှားမယ် (အကယ်၍ ရှိခဲ့ရင်)  
    numbers.contains(1) //  set ထဲမှာ သတ်မှတ်ထားတဲ့ element ပါရင် true ပြန်မယ်  
```  

ကျေးဇူးပြု၍ collections အမျိုးမျိုးနှင့် အသေးစိတ်များအတွက် documentation ကိုဖတ်ပါ။  

## Class and Object <a name="class-and-object"></a>  

### Classes <a name="classes"></a>  

- class ဆိုတာ objects တွေဖန်တီးဖို့ ပုံစံချထားတဲ့ blueprint တစ်ခုဖြစ်တယ်။  
- object ဆိုတာ class တစ်ခုရဲ့ instance တစ်ခုဖြစ်တယ်။  

```kotlin
class Person(val name: String, var age: Int) // class  

val person = Person("Ali", 24) // object  
```  

### Property and methods <a name="property-and-methods"></a>  

- Properties တွေဆိုတာ class/object တစ်ခုရဲ့ အစိတ်အပိုင်းဖြစ်တဲ့ variables တွေဖြစ်တယ်။  
- Methods တွေဆိုတာ class/object တစ်ခုရဲ့ အစိတ်အပိုင်းဖြစ်တဲ့ functions တွေဖြစ်တယ်။  

```kotlin
class Person(val name: String) {  
   var age = 0 // property  

   fun sayHello() { // method  
      println("Hello, my name is $name")  
   }  
}  

val person = Person("Ali")  
person.age = 24  
person.sayHello()  
```  

### Getters and setters <a name="getters-and-setters" ></a>  

Kotlin မှာ Getter နဲ့ setter တွေက variable တစ်ခုရဲ့ တန်ဖိုးကို ရယူဖို့နဲ့ ပြုပြင်ဖို့ အသုံးပြုတဲ့ accessors တွေဖြစ်တယ်။ initializer, getter, နဲ့ setter တွေက optional ဖြစ်တယ်။  

```kotlin
class Person {  
    var name: String = ""  
        get() = field.uppercase(Locale.getDefault())  
        set(value) {  
            field = "Name: $value"  
        }  

    var age = 24 // default getter နဲ့ setter ရှိတယ်  

    val username="Ali" // default getter ရှိတယ်  

}  
```  
Properties, getter/setter, backing fields, backing properties စတာတွေအကြောင်း အသေးစိတ်သိချင်ရင် ဒီ [link](https://kotlinlang.org/docs/properties.html) ကိုဖတ်ပါ။  

### Visibility modifiers <a name="visibility-modifiers" ></a>  

- private: visibility ကို တူညီတဲ့ class အတွင်းမှာသာ ကန့်သတ်မယ်။  
- protected: visibility ကို တူညီတဲ့ class နဲ့ ၎င်းရဲ့ subclasses တွေအတွင်းမှာသာ ကန့်သတ်မယ်။  
- internal: visibility ကို တူညီတဲ့ module အတွင်းမှာသာ ကန့်သတ်မယ်။  
- public: ဘယ်နေရာကမဆို visibility ကို ခွင့်ပြုမယ်။  

### Late-initialized properties and variables <a name="late-initialized-properties-and-variables"></a>  

lateinit variable ကို variable တစ်ခုကို အသုံးမပြုခင် initialized လုပ်မယ်ဆိုတာ သိရင်၊ ဒါပေမယ့် declaration အချိန်မှာ initial value မထည့်ချင်ရင် အသုံးပြုပါတယ်။  

```kotlin
lateinit var myLateInitVar: String  

// variable ကို အခုအချိန်မှာ initialized မလုပ်ရသေးတဲ့အတွက် access လုပ်ဖို့ကြိုးစားရင် exception တက်မယ်  
// println(myLateInitVar) // ဒီစာကြောင်းက "lateinit property has not been initialized" exception ကိုဖြစ်စေမယ်  

// အချိန်အနည်းငယ်ကြာပြီးနောက် variable ကို initialized လုပ်မယ်  
myLateInitVar = "Hello World"  

// အခု exception မရှိဘဲ variable ကို access လုပ်နိုင်ပါပြီ  
println(myLateInitVar) // "Hello World" ကိုရိုက်ထုတ်မယ်  
```  

### Inheritance <a name="inheritance"></a>  
Inheritance ဆိုတာ class တစ်ခုက အခြား class တစ်ခုရဲ့ properties တွေနဲ့ methods တွေကို ရယူဖို့ လုပ်ဆောင်ချက်ဖြစ်တယ်။  

```kotlin
open class Animal(val name: String) {  
   open fun makeSound() {  
      println("Animal sound")  
   }  
}  

class Dog(name: String): Animal(name) {  
   override fun makeSound() {  
      println("Woof!")  
   }  
}  
```  

### Interface and Abstract Class <a name="interface-and-abstract-class"></a>  
Interface နဲ့ abstract class နှစ်ခုလုံးက classes တွေလိုက်နာဖို့ contracts (သို့) blueprints တွေကို သတ်မှတ်ဖို့ နည်းလမ်းတွေပေးပါတယ်။ Abstraction အတွက် အသုံးပြုပါတယ်။  

```kotlin
interface Vehicle {  
    fun start()  
    fun stop()  
    val name: String  
}  
```  
```kotlin
abstract class Animal {  
    abstract fun makeSound()  
    open fun move() {  
        println("Moving...")  
    }  
}  
```  

### Abstraction <a name="abstraction"></a>  
Abstraction ဆိုတာ object တစ်ခုရဲ့ implementation details တွေကို ဖုံးကွယ်ပြီး အသုံးပြုသူအတွက် လိုအပ်တဲ့ details တွေကိုသာ ဖော်ပြဖို့ ယန္တရားတစ်ခုဖြစ်တယ်။ Kotlin မှာ abstraction ကို interfaces နဲ့ abstract classes တွေကနေ ရရှိပါတယ်။  

### Polymorphism <a name="polymorphism"></a>  
Polymorphism ဆိုတာ object တစ်ခုက အမျိုးမျိုးသော ပုံစံတွေကို ယူနိုင်စွမ်းဖြစ်တယ်။  
```kotlin
class Dog : Animal() {  
    override fun makeSound() {  
        println("Woof!")  
    }  
}  

class Cat : Animal() {  
    override fun makeSound() {  
        println("Meow!")  
    }  
}  
```  
ဒီဥပမာမှာ Dog နဲ့ Cat classes နှစ်ခုလုံးက Animal abstract class ကနေ inherit လုပ်ပြီး makeSound() method ရဲ့ ကိုယ်ပိုင် implementation တွေကို ပေးထားတာကို တွေ့ရပါတယ်။ ဒါက polymorphism ကို သရုပ်ပြတာဖြစ်ပါတယ်။  

### Object Expression and Declaration <a name="object-expression-and-declaration"></a>  

Object expression တစ်ခုက anonymous class တစ်ခုရဲ့ instance တစ်ခုကို ဖန်တီးပြီး object declaration တစ်ခုကတော့ class တစ်ခုရဲ့ singleton instance တစ်ခုကို ဖန်တီးပါတယ်။  

```kotlin
val person = object {  
    val name = "Ali"  
    fun sayHello() {  
        println("Hello, my name is $name")  
    }  
}  

object Singleton {  
    fun doSomething() {  
        println("Doing something...")  
    }  
}  
```  

Companion objects  
Class တစ်ခုအတွင်းမှာ object declaration တစ်ခုကို companion keyword နဲ့ မှတ်သားနိုင်ပါတယ်။  
```kotlin
class MyClass {  
    companion object { }  
}  
```  

### Data class <a name="data-class"></a>  
Data class ဆိုတာ data တွေကို သိမ်းဆည်းဖို့ အထူးပြုလုပ်ထားတဲ့ class တစ်ခုဖြစ်တယ်။  

```kotlin
data class Person(val name: String, var age: Int)  

val person = Person("Ali", 24)  
```  

### Nested and Inner class <a name="nested-and-inner-class"></a>  

- Nested class ဆိုတာ အခြား class တစ်ခုအတွင်းမှာ သတ်မှတ်ထားတဲ့ class တစ်ခုဖြစ်တယ်။  
- Inner class ဆိုတာ nested class တစ်ခုဖြစ်ပြီး outer class ရဲ့ members တွေကို access လုပ်နိုင်တယ်။  

```kotlin
class Outer {  
   private val outerProperty = "Outer property"  

   class Nested {  
      fun foo() {  
         // outerProperty ကို access မလုပ်နိုင်ဘူး  
      }  
   }  

   inner class Inner {  
      fun bar() {  
         println(outerProperty) // outerProperty ကို access လုပ်နိုင်တယ်  
      }  
   }  
}  
```  

### Type aliases <a name="type-aliases"></a>  
Type aliases တွေက existing types တွေအတွက် အခြားနာမည်တွေ ပေးဖို့ ဖြစ်တယ်။ Type name က အရမ်းရှည်နေရင် နာမည်တိုတစ်ခုကို မိတ်ဆက်ပြီး အသစ်ကို အစားသုံးနိုင်ပါတယ်။  

Type alias မသုံးခင်  
```kotlin
val numbers = listOf(1, 2, 3, 4, 5)  
numbers.filter { number: Int -> number % 2 == 0 }.map { number: Int -> "Number is $number" }  
```  

Type alias သုံးပြီး  
```kotlin
typealias NumberPredicate = (Int) -> Boolean  
typealias NumberMapper = (Int) -> String  

val numbers = listOf(1, 2, 3, 4, 5)  
val even: NumberPredicate = { number -> number % 2 == 0 }  
val mapper: NumberMapper = { number -> "Number is $number" }  
numbers.filter(even).map(mapper)  
```  

### Enum <a name="enum"></a>  
Enum ဆိုတာ fixed set တစ်ခုရဲ့ တန်ဖိုးတွေကို ကိုယ်စားပြုတဲ့ type တစ်ခုဖြစ်တယ်။  

```kotlin
enum class Color {  
   RED, GREEN, BLUE  
}  
```  

### Sealed class and interface <a name="sealed-class-and-interface"></a>  

Sealed class/interface တစ်ခုက ၎င်းရဲ့ subclasses/interfaces တွေရဲ့ inheritance ကို တူညီတဲ့ file အတွင်းမှာသာ ကန့်သတ်ထားတယ်။  

```kotlin
sealed class Shape  

class Circle: Shape()  

// ဒီ file အပြင်မှာ Shape ကို subclass လုပ်လို့မရဘူး  
```  

### Generics <a name="generics"></a>  
Kotlin မှာ generic concept က type-safe programming ကို ခွင့်ပြုပြီး မည်သည့် data type နဲ့မဆို အလုပ်လုပ်နိုင်တဲ့ reusable classes, functions, နဲ့ interfaces တွေကို ဖန်တီးနိုင်ပါတယ်။  
```kotlin
class Box<T>(t: T) {  
    var value = t  
}  
```  

### Delegation Pattern<a name="delegation-pattern"></a>  
Kotlin က delegation pattern ရဲ့ အလွယ်တကူ implementation ကို boilerplate code မလိုဘဲ native level မှာ ပံ့ပိုးပေးပါတယ်။  

```kotlin
interface Base {  
    fun print()  
}  

class BaseImpl(val x: Int) : Base {  
    override fun print() { print(x) }  
}  

class Derived(b: Base) : Base by b  

fun main() {  
    val b = BaseImpl(10)  
    Derived(b).print()  
}  
```  

### Delegated properties <a name="delegated-properties"></a>  
Kotlin မှာ delegated properties တွေက property တစ်ခုရဲ့ custom getters နဲ့ setters တွေကို lazy initialization of a property လိုမျိုး အခြား object တစ်ခုဆီ delegate လုပ်ဖို့ ခွင့်ပြုပါတယ်။  

Lazy variable တစ်ခုကို ပထမဆုံး access လုပ်တဲ့အခါမှသာ initialized လုပ်ပါတယ်။  
```kotlin
val myLazyVar: String by lazy {  
    // variable ကို initialize လုပ်ဖို့ စရိတ်ကြီးတဲ့ operation တစ်ခုခု လုပ်မယ်  
    "Hello World"  
}  
// variable ကို ပထမဆုံး access မလုပ်မချင်း initialized မလုပ်သေးဘူး  
println(myLazyVar) // "Hello World" ကိုရိုက်ထုတ်မယ်  
```  

## အခြားခေါင်းစဉ်များ <a name="other-topics"></a>  

### Destructuring declarations <a name="destructuring-declarations"></a>  
Kotlin မှာ destructuring declarations တွေက objects တွေကို individual variables တွေအဖြစ် တစ်ကြောင်းတည်းနဲ့ ဖြိုခွဲဖို့ ခွင့်ပြုပါတယ်။  

```kotlin
 val person=Person("Ali",24)  
 val (name, age) = person  
```  

### Reflection <a name="reflection"></a>  
Reflection ဆိုတာ runtime မှာ သင့်ရဲ့ program structure ကို introspect လုပ်ဖို့ language နဲ့ library features တစ်စုံဖြစ်ပါတယ်။  

ဥပမာ:  
```kotlin

  // String class အတွက် Class object တစ်ခုရယူမယ်  
    val stringClass = String::class.java  

    // String class ရဲ့ fields တွေကိုရယူပြီး နာမည်တွေကို ရိုက်ထုတ်မယ်  
    val fields = stringClass.declaredFields  
    for (field in fields) {  
        println(field.name)  
    }  

    // String class ရဲ့ methods တွေကိုရယူပြီး နာမည်တွေကို ရိုက်ထုတ်မယ်  
    val methods = stringClass.declaredMethods  
    for (method in methods) {  
        println(method.name)  
    }  

```  

### Annotations <a name="annotations"></a>  
Annotations တွေက Kotlin မှာ classes, functions, နဲ့ properties တွေကို compile-time နဲ့ runtime မှာ အပိုသတင်းအချက်အလက် (သို့) metadata တွေပေးဖို့ အထူးတံဆိပ်တွေဖြစ်တယ်။  
ဥပမာ:  
```kotlin
@Deprecated("Use newMethod() instead", ReplaceWith("newMethod()"))  
fun oldMethod() {  
    // ...  
}  
```  

### Packages and imports <a name="packages-and-imports"></a>  
Packages တွေက related classes, functions, နဲ့ အခြား declarations တွေကို အုပ်စုဖွဲ့ဖို့ အသုံးပြုပါတယ်။ Imports တွေက အခြား packages က declarations တွေကို သင့်ရဲ့ current file ထဲမှာ access လုပ်နိုင်အောင် အသုံးပြုပါတယ်။  

```kotlin
package com.example.models  

class Person(val name: String, val age: Int) {  
    // class implementation  
}  
```  
```kotlin
import com.example.models.Person  

fun main() {  
    val person = Person("Ali", 24)  
    println("Name: ${person.name}, Age: ${person.age}")  
}  
```  

### Null safety <a name="null-safety"></a>  

Kotlin မှာ null safety ရှိပါတယ်။ null pointer exceptions တွေကို ကာကွယ်ဖို့ ကူညီပေးပါတယ်။ Kotlin က nullable types တွေနဲ့ အလုပ်လုပ်ဖို့ safe call, elvis, နဲ့ not-null assertion operators တွေကို ပံ့ပိုးပေးပါတယ်။  

```kotlin

    var nullableStr: String? = null  
    var nonNullStr: String = "Hello"  

    // safe call operator  
    println(nullableStr?.length) // null ကိုရိုက်ထုတ်မယ်  

    // elvis operator  
    val len = nullableStr?.length ?: -1  
    println(len) // -1 ကိုရိုက်ထုတ်မယ်  

    // not-null assertion operator  
    // nullableStr က null ဖြစ်နေတဲ့အတွက် null pointer exception တက်မယ်  
    println(nullableStr!!.length)  

    // nonNullStr က nullable မဟုတ်တဲ့အတွက် ဒါက compile မဖြစ်ဘူး  
    // nonNullStr = null  

```  

### Equality <a name="equality"></a>  

Kotlin မှာ equality နှစ်မျိုးရှိပါတယ်:  

- Structural equality (== - equals() ကို စစ်ဆေးခြင်း)  

- Referential equality (=== - references နှစ်ခုက တူညီတဲ့ object ကို ညွှန်းနေခြင်း)  

```kotlin
data class Person(val name:String,val age:Int)  

val person1=Person("Ali",24)  
val person2=Person("Reza",27)  
var person3=Person("Ali",24)  

print(person1==person2) // false  
print(person1!=person2) // true  
print(person1===person2) // false  
print(person1==person3) // true  
print(person1===person3) // flase  
print(person1!==person3) // true  

person3=person1  

print(person1===person3) // true  

```  
- Kotlin မှာ == operator က equals() method ကို ခေါ်တာနဲ့ ညီမျှပါတယ်။  
- Data classes တွေက ၎င်းတို့ရဲ့ properties တွေအပေါ်အခြေခံပြီး equals() method တစ်ခုကို generate လုပ်ပေးပါတယ်။ ဒါပေမယ့် regular classes တွေမှာတော့ မလုပ်ပေးပါဘူး။  
- Objects တွေကို ၎င်းတို့ရဲ့ contents အပေါ်အခြေခံပြီး equality စစ်ဖို့ regular classes တွေအတွက် equals() method ကို override လုပ်ဖို့လိုပါတယ်။  
```kotlin
class Test{  
    var name:String=""  
    override fun equals(other: Any?): Boolean {  
        return this.name==(other as Test).name  
    }  
}  
```  
ကျေးဇူးပြု၍ အသေးစိတ်များအတွက် [doc](https://kotlinlang.org/docs/equality.html) ကိုဖတ်ပါ။  

### Comparable <a name="comparable"></a>  
Objects တွေကို Comparable interface သုံးပြီး နှိုင်းယှဉ်နိုင်ပါတယ်။ ဒီ interface က current object ကို အခြား object တစ်ခုနဲ့ နှိုင်းယှဉ်ပြီး objects တွေရဲ့ order ကို ညွှန်ပြတဲ့ integer value တစ်ခုကို return ပြန်တဲ့ compareTo method တစ်ခုကို သတ်မှတ်ပေးပါတယ်။  

```kotlin
data class Person(val name: String, val age: Int) : Comparable<Person> {  
    override fun compareTo(other: Person): Int {  
        return this.age.compareTo(other.age)  
    }  
}  
```  
```kotlin
val person1 = Person("Ali", 24)  
val person2 = Person("Reza", 30)  

if (person1 < person2) {  
    println("${person1.name} is younger than ${person2.name}")  
} else {  
    println("${person1.name} is older than ${person2.name}")  
}  
```  
List တစ်ခုထဲက objects တွေကို sorted() (သို့) sort() function သုံးပြီး sort လုပ်တဲ့အခါ၊ Kotlin က objects တွေရဲ့ natural order ကို ဆုံးဖြတ်ဖို့ ၎င်းတို့ရဲ့ compareTo() method ကို အသုံးပြုပါတယ်။ List ထဲက objects တွေက Comparable interface ကို implement မလုပ်ထားရင် compile-time error တက်ပါလိမ့်မယ်။  
```kotlin
val people = listOf(  
    Person("Ali", 24),  
    Person("Reza", 40),  
    Person("Shabnam", 23)  
)  
val sortedPeople = people.sorted()  
println(sortedPeople) // [Person(name=Shabnam, age=23), Person(name=Ali, age=24), Person(name=Reza, age=40)]  
```  

### Regex <a name="regex"></a>  

Regex ဆိုတာ regular expression ရဲ့အတိုကောက်ဖြစ်ပြီး text တွေကို match လုပ်ဖို့နဲ့ manipulate လုပ်ဖို့ အသုံးပြုတဲ့ characters တစ်စဉ်ဖြစ်တယ်။  

Regex အခြေခံများ  

- `.`	Newline မဟုတ်တဲ့ မည်သည့် character နဲ့မဆို match လုပ်မယ်။  
- `^` String တစ်ခုရဲ့ အစ (သို့) multi-line pattern မှာ line တစ်ခုရဲ့ အစနဲ့ match လုပ်မယ်။  
- `\A` String တစ်ခုရဲ့ အစနဲ့ match လုပ်မယ်။  
- `$` String တစ်ခုရဲ့ အဆုံး (သို့) multi-line pattern မှာ line တစ်ခုရဲ့ အဆုံးနဲ့ match လုပ်မယ်။  
- `\Z` String တစ်ခုရဲ့ အဆုံးနဲ့ match လုပ်မယ်။  
- `\b` Word boundary တစ်ခုနဲ့ match လုပ်မယ်။  
- `\B` Word boundary မဟုတ်တဲ့ နေရာတစ်ခုနဲ့ match လုပ်မယ်။  
- `\d` Digit (0-9) တစ်ခုနဲ့ match လုပ်မယ်။  
- `\D` Non-digit တစ်ခုနဲ့ match လုပ်မယ်။  
- `\w` Word character (letter, digit, or underscore) တစ်ခုနဲ့ match လုပ်မယ်။  
- `\W` Non-word character တစ်ခုနဲ့ match လုပ်မယ်။  
- `\s` Whitespace character (space, tab, newline, etc.) တစ်ခုနဲ့ match လုပ်မယ်။  
- `\S` Non-whitespace character တစ်ခုနဲ့ match လုပ်မယ်။  
- `()` Groups  
- `[]` Square brackets ထဲက မည်သည့် character နဲ့မဆို match လုပ်မယ်။  
- `[^]` Square brackets ထဲမှာ မပါတဲ့ မည်သည့် character နဲ့မဆို match လုပ်မယ်။  
- `*`	နောက်ကွယ်က element ရဲ့ 0 သို့မဟုတ် ထို့ထက်ပိုတဲ့ အကြိမ်နဲ့ match လုပ်မယ်။  
- `+`	နောက်ကွယ်က element ရဲ့ 1 သို့မဟုတ် ထို့ထက်ပိုတဲ့ အကြိမ်နဲ့ match လုပ်မယ်။  
- `?`	နောက်ကွယ်က element ရဲ့ 0 သို့မဟုတ် 1 အကြိမ်နဲ့ match လုပ်မယ်။  
- `{n}`	နောက်ကွယ်က element ရဲ့ n အကြိမ်နဲ့ match လုပ်မယ်။  
- `{n,}`	နောက်ကွယ်က element ရဲ့ n သို့မဟုတ် ထို့ထက်ပိုတဲ့ အကြိမ်နဲ့ match လုပ်မယ်။  
- `{n,m}`	�ောက်ကွယ်က element ရဲ့ n နဲ့ m အကြိမ်ကြား match လုပ်မယ်။  

Kotlin က regular expressions တွေနဲ့ အလုပ်လုပ်ဖို့ `matches`, `find`, `findAll`, `replace`, `split` စတဲ့ functions အမျိုးမျိုးကို ပံ့ပိုးပေးပါတယ်။  

ရိုးရှင်းတဲ့ ဥပမာ:  
```kotlin
    val phoneNumber="9112233445"  
    val phoneNumber2="9178"  
    val phoneNumber3="93abc"  
    val regex = Regex("^\\d{10}$")  
    println(regex.matches(phoneNumber)) // true  
    println(regex.matches(phoneNumber2)) // false  
    println(regex.matches(phoneNumber3)) // false  
```
