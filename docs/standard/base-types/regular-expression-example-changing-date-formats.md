---
title: 正则表达式示例：更改日期格式
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- searching with regular expressions, examples
- parsing text with regular expressions, examples
- regular expressions, examples
- .NET Framework regular expressions, examples
- regular expressions [.NET Framework], examples
- pattern-matching with regular expressions, examples
ms.assetid: 5fcc75a5-09d7-45ae-a4c0-9ad6085ac83d
ms.openlocfilehash: 358e26957747073fec9dfe9eb0d404cb438afaf9
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/15/2020
ms.locfileid: "73084180"
---
# <a name="regular-expression-example-changing-date-formats"></a>正则表达式示例：更改日期格式
下面的代码示例使用 <xref:System.Text.RegularExpressions.Regex.Replace%2A?displayProperty=nameWithType> 方法，将格式为 mm  /dd  /yy  的日期替换为格式为 dd  -mm  -yy  的日期。  
  
## <a name="example"></a>示例  
 [!code-csharp[RegularExpressions.Examples.ChangeDateFormats#1](../../../samples/snippets/csharp/VS_Snippets_CLR/RegularExpressions.Examples.ChangeDateFormats/cs/Example_ChangeDateFormats1.cs#1)]
 [!code-vb[RegularExpressions.Examples.ChangeDateFormats#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/RegularExpressions.Examples.ChangeDateFormats/vb/Example_ChangeDateFormats1.vb#1)]  
  
 下面的代码演示如何在应用程序中调用 `MDYToDMY` 方法。  
  
 [!code-csharp[RegularExpressions.Examples.ChangeDateFormats#2](../../../samples/snippets/csharp/VS_Snippets_CLR/RegularExpressions.Examples.ChangeDateFormats/cs/Example_ChangeDateFormats1.cs#2)]
 [!code-vb[RegularExpressions.Examples.ChangeDateFormats#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/RegularExpressions.Examples.ChangeDateFormats/vb/Example_ChangeDateFormats1.vb#2)]  
  
## <a name="comments"></a>注释  
 正则表达式模式 `\b(?<month>\d{1,2})/(?<day>\d{1,2})/(?<year>\d{2,4})\b` 的释义如下表所示。  
  
|模式|说明|  
|-------------|-----------------|  
|`\b`|在单词边界处开始匹配。|  
|`(?<month>\d{1,2})`|匹配一个或两个十进制数字。 这是 `month` 捕获的组。|  
|`/`|匹配斜杠标记。|  
|`(?<day>\d{1,2})`|匹配一个或两个十进制数字。 这是 `day` 捕获的组。|  
|`/`|匹配斜杠标记。|  
|`(?<year>\d{2,4})`|匹配两个到四个十进制数。 这是 `year` 捕获的组。|  
|`\b`|在单词边界处结束匹配。|  
  
 模式 `${day}-${month}-${year}` 如下表所示定义替换字符串。  
  
|模式|说明|  
|-------------|-----------------|  
|`$(day)`|添加由 `day` 捕获组捕获的字符串。|  
|`-`|添加连字符。|  
|`$(month)`|添加由 `month` 捕获组捕获的字符串。|  
|`-`|添加连字符。|  
|`$(year)`|添加由 `year` 捕获组捕获的字符串。|  
  
## <a name="see-also"></a>另请参阅

- [.NET 正则表达式](../../../docs/standard/base-types/regular-expressions.md)
