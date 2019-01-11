---
title: Enumerar windowsPhone81CompliancePolicies
description: Enumere las propiedades y las relaciones de los objetos windowsPhone81CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6f5dc8242d3f76cf9c96e9d7232542f147a94a8c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890408"
---
# <a name="list-windowsphone81compliancepolicies"></a><span data-ttu-id="c43f4-103">Enumerar windowsPhone81CompliancePolicies</span><span class="sxs-lookup"><span data-stu-id="c43f4-103">List windowsPhone81CompliancePolicies</span></span>

> <span data-ttu-id="c43f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c43f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c43f4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c43f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c43f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c43f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c43f4-107">Enumere las propiedades y las relaciones de los objetos [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c43f4-107">List properties and relationships of the [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c43f4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c43f4-108">Prerequisites</span></span>
<span data-ttu-id="c43f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c43f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c43f4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c43f4-111">Permission type</span></span>|<span data-ttu-id="c43f4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c43f4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c43f4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c43f4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c43f4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="c43f4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="c43f4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c43f4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c43f4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c43f4-116">Not supported.</span></span>|
|<span data-ttu-id="c43f4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c43f4-117">Application</span></span>|<span data-ttu-id="c43f4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c43f4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c43f4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c43f4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="c43f4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c43f4-120">Request headers</span></span>
|<span data-ttu-id="c43f4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c43f4-121">Header</span></span>|<span data-ttu-id="c43f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c43f4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c43f4-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="c43f4-123">Authorization</span></span>|<span data-ttu-id="c43f4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c43f4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c43f4-125">Accept</span><span class="sxs-lookup"><span data-stu-id="c43f4-125">Accept</span></span>|<span data-ttu-id="c43f4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c43f4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c43f4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c43f4-127">Request body</span></span>
<span data-ttu-id="c43f4-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c43f4-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c43f4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c43f4-129">Response</span></span>
<span data-ttu-id="c43f4-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c43f4-130">If successful, this method returns a `200 OK` response code and a collection of [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c43f4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c43f4-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="c43f4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c43f4-132">Request</span></span>
<span data-ttu-id="c43f4-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c43f4-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies
```

### <a name="response"></a><span data-ttu-id="c43f4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c43f4-134">Response</span></span>
<span data-ttu-id="c43f4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c43f4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 958

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsPhone81CompliancePolicy",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
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
  ]
}
```





