---
title: "Cambio del nombre o el logotipo de una aplicación empresarial en la versión preliminar de Azure Active Directory | Microsoft Docs"
description: "Cómo cambiar el nombre o el logotipo de una aplicación empresarial personalizada en Azure Active Directory"
services: active-directory
documentationcenter: 
author: curtand
manager: femila
editor: 
ms.assetid: d01303ce-e6cb-4f3b-a4d6-ec29dfd68146
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 02/13/2017
ms.author: curtand
translationtype: Human Translation
ms.sourcegitcommit: 2ea002938d69ad34aff421fa0eb753e449724a8f
ms.openlocfilehash: 541efc3bdc192d21fd75aa4de9d902adb70b6407


---
# <a name="change-the-name-or-logo-of-an-enterprise-app-in-azure-active-directory-preview"></a>Cambio del nombre o el logotipo de una aplicación empresarial en la versión preliminar de Azure Active Directory
Cambiar el nombre o el logotipo de una aplicación empresarial personalizada en la versión preliminar de Azure Active Directory (Azure AD) es fácil. [¿Qué es la versión preliminar?](active-directory-preview-explainer.md)  Debe tener los permisos adecuados para realizar estos cambios. En la versión preliminar actual, debe ser el creador de la aplicación personalizada.

## <a name="how-do-i-change-an-enterprise-apps-name-or-logo"></a>¿Cómo puedo cambiar el nombre o el logotipo de una aplicación empresarial?
1. Inicie sesión en [Azure Portal](https://portal.azure.com) con una cuenta que tenga el rol de administrador global en el directorio.
2. Seleccione **Más servicios**, escriba **Azure Active Directory** en el cuadro de texto y presione **ENTRAR**.
3. En la hoja **Azure Active Directory - *nombreDelDirectorio*** (es decir, la hoja de Azure AD del directorio que está administrando), seleccione **Aplicaciones empresariales**.

    ![Apertura de Enterprise apps (Aplicaciones empresariales)](./media/active-directory-coreapps-change-app-logo-azure-portal/open-enterprise-apps.png)
4. En la hoja **Aplicaciones empresariales**, seleccione **Todas las aplicaciones**. Verá una lista de las aplicaciones que puede administrar.
5. En la hoja **Enterprise applications (Aplicaciones empresariales) - Todas las aplicaciones** , seleccione una aplicación.
6. En la hoja ***nombreDeLaAplicación*** (es decir, la hoja con el nombre de la aplicación seleccionada en el título), seleccione **Propiedades**.

    ![Selección del comando Propiedades](./media/active-directory-coreapps-change-app-logo-azure-portal/select-app.png)
7. En la hoja ***nombreDeAplicación*** **- Propiedades**, busque el archivo que desea usar como nuevo logotipo o edite el nombre de la aplicación, o ambas opciones.

    ![Cambio del logotipo o de la aplicación o comando de propiedades de nombre](./media/active-directory-coreapps-change-app-logo-azure-portal/change-logo.png)
8. Haga clic en el comando **Guardar** .

## <a name="next-steps"></a>Pasos siguientes
* [Ver todos mis grupos](active-directory-groups-view-azure-portal.md)
* [Asignar un usuario o grupo a una aplicación empresarial](active-directory-coreapps-assign-user-azure-portal.md)
* [Eliminación de asignaciones de usuario o grupo de una aplicación empresarial](active-directory-coreapps-remove-assignment-azure-portal.md)
* [Deshabilitar los inicios de sesión de los usuarios de una aplicación empresarial](active-directory-coreapps-disable-app-azure-portal.md)



<!--HONumber=Nov16_HO3-->


