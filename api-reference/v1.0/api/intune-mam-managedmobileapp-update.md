---
title: Actualizar managedMobileApp
description: Actualice las propiedades de un objeto managedMobileApp.
ms.openlocfilehash: af27f6aef199e896c251259cad7c22ae39566ffc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028750"
---
# <a name="update-managedmobileapp"></a><span data-ttu-id="f679d-103">Actualizar managedMobileApp</span><span class="sxs-lookup"><span data-stu-id="f679d-103">Update managedMobileApp</span></span>

> <span data-ttu-id="f679d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f679d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f679d-105">Actualice las propiedades de un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f679d-105">Update the properties of a [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f679d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f679d-106">Prerequisites</span></span>
<span data-ttu-id="f679d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f679d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f679d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f679d-109">Permission type</span></span>|<span data-ttu-id="f679d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f679d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f679d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f679d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f679d-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f679d-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f679d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f679d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f679d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f679d-114">Not supported.</span></span>|
|<span data-ttu-id="f679d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f679d-115">Application</span></span>|<span data-ttu-id="f679d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f679d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f679d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f679d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps/{managedMobileAppId}
PATCH /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/apps/{managedMobileAppId}
PATCH /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/apps/{managedMobileAppId}
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/apps/{managedMobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="f679d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f679d-118">Request headers</span></span>
|<span data-ttu-id="f679d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f679d-119">Header</span></span>|<span data-ttu-id="f679d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f679d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f679d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f679d-121">Authorization</span></span>|<span data-ttu-id="f679d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f679d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f679d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f679d-123">Accept</span></span>|<span data-ttu-id="f679d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f679d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f679d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f679d-125">Request body</span></span>
<span data-ttu-id="f679d-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f679d-126">In the request body, supply a JSON representation for the [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object.</span></span>

<span data-ttu-id="f679d-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f679d-127">The following table shows the properties that are required when you create the [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span></span>

|<span data-ttu-id="f679d-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f679d-128">Property</span></span>|<span data-ttu-id="f679d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f679d-129">Type</span></span>|<span data-ttu-id="f679d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f679d-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f679d-131">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="f679d-131">mobileAppIdentifier</span></span>|[<span data-ttu-id="f679d-132">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="f679d-132">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="f679d-133">El identificador de una aplicación con el tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f679d-133">The identifier for an app with it's operating system type.</span></span>|
|<span data-ttu-id="f679d-134">id</span><span class="sxs-lookup"><span data-stu-id="f679d-134">id</span></span>|<span data-ttu-id="f679d-135">String</span><span class="sxs-lookup"><span data-stu-id="f679d-135">String</span></span>|<span data-ttu-id="f679d-136">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f679d-136">Key of the entity.</span></span>|
|<span data-ttu-id="f679d-137">version</span><span class="sxs-lookup"><span data-stu-id="f679d-137">version</span></span>|<span data-ttu-id="f679d-138">String</span><span class="sxs-lookup"><span data-stu-id="f679d-138">String</span></span>|<span data-ttu-id="f679d-139">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f679d-139">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="f679d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f679d-140">Response</span></span>
<span data-ttu-id="f679d-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f679d-141">If successful, this method returns a `200 OK` response code and an updated [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f679d-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f679d-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="f679d-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f679d-143">Request</span></span>
<span data-ttu-id="f679d-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f679d-144">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps/{managedMobileAppId}
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

### <a name="response"></a><span data-ttu-id="f679d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f679d-145">Response</span></span>
<span data-ttu-id="f679d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f679d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



