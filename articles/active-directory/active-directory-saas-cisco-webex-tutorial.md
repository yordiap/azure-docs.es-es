---
title: "Tutorial: Integración de Azure Active Directory con Cisco Webex | Microsoft Azure"
description: "Aprenda a usar Cisco Webex con Azure Active Directory para habilitar el inicio de sesión único, el aprovisionamiento automatizado, etc."
services: active-directory
author: jeevansd
documentationcenter: na
manager: femila
ms.assetid: 26704ca7-13ed-4261-bf24-fd6252e2072b
ms.service: active-directory
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 02/10/2017
ms.author: jeedes
translationtype: Human Translation
ms.sourcegitcommit: ada8ffbbdc5565a517f5a06cb640a36aaf8879b4
ms.openlocfilehash: b44b1a5b3e988a51db3325ec8a181651fa84e768
ms.lasthandoff: 02/17/2017


---
# <a name="tutorial-azure-active-directory-integration-with-cisco-webex"></a>Tutorial: integración de Azure Active Directory con Cisco Webex
El objetivo de este tutorial es mostrar la integración de Azure y Cisco Webex.  
En la situación descrita en este tutorial se supone que ya cuenta con los elementos siguientes:

* Una suscripción de Azure válida
* Un inquilino de Cisco Webex

Después de completar este tutorial, los usuarios de Azure AD que ha asignado a Cisco Webex podrán realizar un inicio de sesión único en la aplicación en el sitio de la compañía de Cisco Webex (inicio de sesión iniciado por el proveedor de servicios) o con la [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).

La situación descrita en este tutorial consta de los siguientes bloques de creación:

* Habilitación de la integración de aplicaciones para Cisco Webex
* Configuración del inicio de sesión único (SSO)
* Configuración del aprovisionamiento de usuario
* Asignación de usuarios

![Escenario](./media/active-directory-saas-cisco-webex-tutorial/IC777614.png "Escenario")

## <a name="enable-the-application-integration-for-cisco-webex"></a>Habilitación de la integración de aplicaciones para Cisco Webex
El objetivo de esta sección es describir cómo se habilita la integración de aplicaciones para Cisco Webex.

**Siga estos pasos para habilitar la integración de aplicaciones para Cisco Webex:**

1. En el panel de navegación izquierdo del Portal de Azure clásico, haga clic en **Active Directory**.
   
   ![Active Directory](./media/active-directory-saas-cisco-webex-tutorial/IC700993.png "Active Directory")
2. En la lista **Directory** , seleccione el directorio cuya integración desee habilitar.
3. Para abrir la vista de aplicaciones, haga clic en **Applications** , en el menú superior de la vista de directorios.
   
   ![Aplicaciones](./media/active-directory-saas-cisco-webex-tutorial/IC700994.png "Aplicaciones")
4. Haga clic en **Agregar** en la parte inferior de la página.
   
   ![Agregar aplicaciones](./media/active-directory-saas-cisco-webex-tutorial/IC749321.png "Agregar aplicaciones")
5. En el cuadro de diálogo **¿Qué desea hacer?**, haga clic en **Agregar una aplicación de la galería**.
   
   ![Agregar una aplicación de la galería](./media/active-directory-saas-cisco-webex-tutorial/IC749322.png "Agregar una aplicación de la galería")
6. En el **cuadro de búsqueda**, escriba **Cisco Webex**.
   
   ![Galería de aplicaciones](./media/active-directory-saas-cisco-webex-tutorial/IC777615.png "Galería de aplicaciones")
7. En el panel de resultados, seleccione **Cisco Webex** y, a continuación, haga clic en **Completar** para agregar la aplicación.
   
   ![Cisco Webex](./media/active-directory-saas-cisco-webex-tutorial/IC777616.png "Cisco Webex")
   
## <a name="configure-single-sign-on"></a>Configurar inicio de sesión único

