---
title: "Tutorial: Integración de Azure Active Directory con Condeco | Microsoft Docs"
description: "Aprenda a configurar el inicio de sesión único entre Azure Active Directory y Condeco."
services: active-directory
documentationcenter: 
author: jeevansd
manager: femila
editor: 
ms.assetid: 4601c17d-ad93-4865-8885-b378c4bbe82b
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 02/24/2017
ms.author: jeedes
translationtype: Human Translation
ms.sourcegitcommit: 4a07f946d396a9263d5b00202cd5229ddc86d1be
ms.openlocfilehash: 1990fa17ce06ac3581d7401249a0240cc72b1229
ms.lasthandoff: 03/01/2017


---
# <a name="tutorial-azure-active-directory-integration-with-condeco"></a>Tutorial: Integración de Azure Active Directory con Condeco
El objetivo de este tutorial es mostrar cómo integrar Condeco con Azure Active Directory (Azure AD).

Integrar Condeco con Azure AD proporciona las siguientes ventajas:

* Puede controlar en Azure AD quién tiene acceso a Condeco.
* Puede permitir que los usuarios inicien sesión automáticamente en Condeco (inicio de sesión único) con sus cuentas de Azure AD.
* Puede administrar sus cuentas en una ubicación central, Azure Active Directory. 
* 
Si desea obtener más información sobre la integración de aplicaciones SaaS con Azure AD, vea [Qué es el acceso a las aplicaciones y el inicio de sesión único en Azure Active Directory](active-directory-appssoaccess-whatis.md).

## <a name="prerequisites"></a>Requisitos previos
Para configurar la integración de Azure AD con Condeco, necesita los siguientes elementos:

* Una suscripción de Azure AD
* Una suscripción habilitada para el inicio de sesión único en Condeco

>[!NOTE]
>Para probar los pasos de este tutorial, no se recomienda el uso de un entorno de producción. 
> 

Para probar los pasos de este tutorial, debe seguir estas recomendaciones:

* No debe usar el entorno de producción, a menos que sea necesario.
* Si no dispone de un entorno de prueba de Azure AD, puede [obtener una versión de prueba durante un mes](https://azure.microsoft.com/pricing/free-trial/).

## <a name="scenario-description"></a>Descripción del escenario
El objetivo de este tutorial es permitirle probar el inicio de sesión único de Azure AD en un entorno de prueba.  

La situación descrita en este tutorial consta de dos bloques de creación principales:

1. Adición de Condeco desde la galería
2. Configuración y comprobación del inicio de sesión único de Azure AD

## <a name="add-condeco-from-the-gallery"></a>Adición de Condeco desde la galería
Para configurar la integración de Condeco en Azure AD, deberá agregar Condeco desde la galería a la lista de aplicaciones SaaS administradas.

**Para agregar Condeco desde la galería, realice los pasos siguientes:**

1. En el **Portal de Azure clásico**, en el panel de navegación izquierdo, haga clic en **Active Directory**. 
   
    ![Active Directory][1]
2. En la lista **Directory** , seleccione el directorio cuya integración desee habilitar.
3. Para abrir la vista de aplicaciones, haga clic en **Applications** , en el menú superior de la vista de directorios.
   
    ![Applications][2]
4. Haga clic en **Agregar** en la parte inferior de la página.
   
    ![Aplicaciones][3]
5. En el cuadro de diálogo **¿Qué desea hacer?**, haga clic en **Agregar una aplicación de la galería**.
   
    ![Aplicaciones][4]
6. En el cuadro de búsqueda, escriba **Condeco**.
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/tutorial_condeco_01.png)
7. En el panel de resultados, seleccione **Condeco** y haga clic en **Completar** para agregar la aplicación.
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/tutorial_condeco_02.png)

## <a name="configure-and-test-azure-ad-sso"></a>Configuración y comprobación del inicio de sesión único de Azure AD
El objetivo de esta sección es mostrar cómo configurar y probar el inicio de sesión único de Azure AD con Condeco con un usuario de prueba llamado "Britta Simon".

Para que el inicio de sesión único funcione, Azure AD debe saber cuál es el usuario homólogo de Condeco para un usuario de Azure AD. Es decir, es necesario establecer una relación de vínculo entre un usuario de Azure AD y el usuario relacionado de Condeco.  

