---
title: dotnet tool run 命令
description: dotnet tool run 命令调用本地工具。
ms.date: 02/14/2020
ms.openlocfilehash: a088cd0b7f4bba014234a8189a42a63aa6d88f4e
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/14/2020
ms.locfileid: "78847841"
---
# <a name="dotnet-tool-run"></a>dotnet tool run

 本文适用于： ✔️ .NET Core 3.0 SDK 及更高版本

## <a name="name"></a>“属性”

`dotnet tool run` -调用本地工具。

## <a name="synopsis"></a>摘要

```dotnetcli
dotnet tool run <COMMAND NAME>

dotnet tool run <-h|--help>
```

## <a name="description"></a>描述

`dotnet tool run` 命令将搜索当前目录范围内的工具清单文件。 当找到对指定工具的引用时，它会运行该工具。 有关详细信息，请参阅 [调用本地工具](global-tools.md#invoke-a-local-tool)。

## <a name="arguments"></a>自变量

- **`COMMAND_NAME`**

  要运行的工具的命令名称。

## <a name="options"></a>选项

- **`-h|--help`**

  打印出有关命令的简短帮助。

## <a name="example"></a>示例

- **`dotnet tool run dotnetsay`**

  运行 `dotnetsay` 本地工具。

## <a name="see-also"></a>请参阅

- [.NET Core 工具](global-tools.md)
- [教程：使用 .NET Core CLI 安装和使用 .NET Core 本地工具](local-tools-how-to-use.md)
