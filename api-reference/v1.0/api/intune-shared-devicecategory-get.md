---
title: Obtener deviceCategory
description: Lea las propiedades y las relaciones del objeto deviceCategory.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0c2fac1d5bb242d77a3fbbce110d0bf8e4a2e30e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922455"
---
# <a name="get-devicecategory"></a><span data-ttu-id="8d8c4-103">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="8d8c4-103">Get deviceCategory</span></span>



> <span data-ttu-id="8d8c4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d8c4-105">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="8d8c4-105">Read properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d8c4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8d8c4-106">Prerequisites</span></span>
<span data-ttu-id="8d8c4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8d8c4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8d8c4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8d8c4-109">Permission type</span></span>|<span data-ttu-id="8d8c4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8d8c4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8d8c4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8d8c4-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="8d8c4-112">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="8d8c4-112">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="8d8c4-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d8c4-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="8d8c4-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="8d8c4-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="8d8c4-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="8d8c4-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="8d8c4-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8d8c4-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8d8c4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-117">Not supported.</span></span>|
|<span data-ttu-id="8d8c4-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8d8c4-118">Application</span></span>|<span data-ttu-id="8d8c4-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8d8c4-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8d8c4-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
GET /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8d8c4-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8d8c4-121">Optional query parameters</span></span>
<span data-ttu-id="8d8c4-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8d8c4-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8d8c4-123">Request headers</span></span>
|<span data-ttu-id="8d8c4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d8c4-124">Header</span></span>|<span data-ttu-id="8d8c4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8d8c4-125">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8d8c4-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="8d8c4-126">Authorization</span></span>|<span data-ttu-id="8d8c4-127">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-127">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8d8c4-128">Accept</span><span class="sxs-lookup"><span data-stu-id="8d8c4-128">Accept</span></span>|<span data-ttu-id="8d8c4-129">application/json</span><span class="sxs-lookup"><span data-stu-id="8d8c4-129">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8d8c4-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8d8c4-130">Request body</span></span>
<span data-ttu-id="8d8c4-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8d8c4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d8c4-132">Response</span></span>
<span data-ttu-id="8d8c4-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceCategory](../resources/intune-shared-devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-133">If successful, this method returns a `200 OK` response code and [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8d8c4-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d8c4-134">Example</span></span>

### <a name="request"></a><span data-ttu-id="8d8c4-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8d8c4-135">Request</span></span>
<span data-ttu-id="8d8c4-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-136">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories/{deviceCategoryId}

```

### <a name="response"></a><span data-ttu-id="8d8c4-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d8c4-137">Response</span></span>
<span data-ttu-id="8d8c4-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-138">Here is an example of the response.</span></span> <span data-ttu-id="8d8c4-139">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-139">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="8d8c4-140">Las propiedades que devuelve una llamada real varían según el contexto.</span><span class="sxs-lookup"><span data-stu-id="8d8c4-140">Properties returned from an actual call vary according to context.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 211

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceCategory",
    "id": "f881b841-b841-f881-41b8-81f841b881f8",
    "displayName": "Display Name value",
    "description": "Description value"
  }
}
```



