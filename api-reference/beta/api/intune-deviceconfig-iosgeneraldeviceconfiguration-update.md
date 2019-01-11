---
title: Actualizar iosGeneralDeviceConfiguration
description: Actualice las propiedades de un objeto iosGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8c4aa2af2946c7e99d8a17b3bc98a688b10efd04
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854022"
---
# <a name="update-iosgeneraldeviceconfiguration"></a><span data-ttu-id="0e440-103">Actualizar iosGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e440-103">Update iosGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="0e440-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0e440-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0e440-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0e440-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0e440-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e440-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e440-107">Actualice las propiedades de un objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0e440-107">Update the properties of a [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0e440-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0e440-108">Prerequisites</span></span>
<span data-ttu-id="0e440-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e440-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e440-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e440-111">Permission type</span></span>|<span data-ttu-id="0e440-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e440-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0e440-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e440-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0e440-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e440-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0e440-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e440-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0e440-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e440-116">Not supported.</span></span>|
|<span data-ttu-id="0e440-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e440-117">Application</span></span>|<span data-ttu-id="0e440-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e440-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0e440-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e440-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="0e440-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e440-120">Request headers</span></span>
|<span data-ttu-id="0e440-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e440-121">Header</span></span>|<span data-ttu-id="0e440-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0e440-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0e440-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0e440-123">Authorization</span></span>|<span data-ttu-id="0e440-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0e440-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0e440-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0e440-125">Accept</span></span>|<span data-ttu-id="0e440-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0e440-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0e440-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e440-127">Request body</span></span>
<span data-ttu-id="0e440-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0e440-128">In the request body, supply a JSON representation for the [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="0e440-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0e440-129">The following table shows the properties that are required when you create the [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).</span></span>

|<span data-ttu-id="0e440-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e440-130">Property</span></span>|<span data-ttu-id="0e440-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e440-131">Type</span></span>|<span data-ttu-id="0e440-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e440-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e440-133">id</span><span class="sxs-lookup"><span data-stu-id="0e440-133">id</span></span>|<span data-ttu-id="0e440-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e440-134">String</span></span>|<span data-ttu-id="0e440-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0e440-135">Key of the entity.</span></span> <span data-ttu-id="0e440-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0e440-137">lastModifiedDateTime</span></span>|<span data-ttu-id="0e440-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0e440-138">DateTimeOffset</span></span>|<span data-ttu-id="0e440-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="0e440-139">DateTime the object was last modified.</span></span> <span data-ttu-id="0e440-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="0e440-141">roleScopeTagIds</span></span>|<span data-ttu-id="0e440-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="0e440-142">String collection</span></span>|<span data-ttu-id="0e440-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="0e440-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="0e440-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="0e440-145">supportsScopeTags</span></span>|<span data-ttu-id="0e440-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-146">Boolean</span></span>|<span data-ttu-id="0e440-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="0e440-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="0e440-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="0e440-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="0e440-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="0e440-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="0e440-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0e440-150">This property is read-only.</span></span> <span data-ttu-id="0e440-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0e440-152">createdDateTime</span></span>|<span data-ttu-id="0e440-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0e440-153">DateTimeOffset</span></span>|<span data-ttu-id="0e440-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="0e440-154">DateTime the object was created.</span></span> <span data-ttu-id="0e440-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-156">descripción</span><span class="sxs-lookup"><span data-stu-id="0e440-156">description</span></span>|<span data-ttu-id="0e440-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e440-157">String</span></span>|<span data-ttu-id="0e440-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e440-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="0e440-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-160">displayName</span><span class="sxs-lookup"><span data-stu-id="0e440-160">displayName</span></span>|<span data-ttu-id="0e440-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e440-161">String</span></span>|<span data-ttu-id="0e440-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e440-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="0e440-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-164">version</span><span class="sxs-lookup"><span data-stu-id="0e440-164">version</span></span>|<span data-ttu-id="0e440-165">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-165">Int32</span></span>|<span data-ttu-id="0e440-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e440-166">Version of the device configuration.</span></span> <span data-ttu-id="0e440-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e440-168">accountBlockModification</span><span class="sxs-lookup"><span data-stu-id="0e440-168">accountBlockModification</span></span>|<span data-ttu-id="0e440-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-169">Boolean</span></span>|<span data-ttu-id="0e440-170">Indica si se va a permitir la modificación de cuentas cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-170">Indicates whether or not to allow account modification when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-171">activationLockAllowWhenSupervised</span><span class="sxs-lookup"><span data-stu-id="0e440-171">activationLockAllowWhenSupervised</span></span>|<span data-ttu-id="0e440-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-172">Boolean</span></span>|<span data-ttu-id="0e440-173">Indica si se va a permitir el bloqueo de activación cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-173">Indicates whether or not to allow activation lock when the device is in the supervised mode.</span></span>|
|<span data-ttu-id="0e440-174">airDropBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-174">airDropBlocked</span></span>|<span data-ttu-id="0e440-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-175">Boolean</span></span>|<span data-ttu-id="0e440-176">Indica si se va a permitir AirDrop cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-176">Indicates whether or not to allow AirDrop when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-177">airDropForceUnmanagedDropTarget</span><span class="sxs-lookup"><span data-stu-id="0e440-177">airDropForceUnmanagedDropTarget</span></span>|<span data-ttu-id="0e440-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-178">Boolean</span></span>|<span data-ttu-id="0e440-179">Indica si se va a hacer que AirDrop se considere un destino de colocación no administrado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-179">Indicates whether or not to cause AirDrop to be considered an unmanaged drop target (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-180">airPlayForcePairingPasswordForOutgoingRequests</span><span class="sxs-lookup"><span data-stu-id="0e440-180">airPlayForcePairingPasswordForOutgoingRequests</span></span>|<span data-ttu-id="0e440-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-181">Boolean</span></span>|<span data-ttu-id="0e440-182">Indica si se va a forzar que todos los dispositivos que reciban solicitudes de AirPlay de este dispositivo usen una contraseña de emparejamiento.</span><span class="sxs-lookup"><span data-stu-id="0e440-182">Indicates whether or not to enforce all devices receiving AirPlay requests from this device to use a pairing password.</span></span>|
|<span data-ttu-id="0e440-183">appleWatchBlockPairing</span><span class="sxs-lookup"><span data-stu-id="0e440-183">appleWatchBlockPairing</span></span>|<span data-ttu-id="0e440-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-184">Boolean</span></span>|<span data-ttu-id="0e440-185">Indica si se va a permitir el emparejamiento con Apple Watch cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-185">Indicates whether or not to allow Apple Watch pairing when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-186">appleWatchForceWristDetection</span><span class="sxs-lookup"><span data-stu-id="0e440-186">appleWatchForceWristDetection</span></span>|<span data-ttu-id="0e440-187">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-187">Boolean</span></span>|<span data-ttu-id="0e440-188">Indica si se va a forzar que un Apple Watch emparejado use la detección de muñeca (iOS 8.2 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-188">Indicates whether or not to force a paired Apple Watch to use Wrist Detection (iOS 8.2 and later).</span></span>|
|<span data-ttu-id="0e440-189">appleNewsBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-189">appleNewsBlocked</span></span>|<span data-ttu-id="0e440-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-190">Boolean</span></span>|<span data-ttu-id="0e440-191">Indica si se va a impedir que el usuario use Noticias cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-191">Indicates whether or not to block the user from using News when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-192">appsSingleAppModeList</span><span class="sxs-lookup"><span data-stu-id="0e440-192">appsSingleAppModeList</span></span>|<span data-ttu-id="0e440-193">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-193">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="0e440-194">Obtiene o establece la lista de aplicaciones permitidas de iOS que pueden entrar de forma autónoma en el Modo de aplicación única.</span><span class="sxs-lookup"><span data-stu-id="0e440-194">Gets or sets the list of iOS apps allowed to autonomously enter Single App Mode.</span></span> <span data-ttu-id="0e440-195">Solo bajo supervisión.</span><span class="sxs-lookup"><span data-stu-id="0e440-195">Supervised only.</span></span> <span data-ttu-id="0e440-196">iOS 7.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0e440-196">iOS 7.0 and later.</span></span> <span data-ttu-id="0e440-197">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="0e440-197">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="0e440-198">appsVisibilityList</span><span class="sxs-lookup"><span data-stu-id="0e440-198">appsVisibilityList</span></span>|<span data-ttu-id="0e440-199">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-199">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="0e440-200">Lista de aplicaciones en la lista de visibilidad (sea la lista de aplicaciones visibles o que se pueden iniciar o la lista de aplicaciones ocultas o que no se pueden iniciar, controlada por AppsVisibilityListType) (iOS 9.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-200">List of apps in the visibility list (either visible/launchable apps list or hidden/unlaunchable apps list, controlled by AppsVisibilityListType) (iOS 9.3 and later).</span></span> <span data-ttu-id="0e440-201">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="0e440-201">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="0e440-202">appsVisibilityListType</span><span class="sxs-lookup"><span data-stu-id="0e440-202">appsVisibilityListType</span></span>|[<span data-ttu-id="0e440-203">appListType</span><span class="sxs-lookup"><span data-stu-id="0e440-203">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="0e440-204">Tipo de lista que se encuentra en la AppsVisibilityList.</span><span class="sxs-lookup"><span data-stu-id="0e440-204">Type of list that is in the AppsVisibilityList.</span></span> <span data-ttu-id="0e440-205">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="0e440-205">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="0e440-206">appStoreBlockAutomaticDownloads</span><span class="sxs-lookup"><span data-stu-id="0e440-206">appStoreBlockAutomaticDownloads</span></span>|<span data-ttu-id="0e440-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-207">Boolean</span></span>|<span data-ttu-id="0e440-208">Indica si se va a bloquear la descarga automática de aplicaciones compradas en otros dispositivos cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-208">Indicates whether or not to block the automatic downloading of apps purchased on other devices when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-209">appStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-209">appStoreBlocked</span></span>|<span data-ttu-id="0e440-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-210">Boolean</span></span>|<span data-ttu-id="0e440-211">Indica si se va a impedir que el usuario use el App Store.</span><span class="sxs-lookup"><span data-stu-id="0e440-211">Indicates whether or not to block the user from using the App Store.</span></span>|
|<span data-ttu-id="0e440-212">appStoreBlockInAppPurchases</span><span class="sxs-lookup"><span data-stu-id="0e440-212">appStoreBlockInAppPurchases</span></span>|<span data-ttu-id="0e440-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-213">Boolean</span></span>|<span data-ttu-id="0e440-214">Indica si se va a impedir que el usuario haga compras en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e440-214">Indicates whether or not to block the user from making in app purchases.</span></span>|
|<span data-ttu-id="0e440-215">appStoreBlockUIAppInstallation</span><span class="sxs-lookup"><span data-stu-id="0e440-215">appStoreBlockUIAppInstallation</span></span>|<span data-ttu-id="0e440-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-216">Boolean</span></span>|<span data-ttu-id="0e440-217">Indica si se va a bloquear la aplicación App Store, sin restringir la instalación mediante aplicaciones host.</span><span class="sxs-lookup"><span data-stu-id="0e440-217">Indicates whether or not to block the App Store app, not restricting installation through Host apps.</span></span> <span data-ttu-id="0e440-218">Se aplica solo al modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-218">Applies to supervised mode only (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-219">appStoreRequirePassword</span><span class="sxs-lookup"><span data-stu-id="0e440-219">appStoreRequirePassword</span></span>|<span data-ttu-id="0e440-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-220">Boolean</span></span>|<span data-ttu-id="0e440-221">Indica si se va a requerir una contraseña cuando se use la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0e440-221">Indicates whether or not to require a password when using the app store.</span></span>|
|<span data-ttu-id="0e440-222">bluetoothBlockModification</span><span class="sxs-lookup"><span data-stu-id="0e440-222">bluetoothBlockModification</span></span>|<span data-ttu-id="0e440-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-223">Boolean</span></span>|<span data-ttu-id="0e440-224">Indica si se va a permitir la modificación de la configuración Bluetooth cuando el dispositivo está en modo supervisado (iOS 10.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-224">Indicates whether or not to allow modification of Bluetooth settings when the device is in supervised mode (iOS 10.0 and later).</span></span>|
|<span data-ttu-id="0e440-225">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-225">cameraBlocked</span></span>|<span data-ttu-id="0e440-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-226">Boolean</span></span>|<span data-ttu-id="0e440-227">Indica si se va a impedir que el usuario obtenga acceso a la cámara del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e440-227">Indicates whether or not to block the user from accessing the camera of the device.</span></span>|
|<span data-ttu-id="0e440-228">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="0e440-228">cellularBlockDataRoaming</span></span>|<span data-ttu-id="0e440-229">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-229">Boolean</span></span>|<span data-ttu-id="0e440-230">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="0e440-230">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="0e440-231">cellularBlockGlobalBackgroundFetchWhileRoaming</span><span class="sxs-lookup"><span data-stu-id="0e440-231">cellularBlockGlobalBackgroundFetchWhileRoaming</span></span>|<span data-ttu-id="0e440-232">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-232">Boolean</span></span>|<span data-ttu-id="0e440-233">Indica si se va a impedir la captura de fondo global mientras se está en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="0e440-233">Indicates whether or not to block global background fetch while roaming.</span></span>|
|<span data-ttu-id="0e440-234">cellularBlockPerAppDataModification</span><span class="sxs-lookup"><span data-stu-id="0e440-234">cellularBlockPerAppDataModification</span></span>|<span data-ttu-id="0e440-235">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-235">Boolean</span></span>|<span data-ttu-id="0e440-236">Indica si se van a permitir los cambios en la configuración de uso de datos de aplicaciones de telefonía móvil cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-236">Indicates whether or not to allow changes to cellular app data usage settings when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-237">cellularBlockPersonalHotspot</span><span class="sxs-lookup"><span data-stu-id="0e440-237">cellularBlockPersonalHotspot</span></span>|<span data-ttu-id="0e440-238">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-238">Boolean</span></span>|<span data-ttu-id="0e440-239">Indica si se va a bloquear el punto de acceso personal.</span><span class="sxs-lookup"><span data-stu-id="0e440-239">Indicates whether or not to block Personal Hotspot.</span></span>|
|<span data-ttu-id="0e440-240">cellularBlockVoiceRoaming</span><span class="sxs-lookup"><span data-stu-id="0e440-240">cellularBlockVoiceRoaming</span></span>|<span data-ttu-id="0e440-241">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-241">Boolean</span></span>|<span data-ttu-id="0e440-242">Indica si se va a bloquear la itinerancia de voz.</span><span class="sxs-lookup"><span data-stu-id="0e440-242">Indicates whether or not to block voice roaming.</span></span>|
|<span data-ttu-id="0e440-243">certificatesBlockUntrustedTlsCertificates</span><span class="sxs-lookup"><span data-stu-id="0e440-243">certificatesBlockUntrustedTlsCertificates</span></span>|<span data-ttu-id="0e440-244">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-244">Boolean</span></span>|<span data-ttu-id="0e440-245">Indica si se van a bloquear los certificados TLS que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="0e440-245">Indicates whether or not to block untrusted TLS certificates.</span></span>|
|<span data-ttu-id="0e440-246">classroomAppBlockRemoteScreenObservation</span><span class="sxs-lookup"><span data-stu-id="0e440-246">classroomAppBlockRemoteScreenObservation</span></span>|<span data-ttu-id="0e440-247">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-247">Boolean</span></span>|<span data-ttu-id="0e440-248">Indica si se va a permitir la observación de pantalla remota de la aplicación Classroom cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-248">Indicates whether or not to allow remote screen observation by Classroom app when the device is in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="0e440-249">classroomAppForceUnpromptedScreenObservation</span><span class="sxs-lookup"><span data-stu-id="0e440-249">classroomAppForceUnpromptedScreenObservation</span></span>|<span data-ttu-id="0e440-250">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-250">Boolean</span></span>|<span data-ttu-id="0e440-251">Indica si se va a autorizar de forma automática al profesor de un curso administrado en la aplicación Classroom para que vea la pantalla de un alumno sin preguntarle cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-251">Indicates whether or not to automatically give permission to the teacher of a managed course on the Classroom app to view a student's screen without prompting when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-252">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="0e440-252">compliantAppsList</span></span>|<span data-ttu-id="0e440-253">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-253">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="0e440-254">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="0e440-254">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="0e440-255">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="0e440-255">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="0e440-256">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="0e440-256">compliantAppListType</span></span>|[<span data-ttu-id="0e440-257">appListType</span><span class="sxs-lookup"><span data-stu-id="0e440-257">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="0e440-258">Lista que se encuentra en la AppComplianceList.</span><span class="sxs-lookup"><span data-stu-id="0e440-258">List that is in the AppComplianceList.</span></span> <span data-ttu-id="0e440-259">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="0e440-259">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="0e440-260">configurationProfileBlockChanges</span><span class="sxs-lookup"><span data-stu-id="0e440-260">configurationProfileBlockChanges</span></span>|<span data-ttu-id="0e440-261">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-261">Boolean</span></span>|<span data-ttu-id="0e440-262">Indica si se va a impedir que el usuario instale perfiles de configuración y certificados de forma interactiva cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-262">Indicates whether or not to block the user from installing configuration profiles and certificates interactively when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-263">definitionLookupBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-263">definitionLookupBlocked</span></span>|<span data-ttu-id="0e440-264">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-264">Boolean</span></span>|<span data-ttu-id="0e440-265">Indica si se va a bloquear la búsqueda de definiciones cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-265">Indicates whether or not to block definition lookup when the device is in supervised mode (iOS 8.1.3 and later ).</span></span>|
|<span data-ttu-id="0e440-266">deviceBlockEnableRestrictions</span><span class="sxs-lookup"><span data-stu-id="0e440-266">deviceBlockEnableRestrictions</span></span>|<span data-ttu-id="0e440-267">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-267">Boolean</span></span>|<span data-ttu-id="0e440-268">Indica si se va a permitir que el usuario active las restricciones en los ajustes del dispositivo cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-268">Indicates whether or not to allow the user to enables restrictions in the device settings when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-269">deviceBlockEraseContentAndSettings</span><span class="sxs-lookup"><span data-stu-id="0e440-269">deviceBlockEraseContentAndSettings</span></span>|<span data-ttu-id="0e440-270">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-270">Boolean</span></span>|<span data-ttu-id="0e440-271">Indica si se va a permitir el uso de la opción "Borrar todo el contenido y la configuración" en el dispositivo cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-271">Indicates whether or not to allow the use of the 'Erase all content and settings' option on the device when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-272">deviceBlockNameModification</span><span class="sxs-lookup"><span data-stu-id="0e440-272">deviceBlockNameModification</span></span>|<span data-ttu-id="0e440-273">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-273">Boolean</span></span>|<span data-ttu-id="0e440-274">Indica si se va a permitir modificar el nombre del dispositivo cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-274">Indicates whether or not to allow device name modification when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-275">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="0e440-275">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="0e440-276">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-276">Boolean</span></span>|<span data-ttu-id="0e440-277">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0e440-277">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="0e440-278">diagnosticDataBlockSubmissionModification</span><span class="sxs-lookup"><span data-stu-id="0e440-278">diagnosticDataBlockSubmissionModification</span></span>|<span data-ttu-id="0e440-279">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-279">Boolean</span></span>|<span data-ttu-id="0e440-280">Indica si se va a permitir modificar los ajustes del envío de diagnósticos cuando el dispositivo está en modo supervisado (iOS 9.3.2 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-280">Indicates whether or not to allow diagnostics submission settings modification when the device is in supervised mode (iOS 9.3.2 and later).</span></span>|
|<span data-ttu-id="0e440-281">documentsBlockManagedDocumentsInUnmanagedApps</span><span class="sxs-lookup"><span data-stu-id="0e440-281">documentsBlockManagedDocumentsInUnmanagedApps</span></span>|<span data-ttu-id="0e440-282">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-282">Boolean</span></span>|<span data-ttu-id="0e440-283">Indica si se va a impedir que el usuario visualice documentos administrados en las aplicaciones no administradas.</span><span class="sxs-lookup"><span data-stu-id="0e440-283">Indicates whether or not to block the user from viewing managed documents in unmanaged apps.</span></span>|
|<span data-ttu-id="0e440-284">documentsBlockUnmanagedDocumentsInManagedApps</span><span class="sxs-lookup"><span data-stu-id="0e440-284">documentsBlockUnmanagedDocumentsInManagedApps</span></span>|<span data-ttu-id="0e440-285">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-285">Boolean</span></span>|<span data-ttu-id="0e440-286">Indica si se va a impedir que el usuario visualice documentos no administrados en las aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="0e440-286">Indicates whether or not to block the user from viewing unmanaged documents in managed apps.</span></span>|
|<span data-ttu-id="0e440-287">emailInDomainSuffixes</span><span class="sxs-lookup"><span data-stu-id="0e440-287">emailInDomainSuffixes</span></span>|<span data-ttu-id="0e440-288">Colección String</span><span class="sxs-lookup"><span data-stu-id="0e440-288">String collection</span></span>|<span data-ttu-id="0e440-289">Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.</span><span class="sxs-lookup"><span data-stu-id="0e440-289">An email address lacking a suffix that matches any of these strings will be considered out-of-domain.</span></span>|
|<span data-ttu-id="0e440-290">enterpriseAppBlockTrust</span><span class="sxs-lookup"><span data-stu-id="0e440-290">enterpriseAppBlockTrust</span></span>|<span data-ttu-id="0e440-291">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-291">Boolean</span></span>|<span data-ttu-id="0e440-292">Indica si se va a impedir que el usuario confíe en una aplicación empresarial.</span><span class="sxs-lookup"><span data-stu-id="0e440-292">Indicates whether or not to block the user from trusting an enterprise app.</span></span>|
|<span data-ttu-id="0e440-293">enterpriseAppBlockTrustModification</span><span class="sxs-lookup"><span data-stu-id="0e440-293">enterpriseAppBlockTrustModification</span></span>|<span data-ttu-id="0e440-294">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-294">Boolean</span></span>|<span data-ttu-id="0e440-295">Indica si se va a impedir que el usuario modifique la configuración de confianza de una aplicación empresarial.</span><span class="sxs-lookup"><span data-stu-id="0e440-295">Indicates whether or not to block the user from modifying the enterprise app trust settings.</span></span>|
|<span data-ttu-id="0e440-296">faceTimeBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-296">faceTimeBlocked</span></span>|<span data-ttu-id="0e440-297">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-297">Boolean</span></span>|<span data-ttu-id="0e440-298">Indica si se va a impedir que el usuario use FaceTime.</span><span class="sxs-lookup"><span data-stu-id="0e440-298">Indicates whether or not to block the user from using FaceTime.</span></span>|
|<span data-ttu-id="0e440-299">findMyFriendsBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-299">findMyFriendsBlocked</span></span>|<span data-ttu-id="0e440-300">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-300">Boolean</span></span>|<span data-ttu-id="0e440-301">Indica si se va a bloquear Buscar a mis amigos cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-301">Indicates whether or not to block Find My Friends when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-302">gamingBlockGameCenterFriends</span><span class="sxs-lookup"><span data-stu-id="0e440-302">gamingBlockGameCenterFriends</span></span>|<span data-ttu-id="0e440-303">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-303">Boolean</span></span>|<span data-ttu-id="0e440-304">Indica si se va a impedir que el usuario tenga amigos en el Game Center.</span><span class="sxs-lookup"><span data-stu-id="0e440-304">Indicates whether or not to block the user from having friends in Game Center.</span></span>|
|<span data-ttu-id="0e440-305">gamingBlockMultiplayer</span><span class="sxs-lookup"><span data-stu-id="0e440-305">gamingBlockMultiplayer</span></span>|<span data-ttu-id="0e440-306">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-306">Boolean</span></span>|<span data-ttu-id="0e440-307">Indica si se va a impedir que el usuario use los juegos multijugador.</span><span class="sxs-lookup"><span data-stu-id="0e440-307">Indicates whether or not to block the user from using multiplayer gaming.</span></span>|
|<span data-ttu-id="0e440-308">gameCenterBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-308">gameCenterBlocked</span></span>|<span data-ttu-id="0e440-309">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-309">Boolean</span></span>|<span data-ttu-id="0e440-310">Indica si se va a impedir que el usuario use el Game Center cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-310">Indicates whether or not to block the user from using Game Center when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-311">hostPairingBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-311">hostPairingBlocked</span></span>|<span data-ttu-id="0e440-312">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-312">Boolean</span></span>|<span data-ttu-id="0e440-313">Indica si se va a permitir el emparejamiento de host para controlar los dispositivos con los que se puede emparejar un dispositivo iOS cuando el dispositivo iOS está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-313">indicates whether or not to allow host pairing to control the devices an iOS device can pair with when the iOS device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-314">iBooksStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-314">iBooksStoreBlocked</span></span>|<span data-ttu-id="0e440-315">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-315">Boolean</span></span>|<span data-ttu-id="0e440-316">Indica si se va a impedir que el usuario use iBooks Store cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-316">Indicates whether or not to block the user from using the iBooks Store when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-317">iBooksStoreBlockErotica</span><span class="sxs-lookup"><span data-stu-id="0e440-317">iBooksStoreBlockErotica</span></span>|<span data-ttu-id="0e440-318">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-318">Boolean</span></span>|<span data-ttu-id="0e440-319">Indica si se va a impedir que el usuario descargue archivos multimedia desde el iBook Store que se han etiquetado como eróticos.</span><span class="sxs-lookup"><span data-stu-id="0e440-319">Indicates whether or not to block the user from downloading media from the iBookstore that has been tagged as erotica.</span></span>|
|<span data-ttu-id="0e440-320">iCloudBlockActivityContinuation</span><span class="sxs-lookup"><span data-stu-id="0e440-320">iCloudBlockActivityContinuation</span></span>|<span data-ttu-id="0e440-321">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-321">Boolean</span></span>|<span data-ttu-id="0e440-322">Indica si se va a impedir que el usuario continúe con el trabajo que empezó en el dispositivo iOS en otro dispositivo macOS o iOS.</span><span class="sxs-lookup"><span data-stu-id="0e440-322">Indicates whether or not to block  the the user from continuing work they started on iOS device to another iOS or macOS device.</span></span>|
|<span data-ttu-id="0e440-323">iCloudBlockBackup</span><span class="sxs-lookup"><span data-stu-id="0e440-323">iCloudBlockBackup</span></span>|<span data-ttu-id="0e440-324">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-324">Boolean</span></span>|<span data-ttu-id="0e440-325">Indica si se va a impedir la copia de seguridad de iCloud.</span><span class="sxs-lookup"><span data-stu-id="0e440-325">Indicates whether or not to block iCloud backup.</span></span>|
|<span data-ttu-id="0e440-326">iCloudBlockDocumentSync</span><span class="sxs-lookup"><span data-stu-id="0e440-326">iCloudBlockDocumentSync</span></span>|<span data-ttu-id="0e440-327">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-327">Boolean</span></span>|<span data-ttu-id="0e440-328">Indica si se va a impedir la sincronización de documentos de iCloud.</span><span class="sxs-lookup"><span data-stu-id="0e440-328">Indicates whether or not to block iCloud document sync.</span></span>|
|<span data-ttu-id="0e440-329">iCloudBlockManagedAppsSync</span><span class="sxs-lookup"><span data-stu-id="0e440-329">iCloudBlockManagedAppsSync</span></span>|<span data-ttu-id="0e440-330">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-330">Boolean</span></span>|<span data-ttu-id="0e440-331">Indica si se va a impedir la sincronización en la nube de aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="0e440-331">Indicates whether or not to block Managed Apps Cloud Sync.</span></span>|
|<span data-ttu-id="0e440-332">iCloudBlockPhotoLibrary</span><span class="sxs-lookup"><span data-stu-id="0e440-332">iCloudBlockPhotoLibrary</span></span>|<span data-ttu-id="0e440-333">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-333">Boolean</span></span>|<span data-ttu-id="0e440-334">Indica si se va a bloquear la Fototeca de iCloud.</span><span class="sxs-lookup"><span data-stu-id="0e440-334">Indicates whether or not to block iCloud Photo Library.</span></span>|
|<span data-ttu-id="0e440-335">iCloudBlockPhotoStreamSync</span><span class="sxs-lookup"><span data-stu-id="0e440-335">iCloudBlockPhotoStreamSync</span></span>|<span data-ttu-id="0e440-336">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-336">Boolean</span></span>|<span data-ttu-id="0e440-337">Indica si se va a bloquear la sincronización de fotos en streaming de iCloud.</span><span class="sxs-lookup"><span data-stu-id="0e440-337">Indicates whether or not to block iCloud Photo Stream Sync.</span></span>|
|<span data-ttu-id="0e440-338">iCloudBlockSharedPhotoStream</span><span class="sxs-lookup"><span data-stu-id="0e440-338">iCloudBlockSharedPhotoStream</span></span>|<span data-ttu-id="0e440-339">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-339">Boolean</span></span>|<span data-ttu-id="0e440-340">Indica si se va a bloquear la sincronización de fotos en streaming compartidas.</span><span class="sxs-lookup"><span data-stu-id="0e440-340">Indicates whether or not to block Shared Photo Stream.</span></span>|
|<span data-ttu-id="0e440-341">iCloudRequireEncryptedBackup</span><span class="sxs-lookup"><span data-stu-id="0e440-341">iCloudRequireEncryptedBackup</span></span>|<span data-ttu-id="0e440-342">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-342">Boolean</span></span>|<span data-ttu-id="0e440-343">Indica si se va a requerir que las copias de seguridad de iCloud estén cifradas.</span><span class="sxs-lookup"><span data-stu-id="0e440-343">Indicates whether or not to require backups to iCloud be encrypted.</span></span>|
|<span data-ttu-id="0e440-344">iTunesBlockExplicitContent</span><span class="sxs-lookup"><span data-stu-id="0e440-344">iTunesBlockExplicitContent</span></span>|<span data-ttu-id="0e440-345">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-345">Boolean</span></span>|<span data-ttu-id="0e440-346">Indica si se va a impedir que el usuario obtenga acceso a contenido explícito en iTunes y el App Store.</span><span class="sxs-lookup"><span data-stu-id="0e440-346">Indicates whether or not to block the user from accessing explicit content in iTunes and the App Store.</span></span>|
|<span data-ttu-id="0e440-347">iTunesBlockMusicService</span><span class="sxs-lookup"><span data-stu-id="0e440-347">iTunesBlockMusicService</span></span>|<span data-ttu-id="0e440-348">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-348">Boolean</span></span>|<span data-ttu-id="0e440-349">Indica si se va a bloquear el servicio Música y revertir la aplicación Música al modo clásico cuando el dispositivo está en modo supervisado (iOS 9.3 y versiones posteriores, y macOS 10.12 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-349">Indicates whether or not to block Music service and revert Music app to classic mode when the device is in supervised mode (iOS 9.3 and later and macOS 10.12 and later).</span></span>|
|<span data-ttu-id="0e440-350">iTunesBlockRadio</span><span class="sxs-lookup"><span data-stu-id="0e440-350">iTunesBlockRadio</span></span>|<span data-ttu-id="0e440-351">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-351">Boolean</span></span>|<span data-ttu-id="0e440-352">Indica si se va a impedir que el usuario use iTunes Radio cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-352">Indicates whether or not to block the user from using iTunes Radio when the device is in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="0e440-353">keyboardBlockAutoCorrect</span><span class="sxs-lookup"><span data-stu-id="0e440-353">keyboardBlockAutoCorrect</span></span>|<span data-ttu-id="0e440-354">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-354">Boolean</span></span>|<span data-ttu-id="0e440-355">Indica si se va a bloquear el autocorrector cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-355">Indicates whether or not to block keyboard auto-correction when the device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="0e440-356">keyboardBlockDictation</span><span class="sxs-lookup"><span data-stu-id="0e440-356">keyboardBlockDictation</span></span>|<span data-ttu-id="0e440-357">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-357">Boolean</span></span>|<span data-ttu-id="0e440-358">Indica si se va a impedir que el usuario use la entrada dictada cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-358">Indicates whether or not to block the user from using dictation input when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-359">keyboardBlockPredictive</span><span class="sxs-lookup"><span data-stu-id="0e440-359">keyboardBlockPredictive</span></span>|<span data-ttu-id="0e440-360">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-360">Boolean</span></span>|<span data-ttu-id="0e440-361">Indica si se van a bloquear los teclados predictivos cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-361">Indicates whether or not to block predictive keyboards when device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="0e440-362">keyboardBlockShortcuts</span><span class="sxs-lookup"><span data-stu-id="0e440-362">keyboardBlockShortcuts</span></span>|<span data-ttu-id="0e440-363">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-363">Boolean</span></span>|<span data-ttu-id="0e440-364">Indica si se van a bloquear los atajos del teclado cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-364">Indicates whether or not to block keyboard shortcuts when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-365">keyboardBlockSpellCheck</span><span class="sxs-lookup"><span data-stu-id="0e440-365">keyboardBlockSpellCheck</span></span>|<span data-ttu-id="0e440-366">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-366">Boolean</span></span>|<span data-ttu-id="0e440-367">Indica si se va a bloquear la revisión ortográfica cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-367">Indicates whether or not to block keyboard spell-checking when the device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="0e440-368">kioskModeAllowAssistiveSpeak</span><span class="sxs-lookup"><span data-stu-id="0e440-368">kioskModeAllowAssistiveSpeak</span></span>|<span data-ttu-id="0e440-369">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-369">Boolean</span></span>|<span data-ttu-id="0e440-370">Indica si se va a permitir la lectura de asistencia en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-370">Indicates whether or not to allow assistive speak while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-371">kioskModeAllowAssistiveTouchSettings</span><span class="sxs-lookup"><span data-stu-id="0e440-371">kioskModeAllowAssistiveTouchSettings</span></span>|<span data-ttu-id="0e440-372">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-372">Boolean</span></span>|<span data-ttu-id="0e440-373">Indica si se va a permitir el acceso a la configuración de AssistiveTouch en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-373">Indicates whether or not to allow access to the Assistive Touch Settings while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-374">kioskModeAllowAutoLock</span><span class="sxs-lookup"><span data-stu-id="0e440-374">kioskModeAllowAutoLock</span></span>|<span data-ttu-id="0e440-375">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-375">Boolean</span></span>|<span data-ttu-id="0e440-376">Indica si se va a permitir el bloqueo automático del dispositivo en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-376">Indicates whether or not to allow device auto lock while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-377">kioskModeAllowColorInversionSettings</span><span class="sxs-lookup"><span data-stu-id="0e440-377">kioskModeAllowColorInversionSettings</span></span>|<span data-ttu-id="0e440-378">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-378">Boolean</span></span>|<span data-ttu-id="0e440-379">Indica si se va a permitir el acceso a la configuración de la inversión del color en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-379">Indicates whether or not to allow access to the Color Inversion Settings while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-380">kioskModeAllowRingerSwitch</span><span class="sxs-lookup"><span data-stu-id="0e440-380">kioskModeAllowRingerSwitch</span></span>|<span data-ttu-id="0e440-381">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-381">Boolean</span></span>|<span data-ttu-id="0e440-382">Indica si se va a permitir el uso del cambio de tono en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-382">Indicates whether or not to allow use of the ringer switch while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-383">kioskModeAllowScreenRotation</span><span class="sxs-lookup"><span data-stu-id="0e440-383">kioskModeAllowScreenRotation</span></span>|<span data-ttu-id="0e440-384">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-384">Boolean</span></span>|<span data-ttu-id="0e440-385">Indica si se va a permitir la rotación de pantalla en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-385">Indicates whether or not to allow screen rotation while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-386">kioskModeAllowSleepButton</span><span class="sxs-lookup"><span data-stu-id="0e440-386">kioskModeAllowSleepButton</span></span>|<span data-ttu-id="0e440-387">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-387">Boolean</span></span>|<span data-ttu-id="0e440-388">Indica si se va a permitir el uso del botón de suspensión en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-388">Indicates whether or not to allow use of the sleep button while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-389">kioskModeAllowTouchscreen</span><span class="sxs-lookup"><span data-stu-id="0e440-389">kioskModeAllowTouchscreen</span></span>|<span data-ttu-id="0e440-390">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-390">Boolean</span></span>|<span data-ttu-id="0e440-391">Indica si se va a permitir el uso de la pantalla táctil en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-391">Indicates whether or not to allow use of the touchscreen while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-392">kioskModeAllowVoiceOverSettings</span><span class="sxs-lookup"><span data-stu-id="0e440-392">kioskModeAllowVoiceOverSettings</span></span>|<span data-ttu-id="0e440-393">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-393">Boolean</span></span>|<span data-ttu-id="0e440-394">Indica si se va a permitir el acceso a la configuración de voz en off en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-394">Indicates whether or not to allow access to the voice over settings while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-395">kioskModeAllowVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="0e440-395">kioskModeAllowVolumeButtons</span></span>|<span data-ttu-id="0e440-396">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-396">Boolean</span></span>|<span data-ttu-id="0e440-397">Indica si se va a permitir el uso de los botones de volumen en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-397">Indicates whether or not to allow use of the volume buttons while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-398">kioskModeBlockVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="0e440-398">kioskModeBlockVolumeButtons</span></span>|<span data-ttu-id="0e440-399">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-399">Boolean</span></span>|<span data-ttu-id="0e440-400">Indica si se van a bloquear los botones de volumen durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-400">Indicates whether or not to block the volume buttons while in Kiosk Mode.</span></span>|
|<span data-ttu-id="0e440-401">kioskModeAllowZoomSettings</span><span class="sxs-lookup"><span data-stu-id="0e440-401">kioskModeAllowZoomSettings</span></span>|<span data-ttu-id="0e440-402">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-402">Boolean</span></span>|<span data-ttu-id="0e440-403">Indica si se va a permitir el acceso a la configuración de zoom en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-403">Indicates whether or not to allow access to the zoom settings while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-404">kioskModeAppStoreUrl</span><span class="sxs-lookup"><span data-stu-id="0e440-404">kioskModeAppStoreUrl</span></span>|<span data-ttu-id="0e440-405">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e440-405">String</span></span>|<span data-ttu-id="0e440-406">Dirección URL en la tienda de aplicaciones a la aplicación que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-406">URL in the app store to the app to use for kiosk mode.</span></span> <span data-ttu-id="0e440-407">Úsela si KioskModeManagedAppId es desconocido.</span><span class="sxs-lookup"><span data-stu-id="0e440-407">Use if KioskModeManagedAppId is not known.</span></span>|
|<span data-ttu-id="0e440-408">kioskModeBuiltInAppId</span><span class="sxs-lookup"><span data-stu-id="0e440-408">kioskModeBuiltInAppId</span></span>|<span data-ttu-id="0e440-409">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e440-409">String</span></span>|<span data-ttu-id="0e440-410">Identificador de aplicaciones integradas que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-410">ID for built-in apps to use for kiosk mode.</span></span> <span data-ttu-id="0e440-411">Se usa cuando no se establecen KioskModeManagedAppId y KioskModeAppStoreUrl.</span><span class="sxs-lookup"><span data-stu-id="0e440-411">Used when KioskModeManagedAppId and KioskModeAppStoreUrl are not set.</span></span>|
|<span data-ttu-id="0e440-412">kioskModeRequireAssistiveTouch</span><span class="sxs-lookup"><span data-stu-id="0e440-412">kioskModeRequireAssistiveTouch</span></span>|<span data-ttu-id="0e440-413">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-413">Boolean</span></span>|<span data-ttu-id="0e440-414">Indica si se va a requerir la AssistiveTouch en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-414">Indicates whether or not to require assistive touch while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-415">kioskModeRequireColorInversion</span><span class="sxs-lookup"><span data-stu-id="0e440-415">kioskModeRequireColorInversion</span></span>|<span data-ttu-id="0e440-416">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-416">Boolean</span></span>|<span data-ttu-id="0e440-417">Indica si se va a requerir la inversión de color en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-417">Indicates whether or not to require color inversion while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-418">kioskModeRequireMonoAudio</span><span class="sxs-lookup"><span data-stu-id="0e440-418">kioskModeRequireMonoAudio</span></span>|<span data-ttu-id="0e440-419">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-419">Boolean</span></span>|<span data-ttu-id="0e440-420">Indica si se va a requerir el audio mono en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-420">Indicates whether or not to require mono audio while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-421">kioskModeRequireVoiceOver</span><span class="sxs-lookup"><span data-stu-id="0e440-421">kioskModeRequireVoiceOver</span></span>|<span data-ttu-id="0e440-422">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-422">Boolean</span></span>|<span data-ttu-id="0e440-423">Indica si se va a requerir la voz en off en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-423">Indicates whether or not to require voice over while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-424">kioskModeRequireZoom</span><span class="sxs-lookup"><span data-stu-id="0e440-424">kioskModeRequireZoom</span></span>|<span data-ttu-id="0e440-425">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-425">Boolean</span></span>|<span data-ttu-id="0e440-426">Indica si se va a requerir el zoom en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-426">Indicates whether or not to require zoom while in kiosk mode.</span></span>|
|<span data-ttu-id="0e440-427">kioskModeManagedAppId</span><span class="sxs-lookup"><span data-stu-id="0e440-427">kioskModeManagedAppId</span></span>|<span data-ttu-id="0e440-428">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e440-428">String</span></span>|<span data-ttu-id="0e440-429">identificador de la aplicación administrada de la aplicación que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e440-429">Managed app id of the app to use for kiosk mode.</span></span> <span data-ttu-id="0e440-430">Si se especifica KioskModeManagedAppId, entonces se omitirá KioskModeAppStoreUrl.</span><span class="sxs-lookup"><span data-stu-id="0e440-430">If KioskModeManagedAppId is specified then KioskModeAppStoreUrl will be ignored.</span></span>|
|<span data-ttu-id="0e440-431">lockScreenBlockControlCenter</span><span class="sxs-lookup"><span data-stu-id="0e440-431">lockScreenBlockControlCenter</span></span>|<span data-ttu-id="0e440-432">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-432">Boolean</span></span>|<span data-ttu-id="0e440-433">Indica si se va a impedir que el usuario use el centro de control en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0e440-433">Indicates whether or not to block the user from using control center on the lock screen.</span></span>|
|<span data-ttu-id="0e440-434">lockScreenBlockNotificationView</span><span class="sxs-lookup"><span data-stu-id="0e440-434">lockScreenBlockNotificationView</span></span>|<span data-ttu-id="0e440-435">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-435">Boolean</span></span>|<span data-ttu-id="0e440-436">Indica si se va a impedir que el usuario use la visualización de notificaciones en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0e440-436">Indicates whether or not to block the user from using the notification view on the lock screen.</span></span>|
|<span data-ttu-id="0e440-437">lockScreenBlockPassbook</span><span class="sxs-lookup"><span data-stu-id="0e440-437">lockScreenBlockPassbook</span></span>|<span data-ttu-id="0e440-438">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-438">Boolean</span></span>|<span data-ttu-id="0e440-439">Indica si se va a impedir que el usuario use Passbook cuando el dispositivo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0e440-439">Indicates whether or not to block the user from using passbook when the device is locked.</span></span>|
|<span data-ttu-id="0e440-440">lockScreenBlockTodayView</span><span class="sxs-lookup"><span data-stu-id="0e440-440">lockScreenBlockTodayView</span></span>|<span data-ttu-id="0e440-441">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-441">Boolean</span></span>|<span data-ttu-id="0e440-442">Indica si se va a impedir que el usuario use la vista Hoy en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0e440-442">Indicates whether or not to block the user from using the Today View on the lock screen.</span></span>|
|<span data-ttu-id="0e440-443">mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="0e440-443">mediaContentRatingAustralia</span></span>|[<span data-ttu-id="0e440-444">mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="0e440-444">mediaContentRatingAustralia</span></span>](../resources/intune-deviceconfig-mediacontentratingaustralia.md)|<span data-ttu-id="0e440-445">Clasificación de contenido multimedia para Australia</span><span class="sxs-lookup"><span data-stu-id="0e440-445">Media content rating settings for Australia</span></span>|
|<span data-ttu-id="0e440-446">mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="0e440-446">mediaContentRatingCanada</span></span>|[<span data-ttu-id="0e440-447">mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="0e440-447">mediaContentRatingCanada</span></span>](../resources/intune-deviceconfig-mediacontentratingcanada.md)|<span data-ttu-id="0e440-448">Clasificación de contenido multimedia para Canadá</span><span class="sxs-lookup"><span data-stu-id="0e440-448">Media content rating settings for Canada</span></span>|
|<span data-ttu-id="0e440-449">mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="0e440-449">mediaContentRatingFrance</span></span>|[<span data-ttu-id="0e440-450">mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="0e440-450">mediaContentRatingFrance</span></span>](../resources/intune-deviceconfig-mediacontentratingfrance.md)|<span data-ttu-id="0e440-451">Clasificación de contenido multimedia para Francia</span><span class="sxs-lookup"><span data-stu-id="0e440-451">Media content rating settings for France</span></span>|
|<span data-ttu-id="0e440-452">mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="0e440-452">mediaContentRatingGermany</span></span>|[<span data-ttu-id="0e440-453">mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="0e440-453">mediaContentRatingGermany</span></span>](../resources/intune-deviceconfig-mediacontentratinggermany.md)|<span data-ttu-id="0e440-454">Clasificación de contenido multimedia para Alemania</span><span class="sxs-lookup"><span data-stu-id="0e440-454">Media content rating settings for Germany</span></span>|
|<span data-ttu-id="0e440-455">mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="0e440-455">mediaContentRatingIreland</span></span>|[<span data-ttu-id="0e440-456">mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="0e440-456">mediaContentRatingIreland</span></span>](../resources/intune-deviceconfig-mediacontentratingireland.md)|<span data-ttu-id="0e440-457">Clasificación de contenido multimedia para Irlanda</span><span class="sxs-lookup"><span data-stu-id="0e440-457">Media content rating settings for Ireland</span></span>|
|<span data-ttu-id="0e440-458">mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="0e440-458">mediaContentRatingJapan</span></span>|[<span data-ttu-id="0e440-459">mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="0e440-459">mediaContentRatingJapan</span></span>](../resources/intune-deviceconfig-mediacontentratingjapan.md)|<span data-ttu-id="0e440-460">Clasificación de contenido multimedia para Japón</span><span class="sxs-lookup"><span data-stu-id="0e440-460">Media content rating settings for Japan</span></span>|
|<span data-ttu-id="0e440-461">mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="0e440-461">mediaContentRatingNewZealand</span></span>|[<span data-ttu-id="0e440-462">mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="0e440-462">mediaContentRatingNewZealand</span></span>](../resources/intune-deviceconfig-mediacontentratingnewzealand.md)|<span data-ttu-id="0e440-463">Clasificación de contenido multimedia para Nueva Zelanda</span><span class="sxs-lookup"><span data-stu-id="0e440-463">Media content rating settings for New Zealand</span></span>|
|<span data-ttu-id="0e440-464">mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="0e440-464">mediaContentRatingUnitedKingdom</span></span>|[<span data-ttu-id="0e440-465">mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="0e440-465">mediaContentRatingUnitedKingdom</span></span>](../resources/intune-deviceconfig-mediacontentratingunitedkingdom.md)|<span data-ttu-id="0e440-466">Clasificación de contenido multimedia para el Reino Unido</span><span class="sxs-lookup"><span data-stu-id="0e440-466">Media content rating settings for United Kingdom</span></span>|
|<span data-ttu-id="0e440-467">mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="0e440-467">mediaContentRatingUnitedStates</span></span>|[<span data-ttu-id="0e440-468">mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="0e440-468">mediaContentRatingUnitedStates</span></span>](../resources/intune-deviceconfig-mediacontentratingunitedstates.md)|<span data-ttu-id="0e440-469">Clasificación de contenido multimedia para Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="0e440-469">Media content rating settings for United States</span></span>|
|<span data-ttu-id="0e440-470">networkUsageRules</span><span class="sxs-lookup"><span data-stu-id="0e440-470">networkUsageRules</span></span>|<span data-ttu-id="0e440-471">Colección [iosNetworkUsageRule](../resources/intune-deviceconfig-iosnetworkusagerule.md)</span><span class="sxs-lookup"><span data-stu-id="0e440-471">[iosNetworkUsageRule](../resources/intune-deviceconfig-iosnetworkusagerule.md) collection</span></span>|<span data-ttu-id="0e440-472">Lista de aplicaciones administradas y las reglas de red que se les aplican.</span><span class="sxs-lookup"><span data-stu-id="0e440-472">List of managed apps and the network rules that applies to them.</span></span> <span data-ttu-id="0e440-473">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="0e440-473">This collection can contain a maximum of 1000 elements.</span></span>|
|<span data-ttu-id="0e440-474">mediaContentRatingApps</span><span class="sxs-lookup"><span data-stu-id="0e440-474">mediaContentRatingApps</span></span>|[<span data-ttu-id="0e440-475">ratingAppsType</span><span class="sxs-lookup"><span data-stu-id="0e440-475">ratingAppsType</span></span>](../resources/intune-deviceconfig-ratingappstype.md)|<span data-ttu-id="0e440-476">Configuración de clasificación para las aplicaciones de contenido de medios.</span><span class="sxs-lookup"><span data-stu-id="0e440-476">Media content rating settings for Apps.</span></span> <span data-ttu-id="0e440-477">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12`, `agesAbove17`.</span><span class="sxs-lookup"><span data-stu-id="0e440-477">Possible values are: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12`, `agesAbove17`.</span></span>|
|<span data-ttu-id="0e440-478">messagesBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-478">messagesBlocked</span></span>|<span data-ttu-id="0e440-479">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-479">Boolean</span></span>|<span data-ttu-id="0e440-480">Indica si se va a impedir que el usuario use la aplicación Mensajes en el dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-480">Indicates whether or not to block the user from using the Messages app on the supervised device.</span></span>|
|<span data-ttu-id="0e440-481">notificationsBlockSettingsModification</span><span class="sxs-lookup"><span data-stu-id="0e440-481">notificationsBlockSettingsModification</span></span>|<span data-ttu-id="0e440-482">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-482">Boolean</span></span>|<span data-ttu-id="0e440-483">Indica si se van a permitir modificar la configuración de las notificaciones (iOS 9,3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-483">Indicates whether or not to allow notifications settings modification (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="0e440-484">passcodeBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="0e440-484">passcodeBlockFingerprintUnlock</span></span>|<span data-ttu-id="0e440-485">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-485">Boolean</span></span>|<span data-ttu-id="0e440-486">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="0e440-486">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="0e440-487">passcodeBlockFingerprintModification</span><span class="sxs-lookup"><span data-stu-id="0e440-487">passcodeBlockFingerprintModification</span></span>|<span data-ttu-id="0e440-488">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-488">Boolean</span></span>|<span data-ttu-id="0e440-489">Impide la modificación de huellas digitales registradas de Touch ID en el modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-489">Block modification of registered Touch ID fingerprints when in supervised mode.</span></span>|
|<span data-ttu-id="0e440-490">passcodeBlockModification</span><span class="sxs-lookup"><span data-stu-id="0e440-490">passcodeBlockModification</span></span>|<span data-ttu-id="0e440-491">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-491">Boolean</span></span>|<span data-ttu-id="0e440-492">Indica si se va a permitir modificar los códigos de acceso cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-492">Indicates whether or not to allow passcode modification on the supervised device (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="0e440-493">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="0e440-493">passcodeBlockSimple</span></span>|<span data-ttu-id="0e440-494">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-494">Boolean</span></span>|<span data-ttu-id="0e440-495">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="0e440-495">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="0e440-496">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="0e440-496">passcodeExpirationDays</span></span>|<span data-ttu-id="0e440-497">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-497">Int32</span></span>|<span data-ttu-id="0e440-498">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="0e440-498">Number of days before the passcode expires.</span></span> <span data-ttu-id="0e440-499">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="0e440-499">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="0e440-500">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="0e440-500">passcodeMinimumLength</span></span>|<span data-ttu-id="0e440-501">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-501">Int32</span></span>|<span data-ttu-id="0e440-502">Longitud mínima de los códigos de acceso.</span><span class="sxs-lookup"><span data-stu-id="0e440-502">Minimum length of passcode.</span></span> <span data-ttu-id="0e440-503">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="0e440-503">Valid values 4 to 14</span></span>|
|<span data-ttu-id="0e440-504">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="0e440-504">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="0e440-505">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-505">Int32</span></span>|<span data-ttu-id="0e440-506">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="0e440-506">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="0e440-507">passcodeMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="0e440-507">passcodeMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="0e440-508">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-508">Int32</span></span>|<span data-ttu-id="0e440-509">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0e440-509">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="0e440-510">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="0e440-510">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="0e440-511">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-511">Int32</span></span>|<span data-ttu-id="0e440-512">Número de juegos de caracteres que debe contener un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="0e440-512">Number of character sets a passcode must contain.</span></span> <span data-ttu-id="0e440-513">Valores válidos de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="0e440-513">Valid values 0 to 4</span></span>|
|<span data-ttu-id="0e440-514">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="0e440-514">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="0e440-515">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-515">Int32</span></span>|<span data-ttu-id="0e440-516">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="0e440-516">Number of previous passcodes to block.</span></span> <span data-ttu-id="0e440-517">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="0e440-517">Valid values 1 to 24</span></span>|
|<span data-ttu-id="0e440-518">passcodeSignInFailureCountBeforeWipe</span><span class="sxs-lookup"><span data-stu-id="0e440-518">passcodeSignInFailureCountBeforeWipe</span></span>|<span data-ttu-id="0e440-519">Int32</span><span class="sxs-lookup"><span data-stu-id="0e440-519">Int32</span></span>|<span data-ttu-id="0e440-520">Número de errores de inicio de sesión permitidos antes de borrar los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e440-520">Number of sign in failures allowed before wiping the device.</span></span> <span data-ttu-id="0e440-521">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="0e440-521">Valid values 4 to 11</span></span>|
|<span data-ttu-id="0e440-522">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="0e440-522">passcodeRequiredType</span></span>|[<span data-ttu-id="0e440-523">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="0e440-523">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="0e440-524">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="0e440-524">Type of passcode that is required.</span></span> <span data-ttu-id="0e440-525">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="0e440-525">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="0e440-526">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="0e440-526">passcodeRequired</span></span>|<span data-ttu-id="0e440-527">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-527">Boolean</span></span>|<span data-ttu-id="0e440-528">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="0e440-528">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="0e440-529">podcastsBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-529">podcastsBlocked</span></span>|<span data-ttu-id="0e440-530">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-530">Boolean</span></span>|<span data-ttu-id="0e440-531">Indica si se va a impedir que el usuario use Podcasts cuando el dispositivo está en modo supervisado (iOS 8.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-531">Indicates whether or not to block the user from using podcasts on the supervised device (iOS 8.0 and later).</span></span>|
|<span data-ttu-id="0e440-532">safariBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="0e440-532">safariBlockAutofill</span></span>|<span data-ttu-id="0e440-533">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-533">Boolean</span></span>|<span data-ttu-id="0e440-534">Indica si se va a impedir que el usuario use la opción de autorrellenado en Safari.</span><span class="sxs-lookup"><span data-stu-id="0e440-534">Indicates whether or not to block the user from using Auto fill in Safari.</span></span>|
|<span data-ttu-id="0e440-535">safariBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="0e440-535">safariBlockJavaScript</span></span>|<span data-ttu-id="0e440-536">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-536">Boolean</span></span>|<span data-ttu-id="0e440-537">Indica si se va a bloquear JavaScript en Safari.</span><span class="sxs-lookup"><span data-stu-id="0e440-537">Indicates whether or not to block JavaScript in Safari.</span></span>|
|<span data-ttu-id="0e440-538">safariBlockPopups</span><span class="sxs-lookup"><span data-stu-id="0e440-538">safariBlockPopups</span></span>|<span data-ttu-id="0e440-539">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-539">Boolean</span></span>|<span data-ttu-id="0e440-540">Indica si se van a bloquear los elementos emergentes en Safari.</span><span class="sxs-lookup"><span data-stu-id="0e440-540">Indicates whether or not to block popups in Safari.</span></span>|
|<span data-ttu-id="0e440-541">safariBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-541">safariBlocked</span></span>|<span data-ttu-id="0e440-542">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-542">Boolean</span></span>|<span data-ttu-id="0e440-543">Indica si se va a impedir que el usuario use Safari.</span><span class="sxs-lookup"><span data-stu-id="0e440-543">Indicates whether or not to block the user from using Safari.</span></span>|
|<span data-ttu-id="0e440-544">safariCookieSettings</span><span class="sxs-lookup"><span data-stu-id="0e440-544">safariCookieSettings</span></span>|[<span data-ttu-id="0e440-545">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="0e440-545">webBrowserCookieSettings</span></span>](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|<span data-ttu-id="0e440-546">Configuración de cookies para Safari.</span><span class="sxs-lookup"><span data-stu-id="0e440-546">Cookie settings for Safari.</span></span> <span data-ttu-id="0e440-547">Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.</span><span class="sxs-lookup"><span data-stu-id="0e440-547">Possible values are: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited`, `allowAlways`.</span></span>|
|<span data-ttu-id="0e440-548">safariManagedDomains</span><span class="sxs-lookup"><span data-stu-id="0e440-548">safariManagedDomains</span></span>|<span data-ttu-id="0e440-549">Colección String</span><span class="sxs-lookup"><span data-stu-id="0e440-549">String collection</span></span>|<span data-ttu-id="0e440-550">Las direcciones URL que coinciden con los patrones que se enumeran aquí se considerarán administradas.</span><span class="sxs-lookup"><span data-stu-id="0e440-550">URLs matching the patterns listed here will be considered managed.</span></span>|
|<span data-ttu-id="0e440-551">safariPasswordAutoFillDomains</span><span class="sxs-lookup"><span data-stu-id="0e440-551">safariPasswordAutoFillDomains</span></span>|<span data-ttu-id="0e440-552">Colección String</span><span class="sxs-lookup"><span data-stu-id="0e440-552">String collection</span></span>|<span data-ttu-id="0e440-553">Los usuarios pueden guardar las contraseñas en Safari únicamente de las direcciones URL que coinciden con los patrones que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="0e440-553">Users can save passwords in Safari only from URLs matching the patterns listed here.</span></span> <span data-ttu-id="0e440-554">Se aplica solo a dispositivos en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-554">Applies to devices in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="0e440-555">safariRequireFraudWarning</span><span class="sxs-lookup"><span data-stu-id="0e440-555">safariRequireFraudWarning</span></span>|<span data-ttu-id="0e440-556">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-556">Boolean</span></span>|<span data-ttu-id="0e440-557">Indica si se va a requerir una advertencia de fraude en Safari.</span><span class="sxs-lookup"><span data-stu-id="0e440-557">Indicates whether or not to require fraud warning in Safari.</span></span>|
|<span data-ttu-id="0e440-558">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-558">screenCaptureBlocked</span></span>|<span data-ttu-id="0e440-559">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-559">Boolean</span></span>|<span data-ttu-id="0e440-560">Indica si se impide o no que el usuario tome capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="0e440-560">Indicates whether or not to block the user from taking Screenshots.</span></span>|
|<span data-ttu-id="0e440-561">siriBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-561">siriBlocked</span></span>|<span data-ttu-id="0e440-562">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-562">Boolean</span></span>|<span data-ttu-id="0e440-563">Indica si se va a impedir que el usuario use Siri.</span><span class="sxs-lookup"><span data-stu-id="0e440-563">Indicates whether or not to block the user from using Siri.</span></span>|
|<span data-ttu-id="0e440-564">siriBlockedWhenLocked</span><span class="sxs-lookup"><span data-stu-id="0e440-564">siriBlockedWhenLocked</span></span>|<span data-ttu-id="0e440-565">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-565">Boolean</span></span>|<span data-ttu-id="0e440-566">Indica si se va a impedir que el usuario use Siri cuando está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0e440-566">Indicates whether or not to block the user from using Siri when locked.</span></span>|
|<span data-ttu-id="0e440-567">siriBlockUserGeneratedContent</span><span class="sxs-lookup"><span data-stu-id="0e440-567">siriBlockUserGeneratedContent</span></span>|<span data-ttu-id="0e440-568">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-568">Boolean</span></span>|<span data-ttu-id="0e440-569">Indica si se va a impedir que Siri haga consultas de contenido generado por el usuario cuando se usa en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-569">Indicates whether or not to block Siri from querying user-generated content when used on a supervised device.</span></span>|
|<span data-ttu-id="0e440-570">siriRequireProfanityFilter</span><span class="sxs-lookup"><span data-stu-id="0e440-570">siriRequireProfanityFilter</span></span>|<span data-ttu-id="0e440-571">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-571">Boolean</span></span>|<span data-ttu-id="0e440-572">Indica si se va a evitar que Siri dicte o hable con lenguaje irreverente en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-572">Indicates whether or not to prevent Siri from dictating, or speaking profane language on supervised device.</span></span>|
|<span data-ttu-id="0e440-573">spotlightBlockInternetResults</span><span class="sxs-lookup"><span data-stu-id="0e440-573">spotlightBlockInternetResults</span></span>|<span data-ttu-id="0e440-574">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-574">Boolean</span></span>|<span data-ttu-id="0e440-575">Indica si se va a impedir que la búsqueda Spotlight devuelva resultados de Internet en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-575">Indicates whether or not to block Spotlight search from returning internet results on supervised device.</span></span>|
|<span data-ttu-id="0e440-576">voiceDialingBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-576">voiceDialingBlocked</span></span>|<span data-ttu-id="0e440-577">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-577">Boolean</span></span>|<span data-ttu-id="0e440-578">Indica si se va a bloquear la marcación por voz.</span><span class="sxs-lookup"><span data-stu-id="0e440-578">Indicates whether or not to block voice dialing.</span></span>|
|<span data-ttu-id="0e440-579">wallpaperBlockModification</span><span class="sxs-lookup"><span data-stu-id="0e440-579">wallpaperBlockModification</span></span>|<span data-ttu-id="0e440-580">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-580">Boolean</span></span>|<span data-ttu-id="0e440-581">Indica si se va permitir modificar el fondo de pantalla en un dispositivo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="0e440-581">Indicates whether or not to allow wallpaper modification on supervised device (iOS 9.0 and later) .</span></span>|
|<span data-ttu-id="0e440-582">wiFiConnectOnlyToConfiguredNetworks</span><span class="sxs-lookup"><span data-stu-id="0e440-582">wiFiConnectOnlyToConfiguredNetworks</span></span>|<span data-ttu-id="0e440-583">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-583">Boolean</span></span>|<span data-ttu-id="0e440-584">Indica si se va a forzar al dispositivo para que use solo redes Wi-Fi de perfiles de configuración cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="0e440-584">Indicates whether or not to force the device to use only Wi-Fi networks from configuration profiles when the device is in supervised mode.</span></span>|
|<span data-ttu-id="0e440-585">classroomForceRequestPermissionToLeaveClasses</span><span class="sxs-lookup"><span data-stu-id="0e440-585">classroomForceRequestPermissionToLeaveClasses</span></span>|<span data-ttu-id="0e440-586">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-586">Boolean</span></span>|<span data-ttu-id="0e440-587">Indica si un estudiante inscrito en un curso de no administrado a través de aula solicitará permiso del profesor al intentar deje el curso (iOS 11.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-587">Indicates whether a student enrolled in an unmanaged course via Classroom will request permission from the teacher when attempting to leave the course (iOS 11.3 and later).</span></span>|
|<span data-ttu-id="0e440-588">keychainBlockCloudSync</span><span class="sxs-lookup"><span data-stu-id="0e440-588">keychainBlockCloudSync</span></span>|<span data-ttu-id="0e440-589">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-589">Boolean</span></span>|<span data-ttu-id="0e440-590">Indica si se bloquea iCloud llaves sincronización.</span><span class="sxs-lookup"><span data-stu-id="0e440-590">Indicates whether or not iCloud keychain synchronization is blocked.</span></span>|
|<span data-ttu-id="0e440-591">pkiBlockOTAUpdates</span><span class="sxs-lookup"><span data-stu-id="0e440-591">pkiBlockOTAUpdates</span></span>|<span data-ttu-id="0e440-592">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-592">Boolean</span></span>|<span data-ttu-id="0e440-593">Indica si está o no están bloqueadas por aire actualizaciones PKI.</span><span class="sxs-lookup"><span data-stu-id="0e440-593">Indicates whether or not over-the-air PKI updates are blocked.</span></span> <span data-ttu-id="0e440-594">Si se establece esta restricción a false no deshabilitar las comprobaciones de CRL y OCSP (iOS 7.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-594">Setting this restriction to false does not disable CRL and OCSP checks (iOS 7.0 and later).</span></span>|
|<span data-ttu-id="0e440-595">privacyForceLimitAdTracking</span><span class="sxs-lookup"><span data-stu-id="0e440-595">privacyForceLimitAdTracking</span></span>|<span data-ttu-id="0e440-596">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-596">Boolean</span></span>|<span data-ttu-id="0e440-597">Indica si el seguimiento de anuncios está limitado. (iOS 7.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-597">Indicates if ad tracking is limited.(iOS 7.0 and later).</span></span>|
|<span data-ttu-id="0e440-598">enterpriseBookBlockBackup</span><span class="sxs-lookup"><span data-stu-id="0e440-598">enterpriseBookBlockBackup</span></span>|<span data-ttu-id="0e440-599">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-599">Boolean</span></span>|<span data-ttu-id="0e440-600">Indica si Enterprise book copia de seguridad está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0e440-600">Indicates whether or not Enterprise book back up is blocked.</span></span>|
|<span data-ttu-id="0e440-601">enterpriseBookBlockMetadataSync</span><span class="sxs-lookup"><span data-stu-id="0e440-601">enterpriseBookBlockMetadataSync</span></span>|<span data-ttu-id="0e440-602">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-602">Boolean</span></span>|<span data-ttu-id="0e440-603">Indica si se bloquea en Enterprise libreta de direcciones, notas y resalta la sincronización.</span><span class="sxs-lookup"><span data-stu-id="0e440-603">Indicates whether or not Enterprise book notes and highlights sync is blocked.</span></span>|
|<span data-ttu-id="0e440-604">airPrintBlocked</span><span class="sxs-lookup"><span data-stu-id="0e440-604">airPrintBlocked</span></span>|<span data-ttu-id="0e440-605">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-605">Boolean</span></span>|<span data-ttu-id="0e440-606">Indica si está o no AirPrint bloqueados (iOS 11.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-606">Indicates whether or not AirPrint is blocked (iOS 11.0 and later).</span></span>|
|<span data-ttu-id="0e440-607">airPrintBlockCredentialsStorage</span><span class="sxs-lookup"><span data-stu-id="0e440-607">airPrintBlockCredentialsStorage</span></span>|<span data-ttu-id="0e440-608">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-608">Boolean</span></span>|<span data-ttu-id="0e440-609">Indica si está o no llaves almacenamiento de nombre de usuario y la contraseña de Airprint bloqueados (iOS 11.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-609">Indicates whether or not keychain storage of username and password for Airprint is blocked (iOS 11.0 and later).</span></span>|
|<span data-ttu-id="0e440-610">airPrintForceTrustedTLS</span><span class="sxs-lookup"><span data-stu-id="0e440-610">airPrintForceTrustedTLS</span></span>|<span data-ttu-id="0e440-611">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-611">Boolean</span></span>|<span data-ttu-id="0e440-612">Indica si los certificados de confianza son necesarios para la comunicación de impresión de TLS (iOS 11.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-612">Indicates if trusted certificates are required for TLS printing communication (iOS 11.0 and later).</span></span>|
|<span data-ttu-id="0e440-613">airPrintBlockiBeaconDiscovery</span><span class="sxs-lookup"><span data-stu-id="0e440-613">airPrintBlockiBeaconDiscovery</span></span>|<span data-ttu-id="0e440-614">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-614">Boolean</span></span>|<span data-ttu-id="0e440-615">Indica si se bloquea en iBeacon detección de impresoras AirPrint.</span><span class="sxs-lookup"><span data-stu-id="0e440-615">Indicates whether or not iBeacon discovery of AirPrint printers is blocked.</span></span> <span data-ttu-id="0e440-616">Esto evita falsas balizas de AirPrint Bluetooth de suplantación de identidad para el tráfico de red (iOS 11.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-616">This prevents spurious AirPrint Bluetooth beacons from phishing for network traffic (iOS 11.0 and later).</span></span>|
|<span data-ttu-id="0e440-617">blockSystemAppRemoval</span><span class="sxs-lookup"><span data-stu-id="0e440-617">blockSystemAppRemoval</span></span>|<span data-ttu-id="0e440-618">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-618">Boolean</span></span>|<span data-ttu-id="0e440-619">Indica si la eliminación de las aplicaciones del sistema desde el dispositivo está bloqueada en un dispositivo supervisado (iOS 11.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-619">Indicates whether or not the removal of system apps from the device is blocked on a supervised device (iOS 11.0 and later).</span></span>|
|<span data-ttu-id="0e440-620">vpnBlockCreation</span><span class="sxs-lookup"><span data-stu-id="0e440-620">vpnBlockCreation</span></span>|<span data-ttu-id="0e440-621">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e440-621">Boolean</span></span>|<span data-ttu-id="0e440-622">Indica si está o no la creación de configuraciones de VPN bloqueados (iOS 11.0 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0e440-622">Indicates whether or not the creation of VPN configurations is blocked (iOS 11.0 and later).</span></span>|



## <a name="response"></a><span data-ttu-id="0e440-623">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e440-623">Response</span></span>
<span data-ttu-id="0e440-624">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e440-624">If successful, this method returns a `200 OK` response code and an updated [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e440-625">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e440-625">Example</span></span>
### <a name="request"></a><span data-ttu-id="0e440-626">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e440-626">Request</span></span>
<span data-ttu-id="0e440-627">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e440-627">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 8428

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityListType": "appsInListCompliant",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeBlockVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "https://example.com/kioskModeAppStoreUrl/",
  "kioskModeBuiltInAppId": "Kiosk Mode Built In App Id value",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "Kiosk Mode Managed App Id value",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "allBlocked",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeSignInFailureCountBeforeWipe": 4,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "blockAlways",
  "safariManagedDomains": [
    "Safari Managed Domains value"
  ],
  "safariPasswordAutoFillDomains": [
    "Safari Password Auto Fill Domains value"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true,
  "classroomForceRequestPermissionToLeaveClasses": true,
  "keychainBlockCloudSync": true,
  "pkiBlockOTAUpdates": true,
  "privacyForceLimitAdTracking": true,
  "enterpriseBookBlockBackup": true,
  "enterpriseBookBlockMetadataSync": true,
  "airPrintBlocked": true,
  "airPrintBlockCredentialsStorage": true,
  "airPrintForceTrustedTLS": true,
  "airPrintBlockiBeaconDiscovery": true,
  "blockSystemAppRemoval": true,
  "vpnBlockCreation": true
}
```

### <a name="response"></a><span data-ttu-id="0e440-628">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e440-628">Response</span></span>
<span data-ttu-id="0e440-p132">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e440-p132">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 8604

{
  "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
  "id": "ebba5202-5202-ebba-0252-baeb0252baeb",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityListType": "appsInListCompliant",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeBlockVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "https://example.com/kioskModeAppStoreUrl/",
  "kioskModeBuiltInAppId": "Kiosk Mode Built In App Id value",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "Kiosk Mode Managed App Id value",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "allBlocked",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeSignInFailureCountBeforeWipe": 4,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "blockAlways",
  "safariManagedDomains": [
    "Safari Managed Domains value"
  ],
  "safariPasswordAutoFillDomains": [
    "Safari Password Auto Fill Domains value"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true,
  "classroomForceRequestPermissionToLeaveClasses": true,
  "keychainBlockCloudSync": true,
  "pkiBlockOTAUpdates": true,
  "privacyForceLimitAdTracking": true,
  "enterpriseBookBlockBackup": true,
  "enterpriseBookBlockMetadataSync": true,
  "airPrintBlocked": true,
  "airPrintBlockCredentialsStorage": true,
  "airPrintForceTrustedTLS": true,
  "airPrintBlockiBeaconDiscovery": true,
  "blockSystemAppRemoval": true,
  "vpnBlockCreation": true
}
```





