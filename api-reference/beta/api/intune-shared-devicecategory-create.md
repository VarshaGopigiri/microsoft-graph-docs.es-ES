---
title: Crear deviceCategory
description: Cree un objeto deviceCategory.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fe2d928f784eaa370c964761e54c9ea4e2c4d006
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942965"
---
# <a name="create-devicecategory"></a><span data-ttu-id="8fafb-103">Crear deviceCategory</span><span class="sxs-lookup"><span data-stu-id="8fafb-103">Create deviceCategory</span></span>

> <span data-ttu-id="8fafb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8fafb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8fafb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8fafb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8fafb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8fafb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8fafb-107">Cree un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="8fafb-107">Create a new [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8fafb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8fafb-108">Prerequisites</span></span>

<span data-ttu-id="8fafb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8fafb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8fafb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8fafb-111">Permission type</span></span>|<span data-ttu-id="8fafb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8fafb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8fafb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8fafb-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="8fafb-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="8fafb-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="8fafb-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8fafb-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="8fafb-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8fafb-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8fafb-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fafb-117">Not supported.</span></span>|
|<span data-ttu-id="8fafb-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8fafb-118">Application</span></span>|<span data-ttu-id="8fafb-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fafb-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8fafb-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8fafb-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCategories
```

## <a name="request-headers"></a><span data-ttu-id="8fafb-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8fafb-121">Request headers</span></span>

|<span data-ttu-id="8fafb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fafb-122">Header</span></span>|<span data-ttu-id="8fafb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8fafb-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8fafb-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="8fafb-124">Authorization</span></span>|<span data-ttu-id="8fafb-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8fafb-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8fafb-126">Accept</span><span class="sxs-lookup"><span data-stu-id="8fafb-126">Accept</span></span>|<span data-ttu-id="8fafb-127">application/json</span><span class="sxs-lookup"><span data-stu-id="8fafb-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8fafb-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8fafb-128">Request body</span></span>

<span data-ttu-id="8fafb-129">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCategory.</span><span class="sxs-lookup"><span data-stu-id="8fafb-129">In the request body, supply a JSON representation for the deviceCategory object.</span></span>

<span data-ttu-id="8fafb-130">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCategory.</span><span class="sxs-lookup"><span data-stu-id="8fafb-130">The following table shows the properties that are required when you create the deviceCategory.</span></span>

|<span data-ttu-id="8fafb-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fafb-131">Property</span></span>|<span data-ttu-id="8fafb-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fafb-132">Type</span></span>|<span data-ttu-id="8fafb-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fafb-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8fafb-134">id</span><span class="sxs-lookup"><span data-stu-id="8fafb-134">id</span></span>|<span data-ttu-id="8fafb-135">String</span><span class="sxs-lookup"><span data-stu-id="8fafb-135">String</span></span>|<span data-ttu-id="8fafb-136">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fafb-136">Unique identifier for the device category.</span></span> <span data-ttu-id="8fafb-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8fafb-137">Read-only.</span></span>|
|<span data-ttu-id="8fafb-138">**Obboarding**</span><span class="sxs-lookup"><span data-stu-id="8fafb-138">**Obboarding**</span></span>|
|<span data-ttu-id="8fafb-139">descripción</span><span class="sxs-lookup"><span data-stu-id="8fafb-139">description</span></span>|<span data-ttu-id="8fafb-140">String</span><span class="sxs-lookup"><span data-stu-id="8fafb-140">String</span></span>|<span data-ttu-id="8fafb-141">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fafb-141">Optional description for the device category.</span></span>|
|<span data-ttu-id="8fafb-142">displayName</span><span class="sxs-lookup"><span data-stu-id="8fafb-142">displayName</span></span>|<span data-ttu-id="8fafb-143">String</span><span class="sxs-lookup"><span data-stu-id="8fafb-143">String</span></span>|<span data-ttu-id="8fafb-144">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fafb-144">Display name for the device category.</span></span>|

## <a name="response"></a><span data-ttu-id="8fafb-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fafb-145">Response</span></span>

<span data-ttu-id="8fafb-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCategory](../resources/intune-shared-devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8fafb-146">If successful, this method returns a `201 Created` response code and a [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8fafb-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fafb-147">Example</span></span>

### <a name="request"></a><span data-ttu-id="8fafb-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8fafb-148">Request</span></span>

<span data-ttu-id="8fafb-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8fafb-149">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCategories
Content-type: application/json
Content-length: 135

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "displayName": "Display Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="8fafb-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fafb-150">Response</span></span>

<span data-ttu-id="8fafb-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8fafb-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 184

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "f881b841-b841-f881-41b8-81f841b881f8",
  "displayName": "Display Name value",
  "description": "Description value"
}
```



