---
title: Enumerar windows10CustomConfigurations
description: Enumere las propiedades y las relaciones de los objetos windows10CustomConfiguration.
author: tfitzmac
ms.openlocfilehash: f73fc2628b2bc64a0042484fd732f2fbb61de484
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318175"
---
# <a name="list-windows10customconfigurations"></a><span data-ttu-id="c7ba5-103">Enumerar windows10CustomConfigurations</span><span class="sxs-lookup"><span data-stu-id="c7ba5-103">List windows10CustomConfigurations</span></span>

> <span data-ttu-id="c7ba5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7ba5-105">Enumere las propiedades y las relaciones de los objetos [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c7ba5-105">List properties and relationships of the [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7ba5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7ba5-106">Prerequisites</span></span>
<span data-ttu-id="c7ba5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7ba5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7ba5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7ba5-109">Permission type</span></span>|<span data-ttu-id="c7ba5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7ba5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7ba5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7ba5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c7ba5-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7ba5-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="c7ba5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7ba5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7ba5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-114">Not supported.</span></span>|
|<span data-ttu-id="c7ba5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7ba5-115">Application</span></span>|<span data-ttu-id="c7ba5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7ba5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7ba5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="c7ba5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7ba5-118">Request headers</span></span>
|<span data-ttu-id="c7ba5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7ba5-119">Header</span></span>|<span data-ttu-id="c7ba5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c7ba5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7ba5-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c7ba5-121">Authorization</span></span>|<span data-ttu-id="c7ba5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7ba5-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c7ba5-123">Accept</span></span>|<span data-ttu-id="c7ba5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c7ba5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7ba5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7ba5-125">Request body</span></span>
<span data-ttu-id="c7ba5-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7ba5-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7ba5-127">Response</span></span>
<span data-ttu-id="c7ba5-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-128">If successful, this method returns a `200 OK` response code and a collection of [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7ba5-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ba5-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7ba5-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7ba5-130">Request</span></span>
<span data-ttu-id="c7ba5-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="c7ba5-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7ba5-132">Response</span></span>
<span data-ttu-id="c7ba5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7ba5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 673

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windows10CustomConfiguration",
      "id": "d8ae266e-266e-d8ae-6e26-aed86e26aed8",
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



