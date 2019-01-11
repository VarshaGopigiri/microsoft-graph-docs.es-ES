---
title: Obtener iosCompliancePolicy
description: Lea las propiedades y las relaciones del objeto iosCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: cfd7ea092053f6dd728b8a984a0a64292400bd8b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855555"
---
# <a name="get-ioscompliancepolicy"></a><span data-ttu-id="161ec-103">Obtener iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="161ec-103">Get iosCompliancePolicy</span></span>

> <span data-ttu-id="161ec-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="161ec-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="161ec-105">Lea las propiedades y las relaciones del objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="161ec-105">Read properties and relationships of the [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="161ec-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="161ec-106">Prerequisites</span></span>
<span data-ttu-id="161ec-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="161ec-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="161ec-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="161ec-109">Permission type</span></span>|<span data-ttu-id="161ec-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="161ec-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="161ec-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="161ec-111">Delegated (work or school account)</span></span>|<span data-ttu-id="161ec-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="161ec-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="161ec-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="161ec-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="161ec-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="161ec-114">Not supported.</span></span>|
|<span data-ttu-id="161ec-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="161ec-115">Application</span></span>|<span data-ttu-id="161ec-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="161ec-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="161ec-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="161ec-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="161ec-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="161ec-118">Optional query parameters</span></span>
<span data-ttu-id="161ec-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="161ec-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="161ec-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="161ec-120">Request headers</span></span>
|<span data-ttu-id="161ec-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="161ec-121">Header</span></span>|<span data-ttu-id="161ec-122">Valor</span><span class="sxs-lookup"><span data-stu-id="161ec-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="161ec-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="161ec-123">Authorization</span></span>|<span data-ttu-id="161ec-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="161ec-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="161ec-125">Accept</span><span class="sxs-lookup"><span data-stu-id="161ec-125">Accept</span></span>|<span data-ttu-id="161ec-126">application/json</span><span class="sxs-lookup"><span data-stu-id="161ec-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="161ec-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="161ec-127">Request body</span></span>
<span data-ttu-id="161ec-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="161ec-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="161ec-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="161ec-129">Response</span></span>
<span data-ttu-id="161ec-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="161ec-130">If successful, this method returns a `200 OK` response code and [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="161ec-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="161ec-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="161ec-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="161ec-132">Request</span></span>
<span data-ttu-id="161ec-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="161ec-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="161ec-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="161ec-134">Response</span></span>
<span data-ttu-id="161ec-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="161ec-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 978

{
  "value": {
    "@odata.type": "#microsoft.graph.iosCompliancePolicy",
    "id": "4f501351-1351-4f50-5113-504f5113504f",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "passcodeBlockSimple": true,
    "passcodeExpirationDays": 6,
    "passcodeMinimumLength": 5,
    "passcodeMinutesOfInactivityBeforeLock": 5,
    "passcodePreviousPasscodeBlockCount": 2,
    "passcodeMinimumCharacterSetCount": 0,
    "passcodeRequiredType": "alphanumeric",
    "passcodeRequired": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value",
    "securityBlockJailbrokenDevices": true,
    "deviceThreatProtectionEnabled": true,
    "deviceThreatProtectionRequiredSecurityLevel": "secured",
    "managedEmailProfileRequired": true
  }
}
```



