# 实验2——创建首个Kotlin应用

链接跳转：[主目录](https://github.com/ZW-Q/MySoftware-Development-Practice)	[实验1](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E1)	[实验2](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E2)	[实验3](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E3)	[实验4](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E4)	[实验5](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E5)

```
实验内容
1. 掌握Android Studio开发应用的基本流程
2. 掌握Android Studio开发组件的基本用法
3. 初始Kotlin语言的基本要素
4. 掌握Android Navigation的基本用法
```

## 一、创建并运行第一个Kotlin应用程序

### 1、创建新项目My Application

#### ①**New Project**选择**Basic Activity**

![1](README.assets/1.png)

#### ②设置**Project**基础信息，Language选择**Kotlin**

![2](README.assets/2.png)

#### ③加载gradle

![3](README.assets/3.png)

![4](README.assets/4.png)

#### ④进入`app\build.gradle`查看**dependcies**，出现如下界面即为成功

![5](README.assets/5.png)

#### ⑤Android Studio界面如下

![image-20220422151451644](README.assets/image-20220422151451644.png)

### 2、运行新项目My Application

#### ①创建虚拟机**Create Device**

![6](README.assets/6.png)

#### ②选择API 32镜像

![7](README.assets/7.png)

#### ③设置虚拟机基本信息

![8](README.assets/8.png)

#### ④启动虚拟机Pixel 2

![9](README.assets/9.png)

#### ⑤运行app

![10](README.assets/10.png)

### 二、向页面添加更多的布局

### 1、查看布局编辑器

```
app->res->fragment_first.xml
```

![image-20220422151825406](README.assets/image-20220422151825406.png)

#### ①`fragment_first.xml`，修改**Textview**的**text**属性

```kotlin
android:text="@string/hello_first_fragment"
```

#### ②**Go To > Declaration or Usages**

![image-20220422152730209](README.assets/image-20220422152730209.png)

#### ③跳转到`values/strings.xml`

```kotlin
<string name="hello_first_fragment">Hello first fragment</string>
```

#### ④修改字符串属性值为**“Hello Kotlin!”**

```kotlin
 <string name="hello_first_fragment">Hello Kotlin！</string>
```

#### ⑤修改字体显示属性

在**Design**视图中选择**textview_first**文本组件，在**Common Attributes**属性下的**textAppearance**域，设置相关的文字显示属性

![image-20220422153328035](README.assets/image-20220422153328035.png)

#### ⑥查看xml代码，可见属性修改成功

```kotlin
android:fontFamily="sans-serif-condensed"
android:text="@string/hello_first_fragment"
android:textColor="@android:color/darker_gray"
android:textSize="30sp"
android:textStyle="bold"
```

#### ⑦重新运行程序查看效果

![image-20220422153707764](README.assets/image-20220422153707764.png)

### 2、查看视图的布局约束

#### ①`fragment_first.xml`，查看**TextView**组件的约束属性

```kotlin
app:layout_constraintBottom_toTopOf="@id/button_first"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.498"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent" />
```

#### ②添加按钮和约束

![image-20220422154305578](README.assets/image-20220422154305578.png)

调整**Button**的约束，设置**Button**的`Top>BottonOf textView`

```kotlin
app:layout_constraintTop_toBottomOf="@+id/textview_first" />
```

随后添加**Button**的左侧约束至屏幕的左侧，**Button**的底部约束至屏幕的底部

```kotlin
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toBottomOf="@+id/textview_first"
```

查看**Attributes**面板，修改将id从`button`修改为`toast_button`（注意修改id将重构代码）

![image-20220422155024519](README.assets/image-20220422155024519.png)

查看此**Button**的**xml**文件

```xml
<Button
        android:id="@+id/toast_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="28dp"
        android:layout_marginTop="212dp"
        android:layout_marginBottom="216dp"
        android:text="Button"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textview_first"
/>
```

#### ③调整Next按钮

删除**Next**和**TextView**之间的链，可以在设计视图右键相应约束，选择**Delete**

![image-20220422155549214](README.assets/image-20220422155549214.png)

#### ④添加新的约束

添加**Next**的右边和底部约束至父类屏幕，**Next**的**Top**约束至**TextView**的底部。最后，**TextView**的底部约束至屏幕的底部。效果看起来如下图所示：

![image-20220422161450942](README.assets/image-20220422161450942.png)

### 3、更改组件的文本

#### ①`fragment_first.xml`布局文件代码中，找到toast_button按钮的text属性部分

```kotlin
android:id="@+id/toast_button"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginStart="36dp"
android:layout_marginTop="212dp"
android:text="Button"
```

#### ②选择**Show Context Actions**，并选择**Extract string resource**

![image-20220422162005434](README.assets/image-20220422162005434.png)

#### ③修改**Resource name** 和**Resource value**

![image-20220422162107112](README.assets/image-20220422162107112.png)

### 4、更新Next按钮

#### ①在属性面板中更改**Next**按钮的**id**，从`button_first`改为`random_button`

![image-20220422162411416](README.assets/image-20220422162411416.png)

#### ②在`string.xml`文件，右键**next**字符串资源，选择 **Refactor > Rename**，修改资源名称为**random_button_text**，点击**Refactor** 。随后，修改**Next**值为**Random**

```kotlin
<string name="random_button_text">Random</string>
```

![image-20220422162515219](README.assets/image-20220422162515219.png)

### 5、添加第三个按钮

#### ①向`fragment_first.xml`文件中添加第三个按钮

按钮位于**Toast**和**Random**按钮之间，**TextView**的下方。新**Button**的左右约束分别约束至**Toast**和**Random**，**Top**约束至**TextView**的底部，**Buttom**约束至屏幕的底部

![image-20220422163346094](README.assets/image-20220422163346094.png)

#### ②该按钮的xml文件为

```xml
<Button
android:id="@+id/button2"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Button"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toStartOf="@+id/random_button"
app:layout_constraintStart_toEndOf="@+id/toast_button"
app:layout_constraintTop_toBottomOf="@+id/textview_first" />
```

### 6、完善UI组件的属性设置

#### ①更改新增按钮id为**count_button**

![image-20220422163557847](README.assets/image-20220422163557847.png)

#### ②显示字符串为**Count**，对应字符串资源值为**count_button_text**

![image-20220422163811150](README.assets/image-20220422163811150.png)

#### ③更改**TextView**的文本为**0**

```kotlin
<string name="hello_first_fragment">0</string>
```

#### ④`fragment_first.xml`如下所示

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".FirstFragment">

    <TextView
        android:id="@+id/textview_first"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="sans-serif-condensed"
        android:text="@string/hello_first_fragment"
        android:textColor="@android:color/darker_gray"
        android:textSize="30sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.3"
        />

    <Button
        android:id="@+id/random_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/random_button_text"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toBottomOf="@id/textview_first"
        />

    <Button
        android:id="@+id/toast_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/toast_button_text"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textview_first"
        />

    <Button
        android:id="@+id/count_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/count_button_text"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/random_button"
        app:layout_constraintStart_toEndOf="@+id/toast_button"
        app:layout_constraintTop_toBottomOf="@+id/textview_first" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

#### ⑤运行程序查看效果

![image-20220422164709449](README.assets/image-20220422164709449.png)

## 三、更新按钮和文本框的外观

### 1、添加新的颜色资源

在`values->colors.xml`添加新的颜色

```xml
<color name="screenBackground">#2196F3</color>
<color name="buttonBackground">#BBDEFB</color>
```

### 2、设置组件的外观

#### ①设置屏幕背景色为`@color/screenBackground`

![image-20220422165459268](README.assets/image-20220422165459268.png)

#### ②设置每个按钮的背景色为`@color/buttonBackground`

![image-20220422165633722](README.assets/image-20220422165633722.png)

#### ③移除TextView的背景颜色，设置TextView的文本颜色为color/white，并增大字体大小至72sp

![image-20220422165909676](README.assets/image-20220422165909676.png)

### 3、设置组件的位置

#### ①设置按钮位置

Toast与屏幕的左边距设置为24dp

```kotlin
android:layout_marginStart="24dp"
```

Random与屏幕的右边距设置为24dp

```kotlin
android:layout_marginEnd="24dp"
```

#### ②设置TextView的位置

垂直偏移为0.3

```kotlin
app:layout_constraintVertical_bias="0.3"
```

### 4、运行程序查看效果

![image-20220422170320399](README.assets/image-20220422170320399.png)

### 四、添加代码完成应用程序交互

### 1、TOAST按钮添加一个toast消息

#### ①打开`FirstFragment.kt`文件，在`onViewCreated`方法中使用绑定机制设置**randomButton**按钮的响应事件

```kotlin
override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
    super.onViewCreated(view, savedInstanceState)

    binding.randomButton.setOnClickListener {
        findNavController().navigate(R.id.action_FirstFragment_to_SecondFragment)
    }
}
```

#### ②为**TOAST**按钮添加事件，使用**findViewById()**查找按钮**id**

```kotlin
// find the toast_button by its ID and set a click listener
view.findViewById<Button>(R.id.toast_button).setOnClickListener {
    // create a Toast with some text, to appear for a short time
    val myToast = Toast.makeText(context, "Hello Toast!", Toast.LENGTH_LONG)
    // show the Toast
    myToast.show()
}
```

### 2、使**Count**按钮更新屏幕的数字

#### ①在`FirstFragment.kt`文件，为**count_buttion**按钮添加事件

```kotlin
view.findViewById<Button>(R.id.count_button).setOnClickListener {
   countMe(view)
}
```

#### ②**countMe()**为自定义方法，以**View**为参数，每次点击增加数字1

```kotlin
//    count方法，自增1
private fun countMe(view: View) {
    // Get the text view
    val showCountTextView = view.findViewById<TextView>(R.id.textview_first)

    // Get the value of the text view.
    val countString = showCountTextView.text.toString()

    // Convert value to a number and increment it
    var count = countString.toInt()
    count++

    // Display the new value in the text view.
    showCountTextView.text = count.toString()
}
```

