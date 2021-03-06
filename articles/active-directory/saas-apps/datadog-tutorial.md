---
title: 'Tutorial: Integración del inicio de sesión único (SSO) de Azure Active Directory con Datadog | Microsoft Docs'
description: Aprenda a configurar el inicio de sesión único entre Azure Active Directory y Datadog.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 08/13/2020
ms.author: jeedes
ms.openlocfilehash: 4a94fb855c48f62e1c82354c4c9360edc95cad02
ms.sourcegitcommit: 9b8425300745ffe8d9b7fbe3c04199550d30e003
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "92454922"
---
# <a name="tutorial-azure-active-directory-single-sign-on-sso-integration-with-datadog"></a>Tutorial: Integración del inicio de sesión único (SSO) de Azure Active Directory con Datadog

En este tutorial, aprenderá a integrar Datadog con Azure Active Directory (Azure AD). Al integrar Datadog con Azure AD, puede hacer lo siguiente:

* Controlar en Azure AD quién tiene acceso a Datadog.
* Permitir que los usuarios inicien sesión automáticamente en Datadog con sus cuentas de Azure AD.
* Administrar las cuentas desde una ubicación central (Azure Portal).

Para más información sobre la integración de aplicaciones SaaS con Azure AD, consulte [¿Qué es el acceso a aplicaciones y el inicio de sesión único con Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)

## <a name="prerequisites"></a>Prerrequisitos

Para empezar, necesita los siguientes elementos:

