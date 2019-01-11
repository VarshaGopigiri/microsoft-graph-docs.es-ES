---
title: Obtener deviceEnrollmentWindowsHelloForBusinessConfiguration
description: Lea las propiedades y las relaciones del objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8152ad5a578c210214aa26508b31efcc7d96baef
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882274"
---
# <a name="get-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="c849e-103">Obtener deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="c849e-103">Get deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="c849e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c849e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c849e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c849e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c849e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c849e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c849e-107">Lea las propiedades y las relaciones del objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c849e-107">Read properties and relationships of the [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c849e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c849e-108">Prerequisites</span></span>
<span data-ttu-id="c849e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c849e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c849e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c849e-111">Permission type</span></span>|<span data-ttu-id="c849e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c849e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c849e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c849e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c849e-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="c849e-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="c849e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c849e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c849e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c849e-116">Not supported.</span></span>|
|<span data-ttu-id="c849e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c849e-117">Application</span></span>|<span data-ttu-id="c849e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c849e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c849e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c849e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c849e-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c849e-120">Optional query parameters</span></span>
<span data-ttu-id="c849e-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c849e-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c849e-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c849e-122">Request headers</span></span>
|<span data-ttu-id="c849e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c849e-123">Header</span></span>|<span data-ttu-id="c849e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c849e-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c849e-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="c849e-125">Authorization</span></span>|<span data-ttu-id="c849e-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c849e-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c849e-127">Accept</span><span class="sxs-lookup"><span data-stu-id="c849e-127">Accept</span></span>|<span data-ttu-id="c849e-128">application/json</span><span class="sxs-lookup"><span data-stu-id="c849e-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c849e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c849e-129">Request body</span></span>
<span data-ttu-id="c849e-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c849e-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c849e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c849e-131">Response</span></span>
<span data-ttu-id="c849e-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c849e-132">If successful, this method returns a `200 OK` response code and [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c849e-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c849e-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="c849e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c849e-134">Request</span></span>
<span data-ttu-id="c849e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c849e-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

### <a name="response"></a><span data-ttu-id="c849e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c849e-136">Response</span></span>
<span data-ttu-id="c849e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c849e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 860

{
  "value": {
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
}
```





