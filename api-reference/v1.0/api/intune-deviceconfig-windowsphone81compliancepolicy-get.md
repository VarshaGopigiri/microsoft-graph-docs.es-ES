---
title: Obtener windowsPhone81CompliancePolicy
description: Lea las propiedades y las relaciones del objeto windowsPhone81CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1ee9e9d8569d8fc574537df27e18266b75e640ab
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939542"
---
# <a name="get-windowsphone81compliancepolicy"></a><span data-ttu-id="e9163-103">Obtener windowsPhone81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="e9163-103">Get windowsPhone81CompliancePolicy</span></span>

> <span data-ttu-id="e9163-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9163-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9163-105">Lea las propiedades y las relaciones del objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e9163-105">Read properties and relationships of the [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9163-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9163-106">Prerequisites</span></span>
<span data-ttu-id="e9163-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9163-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9163-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9163-109">Permission type</span></span>|<span data-ttu-id="e9163-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9163-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e9163-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9163-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e9163-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9163-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="e9163-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9163-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e9163-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9163-114">Not supported.</span></span>|
|<span data-ttu-id="e9163-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9163-115">Application</span></span>|<span data-ttu-id="e9163-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9163-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e9163-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9163-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e9163-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e9163-118">Optional query parameters</span></span>
<span data-ttu-id="e9163-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9163-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e9163-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9163-120">Request headers</span></span>
|<span data-ttu-id="e9163-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9163-121">Header</span></span>|<span data-ttu-id="e9163-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e9163-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e9163-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e9163-123">Authorization</span></span>|<span data-ttu-id="e9163-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e9163-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e9163-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e9163-125">Accept</span></span>|<span data-ttu-id="e9163-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e9163-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e9163-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9163-127">Request body</span></span>
<span data-ttu-id="e9163-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e9163-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e9163-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9163-129">Response</span></span>
<span data-ttu-id="e9163-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9163-130">If successful, this method returns a `200 OK` response code and [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9163-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9163-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="e9163-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9163-132">Request</span></span>
<span data-ttu-id="e9163-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9163-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="e9163-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9163-134">Response</span></span>
<span data-ttu-id="e9163-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9163-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 834

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsPhone81CompliancePolicy",
    "id": "e6021ad4-1ad4-e602-d41a-02e6d41a02e6",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "passwordBlockSimple": true,
    "passwordExpirationDays": 6,
    "passwordMinimumLength": 5,
    "passwordMinutesOfInactivityBeforeLock": 5,
    "passwordMinimumCharacterSetCount": 0,
    "passwordRequiredType": "alphanumeric",
    "passwordPreviousPasswordBlockCount": 2,
    "passwordRequired": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value",
    "storageRequireEncryption": true
  }
}
```



