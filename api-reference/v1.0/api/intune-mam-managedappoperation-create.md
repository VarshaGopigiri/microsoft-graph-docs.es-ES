---
title: Crear managedAppOperation
description: Cree un objeto managedAppOperation.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c4afd179a33202eb7780495228f94f23326c7268
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855212"
---
# <a name="create-managedappoperation"></a><span data-ttu-id="7a514-103">Crear managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="7a514-103">Create managedAppOperation</span></span>

> <span data-ttu-id="7a514-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a514-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a514-105">Cree un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="7a514-105">Create a new [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7a514-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7a514-106">Prerequisites</span></span>
<span data-ttu-id="7a514-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7a514-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7a514-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a514-109">Permission type</span></span>|<span data-ttu-id="7a514-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a514-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7a514-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a514-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7a514-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7a514-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7a514-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a514-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7a514-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a514-114">Not supported.</span></span>|
|<span data-ttu-id="7a514-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a514-115">Application</span></span>|<span data-ttu-id="7a514-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a514-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7a514-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a514-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
```

## <a name="request-headers"></a><span data-ttu-id="7a514-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a514-118">Request headers</span></span>
|<span data-ttu-id="7a514-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a514-119">Header</span></span>|<span data-ttu-id="7a514-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7a514-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7a514-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="7a514-121">Authorization</span></span>|<span data-ttu-id="7a514-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7a514-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7a514-123">Accept</span><span class="sxs-lookup"><span data-stu-id="7a514-123">Accept</span></span>|<span data-ttu-id="7a514-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7a514-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7a514-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7a514-125">Request body</span></span>
<span data-ttu-id="7a514-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="7a514-126">In the request body, supply a JSON representation for the managedAppOperation object.</span></span>

<span data-ttu-id="7a514-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="7a514-127">The following table shows the properties that are required when you create the managedAppOperation.</span></span>

|<span data-ttu-id="7a514-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a514-128">Property</span></span>|<span data-ttu-id="7a514-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a514-129">Type</span></span>|<span data-ttu-id="7a514-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a514-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a514-131">displayName</span><span class="sxs-lookup"><span data-stu-id="7a514-131">displayName</span></span>|<span data-ttu-id="7a514-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a514-132">String</span></span>|<span data-ttu-id="7a514-133">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="7a514-133">The operation name.</span></span>|
|<span data-ttu-id="7a514-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7a514-134">lastModifiedDateTime</span></span>|<span data-ttu-id="7a514-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a514-135">DateTimeOffset</span></span>|<span data-ttu-id="7a514-136">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a514-136">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="7a514-137">state</span><span class="sxs-lookup"><span data-stu-id="7a514-137">state</span></span>|<span data-ttu-id="7a514-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a514-138">String</span></span>|<span data-ttu-id="7a514-139">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="7a514-139">The current state of the operation</span></span>|
|<span data-ttu-id="7a514-140">id</span><span class="sxs-lookup"><span data-stu-id="7a514-140">id</span></span>|<span data-ttu-id="7a514-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a514-141">String</span></span>|<span data-ttu-id="7a514-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7a514-142">Key of the entity.</span></span>|
|<span data-ttu-id="7a514-143">version</span><span class="sxs-lookup"><span data-stu-id="7a514-143">version</span></span>|<span data-ttu-id="7a514-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a514-144">String</span></span>|<span data-ttu-id="7a514-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7a514-145">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="7a514-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a514-146">Response</span></span>
<span data-ttu-id="7a514-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a514-147">If successful, this method returns a `201 Created` response code and a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7a514-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a514-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="7a514-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a514-149">Request</span></span>
<span data-ttu-id="7a514-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a514-150">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
Content-type: application/json
Content-length: 159

{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "Display Name value",
  "state": "State value",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="7a514-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a514-151">Response</span></span>
<span data-ttu-id="7a514-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7a514-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



