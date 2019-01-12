---
title: Crear managedAppOperation
description: Cree un objeto managedAppOperation.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9a8be6117a14a2ce87d06928ec8f45fde87c52d8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979869"
---
# <a name="create-managedappoperation"></a><span data-ttu-id="12487-103">Crear managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="12487-103">Create managedAppOperation</span></span>

> <span data-ttu-id="12487-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="12487-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="12487-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="12487-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="12487-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12487-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12487-107">Cree un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="12487-107">Create a new [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="12487-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="12487-108">Prerequisites</span></span>
<span data-ttu-id="12487-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="12487-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="12487-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="12487-111">Permission type</span></span>|<span data-ttu-id="12487-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="12487-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="12487-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="12487-113">Delegated (work or school account)</span></span>|<span data-ttu-id="12487-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="12487-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="12487-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="12487-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="12487-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12487-116">Not supported.</span></span>|
|<span data-ttu-id="12487-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="12487-117">Application</span></span>|<span data-ttu-id="12487-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12487-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="12487-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="12487-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
```

## <a name="request-headers"></a><span data-ttu-id="12487-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="12487-120">Request headers</span></span>
|<span data-ttu-id="12487-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12487-121">Header</span></span>|<span data-ttu-id="12487-122">Valor</span><span class="sxs-lookup"><span data-stu-id="12487-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="12487-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="12487-123">Authorization</span></span>|<span data-ttu-id="12487-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="12487-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="12487-125">Accept</span><span class="sxs-lookup"><span data-stu-id="12487-125">Accept</span></span>|<span data-ttu-id="12487-126">application/json</span><span class="sxs-lookup"><span data-stu-id="12487-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="12487-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="12487-127">Request body</span></span>
<span data-ttu-id="12487-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="12487-128">In the request body, supply a JSON representation for the managedAppOperation object.</span></span>

<span data-ttu-id="12487-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="12487-129">The following table shows the properties that are required when you create the managedAppOperation.</span></span>

|<span data-ttu-id="12487-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="12487-130">Property</span></span>|<span data-ttu-id="12487-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="12487-131">Type</span></span>|<span data-ttu-id="12487-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="12487-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="12487-133">displayName</span><span class="sxs-lookup"><span data-stu-id="12487-133">displayName</span></span>|<span data-ttu-id="12487-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="12487-134">String</span></span>|<span data-ttu-id="12487-135">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="12487-135">The operation name.</span></span>|
|<span data-ttu-id="12487-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="12487-136">lastModifiedDateTime</span></span>|<span data-ttu-id="12487-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="12487-137">DateTimeOffset</span></span>|<span data-ttu-id="12487-138">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="12487-138">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="12487-139">state</span><span class="sxs-lookup"><span data-stu-id="12487-139">state</span></span>|<span data-ttu-id="12487-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="12487-140">String</span></span>|<span data-ttu-id="12487-141">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="12487-141">The current state of the operation</span></span>|
|<span data-ttu-id="12487-142">id</span><span class="sxs-lookup"><span data-stu-id="12487-142">id</span></span>|<span data-ttu-id="12487-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="12487-143">String</span></span>|<span data-ttu-id="12487-144">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="12487-144">Key of the entity.</span></span>|
|<span data-ttu-id="12487-145">version</span><span class="sxs-lookup"><span data-stu-id="12487-145">version</span></span>|<span data-ttu-id="12487-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="12487-146">String</span></span>|<span data-ttu-id="12487-147">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="12487-147">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="12487-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12487-148">Response</span></span>
<span data-ttu-id="12487-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12487-149">If successful, this method returns a `201 Created` response code and a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="12487-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12487-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="12487-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="12487-151">Request</span></span>
<span data-ttu-id="12487-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="12487-152">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="12487-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12487-153">Response</span></span>
<span data-ttu-id="12487-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="12487-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





