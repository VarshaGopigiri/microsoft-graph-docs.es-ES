---
title: Crear sideLoadingKey
description: Crear un nuevo objeto sideLoadingKey.
ms.openlocfilehash: c97b31fd37893433aeaea31539a7eaee021272ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088856"
---
# <a name="create-sideloadingkey"></a><span data-ttu-id="41b73-103">Crear sideLoadingKey</span><span class="sxs-lookup"><span data-stu-id="41b73-103">Create sideLoadingKey</span></span>

> <span data-ttu-id="41b73-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="41b73-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41b73-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="41b73-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="41b73-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41b73-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41b73-107">Crear un nuevo objeto [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .</span><span class="sxs-lookup"><span data-stu-id="41b73-107">Create a new [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="41b73-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="41b73-108">Prerequisites</span></span>
<span data-ttu-id="41b73-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41b73-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="41b73-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41b73-111">Permission type</span></span>|<span data-ttu-id="41b73-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41b73-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="41b73-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41b73-113">Delegated (work or school account)</span></span>|<span data-ttu-id="41b73-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="41b73-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="41b73-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41b73-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="41b73-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41b73-116">Not supported.</span></span>|
|<span data-ttu-id="41b73-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41b73-117">Application</span></span>|<span data-ttu-id="41b73-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41b73-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="41b73-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41b73-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/sideLoadingKeys
```

## <a name="request-headers"></a><span data-ttu-id="41b73-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41b73-120">Request headers</span></span>
|<span data-ttu-id="41b73-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41b73-121">Header</span></span>|<span data-ttu-id="41b73-122">Valor</span><span class="sxs-lookup"><span data-stu-id="41b73-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="41b73-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="41b73-123">Authorization</span></span>|<span data-ttu-id="41b73-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="41b73-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="41b73-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="41b73-125">Accept</span></span>|<span data-ttu-id="41b73-126">application/json</span><span class="sxs-lookup"><span data-stu-id="41b73-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="41b73-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41b73-127">Request body</span></span>
<span data-ttu-id="41b73-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto sideLoadingKey.</span><span class="sxs-lookup"><span data-stu-id="41b73-128">In the request body, supply a JSON representation for the sideLoadingKey object.</span></span>

<span data-ttu-id="41b73-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el sideLoadingKey.</span><span class="sxs-lookup"><span data-stu-id="41b73-129">The following table shows the properties that are required when you create the sideLoadingKey.</span></span>

|<span data-ttu-id="41b73-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41b73-130">Property</span></span>|<span data-ttu-id="41b73-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b73-131">Type</span></span>|<span data-ttu-id="41b73-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="41b73-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="41b73-133">id</span><span class="sxs-lookup"><span data-stu-id="41b73-133">id</span></span>|<span data-ttu-id="41b73-134">String</span><span class="sxs-lookup"><span data-stu-id="41b73-134">String</span></span>|<span data-ttu-id="41b73-135">Lado cargar clave identificador único.</span><span class="sxs-lookup"><span data-stu-id="41b73-135">Side Loading Key Unique Id.</span></span>|
|<span data-ttu-id="41b73-136">valor</span><span class="sxs-lookup"><span data-stu-id="41b73-136">value</span></span>|<span data-ttu-id="41b73-137">String</span><span class="sxs-lookup"><span data-stu-id="41b73-137">String</span></span>|<span data-ttu-id="41b73-138">Valor de clave de carga del lado, es valor de 5 x 5, separados por hiphens.</span><span class="sxs-lookup"><span data-stu-id="41b73-138">Side Loading Key Value, it is 5x5 value, seperated by hiphens.</span></span>|
|<span data-ttu-id="41b73-139">displayName</span><span class="sxs-lookup"><span data-stu-id="41b73-139">displayName</span></span>|<span data-ttu-id="41b73-140">String</span><span class="sxs-lookup"><span data-stu-id="41b73-140">String</span></span>|<span data-ttu-id="41b73-141">Lado carga de clave de nombre que se muestra a la ITPro Admins.</span><span class="sxs-lookup"><span data-stu-id="41b73-141">Side Loading Key Name displayed to the ITPro Admins.</span></span>|
|<span data-ttu-id="41b73-142">descripción</span><span class="sxs-lookup"><span data-stu-id="41b73-142">description</span></span>|<span data-ttu-id="41b73-143">String</span><span class="sxs-lookup"><span data-stu-id="41b73-143">String</span></span>|<span data-ttu-id="41b73-144">Clave de carga de descripción en el que se muestra a la ITPro Admins..</span><span class="sxs-lookup"><span data-stu-id="41b73-144">Side Loading Key description displayed to the ITPro Admins..</span></span>|
|<span data-ttu-id="41b73-145">totalActivation</span><span class="sxs-lookup"><span data-stu-id="41b73-145">totalActivation</span></span>|<span data-ttu-id="41b73-146">Int32</span><span class="sxs-lookup"><span data-stu-id="41b73-146">Int32</span></span>|<span data-ttu-id="41b73-147">Lado carga Total activación de la clave que se muestra a la ITPro Admins.</span><span class="sxs-lookup"><span data-stu-id="41b73-147">Side Loading Key Total Activation displayed to the ITPro Admins.</span></span>|
|<span data-ttu-id="41b73-148">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="41b73-148">lastUpdatedDateTime</span></span>|<span data-ttu-id="41b73-149">String</span><span class="sxs-lookup"><span data-stu-id="41b73-149">String</span></span>|<span data-ttu-id="41b73-150">Lado cargar clave última actualizado fecha que se muestra a la ITPro Admins.</span><span class="sxs-lookup"><span data-stu-id="41b73-150">Side Loading Key Last Updated Date displayed to the ITPro Admins.</span></span>|



## <a name="response"></a><span data-ttu-id="41b73-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41b73-151">Response</span></span>
<span data-ttu-id="41b73-152">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41b73-152">If successful, this method returns a `201 Created` response code and a [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41b73-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41b73-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="41b73-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41b73-154">Request</span></span>
<span data-ttu-id="41b73-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41b73-155">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/sideLoadingKeys
Content-type: application/json
Content-length: 246

{
  "@odata.type": "#microsoft.graph.sideLoadingKey",
  "value": "Value value",
  "displayName": "Display Name value",
  "description": "Description value",
  "totalActivation": 15,
  "lastUpdatedDateTime": "Last Updated Date Time value"
}
```

### <a name="response"></a><span data-ttu-id="41b73-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41b73-156">Response</span></span>
<span data-ttu-id="41b73-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41b73-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 295

{
  "@odata.type": "#microsoft.graph.sideLoadingKey",
  "id": "21c4a3ff-a3ff-21c4-ffa3-c421ffa3c421",
  "value": "Value value",
  "displayName": "Display Name value",
  "description": "Description value",
  "totalActivation": 15,
  "lastUpdatedDateTime": "Last Updated Date Time value"
}
```





