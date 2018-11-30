---
title: Actualizar targetedManagedAppConfiguration
description: Actualice las propiedades de un objeto targetedManagedAppConfiguration.
ms.openlocfilehash: 097665b53250c90bbe553d72b2e82dabac6a11ba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088244"
---
# <a name="update-targetedmanagedappconfiguration"></a><span data-ttu-id="56970-103">Actualizar targetedManagedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="56970-103">Update targetedManagedAppConfiguration</span></span>

> <span data-ttu-id="56970-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="56970-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="56970-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="56970-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="56970-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56970-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56970-107">Actualice las propiedades de un objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="56970-107">Update the properties of a [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="56970-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56970-108">Prerequisites</span></span>
<span data-ttu-id="56970-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="56970-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="56970-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56970-111">Permission type</span></span>|<span data-ttu-id="56970-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56970-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="56970-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56970-113">Delegated (work or school account)</span></span>|<span data-ttu-id="56970-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56970-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="56970-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56970-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="56970-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56970-116">Not supported.</span></span>|
|<span data-ttu-id="56970-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56970-117">Application</span></span>|<span data-ttu-id="56970-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56970-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="56970-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56970-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="56970-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56970-120">Request headers</span></span>
|<span data-ttu-id="56970-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56970-121">Header</span></span>|<span data-ttu-id="56970-122">Valor</span><span class="sxs-lookup"><span data-stu-id="56970-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="56970-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="56970-123">Authorization</span></span>|<span data-ttu-id="56970-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="56970-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="56970-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="56970-125">Accept</span></span>|<span data-ttu-id="56970-126">application/json</span><span class="sxs-lookup"><span data-stu-id="56970-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="56970-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56970-127">Request body</span></span>
<span data-ttu-id="56970-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="56970-128">In the request body, supply a JSON representation for the [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object.</span></span>

<span data-ttu-id="56970-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="56970-129">The following table shows the properties that are required when you create the [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span></span>

|<span data-ttu-id="56970-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56970-130">Property</span></span>|<span data-ttu-id="56970-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="56970-131">Type</span></span>|<span data-ttu-id="56970-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="56970-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56970-133">displayName</span><span class="sxs-lookup"><span data-stu-id="56970-133">displayName</span></span>|<span data-ttu-id="56970-134">String</span><span class="sxs-lookup"><span data-stu-id="56970-134">String</span></span>|<span data-ttu-id="56970-135">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="56970-135">Policy display name.</span></span> <span data-ttu-id="56970-136">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56970-136">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="56970-137">descripción</span><span class="sxs-lookup"><span data-stu-id="56970-137">description</span></span>|<span data-ttu-id="56970-138">String</span><span class="sxs-lookup"><span data-stu-id="56970-138">String</span></span>|<span data-ttu-id="56970-139">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="56970-139">The policy's description.</span></span> <span data-ttu-id="56970-140">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56970-140">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="56970-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="56970-141">createdDateTime</span></span>|<span data-ttu-id="56970-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56970-142">DateTimeOffset</span></span>|<span data-ttu-id="56970-143">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="56970-143">The date and time the policy was created.</span></span> <span data-ttu-id="56970-144">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56970-144">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="56970-145">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="56970-145">lastModifiedDateTime</span></span>|<span data-ttu-id="56970-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56970-146">DateTimeOffset</span></span>|<span data-ttu-id="56970-147">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="56970-147">Last time the policy was modified.</span></span> <span data-ttu-id="56970-148">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56970-148">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="56970-149">id</span><span class="sxs-lookup"><span data-stu-id="56970-149">id</span></span>|<span data-ttu-id="56970-150">String</span><span class="sxs-lookup"><span data-stu-id="56970-150">String</span></span>|<span data-ttu-id="56970-151">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="56970-151">Key of the entity.</span></span> <span data-ttu-id="56970-152">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56970-152">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="56970-153">version</span><span class="sxs-lookup"><span data-stu-id="56970-153">version</span></span>|<span data-ttu-id="56970-154">String</span><span class="sxs-lookup"><span data-stu-id="56970-154">String</span></span>|<span data-ttu-id="56970-155">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="56970-155">Version of the entity.</span></span> <span data-ttu-id="56970-156">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56970-156">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="56970-157">customSettings</span><span class="sxs-lookup"><span data-stu-id="56970-157">customSettings</span></span>|<span data-ttu-id="56970-158">Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="56970-158">[keyValuePair](../resources/intune-shared-keyvaluepair.md) collection</span></span>|<span data-ttu-id="56970-159">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio. Heredado de [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="56970-159">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service Inherited from [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md)</span></span>|
|<span data-ttu-id="56970-160">deployedAppCount</span><span class="sxs-lookup"><span data-stu-id="56970-160">deployedAppCount</span></span>|<span data-ttu-id="56970-161">Int32</span><span class="sxs-lookup"><span data-stu-id="56970-161">Int32</span></span>|<span data-ttu-id="56970-162">Número de aplicaciones en las que se implementará la directiva actual.</span><span class="sxs-lookup"><span data-stu-id="56970-162">Count of apps to which the current policy is deployed.</span></span>|
|<span data-ttu-id="56970-163">isAssigned</span><span class="sxs-lookup"><span data-stu-id="56970-163">isAssigned</span></span>|<span data-ttu-id="56970-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="56970-164">Boolean</span></span>|<span data-ttu-id="56970-165">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="56970-165">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|



## <a name="response"></a><span data-ttu-id="56970-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56970-166">Response</span></span>
<span data-ttu-id="56970-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56970-167">If successful, this method returns a `200 OK` response code and an updated [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="56970-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56970-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="56970-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56970-169">Request</span></span>
<span data-ttu-id="56970-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56970-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
Content-type: application/json
Content-length: 382

{
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
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

### <a name="response"></a><span data-ttu-id="56970-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56970-171">Response</span></span>
<span data-ttu-id="56970-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56970-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





