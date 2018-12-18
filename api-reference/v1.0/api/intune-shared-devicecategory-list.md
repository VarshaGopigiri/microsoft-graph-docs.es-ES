---
title: Enumerar deviceCategories
description: Enumere las propiedades y las relaciones de los objetos deviceCategory.
author: tfitzmac
ms.openlocfilehash: 345fec4d151dab0e73cadccf2b4618f4e292ef4e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304182"
---
# <a name="list-devicecategories"></a><span data-ttu-id="da50a-103">Enumerar deviceCategories</span><span class="sxs-lookup"><span data-stu-id="da50a-103">List deviceCategories</span></span>

> <span data-ttu-id="da50a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="da50a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="da50a-105">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="da50a-105">List properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="da50a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="da50a-106">Prerequisites</span></span>
<span data-ttu-id="da50a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="da50a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="da50a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da50a-109">Permission type</span></span>|<span data-ttu-id="da50a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da50a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="da50a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da50a-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="da50a-112">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="da50a-112">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="da50a-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="da50a-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="da50a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da50a-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="da50a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da50a-115">Not supported.</span></span>|
|<span data-ttu-id="da50a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da50a-116">Application</span></span>|<span data-ttu-id="da50a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da50a-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="da50a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da50a-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCategories
```

## <a name="request-headers"></a><span data-ttu-id="da50a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da50a-119">Request headers</span></span>
|<span data-ttu-id="da50a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da50a-120">Header</span></span>|<span data-ttu-id="da50a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="da50a-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="da50a-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="da50a-122">Authorization</span></span>|<span data-ttu-id="da50a-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="da50a-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="da50a-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="da50a-124">Accept</span></span>|<span data-ttu-id="da50a-125">application/json</span><span class="sxs-lookup"><span data-stu-id="da50a-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="da50a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da50a-126">Request body</span></span>
<span data-ttu-id="da50a-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="da50a-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="da50a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da50a-128">Response</span></span>
<span data-ttu-id="da50a-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCategory](../resources/intune-shared-devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da50a-129">If successful, this method returns a `200 OK` response code and a collection of [deviceCategory](../resources/intune-shared-devicecategory.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da50a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da50a-130">Example</span></span>
### <a name="request"></a><span data-ttu-id="da50a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da50a-131">Request</span></span>
<span data-ttu-id="da50a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da50a-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories
```

### <a name="response"></a><span data-ttu-id="da50a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da50a-133">Response</span></span>
<span data-ttu-id="da50a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="da50a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceCategory",
      "id": "f881b841-b841-f881-41b8-81f841b881f8",
      "displayName": "Display Name value",
      "description": "Description value"
    }
  ]
}
```



