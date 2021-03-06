---
title: Informe de acceso - RBAC de Azure | Microsoft Docs
description: "Utilice Control de acceso basado en rol para generar un informe con todos los cambios en el acceso a las suscripciones de Azure en los últimos 90 días."
services: active-directory
documentationcenter: 
author: kgremban
manager: femila
editor: 
ms.assetid: 2bc68595-145e-4de3-8b71-3a21890d13d9
ms.service: active-directory
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 02/27/2017
ms.author: kgremban
ms.custom: H1Hack27Feb2017
translationtype: Human Translation
ms.sourcegitcommit: 015cc28903bfd366c653a51b0f73512bf8b578ea
ms.openlocfilehash: 433dc731c342924d962e2f08e392556558a0168d
ms.lasthandoff: 02/28/2017

---
# <a name="create-an-access-report-for-role-based-access-control"></a>Creación de un informe de acceso para el control de acceso basado en roles
Cada vez que alguien concede o revoca el acceso dentro de sus suscripciones, los cambios se registran en los eventos de Azure. Puede crear informes de historial de cambios de acceso para ver todos los cambios de los últimos 90 días.

## <a name="create-a-report-with-azure-powershell"></a>Creación de un informe con Azure PowerShell
Para crear un informe de historial de cambios de acceso en PowerShell, utilice el siguiente comando `Get-AzureRMAuthorizationChangeLog` . Puede encontrar más información sobre este cmdlet en la [galería de PowerShell](https://www.powershellgallery.com/packages/AzureRM.Storage/1.0.6/Content/ResourceManagerStartup.ps1).

Al llamar a este comando, puede especificar qué propiedad de las asignaciones desea mostrar, incluidas las siguientes:

| Propiedad | Description |
| --- | --- |
| **Acción** |Si se ha concedido o revocado el acceso. |
| **Autor de llamada** |El propietario responsable del cambio de acceso. |
| **Date** |La fecha y la hora en que se modificó el acceso. |
| **DirectoryName** |El directorio de Azure Active Directory. |
| **PrincipalName** |El nombre del usuario, el grupo o la aplicación. |
| **PrincipalType** |Si la asignación ha sido para un usuario, un grupo o una aplicación. |
| **RoleId** |El GUID del rol que se ha concedido o revocado. |
| **RoleName** |El rol que se ha concedido o revocado. |
| **ScopeName** |El nombre de la suscripción, el grupo de recursos o el recurso. |
| **ScopeType** |Si la asignación era en el ámbito de la suscripción, el grupo de recursos o el recurso. |
| **SubscriptionId** |El GUID de la suscripción de Azure. |
| **SubscriptionName** |El nombre de la suscripción de Azure. |

En el siguiente comando de ejemplo se muestran todos los cambios de acceso de la suscripción que tuvieron lugar en los últimos&7; días:

```
Get-AzureRMAuthorizationChangeLog -StartTime ([DateTime]::Now - [TimeSpan]::FromDays(7)) | FT Caller,Action,RoleName,PrincipalType,PrincipalName,ScopeType,ScopeName
```

![PowerShell Get:AzureRMAuthorizationChangeLog (captura de pantalla)](./media/role-based-access-control-configure/access-change-history.png)

## <a name="create-a-report-with-azure-cli"></a>Creación de un informe con la CLI de Azure
Para crear un informe de historial de cambios de acceso en la interfaz de la línea de comandos (CLI) de Azure, use el comando siguiente `azure role assignment changelog list` .

## <a name="export-to-a-spreadsheet"></a>Exportación a una hoja de cálculo
Para guardar el informe o manipular los datos, exporte los cambios de acceso a un archivo .csv. Así podrá ver el informe en una hoja de cálculo para revisarlo.

![Changelog visto como una hoja de cálculo ( captura de pantalla)](./media/role-based-access-control-configure/change-history-spreadsheet.png)

## <a name="next-steps"></a>Pasos siguientes
* Uso de [roles personalizados en RBAC de Azure](role-based-access-control-custom-roles.md)
* Información sobre cómo administrar [RBAC de Azure con PowerShell](role-based-access-control-manage-access-powershell.md)


