---
title: 如何：在代码中指定客户端绑定
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 6bee5da4-adf7-42e6-8f78-63a9e5c6dbad
ms.openlocfilehash: 9be571d7be020aef546fdd7ec7cb7519a48ea350
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2020
ms.locfileid: "79184054"
---
# <a name="how-to-specify-a-client-binding-in-code"></a>如何：在代码中指定客户端绑定
在本示例中，创建了一个使用计算器服务的客户端，并在代码中以强制方式指定该客户端的绑定。 该客户端访问实现了 `CalculatorService` 接口的 `ICalculator`，并且服务和客户端都使用 <xref:System.ServiceModel.BasicHttpBinding> 类。  
  
 此过程假设计算器服务正在运行。 有关构建服务的信息，请参阅[如何：在 配置 中指定服务绑定](how-to-specify-a-service-binding-in-configuration.md)。 它还使用[服务模型元数据实用程序工具 （Svcutil.exe）](servicemodel-metadata-utility-tool-svcutil-exe.md)Windows 通信基础 （WCF） 提供自动生成客户端组件。 该工具生成用于访问服务的客户端代码。  
  
 客户端分两部分生成。 Svcutil.exe 生成实现 `ClientCalculator` 接口的 `ICalculator`。 然后，通过构造 `ClientCalculator` 的一个实例，并在代码中指定服务的绑定和地址，构造此客户端应用程序。  
  
 有关此示例的源副本，请参阅[基本绑定](./samples/basicbinding.md)示例。  
  
### <a name="to-specify-a-custom-binding-in-code"></a>在代码中指定自定义绑定  
  
1. 在命令行中，使用 Svcutil.exe 根据服务元数据生成代码。  
  
    ```console  
    Svcutil.exe <service's Metadata Exchange (MEX) address or HTTP GET address>
    ```  
  
2. 生成的客户端包含 `ICalculator` 接口，该接口定义了客户端实现必须满足的服务协定。  
  
     [!code-csharp[C_HowTo_CodeClientBinding#1](../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeclientbinding/cs/client.cs#1)]
     [!code-vb[C_HowTo_CodeClientBinding#1](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeclientbinding/vb/client.vb#1)]  
  
3. 生成的客户端还包含 `ClientCalculator` 的实现。  
  
     [!code-csharp[C_HowTo_CodeClientBinding#2](../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeclientbinding/cs/client.cs#2)]
     [!code-vb[C_HowTo_CodeClientBinding#2](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeclientbinding/vb/client.vb#2)]  
  
4. 创建 `ClientCalculator` 的一个实例（该实例在客户端应用程序中使用 <xref:System.ServiceModel.BasicHttpBinding> 类），然后调用指定地址上的服务操作。  
  
     [!code-csharp[C_HowTo_CodeClientBinding#3](../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_codeclientbinding/cs/client.cs#3)]
     [!code-vb[C_HowTo_CodeClientBinding#3](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_codeclientbinding/vb/client.vb#3)]  
  
5. 编译并运行客户端。  
  
## <a name="see-also"></a>另请参阅

- [使用绑定配置服务和客户端](using-bindings-to-configure-services-and-clients.md)
