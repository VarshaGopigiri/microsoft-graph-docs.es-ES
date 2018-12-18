---
title: Obtener roleScopeTag
description: Leer las propiedades y las relaciones del objeto roleScopeTag.
author: tfitzmac
ms.openlocfilehash: 788cfcce79bd451822c1c6a4c85d156a2cae9f1f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321052"
---
# <a name="get-rolescopetag"></a><span data-ttu-id="ea4e8-103">Obtener roleScopeTag</span><span class="sxs-lookup"><span data-stu-id="ea4e8-103">Get roleScopeTag</span></span>

> <span data-ttu-id="ea4e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea4e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ea4e8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea4e8-107">Leer las propiedades y las relaciones del objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4e8-107">Read properties and relationships of the [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea4e8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea4e8-108">Prerequisites</span></span>
<span data-ttu-id="ea4e8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea4e8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea4e8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea4e8-111">Permission type</span></span>|<span data-ttu-id="ea4e8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea4e8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea4e8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea4e8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ea4e8-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="ea4e8-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="ea4e8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea4e8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea4e8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-116">Not supported.</span></span>|
|<span data-ttu-id="ea4e8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea4e8-117">Application</span></span>|<span data-ttu-id="ea4e8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea4e8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea4e8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleScopeTags/{roleScopeTagId}
GET /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/microsoft.graph.deviceAndAppManagementRoleAssignment/roleScopeTags/{roleScopeTagId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ea4e8-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ea4e8-120">Optional query parameters</span></span>
<span data-ttu-id="ea4e8-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ea4e8-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4e8-122">Request headers</span></span>
|<span data-ttu-id="ea4e8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea4e8-123">Header</span></span>|<span data-ttu-id="ea4e8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ea4e8-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea4e8-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="ea4e8-125">Authorization</span></span>|<span data-ttu-id="ea4e8-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea4e8-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ea4e8-127">Accept</span></span>|<span data-ttu-id="ea4e8-128">application/json</span><span class="sxs-lookup"><span data-stu-id="ea4e8-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea4e8-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4e8-129">Request body</span></span>
<span data-ttu-id="ea4e8-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea4e8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea4e8-131">Response</span></span>
<span data-ttu-id="ea4e8-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [roleScopeTag](../resources/intune-rbac-rolescopetag.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-132">If successful, this method returns a `200 OK` response code and [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea4e8-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea4e8-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea4e8-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4e8-134">Request</span></span>
<span data-ttu-id="ea4e8-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/roleScopeTags/{roleScopeTagId}
```

### <a name="response"></a><span data-ttu-id="ea4e8-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea4e8-136">Response</span></span>
<span data-ttu-id="ea4e8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea4e8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





