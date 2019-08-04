# c++目录

- 第一章 绪论
	- 计算机程序设计语言的发展
		- 机器语言与汇编语言
				- 现在使用的高等语言会先转换成汇编语言，然后再由汇编语言转换成机器语言
		- 高级语言
			- 比如c，c++，java，python
		- 面向对象的语言
			- 比如c++（c++和object c不是一个东西，是不同的）
	- 面向对象的方法
		- 面向对象的方法的由来
			- 程序模块间的关系更为简单，程序模块的独立性、数据的安全性就有了良好的保障。
			- 通过继承与多态性，可以大大提高程序的可重用性，使得软件的开发和维护都更为方便。
		- 面向对象的基本概念
			- 把具有共性的东西抽象并且封装成为一个对象
	- 面向对象的软件开发
		- 分析
		- 设计
		- 编程
		- 测试
		- 维护
	- 信息的表示与存储
		- 计算机的数字系统
			- 就是由0和1二进制组成的东西
		- 几种进制记数制之间的转换
			- 根据加权数位计算就可以了
		- 信息的存储单位
			- 存储单位是字节（byte），最小的存储单位是字（bit）
		- 原码，反码，补码
			- 正数的反码与原码表示相同。
			- 负数的反码与原码有如下关系：
				- 符号位相同(仍用1表示)，其余各位取反(0变1，1变0)。例如：
					- $X=-1100110_{(2)}$ $X_原 =11100110_{(2)}$ $X_反 =10011001_{(2)}$
					- $X=+0000000_{(2)}$ $X_原 =00000000_{(2)}$ $X_反 =00000000_{(2)}$
					- 反码中零的表示也不惟一
					- $X=-0000000_{(2)}$ $X_原 =10000000_{(2)}$ $X_反 =11111111_{(2)}$
			- 反码只是求补码的中间码
			- 计算机中的补码表示法
				负数的补码由该数反码的末位加 1 求得
				对补码再求补即得到原码
			- 补码运算规则
				符号位可作为数值参加运算
			- 减法运算可转换为加法运算：
				加上一个负数等于加上该数的补码
				补码运算的结果仍为补码
			- 如果运算结果溢出：
				负数之和得正数，或正数之和得负数
		- 二进制数的编码表示
			- 优点：易于物理实现
							二进制数运算简单
							机器可靠性高
							通用性强
		- 定点数和浮点数
			- 定点数就是我们所谓的整数，在二进制中也是在小数点前面的数；而浮点数就是我们生活中常常说的小数部分。在计算机二进制语言中，表达小数是存在偏差的，所以在这种时候要表示一个整数的时候就需要用到数位加权
		- 数的表示范围
			- 根据这个数分配到的空间和使用这个空间的方法来确定这个数字能够表示的范围
		- 非数值信息的表示
			- 通过内存空间来达到目的
	- 程序开发的基本概念
		- 基本术语
		- 完整的程序过程
		- 实数的表示方法
			- 计算机中通常采用浮点方式表示实数一个数 $N$ 用浮点形式表示可以写成： 
				-	$N = M \times 2^E$
				- $E$表示2的幂，称为数$N$的阶码。阶码确定了数$N$的小数点的位置，其位数影响该浮点数所表示的范围。
				- $M$表示数$N$的全部有效数字，称为数$N$的尾数。其位数影响数据的精度。
		- 非数值信息的表示
			- 西文字符：
				- ASCII码：用7位二进制数表示一个字符，最多可以表示$2^7=128$个字符
				- EBCDIC码：用8位二进制数表示一个字符，最多可以表示$2^8=256$个字符
			- 汉字：
				- 应用较为广泛的是"国家标准信息交换用汉字编码"(GB2312-80标准)，简称国标码。是二字节码，用二个七位二进制数编码表示一个汉字。
- 第二章 c++简单程序设计
	- c++语言概述
		- c++的产生
		- c++的特点
		- c++程序示实例
		- 字符集
		- 词法记号
	- 基本数据类型和表达式
		- 基本数据类型
		- 常量
		- 变量
		- 符号常量
		- 运算符与表达式
			- 特别需要注意的优先级`！> && > ||`
		- 语句
	- 数据的输入与输出
		- I/O流
			- 就是输入输出流
		- 预定义的插入符和提取符
		- 简单的I/O格式控制
	- 算法的基本控制结构
		- 用`if`语句实现选择结构
		- 多重选择结构
		- 循环结构
			- `for（执行前求解；为true的时候开始执行；执行后求解）`
		- 循环结构与选择节后的嵌套
		- 其他控制语句
			- `break`语句
				- 使程序从循环体和`switch`语句内跳出，继续执行逻辑上的下一条语句。不宜用在别处。
			- `continue` 语句
				- 结束本次循环，接着判断是否执行下一次循环。
			- `typedef` 为一个已有的数据类型另外命名
			- 对于`enum`
				- 枚举类型应用说明：
					- 对枚举元素按常量处理，不能对它们赋值。例如，不能写：`SUN = 0;`
					- 枚举元素具有默认值，它们依次为： 0,1,2,......。也可以在声明时另行指定枚举元素的值，如：`enum Weekday{SUN=7,MON=1,TUE,WED,THU,FRI,SAT};`枚举值可以进行关系运算。
					- 整数值不能直接赋给枚举变量，如需要将整数赋值给枚举变量，应进行强制类型转换。
	- 自定义数据类型
		- `typedef`申明
		- 枚举类型`enum`
		- `using`
	- 深度搜索
		- 变量的实现机制
		- c++表达式的执行原理

- 第三章函数
	- 函数的定义与使用
		- 函数的定义
			- 类型名 函数名 （函数参数表）
			- - 其中函数参数表中的变量，寿命和可见性都在函数的内部
		- 函数的调用
			- `rand`
				- 函数原型：`int rand(void);`
				- 所需头文件：`include<random>`
				- 功能和返回值：求出并返回一个伪随机数
			- `srand`
				- 函数原型：`void srand(unsigned int seed);`
				- 参数：seed产生随机数的种子。
				- 所需头文件：`include<random>`
				- 功能：为使`rand()`产生一序列伪随机整数而设置起始点。使用1作为seed参数，可以重新初化`rand()`。
			- 在`rand()`和`srand()`的括号里面可以输入种子名
		- 函数的参数传递
	- 内联函数
		- 声明时使用关键字 `inline`。为了提高运行时的效率，对于较简单的函数可以声明为内联形式。
			- **注意**`inline`已经于C++17废弃
			- 使用内联函数的注意事项：内联函数体中不要有复杂结构（如循环语句和`switch`语句）。
				在类中声明内联成员函数的方式：将函数体放在类的定义中。编译时在调用处用函数体进行替换,节省了参数传递、控制转移等开销。
			- 注意：
				- 内联函数体内不能有循环语句和`switch`语句。
				- 内联函数的声明必须出现在内联函数第一次被调用之前。
				- 对内联函数不能进行异常接口声明。
```cpp
#include <iostream>
using namespace std;

const double PI = 3.14159265358979;
inline double calArea(double radius) {
	return PI * radius * radius;
}

int main() {
	double r = 3.0;
	double area	= calArea(r);
	cout << area << endl;
	return 0;
}
```
- 带默认形参值的函数
	- 函数在声明时可以预先给出缺省的形参值，调用时如给出实参，则采用实参值，否则采用预先给出的缺省形参值。
```cpp
int add(int x = 5,int y = 6) {
	return x + y;
}
int main() {
	add(10,20);//10+20
	add(10);  //10+6
	add();  //5+6
}
```
- 函数重载
  - C++允许功能相近的函数在相同的作用域内以相同函数名声明，从而形成重载。方便使用，便于记忆。
```cpp
int add(int x, int y);
float add(float x, float y);
```
- 重载函数的形参必须不同:个数不同或类型不同。
编译程序将根据实参和形参的类型及个数的最佳匹配来选择调用哪一个函数。
不要将不同功能的函数声明为重载函数，以免出现调用结果的误解、混淆。
除此之外，编译器不已形式参数的名字（但是形式参数的名字是可以用于区别重载函数的）和返回值为区别重载函数的方法
- c++系统函数
与c语言中的系统函数类似
- 深度搜索
	- 运行栈与函数调用的执行
		- 运行栈
			- 运行栈是一段区域的内存空间，分为一个一个栈帧，每个栈帧对应一次函数调用。
			- 栈帧中包括：
				- 本次函数调用的形参值
				- 控制信息
				- 局部变量值
				- 一些临时数据
			- 函数调用时，会有一个栈帧被压入运行栈
				返回时，会有一个栈帧被弹出
		- 函数声明与类型安全

- 第四章 类与对象
	- 面向对象程序设计的基础
		- 抽象
			抽象出一个对象的属性，比如一个人的身高体重等等
		- 封装
			- 把对象的属性和服务结合成一个独立的系统单元。
				表现为：尽可能隐蔽对象的内部细节。对外形成一个边界（或者说一道屏障），只保留有限的对外接口使之与外部发生联系。
		- 继承
			- 继承对于软件复用有着重要意义，是面向对象技术能够提高软件开发效率的重要原因之一。是C++中支持层次分类的一种机制。
				继承允许程序员在保持原有类特性的基础上，进行更具体的说明。
			- 定义：特殊类的对象拥有其一般类的全部属性与服务，称作特殊类对一般类的继承。
				- 例如：将轮船作为一个一般类，客轮便是一个特殊类。
	- 多态
    - 多态是指在一般类中定义的属性或行为，被特殊类继承之后，可以具有不同的数据类型或表现出不同的行为。这使得同一个属性或行为在一般类及其各个特殊类中具有不同的语义。
		- 例如：
			- 数的加法->实数的加法->复数的加法
	- 类和对象
		- 类的定义
			- 类是实现信息封装的基础，是一种用户定义类型，也称类类型。每个类包含数据说明和一组操作数据或传递消息的函数。类的实例称为对象。
			- 类是面向对象程序设计中的概念，是面向对象编程的基础。
			- 类的实质是一种数据类型，类似于int、char等基本类型，不同的是它是一种复杂的数据类型。因为它的本质是类型，而不是数据，所以不存在于内存中，不能被直接操作，只有被实例化为对象时，才会变得可操作。
			- 类是对现实生活中一类具有共同特征的事物的抽象。如果一个程序里提供的类型与应用中的概念有直接的对应，这个程序就会更容易理解，也更容易修改。一组经过很好选择的用户定义的类会使程序更简洁。此外，它还能使各种形式的代码分析更容易进行。特别地，它还会使编译器有可能检查对象的非法使用。 
		- 类的封装
			- 类的内部封装了方法，用于操作自身的成员。类是对某种对象的定义，具有行为，它描述一个对象能够做什么以及做的方法，它们是可以对这个对象进行操作的程序和过程。它包含有关对象行为方式的信息，包括它的名称、方法、属性和事件。
		- 类的构成
			- 类的构成包括数据成员和成员函数。数据成员对应类的属性，类的数据成员也是一种数据类型，并不需要分配内存。成员函数则用于操作类的各项属性，是一个类具有的特有的操作，比如“学生”可以“上课”，而“水果”则不能。类和外界发生交互的操作称为接口
			- 类/结构体的赋值
				- 如果初值个数少于结构体成员个数，则将无初值对应的成员赋以0值。如果初值个数多于结构体成员个数，则编译出错。
			- 例子：定义一个类
```cpp
class 类名
{
	public:	
		公有成员
	private:
		私有成员
 	protected:
		保护成员
};
```
  - 公有成员、私有成员、保护成员均包含数据成员和成员函数两部分，彼此没有顺序之分。一个public/private/protected关键字下可以跟多个成员，直到下一个public/private/protected关键字。如果成员前面没有public/private/protected关键字，那么在c++的类中默认为私有成员。
  - 结尾部分的分号必不可少，否则会发生语法错误。
  - 无论公有成员、私有成员还是保护成员，彼此之间都可以访问。比如公有的成员函数可以操作保护的数据成员，也可以调用私有的成员函数。
  - 类的数据成员是类型，所以不能被赋值，声明数据成员和声明普通变量的格式相同，比如“int n;”。
- 成员函数的实现
	- 成员函数可以在类内实现，也可以在类外实现。
		- `特别注意`：内部实现的成员函数被默认为加上了inline；外部实现的成员函数必须加上域操作符，即“类名::成员函数”。
- 构造函数与析构函数
	- 构造函数和析构函数是特殊的成员函数，和普通成员函数不同的地方在于：
    函数名固定
    构造函数和析构函数的函数名必须是类名。
    声明格式不同
    构造函数和析构函数没有返回值，连空返回值——void也没有。
    -	构造函数和析构函数的申明形式： 
		构造函数的声明形式：类名(参数列表);
    析构函数的声明形式：~类名();
    - 重载的特殊性
    构造函数（存在参数列表）和普通成员函数一样可以被重载，析构函数不可以重载，只能是空参数。
    - 调用过程不同
    	- 构造函数和析构函数不能被显式地调用，只能由编译器自动调用。
		- 构造函数用于创建类的对象，任何创建对象的行为，都会导致构造函数被调用。析构函数和构造函数的功能相反，析构函数用于销毁对象，当类的对象超出作用域被销毁时，析构函数被调用。
			- 即使显式地定义构造函数和析构函数，也还是会有默认的构造函数和析构函数，函数内部无任何语句，不执行任何操作。默认构造函数是无参数的。需要注意的是，一旦显式定义任意形参的构造函数，默认构造函数都不会生成，即只有没有定义构造函数的类才存在默认构造函数。 
			-	一般情况下，默认的构造函数和析构函数可以满足功能需要，然而当需要重载构造函数，或是需要动态分配资源的时候，就不得不定义自己的构造函数甚至析构函数了。
			- 拷贝构造函数是特殊的构造函数，在复制对象时被调用，定义的格式为“类名(类名& 参数名)”。拷贝构造函数也存在默认的，但很多情况下都需要重载。
- 类的实例化：
	- 就像声明某种类型的变量一样，声明一个类类型的对象，就是类的实例化，会涉及到必要的内存分配。
不同语言中类的实例化形式是不同的。
  - C++
    - 类名 对象名(参数列表);
    - 如果没有参数，括号必须省略，即“类名 对象名;”，自动调用构造函数。特殊地，参数可以是类的对象，此时会自动调用拷贝构造函数。
  - Java/C#
    - 类名 对象名 = new 类名(参数列表);
    - 括号不能省略。
- 对象可以访问类的成员，但并不是所有成员都可以被访问，能否访问取决于声明该成员时所用的关键字（public/protected/private）。具体规则如下：
  - 类的公有成员可以被该类，其派生类和类实例化的对象访问。
  - 类的保护成员可以被该类及其派生类访问，不可以被该类的对象访问。
  - 类的私有成员可以被该类访问，不可以被派生类及其该类的对象访问。
- 派生与继承	
	- 举例：
```cpp
class 子类类名：
public 父类类名,private 父类类名,protected 父类类名
{
public:
公有成员
private:
私有成员
protected:
保护成员
};
```
  -	子类即是继承而来的类，父类即是被继承的类，或者称之为基类。
    public修饰的为公有继承，private修饰的为私有继承，protected修饰的为保护继承。
    父类可以只有一个，也可以有多个。只有一个父类称为单继承，多个父类称为多继承。C++支持多继承的机制，Java则只具有单继承功能，并增加了“接口”的概念，一个类可以实现多个接口。
    -	如果不标明继承方式，默认为私有继承。
-	派生和继承
	- 派生和继承是类的重要特性，继承是由抽象到具体的体现。通过继承，子类可以使用父类的成员。
		- 但要注意的是，派生和继承在带来方便的同时，也会使类与类之间的关系变得复杂，尤其是涉及到私有继承和保护继承时，类中成员的关系可能会变得难以理解。所以在涉及类时，尽量避免过多层次的继承，私有继承和保护继承的使用也要慎重。
	- 继承来的成员和自身声明的成员并无本质区别，也有公有成员、私有成员、保护成员之分。继承时，父类中成员类型（公有成员/私有成员/保护成员）和继承方式（公有继承/私有继承/保护继承）不同，情况不同。可以归纳为：
	- 三种类型的继承，父类的成员均被子类继承，只是由类实例化的对象对其继承的成员的访问权限会有所变化。三种不同方式的继承，描述的是子类实例化对象对其成员的访问权限，并非是描述子类时，子类对继承自父类的成员的访问权限。
	- 三种继承方式
    - 公有继承
    - 继承自父类的成员保持不变。
    - 私有继承
    - 继承自父类的成员全部变为私有成员。
    - 保护继承
    - 继承自父类的公有成员变为保护成员，其余不变。
- 操作符重载
	- 操作符重载必须在类中进行，重载操作符可以使操作符对在类中的语义发生变化。除了. ，.* ，：： ，? : 、sizeof、typeid这几个运算符不能重载之外，大部分运算符都能被重载。但要注意，重载操作符并不能改变操作符的优先级和结合律，而且从认知规律上讲，重载的操作符功能必须与原意相近，否则很难被人理解。
	- 操作符重载是函数，在使用该操作符时被调用。操作符重载函数的声明形式：返回值 operator操作符(参数列表);
- 友元
	- 友元可以是函数，被称为友元函数；也可以是类，被称为友元类。
	- 通常，类中的私有成员只能被自身使用，无法被它的对象访问。因此，另一个类即便可以使用该类的对象，也无法访问该类的私有成员，通过定义友元的方法可以做到这一点。
		- 友元就是在一个类中“再次声明”另一个类的成员函数或是另一个类，被“再次声明”的成员函数或类可以访问该类的私有成员。这种“再次声明”并不是普通的声明，格式为：friend 函数/类名;
			- 显然，友元会破坏类的封装性，使本该隐藏的成员暴露出来，因此应当谨慎使用。
- 组合
继承可以描述“交通工具”和“公交车”的关系，却无法描述“公交车”和“车轮”的关系。大致意思就是继承可以增加这一个系列的东西，但是不能阐释这个东西的一个部分。
  - 大多数“车轮”具有的特性是“公交车”所不具有的。比如说“车轮”具有“重量”，而“公交车”的“重量”则是另一个含义。而通过私有成员、保护成员机制控制这些成员的继承性，会使继承变得复杂而难以理解。而且继承来的数据成员只有一个，而一辆“公交车”却有四个“车轮”，四个“车轮”的“重量”。
	- 引入组合的概念，“公交车”完全可以由“车轮”、“方向盘”、“车身”等类组合而来。方法就是将类当成其他的数据类型一样，在另一个类中定义该类类型的数据成员。
- 抽象类
	- 并不是所有种类的事物都可以被实例化，换而言之，有的种类只是一种抽象概念，现实中并没有实际存在的对应物。比如：假设所有的动物都会叫，我们可以定义一个类——“动物”，定义类中的一个成员函数——“叫”，我们知道猫的叫声，也知道狗的叫声，然而“动物”是如何“叫”的？——我们根本无法实现它。所以，我们引入了抽象类的概念，抽象类是无法被实例化的，无法声明抽象类的对象。
		- 通常，用 abstract 修饰的类是抽象类；C++中包含纯虚函数的类是抽象类；Java中含有抽象方法的类是抽象类；继承了纯虚函数而没有实现它的类也是抽象类。
		- 抽象类只能被用作基类，作用体现在：
约束派生类必须实现的成员函数或方法。
不同派生类中同名的成员函数实现不同，体现了多态性。
- 静态成员
	用static修饰的成员是静态成员，可以是成员函数或数据成员。静态成员是所有对象共有的，只分配一次内存，产生新的对象时不会产生副本。
	静态数据成员的初始化必须在类外进行，使用静态成员时必须使用类名和域操作符。
- 类的三大特性
	- 封装性
    将数据和操作封装为一个有机的整体，由于类中私有成员都是隐藏的，只向外部提供有限的接口，所以能够保证内部的高内聚性和与外部的低耦合性。用者不必了解具体的实现细节，而只是要通过外部接口，以特定的访问权限来使用类的成员，能够增强安全性和简化编程。
  - 继承性
    继承性更符合认知规律，使程序更易于理解，同时节省不必要的重复代码。
	- 多态性
    同一操作作用于不同对象，可以有不同的解释，产生不同的执行结果。在运行时，可以通过指向基类的指针，来调用实现派生类中的方法。
- 类与结构体的区别
		在C++中，class和struct都可以定义一个类，它们的区别如下：
    从职能观点来看，class表现为行为；而struct常用于存储数据。
    class支持继承，可以继承自类和接口；而struct没有继承性，struct不能从class继承，也不能作为class的基类，但struct支持接口继承。
    class可以声明无参构造函数，可以声明析构函数；而struct只能声明带参数构造函数，且不能声明析构函数。因此，struct没有自定义的默认无参构造函数，默认无参构造器只是简单地把所有值初始化为它们的0等价值。
    class可以实现抽象类（abstract），可以声明抽象函数；而struct为抽象，也不能声明抽象函数。
    class可以声明protected成员、virtual成员、sealed成员和override成员；而struct不可以，但是值得注意的是，struct可以重载System.Object的3个虚方法，Equals()、ToString()和 GetHashTable()。
    class的对象复制分为浅拷贝和深拷贝，必须经过特别的方法来完成复制；而struct创建的对象复制简单，可以直接以等号连接即可。
    class实例由垃圾回收机制来保证内存的回收处理；而struct变量使用完后立即自动解除内存分配。
    作为参数传递时，class变量是以按址方式传递；而struct变量是以按值方式传递的。

		- 我们可以简单的理解，class是一个可以动的机器，有行为，有多态，有继承；而struct就是个零件箱，组合了不同结构的零件。其实，class和struct最本质的区别就在于class是引用类型，内存分配于托管堆；而struct是值类型，内存分配于线程的堆栈上。由此差异，导致了上述所有的不同点。所以只有深刻的理解内存分配的相关内容，才能更好的驾驭。
		- 当然，使用class基本可以替代struct的任何场合，class后来居上。虽然在某些方面struct有性能方面的优势，但是在面向对象编程里，基本是class横行的天下。
		- 相对于class，struct存在的意义是他的性能比class更加优异

    - 比如：实现一个主要用于存储数据的结构时，可以考虑struct。
   		struct变量占有堆栈的空间，因此只适用于数据量相对小的场合。
    	struct数组具有更高的效率。

- 类的复用
	- 举例：
