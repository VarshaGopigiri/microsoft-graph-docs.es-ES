---
title: Crear managedMobileApp
description: Cree un objeto managedMobileApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a79f8ce7e6cbad49c48f5b9b06bf7a86c8e414c4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805183"
---
# <a name="create-managedmobileapp"></a><span data-ttu-id="e0888-103">Crear managedMobileApp</span><span class="sxs-lookup"><span data-stu-id="e0888-103">Create managedMobileApp</span></span>

> <span data-ttu-id="e0888-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e0888-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e0888-105">Cree un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e0888-105">Create a new [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e0888-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e0888-106">Prerequisites</span></span>
<span data-ttu-id="e0888-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e0888-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e0888-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e0888-109">Permission type</span></span>|<span data-ttu-id="e0888-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e0888-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e0888-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e0888-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e0888-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0888-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e0888-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e0888-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e0888-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0888-114">Not supported.</span></span>|
|<span data-ttu-id="e0888-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e0888-115">Application</span></span>|<span data-ttu-id="e0888-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0888-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e0888-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e0888-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps
POST /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/apps
POST /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/apps
POST /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/apps
```

## <a name="request-headers"></a><span data-ttu-id="e0888-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0888-118">Request headers</span></span>
|<span data-ttu-id="e0888-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0888-119">Header</span></span>|<span data-ttu-id="e0888-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e0888-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e0888-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e0888-121">Authorization</span></span>|<span data-ttu-id="e0888-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e0888-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e0888-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e0888-123">Accept</span></span>|<span data-ttu-id="e0888-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e0888-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e0888-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e0888-125">Request body</span></span>
<span data-ttu-id="e0888-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedMobileApp.</span><span class="sxs-lookup"><span data-stu-id="e0888-126">In the request body, supply a JSON representation for the managedMobileApp object.</span></span>

<span data-ttu-id="e0888-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedMobileApp.</span><span class="sxs-lookup"><span data-stu-id="e0888-127">The following table shows the properties that are required when you create the managedMobileApp.</span></span>

|<span data-ttu-id="e0888-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0888-128">Property</span></span>|<span data-ttu-id="e0888-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0888-129">Type</span></span>|<span data-ttu-id="e0888-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0888-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e0888-131">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="e0888-131">mobileAppIdentifier</span></span>|[<span data-ttu-id="e0888-132">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="e0888-132">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="e0888-133">El identificador de una aplicación con el tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e0888-133">The identifier for an app with it's operating system type.</span></span>|
|<span data-ttu-id="e0888-134">id</span><span class="sxs-lookup"><span data-stu-id="e0888-134">id</span></span>|<span data-ttu-id="e0888-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="e0888-135">String</span></span>|<span data-ttu-id="e0888-136">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e0888-136">Key of the entity.</span></span>|
|<span data-ttu-id="e0888-137">version</span><span class="sxs-lookup"><span data-stu-id="e0888-137">version</span></span>|<span data-ttu-id="e0888-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="e0888-138">String</span></span>|<span data-ttu-id="e0888-139">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e0888-139">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="e0888-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0888-140">Response</span></span>
<span data-ttu-id="e0888-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0888-141">If successful, this method returns a `201 Created` response code and a [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e0888-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0888-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="e0888-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e0888-143">Request</span></span>
<span data-ttu-id="e0888-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0888-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps
Content-type: application/json
Content-length: 181

{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="e0888-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0888-145">Response</span></span>
<span data-ttu-id="e0888-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e0888-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 230

{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "0a129715-9715-0a12-1597-120a1597120a",
  "version": "Version value"
}
```



