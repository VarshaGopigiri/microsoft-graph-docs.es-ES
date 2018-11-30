---
title: Actualizar managedAppOperation
description: Actualice las propiedades de un objeto managedAppOperation.
ms.openlocfilehash: d67766f5d60d518517589ebe033374a8e138a686
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028969"
---
# <a name="update-managedappoperation"></a><span data-ttu-id="4d16e-103">Actualizar managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="4d16e-103">Update managedAppOperation</span></span>

> <span data-ttu-id="4d16e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4d16e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4d16e-105">Actualice las propiedades de un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="4d16e-105">Update the properties of a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4d16e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4d16e-106">Prerequisites</span></span>
<span data-ttu-id="4d16e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d16e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4d16e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d16e-109">Permission type</span></span>|<span data-ttu-id="4d16e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d16e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4d16e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d16e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4d16e-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d16e-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4d16e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d16e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4d16e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d16e-114">Not supported.</span></span>|
|<span data-ttu-id="4d16e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d16e-115">Application</span></span>|<span data-ttu-id="4d16e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d16e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4d16e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d16e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations/{managedAppOperationId}
```

## <a name="request-headers"></a><span data-ttu-id="4d16e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d16e-118">Request headers</span></span>
|<span data-ttu-id="4d16e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d16e-119">Header</span></span>|<span data-ttu-id="4d16e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4d16e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4d16e-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d16e-121">Authorization</span></span>|<span data-ttu-id="4d16e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4d16e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4d16e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4d16e-123">Accept</span></span>|<span data-ttu-id="4d16e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4d16e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4d16e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d16e-125">Request body</span></span>
<span data-ttu-id="4d16e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="4d16e-126">In the request body, supply a JSON representation for the [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>

<span data-ttu-id="4d16e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="4d16e-127">The following table shows the properties that are required when you create the [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span></span>

|<span data-ttu-id="4d16e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d16e-128">Property</span></span>|<span data-ttu-id="4d16e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d16e-129">Type</span></span>|<span data-ttu-id="4d16e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d16e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4d16e-131">displayName</span><span class="sxs-lookup"><span data-stu-id="4d16e-131">displayName</span></span>|<span data-ttu-id="4d16e-132">String</span><span class="sxs-lookup"><span data-stu-id="4d16e-132">String</span></span>|<span data-ttu-id="4d16e-133">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="4d16e-133">The operation name.</span></span>|
|<span data-ttu-id="4d16e-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4d16e-134">lastModifiedDateTime</span></span>|<span data-ttu-id="4d16e-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4d16e-135">DateTimeOffset</span></span>|<span data-ttu-id="4d16e-136">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d16e-136">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="4d16e-137">estado</span><span class="sxs-lookup"><span data-stu-id="4d16e-137">state</span></span>|<span data-ttu-id="4d16e-138">String</span><span class="sxs-lookup"><span data-stu-id="4d16e-138">String</span></span>|<span data-ttu-id="4d16e-139">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="4d16e-139">The current state of the operation</span></span>|
|<span data-ttu-id="4d16e-140">id</span><span class="sxs-lookup"><span data-stu-id="4d16e-140">id</span></span>|<span data-ttu-id="4d16e-141">String</span><span class="sxs-lookup"><span data-stu-id="4d16e-141">String</span></span>|<span data-ttu-id="4d16e-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4d16e-142">Key of the entity.</span></span>|
|<span data-ttu-id="4d16e-143">version</span><span class="sxs-lookup"><span data-stu-id="4d16e-143">version</span></span>|<span data-ttu-id="4d16e-144">String</span><span class="sxs-lookup"><span data-stu-id="4d16e-144">String</span></span>|<span data-ttu-id="4d16e-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4d16e-145">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="4d16e-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d16e-146">Response</span></span>
<span data-ttu-id="4d16e-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d16e-147">If successful, this method returns a `200 OK` response code and an updated [managedAppOperation](../resources/intune-mam-managedappoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d16e-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d16e-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="4d16e-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d16e-149">Request</span></span>
<span data-ttu-id="4d16e-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d16e-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations/{managedAppOperationId}
Content-type: application/json
Content-length: 159

{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "Display Name value",
  "state": "State value",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="4d16e-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d16e-151">Response</span></span>
<span data-ttu-id="4d16e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d16e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