```cpp
class Animal
{
private voidbeat()
{
System.out.println("");
}
public voidbreath()
{
beat();
System.out.println("")
}
}
class bird
{
//
private Animala;
public Bird(Animala)
{
this.a=a;
}
//
pubilc voidbreath()
{
//
a.breath();
}
public voidfly()
{
System.out.println("")
}
}
class Wolf
{
//
private Animala;
}
```
		- 如果初值个数少于结构体成员个数，则将无初值对应的成员赋以0值。如果初值个数多于结构体成员个数，则编译出错。
		- 类成员的访问控制
			- 在关键字public后面声明，它们是类与外部的接口，任何外部函数都可以访问公有类型数据和函数。
			- 在关键字private后面声明，只允许本类中的函数访问，而类外部的任何函数都不能访问。
			- protected与private类似，其差别表现在继承与派生时对派生类的影响不同
		- 类的成员数据
			- 与一般的变量声明相同，但需要将它放在类的定义体中。
			- 在类中说明原型，可以在类外给出函数体实现，并在函数名前使用类名加以限定。也可以直接在类中给出函数体，形成内联成员函数。
		- 对象
			- 类的对象是该类的某一特定实体，即类类型的变量。
			- 定义形式： 类名  对象名；
				- 例： Clock  myClock;
		- 类的成员函数
			- 类中成员互访：
					直接使用成员名
			- 类外访问
					使用“对象名.成员名”方式访问 public 属性的成员
	- 构造函数和析构函数
		- 当用类的一个对象去初始化该类的另一个对象时系统自动调用拷贝构造函数实现复制。
```cpp
int main() {
  Point a(1,2);
  Point b = a; //拷贝构造函数被调用。也可以写Point b(a); 
  cout << b.getX() << endl;
}
```
			- 若函数的形参为类对象，调用函数时，实参赋值给形参，系统自动调用拷贝构造函数。
				- 例如：
```cpp
void fun1(Point p) {
  cout << p.getX() << endl;
} 
int main() {
  Point a(1, 2);
  fun1(a); //调用拷贝构造函数
  return 0;
}     
```
			- 当函数的返回值是类对象时，系统自动调用拷贝构造函数。
				- 例如：
```cpp
Point fun2() {
  Point a(1, 2);
  return a; //调用拷贝构造函数
}
int main() {
  Point b;
  b = fun2();
  return 0; 
}
```
		- 构造函数
			- 构造函数的作用是在对象被创建时使用特定的值构造对象，或者说将对象初始化为一个特定的状态。
			- 构造函数在对象创建时由系统自动调用。
			- 如果程序中未声明，则系统自动产生出一个隐含的参数列表为空的构造函数
			- 允许为内联函数、重载函数、带默认形参值的函数
```cpp
class Clock {
public:
	Clock(int newH,int newM,int newS);//构造函数
	void setTime(int newH, int newM, int newS);
	void showTime();
private:
	int hour, minute, second;
};
```
```cpp
//构造函数的实现：
Clock::Clock(int newH, int newM, int newS) {
	hour = newH;
	minute = newM;
	second = newS;
}
//建立对象时构造函数的作用：
int main() {
  Clock c(0,0,0); //隐含调用构造函数，将初始值作为实参。
  c.showTime();
	return 0;
}
```
		- 拷贝构造函数是一种特殊的构造函数，其形参为本类的对象引用。
```cpp
class 类名 {
public :
    类名（形参）；//构造函数
    类名（类名 &对象名）；//拷贝构造函数
           ...
}；
类名::类（类名 &对象名）//拷贝构造函数的实现
{    函数体    }
```
```cpp
class Point {
public:
	Point(int xx=0, int yy=0) { x = xx; y = yy; }
	Point(Point& p);
	int getX() { return x; }
	int getY() { return y; }
private:
	int x, y;
};
```
```cpp
Point::Point (Point& p) {
  x = p.x;
  y = p.y;
  cout << "Calling the copy constructor " 	<< endl;
}
```
		- 赋值构造函数
		- 隐含的拷贝构造函数
			- 如果程序员没有为类声明拷贝初始化构造函数，则编译器自己生成一个隐含的拷贝构造函数。
这个构造函数执行的功能是：用作为初始值的对象的每个数据成员的值，初始化将要建立的对象的对应数据成员。
		- 析构函数
			- 完成对象被删除前的一些清理工作。
				- 在对象的生存期结束的时刻系统自动调用它，然后再释放此对象所属的空间。
				- 如果程序中未声明析构函数，编译器将自动产生一个隐含的析构函数。
			- 程序实例
```cpp
#include <iostream>
using namespace std;
class Point {     
public:
  Point(int xx,int yy);
  ~Point();
  //...其他函数原型
private:
  int x, y;
};
Point::Point(int xx,int yy) {
  x = xx;
  y = yy;
}
Point::~Point() {
}
//...其他函数的实现略
```
	- 构造函数调用顺序
		- 构造函数调用顺序：先调用内嵌对象的构造函数（按内嵌时的声明顺序，先声明者先构造）。然后调用本类的构造函数。（析构函数的调用顺序相反）
		- 初始化列表中未出现的内嵌对象，用默认构造函数（即无形参的）初始化
		- 系统自动生成的隐含的默认构造函数中，内嵌对象全部用默认构造函数初始化
```cpp
class Part { //部件类
public:
  Part();
  Part(int i);
  ~Part();
  void Print();
private:
  int val;
};
class Whole {
public:
  Whole();
  Whole(int i, int j, int k);
  ~Whole();
  void Print();
private:
  Part one;
  Part two;
  int date;
};
Whole::Whole() {
  date=0;
}
Whole::Whole(int i, int j, int k): two(i), one(j), date(k)
{}
//...其他函数的实现略
```
以下定义了三个Student、Teacher和Tourpair，其中Student类的对象和Teacher类的对象作为了Tourpair的数据成员，观察对象的构造过程和构造函数被执行的顺序。
```cpp
#include <iostream>
class Student
{ public: 
   Student()
    { cout<<”construct student.\n”;
       semeshours=100;       gpa=3.5;   }   
protected:
     int semeshours;     float gpa;
};
class Teacher
{ public:
     Teacher()
   { cout<<”construct Teacher.\n”;     }
 };
class Tourpair
{public:
     Tourpair()
     {cout<<”construct tourpair.\n”;
      nomeeting=0;  }
  protected:
      Student student;
      Teacher teacher;
      int nomeeting;
 };
class Tourpair
{public:
     Tourpair()
     {cout<<”construct tourpair.\n”;
      nomeeting=0;  }
  protected:
      Student student;
      Teacher teacher;
      int nomeeting;
 };
 ```
 			- 由此可见：主函数main()运行开始时，遇到要创建Tourpair类的对象，于是调用其构造函数Tourpair（），该构造启动时，首先分配对象空间（包含一个Student对象、一个Teacher对象和一个int型数据）,然后根据其在类中声明的对象成员的次序依次调用其构造函数。即先调用Student()构造函数，后调用Teacher()构造函数，最后才执行它自己的构造函数的函数体。
    		- 由于上例中Tourpair类的数据成员student和teacher的构造函数都是无参函数，所以系统在构造student和teacher对象时会自动调用各自的构造函数Student()和Teacher()，而不需要用初始化表的方式去调用。
- 类的组合
	- 组合
		- 类中的成员数据是另一个类的对象。
			- 可以在已有抽象的基础上实现更复杂的抽象。
```cpp
class Point {
private:
  float x, y; //点的坐标
public:
  Point(float h, float v); //构造函数
  Point(Point &p);
  float getX(); //取X坐标
  float getY(); //取Y坐标
};
//...函数的实现略
class Line {
private:
  Point p1, p2; //线段的两个端点
  double len;	
public:
  Line(Point a, Point b); //构造函数
  Line (Line &);
	double GetLen(){return len;}
};
//...函数的实现略
```
		- 前向引用声明
- UML图形标志
	- UML简介
		- UML语言是一种可视化的的面向对象建模语言。
	- UML有三个基本的部分
		- 事物（Things） UML中重要的组成部分，在模型中属于最静态的部分，代表概念上的或物理上的元素
		- 关系（Relationships） 关系把事物紧密联系在一起
		- 图（Diagrams） 图是很多有相互相关的事物的组
	- UML类图
		- 实质上更加类似于是类的一个框架
	- 结构体和联合体
		- 结构体
			- 结构体就是struct关键字
		- 联合体
			- 联合体的关键字是union关键字
	- 深度探索
		- 位域
			- 位域：bitsec，意义是把一个字节分成几个部分进行分段操作，一个字节由8个字组成，把这一个字节中的八个字分开进行使用，每一个空间称为位域
		- 用构造函数定义类型转换
		- 对象作为函数参数和返回值的传递方式
		- 隐含转换
			- 由构造函数确立的类型转换，可以隐含执行
				- 例：Line x(1, 4);
					- 效果：构造以(1,0)和(4,0)两坐标为端点的线段，这里Point的构造函数被隐含调用，避免隐含转换的发生。在构造函数中使用explicit关键字，explicit要写在类定义中的构造函数前
```cpp
#include <iostream>
using namespace std;
class Complex{ //复数类
private:
  float real, imag;	//复数的实部和虚部
public:
  //构造函数，可以当作隐式类型转换使用
  Complex(float real = 0, float imag = 0) : real(real), imag(imag) { }
  Complex add(Complex c) {	//复数加法，生成临时对象并返回
    return Complex(real + c.real, imag + c.imag);
  }
  Complex sub(Complex c) {	//复数减法，生成临时对象并返回
    return Complex(real - c.real, imag - c.imag);
  }
  Complex mul(Complex c) {	//复数乘法，生成临时对象并返回
    return Complex(real * c.real - imag * c.imag, real * c.imag + imag * c.real);
  }
  void show() {  //显示复数
    if (imag >= 0)
      cout << real << " + " << imag << 'i' << endl;
    else
      cout << real << " - " << -imag << 'i' << endl;
  }
};
int main() {
	Complex z(1, 2);		//z = 1 + 2i
	z.add(Complex(3, 4)).show(); 	//Complex(3, 4)是临时对象
	static_cast<Complex>(5).sub(z).show(); //输出5 – z，使用了显示类型转换
	z.mul(-3.0f).show(); //输出z * (-3)，使用了隐含类型转换
	return 0;
}
```
- 成员函数的调用
	- 成员函数调用的实现机制
		- 问题的关键：如何传递调用的目的对象
		- 解决办法：把目的对象的引用当作参数传递
		- 示例代码
```cpp
		void Clock::setTime(int newH, int newM, int newS) {
  hour = newH;
  minute = newM;
  second = newS;
}
```
```cpp
void Clock_setTime(_Clock &_this, int newH, int newM, int newS) {
  _this.hour = newH;
  _this.minute = newM;
  _this.second = newS;
}
```
- 对象作为参数的传递方式
	- 对象参数的传递方式：
		- 通过运行栈来传递
	- 主调函数调用拷贝构造函数，在运行栈的传参区域上创建对象
		- 被调函数可以读取传参区域上的对象
			- `注意`有时对拷贝构造函数的调用可以省去
				例：z.add(Complex(3, 4))
		- 直接调用构造函数Complex(float, float)，在运行栈的传参区域上建立对象
- 传递方式
	- 在主调函数中创建临时对象
	- 主调函数把该对象地址（引用）传递给被调函数
		- 被调函数返回时，在该地址上执行拷贝构造
		- `注意`有时返回时可以不调用拷贝构造函数
			例：return Point(1, 2);
		- 直接调用构造函数Point(int, int)，生成返回的对象
		- `注意`有时主调函数中可以不建立临时对象
			例：Point p = fun2();
		- 先为p申请空间，调用fun2()前传递p的地址，这样在返回时可直接在p的空间上构造返回对象
- 第五章 数据的共享和保护
	- 标识符的作用域与可见性
		- 作用域
			- 类作用域作用于特定的成员名。
				- 举例:
			类X的成员m具有类作用域，对m的访问方式如下： 
			如果在X的成员函数中没有声明同名的局部作用域标识符，那么在该函数内可以访问成员m。
			通过表达式x.m或者X::m访问。
			通过表达式ptr->m
		- 可见性
			- 标识符应声明在先，引用在后。
					如果某个标识符在外层中声明，且在内层中没有同一标识符的声明，则该标识符在内层可见。
					对于两个嵌套的作用域，如果在内层作用域内声明了与外层作用域中同名的标识符，则外层作用域的标识符在内层不可见。
	- 对象的生存期
			- 对象从产生到结束的这段时间就是它的生存期。在对象生存期内，对象将保持它的值，直到被更新为止。
		- 静态生存期
			- 好像就是外部成员static变量申明的变量名
		- 动态生存期
			- 好像是由auto申明的变量名
	- 类的静态成员
		- 静态数据成员
			- 这种生存期与程序的运行期相同。
			- 在文件作用域中声明的对象具有这种生存期。
			- 在函数内部声明静态生存期对象，要冠以关键字static 。
```cpp
#include<iostream>
using namespace std;
int i = 5;   //文件作用域
int main() {
     cout << "i=" << i << endl;
     return 0;
}

//i具有静态生存期
```
	- 动态生存区
		- 块作用域中声明的，没有用static修饰的对象是动态生存期的对象（习惯称局部生存期对象）。开始于程序执行到声明点时，结束于命名该标识符的作用域结束处。
			- 代码示例
```cpp
#include <iostream>
using namespace std;
void fun();
int main() {
  fun();
  fun();
}
void fun() {
  static int a=1;
  int i=5;
  a++;
  i++;
  cout<<"i="<<i<<",a="<<a<<endl;
}
```
- 举例子
```cpp
#include<iostream>
//具有静态、动态生存期对象的时钟程序
using namespace std;
class Clock{//定义时钟类
public:
//外部接口
	Clock();
	void setTime(int newH, int newM, int newS);   //三个形参均具有函数原型作用域
	void showTime();
private:	//私有数据成员
	int hour, minute, second;
};
Clock::Clock() : hour(0), minute(0), second(0) { }	//构造函数

void Clock::setTime(int newH, int newM, int newS) {
//三个形参均具有局部作用域
	hour = newH;
	minute = newM;
	second = newS;
}

void Clock::showTime() {
	cout << hour << ":" << minute << ":" << second << endl;
}
Clock globClock;//声明对象globClock，
                //具有静态生存期，文件作用域
int main(){ //主函数
cout << "First time output:" << endl;	
//引用具有文件作用域的对象：
globClock.showTime(); //对象的成员函数具有类作用域
globClock.setTime(8,30,30);	
	Clock myClock(globClock); 
        //声明具有块作用域的对象myClock
	cout<<"Second time output:"<<endl;	
	myClock.showTime();	//引用具有块作用域的对象
	return 0;
}

```
	- 用关键字static声明
		- 该类的所有对象维护该成员的同一个拷贝
		- 必须在类外定义和初始化，用(::)来指明所属的类。
		- 静态函数成员
			- 类外代码可以使用类名和作用域操作符来调用静态成员函数。
静态成员函数只能引用属于该类的静态数据成员或静态成员函数。
```cpp
#include <iostream>
using namespace std;
class Point	{
public:	
	Point(int x=0, int y=0) : x(x), y(y) { count++; }
	Point(Point &p);	
	int getX() { return x; }
	int getY() { return y; }
	void showCount() {
	  cout << " Object count=“ << count << endl;
  }
private:	
	int x,y;
	static int count;
};
Point::Point(Point &p) {
	x = p.x;
	y = p.y;
	count++;
}

int Point::count=0; 
int main() {
	Point a(4,5);	
	cout<<"Point A:"<<a.getX()<<","<<a.getY();
	a.showCount();	
	Point b(a);	
	cout<<"Point B:"<<b.getX()<<","<<b.getY();
	b.showCount();	
	return 0;
}

```
	- 类的友元
		- 有元函数
			- 友元是C++提供的一种破坏数据封装和数据隐藏的机制。
			- 通过将一个模块声明为另一个模块的友元，一个模块能够引用到另一个模块中本是被隐藏的信息。我们可以使用友元函数和友元类。
			- 为了确保数据的完整性，及数据封装与隐藏的原则，建议尽量不使用或少使用友元。
			- 友元函数是在类声明中由关键字friend修饰说明的非成员函数，在它的函数体中能够通过对象名访问 private 和 protected成员
			- 友元的作用：增加灵活性，使程序员可以在封装和快速性方面做合理选择。
		- 访问对象中的成员必须通过对象名。
		- 举例：使用友元函数计算两个点之间的距离
```cpp
#include <iostream>
#include <cmath>
class Point {	//Point类声明
public:	//外部接口
	Point(int x=0, int y=0) : x(x), y(y) { }
	int getX() { return x; }
	int getY() { return y; }
	friend float dist(Point &a, Point &b); 
private:	//私有数据成员
	int x, y;
};
```        
	- 友元类
		- 若一个类为另一个类的友元，则此类的所有成员都能访问对方类的私有成员。
		- 声明语法：将友元类名在另一个类中使用friend修饰说明。
			- 友元类的举例
```cpp
			class A {
  friend class B;
public:
  void display() {
    cout << x << endl;
  }
private:
  int x;
}

class B {
public:
  void set(int i);
  void display();
private:
  A a;
};
void B::set(int i) {
   a.x=i;
}
void B::display() {
   a.display();
}

```

- 友元函数的关系是单向的：如果声明B类是A类的友元，B类的成员函数就可以访问A类的私有和保护数据，但A类的成员函数却不能访问B类的私有、保护数据。
	- 共享数据的保护
		- 常对象
		- 常类型
			- 常类型的对象必须进行初始化，而且不能被更新。
		- 常对象：必须进行初始化,不能被更新。
			- 申明方式：const 类名 对象名
		- 常引用：被引用的对象不能被更新。
			- 声明方式：const  类型说明符  &引用名
		- 常数组：数组元素不能被更新
			- 声明方式：const 类型说明符 数组名[大小]
		- 常指针：指向常量的指针
			- 常对象的举例
```cpp
class A
{
  public:
    A(int i,int j) {x=i; y=j;}
private:
    int x,y;
};
const A a(3,4); //a是常对象，不能被更新
```
- 常成员函数
		- 使用const关键字说明的函数。
		- 常成员函数不更新对象的数据成员。
		- 常成员函数说明格式：
			- 类型说明符  函数名（参数表）const;
				- 这里，const是函数类型的一个组成部分，因此在实现部分也要带const关键字。
					const关键字可以被用于参与对重载函数的区分
					通过常对象只能调用它的常成员函数。
	- 常数据成员
		- 使用const关键字说明的数据成员。
			不能更新对象的常数据成员。
			构造函数对数据成员进行初始化,就只能通过初始化列表.
			常数据成员说明格式：const 类型说明符 标识符 ;
		- 常成员函数举例：
