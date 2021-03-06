# compilers-principles

[1、引论](#1)

[2、一个简单的语法制导翻译器](#2)

<h2 id=1>引论</h2>

- 语言处理器：一个集成的软件开发环境，其中包含很多种语言的处理器，比如编译器、解释器、汇编器、连接器、加成器、调试器以及程序概要提取工具。
- 编译器的步骤：一个编译器的运作需要一系列的步骤，每个步骤把源程序从一个中间表示转换为另一个中间表示。
- 编译器步骤过程：字符流--入》词法分析器--出》符号流--入》语法分析--出》语法树--入》语义分析--出》语法树--入》中间代码生成器--出》中间表现形式--入》机器无关代码优化器--出》中间表现形式--入》代码生成器--出》目标机器语言--入》机器相关代码优化器--出》目标机器语言
- 机器语言和汇编语言：机器语言是第一代程序设计语言，然后是汇编语言。使用这些语言进行编程即耗时，又容易出错。
- 编译器设计中的建模：编译器设计是理论对实践有很大影响的领域之一。已知在编译器设计中有用的模型包括自动机、文法、正则表达式、树形结构和很多其他理论概念。
- 代码优化：提高代码效率的科学既复杂又非常重要，是编译技术研究的重要一部分，优化后的代码更能达到预期效果。
- 高级语言：具有内存管理、类型一致性检查或代码并发执行等功能，且更已阅读及更高效率，是比汇编语言更进一步的语言。
- 编译器何计算机体系结构：编译器技术影响了计算机的体系结构，同时也受体系结构的影响。因为体系机构的很多现代创新依赖于编译其能够从源程序中抽取有效利用硬件能力的机会。
- 软件生产率和软件安全性：使得编译器能够优化代码的技术同时能够用于多种不同的程序分析任务。这些任务既包括探测常见的程序错误，也包括发现程序已知可能收到黑客们入侵方式之一的伤害。
- 作用域规则：一个x声明的作用域是一段上下文，在此上下文中对x的的使用指向了这个声明。如果仅仅是阅读某个语言的程序就可以确定其作用，那么这个原因呢就使用的静态作用域，或者说词法作用域，否则就是动态作用域了。
- 环境：名字和内存位置关联，然后在和值相关联。这种情形可以使用环境和状态来描述。环境是名字映射到存储位置，而状态是把位置映射到他的值。其中名字为左值，所二次映射的值叫做右值。
- 块结构：允许语句块互相嵌套的语言称为块结构语言。假如一个x的声明D，而嵌套于这个块B中有一个对名字x的使用。如果着两个块之间没有声明x的块，则x使用位于D的作用域内。
- 参数传递：参数可以通过值传递或引用传递。
- 别名：当参数是引用传递时，这两个参数会指向同一个对象，一个对象有不同的名字同时指向这个对象。

<h2 id=2>一个简单的语法制导翻译器</h2>



