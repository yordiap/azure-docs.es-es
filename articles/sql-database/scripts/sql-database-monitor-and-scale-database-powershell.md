---
title: "Script de Azure PowerShell: supervisión y escalado de una instancia única de SQL Database | Microsoft Docs"
description: "Ejemplo de script de Azure PowerShell: supervisión y escalado de una instancia única de SQL Database mediante PowerShell"
services: sql-database
documentationcenter: sql-database
author: janeng
manager: jstrauss
editor: carlrab
tags: azure-service-management
ms.assetid: 
ms.service: sql-database
ms.custom: mvc
ms.devlang: PowerShell
ms.topic: sample
ms.tgt_pltfrm: sql-database
ms.workload: database
ms.date: 05/23/2017
ms.author: janeng
ms.translationtype: Human Translation
ms.sourcegitcommit: 67ee6932f417194d6d9ee1e18bb716f02cf7605d
ms.openlocfilehash: fab0994ff9ec4471e0a6814e681b2d3e36433301
ms.contentlocale: es-es
ms.lasthandoff: 05/26/2017

---

# <a name="monitor-and-scale-a-single-sql-database-using-powershell"></a>Supervisión y escalado de una instancia única de SQL Database mediante PowerShell

Este script de PowerShell de ejemplo supervisa las métricas de rendimiento de una base de datos, la escala a un nivel de rendimiento superior y crea una regla de alerta en una de las métricas de rendimiento. 

[!INCLUDE [sample-powershell-install](../../../includes/sample-powershell-install-no-ssh.md)]

## <a name="sample-script"></a>Script de ejemplo

[!code-powershell[main](../../../powershell_scripts/sql-database/monitor-and-scale-database/monitor-and-scale-database.ps1?highlight=13-14 "Supervisión y escalado de una instancia única de SQL Database")]

## <a name="clean-up-deployment"></a>Limpieza de la implementación

Después de ejecutar el script de ejemplo, se puede usar el comando siguiente para quitar el grupo de recursos y todos los recursos asociados.

```powershell
Remove-AzureRmResourceGroup -ResourceGroupName "myResourceGroup"
```

## <a name="script-explanation"></a>Explicación del script

Este script usa los siguientes comandos. Cada comando de la tabla crea un vínculo a documentación específica del comando.

| Comando | Notas |
|---|---|
 [New-AzureRmResourceGroup](/powershell/module/azurerm.resources/new-azurermresourcegroup) | Crea un grupo de recursos en el que se almacenan todos los recursos. |
| [New-AzureRmSqlServer](/powershell/module/azurerm.sql/new-azurermsqlserver) | Crea un servidor lógico que hospeda una base de datos o un grupo elástico. |
| [Get-AzureRmMetric](/powershell/module/azurerm.insights/get-azurermmetric) | Muestra la información de uso del tamaño de la base de datos.|
| [Set-AzureRmSqlDatabase](/powershell/module/azurerm.sql/set-azurermsqldatabase) | Actualiza las propiedades de la base de datos o traslada una base de datos a un grupo elástico, fuera de este o entre grupos elásticos. |
| [Add-AzureRMMetricAlertRule](/powershell/module/azurerm.insights/add-azurermmetricalertrule) | Establece una regla de alerta para supervisar automáticamente las DTU en el futuro. |
| [Remove-AzureRmResourceGroup](/powershell/module/azurerm.resources/remove-azurermresourcegroup) | Elimina un grupo de recursos, incluidos todos los recursos anidados. |
|||

## <a name="next-steps"></a>Pasos siguientes

Para más información sobre Azure PowerShell, consulte la [documentación de Azure PowerShell](/powershell/azure/overview).

Encontrará más ejemplos de scripts de PowerShell de SQL Database en los [scripts de PowerShell de Azure SQL Database](../sql-database-powershell-samples.md).

