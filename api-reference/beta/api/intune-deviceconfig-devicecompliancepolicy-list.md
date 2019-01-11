---
title: Enumerar deviceCompliancePolicies
description: Enumere las propiedades y las relaciones de los objetos deviceCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 74f14e69ab4146f82b15476ccacb62e6ee0111fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891115"
---
# <a name="list-devicecompliancepolicies"></a><span data-ttu-id="a2368-103">Enumerar deviceCompliancePolicies</span><span class="sxs-lookup"><span data-stu-id="a2368-103">List deviceCompliancePolicies</span></span>

> <span data-ttu-id="a2368-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2368-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2368-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2368-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a2368-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2368-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2368-107">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a2368-107">List properties and relationships of the [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a2368-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a2368-108">Prerequisites</span></span>
<span data-ttu-id="a2368-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2368-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2368-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2368-111">Permission type</span></span>|<span data-ttu-id="a2368-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2368-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a2368-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2368-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a2368-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a2368-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a2368-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2368-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a2368-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2368-116">Not supported.</span></span>|
|<span data-ttu-id="a2368-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2368-117">Application</span></span>|<span data-ttu-id="a2368-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2368-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a2368-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2368-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="a2368-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2368-120">Request headers</span></span>
|<span data-ttu-id="a2368-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2368-121">Header</span></span>|<span data-ttu-id="a2368-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a2368-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a2368-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a2368-123">Authorization</span></span>|<span data-ttu-id="a2368-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a2368-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a2368-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a2368-125">Accept</span></span>|<span data-ttu-id="a2368-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a2368-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a2368-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2368-127">Request body</span></span>
<span data-ttu-id="a2368-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a2368-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a2368-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2368-129">Response</span></span>
<span data-ttu-id="a2368-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2368-130">If successful, this method returns a `200 OK` response code and a collection of [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2368-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2368-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="a2368-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2368-132">Request</span></span>
<span data-ttu-id="a2368-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2368-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies
```

### <a name="response"></a><span data-ttu-id="a2368-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2368-134">Response</span></span>
<span data-ttu-id="a2368-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2368-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 467

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceCompliancePolicy",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "id": "4214b716-b716-4214-16b7-144216b71442",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "displayName": "Display Name value",
      "version": 7
    }
  ]
}
```





