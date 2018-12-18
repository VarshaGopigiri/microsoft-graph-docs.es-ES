---
title: Crear managedAppOperation
description: Cree un objeto managedAppOperation.
author: tfitzmac
ms.openlocfilehash: 21b9fdd862b72b6935e694f3a7937e675dcd5343
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313345"
---
# <a name="create-managedappoperation"></a><span data-ttu-id="75aa3-103">Crear managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="75aa3-103">Create managedAppOperation</span></span>

> <span data-ttu-id="75aa3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75aa3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75aa3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75aa3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="75aa3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75aa3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75aa3-107">Cree un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="75aa3-107">Create a new [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="75aa3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="75aa3-108">Prerequisites</span></span>
<span data-ttu-id="75aa3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75aa3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="75aa3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="75aa3-111">Permission type</span></span>|<span data-ttu-id="75aa3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="75aa3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="75aa3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="75aa3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="75aa3-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="75aa3-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="75aa3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="75aa3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="75aa3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75aa3-116">Not supported.</span></span>|
|<span data-ttu-id="75aa3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="75aa3-117">Application</span></span>|<span data-ttu-id="75aa3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75aa3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="75aa3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="75aa3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
```

## <a name="request-headers"></a><span data-ttu-id="75aa3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="75aa3-120">Request headers</span></span>
|<span data-ttu-id="75aa3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75aa3-121">Header</span></span>|<span data-ttu-id="75aa3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="75aa3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="75aa3-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="75aa3-123">Authorization</span></span>|<span data-ttu-id="75aa3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="75aa3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="75aa3-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="75aa3-125">Accept</span></span>|<span data-ttu-id="75aa3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="75aa3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="75aa3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="75aa3-127">Request body</span></span>
<span data-ttu-id="75aa3-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="75aa3-128">In the request body, supply a JSON representation for the managedAppOperation object.</span></span>

<span data-ttu-id="75aa3-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="75aa3-129">The following table shows the properties that are required when you create the managedAppOperation.</span></span>

|<span data-ttu-id="75aa3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75aa3-130">Property</span></span>|<span data-ttu-id="75aa3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="75aa3-131">Type</span></span>|<span data-ttu-id="75aa3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="75aa3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75aa3-133">displayName</span><span class="sxs-lookup"><span data-stu-id="75aa3-133">displayName</span></span>|<span data-ttu-id="75aa3-134">String</span><span class="sxs-lookup"><span data-stu-id="75aa3-134">String</span></span>|<span data-ttu-id="75aa3-135">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="75aa3-135">The operation name.</span></span>|
|<span data-ttu-id="75aa3-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="75aa3-136">lastModifiedDateTime</span></span>|<span data-ttu-id="75aa3-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="75aa3-137">DateTimeOffset</span></span>|<span data-ttu-id="75aa3-138">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75aa3-138">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="75aa3-139">state</span><span class="sxs-lookup"><span data-stu-id="75aa3-139">state</span></span>|<span data-ttu-id="75aa3-140">String</span><span class="sxs-lookup"><span data-stu-id="75aa3-140">String</span></span>|<span data-ttu-id="75aa3-141">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="75aa3-141">The current state of the operation</span></span>|
|<span data-ttu-id="75aa3-142">id</span><span class="sxs-lookup"><span data-stu-id="75aa3-142">id</span></span>|<span data-ttu-id="75aa3-143">String</span><span class="sxs-lookup"><span data-stu-id="75aa3-143">String</span></span>|<span data-ttu-id="75aa3-144">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="75aa3-144">Key of the entity.</span></span>|
|<span data-ttu-id="75aa3-145">version</span><span class="sxs-lookup"><span data-stu-id="75aa3-145">version</span></span>|<span data-ttu-id="75aa3-146">String</span><span class="sxs-lookup"><span data-stu-id="75aa3-146">String</span></span>|<span data-ttu-id="75aa3-147">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="75aa3-147">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="75aa3-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75aa3-148">Response</span></span>
<span data-ttu-id="75aa3-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75aa3-149">If successful, this method returns a `201 Created` response code and a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75aa3-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="75aa3-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="75aa3-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="75aa3-151">Request</span></span>
<span data-ttu-id="75aa3-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="75aa3-152">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
Content-type: application/json
Content-length: 223

{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "State value",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="75aa3-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75aa3-153">Response</span></span>
<span data-ttu-id="75aa3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="75aa3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