El objetivo de esta sección es describir cómo habilitar usuarios para que se autentiquen en Cisco Webex con su cuenta de Azure AD mediante federación basada en el protocolo SAML.  

Como parte de este procedimiento, es necesario crear un certificado codificado en base&64;. Si no está familiarizado con este procedimiento, consulte [Conversión de un certificado binario en un archivo de texto](http://youtu.be/PlgrzUZ-Y1o)

**Siga estos pasos para configurar el inicio de sesión único:**

1. En el Portal de Azure clásico, en la página de integración de aplicaciones de **Cisco Webex**, haga clic en **Configurar inicio de sesión único** para abrir el cuadro de diálogo **Configurar inicio de sesión único**.
   
   ![Configurar inicio de sesión único](./media/active-directory-saas-cisco-webex-tutorial/IC777617.png "Configurar inicio de sesión único")
2. En la página **How would you like users to sign on to Cisco Webex** (¿Cómo desea que los usuarios inicien sesión en Cisco Webex?), seleccione **Inicio de sesión único de Microsoft Azure AD** y, a continuación, haga clic en **Siguiente**.
   
   ![Configurar inicio de sesión único](./media/active-directory-saas-cisco-webex-tutorial/IC777618.png "Configurar inicio de sesión único")
3. En la página **Configurar dirección URL de la aplicación**, realice los pasos siguientes y luego haga clic en **Siguiente**.
   
   ![Configurar dirección URL de la aplicación](./media/active-directory-saas-cisco-webex-tutorial/IC777619.png "Configurar dirección URL de la aplicación")   
   1. En el cuadro de texto **URL de inicio de sesión**, escriba la dirección URL de inquilino de Cisco Webex (p. ej.: *http://contoso.webex.com*).
   2. En el cuadro de texto **URL de respuesta de Cisco Webex**, escriba su **dirección URL de Cisco Webex AssertionConsumerService** (por ejemplo: *https://company.webex.com/dispatcher/SAML2AuthService?siteurl=company*).
4. En la página **Configurar inicio de sesión único en Cisco Webex**, para descargar el certificado, haga clic en **Descargar certificado** y luego guarde el archivo de certificado en el equipo.
   
   ![Configurar inicio de sesión único](./media/active-directory-saas-cisco-webex-tutorial/IC777620.png "Configurar inicio de sesión único")
5. En otra ventana del explorador web, inicie sesión como administrador en el sitio de la compañía de Cisco Webex.
6. En el menú de la parte superior, haga clic en **Site Administration**(Administración de sitio).
   
   ![Administración de sitios](./media/active-directory-saas-cisco-webex-tutorial/IC777621.png "Administración de sitios")
7. En la sección **Manage Site** (Administrar sitio), haga clic en **SSO Configuration** (Configuración de SSO).
   
   ![Configuración de SSO](./media/active-directory-saas-cisco-webex-tutorial/IC777622.png "Configuración de SSO")
8. En la sección Federated Web SSO Configuration (configuración de SSO web federado), realice los pasos siguientes:
   
   ![Configuración de SSO federado](./media/active-directory-saas-cisco-webex-tutorial/IC777623.png "Configuración de SSO federado")  
   1. En la lista de **protocolos de federación**, seleccione **SAML 2.0**.
   2. Cree un archivo **codificado en base&64;** a partir del certificado descargado.  
    >[!TIP]
    >Para obtener más información, consulte [Conversión de un certificado binario en un archivo de texto](http://youtu.be/PlgrzUZ-Y1o)
    >  
   3. Abra el certificado codificado en base&64; en el Bloc de notas y luego copie el contenido del mismo.
   4. Haga clic en **Import SAML Metadata**(Importar metadatos de SAML) y, a continuación, pegue el certificado codificado base&64;.
   5. En el Portal de Azure clásico, en la página del cuadro de diálogo **Configurar inicio de sesión único en Cisco Webex**, copie el valor de **URL del emisor** y péguelo en el cuadro de texto **Issuer for SAML (IdP ID)** (Emisor para SAML [Id. de IdP]).
   6. En el Portal de Azure clásico, en la página del cuadro de diálogo **Configurar inicio de sesión único en Cisco Webex**, copie el valor de **Dirección URL de inicio de sesión remoto** y péguelo en el cuadro de texto **Customer SSO Service Login URL** (URL de inicio de sesión de servicio SSO del cliente).
   7. En la lista **NameID Format** (Formato de NameID), seleccione **Email address** (Dirección de correo electrónico).
   8. En el cuadro de texto **AuthnContextClassRef**, escriba **urn: oasis: nombres: tc: SAML:2.0:ac:classes:Password**.
   9. En el Portal de Azure clásico, en la página del cuadro de diálogo **Configurar inicio de sesión único en Cisco Webex**, copie el valor de **Dirección URL de cierre de sesión remoto** y péguelo en el cuadro de texto **Customer SSO Service Logout URL** (URL de cierre de sesión de servicio SSO del cliente).
   10. Haga clic en **Update**(Actualizar).
9. En el Portal de Azure clásico, en la página del cuadro de diálogo **Configurar inicio de sesión único en Cisco Webex**, seleccione la confirmación de configuración de inicio de sesión único y luego haga clic en **Completa**.
   
   ![Configurar inicio de sesión único](./media/active-directory-saas-cisco-webex-tutorial/IC777624.png "Configurar inicio de sesión único")
   
## <a name="configure-user-provisioning"></a>Configurar aprovisionamiento de usuarios

Para permitir que los usuarios de Azure AD inicien sesión en Cisco Webex, tienen que aprovisionarse en Cisco Webex.  

* En el caso de Cisco Webex, el aprovisionamiento es una tarea manual.

**Para aprovisionar cuentas de usuario, realice estos pasos:**

1. Inicie sesión en su inquilino de **Cisco Webex** .
2. Vaya a **Manage Users (Administrar usuarios) \> Add User** (Agregar usuario).
   
   ![Agregar usuarios](./media/active-directory-saas-cisco-webex-tutorial/IC777625.png "Agregar usuarios")
3. En la sección Add User (agregar usuario), realice estos pasos:
   
   ![Agregar usuario](./media/active-directory-saas-cisco-webex-tutorial/IC777626.png "Agregar usuario")   
   1. En **Account Type** (Tipo de cuenta) seleccione **Host**.
   2. Escriba la información de un usuario existente de Azure AD en los cuadros de texto siguientes: **First name, Last name** (Nombre, Apellido), **User name** (Nombre de usuario), **Email** (Correo electrónico), **Password** (Contraseña), **Confirm Password** (Confirmar contraseña).
   3. Haga clic en **Agregar**.

>[!NOTE]
>Puede usar cualquier otra API o herramienta de creación de cuentas de usuario de Cisco Webex ofrecida por Cisco Webex para aprovisionar cuentas de usuario de AAD. 
> 

## <a name="assign-users"></a>Asignar usuarios
Para probar la configuración, debe conceder acceso a los usuarios de Azure AD a los que quiere permitir el uso de su aplicación.

**Para asignar usuarios a Cisco Webex, realice los siguientes pasos:**

1. En el Portal de Azure clásico, cree una cuenta de prueba.
2. En la página de integración de la aplicación **Cisco Webex**, haga clic en **Asignar usuarios**.
   
   ![Asignar usuarios](./media/active-directory-saas-cisco-webex-tutorial/IC777627.png "Asignar usuarios")
3. Seleccione su usuario de prueba, haga clic en **Asignar** y en **Sí** para confirmar la asignación.
   
   ![Sí](./media/active-directory-saas-cisco-webex-tutorial/IC767830.png "Sí")

Si desea probar la configuración de inicio de sesión único, abra el Panel de acceso. Para obtener más información sobre el Panel de acceso, vea [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).