* Una suscripción de Azure AD. Si no tiene una suscripción, puede crear una [cuenta gratuita](https://azure.microsoft.com/free/).
* Una suscripción habilitada para el inicio de sesión único (SSO) en Datadog.

## <a name="scenario-description"></a>Descripción del escenario

En este tutorial, va a configurar y probar el inicio de sesión único de Azure AD en un entorno de prueba.

* Datadog admite el inicio de sesión único iniciado por **SP e IDP** .
* Una vez configurado Datadog, puede aplicar el control de sesión, que protege la filtración y la infiltración de la información confidencial de la organización en tiempo real. El control de sesión procede del acceso condicional. [Aprenda a aplicar el control de sesión con Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).


## <a name="adding-datadog-from-the-gallery"></a>Adición de Datadog desde la galería

Para configurar la integración de Datadog en Azure AD, deberá agregar Datadog desde la galería a la lista de aplicaciones SaaS administradas.

1. Inicie sesión en [Azure Portal](https://portal.azure.com) con una cuenta personal, profesional o educativa de Microsoft.
1. En el panel de navegación de la izquierda, seleccione el servicio **Azure Active Directory** .
1. Vaya a **Aplicaciones empresariales** y seleccione **Todas las aplicaciones** .
1. Para agregar una nueva aplicación, seleccione **Nueva aplicación** .
1. En la sección **Agregar desde la galería** , escriba **Datadog** en el cuadro de búsqueda.
1. Seleccione **Datadog** en el panel de resultados y agregue la aplicación. Espere unos segundos mientras la aplicación se agrega al inquilino.


## <a name="configure-and-test-azure-ad-sso-for-datadog"></a>Configuración y prueba del inicio de sesión único de Azure AD para Datadog

Configure y pruebe el inicio de sesión único de Azure AD con Datadog mediante un usuario de prueba llamado **B.Simon** . Para que el inicio de sesión único funcione, es preciso establecer una relación de vinculación entre un usuario de Azure AD y el usuario relacionado de Datadog.

Para configurar y probar el inicio de sesión único de Azure AD con Datadog, es preciso completar los siguientes bloques de creación:

1. **[Configuración del inicio de sesión único de Azure AD](#configure-azure-ad-sso)** , para permitir que los usuarios puedan utilizar esta característica.
    1. **[Creación de un usuario de prueba de Azure AD](#create-an-azure-ad-test-user)** , para probar el inicio de sesión único de Azure AD con B.Simon.
    1. **[Asignación del usuario de prueba de Azure AD](#assign-the-azure-ad-test-user)** , para habilitar a B.Simon para que use el inicio de sesión único de Azure AD.
1. **[Configuración del inicio de sesión único en Datadog](#configure-datadog-sso)** , para configurar los valores de inicio de sesión único en la aplicación.
    1. **[Creación de un usuario de prueba de Datadog](#create-datadog-test-user)** : para tener un homólogo de B.Simon en Datadog que esté vinculado a la representación del usuario en Azure AD.
1. **[Prueba del inicio de sesión único](#test-sso)** : para comprobar si la configuración funciona.

## <a name="configure-azure-ad-sso"></a>Configuración del inicio de sesión único de Azure AD

Siga estos pasos para habilitar el inicio de sesión único de Azure AD en Azure Portal.

1. En [Azure Portal](https://portal.azure.com/), en la página de integración de aplicaciones de **Datadog** , busque la sección **Administrar** y seleccione **Inicio de sesión único** .
1. En la página **Seleccione un método de inicio de sesión único** , elija **SAML** .
1. En la página **Configurar el inicio de sesión único con SAML** , haga clic en el icono de edición o con forma de lápiz para abrir el cuadro de diálogo **Configuración básica de SAML** y modificar la configuración.

   ![Edición de la configuración básica de SAML](common/edit-urls.png)

1. En la sección **Configuración básica de SAML** , el usuario no tiene que realizar ningún paso porque la aplicación ya se ha integrado previamente con Azure.

1. Haga clic en **Establecer direcciones URL adicionales** y siga este paso si desea configurar la aplicación en el modo iniciado por **SP** :

    En el cuadro de texto **URL de inicio de sesión** , escriba una dirección URL con el siguiente patrón: `https://app.datadoghq.com/account/login/id/<CUSTOM_IDENTIFIER>`

    > [!NOTE]
    > Este valor no es real. Actualícelo con la dirección URL de inicio de sesión real. Póngase en contacto con el [equipo de soporte técnico para clientes de Datadog](mailto:support@datadoghq.com) para obtener el valor. También puede hacer referencia a los patrones que se muestran en la sección **Configuración básica de SAML** de Azure Portal.

1. Haga clic en **Save** (Guardar).

1. En la página **Configurar el inicio de sesión único con SAML** , en la sección **Certificado de firma de SAML** , busque **XML de metadatos de federación** y seleccione **Descargar** para descargar el certificado y guardarlo en su equipo.

    ![Vínculo de descarga del certificado](common/metadataxml.png)

1. En la sección **Configurar Datadog** , copie las direcciones URL adecuadas según sus necesidades.

    ![Copiar direcciones URL de configuración](common/copy-configuration-urls.png)

### <a name="create-an-azure-ad-test-user"></a>Creación de un usuario de prueba de Azure AD

En esta sección, va a crear un usuario de prueba llamado B.Simon en Azure Portal.

1. En el panel izquierdo de Azure Portal, seleccione **Azure Active Directory** , **Usuarios** y **Todos los usuarios** .
1. Seleccione **Nuevo usuario** en la parte superior de la pantalla.
1. En las propiedades del **usuario** , siga estos pasos:
   1. En el campo **Nombre** , escriba `B.Simon`.  
   1. En el campo **Nombre de usuario** , escriba username@companydomain.extension. Por ejemplo, `B.Simon@contoso.com`.
   1. Active la casilla **Show password** (Mostrar contraseña) y, después, anote el valor que se muestra en el cuadro **Contraseña** .
   1. Haga clic en **Crear** .

### <a name="assign-the-azure-ad-test-user"></a>Asignación del usuario de prueba de Azure AD

En esta sección, va a permitir que B.Simon acceda a Datadog mediante el inicio de sesión único de Azure.

1. En Azure Portal, seleccione sucesivamente **Aplicaciones empresariales** y **Todas las aplicaciones** .
1. En la lista de aplicaciones, seleccione **Datadog** .
1. En la página de información general de la aplicación, busque la sección **Administrar** y seleccione **Usuarios y grupos** .

   ![Vínculo "Usuarios y grupos"](common/users-groups-blade.png)

1. Seleccione **Agregar usuario** . A continuación, en el cuadro de diálogo **Agregar asignación** , seleccione **Usuarios y grupos** .

    ![Vínculo de Agregar usuario](common/add-assign-user.png)

1. En el cuadro de diálogo **Usuarios y grupos** , seleccione **B.Simon** de la lista de usuarios y haga clic en el botón **Seleccionar** de la parte inferior de la pantalla.
1. Si espera que haya un valor de rol en la aserción de SAML, en el cuadro de diálogo **Seleccionar rol** , seleccione en la lista el rol adecuado para el usuario y haga clic en el botón **Seleccionar** en la parte inferior de la pantalla.
1. En el cuadro de diálogo **Agregar asignación** , haga clic en el botón **Asignar** .


## <a name="configure-datadog-sso"></a>Configuración del inicio de sesión único de Datadog

Para configurar el inicio de sesión único en **Datadog** , es preciso enviar el **XML de metadatos de federación** descargado y las direcciones URL apropiadas copiadas de Azure Portal al [equipo de soporte técnico de Datadog](mailto:support@datadoghq.com). Dicho equipo lo configura para establecer la conexión de SSO de SAML correctamente en ambos lados.

### <a name="create-datadog-test-user"></a>Creación de un usuario de prueba de Datadog

En esta sección creará un usuario llamado B.Simon en Datadog. Trabaje con el [equipo de soporte técnico de Datadog](mailto:support@datadoghq.com) para agregar los usuarios a la plataforma de Datadog.

## <a name="test-sso"></a>Prueba de SSO 

En esta sección, probará la configuración de inicio de sesión único de Azure AD mediante el Panel de acceso.

Al hacer clic en el icono de Datadog en el Panel de acceso, debería iniciar sesión automáticamente en la instancia de Datadog para la que configuró el inicio de sesión único. Para más información sobre el Panel de acceso, consulte [Introducción al Panel de acceso](../user-help/my-apps-portal-end-user-access.md).

### <a name="enable-all-users-from-your-tenant-to-authenticate-with-the-app"></a>Habilitación de todos los usuarios del inquilino para que se autentiquen con la aplicación

En esta sección, habilitará a todos los usuarios del inquilino para que accedan a Datadog si un usuario tiene una cuenta en Datadog.

1. En Azure Portal, seleccione sucesivamente **Aplicaciones empresariales** y **Todas las aplicaciones** .
1. En la lista de aplicaciones, seleccione **Datadog** .
1. En la página de información general de la aplicación, en **Administrar** , seleccione **Propiedades** .

    ![Vínculo "Propiedades"](common/properties.png)

1. En **¿Asignación de usuarios?** , seleccione **No** .

    ![No es necesaria la asignación de usuarios.](common/user-assignment-not-required.png)

1. Seleccione **Guardar** .

## <a name="additional-resources"></a>Recursos adicionales

- [Lista de tutoriales acerca de cómo integrar aplicaciones SaaS con Azure Active Directory](./tutorial-list.md)

- [¿Qué es el acceso a las aplicaciones y el inicio de sesión único con Azure Active Directory? ](../manage-apps/what-is-single-sign-on.md)

- [¿Qué es el acceso condicional en Azure Active Directory?](../conditional-access/overview.md)

- [Pruebe Datadog con Azure AD](https://aad.portal.azure.com/)

- [¿Qué es el control de sesiones en Microsoft Cloud App Security?](/cloud-app-security/proxy-intro-aad)