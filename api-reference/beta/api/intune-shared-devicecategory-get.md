---
title: Obtener deviceCategory
description: Lea las propiedades y las relaciones del objeto deviceCategory.
author: tfitzmac
ms.openlocfilehash: 4a43f0d2551e98ce0a51e28764c90b234015ec29
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331072"
---
# <a name="get-devicecategory"></a><span data-ttu-id="03f5c-103">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="03f5c-103">Get deviceCategory</span></span>

> <span data-ttu-id="03f5c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="03f5c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="03f5c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="03f5c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="03f5c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03f5c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03f5c-107">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="03f5c-107">Read properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03f5c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03f5c-108">Prerequisites</span></span>

<span data-ttu-id="03f5c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03f5c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="03f5c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03f5c-111">Permission type</span></span>|<span data-ttu-id="03f5c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03f5c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="03f5c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03f5c-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="03f5c-114">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="03f5c-114">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="03f5c-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="03f5c-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="03f5c-116">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="03f5c-116">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="03f5c-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="03f5c-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="03f5c-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03f5c-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="03f5c-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03f5c-119">Not supported.</span></span>|
|<span data-ttu-id="03f5c-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03f5c-120">Application</span></span>|<span data-ttu-id="03f5c-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03f5c-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="03f5c-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03f5c-122">HTTP Request</span></span>

<span data-ttu-id="03f5c-123">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="03f5c-123">**Device management**</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCategories/{deviceCategoryId}
```

<span data-ttu-id="03f5c-124">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="03f5c-124">**Onboarding**</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/deviceCategory
```

## <a name="optional-query-parameters"></a><span data-ttu-id="03f5c-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="03f5c-125">Optional query parameters</span></span>

<span data-ttu-id="03f5c-126">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03f5c-126">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="03f5c-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03f5c-127">Request headers</span></span>

|<span data-ttu-id="03f5c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03f5c-128">Header</span></span>|<span data-ttu-id="03f5c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="03f5c-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="03f5c-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="03f5c-130">Authorization</span></span>|<span data-ttu-id="03f5c-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="03f5c-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="03f5c-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="03f5c-132">Accept</span></span>|<span data-ttu-id="03f5c-133">application/json</span><span class="sxs-lookup"><span data-stu-id="03f5c-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="03f5c-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03f5c-134">Request body</span></span>

<span data-ttu-id="03f5c-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03f5c-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03f5c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03f5c-136">Response</span></span>

<span data-ttu-id="03f5c-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceCategory](../resources/intune-shared-devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03f5c-137">If successful, this method returns a `200 OK` response code and [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03f5c-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03f5c-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="03f5c-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03f5c-139">Request</span></span>

<span data-ttu-id="03f5c-140">Es aquí son ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03f5c-140">Here is are examples of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/deviceCategory
GET https://graph.microsoft.com/beta/deviceManagement/deviceCategories/{deviceCategoryId}
```

### <a name="response"></a><span data-ttu-id="03f5c-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03f5c-141">Response</span></span>

<span data-ttu-id="03f5c-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03f5c-142">Here is an example of the response.</span></span> <span data-ttu-id="03f5c-143">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="03f5c-143">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="03f5c-144">Las propiedades que devuelve una llamada real varían según el contexto.</span><span class="sxs-lookup"><span data-stu-id="03f5c-144">Properties returned from an actual call vary according to context.</span></span>

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



