---
title: Actualizar deviceManagement
description: Actualice las propiedades de un objeto deviceManagement.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: cd202c2a015b25234a7bf6ffdbedbd1b9f17eacd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846833"
---
# <a name="update-devicemanagement"></a><span data-ttu-id="98ac1-103">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="98ac1-103">Update deviceManagement</span></span>

> <span data-ttu-id="98ac1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="98ac1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="98ac1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="98ac1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="98ac1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="98ac1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="98ac1-107">Actualice las propiedades de un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="98ac1-107">Update the properties of a [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="98ac1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="98ac1-108">Prerequisites</span></span>

<span data-ttu-id="98ac1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98ac1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="98ac1-111">Tenga en cuenta que el permiso varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="98ac1-111">Note that the permission vary according to workflow.</span></span>

| <span data-ttu-id="98ac1-112">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="98ac1-112">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="98ac1-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98ac1-113">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="98ac1-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98ac1-114">Delegated (work or school account)</span></span> ||
| <span data-ttu-id="98ac1-115">&nbsp;&nbsp; **Android para el trabajo**</span><span class="sxs-lookup"><span data-stu-id="98ac1-115">&nbsp; &nbsp; **Android for Work**</span></span> | <span data-ttu-id="98ac1-116">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-116">DeviceManagementConfiguration.ReadWrite.All</span></span>  |
| <span data-ttu-id="98ac1-117">&nbsp; &nbsp; **Auditoría**</span><span class="sxs-lookup"><span data-stu-id="98ac1-117">&nbsp; &nbsp; **Auditing**</span></span> | <span data-ttu-id="98ac1-118">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-118">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-119">&nbsp;&nbsp; **Los términos de la compañía**</span><span class="sxs-lookup"><span data-stu-id="98ac1-119">&nbsp; &nbsp; **Company terms**</span></span> | <span data-ttu-id="98ac1-120">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-120">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-121">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="98ac1-121">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="98ac1-122">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-122">DeviceManagementConfiguration.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-123">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="98ac1-123">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="98ac1-124">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-124">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-125">&nbsp;&nbsp; **SIM electrónica**</span><span class="sxs-lookup"><span data-stu-id="98ac1-125">&nbsp; &nbsp; **Electronic SIM**</span></span> | <span data-ttu-id="98ac1-126">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-126">DeviceManagementConfiguration.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-127">&nbsp; &nbsp; **Inscripción**</span><span class="sxs-lookup"><span data-stu-id="98ac1-127">&nbsp; &nbsp; **Enrollment**</span></span> | <span data-ttu-id="98ac1-128">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-128">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-129">&nbsp;&nbsp; **De barrera**</span><span class="sxs-lookup"><span data-stu-id="98ac1-129">&nbsp; &nbsp; **Fencing**</span></span> | <span data-ttu-id="98ac1-130">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-130">DeviceManagementConfiguration.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-131">&nbsp;&nbsp; **Notificación**</span><span class="sxs-lookup"><span data-stu-id="98ac1-131">&nbsp; &nbsp; **Notification**</span></span> | <span data-ttu-id="98ac1-132">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-132">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-133">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="98ac1-133">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="98ac1-134">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-134">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-135">&nbsp;&nbsp; **Control de acceso basado en roles (RBAC)**</span><span class="sxs-lookup"><span data-stu-id="98ac1-135">&nbsp; &nbsp; **Role-based access control (RBAC)**</span></span> | <span data-ttu-id="98ac1-136">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-136">DeviceManagementRBAC.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-137">&nbsp;&nbsp; **El acceso remoto**</span><span class="sxs-lookup"><span data-stu-id="98ac1-137">&nbsp; &nbsp; **Remote access**</span></span> | <span data-ttu-id="98ac1-138">DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-138">DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="98ac1-139">&nbsp;&nbsp; **Asistencia remota**</span><span class="sxs-lookup"><span data-stu-id="98ac1-139">&nbsp; &nbsp; **Remote assistance**</span></span> | <span data-ttu-id="98ac1-140">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-140">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-141">&nbsp;&nbsp; **Gestión de gastos de telecomunicaciones**</span><span class="sxs-lookup"><span data-stu-id="98ac1-141">&nbsp; &nbsp; **Telecom expense management**</span></span> | <span data-ttu-id="98ac1-142">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-142">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-143">&nbsp;&nbsp; **Esta sección**</span><span class="sxs-lookup"><span data-stu-id="98ac1-143">&nbsp; &nbsp; **Troublehooting**</span></span> | <span data-ttu-id="98ac1-144">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-144">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-145">&nbsp;&nbsp; **Protección de la información de Windows**</span><span class="sxs-lookup"><span data-stu-id="98ac1-145">&nbsp; &nbsp; **Windows Information Protection**</span></span> | <span data-ttu-id="98ac1-146">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98ac1-146">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="98ac1-147">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98ac1-147">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="98ac1-148">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98ac1-148">Not supported.</span></span>|
| <span data-ttu-id="98ac1-149">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98ac1-149">Application</span></span> | <span data-ttu-id="98ac1-150">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98ac1-150">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="98ac1-151">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98ac1-151">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a><span data-ttu-id="98ac1-152">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98ac1-152">Request headers</span></span>

|<span data-ttu-id="98ac1-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98ac1-153">Header</span></span>|<span data-ttu-id="98ac1-154">Valor</span><span class="sxs-lookup"><span data-stu-id="98ac1-154">Value</span></span>|
|:---|:---|
|<span data-ttu-id="98ac1-155">Autorización</span><span class="sxs-lookup"><span data-stu-id="98ac1-155">Authorization</span></span>|<span data-ttu-id="98ac1-156">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="98ac1-156">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="98ac1-157">Accept</span><span class="sxs-lookup"><span data-stu-id="98ac1-157">Accept</span></span>|<span data-ttu-id="98ac1-158">application/json</span><span class="sxs-lookup"><span data-stu-id="98ac1-158">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="98ac1-159">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98ac1-159">Request body</span></span>

<span data-ttu-id="98ac1-160">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="98ac1-160">In the request body, supply a JSON representation for the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>

<span data-ttu-id="98ac1-161">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="98ac1-161">The following table shows the properties that are required when you create the [deviceManagement](../resources/intune-shared-devicemanagement.md).</span></span>

|<span data-ttu-id="98ac1-162">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98ac1-162">Property</span></span>|<span data-ttu-id="98ac1-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="98ac1-163">Type</span></span>|<span data-ttu-id="98ac1-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="98ac1-164">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="98ac1-165">id</span><span class="sxs-lookup"><span data-stu-id="98ac1-165">id</span></span>|<span data-ttu-id="98ac1-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="98ac1-166">String</span></span>|<span data-ttu-id="98ac1-167">Identificador único para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98ac1-167">Unique identifier for the device.</span></span>|
|<span data-ttu-id="98ac1-168">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="98ac1-168">**Device configuration**</span></span>|
|<span data-ttu-id="98ac1-169">intuneAccountId</span><span class="sxs-lookup"><span data-stu-id="98ac1-169">intuneAccountId</span></span>|<span data-ttu-id="98ac1-170">GUID</span><span class="sxs-lookup"><span data-stu-id="98ac1-170">GUID</span></span>|<span data-ttu-id="98ac1-171">Identificador de cuenta Intune para dado inquilino</span><span class="sxs-lookup"><span data-stu-id="98ac1-171">Intune Account ID for given tenant</span></span>|
|<span data-ttu-id="98ac1-172">legacyPcManangementEnabled</span><span class="sxs-lookup"><span data-stu-id="98ac1-172">legacyPcManangementEnabled</span></span>|<span data-ttu-id="98ac1-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="98ac1-173">Boolean</span></span>|<span data-ttu-id="98ac1-174">La propiedad para habilitar no MDM administrados heredado administración de PC para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="98ac1-174">The property to enable Non-MDM managed legacy PC management for this account.</span></span> <span data-ttu-id="98ac1-175">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="98ac1-175">This property is read-only.</span></span>|
|<span data-ttu-id="98ac1-176">maximumDepTokens</span><span class="sxs-lookup"><span data-stu-id="98ac1-176">maximumDepTokens</span></span>|<span data-ttu-id="98ac1-177">Int32</span><span class="sxs-lookup"><span data-stu-id="98ac1-177">Int32</span></span>|<span data-ttu-id="98ac1-178">Número máximo de tokens DEP permitido por inquilino.</span><span class="sxs-lookup"><span data-stu-id="98ac1-178">Maximum number of DEP tokens allowed per-tenant.</span></span>|
|<span data-ttu-id="98ac1-179">configuración</span><span class="sxs-lookup"><span data-stu-id="98ac1-179">settings</span></span>|[<span data-ttu-id="98ac1-180">deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="98ac1-180">deviceManagementSettings</span></span>](../resources/intune-deviceconfig-devicemanagementsettings.md)|<span data-ttu-id="98ac1-181">Configuración de niveles de cuenta.</span><span class="sxs-lookup"><span data-stu-id="98ac1-181">Account level settings.</span></span>|
|<span data-ttu-id="98ac1-182">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="98ac1-182">**Device management**</span></span>|
|<span data-ttu-id="98ac1-183">accountMoveCompletionDateTime</span><span class="sxs-lookup"><span data-stu-id="98ac1-183">accountMoveCompletionDateTime</span></span>|<span data-ttu-id="98ac1-184">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="98ac1-184">DateTimeOffset</span></span>|<span data-ttu-id="98ac1-185">La fecha y la hora cuando mueven los datos de inquilinos entre scaleunits.</span><span class="sxs-lookup"><span data-stu-id="98ac1-185">The date & time when tenant data moved between scaleunits.</span></span>|
|<span data-ttu-id="98ac1-186">adminConsent</span><span class="sxs-lookup"><span data-stu-id="98ac1-186">adminConsent</span></span>|[<span data-ttu-id="98ac1-187">adminConsent</span><span class="sxs-lookup"><span data-stu-id="98ac1-187">adminConsent</span></span>](../resources/intune-devices-adminconsent.md)|<span data-ttu-id="98ac1-188">Información de consentimiento de administración.</span><span class="sxs-lookup"><span data-stu-id="98ac1-188">Admin consent information.</span></span>|
|<span data-ttu-id="98ac1-189">deviceProtectionOverview</span><span class="sxs-lookup"><span data-stu-id="98ac1-189">deviceProtectionOverview</span></span>|[<span data-ttu-id="98ac1-190">deviceProtectionOverview</span><span class="sxs-lookup"><span data-stu-id="98ac1-190">deviceProtectionOverview</span></span>](../resources/intune-devices-deviceprotectionoverview.md)|<span data-ttu-id="98ac1-191">Información general de protección de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="98ac1-191">Device protection overview.</span></span>|
|<span data-ttu-id="98ac1-192">managedDeviceCleanupSettings</span><span class="sxs-lookup"><span data-stu-id="98ac1-192">managedDeviceCleanupSettings</span></span>|[<span data-ttu-id="98ac1-193">managedDeviceCleanupSettings</span><span class="sxs-lookup"><span data-stu-id="98ac1-193">managedDeviceCleanupSettings</span></span>](../resources/intune-devices-manageddevicecleanupsettings.md)|<span data-ttu-id="98ac1-194">Regla para dispositivos de limpieza</span><span class="sxs-lookup"><span data-stu-id="98ac1-194">Device cleanup rule</span></span>|
|<span data-ttu-id="98ac1-195">subscriptionState</span><span class="sxs-lookup"><span data-stu-id="98ac1-195">subscriptionState</span></span>|[<span data-ttu-id="98ac1-196">deviceManagementSubscriptionState</span><span class="sxs-lookup"><span data-stu-id="98ac1-196">deviceManagementSubscriptionState</span></span>](../resources/intune-devices-devicemanagementsubscriptionstate.md)|<span data-ttu-id="98ac1-197">Estado de suscripción de administración de dispositivos móviles del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="98ac1-197">Tenant mobile device management subscription state.</span></span> <span data-ttu-id="98ac1-198">Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked` y `lockedOut`.</span><span class="sxs-lookup"><span data-stu-id="98ac1-198">Possible values are: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked`, `lockedOut`.</span></span>|
|<span data-ttu-id="98ac1-199">suscripciones</span><span class="sxs-lookup"><span data-stu-id="98ac1-199">subscriptions</span></span>|[<span data-ttu-id="98ac1-200">deviceManagementSubscriptions</span><span class="sxs-lookup"><span data-stu-id="98ac1-200">deviceManagementSubscriptions</span></span>](../resources/intune-devices-devicemanagementsubscriptions.md)|<span data-ttu-id="98ac1-201">Suscripción del inquilino.</span><span class="sxs-lookup"><span data-stu-id="98ac1-201">Tenant's Subscription.</span></span> <span data-ttu-id="98ac1-202">Los valores posibles son: `none`, `intune`, `office365`, `intunePremium`, `intune_EDU`, `intune_SMB`.</span><span class="sxs-lookup"><span data-stu-id="98ac1-202">Possible values are: `none`, `intune`, `office365`, `intunePremium`, `intune_EDU`, `intune_SMB`.</span></span>|
|<span data-ttu-id="98ac1-203">windowsMalwareOverview</span><span class="sxs-lookup"><span data-stu-id="98ac1-203">windowsMalwareOverview</span></span>|[<span data-ttu-id="98ac1-204">windowsMalwareOverview</span><span class="sxs-lookup"><span data-stu-id="98ac1-204">windowsMalwareOverview</span></span>](../resources/intune-devices-windowsmalwareoverview.md)|<span data-ttu-id="98ac1-205">Información general de malware para los dispositivos de windows.</span><span class="sxs-lookup"><span data-stu-id="98ac1-205">Malware overview for windows devices.</span></span>|
|<span data-ttu-id="98ac1-206">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="98ac1-206">**Onboarding**</span></span>|
|<span data-ttu-id="98ac1-207">intuneBrand</span><span class="sxs-lookup"><span data-stu-id="98ac1-207">intuneBrand</span></span>|[<span data-ttu-id="98ac1-208">intuneBrand</span><span class="sxs-lookup"><span data-stu-id="98ac1-208">intuneBrand</span></span>](../resources/intune-onboarding-intunebrand.md)|<span data-ttu-id="98ac1-209">intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.</span><span class="sxs-lookup"><span data-stu-id="98ac1-209">intuneBrand contains data which is used in customizing the appearance of the Company Portal applications as well as the end user web portal.</span></span>|

<span data-ttu-id="98ac1-210">Compatibilidad con propiedades de cuerpo de solicitud varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="98ac1-210">Request body property support varies according to workflow.</span></span>

## <a name="response"></a><span data-ttu-id="98ac1-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98ac1-211">Response</span></span>
<span data-ttu-id="98ac1-212">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98ac1-212">If successful, this method returns a `200 OK` response code and an updated [deviceManagement](../resources/intune-shared-devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98ac1-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98ac1-213">Example</span></span>

### <a name="request"></a><span data-ttu-id="98ac1-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98ac1-214">Request</span></span>

<span data-ttu-id="98ac1-215">Este es un ejemplo de una solicitud sigue el flujo de trabajo de administración de dispositivos:</span><span class="sxs-lookup"><span data-stu-id="98ac1-215">Here is an example of a request following the device management workflow:</span></span>

``` http
PATCH https://graph.microsoft.com/beta/deviceManagement
Content-type: application/json
Content-length: 751

{
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```

### <a name="response"></a><span data-ttu-id="98ac1-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98ac1-216">Response</span></span>

<span data-ttu-id="98ac1-217">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98ac1-217">Here is an example of the response.</span></span> 

<span data-ttu-id="98ac1-218">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="98ac1-218">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="98ac1-219">Propiedades devueltas varían según el flujo de trabajo y el contexto.</span><span class="sxs-lookup"><span data-stu-id="98ac1-219">Returned properties vary according to workflow and context.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 855

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b",
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```



