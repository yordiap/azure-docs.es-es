---
title: "Administración de unidades administrativas en Azure Active Directory"
description: "Uso de unidades administrativas para una delegación más detallada de permisos en Azure Active Directory"
services: active-directory
documentationcenter: 
author: curtand
manager: femila
editor: 
ms.assetid: 8464cd6b-1d1a-470d-a4fb-ee29b8eab4c4
ms.service: active-directory
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 05/04/2017
ms.author: curtand
ms.translationtype: Human Translation
ms.sourcegitcommit: e72275ffc91559a30720a2b125fbd3d7703484f0
ms.openlocfilehash: d05b4a34c5271b636400ed90ead76fabf0d911bd
ms.contentlocale: es-es
ms.lasthandoff: 05/05/2017


---
# <a name="administrative-units-management-in-azure-ad---public-preview"></a>Administración de unidades administrativas en Azure AD: vista previa pública
En este artículo se describen las unidades administrativas, un nuevo contenedor de recursos de Azure Active Directory que se puede usar para delegar permisos administrativos en subconjuntos de usuarios y aplicar directivas a un subconjunto de usuarios. En Azure Active Directory, las unidades administrativas habilitan a los administradores centrales para delegar permisos a administradores regionales o para establecer directivas en un nivel detallado.

Esto es útil en organizaciones con divisiones independientes, por ejemplo, una universidad grande que se compone de varias escuelas autónomas (escuela de negocios, escuela de ingenieros, etc.) que son independientes entre ellas. Estas divisiones tienen sus propios administradores de TI que controlan el acceso, administran usuarios y establecen directivas específicamente para su división. Los administradores centrales desean poder otorgar a estos administradores de divisiones para los usuarios en sus divisiones determinadas. Más específicamente, con este ejemplo, un administrador central puede, por ejemplo, crear una unidad administrativa para una determinada escuela (escuela de negocios) y rellenarla solo con usuarios de la escuela de negocios. Luego, un administrador central puede agregar al personal de TI de la escuela de negocios a un rol de ámbito, en otras palabras, conceder al personal de TI permisos administrativos de la escuela de negocios sobre la unidad administrativa de la misma escuela.

> [!IMPORTANT]
> Puede crear y usar unidades administrativas solo si habilita Azure Active Directory Premium. Para obtener más información, consulte [Introducción a Azure AD Premium](active-directory-get-started-premium.md).
>
>

Desde el punto de vista del administrador central, una unidad administrativa es un objeto de directorio que se puede crear y rellenar con recursos. **En esta versión preliminar, estos recursos solo pueden ser usuarios.** Una vez creada y rellenada, la unidad administrativa puede usarse como ámbito para restringir el permiso otorgado para los recursos que contiene la unidad administrativa.

## <a name="managing-administrative-units"></a>Administración de unidades administrativas
En esta versión de vista previa, puede crear y administrar unidades administrativas con los cmdlets del módulo de Azure Active Directory para Windows PowerShell.

Para obtener más información sobre los requisitos de software y la instalación del módulo de Azure AD, además de información sobre los cmdlets del módulo de Azure AD para administrar las unidades administrativas, incluida sintaxis, descripciones de parámetros y ejemplos, consulte [Administración de Azure AD mediante Windows PowerShell](https://msdn.microsoft.com/library/azure/jj151815.aspx).

## <a name="next-steps"></a>Pasos siguientes
[Ediciones de Azure Active Directory](active-directory-editions.md)

