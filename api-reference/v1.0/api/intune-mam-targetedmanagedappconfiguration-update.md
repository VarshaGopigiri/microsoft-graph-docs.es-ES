---
title: Actualizar targetedManagedAppConfiguration
description: Actualice las propiedades de un objeto targetedManagedAppConfiguration.
author: tfitzmac
ms.openlocfilehash: 3207c0ffca215ae3a0669b28e60e624cd7630648
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310545"
---
# <a name="update-targetedmanagedappconfiguration"></a><span data-ttu-id="80903-103">Actualizar targetedManagedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="80903-103">Update targetedManagedAppConfiguration</span></span>

> <span data-ttu-id="80903-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80903-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80903-105">Actualice las propiedades de un objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="80903-105">Update the properties of a [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="80903-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="80903-106">Prerequisites</span></span>
<span data-ttu-id="80903-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="80903-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="80903-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="80903-109">Permission type</span></span>|<span data-ttu-id="80903-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="80903-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="80903-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="80903-111">Delegated (work or school account)</span></span>|<span data-ttu-id="80903-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80903-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="80903-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="80903-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="80903-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80903-114">Not supported.</span></span>|
|<span data-ttu-id="80903-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="80903-115">Application</span></span>|<span data-ttu-id="80903-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80903-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="80903-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="80903-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="80903-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="80903-118">Request headers</span></span>
|<span data-ttu-id="80903-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80903-119">Header</span></span>|<span data-ttu-id="80903-120">Valor</span><span class="sxs-lookup"><span data-stu-id="80903-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="80903-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="80903-121">Authorization</span></span>|<span data-ttu-id="80903-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="80903-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="80903-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="80903-123">Accept</span></span>|<span data-ttu-id="80903-124">application/json</span><span class="sxs-lookup"><span data-stu-id="80903-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="80903-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="80903-125">Request body</span></span>
<span data-ttu-id="80903-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="80903-126">In the request body, supply a JSON representation for the [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object.</span></span>

<span data-ttu-id="80903-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="80903-127">The following table shows the properties that are required when you create the [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span></span>

|<span data-ttu-id="80903-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80903-128">Property</span></span>|<span data-ttu-id="80903-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="80903-129">Type</span></span>|<span data-ttu-id="80903-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="80903-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80903-131">displayName</span><span class="sxs-lookup"><span data-stu-id="80903-131">displayName</span></span>|<span data-ttu-id="80903-132">String</span><span class="sxs-lookup"><span data-stu-id="80903-132">String</span></span>|<span data-ttu-id="80903-133">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="80903-133">Policy display name.</span></span> <span data-ttu-id="80903-134">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="80903-134">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="80903-135">descripción</span><span class="sxs-lookup"><span data-stu-id="80903-135">description</span></span>|<span data-ttu-id="80903-136">String</span><span class="sxs-lookup"><span data-stu-id="80903-136">String</span></span>|<span data-ttu-id="80903-137">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="80903-137">The policy's description.</span></span> <span data-ttu-id="80903-138">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="80903-138">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="80903-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="80903-139">createdDateTime</span></span>|<span data-ttu-id="80903-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80903-140">DateTimeOffset</span></span>|<span data-ttu-id="80903-141">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="80903-141">The date and time the policy was created.</span></span> <span data-ttu-id="80903-142">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="80903-142">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="80903-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="80903-143">lastModifiedDateTime</span></span>|<span data-ttu-id="80903-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80903-144">DateTimeOffset</span></span>|<span data-ttu-id="80903-145">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="80903-145">Last time the policy was modified.</span></span> <span data-ttu-id="80903-146">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="80903-146">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="80903-147">id</span><span class="sxs-lookup"><span data-stu-id="80903-147">id</span></span>|<span data-ttu-id="80903-148">String</span><span class="sxs-lookup"><span data-stu-id="80903-148">String</span></span>|<span data-ttu-id="80903-149">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="80903-149">Key of the entity.</span></span> <span data-ttu-id="80903-150">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="80903-150">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="80903-151">version</span><span class="sxs-lookup"><span data-stu-id="80903-151">version</span></span>|<span data-ttu-id="80903-152">String</span><span class="sxs-lookup"><span data-stu-id="80903-152">String</span></span>|<span data-ttu-id="80903-153">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="80903-153">Version of the entity.</span></span> <span data-ttu-id="80903-154">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="80903-154">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="80903-155">customSettings</span><span class="sxs-lookup"><span data-stu-id="80903-155">customSettings</span></span>|<span data-ttu-id="80903-156">Colección [keyValuePair](../resources/intune-mam-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="80903-156">[keyValuePair](../resources/intune-mam-keyvaluepair.md) collection</span></span>|<span data-ttu-id="80903-157">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio. Heredado de [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80903-157">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service Inherited from [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span></span>|
|<span data-ttu-id="80903-158">deployedAppCount</span><span class="sxs-lookup"><span data-stu-id="80903-158">deployedAppCount</span></span>|<span data-ttu-id="80903-159">Int32</span><span class="sxs-lookup"><span data-stu-id="80903-159">Int32</span></span>|<span data-ttu-id="80903-160">Número de aplicaciones en las que se implementará la directiva actual.</span><span class="sxs-lookup"><span data-stu-id="80903-160">Count of apps to which the current policy is deployed.</span></span>|
|<span data-ttu-id="80903-161">isAssigned</span><span class="sxs-lookup"><span data-stu-id="80903-161">isAssigned</span></span>|<span data-ttu-id="80903-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="80903-162">Boolean</span></span>|<span data-ttu-id="80903-163">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="80903-163">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|



## <a name="response"></a><span data-ttu-id="80903-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80903-164">Response</span></span>
<span data-ttu-id="80903-165">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80903-165">If successful, this method returns a `200 OK` response code and an updated [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="80903-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80903-166">Example</span></span>
### <a name="request"></a><span data-ttu-id="80903-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="80903-167">Request</span></span>
<span data-ttu-id="80903-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80903-168">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
Content-type: application/json
Content-length: 388

{
  "@odata.type": "#microsoft.graph.targetedManagedAppConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "version": "Version value",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "deployedAppCount": 0,
  "isAssigned": true
}
```

### <a name="response"></a><span data-ttu-id="80903-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80903-169">Response</span></span>
<span data-ttu-id="80903-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="80903-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 560

{
  "@odata.type": "#microsoft.graph.targetedManagedAppConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "2444e029-e029-2444-29e0-442429e04424",
  "version": "Version value",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "deployedAppCount": 0,
  "isAssigned": true
}
```