Esta relación de vínculo se establece asignando el valor del **nombre de usuario** en Azure AD como el valor del **nombre de usuario** en Condeco.

Para configurar y probar el inicio de sesión único de Azure AD con Condeco, es preciso completar los siguientes bloques de creación:
 
1. **[Configuración del inicio de sesión único de Azure AD](#configuring-azure-ad-single-single-sign-on)**: para permitir a los usuarios usar esta característica.
2. **[Creación de un usuario de prueba de Azure AD](#creating-an-azure-ad-test-user)** : para probar el inicio de sesión único de Azure AD con Britta Simon.
3. **[Crear un usuario de prueba de Condeco](#creating-a-Condeco-test-user)** : para tener un homólogo de Britta Simon en Condeco que esté vinculado a la representación de ella en Azure AD.
4. **[Asignación del usuario de prueba de Azure AD](#assigning-the-azure-ad-test-user)** : para permitir que Britta Simon use el inicio de sesión único de Azure AD.
5. **[Prueba del inicio de sesión único](#testing-single-sign-on)**: para comprobar si funciona la configuración.

### <a name="configuring-azure-ad-single-sign-on"></a>Configuración del inicio de sesión único de Azure AD
El objetivo de esta sección es habilitar el inicio de sesión único de Azure AD en el Portal de Azure clásico y configurar el inicio de sesión único en la aplicación Condeco.

**Para configurar el inicio de sesión único de Azure AD con Condeco, realice los pasos siguientes:**

1. En el Portal de Azure clásico, en la página de integración de aplicaciones de **Condeco**, haga clic en **Configurar inicio de sesión único** para abrir el cuadro de diálogo **Configurar inicio de sesión único**.
   
    ![Configurar inicio de sesión único][6] 
2. En la página **¿Cómo desea que los usuarios inicien sesión en Condeco?**, seleccione **Inicio de sesión único de Microsoft Azure AD** y haga clic en **Siguiente**.
   
    ![Configurar inicio de sesión único](./media/active-directory-saas-condeco-tutorial/tutorial_condeco_03.png) 
3. En la página del cuadro de diálogo **Configurar las opciones de la aplicación** , realice los pasos siguientes:
   
    ![Configurar inicio de sesión único](./media/active-directory-saas-condeco-tutorial/tutorial_condeco_04.png) 
  1. En el cuadro de texto URL de inicio de sesión, escriba la dirección URL que usan los usuarios para iniciar sesión en su aplicación de Condeco con el siguiente patrón: **“https://companyname.condecosoftware.com”**.
  2. Haga clic en **Siguiente**.
4. En la página **Configurar inicio de sesión único en Condeco** , siga estos pasos:
   
    ![Configurar inicio de sesión único](./media/active-directory-saas-condeco-tutorial/tutorial_condeco_05.png)   
  1. Haga clic en **Descargar metadatos**y luego guarde el archivo en el equipo.
  2. Haga clic en **Siguiente**.
5. Para que se configure el SSO para la aplicación, póngase en contacto con su equipo de soporte técnico de Condesco a través de supportna@condecosoftware.com y adjunte el archivo de metadatos descargado a su correo electrónico.
6. En el Portal de Azure clásico, seleccione la confirmación de la configuración de inicio de sesión único y haga clic en **Siguiente**.
   
    ![Inicio de sesión único de Azure AD ][10]
7. En la página **Confirmación del inicio de sesión único**, haga clic en **Completar**.  
   
    ![Inicio de sesión único de Azure AD ][11]

### <a name="create-an-azure-ad-test-user"></a>Creación de un usuario de prueba de Azure AD
El objetivo de esta sección es crear un usuario de prueba en el Portal de Azure clásico llamado Britta Simon.  

![Creación de un usuario de Azure AD][20]

**Siga estos pasos para crear un usuario de prueba en Azure AD:**

1. En el panel de navegación izquierdo del **Portal de Azure clásico**, haga clic en **Active Directory**.
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/create_aaduser_09.png) 
2. En la lista **Directory** , seleccione el directorio cuya integración desee habilitar.
3. Para mostrar la lista de usuarios, en el menú de la parte superior, haga clic en **Usuarios**.
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/create_aaduser_03.png) 
4. Para abrir el cuadro de diálogo **Agregar usuario**, en la barra de herramientas de la parte inferior, haga clic en **Agregar usuario**.
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/create_aaduser_04.png) 
5. En la página de diálogo **Proporcione información sobre este usuario** , realice los pasos siguientes:
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/create_aaduser_05.png) 
  1. En Tipo de usuario, seleccione Nuevo usuario de la organización. 
  2. En el cuadro de texto **Nombre de usuario**, escriba**BrittaSimon**.
  3. Haga clic en **Siguiente**.
6. En la página de diálogo **Perfil de usuario** , realice los pasos siguientes:
   
   ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/create_aaduser_06.png) 
  1. En el cuadro de texto **Nombre**, escriba **Britta**.    
  2. En el cuadro de texto **Apellidos**, escriba **Simon**.
  3. En el cuadro de texto **Nombre para mostrar**, escriba **Britta Simon**.
  4. En la lista **Rol**, seleccione **Usuario**.
  5. Haga clic en **Siguiente**.
