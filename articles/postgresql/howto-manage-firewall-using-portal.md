---
title: "Creación y administración de reglas de firewall de Azure Database for PostgreSQL mediante Azure Portal | Microsoft Docs"
description: "Creación y administración de reglas de firewall de Azure Database for PostgreSQL mediante Azure Portal"
services: postgresql
author: jasonwhowell
ms.author: jasonh
manager: jhubbard
editor: jasonh
ms.assetid: 
ms.service: postgresql-database
ms.tgt_pltfrm: portal
ms.topic: article
ms.date: 05/10/2017
ms.translationtype: Human Translation
ms.sourcegitcommit: 71fea4a41b2e3a60f2f610609a14372e678b7ec4
ms.openlocfilehash: b93827ec35916759c26e5e58186acaff1f160a35
ms.contentlocale: es-es
ms.lasthandoff: 05/10/2017

---
# <a name="create-and-manage-azure-database-for-postgresql-firewall-rules-using-the-azure-portal"></a>Creación y administración de reglas de firewall de Azure Database for PostgreSQL mediante Azure Portal
Las reglas de firewall de nivel de servidor permiten a los administradores tener acceso a un servidor de Azure Database for PostgreSQL desde una dirección IP o desde un intervalo de direcciones IP especificado. 

## <a name="prerequisites"></a>Requisitos previos
Para seguir esta guía, necesitará:
- Un servidor [Creación de una instancia de Azure Database for PostgreSQL](quickstart-create-server-database-portal.md)

## <a name="create-a-server-level-firewall-rule-in-the-azure-portal"></a>Creación de una regla de firewall de nivel de servidor en Azure Portal
1. En la hoja del servidor de PostgreSQL, en el encabezado Configuración, haga clic en **Seguridad de conexión** para abrir la hoja de seguridad de conexión para Azure Database for PostgreSQL.

  ![Azure Portal: haga clic en Seguridad de conexión](./media/howto-manage-firewall-using-portal/1-connection-security.png)

2. Haga clic en **Agregar mi dirección IP** en la barra de herramientas. Esto creará automáticamente una regla con la dirección IP del equipo, según lo percibido por el sistema de Azure.

  ![Azure Portal: haga clic en Agregar mi dirección IP](./media/howto-manage-firewall-using-portal/2-add-my-ip.png)

3. Compruebe la dirección IP antes de guardar la configuración. En algunos casos, la dirección IP observada por Azure Portal difiere de la dirección IP utilizada para acceder a Internet y a los servidores de Azure. Por tanto, puede necesitar cambiar las direcciones IP inicial y final para que la regla funcione según lo previsto.
Utilice un motor de búsqueda y otra herramienta en línea para comprobar su propia dirección IP (por ejemplo, busque en Bing "cuál es mi ip").

  ![Búsqueda en Bing "cuál es mi ip"](./media/howto-manage-firewall-using-portal/3-what-is-my-ip.png)

4. Agregue intervalos de direcciones adicionales. En las reglas de firewall de Azure Database for PostgreSQL, puede especificar una dirección IP o un intervalo de direcciones. Si desea limitar la regla a una única dirección IP, escriba la misma dirección en los campos de dirección IP inicial y dirección IP final. Abrir el firewall permite a los administradores y usuarios iniciar sesión en cualquier base de datos del servidor de PostgreSQL para el que tengan unas credenciales válidas.

  ![Azure Portal: reglas de firewall ](./media/howto-manage-firewall-using-portal/4-specify-addresses.png)

5. Haga clic en **Guardar**, en la barra de herramientas, para guardar esta regla de firewall de nivel de servidor. Espere la confirmación de que la actualización de las reglas de firewall se realizó correctamente.

  ![Azure Portal: haga clic en Guardar](./media/howto-manage-firewall-using-portal/5-save-firewall-rule.png)


## <a name="manage-existing-server-level-firewall-rules-through-the-azure-portal"></a>Administración de reglas de firewall de nivel de servidor existentes a través del Portal de Azure
Repita los pasos para administrar las reglas de firewall.
* Para agregar el equipo actual, haga clic en el botón + **Agregar mi dirección IP**. Haga clic en **Guardar** para guardar los cambios.
* Para agregar direcciones IP adicionales, escriba el nombre de la regla, la dirección IP inicial y la dirección IP final. Haga clic en **Guardar** para guardar los cambios.
* Para modificar una regla existente, haga clic en cualquiera de los campos de la regla y realice la modificación. Haga clic en **Guardar** para guardar los cambios.
* Para eliminar una regla existente, haga clic en el botón de puntos suspensivos […] y haga clic en Eliminar para quitar la regla. Haga clic en **Guardar** para guardar los cambios.

## <a name="next-steps"></a>Pasos siguientes
- De modo similar, puede utilizar scripts para la [Creación y administración de reglas de firewall de Azure Database for PostgreSQL mediante la CLI de Azure](howto-manage-firewall-using-cli.md).
- Para obtener ayuda para la conexión a un servidor de Azure Database for PostgreSQL, consulte [Bibliotecas de conexión para Azure Database for PostgreSQL](concepts-connection-libraries.md).

