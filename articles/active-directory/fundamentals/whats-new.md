---
title: Novedades Notas de la versión de Azure Active Directory | Microsoft Docs
description: Obtenga información acerca de las novedades de Azure Active Directory, como son las notas de la versión más recientes, los problemas conocidos, las correcciones de errores, las funcionalidades en desuso y los próximos cambios.
services: active-directory
author: ajburnle
manager: daveba
featureFlags:
- clicktale
ms.assetid: 06a149f7-4aa1-4fb9-a8ec-ac2633b031fb
ms.service: active-directory
ms.subservice: fundamentals
ms.workload: identity
ms.topic: conceptual
ms.date: 10/06/2020
ms.author: ajburnle
ms.reviewer: dhanyahk
ms.custom: it-pro
ms.collection: M365-identity-device-management
ms.openlocfilehash: 37dc60fd14eb26ab4c8f5a867b97369a066b743b
ms.sourcegitcommit: 28c5fdc3828316f45f7c20fc4de4b2c05a1c5548
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/22/2020
ms.locfileid: "92362763"
---
# <a name="whats-new-in-azure-active-directory"></a>¿Cuáles son las novedades de Azure Active Directory?

>Reciba notificaciones para volver a visitar esta página y obtener actualizaciones; para ello, copie y pegue la dirección URL `https://docs.microsoft.com/api/search/rss?search=%22Release+notes+-+Azure+Active+Directory%22&locale=en-us` en el ![icono del lector de fuentes icono RSS](./media/whats-new/feed-icon-16x16.png) lector de fuentes.

En Azure AD se realizan mejoras de forma continua. Para mantenerse al día de los avances más recientes, este artículo proporciona información acerca de los elementos siguientes:

- Versiones más recientes
- Problemas conocidos
- Corrección de errores
- Funciones obsoletas
- Planes de cambios

Esta página se actualiza mensualmente, por lo que se recomienda visitarla con frecuencia. Si busca elementos que tengan más de seis meses, puede encontrarlos en el [Archivo de novedades de Azure Active Directory](whats-new-archive.md).

---

## <a name="september-2020"></a>Septiembre de 2020

### <a name="new-provisioning-connectors-in-the-azure-ad-application-gallery---september-2020"></a>Nuevos conectores de aprovisionamiento en la galería de aplicaciones de Azure AD, septiembre de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Integración de terceros
 
Ahora, puede automatizar la creación, actualización y eliminación de cuentas de usuario para estas aplicaciones recién integradas:

- [Coda](../saas-apps/coda-provisioning-tutorial.md)
- [Cofense Recipient Sync](../saas-apps/cofense-provision-tutorial.md)
- [InVision](../saas-apps/invision-provisioning-tutorial.md)
- [myday](../saas-apps/myday-provision-tutorial.md)
- [SAP Analytics Cloud](../saas-apps/sap-analytics-cloud-provisioning-tutorial.md)
- [Webroot Security Awareness](../saas-apps/webroot-security-awareness-training-provisioning-tutorial.md)

Para más información acerca de cómo proteger mejor una organización mediante el aprovisionamiento automatizado de cuentas de usuario, consulte [Automatización del aprovisionamiento y desaprovisionamiento de usuarios para aplicaciones SaaS con Azure Active Directory](../app-provisioning/user-provisioning.md).
 
---
### <a name="cloud-provisioning-public-preview-refresh"></a>Actualización de la versión preliminar pública del aprovisionamiento en la nube

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento en la nube de Azure AD **Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
La actualización de la versión preliminar pública del aprovisionamiento en la nube de Azure AD Connect presenta dos mejoras importantes desarrolladas a partir de los comentarios de los clientes: 

- Experiencia de asignación de atributos a través de Azure Portal

    Con esta característica, los administradores de TI pueden asignar atributos de usuario, grupo o contacto de AD a Azure AD con varios tipos de asignación presentes hoy en día. La asignación de atributos es una característica que se usa para normalizar los valores de los atributos que fluyen desde Active Directory hasta Azure Active Directory. Puede determinar si se debe asignar directamente el valor del atributo tal como es de AD a Azure AD o usar expresiones para transformar los valores del atributo durante el aprovisionamiento de usuarios. [Más información](../cloud-provisioning/how-to-attribute-mapping.md)

- Experiencia del usuario de prueba o aprovisionamiento a petición

    Una vez que haya realizado la configuración, puede que quiere llevar a cabo una prueba para ver si la transformación de usuario funciona según lo esperado antes de aplicarla a todos los usuarios del ámbito. Con el aprovisionamiento a petición, los administradores de TI pueden escribir el nombre distintivo (DN) de un usuario de AD y comprobar si se está sincronizando según lo previsto. El aprovisionamiento a petición proporciona una excelente manera de asegurarse de que las asignaciones de atributos realizadas con anterioridad siguen funcionando según lo esperado. [Más información](../cloud-provisioning/how-to-on-demand-provision.md)
 
---

### <a name="audited-bitlocker-recovery-in-azure-ad---public-preview"></a>Recuperación de BitLocker auditada en Azure AD: versión preliminar pública

**Tipo:** Nueva característica  
**Categoría del servicio:** Administración de acceso de dispositivos  
**Funcionalidad del producto:** Administración del ciclo de vida de dispositivos
 
Ahora, cuando los administradores de TI o los usuarios finales leen las claves de recuperación de BitLocker a las que tienen acceso, Azure Active Directory genera un registro de auditoría que captura quién ha accedido a la clave de recuperación. La misma auditoría proporciona detalles del dispositivo al que está asociada la clave de BitLocker.

