---
title: do（C# 参考）
ms.date: 05/28/2018
f1_keywords:
- do_CSharpKeyword
- do
helpviewer_keywords:
- do keyword [C#]
ms.assetid: 50725f79-9ba6-4898-aa78-6e331568a1bb
ms.openlocfilehash: 89c13f5b547c13052e229ff6eb3a39ae5babce41
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "45994463"
---
# <a name="do-c-reference"></a>do（C# 参考）

在指定的布尔表达式的计算结果为 `true` 时，`do` 语句会执行一条语句或一个语句块。 由于在每次执行循环之后都会计算此表达式，所以 `do-while` 循环会执行一次或多次。 这不同于 [while](while.md) 循环（该循环执行零次或多次）。

在 `do` 语句块中的任何点，都可使用 [break](break.md) 语句中断循环。

可通过使用 [continue](continue.md) 语句直接步入 `while` 表达式的计算部分。 如果表达式计算结果为 `true`，则继续执行循环中的第一个语句。 否则，将在循环后的第一个语句处继续执行。

还可以使用 [goto](goto.md)、[return](return.md) 或 [throw](throw.md) 语句退出 `do-while` 循环。

## <a name="example"></a>示例

下面的示例演示 `do` 语句的用法。 选择“运行”以运行示例代码。 然后可以修改代码并再次运行它。

[!code-csharp-interactive[do loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#4)]

## <a name="c-language-specification"></a>C# 语言规范

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>请参阅

- [C# 参考](../index.md)  
- [C# 编程指南](../../programming-guide/index.md)  
- [C# 关键字](index.md)  
- [do-while 语句 (C++)](/cpp/cpp/do-while-statement-cpp)  
- [迭代语句](iteration-statements.md)  
- [while 语句](while.md)  
