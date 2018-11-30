---
title: Enumerar windows10MobileCompliancePolicies
description: Enumere las propiedades y las relaciones de los objetos windows10MobileCompliancePolicy.
ms.openlocfilehash: d2e0e17f3112be1ba90a99e2d94edc96b25a74fe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028958"
---
# <a name="list-windows10mobilecompliancepolicies"></a><span data-ttu-id="728dc-103">Enumerar windows10MobileCompliancePolicies</span><span class="sxs-lookup"><span data-stu-id="728dc-103">List windows10MobileCompliancePolicies</span></span>

> <span data-ttu-id="728dc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="728dc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="728dc-105">Enumere las propiedades y las relaciones de los objetos [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="728dc-105">List properties and relationships of the [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="728dc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="728dc-106">Prerequisites</span></span>
<span data-ttu-id="728dc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="728dc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="728dc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="728dc-109">Permission type</span></span>|<span data-ttu-id="728dc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="728dc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="728dc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="728dc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="728dc-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="728dc-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="728dc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="728dc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="728dc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="728dc-114">Not supported.</span></span>|
|<span data-ttu-id="728dc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="728dc-115">Application</span></span>|<span data-ttu-id="728dc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="728dc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="728dc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="728dc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="728dc-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="728dc-118">Request headers</span></span>
|<span data-ttu-id="728dc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="728dc-119">Header</span></span>|<span data-ttu-id="728dc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="728dc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="728dc-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="728dc-121">Authorization</span></span>|<span data-ttu-id="728dc-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="728dc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="728dc-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="728dc-123">Accept</span></span>|<span data-ttu-id="728dc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="728dc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="728dc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="728dc-125">Request body</span></span>
<span data-ttu-id="728dc-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="728dc-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="728dc-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="728dc-127">Response</span></span>
<span data-ttu-id="728dc-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="728dc-128">If successful, this method returns a `200 OK` response code and a collection of [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="728dc-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="728dc-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="728dc-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="728dc-130">Request</span></span>
<span data-ttu-id="728dc-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="728dc-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
```

### <a name="response"></a><span data-ttu-id="728dc-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="728dc-132">Response</span></span>
<span data-ttu-id="728dc-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="728dc-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1089

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windows10MobileCompliancePolicy",
      "id": "3d4237b0-37b0-3d42-b037-423db037423d",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "displayName": "Display Name value",
      "version": 7,
      "passwordRequired": true,
      "passwordBlockSimple": true,
      "passwordMinimumLength": 5,
      "passwordMinimumCharacterSetCount": 0,
      "passwordRequiredType": "alphanumeric",
      "passwordPreviousPasswordBlockCount": 2,
      "passwordExpirationDays": 6,
      "passwordMinutesOfInactivityBeforeLock": 5,
      "passwordRequireToUnlockFromIdle": true,
      "osMinimumVersion": "Os Minimum Version value",
      "osMaximumVersion": "Os Maximum Version value",
      "earlyLaunchAntiMalwareDriverEnabled": true,
      "bitLockerEnabled": true,
      "secureBootEnabled": true,
      "codeIntegrityEnabled": true,
      "storageRequireEncryption": true
    }
  ]
}
```



