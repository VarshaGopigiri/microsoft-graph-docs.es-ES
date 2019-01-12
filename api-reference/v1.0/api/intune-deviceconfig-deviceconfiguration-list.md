---
title: Enumerar deviceConfigurations
description: Enumere las propiedades y las relaciones de los objetos deviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ebeb789bc9124176e63db6cb8b653ea232c49a24
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917548"
---
# <a name="list-deviceconfigurations"></a><span data-ttu-id="b32bc-103">Enumerar deviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="b32bc-103">List deviceConfigurations</span></span>

> <span data-ttu-id="b32bc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b32bc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b32bc-105">Enumere las propiedades y las relaciones de los objetos [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b32bc-105">List properties and relationships of the [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b32bc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b32bc-106">Prerequisites</span></span>
<span data-ttu-id="b32bc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b32bc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b32bc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b32bc-109">Permission type</span></span>|<span data-ttu-id="b32bc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b32bc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b32bc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b32bc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b32bc-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b32bc-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b32bc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b32bc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b32bc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b32bc-114">Not supported.</span></span>|
|<span data-ttu-id="b32bc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b32bc-115">Application</span></span>|<span data-ttu-id="b32bc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b32bc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b32bc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b32bc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="b32bc-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b32bc-118">Request headers</span></span>
|<span data-ttu-id="b32bc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b32bc-119">Header</span></span>|<span data-ttu-id="b32bc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b32bc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b32bc-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b32bc-121">Authorization</span></span>|<span data-ttu-id="b32bc-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b32bc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b32bc-123">Accept</span><span class="sxs-lookup"><span data-stu-id="b32bc-123">Accept</span></span>|<span data-ttu-id="b32bc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b32bc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b32bc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b32bc-125">Request body</span></span>
<span data-ttu-id="b32bc-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b32bc-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b32bc-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b32bc-127">Response</span></span>
<span data-ttu-id="b32bc-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b32bc-128">If successful, this method returns a `200 OK` response code and a collection of [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b32bc-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b32bc-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b32bc-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b32bc-130">Request</span></span>
<span data-ttu-id="b32bc-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b32bc-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="b32bc-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b32bc-132">Response</span></span>
<span data-ttu-id="b32bc-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b32bc-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 390

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceConfiguration",
      "id": "34977265-7265-3497-6572-973465729734",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7
    }
  ]
}
```



