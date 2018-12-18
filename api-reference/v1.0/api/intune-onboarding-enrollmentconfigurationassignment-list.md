---
title: Enumerar enrollmentConfigurationAssignments
description: Enumere las propiedades y las relaciones de los objetos enrollmentConfigurationAssignment.
author: tfitzmac
ms.openlocfilehash: d266cb9782e8be4e7e99fd10eef18680adbf4e40
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303874"
---
# <a name="list-enrollmentconfigurationassignments"></a><span data-ttu-id="b7d57-103">Enumerar enrollmentConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="b7d57-103">List enrollmentConfigurationAssignments</span></span>

> <span data-ttu-id="b7d57-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b7d57-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b7d57-105">Enumere las propiedades y las relaciones de los objetos [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b7d57-105">List properties and relationships of the [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b7d57-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b7d57-106">Prerequisites</span></span>
<span data-ttu-id="b7d57-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7d57-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7d57-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7d57-109">Permission type</span></span>|<span data-ttu-id="b7d57-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7d57-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b7d57-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7d57-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b7d57-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b7d57-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="b7d57-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7d57-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b7d57-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7d57-114">Not supported.</span></span>|
|<span data-ttu-id="b7d57-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7d57-115">Application</span></span>|<span data-ttu-id="b7d57-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7d57-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b7d57-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7d57-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="b7d57-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7d57-118">Request headers</span></span>
|<span data-ttu-id="b7d57-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7d57-119">Header</span></span>|<span data-ttu-id="b7d57-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7d57-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b7d57-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b7d57-121">Authorization</span></span>|<span data-ttu-id="b7d57-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b7d57-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b7d57-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b7d57-123">Accept</span></span>|<span data-ttu-id="b7d57-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b7d57-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b7d57-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7d57-125">Request body</span></span>
<span data-ttu-id="b7d57-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b7d57-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b7d57-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7d57-127">Response</span></span>
<span data-ttu-id="b7d57-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7d57-128">If successful, this method returns a `200 OK` response code and a collection of [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b7d57-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7d57-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b7d57-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7d57-130">Request</span></span>
<span data-ttu-id="b7d57-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7d57-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
```

### <a name="response"></a><span data-ttu-id="b7d57-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7d57-132">Response</span></span>
<span data-ttu-id="b7d57-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b7d57-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 275

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
      "id": "705b021c-021c-705b-1c02-5b701c025b70",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```



