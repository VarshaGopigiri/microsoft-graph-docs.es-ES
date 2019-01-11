---
title: Enumerar macOSDeviceFeaturesConfigurations
description: Enumere las propiedades y las relaciones de los objetos macOSDeviceFeaturesConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7ff3369ef4348a4a677fff8c708cbefa09f8beab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884998"
---
# <a name="list-macosdevicefeaturesconfigurations"></a><span data-ttu-id="5bfd7-103">Enumerar macOSDeviceFeaturesConfigurations</span><span class="sxs-lookup"><span data-stu-id="5bfd7-103">List macOSDeviceFeaturesConfigurations</span></span>

> <span data-ttu-id="5bfd7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5bfd7-105">Enumere las propiedades y las relaciones de los objetos [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5bfd7-105">List properties and relationships of the [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5bfd7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5bfd7-106">Prerequisites</span></span>
<span data-ttu-id="5bfd7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5bfd7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5bfd7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5bfd7-109">Permission type</span></span>|<span data-ttu-id="5bfd7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5bfd7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5bfd7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5bfd7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5bfd7-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="5bfd7-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="5bfd7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5bfd7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5bfd7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-114">Not supported.</span></span>|
|<span data-ttu-id="5bfd7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5bfd7-115">Application</span></span>|<span data-ttu-id="5bfd7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5bfd7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5bfd7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="5bfd7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5bfd7-118">Request headers</span></span>
|<span data-ttu-id="5bfd7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bfd7-119">Header</span></span>|<span data-ttu-id="5bfd7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5bfd7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5bfd7-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="5bfd7-121">Authorization</span></span>|<span data-ttu-id="5bfd7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5bfd7-123">Accept</span><span class="sxs-lookup"><span data-stu-id="5bfd7-123">Accept</span></span>|<span data-ttu-id="5bfd7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5bfd7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5bfd7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5bfd7-125">Request body</span></span>
<span data-ttu-id="5bfd7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5bfd7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bfd7-127">Response</span></span>
<span data-ttu-id="5bfd7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-128">If successful, this method returns a `200 OK` response code and a collection of [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5bfd7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5bfd7-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="5bfd7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5bfd7-130">Request</span></span>
<span data-ttu-id="5bfd7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="5bfd7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bfd7-132">Response</span></span>
<span data-ttu-id="5bfd7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5bfd7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 403

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.macOSDeviceFeaturesConfiguration",
      "id": "49fa957d-957d-49fa-7d95-fa497d95fa49",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7
    }
  ]
}
```



