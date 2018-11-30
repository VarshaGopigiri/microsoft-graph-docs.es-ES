---
title: Actualizar managedAppOperation
description: Actualice las propiedades de un objeto managedAppOperation.
ms.openlocfilehash: 793b4eb48a0f70c0b1877aebd40969fba334e65e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087528"
---
# <a name="update-managedappoperation"></a><span data-ttu-id="b8894-103">Actualizar managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="b8894-103">Update managedAppOperation</span></span>

> <span data-ttu-id="b8894-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b8894-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b8894-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b8894-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b8894-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b8894-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b8894-107">Actualice las propiedades de un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="b8894-107">Update the properties of a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b8894-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b8894-108">Prerequisites</span></span>
<span data-ttu-id="b8894-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8894-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8894-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8894-111">Permission type</span></span>|<span data-ttu-id="b8894-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8894-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b8894-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8894-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b8894-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8894-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b8894-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8894-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b8894-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8894-116">Not supported.</span></span>|
|<span data-ttu-id="b8894-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8894-117">Application</span></span>|<span data-ttu-id="b8894-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8894-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b8894-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8894-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations/{managedAppOperationId}
```

## <a name="request-headers"></a><span data-ttu-id="b8894-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8894-120">Request headers</span></span>
|<span data-ttu-id="b8894-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8894-121">Header</span></span>|<span data-ttu-id="b8894-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b8894-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b8894-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8894-123">Authorization</span></span>|<span data-ttu-id="b8894-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b8894-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b8894-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b8894-125">Accept</span></span>|<span data-ttu-id="b8894-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b8894-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b8894-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8894-127">Request body</span></span>
<span data-ttu-id="b8894-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="b8894-128">In the request body, supply a JSON representation for the [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>

<span data-ttu-id="b8894-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="b8894-129">The following table shows the properties that are required when you create the [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span></span>

|<span data-ttu-id="b8894-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b8894-130">Property</span></span>|<span data-ttu-id="b8894-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8894-131">Type</span></span>|<span data-ttu-id="b8894-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8894-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b8894-133">displayName</span><span class="sxs-lookup"><span data-stu-id="b8894-133">displayName</span></span>|<span data-ttu-id="b8894-134">String</span><span class="sxs-lookup"><span data-stu-id="b8894-134">String</span></span>|<span data-ttu-id="b8894-135">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="b8894-135">The operation name.</span></span>|
|<span data-ttu-id="b8894-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b8894-136">lastModifiedDateTime</span></span>|<span data-ttu-id="b8894-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8894-137">DateTimeOffset</span></span>|<span data-ttu-id="b8894-138">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b8894-138">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="b8894-139">estado</span><span class="sxs-lookup"><span data-stu-id="b8894-139">state</span></span>|<span data-ttu-id="b8894-140">String</span><span class="sxs-lookup"><span data-stu-id="b8894-140">String</span></span>|<span data-ttu-id="b8894-141">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="b8894-141">The current state of the operation</span></span>|
|<span data-ttu-id="b8894-142">id</span><span class="sxs-lookup"><span data-stu-id="b8894-142">id</span></span>|<span data-ttu-id="b8894-143">String</span><span class="sxs-lookup"><span data-stu-id="b8894-143">String</span></span>|<span data-ttu-id="b8894-144">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b8894-144">Key of the entity.</span></span>|
|<span data-ttu-id="b8894-145">version</span><span class="sxs-lookup"><span data-stu-id="b8894-145">version</span></span>|<span data-ttu-id="b8894-146">String</span><span class="sxs-lookup"><span data-stu-id="b8894-146">String</span></span>|<span data-ttu-id="b8894-147">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b8894-147">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="b8894-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8894-148">Response</span></span>
<span data-ttu-id="b8894-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8894-149">If successful, this method returns a `200 OK` response code and an updated [managedAppOperation](../resources/intune-mam-managedappoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8894-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8894-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="b8894-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8894-151">Request</span></span>
<span data-ttu-id="b8894-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8894-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations/{managedAppOperationId}
Content-type: application/json
Content-length: 165

{
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "State value",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="b8894-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8894-153">Response</span></span>
<span data-ttu-id="b8894-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8894-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 272

{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "State value",
  "id": "f2867b06-7b06-f286-067b-86f2067b86f2",
  "version": "Version value"
}
```





