---
title: 如何：使用 ChannelFactory
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d48f01b5-582b-4c8b-b547-8adddae7e371
ms.openlocfilehash: 7d542a3dcae514e75194b49c23a8dec5dd7e8c3b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2019
ms.locfileid: "62047251"
---
# <a name="how-to-use-the-channelfactory"></a>如何：使用 ChannelFactory
<xref:System.ServiceModel.ChannelFactory%601> 泛型类用于某些高级方案中，这些方案要求创建可用于创建多个通道的通道工厂。  
  
### <a name="to-create-and-use-the-channelfactory-class"></a>创建和使用 ChannelFactory 类  
  
1. 生成并运行 Windows Communication Foundation (WCF) 服务。 有关详细信息，请参阅[设计和实现服务](../../../../docs/framework/wcf/designing-and-implementing-services.md)，[配置服务](../../../../docs/framework/wcf/configuring-services.md)，并[托管服务](../../../../docs/framework/wcf/hosting-services.md)。  
  
2. 使用[ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)来生成客户端协定 （接口）。  
  
3. 在客户端代码中，使用 <xref:System.ServiceModel.ChannelFactory%601> 类创建多个终结点侦听器。  
  
## <a name="example"></a>示例  
 [!code-csharp[c_HowToUseChannelFactory#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howtousechannelfactory/cs/source.cs#1)]
 [!code-vb[c_HowToUseChannelFactory#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howtousechannelfactory/vb/source.vb#1)]
