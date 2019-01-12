---
title: Obtener targetedManagedAppPolicyAssignment
description: Lea las propiedades y los relaciones del objeto targetedManagedAppPolicyAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a4d630c1981ea543df37a558e0dd0dd05b8fa325
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952947"
---
# <a name="get-targetedmanagedapppolicyassignment"></a><span data-ttu-id="17192-103">Obtener targetedManagedAppPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="17192-103">Get targetedManagedAppPolicyAssignment</span></span>

> <span data-ttu-id="17192-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17192-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17192-105">Lea las propiedades y los relaciones del objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="17192-105">Read properties and relationships of the [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="17192-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="17192-106">Prerequisites</span></span>
<span data-ttu-id="17192-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17192-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17192-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17192-109">Permission type</span></span>|<span data-ttu-id="17192-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17192-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="17192-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17192-111">Delegated (work or school account)</span></span>|<span data-ttu-id="17192-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="17192-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="17192-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17192-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="17192-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17192-114">Not supported.</span></span>|
|<span data-ttu-id="17192-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17192-115">Application</span></span>|<span data-ttu-id="17192-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17192-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="17192-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17192-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
GET /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
GET /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/assignments/{targetedManagedAppPolicyAssignmentId}
GET /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/assignments/{targetedManagedAppPolicyAssignmentId}
GET /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/assignments/{targetedManagedAppPolicyAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="17192-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="17192-118">Optional query parameters</span></span>
<span data-ttu-id="17192-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17192-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="17192-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17192-120">Request headers</span></span>
|<span data-ttu-id="17192-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17192-121">Header</span></span>|<span data-ttu-id="17192-122">Valor</span><span class="sxs-lookup"><span data-stu-id="17192-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="17192-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="17192-123">Authorization</span></span>|<span data-ttu-id="17192-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="17192-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="17192-125">Accept</span><span class="sxs-lookup"><span data-stu-id="17192-125">Accept</span></span>|<span data-ttu-id="17192-126">application/json</span><span class="sxs-lookup"><span data-stu-id="17192-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="17192-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17192-127">Request body</span></span>
<span data-ttu-id="17192-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17192-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17192-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17192-129">Response</span></span>
<span data-ttu-id="17192-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17192-130">If successful, this method returns a `200 OK` response code and [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17192-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17192-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="17192-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17192-132">Request</span></span>
<span data-ttu-id="17192-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17192-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
```

### <a name="response"></a><span data-ttu-id="17192-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17192-134">Response</span></span>
<span data-ttu-id="17192-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17192-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 252

{
  "value": {
    "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
    "id": "8b68c4a6-c4a6-8b68-a6c4-688ba6c4688b",
    "target": {
      "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
    }
  }
}
```