7. En el cuadro de diálogo **Obtener contraseña temporal**, haga clic en **Crear**.
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/create_aaduser_07.png) 
8. En la página de diálogo **Obtener contraseña temporal** , realice los pasos siguientes:
   
    ![Creación de un usuario de prueba de Azure AD](./media/active-directory-saas-condeco-tutorial/create_aaduser_08.png) 
  1. Anote el valor del campo **Nueva contraseña**.
  2. Haga clic en **Completo**.   

### <a name="create-a-condeco-test-user"></a>Creación de un usuario de prueba de Condeco
El objetivo de esta sección es crear un usuario llamado Britta Simon en Condeco. Condeco admite el aprovisionamiento Just-In-Time, que está habilitado de forma predeterminada.

No hay ningún elemento de acción para usted en esta sección. Durante un intento de obtener acceso a Condeco se creará un nuevo usuario, en caso de que no exista. [Configuración del inicio de sesión único de Azure AD](#configuring-azure-ad-single-single-sign-on).

>[!NOTE]
>Si necesita crear manualmente un usuario, es preciso que se ponga contacto con el equipo de soporte técnico de Condeco. 
> 

### <a name="assign-the-azure-ad-test-user"></a>Asignación del usuario de prueba de Azure AD
El objetivo de esta sección es permitir que Britta Simon use el inicio de sesión único de Azure, para lo que se le concederá acceso a Condeco.

![Asignar usuario][200] 

**Para asignar a Britta Simon a Condeco, realice los pasos siguientes:**

1. En el Portal de Azure clásico, para abrir la vista de aplicaciones, en la vista del directorio, haga clic en **Aplicaciones** en el menú superior.
   
    ![Asignar usuario][201] 
2. En la lista de aplicaciones, seleccione **Condeco**.
   
    ![Configurar inicio de sesión único](./media/active-directory-saas-condeco-tutorial/tutorial_condeco_50.png) 
3. En el menú de la parte superior, haga clic en **Usuarios**.
   
    ![Asignar usuario][203] 
4. En la lista Usuarios, seleccione **Britta Simon**.
5. En la barra de herramientas de la parte inferior, haga clic en **Asignar**.
   
    ![Asignar usuario][205]

### <a name="test-single-sign-on"></a>Prueba de inicio de sesión único
El objetivo de esta sección es probar la configuración del inicio de sesión único de Azure AD mediante el panel de acceso.  

Al hacer clic en el icono de Condeco en el Panel de acceso, debería iniciar sesión automáticamente en su aplicación Condeco.

## <a name="additional-resources"></a>Recursos adicionales
* [Lista de tutoriales sobre cómo integrar aplicaciones SaaS con Azure Active Directory](active-directory-saas-tutorial-list.md)
* [¿Qué es el acceso a aplicaciones y el inicio de sesión único con Azure Active Directory?](active-directory-appssoaccess-whatis.md)

<!--Image references-->

[1]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_04.png

[6]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_05.png
[10]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_06.png
[11]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_07.png
[20]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_201.png
[203]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_203.png
[204]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_204.png
[205]: ./media/active-directory-saas-condeco-tutorial/tutorial_general_205.png

