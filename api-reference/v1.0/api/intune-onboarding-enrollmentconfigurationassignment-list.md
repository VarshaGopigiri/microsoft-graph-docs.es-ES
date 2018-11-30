---
title: Enumerar enrollmentConfigurationAssignments
description: Enumere las propiedades y las relaciones de los objetos enrollmentConfigurationAssignment.
ms.openlocfilehash: baeba282dccfbb72821ae75f53e4771771854b14
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030655"
---
# <a name="list-enrollmentconfigurationassignments"></a><span data-ttu-id="6c49c-103">Enumerar enrollmentConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="6c49c-103">List enrollmentConfigurationAssignments</span></span>

> <span data-ttu-id="6c49c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6c49c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6c49c-105">Enumere las propiedades y las relaciones de los objetos [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6c49c-105">List properties and relationships of the [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6c49c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6c49c-106">Prerequisites</span></span>
<span data-ttu-id="6c49c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6c49c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6c49c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c49c-109">Permission type</span></span>|<span data-ttu-id="6c49c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c49c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6c49c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c49c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6c49c-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="6c49c-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="6c49c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c49c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6c49c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c49c-114">Not supported.</span></span>|
|<span data-ttu-id="6c49c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c49c-115">Application</span></span>|<span data-ttu-id="6c49c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c49c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6c49c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c49c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="6c49c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c49c-118">Request headers</span></span>
|<span data-ttu-id="6c49c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c49c-119">Header</span></span>|<span data-ttu-id="6c49c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6c49c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6c49c-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6c49c-121">Authorization</span></span>|<span data-ttu-id="6c49c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6c49c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6c49c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6c49c-123">Accept</span></span>|<span data-ttu-id="6c49c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6c49c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6c49c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c49c-125">Request body</span></span>
<span data-ttu-id="6c49c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6c49c-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6c49c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c49c-127">Response</span></span>
<span data-ttu-id="6c49c-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c49c-128">If successful, this method returns a `200 OK` response code and a collection of [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6c49c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c49c-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="6c49c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c49c-130">Request</span></span>
<span data-ttu-id="6c49c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c49c-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
```

### <a name="response"></a><span data-ttu-id="6c49c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c49c-132">Response</span></span>
<span data-ttu-id="6c49c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c49c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