```cpp
		#include<iostream>
using namespace std;
class R {
public:
  R(int r1, int r2) : r1(r1), r2(r2) { }
  void print();
  void print() const;
private:
  int r1, r2;
};
void R::print() {
  cout << r1 << ":" << r2 << endl;
}
void R::print() const {
  cout << r1 << ";" << r2 << endl;
}
int main() {
  R a(5,4);
  a.print(); //调用void print()
  const R b(20,52);  
  b.print(); //调用void print() const
	return 0;
}

```
- 用const修饰的类成员
	- 常引用
		- 引用(&)是标识符的别名,例如:
				int i, j;int &ri = i;  //建立一个int型的引用ri,并将其初始化为变量i的一个别名j = 10;ri = j;相当于 i = j;
				声明一个引用时，必须同时对它进行初始化，使它指向一个已存在的对象。
				一旦一个引用被初始化后，就不能改为指向其它对象。
				引用可以作为形参void swap(int &a, int &b) {...}
	- 多文件结构和编译预处理命令
		- c++程序的一般组织结构
		- 外部变量与外部函数
		- 标准c++库
		- 条件编译指令(关于#if和endif)(#else)(#elif)
```cpp
#if  常量表达式
 //当“ 常量表达式”非零时编译
     程序正文  
#endif
......
```
```cpp
	 #if   常量表达式
     //当“ 常量表达式”非零时编译
       程序正文1
#else
  //当“ 常量表达式”为零时编译
       程序正文2
#endif
```
```cpp
#if 常量表达式1
    程序正文1  //当“ 常量表达式1”非零时编译
#elif 常量表达式2
    程序正文2  //当“ 常量表达式2”非零时编译
#else
    程序正文3  //其他情况下编译
#endif
```
```cpp
#ifdef 标识符
    程序段1
#else
    程序段2
#endif
//如果“标识符”经#defined定义过，且未经undef删除，则编译程序段1，否则编译程序段2。
```
- 编译预处理
	- #include 包含指令
```cpp
//将一个源文件嵌入到当前源文件中该点处。
#include<文件名>  
//按标准方式搜索，文件位于C++系统目录的include子目录下
#include"文件名"
//首先在当前目录中搜索，若没有，再按标准方式搜索。
#define 宏定义指令
//定义符号常量，很多情况下已被const定义语句取代。
//定义带参数宏，已被内联函数取代。
#undef
//删除由#define定义的宏，使之不再起作用。
```
- 前向引用申明
	- 类应该先定义，后使用。如果需要在某个类的定义之前，引用该类，则应进行前向引用声明。
	-	前向引用声明只为程序引入一个标识符，但具体定义在其他地方。
	- 前向引用注意的事项
		- 使用前向引用声明虽然可以解决一些问题，但它并不是万能的。需要注意的是，尽管使用了前向引用声明，但是在提供一个完整的类定义之前，不能定义该类的对象，也不能在内联成员函数中使用该类的对象。请看下面的程序段：
```cpp
class Fred; //前向引用声明
class Barney {
   Fred x; //错误：类Fred的定义尚不完善
};
class Fred {
   Barney y;
};
```
```cpp
class Fred;	//前向引用声明
class Barney {
public:
  ……
void method() {
    x.yabbaDabbaDo();	//错误：Fred类的对象在定义之前被使用
  }
private:
  Fred &x;//正确，经过前向引用声明，可以声明Fred类的对象引用
};
class Fred {
public:
  void yabbaDabbaDo();
private:
  Barney &y;
}; 
```
- 结构体与类的区别
	- 结构体是一种特殊形态的类
			与类的主要区别：类的缺省访问权限是private，结构体的缺省访问权限是public
			结构体存在的主要原因：与C语言保持兼容，在性能上比class更加优异
	- 什么时候用结构体而不用类:
			定义主要用来保存数据、而没有什么操作的类型
			人们习惯将结构体的数据成员设为公有，因此这时用结构体更方便
	- 结构体定义
```cpp
struct 结构体名称 {
	 公有成员
protected:
    保护型成员
private:
     私有成员
};
```
- 一些结构体变量的初始化可以用以下形式
	类型名 变量名 = { 成员数据1初值, 成员数据2初值, …… };
- 联合体
	- 定义形式
```cpp
union 联合体名称 {
    公有成员
protected:
    保护型成员
private:
    私有成员
};
```
- 特点：	
	- 成员共用相同的内存单元
	- 任何两个成员不会同时有效
- 多文件引用结构
	- 一个源程序可以划分为多个源文件：
		- 类声明文件（.h文件）
		- 类实现文件（.cpp文件）
		- 类的使用文件（main()所在的.cpp文件）
		- 利用工程来组合各个文件。
- 类文件中不使用条件编译的文件示例
```cpp
//main.cpp
#include "file1.h"
#include "file2.h"
int main()
{
    …
}
```
```cpp
//file1.h
#include "head.h"
    …
//file2.h
#include "head.h"
    …

//head.h
    …
class Point
{
    …
}
    …
//head.h
#ifndef  HEAD_H
  #define  HEAD_H
    …
  class Point
  {
      …
  }
      …
#endif
```
- 深度搜索
	- 常成员函数的声明原则
		- 适当地将成员函数声明为常成员函数，能够提高代码质量。
			- `注意`凡是不会改变对象状态的函数，都应当声明为常成员函数。
		- 什么是改变对象状态？
			- 改变对象状态，不简单地等同于改变成员数据的值。只要一个成员函数执行与否，不会影响以后接口函数的调用结果，都可以认为它不会改变对象状态。
		- 示例
```cpp
class Line {	//Line类的定义
public:	//外部接口
	Line(const Point &p1, const Point &p2)
      : p1(p1), p2(p2), len(-1) { }
	double getLen();
private:	//私有数据成员
	Point p1, p2;	//Point类的对象p1,p2
	double len;
};
double Line::getLen() {//改变数据成员但是不改变类的状态
	if (len < 0) {
		double x = p1.getX() - p2.getX();
		double y = p1.getY() - p2.getY();
		len = sqrt(x * x + y * y);
	}
	return len;
}
```
- 在原则上，应当将getLen声明为常成员函数，但由于修改了数据成员的值，语言规则不允许怎么办？使用mutable关键字。mutable关键字使得被修饰的成员对象无视“常对象的成员对象被视为常对象”这一语言原则。Mutable须慎用
	- 符号表：将静态对象与函数的名字与地址关联
		- 重定位记录表：将代码中需用到的地址与符号表关联
	- 代码的执行
		- 操作系统首先将文件从磁盘读入，初始化各段——一些静态数据就在此时被初始化
		- 从引导代码开始执行，引导代码启动main，main返回后，引导代码会通知操作系统程序结束
		- 为什么只有静态对象需要在目标文件中保存信息？
		- 连接器负责为静态对象分配唯一地址，而其它对象都是相对寻址
	- 为什么类的信息不存在于目标文件中？
		- 类的“解构”
- 第六章 数组、指针与字符串
	- 数组
		- 数组的声明与使用
			- 只能一个一个引用数组的元素，不能一下子引用全部的数组
		- 数组的存储与初始化
		- 数组作为函数参数
		- 对象数组
			- 声明：
				类名  数组名[元素个数]；
			- 访问方法：
				通过下标访问；
        数组名[下标].成员名
		- 对象数组初始化
			- 数组中每一个元素对象被创建时，系统都会调用类构造函数初始化该对象。
			- 通过初始化列表赋值：
				- 例：Point A[2]={Point(1,2),Point(3,4)};
			- 如果没有为数组元素指定显式初始值，数组元素便使用默认值初始化（调用默认构造函数）。
		- 数组元素所属类的构造函数
			- 不声明构造函数，则采用默认构造函数。
			- 各元素对象的初值要求为相同的值时，可以声明具有默认形参值的构造函数。
			- 各元素对象的初值要求为不同的值时，需要声明带形参的构造函数。
			- 当数组中每一个对象被删除时，系统都要调用一次析构函数。
		- 程序实例
```cpp
//Point.h
#if !defined(_POINT_H)
#define _POINT_H
class Point
{   public:
       Point(); 
       Point(int xx,int yy);
       ~Point();
       void Move(int x,int y);
       int GetX() {return X;}
       int GetY() {return Y;}
  private:
       int  X,Y;
};
#endif
```
```cpp
//6-2.cpp
#include<iostream>
using namespace std;
#include "Point.h"
Point::Point()
{   X=Y=0;
     cout<<"Default Constructor called."<<endl;
}
Point::Point(int xx,int yy)
{   X=xx;
     Y=yy;
     cout<< "Constructor called."<<endl;
}
Point ::~Point()
{  cout<<"Destructor called."<<endl;  }
void Point ::Move(int x,int y)
{      X=x;    Y=y;  }
```
```cpp
#include<iostream>
#include "Point.h"
using namespace std;
int main()
{
   cout<<"Entering main..."<<endl;
   Point A[2];
   for(int i=0;i<2;i++)
     A[i].Move(i+10,i+20);
   cout<<"Exiting main..."<<endl;
   return 0;
}
```
- 指针
	- 内存空间的访问方式
	- 指针变量的申明
		- 语法形式：
 			存储类型 数据类型 *指针名＝初始地址；
			例：int a,*pa=&a;
- `注意事项`
	- 用变量地址作为初值时，该变量必须在指针初始化之前已说明过，且变量类型应与指针类型一致。
		- 可以用一个已赋初值的指针去初始化另一 个指针变量。
		- 不要用一个内部 auto 变量去初始化 static 指针。
		- 与地址相关的运算“*”与“&”
		- 指针的赋值
			- 指针名=地址
			- “地址”中存放的数据类型与指针类型必须相符。
			- 向指针变量赋的值必须是地址常量或变量，不能是普通整数。但可以赋值为整数0，表示空指针。
			- 指针的类型是它所指向变量的类型，而不是指针本身数据值的类型，任何一个指针本身的数据值都是unsigned long int型。
			- 允许声明指向 void 类型的指针。该指针可以被赋予任何类型对象的地址。
				- 例： void *general; 
		- 指针运算
```cpp
#include<iostream>
using namespace std;
int main()
{int *i_pointer;	//声明int型指针i_pointer
 int i; //声明int型数i
 i_pointer=&i; //取i的地址赋给i_pointer
 i=10; //int型数赋初值
 cout<<"Output int i="<<i<<endl;//输出int型数的值
 cout<<"Output int pointer i="<<*i_pointer<<endl;
           //输出int型指针所指地址的内容
```

```cpp
void vobject;//错，不能声明void类型的变量
void *pv;//对，可以声明void类型的指针
int  *pint; int i;
int main()
{
	pv = &i;	//void类型指针指向整型变量
  //void指针赋值给int指针需要类型强制转换:
  pint = (int *)pv;  
} 

```
- 指向常量的指针
	- 不能通过指针来改变所指对象的值，但指针本身可以改变，可以指向另外的对象。
```cpp
char *name1="John"; //name1是一般指针
*name1='A'; //编译正确，运行出错
例2
const char *name1="John"; //指向常量的指针
char s[]="abc";
name1=s;  //正确，name1本身的值可以改变
*name1='1'; //编译时指出错误
```
- 指针类型的常量
	- 若声明指针常量，则指针本身的值不能被改变。
```cpp
char *const name2="John"; 
name2="abc";//错误，指针常量值不能改变
```
- 指针变量的算数运算
	- 指针与整数的加减运算
	- 指针p加上或减去n，其意义是指针当前指向位置的前方或后方第n个数据的地址。
	- 这种运算的结果值取决于指针指向的数据类型。
	- 指针加一，减一运算
		- 指向下一个或前一个数据。
			例如：y=*px++ 相当于 y=*(px++) (*和++优先级相同，自右向左运算)
	- 用指针处理数组元素
		- 使用数组元素的名字得到的就是这个数组的首地址，使用*之后指向的就是这个首地址指向的所有的内存地址
	- 指针变量的关系运算
		- 关系运算
			- 指向相同类型数据的指针之间可以进行各种关系运算。
			- 指向不同数据类型的指针，以及指针与一般整数变量之间的关系运算是无意义的。
				- 指针可以和零之间进行等于或不等于的关系运算。例如：p==0或p!=0
		- 赋值运算
			- 向指针变量赋的值必须是地址常量或变量，不能是普通整数。但可以赋值为整数0，表示空指针。
	- 指向数组元素的指针
		- 声明与赋值
```cpp
int a[10], *pa;
pa=&a[0]; 或 pa=a;
```
- 通过指针引用数组元素
	- 经过上述声明及赋值后：
		*pa就是a[0]，*(pa+1)就是a[1]，... ，*(pa+i)就是a[i].
					a[i], *(pa+i), *(a+i), pa[i]都是等效的。
		- 注意：不能写 a++，因为a是数组首地址是常量。 
					设有一个int型数组a，有10个元素。用三种方法输出各元素：
		- 使用数组名和下标
		- 使用数组名和指针运算
			- 使用指针变量
```cpp
//使用数组名和下标
int main()
{
   int a[10];
   int i;
   for(i=0; i<10; i++)
     cin>>a[i];
   cout<<endl;
   for(i=0; i<10; i++)
     cout<<a[i];
}
```
- 使用数组名指针运算
```cpp
int main()
{
   int a[10];
   int i;
   for(i=0; i<10; i++)
      cin>>a[i];
   cout<<endl;
   for(i=0; i<10; i++)
     cout<<*(a+i);
}
```
- 使用指针变量
```cpp
int main()
{
   int a[10];
   int *p,i；
   for(i=0; i<10; i++)
        cin>>a[i];
   cout<<endl;
   for(p=a; p<(a+10); p++)
        cout<<*p;
}
```
- 指针数组
	- 数组的元素是指针型
```cpp	
Point  *pa[2];
```
- 由pa[0],pa[1]两个指针组成,利用指针数组存放单位矩阵
```cpp
//输出单位矩阵
  cout<<"Matrix test:"<<endl;
	for(int i=0;i<3;i++) //对指针数组元素循环
	{
	  for(int j=0;j<3;j++)//对矩阵每一行循环
	  { cout<<p_line[i][j]<<" ";   }
	    cout<<endl;
	}
}
```
```cpp
#include <iostream>
using namespace std;
int main()
{	int array2[2][3]={{11,12,13},{21,22,23}};
    for(int i=0;i<2;i++)
    {  cout<<*(array2+i)<<endl;	
	    for(int j=0;j<3;j++)
        {  cout<<*(*(array2+i)+j)<<" ";   
           //或者 cout<<array2[i][j]<<" ";
        }	
	    cout<<endl;
	}
}
```
- 用指针处理数组元素
- 指针数组
	- 用指针作为函数参数
		- 以地址方式传递数据，可以用来返回函数处理结果。
		- 实参是数组名时形参可以是指针。
```cpp
//题目：读入三个浮点数，将整数部分和小数部分分别输出
#include <iostream>
using namespace std;
void  splitfloat(float x, int *intpart, float *fracpart)
{  //形参intpart、 fracpart是指针
   *intpart=int(x); // 取x的整数部分
   *fracpart=x-*intpart; //取x的小数部分
}

int main()
{
	int i, n;
	float x, f;	
	cout<<"Enter three(3) floating point numbers"    << endl;
	for (i = 0; i < 3; i++)
	{
	  cin >> x;
	  splitfloat(x,&n,&f); //变量地址做实参
	  cout<<"Integer Part is "<< n       <<"   Fraction Part is "<<f<<endl;
	}
}
```
- 输出数组元素的内容和地址
```cpp
#include <iostream>
#include <iomanip>
using namespace std;
void Array_Ptr(long *P, int n)
{	int i;
	cout<<"In func, address of array is "    <<unsigned long(P)<<endl;
	cout<<"Accessing array using pointers"<< endl;
	for (i = 0; i < n; i++)
	{ cout<<"   Address for index "<<i<<" is "      <<unsigned long(P+i);
	  cout<<"  Value is "<<*(P+i)<<endl;
	}
}
int main()
{
	long list[5]={50, 60, 70, 80, 90};
	
	cout<<"In main, address of array is "
      << unsigned long(list)<<endl;
	cout<<endl;
	Array_Ptr(list,5);
}
```
- 指向常量的指针作为形参
```cpp
#include<iostream>
using namespace std;
const int N=6;
void print(const int *p,int n);
int main()
{  int array[N];
    for(int i=0;i<N;i++)
         cin>>array[i];
    print(array,N);
}
void print(const int *p, int n)
{
     cout<<"{"<<*p;
     for(int i=1;i<n;i++)
         cout<<"."<<*(p+i);
     cout<<"}"<<endl;
}
```
- 指针形函数
	-	当函数的返回值是地址时，该函数就是指针型函数。
	- 声明形式: 
		- 存储类型  数据类型  *函数名()
	- 声明形式
   	存储类型  数据类型  (*函数指针名)();
		- 含义：
			- 数据指针指向数据存储区，而函数指针指向的是程序代码存储区。
```cpp	
#include <iostream>
using namespace std;
void print_stuff(float data_to_ignore);
void print_message(float list_this_data);
void print_float(float data_to_print);
void (*function_pointer)(float);	
int main()	
{
	float pi=(float)3.14159;
	float two_pi=(float)2.0*pi;
   print_stuff(pi);
   function_pointer = print_stuff;
   function_pointer(pi);
   function_pointer = print_message;
   function_pointer(two_pi);
   function_pointer(13.0);
   function_pointer = print_float;
   function_pointer(pi);
   print_float(pi);
}
void print_stuff(float data_to_ignore)
{	cout<<"This is the print stuff function.\n";    
}

void print_message(float list_this_data)
{	cout<<"The data to be listed is " 
      <<list_this_data<<endl;    
}

void print_float(float data_to_print)
{	cout<<"The data to be printed is " 
      <<data_to_print<<endl;    
}
```
- 对象指针的一般概念
	- 声明形式:
		类名  *对象指针名；
```cpp
Point A(5,10);
Piont *ptr;
ptr=&A;
//通过指针访问对象成员
//对象指针名->成员名
ptr->getx() 相当于 (*ptr).getx();
//对象指针应用举例
int main()
{
     Point A(5,10);
     Point *ptr;
     ptr=&A;
	   int x;
	   x=ptr->GetX();
	   cout<<x<<endl;
     return 0;
}
class Fred;	//前向引用声明
class Barney {
   Fred x;	//错误：类Fred的定义尚不完善
 };
class Fred {
   Barney y;
 };
正确的程序
class Fred;	//前向引用声明
class Barney {
   Fred *x;	 
 };
class Fred {
   Barney y;
 };
```
- this指针
	- 隐含于每一个类的成员函数中的特殊指针。明确地指出了成员函数当前所操作的数据所属的对象。
	- 当通过一个对象调用成员函数时，系统先将该对象的地址赋给this指针，然后调用成员函数，成员函数对对象的数据成员进行操作时，就隐含使用了this指针。
```cpp
//Point类的构造函数体中的语句：
X=xx;
Y=yy; 
相当于：
this->X=xx;
this->Y=yy;
```
- 指向类的非静态成员指针
	- 通过指向成员的指针只能访问公有成员
	- 声明指向成员的指针
   	- 声明指向公有数据成员的指针
			- 类型说明符  类名::*指针名；
			- 声明指向公有函数成员的指针
			- 类型说明符  (类名::*指针名)(参数表)；
		- 指向数据成员的指针
			- 说明指针应该指向哪个成员
				- 指针名=&类名::数据成员名；
				- 通过对象名（或对象指针）与成员指针结合来访问数据成员
					- 对象名.* 类成员指针名 
					- 对象指针名—>*类成员指针名
			- 指向函数成员的指针
				- 初始化：
					指针名=&类名::函数成员名；
					通过对象名（或对象指针）与成员指针结合来访问函数成员
				- (对象名.* 类成员指针名)(参数表)
				- (对象指针名—>*类成员指针名)(参数表)
```cpp
//访问对象的公有成员函数的不同方式
int main()	//主函数
{	Point A(4,5);	//声明对象A
	Point *p1=&A;	//声明对象指针并初始化
   //声明成员函数指针并初始化
	int (Point::*p_GetX)()=Point::GetX;	
   //（1）使用成员函数指针访问成员函数
	cout<<(A.*p_GetX)()<<endl;	
   //（2）使用对象指针访问成员函数
	cout<<(p1->GetX)()<<endl;	
   //（3）使用对象名访问成员函数
	cout<<A.GetX()<<endl; }
```
- 对类的静态成员的访问不依赖于对象
	- 可以用普通的指针来指向和访问静态成员
- 通过指针访问类的静态数据成员
```cpp
#include <iostream>
using namespace std;
class Point	//Point类定义
{public:	//外部接口
	Point(int xx=0, int yy=0) {X=xx;Y=yy;countP++;}//构造函数
	Point(Point &p);	//拷贝构造函数
	int GetX() {return X;}
	int GetY() {return Y;}
	static int countP; //静态数据成员引用性说明
private:	//私有数据成员
	int X,Y;
};
Point::Point(Point &p)
{	X=p.X;  Y=p.Y;  countP++;  }

int Point::countP=0; //静态数据成员定义性说明
int main()	//主函数
{ //声明一个int型指针，指向类的静态成员
	int *count=&Point::countP; 
	Point A(4,5);	//声明对象A
	cout<<"Point A,"<<A.GetX()<<","<<A.GetY();
	//直接通过指针访问静态数据成员
  cout<<" Object id="<<*count<<endl;	
	Point B(A);	//声明对象B
	cout<<"Point B,"<<B.GetX()<<","<<B.GetY();
  //直接通过指针访问静态数据成员
	cout<<" Object id="<<*count<<endl; }
#include <iostream>
using namespace std;
class Point	//Point类定义
{ public:	//外部接口
	static void GetC()  //静态函数成员
  { cout<<" Object id="<<countP<<endl; }
   private:	//私有数据成员
	int X,Y;
	static int countP;	//静态数据成员引用性说明
};
int Point::countP=0;	//静态数据成员定义性说明
int main()	//主函数
{
  //指向函数的指针，指向类的静态成员函数
	void (*gc)()=Point::GetC;	
	Point A(4,5);	//声明对象A
	cout<<"Point A,"<<A.GetX()<<","<<A.GetY();
	gc();//输出对象序号，通过指针访问静态函数成员
	Point B(A);//声明对象B
	cout<<"Point B,"<<B.GetX()<<","<<B.GetY();
	gc();//输出对象序号，通过指针访问静态函数成员
}
```
- 指向函数的指针
- 对象指针
- 动态内存分配
- 动态申请内存操作符new
	- new  类型名T（初值列表）
		- 功能：在程序执行期间，申请用于存放T类型对象的内存空间，并依初值列表赋以初值。
			- 结果值：成功：T类型的指针，指向新分配的内存。失败：0（NULL）
	- 释放内存操作符delete
		- delete 指针P
		- 功能：释放指针P所指向的内存。P必须是new操作的返回值。
```cpp
#include<iostream>
using namespace std;
class Point
{public:
  Point()
  { X=Y=0; cout<<"Default Constructor called.\n";}
  Point(int xx,int yy)
  { X=xx;Y=yy; cout<< "Constructor called.\n";  }
  ~Point() { cout<<"Destructor called.\n";  }
  int GetX(){return X;}
  int GetY(){return Y;}
	void Move(int x,int y) { X=x; Y=y; }
  private:
    int  X,Y;
};
int main()
{   cout<<"Step One:"<<endl;
     Point *Ptr1=new Point;
     delete  Ptr1;   
     cout<<"Step Two:"<<endl;
     Ptr1=new Point(1,2);
     delete Ptr1;
     return 0;
}
```
- 动态创造数组举例
```cpp
#include<iostream>
using namespace std;
class Point
{   //类的定义同例6-16，略 };
int main()
{ Point *Ptr=new Point[2]; //创建对象数组
  Ptr[0].Move(5,10); //通过指针访问数组元素的成员
  Ptr[1].Move(15,20); //通过指针访问数组元素的成员
  cout<<"Deleting..."<<endl;
  delete[ ] Ptr;  //删除整个对象数组
  return 0;
}
```
- 动态数组类
```cpp
#include<iostream>
using namespace std;
class Point
{   //类的定义同例6-16 …  };
class ArrayOfPoints
{ public:
   ArrayOfPoints(int n)
   { numberOfPoints=n; points=new Point[n];}
   ~ArrayOfPoints()
   { cout<<"Deleting..."<<endl;
     numberOfPoints=0;  delete[] points;     
   }
   Point& Element(int n)
   {  return points[n];  }
  private:
   Point *points;
   int numberOfPoints;
};
int main()
{
	int number;
	cout<<"Please enter the number of points:";
	cin>>number;
//创建对象数组
  ArrayOfPoints points(number);    
//通过指针访问数组元素的成员
  points.Element(0).Move(5,10); 
//通过指针访问数组元素的成员
  points.Element(1).Move(15,20);   
}
```  
- 动态创建多维数组
  - new 类型名T[下标表达式1][下标表达式2]…；
	- 如果内存申请成功，new运算返回一个指向新分配内存首地址的指针，是一个T类型的数组，数组元素的个数为除最左边一维外各维下标表达式的乘积。例如：
```cpp
char (*fp)[3];
fp = new char[2][3];

#include<iostream>
using namespace std;
int main()
{	float (*cp)[9][8];
	int i,j,k;
	cp = new float[8][9][8];
	for (i=0; i<8; i++)
	 for (j=0; j<9; j++)
	  for (k=0; k<9; k++)
	   *(*(*(cp+i)+j)+k)=i*100+j*10+k; 
//通过指针访问数组元素
 for (i=0; i<8; i++)
 { for (j=0; j<9; j++)
   { for (k=0; k<8; k++)
	//将指针cp作为数组名使用，
  //通过数组名和下标访问数组元素
  cout<<cp[i][j][k]<<" "<<endl;  
	  }
  }
}
```
- 动态存储分配函数
```cpp
	void *malloc( size );
//参数size：欲分配的字节数
//返回值：成功，则返回void型指针。      失败，则返回空指针。
//头文件：<cstdlib> 和 <cmalloc>
```
- 动态内存释放函数
```cpp
void free( void *memblock );
```
- 参数memblock：指针，指向需释放的内存。
	- 返回值：无
	- 需要使用的头文件：<cstdlib> 和 <cmalloc>
	- 用vector创建数组对象
	- 深复制与浅复制
		- 浅拷贝
				实现对象间数据元素的一一对应复制。
		- 深拷贝
				当被复制的对象数据成员是指针类型时，不是复制该指针成员本身，而是将指针所指的对象进行复制。
```cpp
#include<iostream>
using namespace std;
class Point
{   //类的定义同例6-16
    //……
};
class ArrayOfPoints
{
   //类的定义同例6-18
    //……
};
int main()
{	int number;
	cin>>number;
  ArrayOfPoints pointsArray1(number); pointsArray1.Element(0).Move(5,10); pointsArray1.Element(1).Move(15,20); 
  ArrayOfPoints pointsArray2(pointsArray1); 
  cout<<"Copy of pointsArray1:"<<endl;
  cout<<"Point_0 of array2: "
      <<pointsArray2.Element(0).GetX()
      <<", "<<pointsArray2.Element(0).GetY()<<endl;
  cout<<"Point_1 of array2: "
      <<pointsArray2.Element(1).GetX()
      <<", "<<pointsArray2.Element(1).GetY()<<endl;
 pointsArray1.Element(0).Move(25,30);    
 pointsArray1.Element(1).Move(35,40);   
 cout<<"After the moving of pointsArray1:"<<endl;
 cout<<"Point_0 of array2: "
  <<pointsArray2.Element(0).GetX()
  <<", "<<pointsArray2.Element(0).GetY()<<endl;
 cout<<"Point_1 of array2: "
  <<pointsArray2.Element(1).GetX()
  <<", "<<pointsArray2.Element(1).GetY()<<endl;
}
```
- 运行结果如下：
Please enter the number of points:2

Default Constructor called.

Default Constructor called.

Copy of pointsArray1:

Point_0 of array2: 5, 10

Point_1 of array2: 15, 20

After the moving of pointsArray1:

Point_0 of array2: 25, 30

Point_1 of array2: 35, 40

Deleting...

Destructor called.

Destructor called.

Deleting...

- 接下来程序出现异常，也就是运行错误。
	- 对象的深拷贝
```cpp
#include<iostream>
using namespace std;
class Point
{   //类的定义同例6-16 ……   };
class ArrayOfPoints
{ public:
   ArrayOfPoints(ArrayOfPoints& pointsArray);
    //其他成员同例6-18        
};
ArrayOfPoints ::ArrayOfPoints
(ArrayOfPoints& pointsArray)
{ numberOfPoints
      =pointsArray.numberOfPoints;
  points=new Point[numberOfPoints];
  for (int i=0; i<numberOfPoints; i++)
    points[i].Move(
              pointsArray.Element(i).GetX(),
              pointsArray.Element(i).GetY());
}
int main()
{   //同例6-20   }
```
- 程序的运行结果如下：

Please enter the number of points:2

Default Constructor called.

Default Constructor called.

Default Constructor called.

Default Constructor called.

Copy of pointsArray1:

Point_0 of array2: 5, 10

Point_1 of array2: 15, 20

After the moving of pointsArray1:

Point_0 of array2: 5, 10

Point_1 of array2: 15, 20

Deleting...

Destructor called.

Destructor called.

Deleting...

Destructor called.

Destructor called.

- 字符串
	- 用字符数组存储和处理字符串
		- 字符数组的声明和引用
			- 字符串
- 字符串常量，例如："china"
	- 没有字符串变量，用字符数组来存放字符串
	- 字符串以'\0'为结束标志
	- 字符数组的初始化
```cpp
static char str[8]={112,114,111,103,114,97,109,0};static char str[8]={'p','r','o','g','r','a','m','\0'};static char str[8]="program";static char str[]="program";
```
```cpp
#include<iostream>
using namespace std;
int main()
{
  static char c[10]={'I',' ','a','m',' ','a',' ','b','o','y'};  
int i;
for(i=0;i<10;i++)
  cout<<c[i];
cout<<endl;
}
#include<iostream>
using namespace std;
int main(){  
static char diamond[][5]={
     {' ',' ','*'},
     {' ','*',' ','*'}, 
     {'*',' ',' ',' ','*'},
     {' ','*',' ','*'}, 
     {' ',' ','*'}};
	int i,j;
	for (i=0;i<5;i++) 
	{  for(j=0;j<5 && diamond[i][j]!=0;j++)
		cout<<diamond[i][j];  
	    cout<<endl;
	}
}
```
- 字符串的输入输出
	- 方法
		- 逐个字符输入输出
		- 将整个字符串一次输入或输出
			- 例：char c[]="China";cout<<c;
	- 注意
		-	输出字符不包括 '\0'
			- 输出字符串时，输出项是字符数组名，输出时遇到'\0'结束。
			- 输入多个字符串时，以空格分隔；输入单个字符串时其中 不能有空格。
```cpp
//程序中有下列语句：
    static char str1[5],str2[5],str3[5];
    cin>>str1>>str2>>str3;
//运行时输入数据：How are you?
//内存中变量状态如下： 
  str1: H o w \0 
  str2: a r e \0
  str3: y o u ? \0
```
- 用字符数组存储和处理字符串
	- 注意！若有如下声明:
char a[4], *p1, *p2;
错误的:a="abc";cin>>p1;
正确的:p1="abc";p2=a;    cin>>p2;
若改为：
    static char str[13];
    cin>>str;
  运行时输入数据：
    How are you?
内存中变量 str 内容如下： 
     str:  H o w \0 

- string类
	- 字符串处理函数
		- strcat（连接），strcpy（复制），strcmp（比较），strlen（求长度）， strlwr(转换为小写），strupr（转换为大写）
> 头文件<cstring>
```cpp
#include <string>
#include <iostream>
using namespace std ;
void trueFalse(int x)
{
  cout<<(x? "True": "False")<<endl;
}
int main()
{  string S1="DEF",  S2="123";
   char CP1[ ]="ABC"; 
   char CP2[ ]="DEF";
   cout<<"S1 is "<<S1<<endl;
   cout<<"S2 is "<<S2<<endl;
   cout<<"length of S2:"<<S2.length()<<endl;
   cout<<"CP1 is "<<CP1<<endl;
   cout<<"CP2 is "<<CP2<<endl;
   cout<<"S1<=CP1 returned ";
   trueFalse(S1<=CP1); 
   cout<<"CP2<=S1 returned ";
   trueFalse(CP2<=S1); 
   S2+=S1;
   cout<<"S2=S2+S1:"<<S2<<endl;
   cout<<"length of S2:"<<S2.length()<<endl;
}
```
- 整行输入字符串
	- cin.getline(字符数组名St,字符个数N,结束符);s
	- 功能：一次连续读入多个字符（可以包括空格），直到读满N个，或遇到指定的结束符（默认为'\n'）。读入的字符串存放于字符数组St中。读取但不存储结束符。
	- cin.get(字符数组名St,字符个数N,结束符);
		- 功能：一次连续读入多个字符（可以包括空格），直到读满N个，或遇到指定的结束符（默认为'\n'）。读入的字符串存放于字符数组St中。既不读取也不存储结束符。
```cpp
#include <iostream>
using namespace std;
void main (void)
{	char city[80];
	char state[80];
	int  i;
	for (i = 0; i < 2; i++)
	{ cin.getline(city,80,',');
	  cin.getline(state,80,'\n');
	  cout<<"City: "<<city<<" State: "<<state<<endl;
	}
}
```
- 运行结果
Beijing,China

City: Beijing   Country: China

Shanghai,China

City: Shanghai   Country: China
- 深度搜索
	- 指针与引用
	- 指针的安全性隐患及其应对方案
	- const_cast的应用
- 第七章 继承与派生
	- 类的继承与派生
		- 保持已有类的特性而构造新类的过程称为继承。
		- 在已有类的基础上新增自己的特性而产生新类的过程称为派生。
		- 被继承的已有类称为基类（或父类）。
			-	派生出的新类称为派生类。
		- 继承的目的：实现代码重用。
		-	派生的目的：当新的问题出现，原有程序无法解决（或不能完全解决）时，需要对原有程序进行改造。
		- 派生类的定义/声明
			- class 派生类名：继承方式  基类名
{
        成员声明；
}
- `特别注意`事实上：派生和继承是同一个东西，比如：父类派生出了一个子类，一个子类继承了父类。这两者是同物不同名。
	- 继承方式
		- 不同继承方式的影响主要体现在：
			- 派生类成员对基类成员的访问权限
			- 通过派生类对象对基类成员的访问权限
	- 三种继承方式
		- 公有继承
		- 私有继承
		- 保护继承
	- 派生类生成过程
- 访问控制
	- 公有继承
		- 基类的public和protected成员的访问属性在派生类中保持不变，但基类的private成员不可直接访问。也就是说：派生类中的成员函数可以直接访问基类中的public和protected成员，但不能直接访问基类的private成员。
		- 通过派生类的对象只能访问基类的public成员。
	- 共有继承举例
```cpp
class Point {	//基类Point类的定义
public:	//公有函数成员
	void initPoint(float x = 0, float y = 0) { this->x = x; this->y = y;}
	void move(float offX, float offY) { x += offX; y += offY; }
	float getX() const { return x; }
	float getY() const { return y; }
private:	//私有数据成员
	float x, y;
};
class Rectangle: public Point {//派生类定义部分
public:	//新增公有函数成员
	void initRectangle(float x, float y, float w, float h) {
		initPoint(x, y); //调用基类公有成员函数
		this->w = w;
		this->h = h;
	}
	float getH() const { return h; }
	float getW() const { return w; }
private:	//新增私有数据成员
	float w, h;
};
```
```cpp
#include <iostream>
#include <cmath>
using namespace std;           
int main() {
	Rectangle rect;	//定义Rectangle类的对象
	//设置矩形的数据
	rect.initRectangle(2, 3, 20, 10);	
	rect.move(3,2);	//移动矩形位置
	cout << "The data of rect(x,y,w,h): " << endl;
	//输出矩形的特征参数
	cout << rect.getX() <<", "
		<< rect.getY() << ", "
		<< rect.getW() << ", "
		<< rect.getH() << endl;
	return 0;
}
```
- 私有继承
	- 基类的public和protected成员都以private身份出现在派生类中，但基类的private成员不可直接访问。
	- 派生类中的成员函数可以直接访问基类中的public和protected成员，但不能直接访问基类的private成员。
	- 通过派生类的对象不能直接访问基类中的任何成员。
```cpp
class Rectangle: private Point {//派生类定义部分
public:	//新增公有函数成员
	void initRectangle(float x, float y, float w, float h) {
		initPoint(x, y); //调用基类公有成员函数
		this->w = w;
		this->h = h;	}
	void move(float offX, float offY) { 
		Point::move(offX, offY);
	}
	float getX() const { return Point::getX(); }
	float getY() const { return Point::getY(); }
	float getH() const { return h; }
	float getW() const { return w; }
private:	//新增私有数据成员
	float w, h;};
#include <iostream>
#include <cmath>
using namespace std;
int main() {
	Rectangle rect;	//定义Rectangle类的对象
	rect.initRectangle(2, 3, 20, 10);	//设置矩形的数据
	rect.move(3,2);	//移动矩形位置
	cout << "The data of rect(x,y,w,h): " << endl;
	cout << rect.getX() <<", "	//输出矩形的特征参数
		<< rect.getY() << ", "
		<< rect.getW() << ", "
		<< rect.getH() << endl;
	return 0;
}
```
- 保护继承
	- 基类的public和protected成员都以protected身份出现在派生类中，但基类的private成员不可直接访问。
	- 派生类中的成员函数可以直接访问基类中的public和protected成员，但不能直接访问基类的private成员。
	- 通过派生类的对象不能直接访问基类中的任何成员
	- 对建立其所在类对象的模块来说，它与 private 成员的性质相同。
	- 对于其派生类来说，它与 public 成员的性质相同。既实现了数据隐藏，又方便继承，实现代码重用。
- protected成员举例
```cpp
class A {
protected:
	int x;
};
int main() {
	A a;
	a.x = 5;    //错误
}
class A {
protected:
	int x;
};
class B: public A{
public:
	void function();
};
void B:function() {
	x = 5;   //正确
}
```
- 类型兼容规则
	- 一个公有派生类的对象在使用上可以被当作基类的对象，反之则禁止。具体表现在：
	- 派生类的对象可以隐含转换为基类对象。
		- 派生类的对象可以初始化基类的引用。
		- 派生类的指针可以隐含转换为基类的指针。
		- 通过基类对象名、指针只能使用从基类继承的成员
```cpp
#include <iostream>
using namespace std;
class Base1 { //基类Base1定义
public:
	void display() const {
		cout << "Base1::display()" << endl;
	}
};
class Base2: public Base1 { //公有派生类Base2定义
public:
	void display() const {
		cout << "Base2::display()" << endl;
	}
};
class Derived: public Base2 { //公有派生类Derived定义
public:
	void display() const {
		cout << "Derived::display()" << endl;
	}
};
void fun(Base1 *ptr) { //参数为指向基类对象的指针
	ptr->display();	//"对象指针->成员名"
}
int main() {	//主函数
	Base1 base1;	//声明Base1类对象
	Base2 base2;	//声明Base2类对象
	Derived derived;	//声明Derived类对象

	 //用Base1对象的指针调用fun函数
	fun(&base1);	
	//用Base2对象的指针调用fun函数
	fun(&base2);
	//用Derived对象的指针调用fun函数fun(&derived);

	return 0;
}
void fun(Base1 *ptr)
 { 
	ptr->display();	
}
```
- 基类与派生类的关系
	- 单继承
		- 派生类只从一个基类派生。
	- 多继承
		- 派生类从多个基类派生。
	- 多重派生
		- 由一个基类派生出多个不同的派生类。
	- 多层派生
		- 派生类又作为基类，继续派生新的类。
	- 多继承时派生类的声明
		- class 派生类名：继承方式1  基类名1，继承方式2  基类名2，...
{
        成员声明；
}
- `注意`：每一个“继承方式”，只用于限制对紧随其后之基类的继承。
	- 多继承的举例
```cpp
class A {
public:
 	void setA(int);
	void showA() const;
private:
	int a;
};
class B {
public:
	void setB(int);
	void showB() const;
private:
	int b;
};
class C : public A, private B { 
public:
	void setC(int, int, int);
	void showC() const;
private :
	int c;
};
void  A::setA(int x) {
	a=x; 
}
void B::setB(int x) {
	b=x; 
}
void C::setC(int x, int y, int z) {
	//派生类成员直接访问基类的
	//公有成员
	setA(x); 
	setB(y); 
	c = z;
}
//其他函数实现略
int main() {
	C obj;
	obj.setA(5);
	obj.showA();
	obj.setC(6,7,9);
	obj.showC();
// obj.setB(6);  错误
// obj.showB(); 错误
	return 0;
}
```
- 派生类的构造和析构函数
	- 构造函数
		- 基类的构造函数不被继承，派生类中需要声明自己的构造函数。
			- 定义构造函数时，只需要对本类中新增成员进行初始化，对继承来的基类成员的初始化，自动调用基类构造函数完成。
			- 派生类的构造函数需要给基类的构造函数传递参数
	- 单一继承时的构造函数
		- 派生类名::派生类名(基类所需的形参，本类成员所需的形参):基类名(参数表)
{
	本类成员初始化赋值语句；
}；
```cpp
#include<iostream>
using namespace std;
class B {
public:
	B();
	B(int i);
	~B();
	void print() const;
private:
	int b;
};
B::B() {
	b=0;
	cout << "B's default constructor called." << endl;
}
B::B(int i) {
	b=i;
	cout << "B's constructor called." << endl;
}
B::~B() {
	cout << "B's destructor called." << endl;
}
void B::print() const {
	cout << b << endl;
}
class C: public B {
public:
	C();
	C(int i, int j);
	~C();
	void print() const;
private:
	int c;
};
C::C() {
	c = 0;
	cout << "C's default constructor called." << endl;
}
C::C(int i,int j): B(i) {
	c = j;
	cout << "C's constructor called." << endl;
}
C::~C() {
	cout << "C's destructor called." << endl;
}
void C::print() const {
	B::print();
	cout << c << endl;
}
int main() {
	C obj(5, 6);
	obj.print();
	return 0;
}
```
- 运行结果：

B's default constructor called.

C's default constructor called.

5

6
- 多继承的时候的构造函数
	- 派生类名::派生类名(参数表):基类名1(基类1初始化参数表)
	;基类名2(基类2初始化参数表), ...基类名n(基类n初始化参数表)
{
        本类成员初始化赋值语句；
}；
- 派生类与基类的构造函数
	- 当基类中声明有缺省构造函数或未声明构造函数时，派生类构造函数可以不向基类构造函数传递参数，也可以不声明，构造派生类的对象时，基类的缺省构造函数将被调用。
	- 当需要执行基类中带形参的构造函数来初始化基类数据时，派生类构造函数应在初始化列表中为基类构造函数提供参数。
		- 多继承且有内嵌对象时的构造函数
			- 派生类名::派生类名(形参表):基类名1(参数), 基类名2(参数), ...基类名n(参数)，新增成员对象的初始化
{
        本类成员初始化赋值语句；
}；
- 构造函数的执行顺序
1. 调用基类构造函数，调用顺序按照它们被继承时声明的顺序（从左向右）。
2. 对成员对象进行初始化，初始化顺序按照它们在类中声明的顺序。
3. 执行派生类的构造函数体中的内容。
- 拷贝构造函数
	- 若建立派生类对象时没有编写拷贝构造函数，编译器会生成一个隐含的拷贝构造函数，该函数先调用基类的拷贝构造函数，再为派生类新增的成员对象执行拷贝。
	- 若编写派生类的拷贝构造函数，则需要为基类相应的拷贝构造函数传递参数。
```cpp
C::C(C &c1): B(c1) {…}
```
- 派生类构造函数举例
```cpp
#include <iostream>
using namespace std;
class Base1 {	//基类Base1，构造函数有参数
public:
	Base1(int i) { cout << "Constructing Base1 " << i << endl; }
};
class Base2 {	//基类Base2，构造函数有参数
public:
	Base2(int j) { cout << "Constructing Base2 " << j << endl; }
};
class Base3 {	//基类Base3，构造函数无参数
public:
	Base3() { cout << "Constructing Base3 *" << endl; }
};
class Derived: public Base2, public Base1, public Base3 {
//派生新类Derived，注意基类名的顺序
public:	//派生类的公有成员
	Derived(int a, int b, int c, int d): Base1(a), member2(d), member1(c), Base2(b)
	{ }
	//注意基类名的个数与顺序，//注意成员对象名的个数与顺序
private:	//派生类的私有成员对象
	Base1 member1;
	Base2 member2;
	Base3 member3;};
int main() {
	Derived obj(1, 2, 3, 4);
	return 0;}
```
- 复制构造函数
- 继承时的析构函数
	- 析构函数也不被继承，派生类自行声明
	- 声明方法与一般（无继承关系时）类的析构函数相同。
	- 不需要显式地调用基类的析构函数，系统会自动隐式调用。
	- 析构函数的调用次序与构造函数相反。
```cpp
#include <iostream>
using namespace std;
class Base1 {	//基类Base1，构造函数有参数
public:
	Base1(int i) { cout << "Constructing Base1 " << i << endl; }
	~Base1() { cout << "Destructing Base1" << endl; }};

class Base2 {	//基类Base2，构造函数有参数
public:
	Base2(int j) { cout << "Constructing Base2 " << j << endl; }
	~Base2() { cout << "Destructing Base2" << endl; }};

class Base3 {	//基类Base3，构造函数无参数
public:
	Base3() { cout << "Constructing Base3 *" << endl; }
	~Base3() { cout << "Destructing Base3" << endl; }};
class Derived: public Base2, public Base1, public Base3 {
//派生新类Derived，注意基类名的顺序
public:	//派生类的公有成员
	Derived(int a, int b, int c, int d): Base1(a), member2(d), member1(c), Base2(b) { }
	//注意基类名的个数与顺序，注意成员对象名的个数与顺序
private:	//派生类的私有成员对象
	Base1 member1;
	Base2 member2;
	Base3 member3;};

int main() {
	Derived obj(1, 2, 3, 4);
	return 0;}
```
- 运行结果：

Constructing Base2 2

Constructing Base1 1

Constructing Base3 *

Constructing Base1 3

Constructing Base2 4

Constructing Base3 *

Destructing Base3

Destructing Base2

Destructing Base1

Destructing Base3

Destructing Base1

Destructing Base2

- 派生类成员的标识与访问
	- 同名隐藏规则
		- 当派生类与基类中有相同成员时：
			- 若未强行指名，则通过派生类对象使用的是派生类中的同名成员。
			- 如要通过派生类对象访问基类中被覆盖的同名成员，应使用基类名限定。
```cpp
#include <iostream>
using namespace std;
class Base1 {	//定义基类Base1
public:
	int var;
	void fun() { cout << "Member of Base1" << endl; }};
class Base2 {	//定义基类Base2
public:
	int var;
	void fun() { cout << "Member of Base2" << endl; }};
class Derived: public Base1, public Base2 { //定义派生类public:
	int var;	//同名数据成员
	void fun() { cout << "Member of Derived" << endl; }
//同名函数成员
};
int main() {
	Derived d;   
	Derived *p = &d;
	d.var = 1;	//对象名.成员名标识
	d.fun();	//访问Derived类成员
	d.Base1::var = 2;	//作用域分辨符标识
	d.Base1::fun();	//访问Base1基类成员
	p->Base2::var = 3;	//作用域分辨符标识
	p->Base2::fun();	//访问Base2基类成员
	return 0;
}
```
- 二义性问题
	- 在多继承时，基类与派生类之间，或基类之间出现同名成员时，将出现访问时的二义性（不确定性）——采用虚函数或同名隐藏规则来解决。
	- 当派生类从多个基类派生，而这些基类又从同一个基类派生，则在访问此共同基类中的成员时，将产生二义性——采用虚基类来解决。
```cpp
class A {
public:
	void  f();
};
class B {
public:
	void f();
	void g()；
};
class C: public A, public B {
public:
	void g();
	void h();
};
```
- 如果定义：C  c1;
- 则 c1.f() 具有二义性
- 而 c1.g() 无二义性（同名覆盖）
	- 二义性的解决方法
		- 解决方法一：用类名来限定c1.A::f()或c1.B::f()
		- 解决方法二：同名覆盖在C中声明一个同名成员函数f()，f()再根据需要调用A::f()或B::f()
```cpp
class B {
public:
	int b;
}
class B1: public B {
private:
	int b1;
};
class B2: public B {
private:
	int b2;
};
class C : public B1,public B2 {
public:
	int f();
private:
	int d;
}
```
- 有二义性的情况：

C  c;

c.b

c.B::b
- 无二义性的情况：

c.B1::b

c.B2::b
- 作用域分辨符
	- 虚基类
		- 虚基类的引入
			- 用于有共同基类的场合
	- 声明
		- 以virtual修饰说明基类例：class B1:virtual public B
	- 作用
		- 主要用来解决多继承时可能发生的对同一基类继承多次而产生的二义性问题，为最远的派生类提供唯一的基类成员，而不重复产生多次拷贝
	- `注意`：
		- 在第一级继承时就要将共同基类设计为虚基类。
```cpp
class B { public: int b; };
class B1: virtual public B { public: int b1; };
class B2: virtual public B { public: int b2; };
class C: public B1, public B2 { public: float d; };
```
- 下面的访问是正确的：

C cobj;

cobj.b;

```cpp
#include <iostream>
using namespace std;
class Base0 {	//定义基类Base0
public:
	int var0;
	void fun0() { cout << "Member of Base0" << endl; }
};

class Base1: virtual public Base0 {	//定义派生类Base1
public:	//新增外部接口
	int var1;
};
class Base2: virtual public Base0 {	//定义派生类Base2
public:	//新增外部接口
	int var2;
};
class Derived: public Base1, public Base2 {	//定义派生类Derived 
public:	//新增外部接口
	int var;
	void fun() {
		cout << "Member of Derived" << endl;
	}
};
int main() {	//程序主函数
	Derived d;	//定义Derived类对象d
	d.var0 = 2;	//直接访问虚基类的数据成员
	d.fun0();	//直接访问虚基类的函数成员
	return 0;
}
```
- 虚基类及其派生类构造函数
	- 建立对象时所指定的类称为最（远）派生类。
	- 虚基类的成员是由最派生类的构造函数通过调用虚基类的构造函数进行初始化的。在整个继承结构中，直接或间接继承虚基类的所有派生类，都必须在构造函数的成员初始化表中给出对虚基类的构造函数的调用。如果未列出，则表示调用该虚基类的默认构造函数。
	- 在建立对象时，只有最派生类的构造函数调用虚基类的构造函数，该派生类的其他基类对虚基类构造函数的调用被忽略。
```cpp
#include <iostream>
using namespace std;
class Base0 {	//定义基类Base0
public:
	Base0(int var) : var0(var) { }
	int var0;
	void fun0() { cout << "Member of Base0" << endl; }
};
class Base1: virtual public Base0 {	//定义派生类Base1
public:	//新增外部接口
	Base1(int var) : Base0(var) { }
	int var1;
};
class Base2: virtual public Base0 {	//定义派生类Base2
public:	//新增外部接口
	Base2(int var) : Base0(var) { }
	int var2;};
class Derived: public Base1, public Base2 {
	//定义派生类Derived
public:	//新增外部接口
	Derived(int var) : Base0(var), Base1(var), Base2(var) { }
	int var;
	void fun() { cout << "Member of Derived" << endl; }
};
int main() {	//程序主函数
	Derived d(1);	//定义Derived类对象d
	d.var0 = 2;	//直接访问虚基类的数据成员
	d.fun0();	//直接访问虚基类的函数成员
	return 0;
}
```
- 组合与继承
	- 组合与继承：通过已有类来构造新类的两种基本方式
		- 组合：B类中存在一个A类型的内嵌对象
			- 有一个（has-a）关系：表明每个B类型对象“有一个” A类型对象
			- A类型对象与B类型对象是部分与整体关系
			- B类型的接口不会直接作为A类型的接口
		- “has-a”举例
```cpp
		class Engine {	//发动机类
public:
	void work();	//发动机运转
	……
};
class Wheel {	//轮子类
public:
	void roll();	//轮子转动
	……
};
class Automobile {	//汽车类
public:
	void move();	//汽车移动
private:
	Engine engine;	//汽车引擎
	Wheel wheels[4];//4个车轮
	……
};
```
- 这一段代码的意义：
一辆汽车有一个发动机
,一辆汽车有四个轮子
- 接口
	- 作为整体的汽车不再具备发动机的运转功能，和轮子的转动功能，但通过将这些功能的整合，具有了自己的功能——移动
	- 公有继承的意义
		- 公有继承：A类是B类的公有基类
			是一个（is-a）关系：表明每个B类型对象“是一个” A类型对象
			A类型对象与B类型对象是一般与特殊关系
		- 回顾类的兼容性原则：在需要基类对象的任何地方，都可以使用公有派生类的对象来替代。B类型对象包括A类型的全部接口
		- “is-a”举例
```cpp
class Truck: public Automobile{
//卡车
public:
	void load(…);	//装货
	void dump(…);	//卸货
private:
	……
};
class Pumper: public Automobile {
//消防车
public:
	void water();	//喷水
private:
	……
};
```
- 这一段代码的意义：卡车是汽车,消防车是汽车
	- 接口
卡车和消防车具有汽车的通用功能（移动）
,它们还各自具有自己的功能（卡车：装货、卸货；消防车：喷水）
- 派生类对象的内存布局
	- 因编译器而异
				内存布局应使类型兼容规则便于实现
- 一个基类指针，无论其指向基类对象，还是派生类对象，通过它来访问一个基类中定义的数据成员，都可以用相同的步骤
- 不同情况下的内存布局
	- 单继承：基类数据在前，派生类新增数据在后
	- 多继承：各基类数据按顺序在前，派生类新增数据在后
	- 虚继承：需要增加指针，间接访虚基类数据
- 单继承情形
```cpp
class Base { … };
class Derived: public Base { … };
Derived *pd = new Derived();
Base *pb = pd;
Derived类型指针pd转换为Base类型指针时，地址不需要改变
class Base1 { … };
class Base2 { … };
class Derived: public Base1, public Base2 { … };
Derived *pd = new Derived();
Base1 *pb1 = pd;
Base2 *pb2 = pd;
Derived类型指针pd转换为Base2类型指针时，原地址需要增加一个偏移量
class Base0 { … };
class Base1: virtual public Base0 { … };
class Base2: virtual public Base0 { … };
class Derived: public Base1, public Base2 { … };
Derived *pd = new Derived();
Base1 *pb1 = pd;
Base2 *pb2 = pd;
Base0 *pb0 = pb1;
```
- 通过指针间接访问虚基类的数据成员
	- 基类向派生的转换
	- 基类指针可以转换为派生类指针
- 需要用static_cast显式转换
```cpp
Base *pb = new Derived();
Derived *pd = static_cast<Derived *>(pd);
Derived d;
Base &rb = d;
Derived &rb = static_cast<Derived &>(rb);
```
- `注意事项`
	- 基类对象一般无法被显式转换为派生类对象,对象到对象的转换，需要调用构造函数创建新的对象。
	- 派生类的拷贝构造函数无法接受基类对象作为参数执行基类向派生类的转换时，一定要确保被转换的指针和引用所指向或引用的对象符合转换的目的类型：
	- 对于Derived *pd = static_cast<Derived *>(pb);
	- 一定要保证pb所指向的对象具有Derived类型，或者是Derived类型的派生类。
	- 如果A类型是B类型的虚拟基类，A类型指针无法通过static_cast隐含转换为B类型的指针，可以结合虚继承情况下的对象内存布局，思考为什么不允许这种转换，void指针参加的转换，可能导致不可预期的后果：
```cpp
（Base2是Derived的第二个公共基类）
Derived *pd = new Derived();
void *pv = pd;	//将Derived指针转换为void指针
Base2 *pb = static_cast<Base2 *>(pv);
//转换后pb与pd有相同的地址，而正常的转换下应有一个偏移量

//结论：有void指针参与的转换，兼容性规则不适用

更安全更灵活的基类向派生类转换方式——dynamic_cast，将在下一讲介绍
```
- 用高斯消去法解新型方程组
	- 算法基本原理
	- 程序设计分析
	- 源程序及说明
	- 运行结果与分析
- 深度搜索
	- 组合与继承
	- 派生类对象的内存布局
	- 基类向派生类的转换及其安全性问题
- 第八章 多态性
	- 多态性的概述
		- 多态性是面向对象程序设计的重要特征之一。
		- 多态性是指发出同样的消息被不同类型的对象接收时有可能导致完全不同的行为。
	- 多态的实现：
		- 函数重载
		- 运算符重载
		- 虚函数
```cpp
//复数的运算
class Complex {	//复数类声明
public:	
	Complex(double r = 0.0,double i = 0.0) {
    real = r; imag=i;
  }
	void display() const;	//显示复数的值
private:	
	double real;
	double imag;
};		
```	
- 用“+”、“-”能够实现复数的加减运算吗？
- 实现复数加减运算的方法——重载“+”、“-”运算符
	- 多态的类型
	- 多态的实现
- 运算符重载
	- 运算符重载的实质
	- 运算符重载是对已有的运算符赋予多重含义
- 必要性
	- C++中预定义的运算符其运算对象只能是基本数据类型，而不适用于用户自定义类型（如类）
- 实现机制
	- 将指定的运算表达式转化为对运算符函数的调用，运算对象转化为运算符函数的实参。
	- 编译系统对重载运算符的选择，遵循函数重载的选择原则。
		- 运算符重载的规则:
			- C++中能够被重载的运算符有：
```cpp
new 	delete 	new[] 	delete[]
+     - 	* 	/ 	% 	? 	& 	| 	?
! 	    = 	< 	> 	+= 	-= 	*= 	/= 	%=
?= 	  &= 	|= 	<< 	>> 	>>= 	<<= 	== 	!=
<=	   >=	 && 	|| 	++ 	-- 	, 	->* 	->
() 	   []
```
- 不能被重载的运算符：
  - 类属关系运算符"."、成员指针运算符".*"、作用域分辨符"::"、sizeof运算符和三目运算符"?:"
- 只能重载C++语言中已有的运算符，不可臆造新的。
- 不改变原运算符的优先级和结合性。
- 不能改变操作数个数。
- 经重载的运算符，其操作数中至少应该有一个是自定义类型。
	- 两种形式
		- 重载为类的非静态成员函数
	- 重载为非成员函数
		- 运算符函数
		- 声明形式
函数类型  operator 运算符（形参）
{
       ......
}
- 重载为类成员函数时
1. 参数个数=原操作数个数-1	（后置++、--除外）
2. 重载为非成员函数时  参数个数=原操作数个数，且至少应该有一个自定义类型的形参。
- 运算符成员函数的设计
	- 双目运算符 B
	- 如果要重载 B 为类成员函数，使之能够实现表达式 oprd1 B oprd2，其中 oprd1 为A 类对象，则 B 应被重载为 A 类的成员函数，形参类型应该是 oprd2 所属的类型。
	- 经重载后，表达式 oprd1 B oprd2 相当于 oprd1.operator B(oprd2)
  - 将“+”、“-”运算重载为复数类的成员函数。
- 规则:
实部和虚部分别相加减。
- 操作数:
两个操作数都是复数类的对象。
```cpp
#include <iostream>
using namespace std;
class Complex {	//复数类定义
public:	//外部接口
	Complex(double r = 0.0, double i = 0.0) : real(r), imag(i) { }	//构造函数
	Complex operator + (const Complex &c2) const;	//运算符+重载成员函数
	Complex operator - (const Complex &c2) const;	//运算符-重载成员函数
	void display() const;	//输出复数
private:	//私有数据成员
	double real;	//复数实部
	double imag;	//复数虚部
};
Complex Complex::operator + (const Complex &c2) const {	//重载运算符函数实现
	return Complex(real + c2.real, imag + c2.imag); //创建一个临时无名对象作为返回值
}
Complex Complex::operator - (const Complex &c2) const {	//重载运算符函数实现
	return Complex(real - c2.real, imag - c2.imag); //创建一个临时无名对象作为返回值
}
void Complex::display() const {
	cout << "(" << real << ", " << imag << ")" << endl;
}
int main() {	//主函数
	Complex c1(5, 4), c2(2, 10), c3;//定义复数类的对象
	cout << "c1 = "; c1.display();
	cout << "c2 = "; c2.display();
	c3 = c1 - c2;	//使用重载运算符完成复数减法
	cout << "c3 = c1 - c2 = "; c3.display();
	c3 = c1 + c2;	//使用重载运算符完成复数加法
	cout << "c3 = c1 + c2 = "; c3.display();
	return 0;
}
```
程序输出的结果为：

c1 = (5, 4)

c2 = (2, 10)

c3 = c1 - c2 = (3, -6)

c3 = c1 + c2 = (7, 14)

- 运算符成员函数的设计
	- 前置单目运算符 U
	- 如果要重载 U 为类成员函数，使之能够实现表达式 U oprd，其中 oprd 为A类对象，则 U 应被重载为 A 类的成员函数，无形参。
	- 经重载后，表达式 U oprd 相当于 oprd.operator U()后置单目运算符 ++和--
	- 如果要重载 ++或--为类成员函数，使之能够实现表达式  oprd++ 或 oprd-- ，其中 oprd 为A类对象，则 ++或--  应被重载为 A 类的成员函数，且具有一个 int 类型形参。
	- 经重载后，表达式  oprd++ 相当于  oprd.operator ++(0)
```cpp
//运算符前置++和后置++重载为时钟类的成员函数。
//前置单目运算符，重载函数没有形参，对于后置单目运算符，重载函数需要有一个整型形参。
//操作数是时钟类的对象。
//实现时间增加1秒钟。
#include <iostream>
using namespace std;
class Clock {	//时钟类声明定义
public:	//外部接口
	Clock(int hour = 0, int minute = 0, int second = 0);
	void showTime() const;
	Clock& operator ++ (); //前置单目运算符重载
	Clock operator ++ (int);//后置单目运算符重载
private:	//私有数据成员
	int hour, minute, second;
};
//前置单目运算符重载函数
Clock & Clock::operator ++ () {
	second++;
	if (second >= 60) {
		second -= 60;
		minute++;
		if (minute >= 60) {
			minute -= 60;
			hour = (hour + 1) % 24;
		}
	}
	return *this;
}
//后置单目运算符重载
Clock Clock::operator ++ (int) {
	//注意形参表中的整型参数
	Clock old = *this;
	++(*this);	//调用前置“++”运算符
	return old;
}
//其它成员函数的实现略

int main() {
	Clock myClock(23, 59, 59);
	cout << "First time output: ";
	myClock.showTime();
	cout << "Show myClock++:    ";
	(myClock++).showTime();
	cout << "Show ++myClock:    ";
	(++myClock).showTime();
	return 0;
}
```
程序运行结果为：

First time output: 23:59:59

Show myClock++: 23:59:59

Show ++myClock: 0:0:1

函数的形参代表依自左至右次序排列的各操作数。

后置单目运算符 ++和--的重载函数，形参列表中要增加一个int，但不必写形参名。

如果在运算符的重载函数中需要操作某类对象的私有成员，可以将此函数声明为该类的友元。

双目运算符 B重载后，表达式oprd1 B oprd2 等同于operator B(oprd1,oprd2 )
前置单目运算符 B重载后，表达式 B oprd 等同于operator B(oprd )
后置单目运算符 ++和--重载后，表达式 oprd B 等同于operator B(oprd,0 )
```cpp
//以非成员函数形式重载Complex的加减法运算和“<<”运算符
//将+、-（双目）重载为非成员函数，并将其声明为复数类的友元，两个操作数都是复数类的常引用。
//将<<（双目）重载为非成员函数，并将其声明为复数类的友元，它的左操作数是std::ostream引用，右操作数为复数类的常引用，返回std::ostream引用，用以支持下面形式的输出：cout << a << b;该输出调用的是：operator << (operator << (cout, a), b);
#include <iostream>
using namespace std;
class Complex {	//复数类定义
public:	//外部接口
	Complex(double r = 0.0, double i = 0.0) : real(r), imag(i) { }	//构造函数
	friend Complex operator + (const Complex &c1, const Complex &c2);	//运算符+重载
	friend Complex operator - (const Complex &c1, const Complex &c2);	//运算符-重载
	friend ostream & operator << (ostream &out, const Complex &c); //运算符<<重载
private:	//私有数据成员
	double real;	//复数实部
	double imag;	//复数虚部
};
Complex operator + (const Complex &c1, const Complex &c2) {
	return Complex(c1.real + c2.real, c1.imag + c2.imag) 
}
Complex operator - (const Complex &c1, const Complex &c2) {
	return Complex(c1.real - c2.real, c1.imag - c2.imag) 
}
ostream & operator << (ostream &out, const Complex &c) {
	out << "(" << c.real << ", " << c.imag << ")";
	return out;
}
```

- 静态绑定与动态绑定
	- 绑定
		- 程序自身彼此关联的过程，确定程序中的操作调用与执行该操作的代码间的关系。
	- 静态绑定
		- 绑定过程出现在编译阶段，用对象名或者类名来限定要调用的函数。
	- 动态绑定
		- 绑定工作在程序运行时执行，在程序运行时才确定将要调用的函数。
```cpp
#include<iostream>
using namespace std;
class Point {
public:
	Point(double x, double y) : x(x), y(y) { }
	double area()  const { return 0.0; }
private:
	double x, y;
};
class Rectangle: public Point {
public:
	Rectangle(double x, double y, double w, double h);
	double area() const  { return  w * h; }
private:
	double w, h;
};
Rectangle::Rectangle(double x, double y, double w, double h) :Point(x, y), w(w), h(h) { }

void fun(const Point &s) {
	cout << "Area = " << s.area() << endl;
}
int main() {
	Rectangle rec(3.0, 5.2, 15.0, 25.0);
	fun(rec);
	return 0;
}
```
运行结果：

Area = 0
```cpp
#include<iostream>
using namespace std;
class Point
{
public:
	Point(double x, double y) : x(x), y(y) { }
	virtual double area()  const { return 0.0; }
private:
	double x, y;
};
class Rectangle:public Point {
public:
	Rectangle(double x, double y, double w, double h);
	virtual double area() const { return  w * h; }
  private:
	double w, h;
};
//其他函数同上例
void fun(const Point &s) {
	cout << "Area = " << s.area() << endl;
}
int main() {
	Rectangle rec(3.0, 5.2, 15.0, 25.0);
	fun(rec);
	return 0;
}
```
运行结果：
Area = 375

- 运算符重载为成员函数
	- 运算符重载为非成员函数
		- 虚函数
	- 虚函数是动态绑定的基础。
	- 是非静态的成员函数。
	- 在类的声明中，在函数原型之前写virtual。
	- virtual 只用来说明类声明中的原型，不能用在函数实现时。
	- 具有继承性，基类中声明了虚函数，派生类中无论是否说明，同原型函数都自动为虚函数。
	- 本质：不是重载声明而是覆盖。
		- 调用方式：通过基类指针或引用，执行时会根据指针指向的对象的类，决定调用哪个函数。
```cpp
#include <iostream>
using namespace std;

class Base1 { //基类Base1定义
public:
	virtual void display() const;	//虚函数
};
void Base1::display() const {
	cout << "Base1::display()" << endl;
}

class Base2: public Base1 { //公有派生类Base2定义
public:
	void display() const;	//覆盖基类的虚函数
};
void Base2::display() const {
	cout << "Base2::display()" << endl;
}
//公有派生类Derived定义
class Derived: public Base2 { 
public:
	void display() const; //覆盖基类的虚函数
};
void Derived::display() const {
	cout << "Derived::display()" << endl;
}
//参数为指向基类对象的指针
void fun(Base1 *ptr) { 
	ptr->display();	//"对象指针->成员名"
}
int main() {	//主函数
	Base1 base1;	//定义Base1类对象
	Base2 base2;	//定义Base2类对象
	Derived derived;	//定义Derived类对象
	fun(&base1);	//用Base1对象的指针调用fun函数
	fun(&base2);	//用Base2对象的指针调用fun函数
	fun(&derived);	//用Derived对象的指针调用fun函数
	return 0;
}
```
- 运行结果：

Base1::display()

Base2::display()

Derived::display()
- 一般虚函数成员
- 虚析构函数
	- 为什么需要虚析构函数？
		- 可能通过基类指针删除派生类对象；
		- 如果你打算允许其他人通过基类指针调用对象的析构函数（通过delete这样做是正常的），就需要让基类的析构函数成为虚函数，否则执行delete的结果是不确定的。
		- 构造函数不允许是虚函数。因为创建一个对象时总是要明确指定对象的类型。
	- 纯虚函数与抽象类
		- 纯虚函数
		- 抽象类
			- 带有纯虚函数的类称为抽象类:
```cpp
class  类名
 {
     virtual 类型 函数名(参数表)=0; 
  //纯虚函数
   ...
}
- 作用
  - 抽象类为抽象和设计的目的而声明，将有关的数据和行为组织在一个继承层次结构中，保证派生类具有要求的行为。
	- 对于暂时无法实现的函数，可以声明为纯虚函数，留给派生类去实现。
- 注意
	- 抽象类只能作为基类来使用。
	- 不能声明抽象类的对象。
	- 构造函数不能是虚函数，析构函数可以是虚函数。
```cpp
#include <iostream>
using namespace std;
class Base1 { //基类Base1定义
public:
	virtual void display() const = 0;  //纯虚函数
};
class Base2: public Base1 { //公有派生类Base2定义
public:
	void display() const {  //覆盖基类的虚函数
		cout << "Base2::display()" << endl;
	}
};
class Derived: public Base2 { //公有派生类Derived定义
public:
	void display() const {  //覆盖基类的虚函数
		cout << "Derived::display()" << endl;
	}
};
void fun(Base1 *ptr) {
	ptr->display();	//"对象指针->成员名"
}
int main() {	//主函数
	Base2 base2;	//定义Base2类对象
	Derived derived;	//定义Derived类对象
	fun(&base2);	//用Base2对象的指针调用fun函数
	fun(&derived); //用Derived对象的指针调用fun函数
	return 0;
}
```
运行结果：

Base2::display()

Derived::display()

- 变步长梯形积分算法求解函数的定积分
	- 算法基本原理
	- 程序设计分析
	- 源程序及说明
	- 运行结果与分析
- 深度探索
	- 多态类型与非多态类型
	- 多态类型与非多态类型
	- 有虚函数的类类型称为多态类型
	- 其它类型皆为非多态类型
	- 二者的差异
	- 语言层面的差异
	- 多态类型支持运行时类型识别
	- 多态类型对象占用额外的空间
	- 设计原则上的差异
	- 多态类型
	- 多态类型的析构函数一般应为虚函数
	- 非多态类型	
	- 非多态类型不宜作为公共基类
	-  由于没有利用动态多态性，一般可以用组合，而无需用共有继承；如果继承，则由于析构函数不是虚函数，删除对象时所执行操作与指针类型有关，易引起混乱。
把不需被继承的类型设定为非多态类型
由于成员函数都是静态绑定，调用速度较快；
对象占用空间较小。
- 运行时类型识别
	- 允许在运行时通过基类指针（或引用）辨别对象所属的具体派生类；
	- 只对多态类型适用；
	- 比虚函数动态绑定的开销更大，因此应仅对虚函数无法解决的问题使用。
	- 运行时类型识别的方式
	- 用dynamic_cast做类型转换的尝试；
	- 用typeid直接获取类型信息。
		- dynamic_cast的使用
- 语法形式
	- dynamic_cast<目的类型>(表达式)
	- 功能
		- 将基类指针转换为派生类指针，将基类引用转换为派生类引用；
	- 转换是有条件的
		- 如果指针（或引用）所指对象的实际类型与转换的目的类型兼容，则转换成功进行；
		- 否则如执行的是指针类型的转换，则得到空指针；如执行的是引用类型的转换，则抛出异常。
```cpp
#include <iostream>
using namespace std;
class Base {
public:
	virtual void fun1() { cout << "Base::fun1()" << endl; }
	virtual ~Base() { }
};
class Derived1: public Base {
public:
	virtual void fun1() { cout << "Derived1::fun1()" << endl; }
	virtual void fun2() { cout << "Derived1::fun2()" << endl; }
};
class Derived2: public Derived1 {
public:
	virtual void fun1() { cout << "Derived2::fun1()" << endl; }
	virtual void fun2() { cout << "Derived2::fun2()" << endl; }
}; 
void fun(Base *b) {
	b->fun1();
	//尝试将b转换为Derived1指针
	Derived1 *d = dynamic_cast<Derived1 *>(b);
	//判断转换是否成功
	if (d != 0) d->fun2();
}
int main() {
	Base b;
	fun(&b);
	Derived1 d1;
	fun(&d1);
	Derived2 d2;
	fun(&d2);
	return 0;
}
```
运行结果：

Base::fun1()

Derived1::fun1()

Derived1::fun2()

Derived2::fun1()

Derived2::fun2()
- typeid的使用
	- 语法形式
		- typeid ( 表达式 )
		- typeid ( 类型说明符 )
- 功能
	- 获得表达式或类型说明符的类型信息
	- 表达式有多态类型时，会被求值，并得到动态类型信息；
	- 否则，表达式不被求值，只能得到静态的类型信息。
	- 类型信息用type_info对象表示
	- type_info是typeinfo头文件中声明的类；
		- typeid的结果是type_info类型的常引用；
		- 可以用type_info的重载的“==”、“!=”操作符比较两类型的异同；
	- type_info的name成员函数返回类型名称，类型为const char *。
		- typeid示例
```cpp
#include <iostream>
#include <typeinfo>
using namespace std;
class Base {
public:
	virtual ~Base() { }
};
class Derived: public Base { };
void fun(Base *b) {
	//得到表示b和*b类型信息的对象
	const type_info &info1 = typeid(b);
	const type_info &info2 = typeid(*b);
	cout << "typeid(b): " << info1.name() << endl;
	cout << "typeid(*b): " << info2.name() << endl;
	if (info2 == typeid(Base)) //判断*b是否为Base类型
		cout << "A base class!" << endl;
}
int main() {
	Base b;
	fun(&b);
	Derived d;
	fun(&d);
	return 0;
}
```
运行结果：

typeid(b): class Base *

typeid(*b): class Base

A base class!

typeid(b): class Base *

typeid(*b): class Derived
- 虚函数动态绑定的实现原理
	- 动态选择被执行的函数
	- 函数的调用，需要通过函数代码的入口地址
	- 把函数入口地址作为变量，在不同情况下赋予不同的值，通过该变量调用函数，就可动态选择被执行的函数
- 虚表
	- 每个多态类有一个虚表（virtual table）
	- 虚表中有当前类的各个虚函数的入口地址
	- 每个对象有一个指向当前类的虚表的指针（虚指针vptr）
- 动态绑定的实现
	- 构造函数中为对象的虚指针赋值
	- 通过多态类型的指针或引用调用成员函数时，通过虚指针找到虚表，进而找到所调用的虚函数的入口地址
	- 通过该入口地址调用虚函数
```cpp
class Base {
public:
	virtual void f();
	virtual void g();
private:
	int i;
};
class Derived: public Base {
public:
	virtual void f(); //覆盖Base::f
	virtual void h(); //新增的虚函数
private:
	int j;
};
```
- 第九章 群体类与群体数据的组织
	- 函数模板与类模板
		- 函数模板
			- 函数模板可以用来创建一个通用功能的函数，以支持多种不同形参，进一步简化重载函数的函数体设计。
	- 定义方法：
		- template <模板参数表> 
	- 函数定义
```cpp
//求绝对值函数的模板
#include <iostream>
using namespace std;
template<typename T>
T abs(T x) {
	return x < 0? -x : x;
}
int main() {
	int n = -5;
	double d = -5.5;
	cout << abs(n) << endl;
	cout << abs(d) << endl;
	return 0;
}
```
运行结果：

5

5.5
- 求绝对值函数的模板分析
	- 编译器从调用abs()时实参的类型，推导出函数模板的类型参数。例如，对于调用表达式abs(n)，由于实参n为int型，所以推导出模板中类型参数T为int。
	- 当类型参数的含义确定后，编译器将以函数模板为样板，生成一个函数：
```cpp
	int abs(int x)
	{
		return x < 0 ? –x : x;
	}
```
- 类模板
	- 使用类模板使用户可以为类声明一种模式，使得类中的某些数据成员、某些成员函数的参数、某些成员函数的返回值，能取任意类型（包括基本类型的和用户自定义类型）。
- 类模板的声明
	- 类模板：
```cpp	
template <模板参数表>
class 类名
{类成员声明}
如果需要在类模板以外定义其成员函数，则要采用以下的形式：
template <模板参数表>
类型名 类名<模板参数标识符列表>::函数名(参数表)
```
```cpp
#include <iostream>
#include <cstdlib>
using namespace std;
// 结构体Student
struct Student {
  int id;  //学号
  float gpa;   //平均分
};  
template <class T>
class Store {//类模板：实现对任意类型数据进行存取
private:
	T item;	// item用于存放任意类型的数据
	bool haveValue;  // haveValue标记item是否已被存入内容
public:
	Store();	// 缺省形式（无形参）的构造函数
	T &getElem();	//提取数据函数
	void putElem(const T &x);  //存入数据函数
};
//以下实现各成员函数。
template <class T>	//缺省构造函数的实现 
Store<T>::Store(): haveValue(false) { }
template <class T>     //提取数据函数的实现
T &Store<T>::getElem() {
	//如试图提取未初始化的数据，则终止程序
	if (!haveValue) {	
		cout << "No item present!" << endl;
		exit(1);	//使程序完全退出，返回到操作系统。
	}
	return item;    // 返回item中存放的数据 
}
template <class T>	//存入数据函数的实现 
void Store<T>::putElem(const T &x) {
	// 将haveValue 置为true，表示item中已存入数值	haveValue = true;	
	item = x;			// 将x值存入item
}
int main() {
	Store<int> s1, s2;	
	s1.putElem(3);	
	s2.putElem(-7);
	cout << s1.getElem() << "  " << s2.getElem() << endl;
	Student g = { 1000, 23 };
	Store<Student> s3;
	s3.putElem(g); 
	cout << "The student id is " << s3.getElem().id << endl;
	Store<double> d;
	cout << "Retrieving object D... ";
	cout << d.getElem() << endl
  //由于d未经初始化,执行函数D.getElement()时导致程序终止
	return 0;
}
```
- 线性群体
	- 线性群体的概念
		- 群体是指由多个数据元素组成的集合体。群体可以分为两个大类：线性群体和非线性群体。
		- 线性群体中的元素按位置排列有序，可以区分为第一个元素、第二个元素等。
		- 非线性群体不用位置顺序来标识元素。
		- 线性群体中的元素次序与其位置关系是对应的。在线性群体中，又可按照访问元素的不同方法分为直接访问、顺序访问和索引访问。
		- 直接访问群体————数组类
		静态数组是具有固定元素个数的群体，其中的元素可以通过下标直接访问。
		- 缺点：大小在编译时就已经确定，在运行时无法修改。
		- 动态数组由一系列位置连续的，任意数量相同类型的元素组成。
		- 优点：其元素个数可在程序运行时改变。
		- vector就是用类模板实现的动态数组。
	- 动态数组类模板：
```cpp
#ifndef ARRAY_H
#define ARRAY_H
#include <cassert>
template <class T> //数组类模板定义
class Array {
private:
	T* list;//用于存放动态分配的数组内存首地址
	int size;	//数组大小（元素个数）
public:
	Array(int sz = 50);		//构造函数
	Array(const Array<T> &a);	//拷贝构造函数
	~Array();			//析构函数
	Array<T> & operator = (const Array<T> &rhs); //重载"=“
	T & operator [] (int i); //重载"[]”
	const T & operator [] (int i) const;	
	operator T * ();	//重载到T*类型的转换
	operator const T * () const;
	int getSize() const;	//取数组的大小
	void resize(int sz);	//修改数组的大小
};
```
- 数组类模板模板的构造函数（直接访问的先行群体）
```cpp
// 构造函数
template <class T>
Array<T>::Array(int sz) {
//sz为数组大小（元素个数），应当非负
	assert(sz >= 0);	
	// 将元素个数赋值给变量size
	size = sz;
	//动态分配size个T类型的元素空间
	list = new T [size];	
}
- 数组类模板的拷贝构造函数
//拷贝构造函数
```cpp
template <class T>
Array<T>::Array(const Array<T> &a) {
	//从对象x取得数组大小，并赋值给当前对象的成员
	size = a.size;
	//为对象申请内存并进行出错检查
	list = new T[size];// 动态分配n个T类型的元素空间
	//从对象X复制数组元素到本对象  
	for (int i = 0; i < size; i++)
		list[i] = a.list[i];
}
```
- 关于浅拷贝与深拷贝
	- 先考虑一种情况，对一个已知对象进行拷贝，编译系统会自动调用一种构造函数——拷贝构造函数，如果用户未定义拷贝构造函数，则会调用默认拷贝构造函数。
```cpp
//main.cpp
#include <iostream>
#include "student.h"
int main()
{
  Student s1;
  Student s2(s1);//Student s2 = s1;//复制对象
  return 0;
}
//student.h
#ifndef STUDENT_H
#define STUDENT_H
class Student
{
  private:
  int num;
  char *name;
  public:
  Student();
  ~Student();
};
#endif
//student.cpp
#include "student.h"
#include <iostream>
using namespace std;
Student::Student()
{
  name = new char(20);
  cout << "Student" << endl;
}
Student::~Student()
{
  cout << "~Student " << (int)name << endl;
  delete name;
  name = NULL;
}
```
- 执行结果：调用一次构造函数，调用两次析构函数，两个对象的指针成员所指内存相同，这会导致什么问题呢？
- name指针被分配一次内存，但是程序结束时该内存却被释放了两次，会造成内存泄漏问题！
- 这是由于编译系统在我们没有自己定义拷贝构造函数时，会在拷贝对象时调用默认拷贝构造函数，进行的是浅拷贝！即对指针name拷贝后会出现两个指针指向同一个内存空间。
- 所以，在对含有指针成员的对象进行拷贝时，必须要自己定义拷贝构造函数，使拷贝后的对象指针成员有自己的内存空间，即进行深拷贝，这样就避免了内存泄漏发生。
	- 自己定义拷贝构造函数：
```cpp
//student.h
#ifndef STUDENT_H
#define STUDENT_H
class Student
{
  private:
  int num;
  char *name;
    public:
    Student();//构造函数
    ~Student();//析构函数
    Student(const Student &s);
		//拷贝构造函数，const防止对象被改变
};
#endif
//student.cpp
#include "student.h"
#include <iostream>
#include <string.h>
using namespace std;
Student::Student()
{
  name = new char(20);
  cout << "Student " << endl;
}
Student::~Student()
{
  cout << "~Student " << (int)name << endl;
  delete name;//在这个地方释放内存空间
  name = NULL;
}
Student::Student(const Student &s)
{
         name = new char(20);
         memcpy(name, s.name, strlen(s.name));
         cout << "copy Student " << endl;
}
```
- 执行结果：调用一次构造函数，一次自定义拷贝构造函数，两次析构函数。两个对象的指针成员所指内存不同。
- 总结：浅拷贝只是对指针的拷贝，拷贝后两个指针指向同一个内存空间，深拷贝不但对指针进行拷贝，而且对指针指向的内容进行拷贝，经深拷贝后的指针是指向两个不同地址的指针。
- 再说几句：
	- 当对象中存在指针成员时，除了在复制对象时需要考虑自定义拷贝构造函数，还应该考虑以下两种情形：
1. 当函数的参数为对象时，实参传递给形参的实际上是实参的一个拷贝对象，系统自动通过拷贝构造函数实现；
2. 当函数的返回值为一个对象时，该对象实际上是函数内对象的一个拷贝，用于返回函数调用处。
	- 数组类模板的重载"="运算符函数（直接访问的线性群体）
```cpp
//重载“=”运算符
template <class T>
Array<T> &Array<T>::operator = (const Array<T>& rhs) {
	if (&rhs != this) {
		if (size != rhs.size) {
			delete [] list;	//删除数组原有内存
			size = rhs.size;	//设置本对象的数组大小
			list = new T[size];	//重新分配n个元素的内存
		}
		//从对象X复制数组元素到本对象  
		for (int i = 0; i < size; i++)
			list[i] = rhs.list[i];
	}
	return *this;	//返回当前对象的引用
}
```
- 数组类模板的重载下标操作符函数
```cpp
template <class T>
T &Array<T>::operator[] (int n) {
	assert(n >= 0 && n < size);//越界检查
	return list[n];	 //返回下标为n的数组元素
}
template <class T>
const T &Array<T>::operator[] (int n) const {
	assert(n >= 0 && n < size); //越界检查
	return list[n];	 //返回下标为n的数组元素
}
```
- 为什么有的函数返回引用
	- 如果一个函数的返回值是一个对象的值，就不应成为左值。
	- 如果返回值为引用。由于引用是对象的别名，通过引用当然可以改变对象的值。
		- 重载指针转换操作符
```cpp
template <class T>
Array<T>::operator T * () {
	return list;	//返回私有数组的首地址
}

template <class T>
Array<T>::operator const T * () const {
	return list;	//返回私有数组的首地址
}
#include <iostream>
using namespace std;
void read(int *p, int n) {
 for (int i = 0; i < n; i++)
    cin >> p[i];
}
int main() {
 int a[10];
 read(a, 10);
 return 0;
}
#include "Array.h"
#include <iostream>
using namespace std;
void read(int *p, int n) {
 for (int i = 0; i < n; i++)
   cin >> p[i];
}
int main() {
 Array<int> a(10);
 read(a, 10);
 return 0;
}
		- Array类的应用
		例9-4求范围2~N中的质数，N在程序运行时由键盘输入。
#include <iostream>
#include <iomanip>
#include "Array.h"
using namespace std;
int main() {
Array<int> a(10);	
// 用来存放质数的数组，初始状态有10个元素。
	int n, count = 0;
	cout << "Enter a value >= 2 as upper limit for prime numbers: ";
	cin >> n;
	for (int i = 2; i <= n; i++) {
		bool isPrime = true;
		for (int j = 0; j < count; j++)
			if (i % a[j] == 0) {	//若i被a[j]整除，说明i不是质数
				isPrime = false; break;
			}
		if (isPrime) { 
			if (count == a.getSize()) a.resize(count * 2);
			a[count++] = i;
		}
	}
	for (int i = 0; i < count; i++)	cout << setw(8) << a[i];
	cout << endl;
	return 0;
}
```
- 顺序访问群体————链表类
	- 链表是一种动态数据结构，可以用来表示顺序访问的线性群体。
	- 链表是由系列结点组成的，结点可以在运行时动态生成。
	- 每一个结点包括数据域和指向链表中下一个结点的指针（即下一个结点的地址）。如果链表每个结点中只有一个指向后继结点的指针，则该链表称为单链表。
	- 单链表的结点类模板
```cpp
template <class T>
class Node {
private:
  Node<T> *next;
public:
  T data; 
  Node(const T& item,Node<T>* next = 0);
  void insertAfter(Node<T> *p);
  Node<T> *deleteAfter();
  Node<T> *nextNode() const;
};    
```
- 在结点之后插入一个结点
```cpp
template <class T>
void Node<T>::insertAfter(Node<T> *p) {
  //p节点指针域指向当前节点的后继节点
  p->next = next;     
  next = p; //当前节点的指针域指向p 
}
```
-  删除结点之后的结点
```cpp
Node<T> *Node<T>::deleteAfter(void) {
  Node<T> *tempPtr = next;  
  if (next == 0) 
     return 0;
  next = tempPtr->next; 
  return tempPtr;   
}
```
- 链表的基本操作
	- 生成结点
	- 插入结点
	- 查找结点
	- 删除结点
	- 遍历链表
	- 清空链表
- 链表类模板
```cpp
#ifndef LINKEDLIST_H
#define LINKEDLIST_H
#include "Node.h"
template <class T>
class Link							edList {
private:
	//数据成员：
	Node<T> *front, *rear
	Node<T> *prevPtr, *currPtr;   
	int size;
	int position;	
Node<T> *newNode(const T &item,Node<T> *ptrNext=NULL);
	void freeNode(Node<T> *p);
	void copy(const LinkedList<T>& L);
public:
	LinkedList();	
	LinkedList(const LinkedList<T> &L);  
	~LinkedList();	
LinkedList<T> & operator = (const LinkedList<T> &L); 
int getSize() const;
bool isEmpty() const;
void reset(int pos = 0
	void next();
	bool endOfList() const;
	int currentPosition(void) const;
void insertFront(const T &item);
	void insertRear(const T &item);
	void insertAt(const T &item);
	void insertAfter(const T &item);
	T deleteFront();	
	void deleteCurrent();
	T& data();
	const T& data() const
	void clear();
};
#endif  //LINKEDLIST_H
```
- 链表类应用举例
```cpp
//从键盘输入10个整数，用这些整数值作为结点数据，生成一个链表，按顺序输出链表中结点的数值。然后从键盘输入一个待查找整数，在链表中查找该整数，若找到则删除该整数所在的结点（如果出现多次，全部删除），然后输出删除结点以后的链表。在程序结束之前清空链表。
#include <iostream>
#include "LinkedList.h"
using namespace std;
int main() {
	LinkedList<int> list;
	for (int i = 0; i < 10; i++) {
		int item;
		cin >> item;
		list.insertFront(item);
	}
	
cout << "List: ";
	list.reset();
	while (!list.endOfList()) {
		cout << list.data() << "  ";
		list.next();	
	}
	cout << endl;
int key;
cout << "Please enter some integer needed to be deleted: ";
	cin >> key;
	list.reset();
	while (!list.endOfList()) {
		if (list.data() == key) 
list.deleteCurrent();
		list.next();
	}
	cout << "List: ";
	list.reset();
	while (!list.endOfList()) {
		cout << list.data() << "  ";
		list.next
	}
	cout << endl;
	return 0;
}
```
- 栈类（特殊的线性群体）
	- 栈是只能从一端访问的线性群体，可以访问的这一端称栈顶，另一端称栈底。
		- 栈空
		- 栈中没有元素
		- 栈满
		- 栈中元素个数达到上限
	- 一般状态
		- 栈中有元素，但未达到栈满状态
		- 栈的基本操作
			- 初始化
			- 入栈
			- 出栈
			- 清空栈
			- 访问栈顶元素
			- 检测栈的状态（满、空）
- 栈类模板
```cpp
//Stack.h
#ifndef STACK_H
#define STACK_H
#include <cassert> 
template <class T, 
    int SIZE = 50>
class Stack {
private:
	T list[SIZE];
	int top;
public:
	Stack();
	void push(const T &item);
	T pop();
	void clear();
	const T &peek() const;
	bool isEmpty() const;
	bool isFull() const;
};
```
- 栈的应用
```cpp
//一个简单的整数计算器
//实现一个简单的整数计算器，能够进行加、减、乘、除和乘方运算。使用时算式采用后缀输入法，每个操作数、操作符之间都以空白符分隔。例如，若要计算"3+5"则输入"3  5  +"。乘方运算符用"^"表示。每次运算在前次结果基础上进行，若要将前次运算结果清除，可键入"c"。当键入"q"时程序结束。
Calculator.h  Calculator.cpp 
//Calculator.h
#ifndef CALCULATOR_H
#define CALCULATOR_H
#include "Stack.h"	
//包含栈类模板定义文件
class Calculator {	//计算器类
private:
	Stack<double> s;	// 操作数栈
	void enter(double num);	//将操作数num压入栈
	//连续将两个操作数弹出栈，放在opnd1和opnd2中
	bool getTwoOperands(double &opnd1, double &opnd2);
	void compute(char op);	//执行由操作符op指定的运算
public:
	void run();		//运行计算器程序
	void clear();	//清空操作数栈
};
#endif //CALCULATOR_H
//Calculator.cpp
#include "Calculator.h"
#include <iostream>
#include <sstream>
#include <cmath>
using namespace std;

//工具函数，用于将字符串转换为实数
inline double stringToDouble(const string &str) {
	istringstream stream(str);	//字符串输入流
	double result;
	stream >> result;
	return result;
}
void Calculator::enter(double num) {	//将操作数num压入栈
	s.push(num);
}
bool Calculator::getTwoOperands(double &opnd1, double &opnd2) {
	if (s.isEmpty()) {	//检查栈是否空
		cerr << "Missing operand!" << endl;
		return false;
	}
	opnd1 = s.pop();	//将右操作数弹出栈
	if (s.isEmpty()) {	//检查栈是否空
		cerr << "Missing operand!" << endl;
		return false;
	}
	opnd2 = s.pop();	//将左操作数弹出栈
	return true;
}
void Calculator::compute(char op) {	//执行运算
	double operand1, operand2;
	bool result = getTwoOperands(operand1, operand2);   
	if (result) {	
		//如果成功，执行运算并将运算结果压入栈
		switch(op) {
		case '+': s.push(operand2 + operand1); break;
		case '-': s.push(operand2 - operand1); break;
		case '*': s.push(operand2 * operand1); break;
		case '/':
			if (operand1 == 0) {	//检查除数是否为0
				cerr << "Divided by 0!" << endl;
				s.clear();	//除数为0时清空栈
			} else
				s.push(operand2 / operand1);
			break;
		case '^': s.push(pow(operand2, operand1)); break;
		default:
			cerr << "Unrecognized operator!" << endl;
			break;
		}
		cout << "= " << s.peek() << " ";	//输出本次运算结果 
	} else
		s.clear();	//操作数不够，清空栈
}
void Calculator::run() { //读入并处理后缀表达式
	string str;
	while (cin >> str, str != "q") {
		switch(str[0]) {
		case 'c': s.clear(); break;
		case '-': //遇'-'需判断是减号还是负号
			if (str.size() > 1)
				enter(stringToDouble(str));	
			else
				compute(str[0]);	
			break;
		case '+':	//遇到其它操作符时
		case '*':
		case '/':
		case '^':
			compute(str[0]);
		default: //若读入的是操作数，转换为整型后压入栈
			enter(stringToDouble(str)); break;
		}
	}
}
void Calculator::clear() {	//清空操作数栈
	s.clear(); 
}
```
```cpp
#include "Calculator.h"
int main() {
	Calculator c;
	c.run();
	return 0;
}
```
- 队列类
	- 队列是只能向一端添加元素，从另一端删除元素的线性群体
	- 队列的基本状态
		- 队空
		- 队列中没有元素
		- 队满
		- 队列中元素个数达到上限
	- 一般状态
		- 队列中有元素，但未达到队满状态
			- 循环队列
			- 在想象中将数组弯曲成环形，元素出队时，后继元素不移动，每当队尾达到数组最后一个元素时，便再回到数组开头。
	- 群体数据的组织
		- 插入排序
		- 选择排序
		- 交换排序
		- 顺序查找
		- 折半查找
	- 排序（sorting）
		- 排序是计算机程序设计中的一种重要操作，它的功能是将一个数据元素的任意序列，重新排列成一个按关键字有序的序列。
		- 数据元素：数据的基本单位。在计算机中通常作为一个整体进行考虑。一个数据元素可由若干数据项组成。
		- 关键字：数据元素中某个数据项的值，用它可以标识（识别）一个数据元素。	
		- 在排序过程中需要完成两种基本操作：
			- 比较两个数的大小
			- 调整元素在序列中的位置
				- 内部排序与外部排序
					- 内部排序：待排序的数据元素存放在计算机内存中进行的排序过程。
					- 外部排序：待排序的数据元素数量很大，以致内存存中一次不能容纳全部数据，在排序过程中尚需对外存进行访问的排序过程。
		- 内部排序方法
			- 插入排序
			- 选择排序
			- 交换排序
			- 插入排序
	- 基本思想
		- 每一步将一个待排序元素按其关键字值的大小插入到已排序序列的适当位置上，直到待排序元素插入完为止。
	- 直接插入排序
		- 在插入排序过程中，由于寻找插入位置的方法不同又可以分为不同的插入排序算法，这里我们只介绍最简单的直接插入排序算法。
```cpp		
//直接插入排序函数模板（9_11.h）
template <class T>
void insertionSort(T a[], int n) {
	int i, j;
	T temp;
	for (int i = 1; i < n; i++) {		
		int j = i;
		T temp = a[i];
		while (j > 0 && temp < a[j - 1]) {
			a[j] = a[j - 1];
			j--;
		}
		a[j] = temp;
	}
}
```
- 选择排序
	- 选择排序的基本思想
		- 每次从待排序序列中选择一个关键字最小的元素，（当需要按关键字升序排列时），顺序排在已排序序列的最后，直至全部排完。
		- 直接选择排序
			- 在选择类排序方法中，从待排序序列中选择元素的方法不同，又分为不同的选择排序方法，其中最简单的是通过顺序比较找出待排序序列中的最小元素，称为直接选择排序。
```cpp
//直接选择排序函数模板
template <class T>
void mySwap(T &x, T &y) {
	T temp = x;
	x = y;
	y = temp;
}
template <class T>
void selectionSort(T a[], int n) {
	for (int i = 0; i < n - 1; i++) {
		int leastIndex = i;	
		for (int j = i + 1; j < n; j++)
			if (a[j] < a[leastIndex])
				leastIndex = j;
		mySwap(a[i], a[leastIndex	]);
	}
}
```
- 交换排序
	- 交换排序的基本思想
		- 两两比较待排序序列中的元素，并交换不满足顺序要求的各对元素，直到全部满足顺序要求为止。
		- 最简单的交换排序方法--起泡排序
			对具有n个元素的序列按升序进行起泡排序的步骤：
			- 首先将第一个元素与第二个元素进行比较，若为逆序，则将两元素交换。然后比较第二、第三个元素，依次类推，直到第n-1和第n个元素进行了比较和交换。此过程称为第一趟起泡排序。经过第一趟，最大的元素便被交换到第n个位置。
			- 对前n-1个元素进行第二趟起泡排序，将其中最大元素交换到第n-1个位置。
			- 如此继续，直到某一趟排序未发生任何交换时，排序完毕。对n个元素的序列，起泡排序最多需要进行n-1趟。
```cpp
//起泡排序的举例
//对整数85243按照升序进行排序
//起泡排序函数模板
template <class T>
void mySwap(T &x, T &y) {
	T temp = x;
	x = y;
	y = temp;
}
template <class T>
void bubbleSort(T a[], int n) {
	int i = n – 1;
	while (i > 0) {
		int lastExchangeIndex = 0;
		for (int j = 0; j < i; j++)
			if (a[j + 1] < a[j]) {	
				mySwap(a[j], a[j + 1]);
				lastExchangeIndex = j;
			}
		i = lastExchangeIndex;
	}
}
```
- 顺序查找
	- 其基本思想
		- 从序列的首元素开始，逐个元素与待查找的关键字进行比较，直到找到相等的。若整个序列中没有与待查找关键字相等的元素，就是查找不成功。
```cpp
//顺序查找函数模板
template <class T>
int seqSearch(const T list[], int n, const T &key) {
	for(int i = 0; i < n; i++)
		if (list[i] == key)
			return i;            
	return -1;                 
}
```
- 折半查找
	- 对于已按关键字排序的序列，经过一次比较，可将序列分割成两部分，然后只在有可能包含待查元素的一部分中继续查找，并根据试探结果继续分割，逐步缩小查找范围，直至找到或找不到为止。
```cpp
//折半查找函数模板
			template <class T>
int binSearch(const T list[], int n, const T &key) {
	int low = 0;
	int high = n - 1;
	while (low <= high) {	
		int mid = (low + high) / 2;
		if (key == list[mid])    
			return mid;	
		else if (key < list[mid])
			high = mid – 1;
		else
			low = mid + 1;
	}
	return -1;
}
```
- 深度搜索
	- 类模板 vs 类
		- 类模板不能表示具体的数据类型，但类模板的实例化类是数据类型
```cpp
//如要使reverse函数接收Array的参数
void reverse(Array &arr);
//错误！Array是模板，不能当作一个数据类型。
void reverse(Array<int> &arr);
//正确。Array<int>是数据类型。
template <class T> reverse (Array<T> &arr);
//正确。T虽未定，但Array<T>表示的是一个类模板实例。
//同一模板在不同参数下的实例是完全无关的类型
//彼此不兼容，无法相互赋值
//通过Store<int>的对象调用的成员函数，无法直接访问Store<double>对象的私有成员
```
- 函数模板 vs 函数
	- 函数模板本身不是函数
		- 编译器不会为函数模板本身生成目标代码
		- 只有函数模板的实例能被调用
```cpp
//以下是一个新的模板
template <class T>void outputArray(const T *array, int count);
//若a是int数组，outputArray(a, 10)等价于outputArray<int>(a, 10)，被调用的是outputArray实例
```
- 模板实例化
- 隐含实例化
- 模板的实例化
	- 根据函数模板生成具体的函数、或根据类模板生成具体的类的过程
- 隐含实例化
	- 编译器会自动按需对模板实例化
	- 所有会被使用的模板实例会被生成
	- 对类模板的隐含实例化并不意味着对它成员函数的定义也进行实例化，当类模板成员函数会被使用时，才会被实例化
- 多文件结构中模板的组织
	- 模板实例化机制带来的新问题
	- 不能把下面与模板相关的定义放在与头文件分离的源文件中
- 函数模板的定义
- 类模板成员函数
- 类模板静态数据成员
	- 解决方法
		- 把与模板相关的定义放在头文件中——最通常的解决办法
- 编译器有特殊处理，保证不会有连接冲突
	- 使用export关键字——编译器支持不好
	- 使用模板的显式实例化机制
	- 显式实例化
		- 语法形式
		- template 实例化目标的声明;
	- 作用
		- 一个模板实例无论是否在本编译单元中被使用，都会被生成
```cpp
template void outputArray(const int *array, int count);
template class Store<double>;
```
- 在多文件结构中的用途
	- 使用在程序中可能会被用到的各种参数对模板显式实例化，使得与模板相关的定义可以放在源文件中
- 为模板定义特殊的实现
	- 模板抓住了算法与数据结构上的共性，但忽略了类型的个性
- 设计出的模板对于具体的数据类型而言未必具有最好的效率
> Stack类模板
- 如果以bool作为类型参数，则有7/8的空间浪费
- Stack<bool,32>中的list数组占32个字节，实际上4个字节就够
+ 模板的特化
	- 为一个模板在特定参数下提供特殊定义
	- 既适用于类模板，又适用于函数模板
	- 对Stack<bool, 32>特化的类定义
```cpp
template <>
class Stack<bool, 32> {
private:
	unsigned list;
	int top;
public:
	Stack();
	void push(bool item);
	bool pop();
	void clear();
	bool peek() const;
	bool isEmpty() const;
	bool isFull() const;
};
```
```cpp
//特化类的部分成员函数定义
void Stack<bool, 32>::push(bool item) {
	assert(!isFull());
	++top;
	list = (list << 1) | (item ? 1 : 0);
}
bool Stack<bool, 32>::pop() {
	assert(!isEmpty());	
	bool result = ((list & 1) == 1);
	list >>= 1; --top; 
	return result;		
}
```
- 类模板的偏特化
	- 对Stack<bool,32>特化的问题
		- 适用范围过窄，SIZE必须是32
	- 将一部分参数固定，而使另一部分参数可变，设计特殊的定义
	- 只适用于类模板
```cpp
//对Stack偏特化的类定义
template <int SIZE>
class Stack<bool, SIZE> {
private:
	enum {
		UNIT_BITS = sizeof(unsigned) * 8,
		ARRAY_SIZE = (SIZE - 1) / UNIT_BITS + 1
	};
	unsigned list[ARRAY_SIZE];
	int top;	
public:
	Stack();
	void push(bool item);
	bool pop();
	void clear();
	bool peek() const;
	bool isEmpty() const; 
	bool isFull() const;
};
```
```cpp
//偏特化类的部分成员函数定义
template <int SIZE>
void Stack<bool, SIZE>::push(bool item) {
	assert(!isFull());
	int index = ++top / UNIT_BITS;
	list[index] = (list[index] << 1) | (item ? 1 : 0);
}
template <int SIZE>
bool Stack<bool, SIZE>::pop() {
	assert(!isEmpty());
	int index = top-- / UNIT_BITS;
	bool result = ((list[index] & 1) == 1);
	list[index] >>= 1; 
	return result;
}
```
- 偏特化不仅允许将一部分模板参数固定，还允许将某一个模板参数所能表示的类型范围缩窄
```cpp
template <class T> class X { … };
//原模板，T可以是所有类型参数
template <class T> class X<T *> { … };
//针对指针类型进行偏特化
template <class T> class X<const T *> { … };
//针对常指针类型进行偏特化
//对于X<const int *>，后两个偏特化版本皆能匹配，但由于第二个更为特殊，会被选中
```
- 函数模板的重载
	- 函数模板不支持偏特化，但可重载，从而完成与类模板偏特化类似的功能
	- 若对函数模板的一次使用能与多个函数模板匹配，最特殊的那个会被选中
```cpp
//针对参数为指针类型的情形，为myMax定义特殊实现
template <class T>
T myMax(T a, T b) {
	return (a > b) ? a : b;
}
template <class T>
T *myMax(T *a, T *b) {
	return (*a > *b) ? a : b;
}
```
- 模板的实例化机制
	- 为模板定义特殊的实现
	- 模板元编程简介
- 什么是模板元编程
	- 在模板实例化的同时利用编译器完成一些计算任务
	- 模板元编程可以把一些通常在运行时才能计算的任务提前到编译时，从而提高程序运行效率,提供一些方便
```cpp
//模板元编程的计算结果可以作为静态数组的大小
//例：编译的时候计算n！
template <unsigned N>
struct Factorial { 
//计算N的阶乘
enum {
  VALUE = N * Factorial<N – 1>::VALUE 
  };
};
template <>
struct Factorial<0> { //设定N = 0时N的阶乘
	enum { VALUE = 1 };
};
```
- Factorial的分析
	- Factorial的使用
```cpp
int s[ Factorial<6>::VALUE ];
Factorial::VALUE的计算过程
//首先试图实例化Factorial<6>；
//要计算Factorial<6>的VALUE，需实例化Factorial<5>，然后是Factorial<4>……
//实例化Factorial<1>时，由于Factorial<0>::VALUE的值已确定，Factorial<1>的VALUE值可计算，完成实例化；
//Factorial<2>到Factorial<6>的实例化相继完成
```
```cpp
//整数次乘方的展开
template <unsigned N>
struct Power {
  template <class T>
  static T value(T x) {
    return x * Power<N - 1>::value(x);
  }
};
template <>
struct Power<1> {
  template <class T>
  static T value(T x) {
    return x;
  }
};
template <unsigned N, class T>
inline T power(T v) {
	return Power<N>::value(v);
}
```
- 第十章 泛型程序设计与c++标准模板库
	- 反省程序设计以及STL的结构
		- 泛型程序设计的基本概念
		将程序写得尽可能通用。将算法从特定的数据结构中抽象出来，成为通用的
	- C++的模板为泛型程序设计奠定了关键的基础 
	- STL是泛型程序设计的一个范例 
		- 容器(container)
		- 迭代器(iterator)
		- 算法（algorithms）
		- 函数对象（function object）
	- 命名空间（namespace）
		- 一个命名空间将不同的标识符集合在一个命名作用域（named scope）内
	- 为了解决命名冲突，可以声明一个命名空间NS：
```cpp
namspace NS {
class File;
void Fun ();
}
//则引用标识符的方式如下，
NS:: File obj;
NS:: Fun ();
```
- 没有声明命名空间的标识符都处于无名的命名空间中
- 可以用using来指定命名空间
	- 经过以下声明：
```cpp
using NS::File;
//在当前作用域中就可以直接引用File
using namespace std;
//命名空间std中所有标识符都可直接引用
```
- 在新的C++标准程序库中，所有标识符都声明在命名空间std中，头文件都不使用扩展名
- STL简介
	- 迭代器
		- 输入流迭代器和输出流迭代器
		- 迭代器的分类
		- 迭代器的区间
		- 迭代器的辅助函数
	- 容器
		- 容器类是容纳、包含一组元素或元素集合的对象。	
		- 异类容器类与同类容器类
		- 顺序容器与关联容器
- 七种基本容器：
	- 向量（vector）
	- 双端队列（deque）
	- 列表（list）
	- 集合（set）
	- 多重集合（multiset）
	- 映射（map）
	- 多重映射（multimap）
- 容器的接口
	- /)_>P通用容器运算符
		- ==，!=，>，>=，<，<=，=
		- 方法（函数）
	- 迭代方法
		- begin()，end()，rbegin()，rend()
	- 访问方法
		- size()，max_size()，swap()，empty()
- 容器的基本功能与分类
	- 顺序容器
		- 顺序容器的接口
		- 插入方法
			- push_front()，push_back()，insert()，运算符“=”
		- 删除方法
			- pop() ，erase()，clear()
		- 迭代访问方法
			- 使用迭代器
			- 其他顺序容器访问方法（不修改访问方法）
		- front()，back()，下标[]运算符
			- 顺序容器--向量
				- 向量属于顺序容器，用于容纳不定长线性序列（即线性群体），提供对序列的快速随机访问（也称直接访问）
				- 向量是动态结构，它的大小不固定，可以在程序运行时增加或减少。
```cpp
//求范围2~N中的质数，N在程序运行时由键盘输入。
//10_1.cpp
#include <iostream>
#include <iomanip>
#include <vector>	//包含向量容器头文件
using namespace std ;
int main()
{    
  vector<int>  A(10);	
  int n;	
  int primecount = 0, i, j;
  cout<<"Enter a value>=2 as upper limit: ";
  cin >> n;
  A[primecount++] = 2;	
  for(i = 3; i < n; i++)
  { if (primecount == A.size())	
     A.resize(primecount + 10); 
    if (i % 2 == 0)
     continue;
    j = 3;
    while (j <= i/2 && i % j != 0)
      j += 2;        
    if (j > i/2) A[primecount++] = i;
  }
  for (i = 0; i<primecount; i++)//输出质数
  { cout<<setw(5)<<A[i]; 
    if ((i+1) % 10 == 0) //每输出10个数换行一次
      cout << endl;
  } 
  cout<<endl;
}
```
- 顺序容器--双端队列
	- 双端队列是一种放松了访问权限的队列。元素可以从队列的两端入队和出队，也支持通过下标操作符“[]”进行直接访问。
	- 使用双端队列容器保存double数值序列
		- 顺序容器--列表
			- 列表主要用于存放双向链表，可以从任意一端开始遍历。列表还提供了拼接（splicing）操作，将一个序列中的元素插入到另一个序列中。
```cpp
//从键盘输入10个整数，用这些整数值作为结点数据，生成一个链表，按顺序输出链表中结点的数值。然后从键盘输入一个待查找整数，在链表中查找该整数，若找到则删除该整数所在的结点（如果出现多次，全部删除），然后输出删除结点以后的链表。在程序结束之前清空链表。
#include <iostream>
#include <list>
using namespace std ;
int main()
{
list<int> Link;	
//构造一个列表用于存放整数链表
 int i, key, item;    
 for(i=0;i < 10;i++)// 输入10个整数依次向表头插入
 {
   cin>>item;
   Link.push_front(item);
 }
 cout<<"List: "; // 输出链表
 list<int>::iterator p=Link.begin(); 
 while(p!=Link.end())//输出各节点数据，直到链表尾
 { cout <<*p << "  ";
   p++;  //使P指向下一个节点
 }
 cout << endl;
 cout << "请输入一个需要删除的整数: ";
 cin >> key;
 Link.remove(key);   
 cout << "List: "; // 输出链表
 p=Link.begin();	// 使P重新指向表头
 while(p!=Link.end())	
 { cout <<*p << "  ";
   p++; // 使P指向下一个节点
 }
 cout << endl;
}
```
- 关联容器
	- 适配器
		- 适配器是一种接口类
		- 为已有的类提供新的接口。
		- 目的是简化、约束、使之安全、隐藏或者改变被修改类提供的服务集合。
- 三种类型的适配器：
	- 容器适配器
		- 用来扩展7种基本容器，它们和顺序容器相结合构成栈、队列和优先队列容器
	- 迭代器适配器
	- 函数对象适配器。
- 迭代器
	- 迭代器是面向对象版本的指针，它们提供了访问容器、序列中每个元素的方法。
- 函数对象
	- 函数对象基本概念及分类
	- 函数适配器
- 算法
	- C++标准模板库中包括70多个算法
		- 包括查找算法，排序算法，消除算法，记数算法，比较算法，变换算法，置换算法和容器管理等等。
	- 这些算法的一个最重要的特性就是它们的统一性，并且可以广泛用于不同的对象和内置的数据类型。
- 容器适配器
	- 容器适配器是用来扩展7种基本容器的
- 栈容器
	- 使用适配器与一种基础容器相结合来实现
	- 应用标准库中的deque顺序容器生成一个整数栈stack。
- 队列容器
	- 使用适配器与一种基础容器相结合来实现的先进先出数据结构。
	- 应用标准库中的deque顺序容器生成一个整数标准队列queue。
- 迭代器
	- 迭代器是面向对象版本的指针
	- 指针可以指向内存中的一个地址
	- 迭代器可以指向容器中的一个位置
	- STL的每一个容器类模版中，都定义了一组对应的迭代器类。使用迭代器，算法函数可以访问容器中指定位置的元素，而无需关心元素的具体类型。
- 迭代器的类型
	- 输入迭代器
	- 可以用来从序列中读取数据
- 输出迭代器
	- 允许向序列中写入数据
- 前向迭代器
	- 既是输入迭代器又是输出迭代器，并且可以对序列进行单向的遍历
- 双向迭代器
	- 与前向迭代器相似，但是在两个方向上都可以对数据遍历
- 随机访问迭代器
	- 也是双向迭代器，但能够在序列中的任意两个位置之间进行跳转。
- 迭代器的适配器 
	- 迭代器适配器是用来扩展（或调整）迭代器功能的类。它本身也被称为迭代器，只是这种迭代器是通过改变另一个迭代器而得到的
- 逆向迭代器
	- 通过重新定义递增运算和递减运算，使其行为正好倒置
- 插入型迭代器
	- 将赋值操作转换为插入操作。通过这种迭代器，算法可以执行插入行为而不是覆盖行为
	- 应用逆向迭代器和后插迭代器来操作向量容器中的元素
- 迭代器相关的辅助函数
	- advance()函数
	- 将迭代器的位置增加，增加的幅度由参数决定
	- distance()函数
	- 返回迭代器之间的距离
	- 函数iter_swap()
		- 交换两个迭代器所指向的元素值
		- 用三个迭代器辅助函数来操作列表容器中的元素。
	- 标准c++库中的算法
		- 算法本身是一种函数模板
		- 不可变序列算法（non-mutating algorithms）
		- 不直接修改所操作的容器内容的算法
		- 可变序列算法（mutating algorithms）
		- 可以修改它们所操作的容器的元素。
- 排序相关算法
	- 数值算法
	- STL算法适配器
	- 不可变序列算法
	- 可变序列算法
	- 排序和搜索算法
	- 数值算法
	- 函数对象
		- 一个行为类似函数的对象，它可以没有参数，也可以带有若干参数，其功能是获取一个值，或者改变操作的状态。
		- 任何普通的函数和任何重载了调用运算符operator()的类的对象都满足函数对象的特征
		- STL中也定义了一些标准的函数对象，如果以功能划分，可以分为算术运算、关系运算、逻辑运算三大类。为了调用这些标准函数对象，需要包含头文件<functional>。
- 深度搜索
	- swap
	- STL组件的类型特征与STL的拓展
	- Boost简介
- 第十一章 流类库与输入输出
	- I/O流的概念及流类库文件
		- 流的引入
```cpp
  scanf("%d",&a); 
	cin>>a;
  printf("%d",a);        
	cout<<a;
```
  - 流：数据从一个对象流动到另一个对象，这种流动抽象为流。
  - 流的操作：建立流、删除流、提取（读操作/输入）、插入（写操作/输出）。
	- 当程序与外界环境进行信息交换时，存在着两个对象，一个是程序中的对象，另一个是文件对象。
	- 流是一种抽象，它负责在数据的生产者和数据的消费者之间建立联系，并管理数据的流动。
	- 程序建立一个流对象，并指定这个流对象与某个文件对象建立连接，程序操作流对象，流对象通过文件系统对所连接的文件对象产生作用。
	- 读操作在流数据抽象中被称为（从流中）提取，写操作被称为（向流中）插入。
- 输出流
	- 最重要的三个输出流是
		- ostream
		- ofstream
		- ostringstream
- 构造输出流对象
	- 预先定义的输出流对象:
		- cout 标准输出
		- cerr 标准错误输出，没有缓冲，发送给它的内容立即被输出。
		- clog 类似于cerr，但是有缓冲，缓冲区满时被输出。
- ofstream类支持磁盘文件输出
	- 如果在构造函数中指定一个文件名，当构造这个文件时该文件是自动打开的
- ofstream myFile("filename");
	- 可以在调用默认构造函数之后使用open成员函数打开文件
- ofstream myFile; //声明一个静态文件输出流对象
```cpp
myFile.open("filename");
//打开文件，使流对象与文件建立联系
//在构造对象或用open打开文件时可以指定模式
ofstream myFile("filename", ios_base::out | ios_base::binary);
```
- 使用插入运算符和操纵符
	- 插入运算符<<
		- 插入(<<)运算符是所有标准C++数据类型预先设计的。
- 用于传送字节到一个输出流对象。
	- 控制输出格式
	- 控制输出宽度
- 为了调整输出，可以通过在流中放入setw操纵符或调用width成员函数为每个项指定输出宽度。
```cpp
//使用width控制输出宽度
#include <iostream>   
using namespace std;
int main() {
	double values[] = { 1.23, 35.36, 653.7, 4358.24 };
	for(int i = 0; i < 4; i++) {
		 cout.width(10);
		 cout << values[i] << endl;}
	return 0;}
```
输出结果:

1.23

35.36

653.7

4358.24
```cpp
//使用*填充
#include <iostream>  
using namespace std; 
int main() {
  double values[]={ 1.23, 35.36, 653.7, 4358.24 };
  for(int i = 0; i < 4; i++)
 { cout.width(10);
    cout.fill('*');
    cout << values[i] << '\n';   }
  return 0;}
```
输出结果：

******1.23

*****35.36

*****653.7

***4358.24
```cpp
//使用setw指定宽度
#include <iostream>
#include <iomanip>
#include <string>
using namespace std;
int main() {
	double values[] = { 1.23, 35.36, 653.7, 4358.24 };
	string names[] = { "Zoot", "Jimmy", "Al", "Stan" };
	for (int i = 0; i < 4; i++)
		cout << setw(6) << names[i]	<< setw(10) << values[i] << endl;
	return 0;}
```
输出结果：
  
	Zoot      1.23
 
 Jimmy     35.36
 
    Al     653.7
 
  Stan   4358.24
```cpp
//设置对齐方式
//输出对齐方式控制可通过预定义格式控制函数setiosflags实现。
//setiosflags函数的调用格式为：
//setiosflags(参数);
//其参数可实现的控制：
    ①对齐方式
    ②输出进制
    ③显示方式 
#include <iostream>
#include <iomanip>
#include <string>
using namespace std;
int main() {
	double values[] = { 1.23, 35.36, 653.7, 4358.24 };
	string names[] = { "Zoot", "Jimmy", "Al", "Stan" };
	for (int i=0;i<4;i++)
		cout << setiosflags(ios_base::left)
			<< setw(6) << names[i]
			<< resetiosflags(ios_base::left)
			<< setw(10) << values[i] << endl;
	return 0;}
```
输出结果:

Zoot     1.23

Jimmy   35.36

Al      653.7

Stan  4358.24
```cpp
//控制输出精度
//输出精度可用预定义格式控制函数   setprecision()来设置,调用格式为：
setprecision(n)； 
#include <iostream>
#include <iomanip>
#include <string>
using namespace std;
int main() {
	double values[] = { 1.23, 35.36, 653.7, 4358.24 };
	string names[] = { "Zoot", "Jimmy", "Al", "Stan" };
	for (int i=0;i<4;i++)
		cout << setiosflags(ios_base::left)
		<< setw(6) << names[i]
		<< resetiosflags(ios_base::left)
		<< setw(10) << setprecision(1) << values[i]<< endl;
		return 0;}
```
输出结果：

Zoot         1

Jimmy   4e+001

Al      7e+002

Stan    4e+003
- 进制
	- 输出进制有两种设置方式：
1. 用setiosflags函数；
2. 用C++预定义的格式控制符dec、oct、hex设置默认输入/输出进制。 
	- 二进制输出文件
		- 字符串输出流
	- 输出流
		- 文件输出流成员函数
	- 输出流成员函数有三种类型：
1. 与操纵符等价的成员函数。
2. 执行非格式化写操作的成员函数。
3. 其它修改流状态且不同于操纵符或插入运算符的成员函数。
	- 文件输出流成员函数
		- open函数
			- 把流与一个特定的磁盘文件关联起来。
			- 需要指定打开模式。
		- put函数
			- 把一个字符写到输出流中。
		- write函数
			- 把内存中的一块内容写到一个文件输出流中
		- seekp和tellp函数
			- 操作文件流的内部指针
		- close函数
			- 关闭与一个文件输出流关联的磁盘文件
		- 错误处理函数
			- 在写到一个流时进行错误处理
```cpp
//使用成员函数open()打开文件
//打开文件的格式为：
//文件流对象.open(“文件名”，ios_base::moda)；
//文件打开方式：moda=in、out、app、nocreate、noreplace、binary。(见p488表11-2)
outfile.open("youfile.txt", ios_base ::out);
       或 outfile.open("youfile.txt");
```
- 判断文件打开成功
  - 无论是调用成员函数open()来打开文件，还是用构造函数来打开文件，在打开后，都要判断打开是否成功。若文件打开成功，则文件流对象值为非零值；若打开不成功，则其值为0。
```cpp
//按只读方式打开文件myfile.txt的一般过程为：
ofstream  outfile("myfile.txt");
if  (!outfile) 
{  
	cout<<"不能打开的文件："<< "myfile.txt“<<endl;
  exit(1); 
}
```
- 判断文件打开成功
```cpp
char filename[256];
cout<<"输入文件名："；
cin>>filename;
ifstream outfile;
outfile.open(filename);
if (!outfile)
{  cout<<"不能打开的文件："<<filename<<endl;
   exit(1);
}
```
```cpp
//向文件输出
#include <fstream>
using namespace std;
struct Date { 	int mondy, day, year;  };
int main() {
	Date dt = { 6, 10, 92 };
	ofstream file("date.dat", ios_base::binary);
	file.write(reinterpret_cast<char *>(&dt), sizeof(dt));
	file.close();
	return 0;}//reinterpret_cast见6.8.2
```
- 二进制输出文件
	- 以通常方式构造一个流，然后使用setmode成员函数，在文件打开后改变模式。
	- 使用ofstream构造函数中的模式参量指定二进制输出模式
		- 字符串输出流ostringstream
用于构造字符串
- 功能
	- 支持ofstream类的除open、close外的所有操作
	- str函数可以返回当前已构造的字符串
- 典型应用
	- 将数值转换为字符串
```cpp
//字符串输出流应用
#include <iostream>
#include <sstream>
#include <string>
using namespace std;
template <class T>
inline string toString(const T &v) {
	ostringstream os;	//创建字符串输出流
	os << v;		//将变量v的值写入字符串流
	return os.str(); }	//返回输出流生成的字符串
int main() {
	string str1 = toString(5);
	cout << str1 << endl;
	string str2 = toString(1.2);
	cout << str2 << endl;
	return 0;}
输出结果：
5
1.2
```
- 构造输入流对象
	- 使用提取运算符
	- 输入流操纵符
	- 输入流相关函数
	- 字符串输入流
- 输入输出流
	- 输入流
- 重要的输入流类：
	- istream类最适合用于顺序文本模式输入。cin是其实例。
	- ifstream类支持磁盘文件输入。
	- istringstream
- 输入流对象
	- 如果在构造函数中指定一个文件名，在构造该对象时该文件便自动打开。
	- ifstream myFile("filename");
	- 在调用默认构造函数之后使用open函数来打开文件。
		- ifstream myFile;//建立一个文件流对象
		- myFile.open("filename",);  //打开文件"filename”
	- 打开文件时可以指定模式
		- ifstream myFile("filename", ios_base::in | ios_base::binary);
		- 提取运算符>>
		提取运算符(>>)对于所有标准C++数据类型都是预先设计好的。	
		- 是从一个输入流对象获取字节最容易的方法。
		- ios类中的很多操纵符都可以应用于输入流。但是只有少数几个对输入流对象具有实际影响，其中最重要的是进制操纵符dec、oct和hex。
			- 输入流成员函数
				- open函数把该流与一个特定磁盘文件相关联。
			- get函数的功能与提取运算符（>>）很相像，主要的不同点是get函数在读入数据时包括空白字符。
```cpp
#include <iostream>
using namespace std;
int main()
     {  char ch;
        while ((ch=cin.get())!=EOF)
         cout.put(ch);}
//getline的功能是从输入流中读取多个字符，并且允许指定输入终止字符，读取完成后，从读取的内容中删除终止字符。
```
```cpp
   #include <iostream>
   using namespace std;
   int main()
      { char line[100]
        cout << "Type a line terminated by 't' " << endl; 
       cin.getline(line,100,'t'); 
       cout << line;}
//read成员函数从一个文件读字节到一个指定的内存区域，由长度参数确定要读的字节数。如果给出长度参数，当遇到文件结束或者在文本模式文件中遇到文件结束标记字符时结束读取。
```
- 输入流成员函数
	- seekg函数用来设置文件输入流中读取数据位置的指针。
	- tellg函数返回当前文件读指针的位置。这个值是streampos类型，该typedef结构定义在iostream．h中。
	- close函数关闭与一个文件输入流关联的磁盘文件。
```cpp
//从文件读二进制记录
#include <iostream>
#include <fstream>
#include <cstring>
using namespace std;
struct SalaryInfo {
	unsigned id;
	double salary;};
int main() {
	SalaryInfo employee1 = { 600001, 8000 };
	ofstream os("payroll", ios_base::out | ios_base::binary);
	os.write(reinterpret_cast<char *>(&employee1), sizeof(employee1));
	os.close();
	ifstream is("payroll", ios_base::in | ios_base::binary);
	if (is) {
		SalaryInfo employee2;
		is.read(reinterpret_cast<char *>(&employee2), 
		sizeof(employee2));
		cout << employee2.id << " " << employee2.salary << endl;	}
 else {
		cout << "ERROR: Cannot open file 'payroll'." << endl;	}
	is.close();	return 0;}
```
```cpp
//设置位置指针
#include <iostream>
#include <fstream>
using namespace std;
int main() {
	int values[] = { 3, 7, 0, 5, 4 };
	ofstream os("integers", ios_base::out | ios_base::binary);
	os.write(reinterpret_cast<char *>(values), sizeof(values));
	os.close();
ifstream is("integers", ios_base::in | ios_base::binary);
	if (is) {
		is.seekg(3 * sizeof(int));
		int v;
		is.read(reinterpret_cast<char *>(&v), sizeof(int));
		cout << "The 4th integer in the file 'integers' is " << v << endl;
	} else
		cout << "ERROR: Cannot open file 'integers'." << endl;	return 0;}
```
```cpp
//读文件并显示其中0元素的位置
#include <iostream>
#include <fstream>
using namespace std;
int main() {
	ifstream file("integers", ios_base::in | ios_base::binary);
	if (file) {
		while (file) {streampos here = file.tellg();
			int v;
			file.read(reinterpret_cast<char *>(&v), sizeof(int));
			if (file && v == 0) 
				cout << "Position " << here << " is 0" << endl;}
	} else {cout << "ERROR: Cannot open file 'integers'." << endl;	}file.close();	return 0;}
```
- 字符串输入流istringstream
	- 用于从字符串读取数据
	- 在构造函数中设置要读取的字符串
- 功能
	- 支持ifstream类的除open、close外的所有操作
- 典型应用
	- 将字符串转换为数值
```cpp
//字符串输入流应用
#include <iostream>
#include <sstream>
#include <string>
using namespace std;
template <class T>
inline T fromString(const string &str)
{
istringstream is(str);	
//创建字符串输入流
T v;
is >> v;		
//从字符串输入流中读取变量v
return v;	}	
	//返回变量v
int main() {
	int v1 = fromString<int>("5");
	cout << v1 << endl;
	double v2 = fromString<double>("1.2");
	cout << v2 << endl;	return 0;}
输出结果：
5
1.2
```
- 深度搜索
	- 宽字符、宽字符串与宽流
	- 普通字符和字符串的缺陷
	- 一个汉字被拆成两个字符
		- 例：string s = “这是一个中文字符串”;
```cpp
s.size()：返回18
s.substr(3,2)：得到的结果是“且”
s.find(“且”)：返回3
```
- 普通字符和字符串的缺陷
	- 一个汉字被拆成两个字符
	- 例：string s = “这是一个中文字符串”;
```cpp
s.size()：返回18
s.substr(3,2)：得到的结果是“且”
s.find(“且”)：返回3
#include<iostream>
#include<string>
using namespace std;
main()
{
string s="这是一个中文字符串";
cout<<s.size()<<endl;
cout<<s.substr(3,2)<<endl;
return 0;
}
```
- 宽字符：wchar_t类型
	- 一般占2个字节，可以直接存下一个汉字
	- 宽字符的文字以“L”开头，比如：wchar_t c = L’人’;
	- 宽字符串：wstring类型
- 与string同源
```cpp
typedef basic_string<char> string;
typedef basic_string<wchar_t> wstring;
wstring s = L"这是一个中文字符串";
s.size()：返回9
```
- 宽流
	- 宽流：以宽字符为基本单位的流
	- wistream、wifstream、wistringstream、wostream、wofstream、wostringstream、wios……wcin、wcout、wcerr、wclog
	- 宽字符和宽字符串需要通过宽流输入输出
- 宽流与普通流一一对应，彼此同源
```cpp
typedef basic_ifstream<char> ifstream;
typedef basic_ifstream<wchar_t> wifstream;
```
- 为宽文件流配置编码方案
	- 文件以字节为单位，编码方案决定了宽字符和字节的对应关系
	- L“ABCD”占4个字节，L“甲乙丙丁”占8个字节，这由编码方案体现
- 配置方法：
	- 用“代码页”编号构造locale对象
	- 执行流的imbue成员函数
```cpp
locale loc(".936"); //创建本地化配置方案对象
wcout.imbue(loc); //设置wcout对象的编码方案
wcout << L"这是一个中文字符串" << endl;	//输出字符串
//宽流的应用
#include <iostream>
#include <string>
#include <fstream>
#include <locale>
using namespace std;
int main() {
	locale loc(".936");	//创建本地化配置方案
	wcout.imbue(loc);	//为wcout设置编码方案
	wifstream in(“article.txt”);//创建文件宽输入流，打开文件
	in.imbue(loc);	//为in设置编码方案
	wstring line;	//用来存储一行内容
	unsigned number = 0;	//记录行号
	while (getline(in, line)) {
		number++;			//行号加1
		if (line.find_first_of(L'人') != wstring::npos)
			wcout << number << L“: ” << line << endl; 
	}
	return 0;
}
```
- 对象的串行化
	- 串行化：将对象写入文件，使得在适当的时候对象能从文件中读出并恢复
	- 直接用write将对象内容输出、用read将对象恢复的问题
	- 对象中存在指针时，指针所指对象内容不会被保存；
	- 对象的成员本身可能是存在指针的对象；
	- 对象不仅是数据的集合，还包括一系列行为，用read只能恢复数据，不能触发相应行为
- 串行化的基本方法
	- 手工串行化的基本方法
- 手工编写save和load函数
	- 按照相同的顺序保存/恢复数据成员碰到指针时，首先保存指针是否为空的标志，如非空，将指针对象的内容保存，load做相反操作
- 完全手工编写串行化函数的困境
	- save和load对成员的操作顺序完全相同，存在逻辑上的重复
	- 处理指针等操作过于繁琐
		- boost::serialization
		- 用Serialization库将下列结构体串行化：
```cpp
struct SalaryInfo {
string name;
double salary;
TaxInfo *tax;
};
```
- 只需增加一个成员函数模板（需要TaxInfo也实现了同样的成员函数模板）：
```cpp
template <class Archive>
void SalaryInfo::serialize(Archive & ar, unsigned int version) {
	ar & name & salary & tax;
}
```
- 理解Serialization
	- serialize函数
		- serialize是模板，串行化和恢复都通过这一段源代码
		- “&”被Serialization重载了，能够处理各种基本数据类型、标准库类型
		- “&”碰到指针时，如果指针的目的类型也有serialize成员函数，则用该函数将指针内容串行化/恢复
	- Serialization的文档类
- 文档类
	- 用于实际执行串行化操作
- 支持5种串行化格式
	- 普通文本：text_oachive/text_iachive
	- 宽文本：text_woachive/text_wiachive
	- 普通字符XML：xml_oachive/xml_iachive
	- 宽字符XML：xml_woachive/xml_wiachive
	- 二进制：binary_oachive/binary_iachive
- 文档类的使用
	- 保存对象：用“<<”
```cpp
ofstream ofs("salary.txt", ios_base::out);
text_oarchive oa(ofs);
oa << s1;
```
- 读取对象：用“>>”
```cpp
ifstream ifs("salary.txt", ios_base::in);
text_iarchive ia(ifs);	
SalaryInfo s2;
ia >> s2;
```
- Serialization的其它功能
	- 可以进行版本控制
	- 全面支持对STL容器的串行化
	- 允许将serialize分开定义为两个不同的模板（save和load）
	- 进行“对象追踪”，如有两个指针指向同一对象，它能保证这个对象只被串行化一次，而且恢复时也只生成一个对象
- 第十二章 异常处理
	- 异常处理的基本思想
		- 调用者->函数$\huge f(\ )$捕获并处理异常->调用关系->函数$\huge g（\ ）$->函数$\huge h（\ ）$引发异常->函数$\huge g（\ ）$->异常传播方向->函数$\huge f（\）$捕获并处理异常->调用者
	- 异常处理的实现机制
		- 抛掷异常的程序段
```cpp
......
throw    表达式;
......
捕获并处理异常的程序段
try
   复合语句
catch（异常类型声明）
    复合语句
catch（异常类型声明）
    复合语句
    …
```
- 若有异常则通过throw操作创建一个异常对象并抛掷。
- 将可能抛出异常的程序段嵌在try块之中。控制通过正常的顺序执行到达try语句，然后执行try块内的保护段。
- 如果在保护段执行期间没有引起异常，那么跟在try块后的catch子句就不执行。程序从try块后跟随的最后一个catch子句后面的语句继续执行下去。
- catch子句按其在try块后出现的顺序被检查。匹配的catch子句将捕获并处理异常（或继续抛掷异常）。
- 如果匹配的catch子句未找到，则运行函数terminate将被自动调用，其缺省功能是调用abort终止程序。
```cpp
//处理除零异常
#include<iostream.h>
int Div(int x,int y);
int main()
{	try
	{ cout<<"5/2="<<Div(5,2)<<endl;
	  cout<<"8/0="<<Div(8,0)<<endl;
	  cout<<"7/1="<<Div(7,1)<<endl;
	}
   catch(int)
	{ cout<<"except of deviding zero.\n"; }
	cout<<"that is ok.\n";
}
int Div(int x,int y)
{	if(y==0) throw y;
	return x/y;
}
程序运行结果如下：
5/2=2
except of deviding zero.
that is ok.
```
- c++异常处理的实现
	- 异常处理的语法
	- 异常接口声明
		- 可以在函数的声明中列出这个函数可能抛掷的所有异常类型。
		- 比如：void fun() throw(A，B，C，D);
		- 若无异常接口声明，则此函数可以抛掷任何类型的异常。
		- 不抛掷任何类型异常的函数声明如下：
			- void fun() throw();
	- 异常处理中的构造与析构
		- 找到一个匹配的catch异常处理后初始化参数。
		- 将从对应的try块开始到异常被抛掷处之间构造（且尚未析构）的所有自动对象进行析构。
		- 从最后一个catch处理之后开始恢复执行。
```cpp
//异常处理时的析构
#include <iostream.h>
void MyFunc( void );
class Expt
{ public:
   Expt(){};
   ~Expt(){};
   const char *ShowReason() const
   {  return "Expt类异常。"; 
	 }
};
class Demo
{ public:
   Demo();
   ~Demo();
};
Demo::Demo( )
{
  cout<<"构造 Demo."<<endl;
}
Demo::~Demo()
{
  cout<<"析构 Demo."<<endl;
}
void MyFunc()
{ Demo D;
  cout<<"在MyFunc()中抛掷Expt类异常。"<<endl;
  throw Expt( );
}
int main()
{ cout<<"在main函数中。"<<endl;
  try
  { cout<<"在try块中，调用MyFunc()。" <<endl;
    MyFunc( );
  }
  catch( Expt E )
  { cout<<"在catch异常处理程序中。"<<endl;
    cout<<"捕获到Expt类型异常：";
    cout<<E.ShowReason()<<endl;
  }
  catch( char *str )
  { cout<<"捕获到其他的异常："<<str<<endl;}
  cout<<"回到main函数。从这里恢复执行。" 
      <<endl;
  return 0;
}
程序运行时输出:
在main函数中。
在try块中，调用MyFunc()。
构造 Demo.
在MyFunc()中抛掷Expt类异常。
析构 Demo.
在catch异常处理程序中。
捕获到Expt类型异常：Expt类异常。
回到main函数。从这里恢复执行。
```
- 标准程序库异常处理
-  深度探索
	- 异常安全性问题
	- 避免异常发生时的资源泄露 
- MFC库与Windows程序开发概述
	- Windows程序的基本结构
		- 开始执行--初始化应用--初始化和创建应用窗口--进入消息循环并从消息队列得到一个消息--当前消息是否退出--是--终止执行--否--程序是否定义了对此消息的处理--否--进行默认处理--是--处理消息
	- WinMain()函数
		- 初始化应用
		- 初始化和创建应用窗口
		- 进入应用程序的消息循环
	- 窗口过程WndProc()
		- 执行窗口的消息处理：
			- 分析消息信息，决定应用程序如何处理消息或响应一个事件。
	- MFC库简介
		- 类库是一个可以在应用程序中使用的相互关联的类的集合。
	- MFC库——Microsoft 基本类库是一个Windows应用程序框架，它定义了应用程序的结构，并实现了标准的用户接口：
		- 管理窗口、菜单、对话框，实现基本的输入/输出和数据存储。
	- 应用程序框架
		- 应用程序框架是一种类库的超集
		- 在程序运行时，流程的控制多数是由框架实现的。
		- 应用MFC框架来构造应用程序时，程序员的角色就是提供应用程序专用的代码，并指定这些代码是用来响应哪些消息和命令的，以使框架能够在消息和代码间建立联系。
	- "文档—视图"结构
		- 应用程序框架的核心是"文档—视图"结构。MFC通过"文档—视图"结构为应用程序提供一种将数据与视图相分离的存储方式。
		- 文档类的作用是将应程序的数据保存在文档类对象中，以及从磁盘文件中读或向磁盘文件中写数据。
视图类的作用是显示数据和编辑数据。
- 使用Visual C++开发Windows程序
	- 建立一个应用程序框架
	- 观察自动生成的应用程序
	- 构造应用程序的用户接口
	- 将菜单映射到消息处理函数
	- 将工具栏按钮映射到命令
	- 测试自己编写的消息处理函数
	- 增加对话框
	- 初始化、验证和提取对话框中的数据
	- 创建新增的类
	- 添加现成的组件到应用程序中
	- 实现自己的文档类
	- 实现Open、Save和Save As命令
	- 实现视图类
	- 改进缺省的打印
	- 增加屏幕滚动
	- 创建表单视图
	- 创建数据库表单
	- 构造（Build）、测试和调试应用程序











































































