---
title: getAssignedRoleIdsForLoggedInUser (función)
description: Recupera las definiciones de rol asignado y asignaciones de funciones del usuario autenticado actualmente.
author: tfitzmac
ms.openlocfilehash: 0e9cf6e45c0f7ce7e321d746d12648a598109df5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331097"
---
# <a name="getassignedroleidsforloggedinuser-function"></a><span data-ttu-id="ea93a-103">getAssignedRoleIdsForLoggedInUser (función)</span><span class="sxs-lookup"><span data-stu-id="ea93a-103">getAssignedRoleIdsForLoggedInUser function</span></span>

> <span data-ttu-id="ea93a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea93a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea93a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea93a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ea93a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea93a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea93a-107">Recupera las definiciones de rol asignado y asignaciones de funciones del usuario autenticado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ea93a-107">Retrieves the assigned role definitions and role assignments of the currently authenticated user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea93a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea93a-108">Prerequisites</span></span>
<span data-ttu-id="ea93a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea93a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea93a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea93a-111">Permission type</span></span>|<span data-ttu-id="ea93a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea93a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea93a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea93a-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="ea93a-114">&nbsp;&nbsp; **Control de acceso basado en roles (RBAC)**</span><span class="sxs-lookup"><span data-stu-id="ea93a-114">&nbsp; &nbsp; **Role-based access control (RBAC)**</span></span> | <span data-ttu-id="ea93a-115">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="ea93a-115">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="ea93a-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea93a-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea93a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea93a-117">Not supported.</span></span>|
|<span data-ttu-id="ea93a-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea93a-118">Application</span></span>|<span data-ttu-id="ea93a-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea93a-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea93a-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea93a-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/getAssignedRoleIdsForLoggedInUser
```

## <a name="request-headers"></a><span data-ttu-id="ea93a-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea93a-121">Request headers</span></span>
|<span data-ttu-id="ea93a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea93a-122">Header</span></span>|<span data-ttu-id="ea93a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ea93a-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea93a-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="ea93a-124">Authorization</span></span>|<span data-ttu-id="ea93a-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea93a-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea93a-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ea93a-126">Accept</span></span>|<span data-ttu-id="ea93a-127">application/json</span><span class="sxs-lookup"><span data-stu-id="ea93a-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea93a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea93a-128">Request body</span></span>
<span data-ttu-id="ea93a-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ea93a-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea93a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea93a-130">Response</span></span>
<span data-ttu-id="ea93a-131">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y un [deviceAndAppManagementAssignedRoleIds](../resources/intune-rbac-deviceandappmanagementassignedroleids.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea93a-131">If successful, this function returns a `200 OK` response code and a [deviceAndAppManagementAssignedRoleIds](../resources/intune-rbac-deviceandappmanagementassignedroleids.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea93a-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea93a-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea93a-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea93a-133">Request</span></span>
<span data-ttu-id="ea93a-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea93a-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/getAssignedRoleIdsForLoggedInUser
```

### <a name="response"></a><span data-ttu-id="ea93a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea93a-135">Response</span></span>
<span data-ttu-id="ea93a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea93a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 263

{
  "value": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignedRoleIds",
    "roleDefinitionIds": [
      "df52f163-f163-df52-63f1-52df63f152df"
    ],
    "roleAssignmentIds": [
      "1f35d53d-d53d-1f35-3dd5-351f3dd5351f"
    ]
  }
}
```





