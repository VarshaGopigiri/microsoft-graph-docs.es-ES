---
title: Introducción a API de sincronización de Azure AD
description: ') le permite automatizar la creación, mantenimiento y la eliminación de las identidades en la nube aplicaciones (software como un servicio o SaaS) como lista desplegable, fuerza de ventas, ServiceNow y mucho más. Puede usar las API de sincronización en Microsoft Graph para administrar la sincronización de identidad mediante programación, incluidos:'
ms.openlocfilehash: ff3acb00801c9b04b8257345b06100297e11710c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089794"
---
# <a name="azure-ad-synchronization-api-overview"></a>Introducción a API de sincronización de Azure AD

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Sincronización de identidades de Active Directory (AD Azure) Azure (también denominada "aprovisionamiento") le permite automatizar la creación, el mantenimiento y la eliminación de las identidades en la nube (software como un servicio o SaaS) aplicaciones como lista desplegable, fuerza de ventas, ServiceNow, y mucho más. Puede usar las API de sincronización en Microsoft Graph para administrar la sincronización de identidad mediante programación, incluidos:

- Crear, iniciar y detener los trabajos de sincronización
- Realizar cambios en el esquema para los trabajos de sincronización
- Compruebe el estado actual de la sincronización 

Para obtener más información acerca de la sincronización en Azure AD, consulte:

* [Automatizar usuario aprovisionamiento y desaprovisionamiento a las aplicaciones de SaaS con Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-app-provisioning)
* [Administración de la cuenta de usuario de aprovisionamiento de aplicaciones de empresa en el portal de Azure](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-enterprise-apps-manage-provisioning)

