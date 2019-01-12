---
title: Obtener roleScopeTag
description: Leer las propiedades y las relaciones del objeto roleScopeTag.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2a0126f4b39fbee3c154837661b368512e29ac97
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983292"
---
# <a name="get-rolescopetag"></a><span data-ttu-id="26f00-103">Obtener roleScopeTag</span><span class="sxs-lookup"><span data-stu-id="26f00-103">Get roleScopeTag</span></span>

> <span data-ttu-id="26f00-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26f00-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26f00-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26f00-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="26f00-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="26f00-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="26f00-107">Leer las propiedades y las relaciones del objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .</span><span class="sxs-lookup"><span data-stu-id="26f00-107">Read properties and relationships of the [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="26f00-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="26f00-108">Prerequisites</span></span>
<span data-ttu-id="26f00-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="26f00-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="26f00-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="26f00-111">Permission type</span></span>|<span data-ttu-id="26f00-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="26f00-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="26f00-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="26f00-113">Delegated (work or school account)</span></span>|<span data-ttu-id="26f00-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="26f00-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="26f00-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="26f00-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="26f00-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26f00-116">Not supported.</span></span>|
|<span data-ttu-id="26f00-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="26f00-117">Application</span></span>|<span data-ttu-id="26f00-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26f00-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="26f00-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="26f00-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleScopeTags/{roleScopeTagId}
GET /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/microsoft.graph.deviceAndAppManagementRoleAssignment/roleScopeTags/{roleScopeTagId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="26f00-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="26f00-120">Optional query parameters</span></span>
<span data-ttu-id="26f00-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26f00-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="26f00-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="26f00-122">Request headers</span></span>
|<span data-ttu-id="26f00-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26f00-123">Header</span></span>|<span data-ttu-id="26f00-124">Valor</span><span class="sxs-lookup"><span data-stu-id="26f00-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="26f00-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="26f00-125">Authorization</span></span>|<span data-ttu-id="26f00-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="26f00-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="26f00-127">Accept</span><span class="sxs-lookup"><span data-stu-id="26f00-127">Accept</span></span>|<span data-ttu-id="26f00-128">application/json</span><span class="sxs-lookup"><span data-stu-id="26f00-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="26f00-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="26f00-129">Request body</span></span>
<span data-ttu-id="26f00-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="26f00-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="26f00-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26f00-131">Response</span></span>
<span data-ttu-id="26f00-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [roleScopeTag](../resources/intune-rbac-rolescopetag.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26f00-132">If successful, this method returns a `200 OK` response code and [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="26f00-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26f00-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="26f00-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="26f00-134">Request</span></span>
<span data-ttu-id="26f00-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26f00-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/roleScopeTags/{roleScopeTagId}
```

### <a name="response"></a><span data-ttu-id="26f00-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26f00-136">Response</span></span>
<span data-ttu-id="26f00-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="26f00-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 209

{
  "value": {
    "@odata.type": "#microsoft.graph.roleScopeTag",
    "id": "9ed1e179-e179-9ed1-79e1-d19e79e1d19e",
    "displayName": "Display Name value",
    "description": "Description value"
  }
}
```





