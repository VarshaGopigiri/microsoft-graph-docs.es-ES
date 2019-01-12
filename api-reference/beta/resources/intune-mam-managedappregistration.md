---
title: Tipo de recurso managedAppRegistration
description: El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 69d532f7c8287b678c1f62f5b8b78c6e4a99d2ef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944820"
---
# <a name="managedappregistration-resource-type"></a><span data-ttu-id="5c367-103">Tipo de recurso managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="5c367-103">managedAppRegistration resource type</span></span>

> <span data-ttu-id="5c367-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5c367-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5c367-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5c367-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5c367-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c367-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c367-107">El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5c367-107">The ManagedAppEntity is the base entity type for all other entity types under app management workflow.</span></span>
<span data-ttu-id="5c367-108">El recurso ManagedAppRegistration representa los detalles de una aplicación, con capacidad de administración, usado por un miembro de la organización.</span><span class="sxs-lookup"><span data-stu-id="5c367-108">The ManagedAppRegistration resource represents the details of an app, with management capability, used by a member of the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="5c367-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c367-109">Methods</span></span>
|<span data-ttu-id="5c367-110">Método</span><span class="sxs-lookup"><span data-stu-id="5c367-110">Method</span></span>|<span data-ttu-id="5c367-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c367-111">Return Type</span></span>|<span data-ttu-id="5c367-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c367-112">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="5c367-113">Enumerar managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="5c367-113">List managedAppRegistrations</span></span>](../api/intune-mam-managedappregistration-list.md)|<span data-ttu-id="5c367-114">Colección [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5c367-114">[managedAppRegistration](../resources/intune-mam-managedappregistration.md) collection</span></span>|<span data-ttu-id="5c367-115">Enumere las propiedades y las relaciones de los objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5c367-115">List properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) objects.</span></span>|
|[<span data-ttu-id="5c367-116">Obtener managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="5c367-116">Get managedAppRegistration</span></span>](../api/intune-mam-managedappregistration-get.md)|[<span data-ttu-id="5c367-117">managedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="5c367-117">managedAppRegistration</span></span>](../resources/intune-mam-managedappregistration.md)|<span data-ttu-id="5c367-118">Lea las propiedades y las relaciones del objeto [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5c367-118">Read properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) object.</span></span>|
|[<span data-ttu-id="5c367-119">Función getUserIdsWithFlaggedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="5c367-119">getUserIdsWithFlaggedAppRegistration function</span></span>](../api/intune-mam-managedappregistration-getuseridswithflaggedappregistration.md)|<span data-ttu-id="5c367-120">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="5c367-120">String collection</span></span>|<span data-ttu-id="5c367-121">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5c367-121">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="5c367-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c367-122">Properties</span></span>
|<span data-ttu-id="5c367-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c367-123">Property</span></span>|<span data-ttu-id="5c367-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c367-124">Type</span></span>|<span data-ttu-id="5c367-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c367-125">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c367-126">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5c367-126">createdDateTime</span></span>|<span data-ttu-id="5c367-127">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c367-127">DateTimeOffset</span></span>|<span data-ttu-id="5c367-128">Fecha y hora de creación</span><span class="sxs-lookup"><span data-stu-id="5c367-128">Date and time of creation</span></span>|
|<span data-ttu-id="5c367-129">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="5c367-129">lastSyncDateTime</span></span>|<span data-ttu-id="5c367-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c367-130">DateTimeOffset</span></span>|<span data-ttu-id="5c367-131">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="5c367-131">Date and time of last the app synced with management service.</span></span>|
|<span data-ttu-id="5c367-132">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="5c367-132">applicationVersion</span></span>|<span data-ttu-id="5c367-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-133">String</span></span>|<span data-ttu-id="5c367-134">Versión de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5c367-134">App version</span></span>|
|<span data-ttu-id="5c367-135">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="5c367-135">managementSdkVersion</span></span>|<span data-ttu-id="5c367-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-136">String</span></span>|<span data-ttu-id="5c367-137">Versión del SDK de administración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5c367-137">App management SDK version</span></span>|
|<span data-ttu-id="5c367-138">platformVersion</span><span class="sxs-lookup"><span data-stu-id="5c367-138">platformVersion</span></span>|<span data-ttu-id="5c367-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-139">String</span></span>|<span data-ttu-id="5c367-140">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5c367-140">Operating System version</span></span>|
|<span data-ttu-id="5c367-141">deviceType</span><span class="sxs-lookup"><span data-stu-id="5c367-141">deviceType</span></span>|<span data-ttu-id="5c367-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-142">String</span></span>|<span data-ttu-id="5c367-143">Tipo de dispositivo host</span><span class="sxs-lookup"><span data-stu-id="5c367-143">Host device type</span></span>|
|<span data-ttu-id="5c367-144">deviceTag</span><span class="sxs-lookup"><span data-stu-id="5c367-144">deviceTag</span></span>|<span data-ttu-id="5c367-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-145">String</span></span>|<span data-ttu-id="5c367-146">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c367-146">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="5c367-147">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="5c367-147">Not guaranteed to relate apps in all conditions.</span></span>|
|<span data-ttu-id="5c367-148">deviceName</span><span class="sxs-lookup"><span data-stu-id="5c367-148">deviceName</span></span>|<span data-ttu-id="5c367-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-149">String</span></span>|<span data-ttu-id="5c367-150">Nombre del dispositivo host</span><span class="sxs-lookup"><span data-stu-id="5c367-150">Host device name</span></span>|
|<span data-ttu-id="5c367-151">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="5c367-151">managedDeviceId</span></span>|<span data-ttu-id="5c367-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-152">String</span></span>|<span data-ttu-id="5c367-153">El identificador de dispositivo administrado del dispositivo host.</span><span class="sxs-lookup"><span data-stu-id="5c367-153">The Managed Device identifier of the host device.</span></span> <span data-ttu-id="5c367-154">Valor puede estar vacío, incluso cuando se administra el dispositivo host.</span><span class="sxs-lookup"><span data-stu-id="5c367-154">Value could be empty even when the host device is managed.</span></span>|
|<span data-ttu-id="5c367-155">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="5c367-155">azureADDeviceId</span></span>|<span data-ttu-id="5c367-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-156">String</span></span>|<span data-ttu-id="5c367-157">El identificador de dispositivo de Azure Active Directory del dispositivo host.</span><span class="sxs-lookup"><span data-stu-id="5c367-157">The Azure Active Directory Device identifier of the host device.</span></span> <span data-ttu-id="5c367-158">Valor puede estar vacío, incluso cuando el dispositivo de host es Azure Active Directory registrada.</span><span class="sxs-lookup"><span data-stu-id="5c367-158">Value could be empty even when the host device is Azure Active Directory registered.</span></span>|
|<span data-ttu-id="5c367-159">deviceModel</span><span class="sxs-lookup"><span data-stu-id="5c367-159">deviceModel</span></span>|<span data-ttu-id="5c367-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-160">String</span></span>|<span data-ttu-id="5c367-161">El modelo de dispositivo para el registro actual de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5c367-161">The device model for the current app registration</span></span> |
|<span data-ttu-id="5c367-162">entradas deviceManufacturer</span><span class="sxs-lookup"><span data-stu-id="5c367-162">deviceManufacturer</span></span>|<span data-ttu-id="5c367-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-163">String</span></span>|<span data-ttu-id="5c367-164">El fabricante del dispositivo para el registro actual de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5c367-164">The device manufacturer for the current app registration</span></span> |
|<span data-ttu-id="5c367-165">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="5c367-165">flaggedReasons</span></span>|<span data-ttu-id="5c367-166">colección de [managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)</span><span class="sxs-lookup"><span data-stu-id="5c367-166">[managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md) collection</span></span>|<span data-ttu-id="5c367-167">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c367-167">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="5c367-168">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="5c367-168">E.g.</span></span> <span data-ttu-id="5c367-169">una aplicación que se ejecuta en el dispositivo liberado</span><span class="sxs-lookup"><span data-stu-id="5c367-169">app running on rooted device</span></span>|
|<span data-ttu-id="5c367-170">userId</span><span class="sxs-lookup"><span data-stu-id="5c367-170">userId</span></span>|<span data-ttu-id="5c367-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-171">String</span></span>|<span data-ttu-id="5c367-172">El identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c367-172">The user Id to who this app registration belongs.</span></span>|
|<span data-ttu-id="5c367-173">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="5c367-173">appIdentifier</span></span>|[<span data-ttu-id="5c367-174">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="5c367-174">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="5c367-175">El identificador del paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="5c367-175">The app package Identifier</span></span>|
|<span data-ttu-id="5c367-176">id</span><span class="sxs-lookup"><span data-stu-id="5c367-176">id</span></span>|<span data-ttu-id="5c367-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-177">String</span></span>|<span data-ttu-id="5c367-178">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5c367-178">Key of the entity.</span></span>|
|<span data-ttu-id="5c367-179">version</span><span class="sxs-lookup"><span data-stu-id="5c367-179">version</span></span>|<span data-ttu-id="5c367-180">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c367-180">String</span></span>|<span data-ttu-id="5c367-181">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5c367-181">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5c367-182">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5c367-182">Relationships</span></span>
|<span data-ttu-id="5c367-183">Relación</span><span class="sxs-lookup"><span data-stu-id="5c367-183">Relationship</span></span>|<span data-ttu-id="5c367-184">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c367-184">Type</span></span>|<span data-ttu-id="5c367-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c367-185">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c367-186">appliedPolicies</span><span class="sxs-lookup"><span data-stu-id="5c367-186">appliedPolicies</span></span>|<span data-ttu-id="5c367-187">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="5c367-187">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="5c367-188">Ya se habían aplicado cero o más directivas en la aplicación registrada cuando se sincronizó por última vez con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="5c367-188">Zero or more policys already applied on the registered app when it last synchronized with managment service.</span></span>|
|<span data-ttu-id="5c367-189">intendedPolicies</span><span class="sxs-lookup"><span data-stu-id="5c367-189">intendedPolicies</span></span>|<span data-ttu-id="5c367-190">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="5c367-190">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="5c367-191">El administrador esperaba cero o más directivas hasta el momento.</span><span class="sxs-lookup"><span data-stu-id="5c367-191">Zero or more policies admin intended for the app as of now.</span></span>|
|<span data-ttu-id="5c367-192">operaciones</span><span class="sxs-lookup"><span data-stu-id="5c367-192">operations</span></span>|<span data-ttu-id="5c367-193">Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)</span><span class="sxs-lookup"><span data-stu-id="5c367-193">[managedAppOperation](../resources/intune-mam-managedappoperation.md) collection</span></span>|<span data-ttu-id="5c367-194">Se activaron cero o más operaciones de larga duración en el registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c367-194">Zero or more long running operations triggered on the app registration.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5c367-195">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5c367-195">JSON Representation</span></span>
<span data-ttu-id="5c367-196">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5c367-196">Here is a JSON representation of the resource.</span></span>
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
  "managedDeviceId": "String",
  "azureADDeviceId": "String",
  "deviceModel": "String",
  "deviceManufacturer": "String",
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





