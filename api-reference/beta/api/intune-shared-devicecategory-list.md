---
title: Enumerar deviceCategories
description: Enumere las propiedades y las relaciones de los objetos deviceCategory.
ms.openlocfilehash: 9bcddc9b76f7d5223955412854f8de88552af505
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088724"
---
# <a name="list-devicecategories"></a><span data-ttu-id="79de7-103">Enumerar deviceCategories</span><span class="sxs-lookup"><span data-stu-id="79de7-103">List deviceCategories</span></span>

> <span data-ttu-id="79de7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="79de7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="79de7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="79de7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="79de7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="79de7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="79de7-107">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="79de7-107">List properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="79de7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="79de7-108">Prerequisites</span></span>
<span data-ttu-id="79de7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="79de7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="79de7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79de7-111">Permission type</span></span>|<span data-ttu-id="79de7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79de7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="79de7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79de7-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="79de7-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="79de7-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="79de7-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="79de7-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="79de7-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79de7-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="79de7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79de7-117">Not supported.</span></span>|
|<span data-ttu-id="79de7-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79de7-118">Application</span></span>|<span data-ttu-id="79de7-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79de7-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="79de7-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79de7-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCategories
```

## <a name="request-headers"></a><span data-ttu-id="79de7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79de7-121">Request headers</span></span>

|<span data-ttu-id="79de7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79de7-122">Header</span></span>|<span data-ttu-id="79de7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="79de7-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="79de7-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="79de7-124">Authorization</span></span>|<span data-ttu-id="79de7-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="79de7-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="79de7-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="79de7-126">Accept</span></span>|<span data-ttu-id="79de7-127">application/json</span><span class="sxs-lookup"><span data-stu-id="79de7-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="79de7-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79de7-128">Request body</span></span>

<span data-ttu-id="79de7-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79de7-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="79de7-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79de7-130">Response</span></span>

<span data-ttu-id="79de7-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCategory](../resources/intune-shared-devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79de7-131">If successful, this method returns a `200 OK` response code and a collection of [deviceCategory](../resources/intune-shared-devicecategory.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="79de7-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79de7-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="79de7-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79de7-133">Request</span></span>

<span data-ttu-id="79de7-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79de7-134">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCategories
```

### <a name="response"></a><span data-ttu-id="79de7-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79de7-135">Response</span></span>

<span data-ttu-id="79de7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="79de7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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