Los usuarios finales pueden [acceder a sus claves de recuperación a través de Mi cuenta](../user-help/my-account-portal-devices-page.md#view-a-bitlocker-key). Los administradores de TI pueden acceder a las claves de recuperación mediante la [API de claves de recuperación de BitLocker en versión beta](/graph/api/resources/bitlockerrecoverykey?view=graph-rest-beta) o a través del portal de Azure AD. Para obtener más información, vea [Ver o copiar las claves de BitLocker en el portal de Azure AD](../devices/device-management-azure-portal.md#view-or-copy-bitlocker-keys).

---

### <a name="teams-devices-administrator-built-in-role"></a>Rol integrado de Administrador de dispositivos de Teams

**Tipo:** Nueva característica  
**Categoría del servicio:** RBAC  
**Funcionalidad del producto:** Control de acceso
 
Los usuarios con el rol de [Administrador de dispositivos de Teams](../roles/permissions-reference.md#teams-devices-administrator) pueden administrar [dispositivos certificados para Teams](https://www.microsoft.com/microsoft-365/microsoft-teams/across-devices/devices) desde el centro de administración de Teams. 

Este rol permite a los usuarios ver todos los dispositivos de un solo vistazo, con la posibilidad de buscar y filtrar dispositivos. El usuario también puede comprobar los detalles de cada dispositivo, por ejemplo, la cuenta con la que se ha iniciado sesión, la marca y el modelo del dispositivo. El usuario puede cambiar la configuración en el dispositivo y actualizar las versiones de software. Este rol no concede permisos para comprobar la actividad de Teams ni la calidad de las llamadas del dispositivo.
 
---

### <a name="advanced-query-capabilities-for-directory-objects"></a>Capacidades de consulta avanzada para objetos de directorio

**Tipo:** Nueva característica  
**Categoría del servicio:** MS Graph  
**Funcionalidad del producto:** Experiencia para el desarrollador
 
Todas las nuevas capacidades de consulta presentadas para objetos de directorio en las API de Azure AD ahora están disponibles en el punto de conexión v1.0 y están listas para producción. Los desarrolladores pueden contar, buscar, filtrar y ordenar objetos de directorio y vínculos relacionados mediante los operadores estándar de OData.

Para obtener más información, vea la documentación [aquí](https://aka.ms/BlogPostMezzoGA); también puede enviar comentarios mediante esta [breve encuesta](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR_yN8EPoGo5OpR1hgmCp1XxUMENJRkNQTk5RQkpWTE44NEk2U0RIV0VZRy4u).
 
---

### <a name="public-preview-continuous-access-evaluation-for-tenants-who-configured-conditional-access-policies"></a>Versión preliminar pública: evaluación de acceso continua para inquilinos que han configurado directivas de acceso condicional

**Tipo:** Nueva característica  
**Categoría del servicio:** Autenticaciones (inicios de sesión)  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 
La evaluación de acceso continua (CAE) ahora está disponible en versión preliminar pública para inquilinos de Azure AD con directivas de acceso condicional. Con CAE, los eventos de seguridad críticos y las directivas se evalúan en tiempo real. Esto incluye la deshabilitación de cuentas, el restablecimiento de contraseñas y el cambio de ubicación. Para obtener más información, vea [Evaluación continua de acceso](../conditional-access/concept-continuous-access-evaluation.md).

---

### <a name="public-preview-ask-users-requesting-an-access-package-additional-questions-to-improve-approval-decisions"></a>Versión preliminar pública: preguntas adicionales a los usuarios que solicitan un paquete de acceso para mejorar las decisiones de aprobación

**Tipo:** Nueva característica  
**Categoría del servicio:** Administración de acceso de usuarios  
**Funcionalidad del producto:** Administración de derechos
 
Los administradores ahora pueden exigir que los usuarios que solicitan un paquete de acceso respondan a preguntas adicionales más allá de la justificación comercial en el portal Mi acceso de administración de derechos de Azure AD. Las respuestas de los usuarios se muestran a los aprobadores para ayudarles a tomar una decisión de aprobación de acceso más precisa. Para obtener más información, vea [Recopilación de información del solicitante adicional para su aprobación (versión preliminar)](../governance/entitlement-management-access-package-approval-policy.md#collect-additional-requestor-information-for-approval-preview).
 
---

### <a name="public-preview-enhanced-user-management"></a>Versión preliminar pública: administración de usuarios mejorada

**Tipo:** Nueva característica  
**Categoría del servicio:** User Management  
**Funcionalidad del producto:** User Management
 

El portal de Azure AD se ha actualizado para facilitar la búsqueda de usuarios en las páginas Todos los usuarios y Usuarios eliminados. Estos son algunos de los cambios de esta versión preliminar: 
- Propiedades de usuario más visibles, incluidos el identificador de objeto, el estado de sincronización de directorios, el tipo de creación y el emisor de identidades.
- Al buscar ahora se permite la búsqueda combinada de nombres, correos electrónicos e identificadores de objeto.
- Filtrado mejorado por tipo de usuario (miembro, invitado y ninguno), estado de sincronización de directorios, tipo de creación, nombre de la empresa y nombre de dominio.
- Nuevas capacidades de organización en propiedades como el nombre, el nombre principal de usuario y la fecha de eliminación.
- Un nuevo recuento de usuarios totales que se actualiza con cualquier búsqueda o filtro.

Para obtener más información, vea [Mejoras en la administración de usuarios (versión preliminar) en Azure Active Directory](../enterprise-users/users-search-enhanced.md).

---

### <a name="new-notes-field-for-enterprise-applications"></a>Nuevo campo de notas para aplicaciones empresariales

**Tipo:** Nueva característica  
**Categoría del servicio:** **Funcionalidad del producto:** Aplicaciones empresariales SSO

Puede agregar notas de texto libre a aplicaciones empresariales. Puede agregar cualquier información relevante que le ayude a administrar aplicaciones a aplicaciones empresariales. Para más información, consulte [Inicio rápido: Configuración de las propiedades de una aplicación en el inquilino de Azure Active Directory (Azure AD)](../manage-apps/add-application-portal-configure.md). 

---

### <a name="new-federated-apps-available-in-azure-ad-application-gallery---september-2020"></a>Nuevas aplicaciones federadas disponibles en la galería de aplicaciones de Azure AD, septiembre de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** Integración de terceros

En septiembre de 2020 se han agregado las siguientes 34 aplicaciones nuevas a la galería de aplicaciones con compatibilidad con la federación:

[VMware Horizon - Unified Access Gateway](), [Pulse Secure PCS](../saas-apps/vmware-horizon-unified-access-gateway-tutorial.md), [Inventory360](../saas-apps/pulse-secure-pcs-tutorial.md), [Frontitude](https://services.enteksystems.de/sso/microsoft/signup), [BookWidgets](https://www.bookwidgets.com/sso/office365), [ZVD_Server](https://zaas.zenmutech.com/user/signin), [HashData for Business](https://hashdata.app/login.xhtml), [SecureLogin](https://securelogin.securelogin.nu/sso/azure/login), [CyberSolutions MAILBASEΣ/CMSS](../saas-apps/cybersolutions-mailbase-tutorial.md), [CyberSolutions CYBERMAILΣ](../saas-apps/cybersolutions-cybermail-tutorial.md), [LimbleCMMS](https://auth.limblecmms.com/), [Glint Inc](../saas-apps/glint-inc-tutorial.md), [zeroheight](../saas-apps/zeroheight-tutorial.md), [Gender Fitness](https://app.genderfitness.com/), [Coeo Portal](https://my.coeo.com/), [Grammarly](../saas-apps/grammarly-tutorial.md), [Fivetran](../saas-apps/fivetran-tutorial.md), [Kumolus](../saas-apps/kumolus-tutorial.md), [RSA Archer Suite](../saas-apps/rsa-archer-suite-tutorial.md), [TeamzSkill](../saas-apps/teamzskill-tutorial.md), [raumfürraum](../saas-apps/raumfurraum-tutorial.md), [Saviynt](../saas-apps/saviynt-tutorial.md), [BizMerlinHR](https://marketplace.bizmerlin.net/bmone/signup), [Mobile Locker](../saas-apps/mobile-locker-tutorial.md), [Zengine](../saas-apps/zengine-tutorial.md), [CloudCADI](https://app.cloudcadi.com/login), [Simfoni Analytics](https://simfonianalytics.com/accounts/microsoft/login/), [Priva Identity & Access Management](https://my.priva.com/), [Nitro Pro](https://www.gonitro.com/nps/product-details/downloads), [Eventfinity](../saas-apps/eventfinity-tutorial.md), [Fexa](../saas-apps/fexa-tutorial.md), [Secured Signing Enterprise Portal](https://www.securedsigning.com/aad/Auth/ExternalLogin/AdminPortal), [Secured Signing Enterprise Portal AAD Setup](https://www.securedsigning.com/aad/Auth/ExternalLogin/AdminPortal), [Wistec Online](https://wisteconline.com/auth/oidc), [Oracle PeopleSoft - Protected by F5 BIG-IP APM](../saas-apps/oracle-peoplesoft-protected-by-f5-big-ip-apm-tutorial.md)

La documentación de todas las aplicaciones está disponible en https://aka.ms/AppsTutorial.

Para mostrar una aplicación en la galería de aplicaciones de Azure AD, lea los detalles de https://aka.ms/AzureADAppRequest.

---

### <a name="new-delegation-role-in-azure-ad-entitlement-management-access-package-assignment-manager"></a>Nuevo rol de delegación en la administración de derechos de Azure AD: Administrador de asignaciones de paquetes de acceso

**Tipo:** Nueva característica  
**Categoría del servicio:** Administración de acceso de usuarios  
**Funcionalidad del producto:** Administración de derechos
 
Se ha agregado un nuevo rol de Administrador de asignaciones de paquetes de acceso a la administración de derechos de Azure AD para proporcionar permisos pormenorizados para administrar asignaciones. Ahora puede delegar tareas a un usuario de este rol, que puede delegar la administración de asignaciones de un paquete de acceso a un propietario empresarial. Pero un administrador de asignaciones de paquetes de acceso no puede modificar las directivas de paquetes de acceso ni otras propiedades establecidas por los administradores. 

Con este nuevo rol, se beneficia de los privilegios mínimos necesarios para delegar la administración de asignaciones y mantener el control administrativo sobre todas las demás configuraciones de paquetes de acceso. Para obtener más información, vea [Roles de administración de derechos](../governance/entitlement-management-delegate.md#entitlement-management-roles).
 
---

### <a name="changes-to-privileged-identity-managements-onboarding-flow"></a>Cambios en el flujo de incorporación de Privileged Identity Management

**Tipo:** Característica modificada  
**Categoría del servicio:** Privileged Identity Management  
**Funcionalidad del producto:** Privileged Identity Management
 
Anteriormente, la incorporación a Privileged Identity Management (PIM) requería el consentimiento del usuario y un flujo de incorporación en la hoja de PIM que incluía la inscripción en Azure MFA. Con la reciente integración de la experiencia de PIM en la hoja de roles y administradores de Azure AD, se elimina dicha experiencia. Cualquier inquilino con una licencia P2 válida se incorpora automáticamente a PIM.

La incorporación a PIM no tiene ningún efecto adverso directo en el inquilino. Puede contar con los siguientes cambios:
- Opciones de asignación adicionales, como activa frente a válida con hora de inicio y finalización al realizar una asignación en la hoja de roles y administradores tanto de PIM como de Azure AD. 
- Mecanismos de ámbito adicionales, como Unidades administrativas y roles personalizados, incorporados directamente en la experiencia de asignación. 
- Si es un administrador global o un administrador de roles con privilegios, puede empezar a recibir algunos correos electrónicos adicionales, como el resumen semanal de PIM. 
- También podría ver la entidad de servicio MS-PIM en el registro de auditoría relacionado con la asignación de roles. Este cambio esperado no debe afectar al flujo de trabajo normal.

 Para obtener más información, vea [Empiece a usar Privileged Identity Management](../privileged-identity-management/pim-getting-started.md).

---

### <a name="azure-ad-entitlement-management-the-select-pane-of-access-package-resources-now-shows-by-default-the-resources-currently-in-the-selected-catalog"></a>Administración de derechos de Azure AD: el panel Seleccionar de los recursos de paquete de acceso muestra ahora de forma predeterminada los recursos contenidos actualmente en el catálogo seleccionado

**Tipo:** Característica modificada  
**Categoría del servicio:** Administración de acceso de usuarios  
**Funcionalidad del producto:** Administración de derechos
 

En el flujo de creación de paquetes de acceso, en la pestaña Roles de recursos, el comportamiento del panel Seleccionar cambia. Actualmente, el comportamiento predeterminado es mostrar todos los recursos que son propiedad del usuario y los recursos agregados al catálogo seleccionado. 

Esta experiencia se modifica para mostrar de forma predeterminada solo los recursos agregados actualmente al catálogo, de modo que los usuarios puedan elegir fácilmente los recursos del catálogo. La actualización ayuda a detectar los recursos que se van a agregar a los paquetes de acceso y reduce el riesgo de agregar de forma accidental los recursos que pertenecen al usuario y que no forman parte del catálogo. Para obtener más información, vea [Creación de un paquete de acceso en la administración de derechos de Azure AD](../governance/entitlement-management-access-package-create.md#resource-roles).
 
---

## <a name="august-2020"></a>Agosto de 2020 
 
### <a name="updates-to-azure-multi-factor-authentication-server-firewall-requirements"></a>Actualizaciones de los requisitos de firewall del Servidor Microsoft Azure Multi-Factor Authentication

**Tipo:** Plan de cambio  
**Categoría del servicio:** MFA  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 
A partir del 1 de octubre de 2020, los requisitos de firewall del Servidor Azure MFA requerirán intervalos IP adicionales.

Si tiene reglas de firewall de salida en la organización, actualícelas para que los servidores MFA puedan comunicarse con todos los intervalos IP necesarios. Los intervalos IP se documentan en [Requisitos de firewall de Servidor Microsoft Azure Multi-Factor Authentication](../authentication/howto-mfaserver-deploy.md#azure-multi-factor-authentication-server-firewall-requirements).

---

### <a name="upcoming-changes-to-user-experience-in-identity-secure-score"></a>Próximos cambios en la experiencia del usuario en Puntuación segura de identidad

**Tipo:** Plan de cambio  
**Categoría del servicio:** **Funcionalidad del producto:** Identity Protection Seguridad y protección de la identidad

Vamos a actualizar el portal de Puntuación segura de identidad para que se corresponda con los cambios introducidos en la [nueva versión](/microsoft-365/security/mtp/microsoft-secure-score-whats-new?view=o365-worldwide) de Puntuación de seguridad de Microsoft. 

La versión preliminar con los cambios estará disponible a principios de septiembre. Los cambios en la versión preliminar incluyen:
- "Puntuación segura de identidad" se ha cambiado a "Puntuación de seguridad de la identidad" a fin de alinear la marca con Puntuación de seguridad de Microsoft.
- Puntos normalizados para la escala estándar que se indican en porcentajes en lugar de con puntos

En esta versión preliminar, los clientes pueden alternar entre la experiencia existente y la nueva. Esta versión preliminar pública durará hasta finales de noviembre de 2020. Después de la versión preliminar, los clientes se dirigirán automáticamente a la nueva experiencia del usuario.

---

### <a name="new-restricted-guest-access-permissions-in-azure-ad---public-preview"></a>Nuevos permisos de acceso de invitado restringido en Azure AD: versión preliminar pública

**Tipo:** Nueva característica  
**Categoría del servicio:** Control de acceso   
**Funcionalidad del producto:** User Management

Hemos actualizado los permisos del nivel de directorio para los usuarios invitados. Estos permisos permiten a los administradores requerir restricciones y controles adicionales en el acceso de los usuarios invitados externos. Los administradores ahora pueden agregar restricciones adicionales para el acceso de los invitados externos a la información de pertenencia y al perfil de los usuarios y los grupos. Con esta característica de la versión preliminar pública, los clientes pueden administrar el acceso de los usuarios externos a escala mediante la ofuscación de las pertenencias a grupos, incluida la restricción de los usuarios invitados para ver la pertenencia de los grupos en los que se encuentran.

Para más información, consulte [Restricción del acceso a usuarios invitados](../enterprise-users/users-restrict-guest-permissions.md) y [Permisos predeterminados de usuario](./users-default-permissions.md).
 
---

### <a name="general-availability-of-delta-queries-for-service-principals"></a>Disponibilidad general de consultas delta para entidades de servicio

**Tipo:** Nueva característica  
**Categoría del servicio:** MS Graph  
**Funcionalidad del producto:** Experiencia para el desarrollador
 
Microsoft Graph Delta Query ahora admite el tipo de recurso en v1.0:
- Entidad de servicio

Ahora los clientes pueden realizar un seguimiento eficaz de los cambios en esos recursos. Proporciona la mejor solución para sincronizar los cambios en esos recursos con un almacén de datos local. Para aprender a configurar estos recursos en una consulta, vea [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).
 
---

### <a name="general-availability-of-delta-queries-for-oauth2permissiongrant"></a>Disponibilidad general de consultas delta para oAuth2PermissionGrant

**Tipo:** Nueva característica  
**Categoría del servicio:** MS Graph  
**Funcionalidad del producto:** Experiencia para el desarrollador

Microsoft Graph Delta Query ahora admite el tipo de recurso en v1.0:
- OAuth2PermissionGrant

Los clientes ahora pueden realizar el seguimiento de los cambios de esos recursos de manera eficaz. Proporciona la mejor solución para sincronizar los cambios en esos recursos con un almacén de datos local. Para aprender a configurar estos recursos en una consulta, vea [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).

---

### <a name="new-federated-apps-available-in-azure-ad-application-gallery---august-2020"></a>Nuevas aplicaciones federadas disponibles en la galería de aplicaciones de Azure AD, agosto de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** Integración de terceros

En agosto de 2020 se han agregado las siguientes 25 aplicaciones nuevas a la galería de aplicaciones con compatibilidad con la federación:

[Backup365](https://portal.backup365.io/login), [Soapbox](https://app.soapboxhq.com/create?step=auth&provider=azure-ad2-oauth2), [Alma SIS](https://almau.getalma.com/), [Enlyft Dynamics 365 Connector](http://enlyft.com/), [Serraview Space Utilization Software Solutions](../saas-apps/serraview-space-utilization-software-solutions-tutorial.md), [Uniq](https://web.uniq.app/), [Visibly](../saas-apps/visibly-tutorial.md), [Zylo](../saas-apps/zylo-tutorial.md), [Edmentum - Courseware Assessments Exact Path](https://auth.edmentum.com/elf/login), [CyberLAB](https://cyberlab.evolvesecurity.com/#/welcome), [Altamira HRM](../saas-apps/altamira-hrm-tutorial.md), [WireWheel](../saas-apps/wirewheel-tutorial.md), [Zix Compliance and Capture](https://sminstall.zixcorp.com/teams/teams.php?install_request=true&tenant_id=common), [Greenlight Enterprise Business Controls Platform](../saas-apps/greenlight-enterprise-business-controls-platform-tutorial.md), [Genetec Clearance](https://www.clearance.network/), [iSAMS](../saas-apps/isams-tutorial.md), [VeraSMART](../saas-apps/verasmart-tutorial.md), [Amiko](https://amiko.web.rivero.app/), [Twingate](https://auth.twingate.com/signup), [Funnel Leasing](https://nestiolistings.com/sso/oidc/azure/authorize/), [Scalefusion](https://scalefusion.com/users/sign_in/), [Bpanda](https://goto.bpanda.com/login), [Vivun Calendar Connect](https://app.vivun.com/dashboard/calendar/connect), [FortiGate SSL VPN](../saas-apps/fortigate-ssl-vpn-tutorial.md), [Wandera End User](https://www.wandera.com/)

La documentación de todas las aplicaciones está disponible en https://aka.ms/AppsTutorial.

Para mostrar su aplicación en la galería de aplicaciones de Azure AD, lea los detalles aquí https://aka.ms/AzureADAppRequest.

---

### <a name="resource-forests-now-available-for-azure-ad-ds"></a>Los bosques de recursos ahora están disponibles para Azure AD DS. 

**Tipo:** **Categoría del servicio:** Nueva característica Azure AD Domain Services   
**Funcionalidad del producto:** Azure AD Domain Services
 
La funcionalidad de los bosques de recursos en Azure AD Domain Services ahora está disponible con carácter general. Ahora puede habilitar la autorización sin sincronización de hash de contraseñas para usar Azure AD Domain Services, incluida la autorización con tarjetas inteligentes. Para más información consulte [Conceptos y características de los conjuntos de réplicas de Azure Active Directory Domain Services (versión preliminar)](../../active-directory-domain-services/concepts-replica-sets.md).
 
---

### <a name="regional-replica-support-for-azure-ad-ds-managed-domains-now-available"></a>Ya está disponible la compatibilidad con la réplica regional para dominios administrados de Azure AD DS.

**Tipo:** Nueva característica   
**Categoría del servicio:** Azure AD Domain Services  
**Funcionalidad del producto:** Azure AD Domain Services
 
Puede ampliar un dominio administrado para que tenga más de un conjunto de réplicas por cada inquilino de Azure AD. Los conjuntos de réplicas pueden agregarse a cualquier red virtual emparejada en cualquier región de Azure que admita Azure AD Domain Services. Contar con conjuntos de réplicas adicionales en diferentes regiones de Azure facilita la recuperación geográfica ante desastres de las aplicaciones heredadas si una región de Azure se queda sin conexión. Para más información consulte [Conceptos y características de los conjuntos de réplicas de Azure Active Directory Domain Services (versión preliminar)](../../active-directory-domain-services/concepts-replica-sets.md).

---

### <a name="general-availability-of-azure-ad-my-sign-ins"></a>Disponibilidad general de Mis inicios de sesión de Azure AD

**Tipo:** Nueva característica  
**Categoría del servicio:** Autenticaciones (inicios de sesión)  
**Funcionalidad del producto:** Experiencias de usuario final
 
Mis inicios de sesión de Azure AD es una característica nueva que permite a los usuarios empresariales revisar su historial de inicios de sesión para comprobar si hay alguna actividad inusual. Además, esta característica posibilita a los usuarios finales comunicar si fueron o no los causantes de actividades sospechosas. Para más información sobre el uso de esta característica, consulte [Visualización de las actividades de inicio de sesión recientes](../user-help/my-account-portal-sign-ins-page.md#confirm-unusual-activity).
 
---

### <a name="sap-successfactors-hr-driven-user-provisioning-to-azure-ad-is-now-generally-available"></a>El aprovisionamiento de usuarios controlado por SuccessFactors HR de SAP para Azure AD ya está disponible con carácter general

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
Ahora puede integrar SAP SuccessFactors como el origen de identidad de autoridad con Azure AD y automatizar el ciclo de vida de identidad de un extremo a otro mediante eventos de RR. HH. como nuevas contrataciones y conclusión de contratos para impulsar el aprovisionamiento y el desaprovisionamiento de las cuentas en Azure AD. 

Para más información sobre cómo configurar el aprovisionamiento de entrada de SAP SuccessFactors para Azure AD, consulte el tutorial [Configuración del aprovisionamiento de usuarios de SAP SuccessFactors a Active Directory](../saas-apps/sap-successfactors-inbound-provisioning-tutorial.md).
 
---

### <a name="custom-open-id-connect-ms-graph-api-support-for-azure-ad-b2c"></a>Compatibilidad con Open ID Connect personalizado de MS Graph API para Azure AD B2C

**Tipo:** Nueva característica  
**Categoría del servicio:** B2C: administración de identidades de consumidor  
**Funcionalidad del producto:** B2B/B2C
 
Anteriormente, los proveedores personalizados de Open ID Connect solo se podían agregar o administrar mediante Azure Portal. Ahora, los clientes de Azure AD B2C pueden agregarlos y administrarlos con la versión beta de Microsoft Graph API. Para obtener información sobre cómo configurar este recurso con las API, consulte [Tipo de recurso identityProvider](/graph/api/resources/identityprovider?view=graph-rest-beta).
 
---

### <a name="assign-azure-ad-built-in-roles-to-cloud-groups"></a>Asignación de roles integrados de Azure AD a grupos en la nube

**Tipo:** Nueva característica  
**Categoría del servicio:** Roles de Azure AD  
**Funcionalidad del producto:** Control de acceso

Ahora puede asignar roles integrados de Azure AD a grupos en la nube con esta nueva característica. Por ejemplo, puede asignar el rol Administrador de SharePoint al grupo Contoso_SharePoint_Admins. También puede usar PIM para convertir el grupo en miembro del rol, en lugar de conceder acceso permanente. Para obtener información sobre cómo configurar esta característica, consulte [Uso de grupos en la nube para administrar asignaciones de roles en Azure Active Directory (versión preliminar)](../roles/groups-concept.md).
 
---

### <a name="insights-business-leader-built-in-role-now-available"></a>Ya está disponible el rol integrado Coordinador de Insights de la empresa.

**Tipo:** Nueva característica  
**Categoría del servicio:** Roles de Azure AD  
**Funcionalidad del producto:** Control de acceso
 
Los usuarios con el rol Coordinador de Insights de la empresa pueden acceder a un conjunto de paneles y conclusiones a través de la [aplicación M365 Insights](https://www.microsoft.com/microsoft-365/partners/workplaceanalytics). Esto incluye el acceso completo a todos los paneles y la funcionalidad de exploración de datos y conclusiones presentadas. Sin embargo, los usuarios con este rol no tienen acceso a las opciones de configuración del producto, que es responsabilidad del rol Administrador de Insights. Para más información acerca de este rol, consulte [Permisos de roles de administrador en Azure Active Directory](../roles/permissions-reference.md#insights-business-leader).
 
---

### <a name="insights-administrator-built-in-role-now-available"></a>El rol integrado Administrador de Insights ya está disponible.

**Tipo:** Nueva característica  
**Categoría del servicio:** Roles de Azure AD  
**Funcionalidad del producto:** Control de acceso
 
Los usuarios con el rol Administrador de Insights pueden tener acceso al conjunto completo de funcionalidades administrativas de la [aplicación M365 Insights](https://www.microsoft.com/microsoft-365/partners/workplaceanalytics). Un usuario con este rol puede leer información de directorios, supervisar el mantenimiento del servicio, presentar vales de soporte técnico y acceder a los aspectos de configuración del administrador de Insights. Para más información sobre este rol, consulte [Permisos de roles de administrador en Azure Active Directory](../roles/permissions-reference.md#insights-administrator).
 
--- 

### <a name="application-admin-and-cloud-application-admin-can-manage-extension-properties-of-applications"></a>El administrador de aplicaciones y el administrador de aplicaciones en la nube pueden administrar las propiedades de extensión de las aplicaciones.

**Tipo:** Característica modificada  
**Categoría del servicio:** Roles de Azure AD  
**Funcionalidad del producto:** Control de acceso
 
Anteriormente, solo el administrador global podía administrar la [propiedad de extensión](/graph/api/application-post-extensionproperty?view=graph-rest-beta&tabs=http). Ahora vamos a habilitar esta funcionalidad para el administrador de la aplicación y también para el administrador de aplicaciones en la nube.
 
---

### <a name="mim-2016-sp2-hotfix-462630-and-connectors-1113010"></a>Revisión 4.6.263.0 de MIM 2016 SP2 y conectores 1.1.1301.0

**Tipo:** Característica modificada  
**Categoría del servicio:** Microsoft Identity Manager  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad

Un [paquete acumulativo de revisiones (compilación 4.6.263.0)](https://support.microsoft.com/help/4576473/hotfix-rollup-package-build-4-6-263-0-is-available-for-microsoft-ident) está disponible para Microsoft Identity Manager (MIM) 2016 Service Pack 2 (SP2). Este paquete acumulativo contiene actualizaciones para los componentes de PAM, MIM CM y el administrador de sincronización de MIM. Además, la compilación de conectores genéricos de MIM 1.1.1301.0 incluye actualizaciones para el conector de Graph.

---
 
## <a name="july-2020"></a>Julio de 2020

### <a name="as-an-it-admin-i-want-to-target-client-apps-using-conditional-access"></a>Como administrador de TI, quiero dirigirme a las aplicaciones cliente mediante el acceso condicional

**Tipo:** Plan de cambio   
**Categoría del servicio:** Acceso condicional  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 
Con la versión de disponibilidad general (GA) de la condición de las aplicaciones de cliente en el acceso condicional, ahora las nuevas directivas se aplicarán de manera predeterminada a todas las aplicaciones cliente. Esto incluye los clientes de autenticación heredados. Las directivas existentes permanecerán sin cambios, pero la opción de alternancia *Configurar sí/no* se quitará de las directivas existentes para ver fácilmente las aplicaciones cliente que se aplican a través de la directiva. 

Al crear una nueva directiva, asegúrese de excluir los usuarios y las cuentas de servicio que siguen usando la autenticación heredada. Si no lo hace, se bloquearán. [Más información](../conditional-access/concept-conditional-access-conditions.md).
 
---

### <a name="upcoming-scim-compliance-fixes"></a>Próximas correcciones de cumplimiento de SCIM

**Tipo:** Plan de cambio  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
El servicio de aprovisionamiento de Azure AD aprovecha el estándar SCIM para la integración con las aplicaciones. Nuestra implementación del estándar SCIM está evolucionando y esperamos realizar cambios en nuestro comportamiento en torno a la realización de las operaciones de revisión, así como al establecimiento de la propiedad "activa" en un recurso. [Más información](../app-provisioning/application-provisioning-config-problem-scim-compatibility.md).
 
---

### <a name="group-owner-setting-on-azure-admin-portal-will-be-changed"></a>Se cambiará la configuración del propietario del grupo en el portal de administración de Azure

**Tipo:** Plan de cambio  
**Categoría del servicio:** Administración de grupos  
**Funcionalidad del producto:** Colaboración

La configuración del propietario en la página de configuración de grupos general puede configurarse para restringir los privilegios de asignación de propietario a un grupo limitado de usuarios en el Panel de acceso y el portal de administración de Azure. Pronto tendremos la capacidad de asignar privilegios de propietario de grupo no solo en estos dos portales de la experiencia de usuario, sino también aplicar la directiva en el back-end para proporcionar un comportamiento coherente entre los puntos de conexión, como PowerShell y Microsoft Graph. 

Comenzaremos a deshabilitar la configuración actual de los clientes que no la estén usando y ofreceremos una opción para el ámbito de los usuarios de privilegios de propietario de grupo en los próximos meses. Para obtener instrucciones sobre la actualización de la configuración de grupo, consulte la edición de la información de grupo mediante [Azure Active Directory](./active-directory-groups-settings-azure-portal.md?context=azure%2factive-directory%2fusers-groups-roles%2fcontext%2fugr-context).

---

### <a name="azure-active-directory-registration-service-is-ending-support-for-tls-10-and-11"></a>El servicio de registro de Azure Active Directory va a finalizar la compatibilidad con TLS 1.0 y 1.1

**Tipo:** Plan de cambio  
**Categoría del servicio:** Administración y registro de dispositivos  
**Funcionalidad del producto:** plataforma

La Seguridad de la capa de transporte (TLS) 1.2 y los servidores y clientes de actualización se comunicarán pronto con el servicio Registro de dispositivos de Azure Active Directory. La compatibilidad con TLS 1.0 y 1.1 para la comunicación con el servicio Registro de dispositivos de Azure AD se retirará:
- El 31 de agosto de 2020, en todas las nubes independientes (GCC High, DoD, etc.).
- El 30 de octubre de 2020, en todas las nubes comerciales.

[Más información](../devices/reference-device-registration-tls-1-2.md) sobre TLS 1.2 para el servicio de registro de Azure AD.

---

### <a name="windows-hello-for-business-sign-ins-visible-in-azure-ad-sign-in-logs"></a>Inicios de sesión de Windows Hello para empresas visibles en registros de inicio de sesión de Azure AD

**Tipo:** Corregido  
**Categoría del servicio:** Notificación  
**Funcionalidad del producto:** Supervisión e informes
 
Windows Hello para empresas permite a los usuarios finales iniciar sesión en máquinas Windows con un gesto (como un PIN o datos biométricos). Los administradores de Azure AD pueden querer diferenciar los inicios de sesión de Windows Hello para empresas de otros inicios de sesión de Windows como parte del recorrido de una organización para la autenticación sin contraseña. 

Los administradores ya pueden ver si una autenticación de Windows ha usado Windows Hello para empresas mediante la comprobación de la pestaña Detalles de autenticación de un evento de inicio de sesión de Windows en la hoja Inicios de sesión de Azure AD en Azure Portal. Las autenticaciones de Windows Hello para empresas incluirán "WindowsHelloForBusiness" en el campo Método de autenticación. Para obtener más información sobre cómo interpretar los registros de inicio de sesión, consulte la [documentación de registros de inicio de sesión](../reports-monitoring/concept-sign-ins.md).
 
---

### <a name="fixes-to-group-deletion-behavior-and-performance-improvements"></a>Correcciones del comportamiento de eliminación de grupos y mejoras de rendimiento

**Tipo:** Corregido  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
Anteriormente, cuando un grupo cambiaba de "en el ámbito" a "fuera de ámbito" y un administrador hacía clic en reiniciar antes de que se completara el cambio, el objeto de grupo no se eliminaba. Ahora, el objeto de grupo de la aplicación de destino se eliminará cuando salga del ámbito (deshabilitado, eliminado, sin asignar o sin pasar el filtro de ámbito). [Más información](../app-provisioning/how-provisioning-works.md#incremental-cycles).
 
---

### <a name="public-preview-admins-can-now-add-custom-content-in-the-email-to-reviewers-when-creating-an-access-review"></a>Versión preliminar pública: los administradores ya pueden agregar contenido personalizado en el correo electrónico para los revisores al crear una revisión de acceso.

**Tipo:** Nueva característica  
**Categoría del servicio:** Revisiones de acceso  
**Funcionalidad del producto:** Identity Governance
 
Cuando se crea una nueva revisión de acceso, el revisor recibe un correo electrónico que le solicita que complete la revisión de acceso. Muchos de nuestros clientes han solicitado la posibilidad de agregar contenido personalizado al correo electrónico, como información de contacto, u otro contenido adicional de soporte técnico para guiar al revisor. 

Ya disponible en la versión preliminar pública, los administradores pueden especificar contenido personalizado en el correo electrónico que se envía a los revisores mediante la adición de contenido en la sección "Opciones avanzadas" de las revisiones de acceso de Azure AD. Para obtener instrucciones sobre cómo crear revisiones de acceso, consulte [Creación de una revisión de acceso de los grupos y las aplicaciones en las revisiones de acceso de Azure AD](../governance/create-access-review.md).
 
---

### <a name="authorization-code-flow-for-single-page-apps-available"></a>Flujo de código de autorización para aplicaciones de una sola página disponibles

**Tipo:** Nueva característica  
**Categoría del servicio:** Autenticaciones (inicios de sesión)  
**Funcionalidad del producto:** Experiencia para el desarrollador
 
Debido a las restricciones de cookies de terceros como Safari ITP aplicadas en el explorador, las aplicaciones de página única (SPA) tendrán que usar el flujo de código de autorización en lugar del flujo implícito para mantener el SSO. MSAL.js v2.x admite ahora el flujo de código de autorización. 

Las actualizaciones correspondientes están disponibles en Azure Portal. De este modo, podrá actualizar sus aplicaciones de página única para que sean del tipo "spa" y utilicen el flujo de código de autenticación. Consulte [Inicio de sesión de los usuarios y obtención de un token de acceso en una SPA de JavaScript mediante el flujo de código de autorización](../develop/quickstart-v2-javascript-auth-code.md) para obtener más instrucciones.
 
---

### <a name="azure-ad-application-proxy-now-supports-the-remote-desktop-services-web-client"></a>Azure AD Application Proxy ya admite el cliente web de Servicios de Escritorio remoto

**Tipo:** Nueva característica  
**Categoría del servicio:** Proxy de aplicaciones  
**Funcionalidad del producto:** Control de acceso

Azure AD Application Proxy ya admite el cliente web de Servicios de Escritorio remoto (RDS). El cliente web de RDS permite a los usuarios tener acceso a la infraestructura de Escritorio remoto a través de cualquier explorador compatible con HTLM5, como Microsoft Edge, Internet Explorer 11, Google Chrome, etc. Los usuarios pueden interactuar con escritorios o aplicaciones remotos como lo harían con un dispositivo local desde cualquier lugar. Mediante el uso de Azure AD Application Proxy, puede aumentar la seguridad de la implementación de RDS mediante la exigencia de directivas de acceso condicional y autenticación previa para todos los tipos de aplicaciones cliente enriquecidas. Para obtener instrucciones, consulte [Publicación de Escritorio Remoto con Azure AD Application Proxy](../manage-apps/application-proxy-integrate-with-remote-desktop-services.md).
 
---

### <a name="next-generation-azure-ad-b2c-user-flows-in-public-preview"></a>Flujos de usuario de última generación de Azure AD B2C en versión preliminar pública

**Tipo:** Nueva característica  
**Categoría del servicio:** B2C: administración de identidades de consumidor  
**Funcionalidad del producto:** B2B/B2C
 
La experiencia simplificada de flujo de usuario ofrece paridad de características con características en vista previa (GB) y es donde se encuentran todas las características nuevas. Los usuarios podrán habilitar nuevas características en el mismo flujo de usuario, lo que reduce la necesidad de crear varias versiones con cada nueva versión de actualización de características. Por último, la nueva experiencia de usuario fácil de usar simplifica la selección y creación de flujos de usuario. Para probarla, [cree un flujo de usuario](../../active-directory-b2c/tutorial-create-user-flows.md). 

Para más información sobre los flujos de usuario, consulte [Versiones de flujos de usuario de Azure Active Directory B2C](../../active-directory-b2c/user-flow-versions.md#:~:text=    User flow  ,account. Usi ...  1 more rows ).

---

### <a name="new-federated-apps-available-in-azure-ad-application-gallery---july-2020"></a>Nuevas aplicaciones federadas disponibles en la galería de aplicaciones de Azure AD, julio de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** Integración de terceros
 
En julio de 2020, agregamos 55 aplicaciones nuevas a la galería de aplicaciones con compatibilidad de federación:

[Clap Your Hands](http://www.rmit.com.ar/), [Appreiz](https://microsoftteams.appreiz.com/), [Inextor Vault](https://inexto.com/inexto-suite/inextor), [Beekast](https://my.beekast.com/), [Templafy OpenID Connect](https://app.templafy.com/), [PeterConnects receptionist](https://msteams.peterconnects.com/), [AlohaCloud](https://appfusions.alohacloud.com/auth), [Control Tower](https://bpm.tnxcorp.com/sso/microsoft), [Cocoom](https://start.cocoom.com/), [COINS Construction Cloud](https://sso.coinsconstructioncloud.com/#login/), [Medxnote MT](https://task.teamsmain.medx.im/authorization), [Reflekt](https://reflekt.konsolute.com/login), [Rever](https://app.reverscore.net/access), [MyCompanyArchive](https://login.mycompanyarchive.com/), [GReminders](https://app.greminders.com/o365-oauth), [Titanfile](../saas-apps/titanfile-tutorial.md), [Wootric](../saas-apps/wootric-tutorial.md), [SolarWinds Orion](https://support.solarwinds.com/SuccessCenter/s/orion-platform?language=en_US),  [OpenText Directory Services](../saas-apps/opentext-directory-services-tutorial.md), [Datasite](../saas-apps/datasite-tutorial.md), [BlogIn](../saas-apps/blogin-tutorial.md), [IntSights](../saas-apps/intsights-tutorial.md), [kpifire](../saas-apps/kpifire-tutorial.md), [Textline](../saas-apps/textline-tutorial.md), [Cloud Academy - SSO](../saas-apps/cloud-academy-sso-tutorial.md), [Community Spark](../saas-apps/community-spark-tutorial.md), [Chatwork](../saas-apps/chatwork-tutorial.md), [CloudSign](../saas-apps/cloudsign-tutorial.md), [C3M Cloud Control](../saas-apps/c3m-cloud-control-tutorial.md), [SmartHR](https://smarthr.jp/), [NumlyEngage™](../saas-apps/numlyengage-tutorial.md), [Michigan Data Hub Single Sign-On](../saas-apps/michigan-data-hub-single-sign-on-tutorial.md), [Egress](../saas-apps/egress-tutorial.md), [SendSafely](../saas-apps/sendsafely-tutorial.md), [Eletive](https://app.eletive.com/), [Right-Hand Cybersecurity ADI](https://right-hand.ai/), [Fyde Enterprise Authentication](https://enterprise.fyde.com/), [Verme](../saas-apps/verme-tutorial.md), [Lenses.io](../saas-apps/lensesio-tutorial.md), [Momenta](../saas-apps/momenta-tutorial.md), [Uprise](https://app.uprise.co/sign-in), [Q](https://q.moduleq.com/login), [CloudCords](../saas-apps/cloudcords-tutorial.md), [TellMe Bot](https://tellme365liteweb.azurewebsites.net/), [Inspire](https://app.inspiresoftware.com/), [Maverics Identity Orchestrator SAML Connector](https://www.strata.io/identity-fabric/), [Smartschool (School Management System)](https://smartschoolz.com/login), [Zepto - Intelligent timekeeping](https://user.zepto-ai.com/signin), [Studi.ly](https://studi.ly/), [Trackplan](http://www.trackplanfm.com/), [Skedda](../saas-apps/skedda-tutorial.md), [WhosOnLocation](../saas-apps/whos-on-location-tutorial.md), [Coggle](../saas-apps/coggle-tutorial.md), [Kemp LoadMaster](https://kemptechnologies.com/cloud-load-balancer/), [BrowserStack Single Sign-on](../saas-apps/browserstack-single-sign-on-tutorial.md)

La documentación de todas las aplicaciones está disponible en https://aka.ms/AppsTutorial.

Para mostrar su aplicación en la galería de aplicaciones de Azure AD, lea los detalles aquí: https://aka.ms/AzureADAppRequest.

---

### <a name="new-provisioning-connectors-in-the-azure-ad-application-gallery---july-2020"></a>Nuevos conectores de aprovisionamiento disponibles en la galería de aplicaciones de Azure AD, julio de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Integración de terceros

Ahora, puede automatizar la creación, actualización y eliminación de cuentas de usuario para la aplicación recién integrada [LinkedIn Learning](../saas-apps/linkedin-learning-provisioning-tutorial.md).

Para más información acerca de cómo proteger mejor una organización mediante el aprovisionamiento automatizado de cuentas de usuario, consulte [Automatización del aprovisionamiento y desaprovisionamiento de usuarios para aplicaciones SaaS con Azure Active Directory](../app-provisioning/user-provisioning.md).

---

### <a name="view-role-assignments-across-all-scopes-and-ability-to-download-them-to-a-csv-file"></a>Visualización de las asignaciones de roles en todos los ámbitos y capacidad de descargarlas en un archivo CSV

**Tipo:** Característica modificada  
**Categoría del servicio:** Roles de Azure AD  
**Funcionalidad del producto:** Control de acceso
 
Ahora puede ver las asignaciones de roles en todos los ámbitos de un rol en la pestaña "Roles y administradores" en el portal de Azure AD. También puede descargar estas asignaciones de roles para cada rol en un archivo CSV. Para obtener instrucciones sobre cómo ver y agregar asignaciones de roles, consulte [Visualización y asignación de roles de administrador en Azure Active Directory](../roles/manage-roles-portal.md).
 
---

### <a name="azure-multi-factor-authentication-software-development-azure-mfa-sdk-deprecation"></a>Desuso del desarrollo de software de Azure Multi-Factor Authentication (SDK de Azure MFA)

**Tipo:** Obsoleto  
**Categoría del servicio:** MFA  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 
El desarrollo de software de Azure Multi-Factor Authentication (SDK de Azure MFA) alcanzó el final del ciclo de vida el 14 de noviembre de 2018, como se anunció por primera vez en noviembre de 2017. Microsoft apagará el servicio de SDK a partir del 30 de septiembre de 2020. Se producirá un error en todas las llamadas realizadas al SDK.

Si su organización usa el SDK de Azure MFA, debe realizar la migración antes del 30 de septiembre de 2020:
- SDK de Azure MFA para MIM:  Si usa el SDK con MIM, debe migrar al Servidor Azure MFA y activar Privileged Access Management (PAM) siguiendo estas [instrucciones](/microsoft-identity-manager/working-with-mfaserver-for-mim).   
- SDK de Azure MFA para aplicaciones personalizadas: Considere la posibilidad de integrar la aplicación en Azure AD y usar el acceso condicional para aplicar MFA. Para empezar, revise esta [página](../manage-apps/plan-an-application-integration.md). 

---

## <a name="june-2020"></a>Junio de 2020 

### <a name="user-risk-condition-in-conditional-access-policy"></a>Condición de riesgo de usuario de la directiva de acceso condicional

**Tipo:** Plan de cambio  
**Categoría del servicio:** Acceso condicional  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 

La compatibilidad con el riesgo de usuario en la directiva de acceso condicional de Azure AD permite crear varias directivas basadas en el riesgo de usuario. Pueden requerirse diferentes niveles de riesgo de usuario mínimo para diferentes usuarios y aplicaciones. En función del riesgo de usuario, puede crear directivas para bloquear el acceso, requerir la autenticación multifactor, proteger el cambio de contraseña o redirigir a Microsoft Cloud App Security para aplicar la directiva de sesión, como la auditoría adicional.

La condición de riesgo de usuario requiere Azure AD Premium P2 porque usa Azure Identity Protection, que es una oferta P2. Para más información sobre el acceso condicional, vea la [documentación sobre el acceso condicional de Azure AD](../conditional-access/index.yml).

---

### <a name="saml-sso-now-supports-apps-that-require-spnamequalifier-to-be-set-when-requested"></a>SSO de SAML admite ahora aplicaciones que requieren establecer SPNameQualifier cuando se solicite

**Tipo:** Corregido  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** SSO
 
Algunas aplicaciones de SAML requieren que se devuelva SPNameQualifier en el sujeto de la aserción cuando se solicita. Ahora Azure AD responde correctamente cuando se solicita un SPNameQualifier en la directiva de NameID de la solicitud. Esto también funciona para el inicio de sesión iniciado por el SP y se seguirá el inicio de sesión iniciado por IdP.  Para más información sobre el protocolo de SAML en Azure Active Directory, vea [Protocolo SAML de inicio de sesión único](../develop/single-sign-on-saml-protocol.md).

---

### <a name="azure-ad-b2b-collaboration-supports-inviting-msa-and-google-users-in-azure-government-tenants"></a>La colaboración B2B de Azure AD permite invitar a los usuarios de MSA y Google en inquilinos de Azure Government

**Tipo:** Nueva característica  
**Categoría del servicio:** B2B  
**Funcionalidad del producto:** B2B/B2C
 

Los inquilinos de Azure Government que usan las características de colaboración B2B ahora pueden invitar a los usuarios que tienen una cuenta de Microsoft o Google. Para averiguar si su inquilino puede usar estas funcionalidades, siga las instrucciones que se indican en [¿Cómo puedo saber si la colaboración B2B está disponible en mi inquilino de Azure US Government?](../external-identities/current-limitations.md#how-can-i-tell-if-b2b-collaboration-is-available-in-my-azure-us-government-tenant)

 
---
 
### <a name="user-object-in-ms-graph-v1-now-includes-externaluserstate-and-externaluserstatechangeddatetime-properties"></a>El objeto de usuario de MS Graph v1 ahora incluye las propiedades externalUserState y externalUserStateChangedDateTime

**Tipo:** Nueva característica  
**Categoría del servicio:** B2B  
**Funcionalidad del producto:** B2B/B2C
 

Las propiedades externalUserState y externalUserStateChangedDateTime se pueden usar para buscar invitados B2B que aún no han aceptado sus invitaciones, así como para crear automatización, como la eliminación de usuarios que no han aceptado sus invitaciones después de un número determinado de días. Estas propiedades están ahora disponibles en MS Graph v1. Para obtener instrucciones sobre el uso de estas propiedades, consulte [Tipo de recurso del usuario](/graph/api/resources/user?view=graph-rest-1.0).
 
---

### <a name="manage-authentication-sessions-in-azure-ad-conditional-access-is-now-generally-available"></a>La administración de sesiones de autenticación en el acceso condicional de Azure AD ya está disponible con carácter general

**Tipo:** Nueva característica  
**Categoría del servicio:** Acceso condicional  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 
Las funcionalidades de administración de sesiones de autenticación permiten configurar la frecuencia con que los usuarios necesitan proporcionar credenciales de inicio de sesión y si necesitan proporcionar credenciales después de cerrar y volver a abrir los exploradores para ofrecer más seguridad y flexibilidad en el entorno.
 
Además, la administración de sesiones de autenticación se aplicaba solo a la autenticación del primer factor en los dispositivos unidos a Azure AD, unidos a Azure AD híbrido y registrados en Azure AD. Ahora la administración de sesiones de autenticación también se aplicará a MFA. Para más información, vea [Configuración de la administración de las sesiones de autenticación con el acceso condicional](../conditional-access/howto-conditional-access-session-lifetime.md).

---

### <a name="new-federated-apps-available-in-azure-ad-application-gallery---june-2020"></a>Nuevas aplicaciones federadas disponibles en la galería de aplicaciones de Azure AD, junio de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** Integración de terceros
 
En junio de 2020, hemos agregado 29 nuevas aplicaciones a la galería de aplicaciones con compatibilidad de federación:

[Shopify Plus](../saas-apps/shopify-plus-tutorial.md), [Ekarda](../saas-apps/ekarda-tutorial.md), [MailGates](../saas-apps/mailgates-tutorial.md), [BullseyeTDP](../saas-apps/bullseyetdp-tutorial.md), [Raketa](../saas-apps/raketa-tutorial.md), [Segment](../saas-apps/segment-tutorial.md), [Ai Auditor](https://www.mindbridge.ai/products/ai-auditor/), [Pobuca Connect](https://app.pobu.ca/), [Proto.io](../saas-apps/proto.io-tutorial.md), [Gatekeeper](https://www.gatekeeperhq.com/), [Hub Planner](../saas-apps/hub-planner-tutorial.md), [Ansira-Partner Go-to-Market Toolbox](https://ansira.com/technology/channel-engagement), [IBM Digital Business Automation on Cloud](../saas-apps/ibm-digital-business-automation-on-cloud-tutorial.md), [Kisi Physical Security](../saas-apps/kisi-physical-security-tutorial.md), [ViewpointOne](https://team.viewpoint.com/), [IntelligenceBank](../saas-apps/intelligencebank-tutorial.md), [pymetrics](../saas-apps/pymetrics-tutorial.md), [Zero](https://www.teamzero.com/), [InStation](https://instation.invillia.com/), [edX for Business SAML 2.0 Integration](../saas-apps/edx-for-business-saml-integration-tutorial.md), [MOOC Office 365](https://mooc.office365-training.com/en/), [SmartKargo](../saas-apps/smartkargo-tutorial.md), [PKIsigning platform](https://platform.pkisigning.nl/), [SiteIntel](../saas-apps/siteintel-tutorial.md), [Field iD](../saas-apps/field-id-tutorial.md), [Curricula SAML](../saas-apps/curricula-saml-tutorial.md), [Perforce Helix Core - Helix Authentication Service](../saas-apps/perforce-helix-core-tutorial.md), [MyCompliance Cloud](https://cloud.metacompliance.com/) y [Smallstep SSH](https://smallstep.com/sso-ssh/)  

La documentación de todas las aplicaciones está disponible aquí: https://aka.ms/AppsTutorial Para mostrar su aplicación en la galería de aplicaciones Azure AD, lea los detalles aquí: https://aka.ms/AzureADAppRequest.

---

### <a name="api-connectors-for-external-identities-self-service-sign-up-are-now-in-public-preview"></a>Los conectores de API para el registro de autoservicio de identidades externas ya está disponible en versión preliminar pública

**Tipo:** Nueva característica  
**Categoría del servicio:** B2B  
**Funcionalidad del producto:** B2B/B2C
 
Los conectores de API para identidades externas permiten utilizar las API web para integrar el registro de autoservicio con sistemas en la nube externos. Esto significa que ahora puede invocar las API web como pasos específicos en un flujo de registro para desencadenar flujos de trabajo personalizados basados en la nube. Por ejemplo, puede usar conectores de API para:

- Integrarse con un flujo de trabajo de aprobación personalizado.
- Realizar correcciones de identidad
- Validar los datos de entrada del usuario
- Sobrescribir atributos de usuario
- Ejecutar una lógica de negocios personalizada

Para más información sobre todas las experiencias posibles con los conectores de API, vea [Uso de conectores de API para personalizar y extender el registro de autoservicio](../external-identities/api-connectors-overview.md) o [Personalización del registro de autoservicio de las identidades externas con las integraciones de API web](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/customize-external-identities-self-service-sign-up-with-web-api/ba-p/1257364#.XvNz2fImuQg.linkedin).
 
---

### <a name="provision-on-demand-and-get-users-into-your-apps-in-seconds"></a>Aprovisionamiento a petición e integración de usuarios en las aplicaciones en cuestión de segundos

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
El servicio de aprovisionamiento de Azure AD actualmente funciona de forma cíclica. El servicio se ejecuta cada 40 minutos. La [funcionalidad de aprovisionamiento a petición](https://aka.ms/provisionondemand) permite elegir un usuario y aprovisionarlo en segundos. Esta funcionalidad permite solucionar problemas de aprovisionamiento rápidamente, sin tener que reiniciar para forzar el inicio del ciclo de aprovisionamiento. 
 
---

### <a name="new-permission-for-using-azure-ad-entitlement-management-in-graph"></a>Nuevo permiso para usar la administración de derechos de Azure AD en Graph

**Tipo:** Nueva característica  
**Categoría del servicio:** Otros  
**Funcionalidad del producto:** Administración de derechos
 
Un nuevo permiso delegado EntitlementManagement.Read.All ahora está disponible para su uso con la API de administración de derechos en la versión beta de Microsoft Graph. Para obtener más información sobre las API disponibles, vea [Trabajar con la API de administración de derechos de Azure AD](/graph/api/resources/entitlementmanagement-root?view=graph-rest-beta).

---

### <a name="identity-protection-apis-available-in-v10"></a>API de Identity Protection disponibles en la versión 1.0

**Tipo:** Nueva característica  
**Categoría del servicio:** Protección de identidad  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 
Las API riskyUsers y riskDetections de Microsoft Graph ahora están disponibles con carácter general. Ahora que están disponibles en el punto de conexión v 1.0, lo invitamos a utilizarlos en producción. Para más información, vea la [documentación de Microsoft Graph](/graph/api/resources/identityprotectionroot?view=graph-rest-1.0).
 
---

### <a name="sensitivity-labels-to-apply-policies-to-microsoft-365-groups-is-now-generally-available"></a>Las etiquetas de confidencialidad para aplicar directivas a grupos de Microsoft 365 ya están disponibles con carácter general

**Tipo:** Nueva característica  
**Categoría del servicio:** Administración de grupos  
**Funcionalidad del producto:** Colaboración
 

Ahora puede crear etiquetas de confidencialidad y usar la configuración de la etiqueta para aplicar directivas a grupos de Microsoft 365, incluida la directiva de privacidad (pública o privada) y la directiva de acceso de usuarios externos. Puede crear una etiqueta con la directiva de privacidad para que sea privada y con la directiva de acceso de usuarios externos para no permitir que se agreguen usuarios invitados. Cuando un usuario aplica esta etiqueta a un grupo, este será privado y no se permitirá agregar usuarios invitados al grupo. 

Las etiquetas de confidencialidad son importantes para proteger los datos críticos para la empresa y permiten administrar grupos a escala, de manera compatible y segura. Para obtener orientación sobre el uso de etiquetas de confidencialidad, vea [Asignación de etiquetas de confidencialidad a grupos de Microsoft 365 en Azure Active Directory (versión preliminar)](../enterprise-users/groups-assign-sensitivity-labels.md).
 
---

### <a name="updates-to-support-for-microsoft-identity-manager-for-azure-ad-premium-customers"></a>Actualizaciones de compatibilidad con Microsoft Identity Manager para clientes de Azure AD Premium

**Tipo:** Característica modificada  
**Categoría del servicio:** Microsoft Identity Manager  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
El Soporte técnico de Azure ya está disponible para los componentes de integración de Azure AD de Microsoft Identity Manager 2016, hasta el final del soporte extendido para Microsoft Identity Manager 2016. Para más información, vea [Actualización de soporte técnico para clientes de Azure AD Premium que usan Microsoft Identity Manager](/microsoft-identity-manager/support-update-for-azure-active-directory-premium-customers).

---

### <a name="the-use-of-group-membership-conditions-in-sso-claims-configuration-is-increased"></a>Aumento del uso de condiciones de pertenencia a grupos en la configuración de notificaciones de SSO

**Tipo:** Característica modificada  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** SSO
 
Anteriormente, el número de grupos que podía usar al cambiar condicionalmente las notificaciones basadas en la pertenencia a grupos dentro de cualquier configuración de aplicación única estaba limitado a 10. El uso de las condiciones de pertenencia a grupos en la configuración de notificaciones de SSO ahora se ha aumentado a un máximo de 50 grupos. Para más información sobre cómo configurar las notificaciones, vea [Configuración de notificaciones de SSO en aplicaciones empresariales](../develop/active-directory-saml-claims-customization.md#emitting-claims-based-on-conditions). 

---

### <a name="enabling-basic-formatting-on-the-sign-in-page-text-component-in-company-branding"></a>Habilitar el formato básico en el componente de texto de la página de inicio de sesión para la personalización de marca de empresas

**Tipo:** Característica modificada  
**Categoría del servicio:** Autenticaciones (inicios de sesión)  
**Funcionalidad del producto:** Autenticación de usuarios
 
La funcionalidad de personalización de marca de la empresa en la experiencia de inicio de sesión de Azure AD/Microsoft 365 se ha actualizado para que el cliente pueda agregar hipervínculos y formatos sencillos, como negrita, subrayado y cursiva. Para obtener orientación sobre el uso de esta funcionalidad, vea [Incorporación de la personalización de marca en la página de inicio de sesión de Azure Active Directory de la organización](./customize-branding.md).

---

### <a name="provisioning-performance-improvements"></a>Mejoras en el rendimiento de aprovisionamiento

**Tipo:** Característica modificada  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
El servicio de aprovisionamiento se ha actualizado para reducir el tiempo que tarda un [ciclo incremental](../app-provisioning/how-provisioning-works.md#incremental-cycles) en completarse. Esto significa que los usuarios y grupos se aprovisionarán en sus aplicaciones más rápido que antes. Todos los nuevos trabajos de aprovisionamiento creados después del 10/6/2020 se beneficiarán automáticamente de las mejoras de rendimiento. Las aplicaciones configuradas para el aprovisionamiento antes del 10/6/2020 deberán reiniciarse una vez después del 10/6/2020 para beneficiarse de las mejoras de rendimiento. 

---

### <a name="announcing-the-deprecation-of-adal-and-ms-graph-parity"></a>Anuncio de desuso de la paridad de ADAL y MS Graph

**Tipo:** Obsoleto  
**Categoría del servicio:** N/D  
**Funcionalidad del producto:** Administración del ciclo de vida de dispositivos

Ahora que las bibliotecas de autenticación de Microsoft (MSAL) están disponibles, ya no se agregarán nuevas características a las bibliotecas de autenticación de Azure Active Directory (ADAL) y las revisiones de seguridad finalizarán el 30 de junio de 2022. Para más información sobre cómo migrar a MSAL, vea [Migración de aplicaciones a la Biblioteca de autenticación de Microsoft (MSAL)](../develop/msal-migration.md).

Además, hemos finalizado el trabajo para que toda la funcionalidad de Azure AD Graph esté disponible mediante MS Graph. Por lo tanto, las Graph API de Azure AD solo recibirán correcciones de errores y de seguridad hasta el 30 de junio de 2022. Para más información, vea [Actualización de las aplicaciones para usar la Biblioteca de autenticación de Microsoft y Microsoft Graph API](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/update-your-applications-to-use-microsoft-authentication-library/ba-p/1257363).
 
---
 
## <a name="may-2020"></a>Mayo de 2020

### <a name="retirement-of-properties-in-signins-riskyusers-and-riskdetections-apis"></a>Retirada de propiedades en las API signIns, riskyUsers y riskDetections

**Tipo:** Plan de cambio  
**Categoría del servicio:** Protección de identidad  
**Funcionalidad del producto:** Seguridad y protección de la identidad

Actualmente, los tipos enumerados se usan para representar la propiedad riskType en riskDetections API y riskyUserHistoryItem (en versión preliminar). Los tipos enumerados también se usan para la propiedad riskEventTypes de signIns API. En el futuro, se representarán estas propiedades como cadenas. 

Los clientes deben realizar la transición a la propiedad riskEventType de la versión beta de riskDetections y riskyUserHistoryItem API, así como a la propiedad riskEventTypes_v2 de la versión beta de signIns API antes del 9 de septiembre de 2020. En esa fecha, se retirarán las propiedades actuales riskType y riskEventTypes. Para más información, vea [Cambios en las propiedades de eventos de riesgo y en las API de Identity Protection en Microsoft Graph](https://developer.microsoft.com/graph/blogs/changes-to-risk-event-properties-and-identity-protection-apis-on-microsoft-graph/).

--- 

### <a name="deprecation-of-riskeventtypes-property-in-signins-v10-api-on-microsoft-graph"></a>Desuso de la propiedad riskEventTypes en signIns v1.0 API en Microsoft Graph

**Tipo:** Plan de cambio  
**Categoría del servicio:** Notificación  
**Funcionalidad del producto:** Seguridad y protección de la identidad

Los tipos enumerados cambiarán a tipos de cadena al representar las propiedades de evento de riesgo en Microsoft Graph en septiembre de 2020. Además de afectar a las API en versión preliminar, este cambio también afectará a signIns API en producción.

Hemos introducido una nueva propiedad riskEventsTypes_v2 (cadena) en signIns v1.0 API. Se retirará la propiedad riskEventTypes (enumeración) actual el 11 de junio de 2022 de acuerdo con la directiva de desuso de Microsoft Graph. Los clientes deben realizar la transición a la propiedad riskEventTypes_v2 de v1.0 signIns API antes del 11 de junio de 2022. Para más información, vea [Desuso de la propiedad riskEventTypes en signIns v1.0 API en Microsoft Graph](https://developer.microsoft.com/graph/blogs/deprecation-of-riskeventtypes-property-in-signins-v1-0-api-on-microsoft-graph//).

--- 

### <a name="upcoming-changes-to-mfa-email-notifications"></a>Próximos cambios en las notificaciones por correo electrónico de MFA

**Tipo:** Plan de cambio  
**Categoría del servicio:** MFA  
**Funcionalidad del producto:** Seguridad y protección de la identidad
 

Vamos a realizar los siguientes cambios en las notificaciones por correo electrónico de MFA en la nube:

Las notificaciones por correo electrónico se enviarán desde las siguientes direcciones: azure-noreply@microsoft.com y msonlineservicesteam@microsoftonline.com. Estamos actualizando el contenido de los correos electrónicos de alerta sobre fraudes a fin de explicar mejor los pasos necesarios para desbloquear los usos.

---

### <a name="new-self-service-sign-up-for-users-in-federated-domains-who-cant-access-microsoft-teams-because-they-arent-synced-to-azure-active-directory"></a>Nuevo registro de autoservicio para usuarios de dominios federados que no pueden acceder a Microsoft Teams porque no están sincronizados con Azure Active Directory.

**Tipo:** Plan de cambio  
**Categoría del servicio:** Autenticaciones (inicios de sesión)  
**Funcionalidad del producto:** Autenticación de usuarios
 

Actualmente, los usuarios que están en dominios federados en Azure AD, pero que no están sincronizados en el inquilino, no pueden acceder a Teams. A partir de finales de junio, esta nueva funcionalidad les permitirá hacerlo gracias a la extensión de la característica de registro con verificación por correo electrónico. Esto permitirá a los usuarios iniciar sesión en un proveedor de identidades (IdP) federado. En el caso de los usuarios que aún no tengan un objeto de usuario en Azure ID, el objeto se creará automáticamente y se autenticará para Teams. El objeto de usuario se marcará como "registro de autoservicio". Se trata de una extensión de la característica existente para que los usuarios de los dominios administrados puedan registrarse mediante la verificación por correo electrónico y se pueda llevar un control utilizando la misma marca. La implementación de este cambio se llevará a cabo durante los dos próximos meses. Vea las actualizaciones de la documentación [aquí](../enterprise-users/directory-self-service-signup.md).
 
---

### <a name="upcoming-fix-the-oidc-discovery-document-for-the-azure-government-cloud-is-being-updated-to-reference-the-correct-graph-endpoints"></a>Próxima corrección: El documento de detección de OIDC para la nube de Azure Government se está actualizando para que haga referencia a los puntos de conexión de Graph correctos.

**Tipo:** Plan de cambio  
**Categoría del servicio:** Nubes soberanas  
**Funcionalidad del producto:** Autenticación de usuarios
 
A partir de junio, el documento de detección de OIDC [Plataforma de identidad de Microsoft y protocolo OpenID Connect](../develop/v2-protocols-oidc.md) sobre el punto de conexión de la [nube de Azure Government](../develop/authentication-national-cloud.md) (login.microsoftonline.us), comenzará a devolver el punto de conexión de [Graph de la nube nacional ](/graph/deployments) correcto (https://graph.microsoft.us o https://dod-graph.microsoft.us), según el inquilino proporcionado).  Actualmente, proporciona el campo "msgraph_host" del punto de conexión de Graph incorrecto (graph.microsoft.com).  

Esta corrección de errores se implementará gradualmente durante 2 meses aproximadamente.  

---

### <a name="azure-government-users-will-no-longer-be-able-to-sign-in-on-loginmicrosoftonlinecom"></a>Los usuarios de Azure Government ya no podrán iniciar sesión en login.microsoftonline.com

**Tipo:** Plan de cambio  
**Categoría del servicio:** Nubes soberanas  
**Funcionalidad del producto:** Autenticación de usuarios
 
El 1 de junio de 2018, la autoridad oficial de Azure Active Directory (Azure AD) para Azure Government cambió de https://login-us.microsoftonline.com a https://login.microsoftonline.us. Si posee una aplicación en un inquilino de Azure Government, tiene que actualizarla para que los usuarios inicien sesión en el punto de conexión .us.

El 5 de mayo, Azure AD comenzó a aplicar el cambio relativo al punto de conexión, por lo que los usuarios de Azure Government no podrán iniciar sesión en aplicaciones hospedadas en inquilinos de Azure Government mediante el punto de conexión público (microsoftonline.com). Las aplicaciones afectadas comenzarán a obtener el error AADSTS900439 - USGClientNotSupportedOnPublicEndpoint. 

Este cambio se implementará de forma gradual y se espera que se haya completado para todas las aplicaciones en junio de 2020. Para más información, consulte la [entrada de blog sobre Azure Government](https://devblogs.microsoft.com/azuregov/azure-government-aad-authority-endpoint-update/).

---

### <a name="saml-single-logout-request-now-sends-nameid-in-the-correct-format"></a>La solicitud de cierre de sesión único de SAML ahora envía el valor de NameID con el formato correcto

**Tipo:** Corregido  
**Categoría del servicio:** Autenticaciones (inicios de sesión)  
**Funcionalidad del producto:** Autenticación de usuarios
 
Cuando un usuario hace clic para cerrar sesión (por ejemplo, en el portal Mis aplicaciones), Azure AD envía un mensaje de cierre de sesión único de SAML a cada aplicación que esté activa en la sesión de usuario y tenga configurada una dirección URL de cierre de sesión. Estos mensajes contienen un valor de NameID con formato persistente.

Si el token de inicio de sesión de SAML original utilizaba un formato diferente para NameID (por ejemplo, correo electrónico o UPN), la aplicación SAML no podía correlacionar el valor de NameID en el mensaje de cierre de sesión para una sesión existente, dado que los valores de NameID utilizados en ambos mensajes eran diferentes. Esto hacía que la aplicación SAML descartara el mensaje de cierre de sesión y que la sesión del usuario se mantuviera activa. Esta corrección hace que el mensaje de cierre de sesión sea coherente con el valor de NameID configurado para la aplicación.

---

### <a name="hybrid-identity-administrator-role-is-now-available-with-cloud-provisioning"></a>El rol de administrador de identidades híbridas ahora está disponible con aprovisionamiento en la nube

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento en la nube de Azure AD  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
Los administradores de TI pueden empezar a usar el nuevo rol de administrador de identidades híbridas como el rol con privilegios mínimos para configurar el aprovisionamiento en la nube de Azure ADConnect. Con este nuevo rol, ya no tiene que usar el rol de administrador global para instalar y configurar el aprovisionamiento en la nube. [Más información](../roles/delegate-by-task.md#connect).
 
---

### <a name="new-federated-apps-available-in-azure-ad-application-gallery---may-2020"></a>Nuevas aplicaciones federadas disponibles en la galería de aplicaciones de Azure AD, mayo de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** Integración de terceros
 
En mayo de 2020, hemos agregado 36 nuevas aplicaciones a la galería de aplicaciones con compatibilidad de federación:

[Moula](https://moula.com.au/pay/merchants), [Surveypal](https://www.surveypal.com/app), [Kbot365](https://www.konverso.ai/virtual-assistant-digital-workplace/), [TackleBox](http://www.tacklebox.app/), [Powell Teams](https://powell-software.com/en/powell-teams-en/), [Talentsoft Assistant](https://msteams.talent-soft.com/), [ASC Recording Insights](https://teams.asc-recording.app/product), [GO1](https://www.go1.com/), [B-Engaged](https://b-engaged.se/), [Competella Contact Center Workgroup](http://www.competella.com/), [Asite](http://www.asite.com/), [ImageSoft Identity](https://identity.imagesoftinc.com/), [My IBISWorld](https://identity.imagesoftinc.com/), [insuite](../saas-apps/insuite-tutorial.md), [Change Process Management](../saas-apps/change-process-management-tutorial.md), [Cyara CX Assurance Platform](../saas-apps/cyara-cx-assurance-platform-tutorial.md), [Smart Global Governance](../saas-apps/smart-global-governance-tutorial.md), [Prezi](../saas-apps/prezi-tutorial.md), [Mapbox](../saas-apps/mapbox-tutorial.md), [Datava Enterprise Service Platform](../saas-apps/datava-enterprise-service-platform-tutorial.md), [Whimsical](../saas-apps/whimsical-tutorial.md), [Trelica](../saas-apps/trelica-tutorial.md), [EasySSO for Confluence](../saas-apps/easysso-for-confluence-tutorial.md), [EasySSO for BitBucket](../saas-apps/easysso-for-bitbucket-tutorial.md), [EasySSO for Bamboo](../saas-apps/easysso-for-bamboo-tutorial.md), [Torii](../saas-apps/torii-tutorial.md), [Axiad Cloud](../saas-apps/axiad-cloud-tutorial.md), [Humanage](../saas-apps/humanage-tutorial.md), [ColorTokens ZTNA](../saas-apps/colortokens-ztna-tutorial.md), [CCH Tagetik](../saas-apps/cch-tagetik-tutorial.md), [ShareVault](../saas-apps/sharevault-tutorial.md), [Vyond](../saas-apps/vyond-tutorial.md), [TextExpander](../saas-apps/textexpander-tutorial.md), [Anyone Home CRM](../saas-apps/anyone-home-crm-tutorial.md), [askSpoke](../saas-apps/askspoke-tutorial.md), [ice Contact Center](../saas-apps/ice-contact-center-tutorial.md)

La documentación de todas las aplicaciones está disponible aquí: https://aka.ms/AppsTutorial

Para mostrar su aplicación en la galería de aplicaciones Azure AD, lea los detalles aquí: https://aka.ms/AzureADAppRequest

---

### <a name="report-only-mode-for-conditional-access-is-now-generally-available"></a>El modo Solo informe para el Acceso condicional ya está disponible con carácter general.

**Tipo:** Nueva característica  
**Categoría del servicio:** Acceso condicional  
**Funcionalidad del producto:** Seguridad y protección de la identidad

El [modo Solo informe para el Acceso condicional de Azure AD](../conditional-access/concept-conditional-access-report-only.md) le permite evaluar el resultado de una directiva sin necesidad de aplicar controles de acceso. Puede probar las directivas del modo Solo informe en toda la organización y comprender su impacto antes de habilitarlas, lo que hará que la implementación sea más segura y fácil. En los últimos meses, hemos observado una importante adopción del modo de solo informe, y más de 26 millones de usuarios están incluidos en el ámbito de la directiva de solo informe. Con el anuncio de hoy, se crearán nuevas directivas de acceso condicional de Azure AD en el modo de solo informe de forma predeterminada. Esto significa que puede supervisar el impacto de las directivas desde el momento en el que se crean. Además, aquellos usuarios que utilizan Microsoft Graph API, también pueden [administrar directivas de solo informe mediante programación](/graph/api/resources/conditionalaccesspolicy?view=graph-rest-beta). 

---

### <a name="self-service-sign-up-for-guest-users"></a>Registro de autoservicio para usuarios invitados

**Tipo:** Nueva característica  
**Categoría del servicio:** B2B  
**Funcionalidad del producto:** B2B/B2C
 
Mediante las identidades externas en Azure AD, puede facilitar a personas ajenas a la organización el acceso a sus aplicaciones y recursos, además de permitirles iniciar sesión con la identidad que prefieran. Al compartir una aplicación con usuarios externos, es posible que no siempre sepa de antemano quién necesitará tener acceso a la aplicación. Con el [registro de autoservicio](../external-identities/self-service-sign-up-overview.md), puede facilitar a los usuarios invitados el registro y el acceso a una cuenta de invitado para sus aplicaciones de línea de negocio (LOB). El flujo de registro se puede crear y personalizar para admitir Azure AD e identidades sociales. También puede recopilar información adicional sobre el usuario durante el registro.

---

 ### <a name="conditional-access-insights-and-reporting-workbook-is-generally-available"></a>El libro Conditional Access Insights and Reporting (Información detallada e informes del acceso condicional) está disponible con carácter general

**Tipo:** Nueva característica  
**Categoría del servicio:** Acceso condicional  
**Funcionalidad del producto:** Seguridad y protección de la identidad

El [libro Conditional Access Insights and Reporting (Información detallada e informes del acceso condicional)](../conditional-access/howto-conditional-access-insights-reporting.md) ofrece a los administradores un resumen del acceso condicional de Azure AD en su inquilino. Con la funcionalidad de seleccionar una directiva individual, los administradores pueden comprender mejor lo que hace cada directiva y supervisar los cambios en tiempo real. El libro transmite los datos almacenados en Azure Monitor, que puede configurar en unos minutos [según estas instrucciones](../reports-monitoring/howto-integrate-activity-logs-with-log-analytics.md). Para encontrar el panel con más facilidad, lo hemos trasladado a la nueva pestaña Conclusiones e informes del menú Acceso condicional de Azure AD.

---

### <a name="policy-details-blade-for-conditional-access-is-in-public-preview"></a>La hoja Detalles de la directiva de Acceso condicional está en versión preliminar pública.

**Tipo:** Nueva característica  
**Categoría del servicio:** Acceso condicional  
**Funcionalidad del producto:** Seguridad y protección de la identidad

La nueva [hoja Detalles de la directiva](../conditional-access/troubleshoot-conditional-access.md) muestra las asignaciones, condiciones y controles que se han llevado a cabo durante la evaluación de la directiva de acceso condicional. Para acceder a la hoja, seleccione una fila en las pestañas Acceso condicional o Solo informe, en los detalles de inicio de sesión.

---

### <a name="new-query-capabilities-for-directory-objects-in-microsoft-graph-are-in-public-preview"></a>Nuevas funciones de consulta para objetos de directorio en Microsoft Graph ahora disponibles en versión preliminar pública

**Tipo:** Nueva característica  
**Categoría del servicio:** MS Graph **Funcionalidad del producto:** Experiencia para el desarrollador

Se están incorporando nuevas funciones a las API de objetos de directorio de Microsoft Graph, que permiten realizar operaciones de recuento, búsqueda, filtrado y ordenación. Esto permitirá a los desarrolladores consultar rápidamente nuestros objetos de directorio sin necesidad de buscar alternativas como la ordenación y el filtrado en memoria. Puede obtener más información en esta [entrada de blog](https://aka.ms/CountFilterMSGraphAAD).

Actualmente nos encontramos en la fase de versión preliminar pública, a la espera de comentarios. Envíe sus comentarios por medio de esta [breve encuesta](https://aka.ms/MsGraphAADSurveyDocs).

---

### <a name="configure-saml-based-single-sign-on-using-microsoft-graph-api-beta"></a>Configuración del inicio de sesión único basado en SAML mediante Microsoft Graph API (beta)

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** SSO
 
Ya se ofrece compatibilidad para crear y configurar una aplicación desde la galería de Azure AD mediante MS Graph API en la versión beta. Si necesita configurar el inicio de sesión único basado en SAML para varias instancias de una aplicación, ahorre tiempo y utilice Microsoft Graph API para [automatizar la configuración del inicio de sesión único basado en SAML](/graph/application-saml-sso-configure-api).
 
---

### <a name="new-provisioning-connectors-in-the-azure-ad-application-gallery---may-2020"></a>Nuevos conectores de aprovisionamiento disponibles en la galería de aplicaciones de Azure AD, mayo de 2020

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Integración de terceros
 
Ahora, puede automatizar la creación, actualización y eliminación de cuentas de usuario para estas aplicaciones recién integradas:

* [8x8](../saas-apps/8x8-provisioning-tutorial.md)
* [Juno Journey](../saas-apps/juno-journey-provisioning-tutorial.md)
* [MediusFlow](../saas-apps/mediusflow-provisioning-tutorial.md)
* [New Relic by Organization](../saas-apps/new-relic-by-organization-provisioning-tutorial.md)
* [Oracle Cloud Infrastructure Console](../saas-apps/oracle-cloud-infratstructure-console-provisioning-tutorial.md)

Para más información acerca de cómo proteger mejor una organización mediante el aprovisionamiento automatizado de cuentas de usuario, consulte [Automatización del aprovisionamiento y desaprovisionamiento de usuarios para aplicaciones SaaS con Azure Active Directory](../app-provisioning/user-provisioning.md).

---

### <a name="saml-token-encryption-is-generally-available"></a>El cifrado de tokens SAML está disponible con carácter general

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** SSO
 
El [cifrado de tokens SAML](../manage-apps/howto-saml-token-encryption.md) permite configurar las aplicaciones para que reciban aserciones de SAML cifradas. La característica ya está disponible con carácter general en todas las nubes.
 
---

### <a name="group-name-claims-in-application-tokens-is-generally-available"></a>Las notificaciones de nombre de grupo en tokens de aplicación están disponibles con carácter general

**Tipo:** Nueva característica  
**Categoría del servicio:** Aplicaciones empresariales  
**Funcionalidad del producto:** SSO
 
Las notificaciones de grupo emitidas en un token ahora se pueden limitar a los grupos asignados a la aplicación.  Esto es especialmente importante cuando los usuarios son miembros de un gran número de grupos y había riesgo de superar los límites de tamaño del token. Esta nueva funcionalidad permite [agregar nombres de grupo a los tokens](../hybrid/how-to-connect-fed-group-claims.md) con carácter general.
 
---

### <a name="workday-writeback-now-supports-setting-work-phone-number-attributes"></a>La escritura diferida de Workday ahora admite el establecimiento de atributos relativos al número de teléfono del trabajo

**Tipo:** Nueva característica  
**Categoría del servicio:** Aprovisionamiento de aplicaciones  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
Hemos mejorado la aplicación de aprovisionamiento de escritura diferida de Workday para que admita la escritura diferida de los atributos relativos al número de teléfono del trabajo y al número de móvil. Además del correo electrónico y el nombre de usuario, ahora puede configurar la aplicación de aprovisionamiento de escritura diferida de Workday para transferir los valores de número de teléfono de Azure AD a Workday. Para más información sobre cómo configurar la escritura diferida de números de teléfono, consulte el tutorial de la aplicación de [escritura diferida de Workday](../saas-apps/workday-writeback-tutorial.md). 

---

### <a name="publisher-verification-preview"></a>Comprobación del publicador (versión preliminar)

**Tipo:** Nueva característica  
**Categoría del servicio:** Otros  
**Funcionalidad del producto:** Experiencia para el desarrollador
 
La verificación del publicador (versión preliminar) ayuda a los administradores y usuarios finales a comprender la autenticidad de los desarrolladores de aplicaciones que se integran con la plataforma de identidad de Microsoft. Para más información, consulte [Comprobación del publicador (versión preliminar)](../develop/publisher-verification-overview.md).
 
---

### <a name="authorization-code-flow-for-single-page-apps"></a>Flujo de código de autorización para aplicaciones de una sola página

**Tipo:** Característica modificada **Categoría del servicio:** Autenticación **Funcionalidad del producto:** Experiencia para el desarrollador

Debido a las [restricciones de cookies de terceros como Safari ITP](../develop/reference-third-party-cookies-spas.md) aplicadas en el explorador, las aplicaciones de página única (SPA) tendrán que usar el flujo de código de autorización en lugar del flujo implícito para mantener el SSO. MSAL.js v2.x admite ahora el flujo de código de autorización. Las actualizaciones correspondientes están disponibles en Azure Portal. De este modo, podrá actualizar sus aplicaciones de página única para que sean del tipo "spa" y utilicen el flujo de código de autenticación. Para más instrucciones, consulte [Inicio rápido: Inicio de sesión de los usuarios y obtención de un token de acceso en una SPA de JavaScript mediante el flujo de código de autorización](../develop/quickstart-v2-javascript-auth-code.md).

---

### <a name="improved-filtering-for-devices-is-in-public-preview"></a>El filtrado mejorado para dispositivos está en versión preliminar pública

**Tipo:** Característica modificada   
**Categoría del servicio:** Administración de dispositivos **Funcionalidad del producto:** Administración del ciclo de vida de dispositivos
 
Antes, los únicos filtros que se podían usar eran "Habilitado" y "Fecha de actividad". Ahora, puede [filtrar la lista de dispositivos en función de más propiedades](../devices/device-management-azure-portal.md#device-list-filtering-preview), como el tipo de sistema operativo, el tipo de combinación, el cumplimiento, etc. Estas incorporaciones permitirán encontrar fácilmente un dispositivo determinado.

---

### <a name="the-new-app-registrations-experience-for-azure-ad-b2c-is-now-generally-available"></a>La nueva experiencia Registros de aplicaciones para Azure AD B2C ya está disponible con carácter general

**Tipo:** Característica modificada   
**Categoría del servicio:** B2C: administración de identidades de consumidor  
**Funcionalidad del producto:** Administración del ciclo de vida de la identidad
 
La nueva experiencia Registros de aplicaciones para Azure AD B2C ya está disponible con carácter general. 

Antes, había que administrar las aplicaciones Azure AD B2C orientadas al consumidor con independencia del resto de aplicaciones mediante la experiencia "Aplicaciones" heredada. Eso implicaba distintas experiencias de creación de aplicaciones en distintas ubicaciones de Azure.

La nueva experiencia muestra todos los registros de aplicaciones de Azure AD B2C y Azure AD en un solo lugar y proporciona una manera coherente de administrarlos. Si necesita administrar una aplicación orientada al cliente o una aplicación que tenga acceso a Microsoft Graph para administrar recursos de Azure AD B2C mediante programación, solo tendrá que aprender una manera de hacer cosas.

Puede acceder a la nueva experiencia desde el servicio Azure AD B2C. Una vez ahí, seleccione la hoja Registros de aplicaciones. También puede acceder a la experiencia desde el servicio de Azure Active Directory.

La experiencia Registros de aplicaciones de Azure AD B2C se basa en la [experiencia de registro de aplicaciones](https://developer.microsoft.com/identity/blogs/new-app-registrations-experience-is-now-generally-available/) general para inquilinos de Azure AD, pero se ha adaptado para Azure AD B2C. La experiencia "Aplicaciones" heredada dejará de utilizarse en el futuro.

Para más información, visite [ La nueva experiencia Registros de aplicaciones para Azure Active Directory B2C ](../../active-directory-b2c/app-registrations-training-guide.md).

---

## <a name="april-2020"></a>Abril de 2020

### <a name="combined-security-info-registration-experience-is-now-generally-available"></a>La experiencia combinada del registro de la información de seguridad ya está disponible con carácter general.

**Tipo:** Nueva característica

**Categoría del servicio:** Autenticaciones (inicios de sesión)

**Funcionalidad del producto:** Seguridad y protección de la identidad

La experiencia de registro combinada con autenticación multifactor (MFA) y autoservicio de restablecimiento de contraseña (SSPR) ahora están disponibles con carácter general. Esta nueva experiencia de registro permite a los usuarios registrarse en MFA y SSPR en un único proceso paso a paso. Al implementar la nueva experiencia para la organización, los usuarios pueden registrarse en menos tiempo y con menos complicaciones. Consulte la entrada de blog [aquí](https://bit.ly/3etiRyQ).

---

### <a name="continuous-access-evaluation"></a>Evaluación continua de acceso

**Tipo:** Nueva característica

**Categoría del servicio:** Autenticaciones (inicios de sesión)

**Funcionalidad del producto:** Seguridad y protección de la identidad

Evaluación continua de acceso es una nueva característica de seguridad que permite el cumplimiento casi en tiempo real de las directivas en los usuarios de confianza que consumen tokens de acceso de Azure AD cuando se producen eventos en Azure AD (por ejemplo, la eliminación de cuentas de usuario). Esta característica la vamos a implementar en primer lugar para clientes de Teams y Outlook. Para más información, consulte el [blog](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/moving-towards-real-time-policy-and-security-enforcement/ba-p/1276933) y la [documentación](../conditional-access/concept-continuous-access-evaluation.md).

---

### <a name="sms-sign-in-firstline-workers-can-sign-in-to-azure-ad-backed-applications-with-their-phone-number-and-no-password"></a>Inicio de sesión por SMS: Los trabajadores de primera línea pueden iniciar sesión en las aplicaciones respaldadas por Azure AD con su número de teléfono y sin contraseña.

**Tipo:** Nueva característica

**Categoría del servicio:** Autenticaciones (inicios de sesión)

**Funcionalidad del producto:** Autenticación de usuarios

Office está lanzando una serie de aplicaciones empresariales orientadas a móviles dirigidas a organizaciones no tradicionales y a empleados de grandes organizaciones que no usan el correo electrónico como método de comunicación principal. Estas aplicaciones se dirigen a empleados de primera línea, trabajadores sin escritorio, agentes de campo o empleados de comercios minoristas que podrían no recibir una dirección de correo electrónico de su empleador, tener acceso a un equipo o a recursos de TI. Este proyecto permitirá a estos empleados iniciar sesión en las aplicaciones empresariales solo con un número de teléfono y la devolución de un código. Para más información, consulte la [documentación del administrador](../authentication/howto-authentication-sms-signin.md) y la [documentación del usuario final](../user-help/sms-sign-in-explainer.md).

---

### <a name="invite-internal-users-to-use-b2b-collaboration"></a>Invitar a usuarios internos a usar la colaboración B2B

**Tipo:** Nueva característica

**Categoría del servicio:** B2B

**Funcionalidad del producto:**

Vamos a expandir la funcionalidad de invitación B2B para que se pueda invitar a las cuentas internas existentes a usar las credenciales de colaboración B2B en adelante. Esto se consigue pasando el objeto de usuario a la API de invitación, además de los parámetros típicos, como la dirección de correo electrónico invitada. El identificador de objeto del usuario, su UPN, la pertenencia a grupos, la asignación de aplicaciones, entre otros, permanecen intactos, pero en adelante usarán B2B para autenticarse con las credenciales de su inquilino particular en lugar de con las credenciales internas que usaban antes de la invitación. Para más información, consulte la [documentación](../external-identities/invite-internal-users.md).

---

### <a name="report-only-mode-for-conditional-access-is-now-generally-available"></a>El modo Solo informe para el Acceso condicional ya está disponible con carácter general.

**Tipo:** Nueva característica

**Categoría del servicio:** Acceso condicional

**Funcionalidad del producto:** Seguridad y protección de la identidad

El [modo Solo informe para el Acceso condicional de Azure AD](../conditional-access/concept-conditional-access-report-only.md) le permite evaluar el resultado de una directiva sin necesidad de aplicar controles de acceso. Puede probar las directivas del modo Solo informe en toda la organización y comprender su impacto antes de habilitarlas, lo que hará que la implementación sea más segura y fácil. Durante los últimos meses, hemos visto una importante adopción del modo Solo informe, con más de 26 millones de usuarios. Con este anuncio, se crearán nuevas directivas de acceso condicional de Azure AD en modo Solo informe de forma predeterminada. Esto significa que puede supervisar el impacto de las directivas desde el momento en el que se crean. Además, para aquellos usuarios que utilizan Microsoft Graph API, también puede [administrar directivas de Solo informe mediante programación](/graph/api/resources/conditionalaccesspolicy?view=graph-rest-beta). 

---

### <a name="conditional-access-insights-and-reporting-workbook-is-generally-available"></a>El libro Conclusiones e informes de Acceso condicional está disponible con carácter general.

**Tipo:** Nueva característica

**Categoría del servicio:** Acceso condicional

**Funcionalidad del producto:** Seguridad y protección de la identidad

El [libro Conclusiones e informes](../conditional-access/howto-conditional-access-insights-reporting.md) de Acceso condicional proporciona a los administradores una vista resumida del acceso condicional de Azure AD en el inquilino. Con la funcionalidad de seleccionar una directiva individual, los administradores pueden comprender mejor lo que hace cada directiva y supervisar los cambios en tiempo real. El libro transmite los datos almacenados en Azure Monitor, que puede configurar en unos minutos [según estas instrucciones](../reports-monitoring/howto-integrate-activity-logs-with-log-analytics.md). Para encontrar el panel con más facilidad, lo hemos trasladado a la nueva pestaña Conclusiones e informes del menú Acceso condicional de Azure AD.

---

### <a name="policy-details-blade-for-conditional-access-is-in-public-preview"></a>La hoja Detalles de la directiva de Acceso condicional está en versión preliminar pública.

**Tipo:** Nueva característica

**Categoría del servicio:** Acceso condicional

**Funcionalidad del producto:** Seguridad y protección de la identidad

La nueva [hoja Detalles de la directiva](../conditional-access/troubleshoot-conditional-access.md) muestra qué asignaciones, condiciones y controles se cumplieron durante la evaluación de la directiva de acceso condicional. Para acceder a la hoja, seleccione una fila en las pestañas **Acceso condicional** o **Solo informe** de los detalles de inicio de sesión.

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---april-2020"></a>Nuevas aplicaciones federadas disponibles en la galería de aplicaciones de Azure AD (abril de 2020)

**Tipo:** Nueva característica

**Categoría del servicio:** Aplicaciones empresariales

**Funcionalidad del producto:** Integración de terceros

En abril de 2020, hemos agregado a la galería de aplicaciones estas 31 nuevas aplicaciones que admiten federación: 

[SincroPool Apps](https://www.sincropool.com/), [SmartDB](https://hibiki.dreamarts.co.jp/smartdb/trial/), [Float](../saas-apps/float-tutorial.md), [LMS365](https://lms.365.systems/), [IWT Procurement Suite](../saas-apps/iwt-procurement-suite-tutorial.md), [Lunni](https://lunni.fi/), [EasySSO for Jira](../saas-apps/easysso-for-jira-tutorial.md), [Virtual Training Academy](https://vta.c3p.ca/app/en/openid?authenticate_with=microsoft), [Meraki Dashboard](../saas-apps/meraki-dashboard-tutorial.md), [Microsoft 365 Mover](https://app.mover.io/login), [Speaker Engage](https://speakerengage.com/login.php), [Honestly](../saas-apps/honestly-tutorial.md), [Ally](../saas-apps/ally-tutorial.md), [DutyFlow](https://app.dutyflow.nl/), [AlertMedia](../saas-apps/alertmedia-tutorial.md), [gr8 People](../saas-apps/gr8-people-tutorial.md), [Pendo](../saas-apps/pendo-tutorial.md), [HighGround](../saas-apps/highground-tutorial.md), [Harmony](../saas-apps/harmony-tutorial.md), [Timetabling Solutions](../saas-apps/timetabling-solutions-tutorial.md), [SynchroNet CLICK](../saas-apps/synchronet-click-tutorial.md), [empower](https://www.made-in-office.com/en/), [Fortes Change Cloud](../saas-apps/fortes-change-cloud-tutorial.md), [Litmus](../saas-apps/litmus-tutorial.md), [GroupTalk](https://recorder.grouptalk.com/), [Frontify](../saas-apps/frontify-tutorial.md), [MongoDB Cloud](../saas-apps/mongodb-cloud-tutorial.md), [TickitLMS Learn](../saas-apps/tickitlms-learn-tutorial.md), [COCO](https://hexaware.com/partnerships-and-alliances/digital-transformation-using-microsoft-azure/), [Nitro Productivity Suite](../saas-apps/nitro-productivity-suite-tutorial.md), [Trend Micro Web Security(TMWS)](https://review.docs.microsoft.com/azure/active-directory/saas-apps/trend-micro-tutorial)

Para obtener más información acerca de las aplicaciones, consulte [Integración de aplicación SaaS con Azure Active Directory](../saas-apps/tutorial-list.md). Para obtener más información para que una aplicación se muestre en la galería de aplicaciones de Azure AD, consulte [Aprenda a mostrar su aplicación en la galería de aplicaciones de Azure Active Directory](../azuread-dev/howto-app-gallery-listing.md).

---

### <a name="microsoft-graph-delta-query-support-for-oauth2permissiongrant-available-for-public-preview"></a>La compatibilidad con las consultas delta de Microsoft Graph para oAuth2PermissionGrant está disponible para la versión preliminar pública.

**Tipo:** Nueva característica

**Categoría del servicio:** MS Graph

**Funcionalidad del producto:** Experiencia para el desarrollador

Las consultas delta para oAuth2PermissionGrant están disponibles en versión preliminar pública. Ahora puede realizar el seguimiento de los cambios sin necesidad de sondear Microsoft Graph continuamente. [Más información.](/graph/api/oAuth2PermissionGrant-delta?tabs=http&view=graph-rest-beta)

---

### <a name="microsoft-graph-delta-query-support-for-organizational-contact-generally-available"></a>La compatibilidad con las consultas delta de Microsoft Graph para contactos de la organización está disponible con carácter general.

**Tipo:** Nueva característica

**Categoría del servicio:** MS Graph

**Funcionalidad del producto:** Experiencia para el desarrollador

Las consultas delta para contactos de la organización están disponibles con carácter general. Ahora puede realizar el seguimiento de los cambios en las aplicaciones de producción sin necesidad de sondear Microsoft Graph continuamente. Reemplace el código existente que ahora sondea continuamente los datos de orgContact por una consulta delta para mejorar significativamente el rendimiento. [Más información.](/graph/api/orgcontact-delta?tabs=http&view=graph-rest-1.0)

---

### <a name="microsoft-graph-delta-query-support-for-application-generally-available"></a>La compatibilidad con las consultas delta de Microsoft Graph para aplicaciones está disponible con carácter general.

**Tipo:** Nueva característica

**Categoría del servicio:** MS Graph

**Funcionalidad del producto:** Experiencia para el desarrollador

Las consultas delta para aplicaciones están disponibles con carácter general. Ahora puede realizar el seguimiento de los cambios en las aplicaciones de producción sin necesidad de sondear Microsoft Graph continuamente. Reemplace el código existente que ahora sondea continuamente los datos de la aplicación por una consulta delta para mejorar significativamente el rendimiento. [Más información.](/graph/api/application-delta?view=graph-rest-1.0)

---

### <a name="microsoft-graph-delta-query-support-for-administrative-units-available-for-public-preview"></a>La compatibilidad con las consultas delta de Microsoft Graph para unidades administrativas está disponible en versión preliminar pública.

**Tipo:** Nueva característica

**Categoría del servicio:** MS Graph

**Funcionalidad del producto:** Las consultas delta de la experiencia del desarrollador para unidades administrativas están disponibles en versión preliminar pública. Ahora puede realizar el seguimiento de los cambios sin necesidad de sondear Microsoft Graph continuamente. [Más información.](/graph/api/administrativeunit-delta?tabs=http&view=graph-rest-beta)

---

### <a name="manage-authentication-phone-numbers-and-more-in-new-microsoft-graph-beta-apis"></a>Administre los números de teléfono de autenticación y mucho más en las nuevas Microsoft Graph API en versión beta.

**Tipo:** Nueva característica

**Categoría del servicio:** MS Graph

**Funcionalidad del producto:** Experiencia para el desarrollador

Estas API son una herramienta fundamental para administrar los métodos de autenticación de los usuarios. Ahora puede realizar un registro previo y administrar mediante programación los autenticadores usados para MFA y el autoservicio de restablecimiento de contraseña (SSPR). Esta ha sido una de las características más solicitadas en las áreas de Azure MFA, SSPR y Microsoft Graph. Las nuevas API que hemos publicado en esta oleada le ofrecen la posibilidad de:

- Leer, agregar, actualizar y eliminar los teléfonos de autenticación de un usuario
- Restablecer la contraseña de un usuario
- Activar y desactivar el inicio de sesión por SMS

Para más información, consulte [Introducción a la API de métodos de autenticación de Azure AD](/graph/api/resources/authenticationmethods-overview?view=graph-rest-beta).

---

### <a name="administrative-units-public-preview"></a>Versión preliminar de las unidades administrativas

**Tipo:** Nueva característica

**Categoría del servicio:** Roles de Azure AD

**Funcionalidad del producto:** Control de acceso

Las unidades administrativas permiten conceder permisos de administrador que están restringidos a un departamento, a una región o a otro segmento de la organización que se defina. Puede usar las unidades administrativas para delegar permisos en los administradores regionales o establecer directivas de forma pormenorizada. Por ejemplo, un administrador de cuentas de usuario podría actualizar la información del perfil, restablecer las contraseñas y asignar las licencias para los usuarios solo en su unidad administrativa.

Mediante el uso de unidades administrativas, un administrador central podría:

- Crear una unidad administrativa para la administración descentralizada de los recursos.
- Asignar un rol con permisos administrativos solo sobre los usuarios de Azure AD de una unidad administrativa.
- Rellenar las unidades administrativas con usuarios y grupos según sea necesario.

Para más información, consulte [Administración de unidades administrativas en Azure Active Directory (versión preliminar)](../users-groups-roles/directory-administrative-units.md).

---

### <a name="printer-administrator-and-printer-technician-built-in-roles"></a>Roles integrados Administrador de impresoras y Técnico de impresoras

**Tipo:** Nueva característica

**Categoría del servicio:** Roles de Azure AD

**Funcionalidad del producto:** Control de acceso

**Administrador de impresoras** : los usuarios con este rol pueden registrar impresoras y administrar todos los aspectos de todas las configuraciones de impresora en la solución de impresión universal de Microsoft, incluida la configuración del conector de impresión universal. Pueden dar su consentimiento a todas las solicitudes de permiso de impresión delegada. Los administradores de impresoras también tienen acceso a los informes de impresión. 

**Técnico de impresoras** : los usuarios con este rol pueden registrar impresoras y administrar el estado de la impresora en la solución de impresión universal de Microsoft. También pueden leer toda la información del conector. Una tarea clave que un Técnico de impresoras no puede realizar es establecer permisos de usuario en las impresoras ni compartir impresoras. [Más información.](../roles/permissions-reference.md#printer-administrator)

---

### <a name="hybrid-identity-admin-built-in-role"></a>Rol integrado Administrador de identidades híbridas

**Tipo:** Nueva característica

**Categoría del servicio:** Roles de Azure AD

**Funcionalidad del producto:** Control de acceso

Los usuarios de este rol pueden habilitar, configurar y administrar servicios y configuraciones relacionados con la habilitación de la identidad híbrida en Azure AD. Este rol concede la capacidad de configurar Azure AD en uno de los tres métodos de autenticación admitidos: la sincronización de hash de contraseña (PHS), la autenticación de paso a través (PTA) o la federación (AD FS o proveedor de federación de terceros), así como implementar la infraestructura local relacionada para habilitarlos. La infraestructura local incluye agentes de aprovisionamiento y PTA. Este rol concede la capacidad de habilitar el inicio de sesión único de conexión directa (S-SSO) para habilitar la autenticación directa en dispositivos que no son de Windows 10 o equipos que no son de Windows Server 2016. Además, este rol concede la capacidad de ver los registros de inicio de sesión y el acceso a los datos de mantenimiento y análisis para la supervisión y la solución de problemas. [Más información.](../roles/permissions-reference.md#hybrid-identity-administrator)

---

### <a name="network-administrator-built-in-role"></a>Rol integrado Administrador de red

**Tipo:** Nueva característica

**Categoría del servicio:** Roles de Azure AD

**Funcionalidad del producto:** Control de acceso

Los usuarios con este rol pueden revisar las recomendaciones de la arquitectura de perímetro de red de Microsoft que se basan en la telemetría de red desde sus ubicaciones de usuario. El rendimiento de red para Microsoft 365 se basa en una cuidadosa arquitectura de perímetro de red de cliente empresarial que suele ser específica de la ubicación del usuario. Este rol permite la edición de ubicaciones de usuario detectadas y la configuración de parámetros de red para esas ubicaciones con el fin de facilitar la mejora de las medidas de telemetría y las recomendaciones de diseño. [Más información.](../roles/permissions-reference.md#network-administrator)

---

### <a name="bulk-activity-and-downloads-in-the-azure-ad-admin-portal-experience"></a>Actividad y descargas masivas en la experiencia del portal de administración de Azure AD

**Tipo:** Nueva característica

**Categoría del servicio:** User Management

**Funcionalidad del producto:** Directorio

Ahora puede realizar actividades masivas con usuarios y grupos de Azure AD mediante la carga de un archivo CSV en la experiencia del portal de administración de Azure AD. Puede crear usuarios o eliminar usuarios, e invitar a usuarios. También puede agregar y quitar miembros de un grupo.

Además, puede descargar listas de recursos de Azure AD desde la experiencia del portal de administración de Azure AD. Puede descargar la lista de usuarios del directorio, la lista de grupos del directorio y los miembros de un grupo determinado.

Para más información, consulte lo siguiente:

- [Crear usuarios](../enterprise-users/users-bulk-add.md) o [invitar a usuarios ](../external-identities/tutorial-bulk-invite.md).
- [Eliminar usuarios](../enterprise-users/users-bulk-delete.md) o [restaurar usuarios eliminados](../enterprise-users/users-bulk-restore.md).
- [Descargar la lista de usuarios](../enterprise-users/users-bulk-download.md) o [descargar la lista de grupos](../enterprise-users/groups-bulk-download.md)
- [Agregar (importar) miembros](../enterprise-users/groups-bulk-import-members.md), [eliminar miembros](../enterprise-users/groups-bulk-remove-members.md) o [descargar la lista de miembros](../enterprise-users/groups-bulk-download-members.md) de un grupo.

---

### <a name="my-staff-delegated-user-management"></a>Administración delegada de usuarios Mi personal

**Tipo:** Nueva característica

**Categoría del servicio:** User Management

**Funcionalidad del producto:**

Mi personal permite a los administradores de primera línea, como el administrador de una tienda, garantizar que los miembros del personal puedan acceder a sus cuentas de Azure AD. En lugar de depender de un departamento de soporte técnico central, las organizaciones pueden delegar tareas comunes, como el restablecimiento de contraseñas o el cambio de números de teléfono, en un administrador de primera línea. Con Mi personal, un usuario que no puede acceder a su cuenta puede recuperar el acceso con tan solo un par de clics, sin necesidad de ayuda del personal de TI o el departamento de soporte técnico. Para más información, consulte [Administración de usuarios con Mi personal (versión preliminar)](../users-groups-roles/my-staff-configure.md) y [Delegación de la administración de usuarios con Mi personal (versión preliminar)](../user-help/my-staff-team-manager.md).

---

### <a name="an-upgraded-end-user-experience-in-access-reviews"></a>Una experiencia de usuario final actualizada en las revisiones de acceso

**Tipo:** Característica modificada

**Categoría del servicio:** Revisiones de acceso

**Funcionalidad del producto:** Identity Governance

Hemos actualizado la experiencia del revisor para las revisiones de acceso de Azure AD en el portal Aplicaciones. A finales de abril, los revisores que han iniciado sesión en la experiencia del revisor de las revisiones de acceso de Azure AD, verán un banner que les permitirá probar la experiencia actualizada en Mi acceso. Tenga en cuenta que la experiencia de revisiones de acceso actualizada ofrece la misma funcionalidad que la experiencia actual, pero con una interfaz de usuario mejorada sobre nuevas funcionalidades para permitir que los usuarios sean productivos. [Aquí encontrará más información sobre la experiencia actualizada](../governance/perform-access-review.md). Esta versión preliminar pública durará hasta finales de julio de 2020. A finales de julio, los revisores que no hayan participado en la experiencia en versión preliminar serán redirigidos automáticamente a Mi acceso para realizar las revisiones de acceso. Si desea que los revisores cambien permanentemente a la experiencia en versión preliminar en Mi acceso ahora, [realice una solicitud aquí](https://forms.microsoft.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR5dv-S62099HtxdeKIcgO-NUOFJaRDFDWUpHRk8zQ1BWVU1MMTcyQ1FFUi4u).

---

### <a name="workday-inbound-user-provisioning-and-writeback-apps-now-support-the-latest-versions-of-workday-web-services-api"></a>Las aplicaciones de aprovisionamiento y escritura diferida de usuarios de entrada de WorkDay ahora admiten las versiones más recientes de la API Workday Web Services

**Tipo:** Característica modificada

**Categoría del servicio:** Aprovisionamiento de aplicaciones

**Funcionalidad del producto:** 

Hemos tenido en cuenta los comentarios de los clientes y hemos actualizado las aplicaciones de aprovisionamiento y escritura diferida de usuarios de entrada de WorkDay en la galería de aplicaciones empresariales para admitir las versiones más recientes de la API Workday Web Services (WWS). Con este cambio, los clientes pueden especificar la versión de la API WWS que desean usar en la cadena de conexión. Esto proporciona a los clientes la capacidad de recuperar más atributos de recursos humanos disponibles en las versiones de WorkDay. La aplicación de escritura diferida de WorkDay ahora usa el servicio web de WorkDay recomendado, Change_Work_Contact_Info, para superar las limitaciones de Maintain_Contact_Info.

De forma predeterminada, si no se especifica ninguna versión en la cadena de conexión, las aplicaciones de aprovisionamiento de entrada de WorkDay seguirán usando WWS v21.1. Para cambiar a las versiones más recientes de la API Workday Web Services para el aprovisionamiento de usuarios de entrada, los clientes deben actualizar la cadena de conexión tal y como se documenta [en el tutorial](../saas-apps/workday-inbound-tutorial.md#which-workday-apis-does-the-solution-use-to-query-and-update-workday-worker-profiles), y también actualizar los valores de XPATH utilizados para los atributos de WorkDay, tal y como se describe en [Guía de referencia de atributos de Workday](../app-provisioning/workday-attribute-reference.md#xpath-values-for-workday-web-services-wws-api-v30). 

Para usar la nueva API para la escritura diferida, no se requieren cambios en la aplicación de aprovisionamiento de escritura diferida de WorkDay. En WorkDay, asegúrese de que la cuenta de usuario del sistema de integración (ISU) de WorkDay tiene permisos para invocar el proceso empresarial Change_Work_Contact, tal y como se describe en la sección del tutorial [Configuración de los permisos de la directiva de seguridad de procesos empresariales](../saas-apps/workday-inbound-tutorial.md#configuring-business-process-security-policy-permissions). 

Hemos actualizado la [guía de tutoriales](../saas-apps/workday-inbound-tutorial.md) para reflejar la compatibilidad con la nueva versión de la API.

---

### <a name="users-with-default-access-role-are-now-in-scope-for-provisioning"></a>Los usuarios con el rol de acceso predeterminado ahora están dentro del ámbito del aprovisionamiento

**Tipo:** Característica modificada

**Categoría del servicio:** Aprovisionamiento de aplicaciones

**Funcionalidad del producto:** Administración del ciclo de vida de la identidad

Históricamente, los usuarios con el rol de acceso predeterminado han estado fuera del ámbito del aprovisionamiento. Hemos recibido comentarios acerca de que los clientes quieren que los usuarios con este rol estén dentro del ámbito del aprovisionamiento. A partir del 16 de abril de 2020, todas las nuevas configuraciones de aprovisionamiento permiten aprovisionar a los usuarios con el rol de acceso predeterminado. Cambiaremos gradualmente el comportamiento de las configuraciones de aprovisionamiento existentes para admitir el aprovisionamiento de usuarios con este rol. [Más información.](../app-provisioning/application-provisioning-config-problem-no-users-provisioned.md)

---

### <a name="updated-provisioning-ui"></a>Actualización de la interfaz de usuario de aprovisionamiento

**Tipo:** Característica modificada

**Categoría del servicio:** Aprovisionamiento de aplicaciones

**Funcionalidad del producto:** Administración del ciclo de vida de la identidad

Hemos actualizado la experiencia de aprovisionamiento para crear una vista de administración más centrada. Cuando vaya a la hoja de aprovisionamiento de una aplicación empresarial que ya se ha configurado, podrá supervisar fácilmente el progreso del aprovisionamiento y administrar acciones como el inicio, la detención y el reinicio del aprovisionamiento. [Más información.](../app-provisioning/configure-automatic-user-provisioning-portal.md)

---

### <a name="dynamic-group-rule-validation-is-now-available-for-public-preview"></a>La validación de reglas de grupos dinámicos ahora está disponible en versión preliminar pública

**Tipo:** Característica modificada

**Categoría del servicio:** Administración de grupos

**Funcionalidad del producto:** Colaboración

Azure Active Directory (Azure AD) ahora ofrece los medios para validar las reglas de grupos dinámicos. En la pestaña **Validación de las reglas** , puede validar la regla dinámica con los miembros del grupo de ejemplo, para confirmar que la regla funciona según lo previsto. Al crear o actualizar reglas de grupos dinámicos, los administradores quieren saber si un usuario o un dispositivo será miembro del grupo. Esto ayuda a evaluar si el usuario o el dispositivo cumplen los criterios de la regla y ayuda a solucionar problemas cuando no se espera la pertenencia.

Para más información, consulte [Validación de una regla de pertenencia dinámica a grupos (versión preliminar)](../enterprise-users/groups-dynamic-rule-validation.md).

---

### <a name="identity-secure-score---security-defaults-and-mfa-improvement-action-updates"></a>Puntuación de seguridad de la identidad: valores predeterminados de seguridad y actualizaciones de las acciones de mejora de MFA

**Tipo:** Característica modificada

**Categoría del servicio:** N/D

**Funcionalidad del producto:** Seguridad y protección de la identidad

**Compatibilidad con los valores predeterminados de seguridad para las acciones de mejora de Azure AD:** La Puntuación de seguridad de Microsoft se actualizará con acciones de mejora para admitir [valores predeterminados de seguridad en Azure AD](./concept-fundamentals-security-defaults.md), lo que facilita la protección de la organización con una configuración de seguridad preconfigurada para ataques comunes. Esto afectará a las siguientes acciones de mejora:

- Garantizar que todos los usuarios pueden completar la autenticación multifactor para el acceso seguro
- Requerir MFA para roles administrativos
- Habilitar la directiva para bloquear la autenticación heredada
 
**Actualizaciones de las acciones de mejora de MFA:** Para reflejar la necesidad de las empresas de garantizar la mayor seguridad al aplicar directivas que funcionen con su negocio, la Puntuación de seguridad de Microsoft ha eliminado tres acciones de mejora centradas en la autenticación multifactor y ha agregado otras dos.

Acciones de mejora eliminadas:

- Registrar a todos los usuarios para la autenticación multifactor
- Exigir autenticación multifactor para todos los usuarios
- Requerir MFA para roles con privilegios Azure AD

Acciones de mejora agregadas:

- Garantizar que todos los usuarios pueden completar la autenticación multifactor para el acceso seguro
- Requerir MFA para roles administrativos

Estas nuevas acciones de mejora requerirán el registro de usuarios o administradores para la autenticación multifactor (MFA) en todo el directorio y el establecimiento del conjunto adecuado de directivas que se adapten a las necesidades de la organización. El objetivo principal es tener flexibilidad, asegurando al mismo tiempo que todos los usuarios y administradores puedan autenticarse con varios factores o solicitudes de comprobación de identidad basadas en riesgos. Se puede hacer con varias directivas que apliquen decisiones de ámbito o estableciendo valores predeterminados de seguridad (a partir del 16 de marzo) que permitan a Microsoft decidir cuándo desafiar a los usuarios con MFA. [Más información sobre las novedades en la Puntuación de seguridad de Microsoft](/microsoft-365/security/mtp/microsoft-secure-score?view=o365-worldwide#whats-new).

---