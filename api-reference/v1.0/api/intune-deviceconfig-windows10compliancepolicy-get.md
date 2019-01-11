---
title: Obtener windows10CompliancePolicy
description: Lea las propiedades y las relaciones del objeto windows10CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 592666fb0d0e2edb50c4746af7d4d5228023c472
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885956"
---
# <a name="get-windows10compliancepolicy"></a><span data-ttu-id="b6fb1-103">Obtener windows10CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="b6fb1-103">Get windows10CompliancePolicy</span></span>

> <span data-ttu-id="b6fb1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b6fb1-105">Lea las propiedades y las relaciones del objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b6fb1-105">Read properties and relationships of the [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6fb1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6fb1-106">Prerequisites</span></span>
<span data-ttu-id="b6fb1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6fb1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6fb1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6fb1-109">Permission type</span></span>|<span data-ttu-id="b6fb1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6fb1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b6fb1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6fb1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b6fb1-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6fb1-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b6fb1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6fb1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b6fb1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-114">Not supported.</span></span>|
|<span data-ttu-id="b6fb1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6fb1-115">Application</span></span>|<span data-ttu-id="b6fb1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b6fb1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6fb1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b6fb1-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b6fb1-118">Optional query parameters</span></span>
<span data-ttu-id="b6fb1-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b6fb1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6fb1-120">Request headers</span></span>
|<span data-ttu-id="b6fb1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6fb1-121">Header</span></span>|<span data-ttu-id="b6fb1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b6fb1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b6fb1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b6fb1-123">Authorization</span></span>|<span data-ttu-id="b6fb1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b6fb1-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b6fb1-125">Accept</span></span>|<span data-ttu-id="b6fb1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b6fb1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6fb1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6fb1-127">Request body</span></span>
<span data-ttu-id="b6fb1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6fb1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6fb1-129">Response</span></span>
<span data-ttu-id="b6fb1-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-130">If successful, this method returns a `200 OK` response code and [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6fb1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6fb1-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="b6fb1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6fb1-132">Request</span></span>
<span data-ttu-id="b6fb1-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="b6fb1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6fb1-134">Response</span></span>
<span data-ttu-id="b6fb1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6fb1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1197

{
  "value": {
    "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
    "id": "2919ae62-ae62-2919-62ae-192962ae1929",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "passwordRequired": true,
    "passwordBlockSimple": true,
    "passwordRequiredToUnlockFromIdle": true,
    "passwordMinutesOfInactivityBeforeLock": 5,
    "passwordExpirationDays": 6,
    "passwordMinimumLength": 5,
    "passwordMinimumCharacterSetCount": 0,
    "passwordRequiredType": "alphanumeric",
    "passwordPreviousPasswordBlockCount": 2,
    "requireHealthyDeviceReport": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value",
    "mobileOsMinimumVersion": "Mobile Os Minimum Version value",
    "mobileOsMaximumVersion": "Mobile Os Maximum Version value",
    "earlyLaunchAntiMalwareDriverEnabled": true,
    "bitLockerEnabled": true,
    "secureBootEnabled": true,
    "codeIntegrityEnabled": true,
    "storageRequireEncryption": true
  }
}
```



