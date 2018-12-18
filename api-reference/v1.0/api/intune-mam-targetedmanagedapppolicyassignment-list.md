---
title: Enumerar targetedManagedAppPolicyAssignments
description: Enumere las propiedades y los relaciones de los objetos targetedManagedAppPolicyAssignment.
author: tfitzmac
ms.openlocfilehash: bc482707ee2c58e5778df68926f997f20ef68801
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362569"
---
# <a name="list-targetedmanagedapppolicyassignments"></a><span data-ttu-id="f7607-103">Enumerar targetedManagedAppPolicyAssignments</span><span class="sxs-lookup"><span data-stu-id="f7607-103">List targetedManagedAppPolicyAssignments</span></span>

> <span data-ttu-id="f7607-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f7607-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f7607-105">Enumere las propiedades y los relaciones de los objetos [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="f7607-105">List properties and relationships of the [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f7607-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f7607-106">Prerequisites</span></span>
<span data-ttu-id="f7607-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f7607-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f7607-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7607-109">Permission type</span></span>|<span data-ttu-id="f7607-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7607-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f7607-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7607-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f7607-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="f7607-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="f7607-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7607-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f7607-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7607-114">Not supported.</span></span>|
|<span data-ttu-id="f7607-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7607-115">Application</span></span>|<span data-ttu-id="f7607-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7607-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f7607-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7607-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments
GET /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/assignments
GET /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/assignments
GET /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/assignments
GET /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="f7607-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7607-118">Request headers</span></span>
|<span data-ttu-id="f7607-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7607-119">Header</span></span>|<span data-ttu-id="f7607-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f7607-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f7607-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f7607-121">Authorization</span></span>|<span data-ttu-id="f7607-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f7607-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f7607-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f7607-123">Accept</span></span>|<span data-ttu-id="f7607-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f7607-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f7607-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7607-125">Request body</span></span>
<span data-ttu-id="f7607-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f7607-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f7607-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7607-127">Response</span></span>
<span data-ttu-id="f7607-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7607-128">If successful, this method returns a `200 OK` response code and a collection of [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f7607-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7607-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f7607-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7607-130">Request</span></span>
<span data-ttu-id="f7607-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7607-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments
```

### <a name="response"></a><span data-ttu-id="f7607-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7607-132">Response</span></span>
<span data-ttu-id="f7607-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f7607-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 276

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
      "id": "8b68c4a6-c4a6-8b68-a6c4-688ba6c4688b",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```



