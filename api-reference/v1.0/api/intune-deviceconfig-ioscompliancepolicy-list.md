---
title: Enumerar iosCompliancePolicies
description: Enumere las propiedades y las relaciones de los objetos iosCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 42c44fd4acfbde69982380a191c32a5c07bdd59e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924562"
---
# <a name="list-ioscompliancepolicies"></a><span data-ttu-id="25994-103">Enumerar iosCompliancePolicies</span><span class="sxs-lookup"><span data-stu-id="25994-103">List iosCompliancePolicies</span></span>

> <span data-ttu-id="25994-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25994-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25994-105">Enumere las propiedades y las relaciones de los objetos [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="25994-105">List properties and relationships of the [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="25994-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25994-106">Prerequisites</span></span>
<span data-ttu-id="25994-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25994-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25994-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25994-109">Permission type</span></span>|<span data-ttu-id="25994-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25994-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="25994-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25994-111">Delegated (work or school account)</span></span>|<span data-ttu-id="25994-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="25994-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="25994-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25994-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="25994-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25994-114">Not supported.</span></span>|
|<span data-ttu-id="25994-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25994-115">Application</span></span>|<span data-ttu-id="25994-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25994-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="25994-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25994-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="25994-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25994-118">Request headers</span></span>
|<span data-ttu-id="25994-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25994-119">Header</span></span>|<span data-ttu-id="25994-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25994-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="25994-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="25994-121">Authorization</span></span>|<span data-ttu-id="25994-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="25994-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="25994-123">Accept</span><span class="sxs-lookup"><span data-stu-id="25994-123">Accept</span></span>|<span data-ttu-id="25994-124">application/json</span><span class="sxs-lookup"><span data-stu-id="25994-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="25994-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25994-125">Request body</span></span>
<span data-ttu-id="25994-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="25994-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="25994-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25994-127">Response</span></span>
<span data-ttu-id="25994-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25994-128">If successful, this method returns a `200 OK` response code and a collection of [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25994-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25994-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="25994-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25994-130">Request</span></span>
<span data-ttu-id="25994-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25994-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
```

### <a name="response"></a><span data-ttu-id="25994-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25994-132">Response</span></span>
<span data-ttu-id="25994-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25994-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1034

{
  "value": [
    {
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
  ]
}
```



