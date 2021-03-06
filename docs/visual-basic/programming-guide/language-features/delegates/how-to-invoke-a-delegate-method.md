---
title: 如何：调用委托方法
ms.date: 07/20/2015
ms.assetid: b56866ae-abf9-4a5a-a855-486359455e9c
ms.openlocfilehash: 520bacfbe6103490e0459cd5af149c1d55a8fce4
ms.sourcegitcommit: 17ee6605e01ef32506f8fdc686954244ba6911de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2019
ms.locfileid: "74345256"
---
# <a name="how-to-invoke-a-delegate-method-visual-basic"></a>如何：调用委托方法 (Visual Basic)

此示例演示如何将方法与委托相关联，然后通过委托调用该方法。

### <a name="create-the-delegate-and-matching-procedures"></a>创建委托和匹配过程

1. 创建一个名为 `MySubDelegate`的委托。

    ```vb
    Delegate Sub MySubDelegate(ByVal x As Integer)
    ```

2. 声明一个类，该类包含具有与委托相同的签名的方法。

    ```vb
    Class class1
        Sub Sub1(ByVal x As Integer)
            MsgBox("The value of x is: " & CStr(x))
        End Sub
    End Class
    ```

3. 定义一个方法，该方法通过调用内置 `Invoke` 方法来创建委托的实例并调用与该委托相关联的方法。

    ```vb
    Protected Sub DelegateTest()
        Dim c1 As New class1
        ' Create an instance of the delegate.
        Dim msd As MySubDelegate = AddressOf c1.Sub1
        ' Call the method.
        msd.Invoke(10)
    End Sub
    ```

## <a name="see-also"></a>另请参阅

- [Delegate 语句](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [委托](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [事件](../../../../visual-basic/programming-guide/language-features/events/index.md)
- [多线程应用程序](../../../../standard/threading/using-threads-and-threading.md)
