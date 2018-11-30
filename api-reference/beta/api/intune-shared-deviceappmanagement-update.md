---
title: Actualizar deviceAppManagement
description: Actualice las propiedades de un objeto deviceAppManagement.
ms.openlocfilehash: e842e81f098a42e064be1aa00616a84d7f08eb34
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088336"
---
# <a name="update-deviceappmanagement"></a><span data-ttu-id="6269f-103">Actualizar deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="6269f-103">Update deviceAppManagement</span></span>

> <span data-ttu-id="6269f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6269f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6269f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6269f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6269f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6269f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6269f-107">Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="6269f-107">Update the properties of a [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6269f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6269f-108">Prerequisites</span></span>
<span data-ttu-id="6269f-109">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6269f-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6269f-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6269f-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="6269f-111">Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6269f-111">Note that the appropriate permission varies according to the workflow.</span></span>

|<span data-ttu-id="6269f-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6269f-112">Permission type</span></span>|<span data-ttu-id="6269f-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6269f-113">Permissions (from most to least privileged)</span></span>|
|:---|:---|
| <span data-ttu-id="6269f-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6269f-114">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="6269f-115">&nbsp;&nbsp; **Aplicaciones**, **libros**o **incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="6269f-115">&nbsp; &nbsp; **Apps**, **books**, or **onboarding**</span></span> | <span data-ttu-id="6269f-116">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6269f-116">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="6269f-117">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="6269f-117">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="6269f-118">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6269f-118">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="6269f-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6269f-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6269f-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6269f-120">Not supported.</span></span> |
| <span data-ttu-id="6269f-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6269f-121">Application</span></span> | <span data-ttu-id="6269f-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6269f-122">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6269f-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6269f-123">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement
```

## <a name="request-headers"></a><span data-ttu-id="6269f-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6269f-124">Request headers</span></span>
|<span data-ttu-id="6269f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6269f-125">Header</span></span>|<span data-ttu-id="6269f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6269f-126">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6269f-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="6269f-127">Authorization</span></span>|<span data-ttu-id="6269f-128">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6269f-128">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6269f-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6269f-129">Accept</span></span>|<span data-ttu-id="6269f-130">application/json</span><span class="sxs-lookup"><span data-stu-id="6269f-130">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6269f-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6269f-131">Request body</span></span>
<span data-ttu-id="6269f-132">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="6269f-132">In the request body, supply a JSON representation for the [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object.</span></span>

<span data-ttu-id="6269f-133">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="6269f-133">The following table shows the properties that are required when you create the [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span></span>

|<span data-ttu-id="6269f-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6269f-134">Property</span></span>|<span data-ttu-id="6269f-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="6269f-135">Type</span></span>|<span data-ttu-id="6269f-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="6269f-136">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6269f-137">id</span><span class="sxs-lookup"><span data-stu-id="6269f-137">id</span></span>|<span data-ttu-id="6269f-138">String</span><span class="sxs-lookup"><span data-stu-id="6269f-138">String</span></span>|<span data-ttu-id="6269f-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6269f-139">Key of the entity.</span></span>|
|<span data-ttu-id="6269f-140">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="6269f-140">**On-boarding**</span></span>|
|<span data-ttu-id="6269f-141">isEnabledForMicrosoftStoreForBusiness</span><span class="sxs-lookup"><span data-stu-id="6269f-141">isEnabledForMicrosoftStoreForBusiness</span></span>|<span data-ttu-id="6269f-142">Booleano</span><span class="sxs-lookup"><span data-stu-id="6269f-142">Boolean</span></span>|<span data-ttu-id="6269f-143">Indica si la cuenta está habilitada para la sincronización de aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="6269f-143">Whether the account is enabled for syncing applications from the Microsoft Store for Business.</span></span>|
|<span data-ttu-id="6269f-144">microsoftStoreForBusinessLanguage</span><span class="sxs-lookup"><span data-stu-id="6269f-144">microsoftStoreForBusinessLanguage</span></span>|<span data-ttu-id="6269f-145">String</span><span class="sxs-lookup"><span data-stu-id="6269f-145">String</span></span>|<span data-ttu-id="6269f-146">Información local que se usa para sincronizar las aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="6269f-146">The locale information used to sync applications from the Microsoft Store for Business.</span></span> <span data-ttu-id="6269f-147">Referencias culturales que son específicas de un país o región.</span><span class="sxs-lookup"><span data-stu-id="6269f-147">Cultures that are specific to a country/region.</span></span> <span data-ttu-id="6269f-148">Los nombres de dichas referencias culturales siguen RFC 4646 (Windows Vista y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="6269f-148">The names of these cultures follow RFC 4646 (Windows Vista and later).</span></span> <span data-ttu-id="6269f-149">El formato es <languagecode2>-<country/regioncode2>, donde <languagecode2> es un código de dos letras en minúsculas proveniente de ISO 639-1 y <country/regioncode2> es un código de dos letras en mayúsculas derivado de ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="6269f-149">The format is <languagecode2>-<country/regioncode2>, where <languagecode2> is a lowercase two-letter code derived from ISO 639-1 and <country/regioncode2> is an uppercase two-letter code derived from ISO 3166.</span></span> <span data-ttu-id="6269f-150">Por ejemplo, en-US para inglés (Estados Unidos) es una referencia cultural específica.</span><span class="sxs-lookup"><span data-stu-id="6269f-150">For example, en-US for English (United States) is a specific culture.</span></span>|
|<span data-ttu-id="6269f-151">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span><span class="sxs-lookup"><span data-stu-id="6269f-151">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span></span>|<span data-ttu-id="6269f-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6269f-152">DateTimeOffset</span></span>|<span data-ttu-id="6269f-153">La última vez que se completó una sincronización de aplicaciones desde Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="6269f-153">The last time an application sync from the Microsoft Store for Business was completed.</span></span>|
|<span data-ttu-id="6269f-154">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="6269f-154">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="6269f-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6269f-155">DateTimeOffset</span></span>|<span data-ttu-id="6269f-156">Última vez que se sincronizaron correctamente las aplicaciones de Microsoft Store para Empresas en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="6269f-156">The last time the apps from the Microsoft Store for Business were synced successfully for the account.</span></span>|
|<span data-ttu-id="6269f-157">microsoftStoreForBusinessPortalSelection</span><span class="sxs-lookup"><span data-stu-id="6269f-157">microsoftStoreForBusinessPortalSelection</span></span>|[<span data-ttu-id="6269f-158">microsoftStoreForBusinessPortalSelectionOptions</span><span class="sxs-lookup"><span data-stu-id="6269f-158">microsoftStoreForBusinessPortalSelectionOptions</span></span>](../resources/intune-onboarding-microsoftstoreforbusinessportalselectionoptions.md)|<span data-ttu-id="6269f-159">La información del portal de usuario final se usa para sincronizar las aplicaciones de Portal de empresa Intune de Microsoft Store para la empresa.</span><span class="sxs-lookup"><span data-stu-id="6269f-159">The end user portal information is used to sync applications from the Microsoft Store for Business to Intune Company Portal.</span></span> <span data-ttu-id="6269f-160">Hay tres opciones para elegir entre \['Sólo el portal de la empresa', 'Almacenar compañía del portal y privada', 'Sólo almacén privado'\].</span><span class="sxs-lookup"><span data-stu-id="6269f-160">There are three options to pick from \['Company portal only', 'Company portal and private store', 'Private store only'\].</span></span> <span data-ttu-id="6269f-161">Los valores posibles son: `none`, `companyPortal` y `privateStore`.</span><span class="sxs-lookup"><span data-stu-id="6269f-161">Possible values are: `none`, `companyPortal`, `privateStore`.</span></span>|

<span data-ttu-id="6269f-162">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6269f-162">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="6269f-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6269f-163">Response</span></span>
<span data-ttu-id="6269f-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6269f-164">If successful, this method returns a `200 OK` response code and an updated [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6269f-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6269f-165">Example</span></span>

### <a name="request"></a><span data-ttu-id="6269f-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6269f-166">Request</span></span>

<span data-ttu-id="6269f-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6269f-167">Here is an example of the request.</span></span>

``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="6269f-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6269f-168">Response</span></span>

<span data-ttu-id="6269f-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6269f-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 110

{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
}
```


