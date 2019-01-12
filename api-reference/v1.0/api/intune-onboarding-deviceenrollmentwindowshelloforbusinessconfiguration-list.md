---
title: Enumerar deviceEnrollmentWindowsHelloForBusinessConfigurations
description: Enumere las propiedades y las relaciones de los objetos deviceEnrollmentWindowsHelloForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 542b851e2750e3cf8c700f31cd503608bef60ce9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931254"
---
# <a name="list-deviceenrollmentwindowshelloforbusinessconfigurations"></a><span data-ttu-id="ed44e-103">Enumerar deviceEnrollmentWindowsHelloForBusinessConfigurations</span><span class="sxs-lookup"><span data-stu-id="ed44e-103">List deviceEnrollmentWindowsHelloForBusinessConfigurations</span></span>

> <span data-ttu-id="ed44e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed44e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed44e-105">Enumere las propiedades y las relaciones de los objetos [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ed44e-105">List properties and relationships of the [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ed44e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ed44e-106">Prerequisites</span></span>
<span data-ttu-id="ed44e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed44e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed44e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed44e-109">Permission type</span></span>|<span data-ttu-id="ed44e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed44e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ed44e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed44e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ed44e-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="ed44e-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="ed44e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed44e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ed44e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed44e-114">Not supported.</span></span>|
|<span data-ttu-id="ed44e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed44e-115">Application</span></span>|<span data-ttu-id="ed44e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed44e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ed44e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed44e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="ed44e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed44e-118">Request headers</span></span>
|<span data-ttu-id="ed44e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed44e-119">Header</span></span>|<span data-ttu-id="ed44e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ed44e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ed44e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ed44e-121">Authorization</span></span>|<span data-ttu-id="ed44e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ed44e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ed44e-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ed44e-123">Accept</span></span>|<span data-ttu-id="ed44e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ed44e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ed44e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed44e-125">Request body</span></span>
<span data-ttu-id="ed44e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ed44e-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ed44e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed44e-127">Response</span></span>
<span data-ttu-id="ed44e-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed44e-128">If successful, this method returns a `200 OK` response code and a collection of [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ed44e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed44e-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="ed44e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed44e-130">Request</span></span>
<span data-ttu-id="ed44e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed44e-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations
```

### <a name="response"></a><span data-ttu-id="ed44e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed44e-132">Response</span></span>
<span data-ttu-id="ed44e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed44e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 914

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
      "id": "3068e0cd-e0cd-3068-cde0-6830cde06830",
      "displayName": "Display Name value",
      "description": "Description value",
      "priority": 8,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "version": 7,
      "pinMinimumLength": 0,
      "pinMaximumLength": 0,
      "pinUppercaseCharactersUsage": "required",
      "pinLowercaseCharactersUsage": "required",
      "pinSpecialCharactersUsage": "required",
      "state": "enabled",
      "securityDeviceRequired": true,
      "unlockWithBiometricsEnabled": true,
      "remotePassportEnabled": true,
      "pinPreviousBlockCount": 5,
      "pinExpirationInDays": 3,
      "enhancedBiometricsState": "enabled"
    }
  ]
}
```



