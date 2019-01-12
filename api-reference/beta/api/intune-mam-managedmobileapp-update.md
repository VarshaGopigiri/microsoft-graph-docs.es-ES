---
title: Actualizar managedMobileApp
description: Actualice las propiedades de un objeto managedMobileApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8d4c15837222d67cdbc806006a27354f14a7fa1b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933564"
---
# <a name="update-managedmobileapp"></a><span data-ttu-id="35f8a-103">Actualizar managedMobileApp</span><span class="sxs-lookup"><span data-stu-id="35f8a-103">Update managedMobileApp</span></span>

> <span data-ttu-id="35f8a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35f8a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35f8a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35f8a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="35f8a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35f8a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35f8a-107">Actualice las propiedades de un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="35f8a-107">Update the properties of a [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="35f8a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="35f8a-108">Prerequisites</span></span>
<span data-ttu-id="35f8a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35f8a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="35f8a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35f8a-111">Permission type</span></span>|<span data-ttu-id="35f8a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35f8a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="35f8a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35f8a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="35f8a-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="35f8a-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="35f8a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35f8a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="35f8a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35f8a-116">Not supported.</span></span>|
|<span data-ttu-id="35f8a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35f8a-117">Application</span></span>|<span data-ttu-id="35f8a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35f8a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="35f8a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35f8a-119">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="35f8a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35f8a-120">Request headers</span></span>
|<span data-ttu-id="35f8a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35f8a-121">Header</span></span>|<span data-ttu-id="35f8a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="35f8a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="35f8a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="35f8a-123">Authorization</span></span>|<span data-ttu-id="35f8a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="35f8a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="35f8a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="35f8a-125">Accept</span></span>|<span data-ttu-id="35f8a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="35f8a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="35f8a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35f8a-127">Request body</span></span>
<span data-ttu-id="35f8a-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="35f8a-128">In the request body, supply a JSON representation for the [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object.</span></span>

<span data-ttu-id="35f8a-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="35f8a-129">The following table shows the properties that are required when you create the [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span></span>

|<span data-ttu-id="35f8a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="35f8a-130">Property</span></span>|<span data-ttu-id="35f8a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="35f8a-131">Type</span></span>|<span data-ttu-id="35f8a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="35f8a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="35f8a-133">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="35f8a-133">mobileAppIdentifier</span></span>|[<span data-ttu-id="35f8a-134">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="35f8a-134">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="35f8a-135">El identificador de una aplicación con el tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="35f8a-135">The identifier for an app with it's operating system type.</span></span>|
|<span data-ttu-id="35f8a-136">id</span><span class="sxs-lookup"><span data-stu-id="35f8a-136">id</span></span>|<span data-ttu-id="35f8a-137">String</span><span class="sxs-lookup"><span data-stu-id="35f8a-137">String</span></span>|<span data-ttu-id="35f8a-138">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="35f8a-138">Key of the entity.</span></span>|
|<span data-ttu-id="35f8a-139">version</span><span class="sxs-lookup"><span data-stu-id="35f8a-139">version</span></span>|<span data-ttu-id="35f8a-140">String</span><span class="sxs-lookup"><span data-stu-id="35f8a-140">String</span></span>|<span data-ttu-id="35f8a-141">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="35f8a-141">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="35f8a-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35f8a-142">Response</span></span>
<span data-ttu-id="35f8a-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35f8a-143">If successful, this method returns a `200 OK` response code and an updated [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="35f8a-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35f8a-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="35f8a-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35f8a-145">Request</span></span>
<span data-ttu-id="35f8a-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35f8a-146">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps/{managedMobileAppId}
Content-type: application/json
Content-length: 126

{
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="35f8a-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35f8a-147">Response</span></span>
<span data-ttu-id="35f8a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35f8a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





