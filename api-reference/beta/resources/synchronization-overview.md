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
# <a name="azure-ad-synchronization-api-overview"></a><span data-ttu-id="74408-104">Introducción a API de sincronización de Azure AD</span><span class="sxs-lookup"><span data-stu-id="74408-104">Azure AD synchronization API overview</span></span>

> <span data-ttu-id="74408-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="74408-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="74408-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="74408-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="74408-107">Sincronización de identidades de Active Directory (AD Azure) Azure (también denominada "aprovisionamiento") le permite automatizar la creación, el mantenimiento y la eliminación de las identidades en la nube (software como un servicio o SaaS) aplicaciones como lista desplegable, fuerza de ventas, ServiceNow, y mucho más.</span><span class="sxs-lookup"><span data-stu-id="74408-107">Azure Active Directory (Azure AD) identity synchronization (also called "provisioning") allows you to automate the creation, maintenance, and removal of identities in cloud (software as a service, or SaaS) applications such as Dropbox, Salesforce, ServiceNow, and more.</span></span> <span data-ttu-id="74408-108">Puede usar las API de sincronización en Microsoft Graph para administrar la sincronización de identidad mediante programación, incluidos:</span><span class="sxs-lookup"><span data-stu-id="74408-108">You can use the synchronization APIs in Microsoft Graph to manage identity synchronization programmatically, including:</span></span>

- <span data-ttu-id="74408-109">Crear, iniciar y detener los trabajos de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-109">Create, start, and stop synchronization jobs</span></span>
- <span data-ttu-id="74408-110">Realizar cambios en el esquema para los trabajos de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-110">Make changes to the synchronization schema for jobs</span></span>
- <span data-ttu-id="74408-111">Compruebe el estado actual de la sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-111">Verify the current synchronization status</span></span> 

<span data-ttu-id="74408-112">Para obtener más información acerca de la sincronización en Azure AD, consulte:</span><span class="sxs-lookup"><span data-stu-id="74408-112">For more information about synchronization in Azure AD, see:</span></span>

* [<span data-ttu-id="74408-113">Automatizar usuario aprovisionamiento y desaprovisionamiento a las aplicaciones de SaaS con Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="74408-113">Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-app-provisioning)
* [<span data-ttu-id="74408-114">Administración de la cuenta de usuario de aprovisionamiento de aplicaciones de empresa en el portal de Azure</span><span class="sxs-lookup"><span data-stu-id="74408-114">Managing user account provisioning for enterprise apps in the Azure portal</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-enterprise-apps-manage-provisioning)

