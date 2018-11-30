---
title: Enumerar deviceEnrollmentPlatformRestrictionsConfigurations
description: Enumere las propiedades y las relaciones de los objetos deviceEnrollmentPlatformRestrictionsConfiguration.
ms.openlocfilehash: 006df0f78570d65c25aa2a619daee634d6921f34
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030231"
---
# <a name="list-deviceenrollmentplatformrestrictionsconfigurations"></a><span data-ttu-id="c720a-103">Enumerar deviceEnrollmentPlatformRestrictionsConfigurations</span><span class="sxs-lookup"><span data-stu-id="c720a-103">List deviceEnrollmentPlatformRestrictionsConfigurations</span></span>

> <span data-ttu-id="c720a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c720a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c720a-105">Enumere las propiedades y las relaciones de los objetos [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c720a-105">List properties and relationships of the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c720a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c720a-106">Prerequisites</span></span>
<span data-ttu-id="c720a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c720a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c720a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c720a-109">Permission type</span></span>|<span data-ttu-id="c720a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c720a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c720a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c720a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c720a-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="c720a-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="c720a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c720a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c720a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c720a-114">Not supported.</span></span>|
|<span data-ttu-id="c720a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c720a-115">Application</span></span>|<span data-ttu-id="c720a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c720a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c720a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c720a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="c720a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c720a-118">Request headers</span></span>
|<span data-ttu-id="c720a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c720a-119">Header</span></span>|<span data-ttu-id="c720a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c720a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c720a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="c720a-121">Authorization</span></span>|<span data-ttu-id="c720a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c720a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c720a-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c720a-123">Accept</span></span>|<span data-ttu-id="c720a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c720a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c720a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c720a-125">Request body</span></span>
<span data-ttu-id="c720a-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c720a-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c720a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c720a-127">Response</span></span>
<span data-ttu-id="c720a-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c720a-128">If successful, this method returns a `200 OK` response code and a collection of [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c720a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c720a-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="c720a-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c720a-130">Request</span></span>
<span data-ttu-id="c720a-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c720a-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations
```

### <a name="response"></a><span data-ttu-id="c720a-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c720a-132">Response</span></span>
<span data-ttu-id="c720a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c720a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2027

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
      "id": "3acb2d75-2d75-3acb-752d-cb3a752dcb3a",
      "displayName": "Display Name value",
      "description": "Description value",
      "priority": 8,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "version": 7,
      "iosRestriction": {
        "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
        "platformBlocked": true,
        "personalDeviceEnrollmentBlocked": true,
        "osMinimumVersion": "Os Minimum Version value",
        "osMaximumVersion": "Os Maximum Version value"
      },
      "windowsRestriction": {
        "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
        "platformBlocked": true,
        "personalDeviceEnrollmentBlocked": true,
        "osMinimumVersion": "Os Minimum Version value",
        "osMaximumVersion": "Os Maximum Version value"
      },
      "windowsMobileRestriction": {
        "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
        "platformBlocked": true,
        "personalDeviceEnrollmentBlocked": true,
        "osMinimumVersion": "Os Minimum Version value",
        "osMaximumVersion": "Os Maximum Version value"
      },
      "androidRestriction": {
        "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
        "platformBlocked": true,
        "personalDeviceEnrollmentBlocked": true,
        "osMinimumVersion": "Os Minimum Version value",
        "osMaximumVersion": "Os Maximum Version value"
      },
      "macOSRestriction": {
        "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
        "platformBlocked": true,
        "personalDeviceEnrollmentBlocked": true,
        "osMinimumVersion": "Os Minimum Version value",
        "osMaximumVersion": "Os Maximum Version value"
      }
    }
  ]
}
```



