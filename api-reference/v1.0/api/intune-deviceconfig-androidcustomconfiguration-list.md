---
title: Enumerar androidCustomConfigurations
description: Enumere las propiedades y las relaciones de los objetos androidCustomConfiguration.
ms.openlocfilehash: becd3644d4f9394105b6a2037a61a1b76b23b82a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032315"
---
# <a name="list-androidcustomconfigurations"></a><span data-ttu-id="70a91-103">Enumerar androidCustomConfigurations</span><span class="sxs-lookup"><span data-stu-id="70a91-103">List androidCustomConfigurations</span></span>

> <span data-ttu-id="70a91-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="70a91-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="70a91-105">Enumere las propiedades y las relaciones de los objetos [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="70a91-105">List properties and relationships of the [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="70a91-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="70a91-106">Prerequisites</span></span>
<span data-ttu-id="70a91-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="70a91-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="70a91-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70a91-109">Permission type</span></span>|<span data-ttu-id="70a91-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70a91-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="70a91-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70a91-111">Delegated (work or school account)</span></span>|<span data-ttu-id="70a91-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="70a91-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="70a91-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70a91-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="70a91-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70a91-114">Not supported.</span></span>|
|<span data-ttu-id="70a91-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70a91-115">Application</span></span>|<span data-ttu-id="70a91-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70a91-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="70a91-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70a91-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="70a91-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70a91-118">Request headers</span></span>
|<span data-ttu-id="70a91-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70a91-119">Header</span></span>|<span data-ttu-id="70a91-120">Valor</span><span class="sxs-lookup"><span data-stu-id="70a91-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="70a91-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="70a91-121">Authorization</span></span>|<span data-ttu-id="70a91-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="70a91-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="70a91-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="70a91-123">Accept</span></span>|<span data-ttu-id="70a91-124">application/json</span><span class="sxs-lookup"><span data-stu-id="70a91-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="70a91-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70a91-125">Request body</span></span>
<span data-ttu-id="70a91-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="70a91-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="70a91-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70a91-127">Response</span></span>
<span data-ttu-id="70a91-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70a91-128">If successful, this method returns a `200 OK` response code and a collection of [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="70a91-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70a91-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="70a91-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70a91-130">Request</span></span>
<span data-ttu-id="70a91-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70a91-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="70a91-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70a91-132">Response</span></span>
<span data-ttu-id="70a91-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70a91-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 671

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidCustomConfiguration",
      "id": "619b5e6d-5e6d-619b-6d5e-9b616d5e9b61",
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



