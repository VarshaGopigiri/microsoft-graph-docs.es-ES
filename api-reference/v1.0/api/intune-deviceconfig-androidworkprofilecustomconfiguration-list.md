---
title: Lista androidWorkProfileCustomConfigurations
description: Propiedades de la lista y relaciones de los objetos androidWorkProfileCustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 566a04b1d732dab6b765876f8b1823a1c640ee6b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850900"
---
# <a name="list-androidworkprofilecustomconfigurations"></a><span data-ttu-id="2bd8b-103">Lista androidWorkProfileCustomConfigurations</span><span class="sxs-lookup"><span data-stu-id="2bd8b-103">List androidWorkProfileCustomConfigurations</span></span>

> <span data-ttu-id="2bd8b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2bd8b-105">Propiedades de la lista y relaciones de los objetos [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd8b-105">List properties and relationships of the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2bd8b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2bd8b-106">Prerequisites</span></span>
<span data-ttu-id="2bd8b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2bd8b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2bd8b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bd8b-109">Permission type</span></span>|<span data-ttu-id="2bd8b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bd8b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2bd8b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bd8b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2bd8b-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="2bd8b-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="2bd8b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bd8b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2bd8b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-114">Not supported.</span></span>|
|<span data-ttu-id="2bd8b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bd8b-115">Application</span></span>|<span data-ttu-id="2bd8b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2bd8b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bd8b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="2bd8b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bd8b-118">Request headers</span></span>
|<span data-ttu-id="2bd8b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bd8b-119">Header</span></span>|<span data-ttu-id="2bd8b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2bd8b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2bd8b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2bd8b-121">Authorization</span></span>|<span data-ttu-id="2bd8b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2bd8b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="2bd8b-123">Accept</span></span>|<span data-ttu-id="2bd8b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2bd8b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2bd8b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2bd8b-125">Request body</span></span>
<span data-ttu-id="2bd8b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2bd8b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bd8b-127">Response</span></span>
<span data-ttu-id="2bd8b-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-128">If successful, this method returns a `200 OK` response code and a collection of [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2bd8b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bd8b-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="2bd8b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bd8b-130">Request</span></span>
<span data-ttu-id="2bd8b-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="2bd8b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bd8b-132">Response</span></span>
<span data-ttu-id="2bd8b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2bd8b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 682

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
      "id": "76c5d59b-d59b-76c5-9bd5-c5769bd5c576",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "omaSettings": [
        {
          "@odata.type": "microsoft.graph.omaSettingInteger",
          "displayName": "Display Name value",
          "description": "Description value",
          "omaUri": "Oma Uri value",
          "value": 5
        }
      ]
    }
  ]
}
```



