---
title: Tipo de recurso managedAppRegistration
description: El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7543f7cf591e1e89c05359634b7c4ec55a327b33
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825770"
---
# <a name="managedappregistration-resource-type"></a><span data-ttu-id="b994d-103">Tipo de recurso managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="b994d-103">managedAppRegistration resource type</span></span>

> <span data-ttu-id="b994d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b994d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b994d-105">El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b994d-105">The ManagedAppEntity is the base entity type for all other entity types under app management workflow.</span></span>
<span data-ttu-id="b994d-106">El recurso ManagedAppRegistration representa los detalles de una aplicación, con capacidad de administración, usado por un miembro de la organización.</span><span class="sxs-lookup"><span data-stu-id="b994d-106">The ManagedAppRegistration resource represents the details of an app, with management capability, used by a member of the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="b994d-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="b994d-107">Methods</span></span>
|<span data-ttu-id="b994d-108">Método</span><span class="sxs-lookup"><span data-stu-id="b994d-108">Method</span></span>|<span data-ttu-id="b994d-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b994d-109">Return Type</span></span>|<span data-ttu-id="b994d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b994d-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="b994d-111">Enumerar managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="b994d-111">List managedAppRegistrations</span></span>](../api/intune-mam-managedappregistration-list.md)|<span data-ttu-id="b994d-112">Colección [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="b994d-112">[managedAppRegistration](../resources/intune-mam-managedappregistration.md) collection</span></span>|<span data-ttu-id="b994d-113">Enumere las propiedades y las relaciones de los objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="b994d-113">List properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) objects.</span></span>|
|[<span data-ttu-id="b994d-114">Obtener managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="b994d-114">Get managedAppRegistration</span></span>](../api/intune-mam-managedappregistration-get.md)|[<span data-ttu-id="b994d-115">managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="b994d-115">managedAppRegistration</span></span>](../resources/intune-mam-managedappregistration.md)|<span data-ttu-id="b994d-116">Lea las propiedades y las relaciones del objeto [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="b994d-116">Read properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) object.</span></span>|
|[<span data-ttu-id="b994d-117">Función getUserIdsWithFlaggedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="b994d-117">getUserIdsWithFlaggedAppRegistration function</span></span>](../api/intune-mam-managedappregistration-getuseridswithflaggedappregistration.md)|<span data-ttu-id="b994d-118">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="b994d-118">String collection</span></span>|<span data-ttu-id="b994d-119">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b994d-119">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="b994d-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b994d-120">Properties</span></span>
|<span data-ttu-id="b994d-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b994d-121">Property</span></span>|<span data-ttu-id="b994d-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b994d-122">Type</span></span>|<span data-ttu-id="b994d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b994d-123">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b994d-124">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b994d-124">createdDateTime</span></span>|<span data-ttu-id="b994d-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b994d-125">DateTimeOffset</span></span>|<span data-ttu-id="b994d-126">Fecha y hora de creación</span><span class="sxs-lookup"><span data-stu-id="b994d-126">Date and time of creation</span></span>|
|<span data-ttu-id="b994d-127">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="b994d-127">lastSyncDateTime</span></span>|<span data-ttu-id="b994d-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b994d-128">DateTimeOffset</span></span>|<span data-ttu-id="b994d-129">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="b994d-129">Date and time of last the app synced with management service.</span></span>|
|<span data-ttu-id="b994d-130">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="b994d-130">applicationVersion</span></span>|<span data-ttu-id="b994d-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-131">String</span></span>|<span data-ttu-id="b994d-132">Versión de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b994d-132">App version</span></span>|
|<span data-ttu-id="b994d-133">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="b994d-133">managementSdkVersion</span></span>|<span data-ttu-id="b994d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-134">String</span></span>|<span data-ttu-id="b994d-135">Versión del SDK de administración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b994d-135">App management SDK version</span></span>|
|<span data-ttu-id="b994d-136">platformVersion</span><span class="sxs-lookup"><span data-stu-id="b994d-136">platformVersion</span></span>|<span data-ttu-id="b994d-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-137">String</span></span>|<span data-ttu-id="b994d-138">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b994d-138">Operating System version</span></span>|
|<span data-ttu-id="b994d-139">deviceType</span><span class="sxs-lookup"><span data-stu-id="b994d-139">deviceType</span></span>|<span data-ttu-id="b994d-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-140">String</span></span>|<span data-ttu-id="b994d-141">Tipo de dispositivo host</span><span class="sxs-lookup"><span data-stu-id="b994d-141">Host device type</span></span>|
|<span data-ttu-id="b994d-142">deviceTag</span><span class="sxs-lookup"><span data-stu-id="b994d-142">deviceTag</span></span>|<span data-ttu-id="b994d-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-143">String</span></span>|<span data-ttu-id="b994d-144">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b994d-144">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="b994d-145">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="b994d-145">Not guaranteed to relate apps in all conditions.</span></span>|
|<span data-ttu-id="b994d-146">deviceName</span><span class="sxs-lookup"><span data-stu-id="b994d-146">deviceName</span></span>|<span data-ttu-id="b994d-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-147">String</span></span>|<span data-ttu-id="b994d-148">Nombre del dispositivo host</span><span class="sxs-lookup"><span data-stu-id="b994d-148">Host device name</span></span>|
|<span data-ttu-id="b994d-149">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="b994d-149">flaggedReasons</span></span>|<span data-ttu-id="b994d-150">colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)</span><span class="sxs-lookup"><span data-stu-id="b994d-150">[managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md) collection</span></span>|<span data-ttu-id="b994d-151">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b994d-151">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="b994d-152">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="b994d-152">E.g.</span></span> <span data-ttu-id="b994d-153">una aplicación que se ejecuta en el dispositivo liberado</span><span class="sxs-lookup"><span data-stu-id="b994d-153">app running on rooted device</span></span>|
|<span data-ttu-id="b994d-154">userId</span><span class="sxs-lookup"><span data-stu-id="b994d-154">userId</span></span>|<span data-ttu-id="b994d-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-155">String</span></span>|<span data-ttu-id="b994d-156">El identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b994d-156">The user Id to who this app registration belongs.</span></span>|
|<span data-ttu-id="b994d-157">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="b994d-157">appIdentifier</span></span>|[<span data-ttu-id="b994d-158">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="b994d-158">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="b994d-159">El identificador del paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="b994d-159">The app package Identifier</span></span>|
|<span data-ttu-id="b994d-160">id</span><span class="sxs-lookup"><span data-stu-id="b994d-160">id</span></span>|<span data-ttu-id="b994d-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-161">String</span></span>|<span data-ttu-id="b994d-162">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b994d-162">Key of the entity.</span></span>|
|<span data-ttu-id="b994d-163">version</span><span class="sxs-lookup"><span data-stu-id="b994d-163">version</span></span>|<span data-ttu-id="b994d-164">Cadena</span><span class="sxs-lookup"><span data-stu-id="b994d-164">String</span></span>|<span data-ttu-id="b994d-165">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b994d-165">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b994d-166">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b994d-166">Relationships</span></span>
|<span data-ttu-id="b994d-167">Relación</span><span class="sxs-lookup"><span data-stu-id="b994d-167">Relationship</span></span>|<span data-ttu-id="b994d-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="b994d-168">Type</span></span>|<span data-ttu-id="b994d-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="b994d-169">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b994d-170">appliedPolicies</span><span class="sxs-lookup"><span data-stu-id="b994d-170">appliedPolicies</span></span>|<span data-ttu-id="b994d-171">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b994d-171">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="b994d-172">Ya se habían aplicado cero o más directivas en la aplicación registrada cuando se sincronizó por última vez con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="b994d-172">Zero or more policys already applied on the registered app when it last synchronized with managment service.</span></span>|
|<span data-ttu-id="b994d-173">intendedPolicies</span><span class="sxs-lookup"><span data-stu-id="b994d-173">intendedPolicies</span></span>|<span data-ttu-id="b994d-174">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b994d-174">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="b994d-175">El administrador esperaba cero o más directivas hasta el momento.</span><span class="sxs-lookup"><span data-stu-id="b994d-175">Zero or more policies admin intended for the app as of now.</span></span>|
|<span data-ttu-id="b994d-176">operaciones</span><span class="sxs-lookup"><span data-stu-id="b994d-176">operations</span></span>|<span data-ttu-id="b994d-177">Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)</span><span class="sxs-lookup"><span data-stu-id="b994d-177">[managedAppOperation](../resources/intune-mam-managedappoperation.md) collection</span></span>|<span data-ttu-id="b994d-178">Se activaron cero o más operaciones de larga duración en el registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b994d-178">Zero or more long running operations triggered on the app registration.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b994d-179">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b994d-179">JSON Representation</span></span>
<span data-ttu-id="b994d-180">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b994d-180">Here is a JSON representation of the resource.</span></span>
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