<span data-ttu-id="74408-115">También puede intentar la API en el [Explorador de gráfico](https://developer.microsoft.com/graph/graph-explorer) en un inquilino de ejemplo o su propio inquilino.</span><span class="sxs-lookup"><span data-stu-id="74408-115">You can also try the API in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) in a sample tenant or your own tenant.</span></span>

## <a name="synchronization-job"></a><span data-ttu-id="74408-116">Trabajo de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-116">Synchronization job</span></span>

<span data-ttu-id="74408-117">Los trabajos de sincronización realizan la sincronización por sondeo para que los cambios en un directorio y la inserción de ellos en otro directorio, periódicamente que se ejecuta en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="74408-117">Synchronization jobs perform synchronization by periodically running in the background, polling for changes in one directory, and pushing them to another directory.</span></span> <span data-ttu-id="74408-118">El trabajo de sincronización siempre es específico de una instancia determinada de una aplicación en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="74408-118">The synchronization job is always specific to a particular instance of an application in your tenant.</span></span> <span data-ttu-id="74408-119">Como parte de la configuración del trabajo de sincronización, debe conceder autorización para leer y escribir objetos en el directorio de destino y personalizar el esquema de sincronización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="74408-119">As part of the synchronization job setup, you need to give authorization to read and write objects in your target directory, and customize the job's synchronization schema.</span></span>

<span data-ttu-id="74408-120">Para obtener más información, vea el [trabajo de sincronización](synchronization-synchronizationjob.md).</span><span class="sxs-lookup"><span data-stu-id="74408-120">For more information, see [synchronization job](synchronization-synchronizationjob.md).</span></span>

## <a name="synchronization-schema"></a><span data-ttu-id="74408-121">Esquema de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-121">Synchronization schema</span></span>

<span data-ttu-id="74408-122">El esquema de sincronización define cuáles serán los objetos sincronizados y cómo se sincronizarán.</span><span class="sxs-lookup"><span data-stu-id="74408-122">The synchronization schema defines what objects will be synchronized and how they will be synchronized.</span></span> <span data-ttu-id="74408-123">El esquema de sincronización contiene la mayoría de la información de configuración para un trabajo de sincronización determinado.</span><span class="sxs-lookup"><span data-stu-id="74408-123">The synchronization schema contains most of the setup information for a particular synchronization job.</span></span> <span data-ttu-id="74408-124">Normalmente, va a personalizar algunas de las [asignaciones de atributos](synchronization-attributemapping.md), o agregar un [filtro de ámbito](synchronization-filter.md) para sincronizar solo los objetos que cumplen una condición determinada.</span><span class="sxs-lookup"><span data-stu-id="74408-124">Typically, you will customize some of the [attribute mappings](synchronization-attributemapping.md), or add a [scoping filter](synchronization-filter.md) to synchronize only objects that satisfy a certain condition.</span></span>

<span data-ttu-id="74408-125">El esquema de sincronización incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="74408-125">The synchronization schema includes the following components:</span></span>

- <span data-ttu-id="74408-126">Definiciones de Active Directory</span><span class="sxs-lookup"><span data-stu-id="74408-126">Directory definitions</span></span>
- <span data-ttu-id="74408-127">Reglas de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-127">Synchronization rules</span></span>
- <span data-ttu-id="74408-128">Asignaciones de objetos</span><span class="sxs-lookup"><span data-stu-id="74408-128">Object mappings</span></span>

<span data-ttu-id="74408-129">Para obtener más información, vea [esquema de sincronización](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="74408-129">For more information, see [synchronization schema](synchronization-synchronizationschema.md).</span></span>

## <a name="synchronization-template"></a><span data-ttu-id="74408-130">Plantilla de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-130">Synchronization template</span></span>

<span data-ttu-id="74408-131">La plantilla de sincronización proporciona opciones de configuración de sincronización preconfigurado para una aplicación concreta.</span><span class="sxs-lookup"><span data-stu-id="74408-131">The synchronization template provides pre-configured synchronization settings for a particular application.</span></span> <span data-ttu-id="74408-132">Estas opciones de configuración (lo que es más importante, el [esquema de sincronización](synchronization-synchronizationschema.md)) se usará de forma predeterminada para cualquier [trabajo de sincronización](synchronization-synchronizationjob.md) que se basa en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="74408-132">These settings (most importantly, [synchronization schema](synchronization-synchronizationschema.md)) will be used by default for any [synchronization job](synchronization-synchronizationjob.md) that is based on the template.</span></span> <span data-ttu-id="74408-133">Las plantillas especificadas por el desarrollador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="74408-133">Templates are specified by the application developer.</span></span>

<span data-ttu-id="74408-134">Para obtener más información, vea [plantilla de sincronización](synchronization-synchronizationtemplate.md).</span><span class="sxs-lookup"><span data-stu-id="74408-134">For more information, see [synchronization template](synchronization-synchronizationtemplate.md).</span></span>

## <a name="working-with-the-synchronization-api"></a><span data-ttu-id="74408-135">Trabajar con la API de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-135">Working with the synchronization API</span></span>

<span data-ttu-id="74408-136">Trabajar con la sincronización de API principalmente implica el acceso a los recursos [synchronizationJob](synchronization-synchronizationjob.md) y [synchronizationSchema](synchronization-synchronizationschema.md) .</span><span class="sxs-lookup"><span data-stu-id="74408-136">Working with synchronization API primarily involves accessing the [synchronizationJob](synchronization-synchronizationjob.md) and [synchronizationSchema](synchronization-synchronizationschema.md) resources.</span></span> <span data-ttu-id="74408-137">Para encontrar el recurso [synchronizationJob](synchronization-synchronizationjob.md) , debe conocer el identificador del objeto entidad de seguridad que pertenece el trabajo de sincronización.</span><span class="sxs-lookup"><span data-stu-id="74408-137">To find your [synchronizationJob](synchronization-synchronizationjob.md) resource, you need to know the ID of the service principal object that the synchronization job belongs to.</span></span> <span data-ttu-id="74408-138">Los siguientes ejemplos muestran cómo trabajar con los recursos **synchronizationJob** y **synchronizationSchema** .</span><span class="sxs-lookup"><span data-stu-id="74408-138">The following examples show you how to work with the **synchronizationJob** and **synchronizationSchema** resources.</span></span>

### <a name="authorization"></a><span data-ttu-id="74408-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="74408-139">Authorization</span></span>

<span data-ttu-id="74408-140">La API de sincronización de Azure AD utiliza OAuth 2.0 para la autorización.</span><span class="sxs-lookup"><span data-stu-id="74408-140">The Azure AD synchronization API uses OAuth 2.0 for authorization.</span></span> <span data-ttu-id="74408-141">Antes de realizar las solicitudes de la API, debe obtener un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="74408-141">Before making any requests to the API, you need to get an access token.</span></span> <span data-ttu-id="74408-142">Para obtener más información, vea [tokens de acceso Get para llamar a Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview).</span><span class="sxs-lookup"><span data-stu-id="74408-142">For more information, see [Get access tokens to call Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview).</span></span> <span data-ttu-id="74408-143">Para obtener acceso a recursos de sincronización, la aplicación necesita permisos de Directory.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="74408-143">To access synchronization resources, your application needs Directory.ReadWrite.All permissions.</span></span> <span data-ttu-id="74408-144">Para obtener más información, vea [permisos de Active Directory](/graph/permissions-reference#directory-permissions).</span><span class="sxs-lookup"><span data-stu-id="74408-144">For more information, see [Directory permissions](/graph/permissions-reference#directory-permissions).</span></span>

### <a name="find-the-service-principal-object-by-display-name"></a><span data-ttu-id="74408-145">Busque el objeto de entidad de seguridad de servicio por nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="74408-145">Find the service principal object by display name</span></span>

<span data-ttu-id="74408-146">En el ejemplo siguiente se muestra cómo buscar el objeto de entidad de seguridad de servicio por nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="74408-146">The following example shows how to find service principal object by display name.</span></span>

<span data-ttu-id="74408-147">**Solicitud**</span><span class="sxs-lookup"><span data-stu-id="74408-147">**Request**</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/servicePrincipals?$select=id,appId,displayName&$filter=startswith(displayName, 'salesforce')
```

<span data-ttu-id="74408-148">**Response**</span><span class="sxs-lookup"><span data-stu-id="74408-148">**Response**</span></span>

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

### <a name="find-the-service-principal-object-by-app-id"></a><span data-ttu-id="74408-149">Buscar el objeto de entidad de seguridad de servicio por identificador de la aplicación</span><span class="sxs-lookup"><span data-stu-id="74408-149">Find the service principal object by app ID</span></span>

<span data-ttu-id="74408-150">En el ejemplo siguiente se muestra cómo buscar el objeto de entidad de seguridad de servicio por identificador de aplicación.</span><span class="sxs-lookup"><span data-stu-id="74408-150">The following example shows how to find the service principal object by app ID.</span></span>

<span data-ttu-id="74408-151">**Solicitud** 
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-151">**Request** 
<!-- { "blockType": "ignored" } --></span></span>
```http
GET https://graph.microsoft.com/beta/servicePrincipals?$select=id,appId,displayName&$filter=AppId eq '219561ee-1480-4c67-9aa6-63d861fae3ef'
```

<span data-ttu-id="74408-152">**Respuesta**
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-152">**Response**
<!-- { "blockType": "ignored" } --></span></span>
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

### <a name="list-existing-synchronization-jobs"></a><span data-ttu-id="74408-153">Lista de los trabajos de sincronización existente</span><span class="sxs-lookup"><span data-stu-id="74408-153">List existing synchronization jobs</span></span>

<span data-ttu-id="74408-154">En el ejemplo siguiente se muestra cómo obtener una lista de los trabajos de sincronización existente.</span><span class="sxs-lookup"><span data-stu-id="74408-154">The following example shows you how to list existing synchronization jobs.</span></span>

<span data-ttu-id="74408-155">**Solicitud**
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-155">**Request**
<!-- { "blockType": "ignored" } --></span></span>
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs
GET https://graph.microsoft.com/beta/servicePrincipals/60443998-8cf7-4e61-b05c-a53b658cb5e1/synchronization/jobs
```

<span data-ttu-id="74408-156">**Respuesta**
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-156">**Response**
<!-- { "blockType": "ignored" } --></span></span>
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

### <a name="get-synchronization-job-status"></a><span data-ttu-id="74408-157">Obtener el estado del trabajo de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-157">Get synchronization job status</span></span>
<span data-ttu-id="74408-158">En el ejemplo siguiente se muestra cómo obtener el estado de un trabajo de sincronización.</span><span class="sxs-lookup"><span data-stu-id="74408-158">The following example shows you how to get the status of a synchronization job.</span></span>

<span data-ttu-id="74408-159">**Solicitud**
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-159">**Request**
<!-- { "blockType": "ignored" } --></span></span>
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}

GET https://graph.microsoft.com/beta/servicePrincipals/60443998-8cf7-4e61-b05c-a53b658cb5e1/synchronization/jobs/SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa
```

<span data-ttu-id="74408-160">**Respuesta**
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-160">**Response**
<!-- { "blockType": "ignored" } --></span></span>
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

### <a name="get-synchronization-schema"></a><span data-ttu-id="74408-161">Obtener el esquema de sincronización</span><span class="sxs-lookup"><span data-stu-id="74408-161">Get synchronization schema</span></span>
<span data-ttu-id="74408-162">En el ejemplo siguiente se muestra cómo obtener el esquema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="74408-162">The following example shows you how to get the synchronization schema.</span></span>

<span data-ttu-id="74408-163">**Solicitud**
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-163">**Request**
<!-- { "blockType": "ignored" } --></span></span>
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
```

<span data-ttu-id="74408-164">**Respuesta**
<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="74408-164">**Response**
<!-- { "blockType": "ignored" } --></span></span>
```http
HTTP/1.1 200 OK
{
    "directories": [],
    "synchronizationRules": []
}
```
## <a name="see-also"></a><span data-ttu-id="74408-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="74408-165">See also</span></span>

* [<span data-ttu-id="74408-166">Configurar la sincronización con los atributos de extensión de Active directory</span><span class="sxs-lookup"><span data-stu-id="74408-166">Configure synchronization with directory extension attributes</span></span>](../resources/synchronization-configure-with-directory-extension-attributes.md)
* [<span data-ttu-id="74408-167">Configurar la sincronización con los atributos de destino personalizado</span><span class="sxs-lookup"><span data-stu-id="74408-167">Configure synchronization with custom target attributes</span></span>](../resources/synchronization-configure-with-custom-target-attributes.md)



