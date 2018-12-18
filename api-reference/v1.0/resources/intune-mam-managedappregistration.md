---
title: Tipo de recurso managedAppRegistration
description: El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.
author: tfitzmac
ms.openlocfilehash: 218a36a283febe646afcc6f9c9bcbd0ed5abf46a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347792"
---
# <a name="managedappregistration-resource-type"></a><span data-ttu-id="a7589-103">Tipo de recurso managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="a7589-103">managedAppRegistration resource type</span></span>

> <span data-ttu-id="a7589-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7589-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7589-105">El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a7589-105">The ManagedAppEntity is the base entity type for all other entity types under app management workflow.</span></span>
<span data-ttu-id="a7589-106">El recurso ManagedAppRegistration representa los detalles de una aplicación, con capacidad de administración, usado por un miembro de la organización.</span><span class="sxs-lookup"><span data-stu-id="a7589-106">The ManagedAppRegistration resource represents the details of an app, with management capability, used by a member of the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="a7589-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a7589-107">Methods</span></span>
|<span data-ttu-id="a7589-108">Método</span><span class="sxs-lookup"><span data-stu-id="a7589-108">Method</span></span>|<span data-ttu-id="a7589-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7589-109">Return Type</span></span>|<span data-ttu-id="a7589-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7589-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a7589-111">Enumerar managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="a7589-111">List managedAppRegistrations</span></span>](../api/intune-mam-managedappregistration-list.md)|<span data-ttu-id="a7589-112">Colección [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="a7589-112">[managedAppRegistration](../resources/intune-mam-managedappregistration.md) collection</span></span>|<span data-ttu-id="a7589-113">Enumere las propiedades y las relaciones de los objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="a7589-113">List properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) objects.</span></span>|
|[<span data-ttu-id="a7589-114">Obtener managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="a7589-114">Get managedAppRegistration</span></span>](../api/intune-mam-managedappregistration-get.md)|[<span data-ttu-id="a7589-115">managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="a7589-115">managedAppRegistration</span></span>](../resources/intune-mam-managedappregistration.md)|<span data-ttu-id="a7589-116">Lea las propiedades y las relaciones del objeto [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="a7589-116">Read properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) object.</span></span>|
|[<span data-ttu-id="a7589-117">Función getUserIdsWithFlaggedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="a7589-117">getUserIdsWithFlaggedAppRegistration function</span></span>](../api/intune-mam-managedappregistration-getuseridswithflaggedappregistration.md)|<span data-ttu-id="a7589-118">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="a7589-118">String collection</span></span>|<span data-ttu-id="a7589-119">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a7589-119">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="a7589-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7589-120">Properties</span></span>
|<span data-ttu-id="a7589-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7589-121">Property</span></span>|<span data-ttu-id="a7589-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7589-122">Type</span></span>|<span data-ttu-id="a7589-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7589-123">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a7589-124">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a7589-124">createdDateTime</span></span>|<span data-ttu-id="a7589-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a7589-125">DateTimeOffset</span></span>|<span data-ttu-id="a7589-126">Fecha y hora de creación</span><span class="sxs-lookup"><span data-stu-id="a7589-126">Date and time of creation</span></span>|
|<span data-ttu-id="a7589-127">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="a7589-127">lastSyncDateTime</span></span>|<span data-ttu-id="a7589-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a7589-128">DateTimeOffset</span></span>|<span data-ttu-id="a7589-129">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="a7589-129">Date and time of last the app synced with management service.</span></span>|
|<span data-ttu-id="a7589-130">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="a7589-130">applicationVersion</span></span>|<span data-ttu-id="a7589-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7589-131">String</span></span>|<span data-ttu-id="a7589-132">Versión de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a7589-132">App version</span></span>|
|<span data-ttu-id="a7589-133">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="a7589-133">managementSdkVersion</span></span>|<span data-ttu-id="a7589-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7589-134">String</span></span>|<span data-ttu-id="a7589-135">Versión del SDK de administración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a7589-135">App management SDK version</span></span>|
|<span data-ttu-id="a7589-136">platformVersion</span><span class="sxs-lookup"><span data-stu-id="a7589-136">platformVersion</span></span>|<span data-ttu-id="a7589-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7589-137">String</span></span>|<span data-ttu-id="a7589-138">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a7589-138">Operating System version</span></span>|
|<span data-ttu-id="a7589-139">deviceType</span><span class="sxs-lookup"><span data-stu-id="a7589-139">deviceType</span></span>|<span data-ttu-id="a7589-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7589-140">String</span></span>|<span data-ttu-id="a7589-141">Tipo de dispositivo host</span><span class="sxs-lookup"><span data-stu-id="a7589-141">Host device type</span></span>|
|<span data-ttu-id="a7589-142">deviceTag</span><span class="sxs-lookup"><span data-stu-id="a7589-142">deviceTag</span></span>|<span data-ttu-id="a7589-143">String</span><span class="sxs-lookup"><span data-stu-id="a7589-143">String</span></span>|<span data-ttu-id="a7589-144">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7589-144">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="a7589-145">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="a7589-145">Not guaranteed to relate apps in all conditions.</span></span>|
|<span data-ttu-id="a7589-146">deviceName</span><span class="sxs-lookup"><span data-stu-id="a7589-146">deviceName</span></span>|<span data-ttu-id="a7589-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7589-147">String</span></span>|<span data-ttu-id="a7589-148">Nombre del dispositivo host</span><span class="sxs-lookup"><span data-stu-id="a7589-148">Host device name</span></span>|
|<span data-ttu-id="a7589-149">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="a7589-149">flaggedReasons</span></span>|<span data-ttu-id="a7589-150">colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)</span><span class="sxs-lookup"><span data-stu-id="a7589-150">[managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md) collection</span></span>|<span data-ttu-id="a7589-151">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a7589-151">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="a7589-152">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="a7589-152">E.g.</span></span> <span data-ttu-id="a7589-153">una aplicación que se ejecuta en el dispositivo liberado</span><span class="sxs-lookup"><span data-stu-id="a7589-153">app running on rooted device</span></span>|
|<span data-ttu-id="a7589-154">userId</span><span class="sxs-lookup"><span data-stu-id="a7589-154">userId</span></span>|<span data-ttu-id="a7589-155">String</span><span class="sxs-lookup"><span data-stu-id="a7589-155">String</span></span>|<span data-ttu-id="a7589-156">El identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a7589-156">The user Id to who this app registration belongs.</span></span>|
|<span data-ttu-id="a7589-157">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="a7589-157">appIdentifier</span></span>|[<span data-ttu-id="a7589-158">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="a7589-158">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="a7589-159">El identificador del paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="a7589-159">The app package Identifier</span></span>|
|<span data-ttu-id="a7589-160">id</span><span class="sxs-lookup"><span data-stu-id="a7589-160">id</span></span>|<span data-ttu-id="a7589-161">String</span><span class="sxs-lookup"><span data-stu-id="a7589-161">String</span></span>|<span data-ttu-id="a7589-162">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a7589-162">Key of the entity.</span></span>|
|<span data-ttu-id="a7589-163">version</span><span class="sxs-lookup"><span data-stu-id="a7589-163">version</span></span>|<span data-ttu-id="a7589-164">String</span><span class="sxs-lookup"><span data-stu-id="a7589-164">String</span></span>|<span data-ttu-id="a7589-165">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a7589-165">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a7589-166">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a7589-166">Relationships</span></span>
|<span data-ttu-id="a7589-167">Relación</span><span class="sxs-lookup"><span data-stu-id="a7589-167">Relationship</span></span>|<span data-ttu-id="a7589-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7589-168">Type</span></span>|<span data-ttu-id="a7589-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7589-169">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a7589-170">appliedPolicies</span><span class="sxs-lookup"><span data-stu-id="a7589-170">appliedPolicies</span></span>|<span data-ttu-id="a7589-171">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="a7589-171">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="a7589-172">Ya se habían aplicado cero o más directivas en la aplicación registrada cuando se sincronizó por última vez con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="a7589-172">Zero or more policys already applied on the registered app when it last synchronized with managment service.</span></span>|
|<span data-ttu-id="a7589-173">intendedPolicies</span><span class="sxs-lookup"><span data-stu-id="a7589-173">intendedPolicies</span></span>|<span data-ttu-id="a7589-174">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="a7589-174">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="a7589-175">El administrador esperaba cero o más directivas hasta el momento.</span><span class="sxs-lookup"><span data-stu-id="a7589-175">Zero or more policies admin intended for the app as of now.</span></span>|
|<span data-ttu-id="a7589-176">operaciones</span><span class="sxs-lookup"><span data-stu-id="a7589-176">operations</span></span>|<span data-ttu-id="a7589-177">Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)</span><span class="sxs-lookup"><span data-stu-id="a7589-177">[managedAppOperation](../resources/intune-mam-managedappoperation.md) collection</span></span>|<span data-ttu-id="a7589-178">Se activaron cero o más operaciones de larga duración en el registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a7589-178">Zero or more long running operations triggered on the app registration.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a7589-179">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7589-179">JSON Representation</span></span>
<span data-ttu-id="a7589-180">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a7589-180">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppRegistration",
  "createdDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "applicationVersion": "String",
  "managementSdkVersion": "String",
  "platformVersion": "String",
  "deviceType": "String",
  "deviceTag": "String",
  "deviceName": "String",
  "flaggedReasons": [
    "String"
  ],
  "userId": "String",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "String (identifier)",
  "version": "String"
}
```


<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-mam-managedappregistration.md/microsoft.graph.managedAppRegistration/flaggedReasons:
      Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->
