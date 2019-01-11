---
title: Enumerar deviceEnrollmentLimitConfigurations
description: Enumere las propiedades y las relaciones de los objetos deviceEnrollmentLimitConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ed0970122783f7c134268db7910ab03e15029ba7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848715"
---
# <a name="list-deviceenrollmentlimitconfigurations"></a><span data-ttu-id="cd0d7-103">Enumerar deviceEnrollmentLimitConfigurations</span><span class="sxs-lookup"><span data-stu-id="cd0d7-103">List deviceEnrollmentLimitConfigurations</span></span>

> <span data-ttu-id="cd0d7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd0d7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cd0d7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cd0d7-107">Enumere las propiedades y las relaciones de los objetos [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cd0d7-107">List properties and relationships of the [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cd0d7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cd0d7-108">Prerequisites</span></span>
<span data-ttu-id="cd0d7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd0d7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cd0d7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd0d7-111">Permission type</span></span>|<span data-ttu-id="cd0d7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd0d7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cd0d7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd0d7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cd0d7-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="cd0d7-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="cd0d7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd0d7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cd0d7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-116">Not supported.</span></span>|
|<span data-ttu-id="cd0d7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd0d7-117">Application</span></span>|<span data-ttu-id="cd0d7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cd0d7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd0d7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="cd0d7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd0d7-120">Request headers</span></span>
|<span data-ttu-id="cd0d7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd0d7-121">Header</span></span>|<span data-ttu-id="cd0d7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cd0d7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cd0d7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cd0d7-123">Authorization</span></span>|<span data-ttu-id="cd0d7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cd0d7-125">Accept</span><span class="sxs-lookup"><span data-stu-id="cd0d7-125">Accept</span></span>|<span data-ttu-id="cd0d7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cd0d7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cd0d7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd0d7-127">Request body</span></span>
<span data-ttu-id="cd0d7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cd0d7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd0d7-129">Response</span></span>
<span data-ttu-id="cd0d7-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-130">If successful, this method returns a `200 OK` response code and a collection of [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cd0d7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd0d7-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="cd0d7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd0d7-132">Request</span></span>
<span data-ttu-id="cd0d7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations
```

### <a name="response"></a><span data-ttu-id="cd0d7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd0d7-134">Response</span></span>
<span data-ttu-id="cd0d7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cd0d7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 446

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceEnrollmentLimitConfiguration",
      "id": "4f8c4e4c-4e4c-4f8c-4c4e-8c4f4c4e8c4f",
      "displayName": "Display Name value",
      "description": "Description value",
      "priority": 8,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "version": 7,
      "limit": 5
    }
  ]
}
```





