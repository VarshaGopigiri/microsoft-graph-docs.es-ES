---
title: Actualizar managedAppOperation
description: Actualice las propiedades de un objeto managedAppOperation.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5d0baf0b503edcde0bdc03329ec354a4d6e42a4c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980135"
---
# <a name="update-managedappoperation"></a><span data-ttu-id="02066-103">Actualizar managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="02066-103">Update managedAppOperation</span></span>

> <span data-ttu-id="02066-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="02066-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="02066-105">Actualice las propiedades de un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="02066-105">Update the properties of a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="02066-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="02066-106">Prerequisites</span></span>
<span data-ttu-id="02066-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="02066-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="02066-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="02066-109">Permission type</span></span>|<span data-ttu-id="02066-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="02066-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="02066-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="02066-111">Delegated (work or school account)</span></span>|<span data-ttu-id="02066-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="02066-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="02066-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="02066-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="02066-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="02066-114">Not supported.</span></span>|
|<span data-ttu-id="02066-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="02066-115">Application</span></span>|<span data-ttu-id="02066-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="02066-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="02066-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="02066-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations/{managedAppOperationId}
```

## <a name="request-headers"></a><span data-ttu-id="02066-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="02066-118">Request headers</span></span>
|<span data-ttu-id="02066-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02066-119">Header</span></span>|<span data-ttu-id="02066-120">Valor</span><span class="sxs-lookup"><span data-stu-id="02066-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="02066-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="02066-121">Authorization</span></span>|<span data-ttu-id="02066-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="02066-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="02066-123">Accept</span><span class="sxs-lookup"><span data-stu-id="02066-123">Accept</span></span>|<span data-ttu-id="02066-124">application/json</span><span class="sxs-lookup"><span data-stu-id="02066-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="02066-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="02066-125">Request body</span></span>
<span data-ttu-id="02066-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="02066-126">In the request body, supply a JSON representation for the [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>

<span data-ttu-id="02066-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="02066-127">The following table shows the properties that are required when you create the [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span></span>

|<span data-ttu-id="02066-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="02066-128">Property</span></span>|<span data-ttu-id="02066-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="02066-129">Type</span></span>|<span data-ttu-id="02066-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="02066-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="02066-131">displayName</span><span class="sxs-lookup"><span data-stu-id="02066-131">displayName</span></span>|<span data-ttu-id="02066-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="02066-132">String</span></span>|<span data-ttu-id="02066-133">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="02066-133">The operation name.</span></span>|
|<span data-ttu-id="02066-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="02066-134">lastModifiedDateTime</span></span>|<span data-ttu-id="02066-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="02066-135">DateTimeOffset</span></span>|<span data-ttu-id="02066-136">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="02066-136">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="02066-137">state</span><span class="sxs-lookup"><span data-stu-id="02066-137">state</span></span>|<span data-ttu-id="02066-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="02066-138">String</span></span>|<span data-ttu-id="02066-139">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="02066-139">The current state of the operation</span></span>|
|<span data-ttu-id="02066-140">id</span><span class="sxs-lookup"><span data-stu-id="02066-140">id</span></span>|<span data-ttu-id="02066-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="02066-141">String</span></span>|<span data-ttu-id="02066-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="02066-142">Key of the entity.</span></span>|
|<span data-ttu-id="02066-143">version</span><span class="sxs-lookup"><span data-stu-id="02066-143">version</span></span>|<span data-ttu-id="02066-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="02066-144">String</span></span>|<span data-ttu-id="02066-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="02066-145">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="02066-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02066-146">Response</span></span>
<span data-ttu-id="02066-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02066-147">If successful, this method returns a `200 OK` response code and an updated [managedAppOperation](../resources/intune-mam-managedappoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="02066-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02066-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="02066-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="02066-149">Request</span></span>
<span data-ttu-id="02066-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="02066-150">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="02066-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02066-151">Response</span></span>
<span data-ttu-id="02066-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="02066-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