También puede intentar la API en el [Explorador de gráfico](https://developer.microsoft.com/graph/graph-explorer) en un inquilino de ejemplo o su propio inquilino.

## <a name="synchronization-job"></a>Trabajo de sincronización

Los trabajos de sincronización realizan la sincronización por sondeo para que los cambios en un directorio y la inserción de ellos en otro directorio, periódicamente que se ejecuta en segundo plano. El trabajo de sincronización siempre es específico de una instancia determinada de una aplicación en el inquilino. Como parte de la configuración del trabajo de sincronización, debe conceder autorización para leer y escribir objetos en el directorio de destino y personalizar el esquema de sincronización de la tarea.

Para obtener más información, vea el [trabajo de sincronización](synchronization-synchronizationjob.md).

## <a name="synchronization-schema"></a>Esquema de sincronización

El esquema de sincronización define cuáles serán los objetos sincronizados y cómo se sincronizarán. El esquema de sincronización contiene la mayoría de la información de configuración para un trabajo de sincronización determinado. Normalmente, va a personalizar algunas de las [asignaciones de atributos](synchronization-attributemapping.md), o agregar un [filtro de ámbito](synchronization-filter.md) para sincronizar solo los objetos que cumplen una condición determinada.

El esquema de sincronización incluye los siguientes componentes:

- Definiciones de Active Directory
- Reglas de sincronización
- Asignaciones de objetos

Para obtener más información, vea [esquema de sincronización](synchronization-synchronizationschema.md).

## <a name="synchronization-template"></a>Plantilla de sincronización

La plantilla de sincronización proporciona opciones de configuración de sincronización preconfigurado para una aplicación concreta. Estas opciones de configuración (lo que es más importante, el [esquema de sincronización](synchronization-synchronizationschema.md)) se usará de forma predeterminada para cualquier [trabajo de sincronización](synchronization-synchronizationjob.md) que se basa en la plantilla. Las plantillas especificadas por el desarrollador de aplicaciones.

Para obtener más información, vea [plantilla de sincronización](synchronization-synchronizationtemplate.md).

## <a name="working-with-the-synchronization-api"></a>Trabajar con la API de sincronización

Trabajar con la sincronización de API principalmente implica el acceso a los recursos [synchronizationJob](synchronization-synchronizationjob.md) y [synchronizationSchema](synchronization-synchronizationschema.md) . Para encontrar el recurso [synchronizationJob](synchronization-synchronizationjob.md) , debe conocer el identificador del objeto entidad de seguridad que pertenece el trabajo de sincronización. Los siguientes ejemplos muestran cómo trabajar con los recursos **synchronizationJob** y **synchronizationSchema** .

### <a name="authorization"></a>Authorization

La API de sincronización de Azure AD utiliza OAuth 2.0 para la autorización. Antes de realizar las solicitudes de la API, debe obtener un token de acceso. Para obtener más información, vea [tokens de acceso Get para llamar a Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview). Para obtener acceso a recursos de sincronización, la aplicación necesita permisos de Directory.ReadWrite.All. Para obtener más información, vea [permisos de Active Directory](/graph/permissions-reference#directory-permissions).

### <a name="find-the-service-principal-object-by-display-name"></a>Busque el objeto de entidad de seguridad de servicio por nombre para mostrar

En el ejemplo siguiente se muestra cómo buscar el objeto de entidad de seguridad de servicio por nombre para mostrar.

**Solicitud** 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/servicePrincipals?$select=id,appId,displayName&$filter=startswith(displayName, 'salesforce')
```

**Response**

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
{
    "value": [
    {
        "id": "bc0dc311-87df-48ac-91b1-259bd2c3a31c",
        "appId": "f7808c5e-cb57-4e37-8094-406d302c0f8d",
        "displayName": "Salesforce"
    },
    {
        "id": "d813d7d7-0f41-4edc-b284-d0dfaf399d15",
        "appId": "219561ee-1480-4c67-9aa6-63d861fae3ef",
        "displayName": "salesforce 3"
    }
    ]
}
```

### <a name="find-the-service-principal-object-by-app-id"></a>Buscar el objeto de entidad de seguridad de servicio por identificador de la aplicación

En el ejemplo siguiente se muestra cómo buscar el objeto de entidad de seguridad de servicio por identificador de aplicación.

**Solicitud** 
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/servicePrincipals?$select=id,appId,displayName&$filter=AppId eq '219561ee-1480-4c67-9aa6-63d861fae3ef'
```

**Respuesta**
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
{
    "value": [
        {
            "id": "d813d7d7-0f41-4edc-b284-d0dfaf399d15",
            "appId": "219561ee-1480-4c67-9aa6-63d861fae3ef",
            "displayName": "salesforce 3"
        }
    ]
}
```

### <a name="list-existing-synchronization-jobs"></a>Lista de los trabajos de sincronización existente

En el ejemplo siguiente se muestra cómo obtener una lista de los trabajos de sincronización existente.

**Solicitud**
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs
GET https://graph.microsoft.com/beta/servicePrincipals/60443998-8cf7-4e61-b05c-a53b658cb5e1/synchronization/jobs
```

**Respuesta**
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
{
    "value": [
        {
            "id": "SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa",
            "templateId": "SfSandboxOutDelta",
            "schedule": {
                "expiration": null,
                "interval": "PT20M",
                "state": "Active"
            },
            "status": {}
        }
    ]
}
```

### <a name="get-synchronization-job-status"></a>Obtener el estado del trabajo de sincronización
En el ejemplo siguiente se muestra cómo obtener el estado de un trabajo de sincronización.

**Solicitud**
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}

GET https://graph.microsoft.com/beta/servicePrincipals/60443998-8cf7-4e61-b05c-a53b658cb5e1/synchronization/jobs/SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa
```

**Respuesta**
<!-- { "blockType": "ignored" } -->
```http
    HTTP/1.1 200 OK
    {
        "id": "SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa",
        "templateId": "SfSandboxOutDelta",
        "schedule": {
            "expiration": null,
            "interval": "PT20M",
            "state": "Active"
        },
        "status": {}
    }
```

### <a name="get-synchronization-schema"></a>Obtener el esquema de sincronización
En el ejemplo siguiente se muestra cómo obtener el esquema de sincronización.

**Solicitud**
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
```

**Respuesta**
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
{
    "directories": [],
    "synchronizationRules": []
}
```
## <a name="see-also"></a>Vea también

* [Configurar la sincronización con los atributos de extensión de Active directory](../resources/synchronization-configure-with-directory-extension-attributes.md)
* [Configurar la sincronización con los atributos de destino personalizado](../resources/synchronization-configure-with-custom-target-attributes.md)



