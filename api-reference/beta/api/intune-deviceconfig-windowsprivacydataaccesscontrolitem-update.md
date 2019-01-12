---
title: Actualizar windowsPrivacyDataAccessControlItem
description: Actualizar las propiedades de un objeto windowsPrivacyDataAccessControlItem.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2a5e6e9ea080edca75de6ef4c8a4df5079ac98b7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960983"
---
# <a name="update-windowsprivacydataaccesscontrolitem"></a><span data-ttu-id="fa7d3-103">Actualizar windowsPrivacyDataAccessControlItem</span><span class="sxs-lookup"><span data-stu-id="fa7d3-103">Update windowsPrivacyDataAccessControlItem</span></span>

> <span data-ttu-id="fa7d3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fa7d3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fa7d3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fa7d3-107">Actualizar las propiedades de un objeto [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fa7d3-107">Update the properties of a [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fa7d3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fa7d3-108">Prerequisites</span></span>
<span data-ttu-id="fa7d3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fa7d3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fa7d3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fa7d3-111">Permission type</span></span>|<span data-ttu-id="fa7d3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fa7d3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fa7d3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fa7d3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="fa7d3-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fa7d3-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="fa7d3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fa7d3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fa7d3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-116">Not supported.</span></span>|
|<span data-ttu-id="fa7d3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fa7d3-117">Application</span></span>|<span data-ttu-id="fa7d3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fa7d3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fa7d3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/privacyAccessControls/{windowsPrivacyDataAccessControlItemId}
```

## <a name="request-headers"></a><span data-ttu-id="fa7d3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fa7d3-120">Request headers</span></span>
|<span data-ttu-id="fa7d3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa7d3-121">Header</span></span>|<span data-ttu-id="fa7d3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fa7d3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fa7d3-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fa7d3-123">Authorization</span></span>|<span data-ttu-id="fa7d3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fa7d3-125">Accept</span><span class="sxs-lookup"><span data-stu-id="fa7d3-125">Accept</span></span>|<span data-ttu-id="fa7d3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fa7d3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fa7d3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fa7d3-127">Request body</span></span>
<span data-ttu-id="fa7d3-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fa7d3-128">In the request body, supply a JSON representation for the [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) object.</span></span>

<span data-ttu-id="fa7d3-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md).</span><span class="sxs-lookup"><span data-stu-id="fa7d3-129">The following table shows the properties that are required when you create the [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md).</span></span>

|<span data-ttu-id="fa7d3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa7d3-130">Property</span></span>|<span data-ttu-id="fa7d3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa7d3-131">Type</span></span>|<span data-ttu-id="fa7d3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa7d3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fa7d3-133">id</span><span class="sxs-lookup"><span data-stu-id="fa7d3-133">id</span></span>|<span data-ttu-id="fa7d3-134">String</span><span class="sxs-lookup"><span data-stu-id="fa7d3-134">String</span></span>|<span data-ttu-id="fa7d3-135">La clave de WindowsPrivacyDataAccessControlItem.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-135">The key of WindowsPrivacyDataAccessControlItem.</span></span>|
|<span data-ttu-id="fa7d3-136">accessLevel</span><span class="sxs-lookup"><span data-stu-id="fa7d3-136">accessLevel</span></span>|[<span data-ttu-id="fa7d3-137">windowsPrivacyDataAccessLevel</span><span class="sxs-lookup"><span data-stu-id="fa7d3-137">windowsPrivacyDataAccessLevel</span></span>](../resources/intune-deviceconfig-windowsprivacydataaccesslevel.md)|<span data-ttu-id="fa7d3-138">Esto indica un nivel de acceso para la categoría de datos de privacidad a la que se le dará la aplicación especificada a.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-138">This indicates an access level for the privacy data category to which the specified application will be given to.</span></span> <span data-ttu-id="fa7d3-139">Los valores posibles son: `notConfigured`, `forceAllow`, `forceDeny` y `userInControl`.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-139">Possible values are: `notConfigured`, `forceAllow`, `forceDeny`, `userInControl`.</span></span>|
|<span data-ttu-id="fa7d3-140">dataCategory</span><span class="sxs-lookup"><span data-stu-id="fa7d3-140">dataCategory</span></span>|[<span data-ttu-id="fa7d3-141">windowsPrivacyDataCategory</span><span class="sxs-lookup"><span data-stu-id="fa7d3-141">windowsPrivacyDataCategory</span></span>](../resources/intune-deviceconfig-windowsprivacydatacategory.md)|<span data-ttu-id="fa7d3-142">Esto indica una categoría de datos de privacidad al que se aplicará el control de acceso específico.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-142">This indicates a privacy data category to which the specific access control will apply.</span></span> <span data-ttu-id="fa7d3-143">Los valores posibles son: `notConfigured`, `accountInfo`, `appsRunInBackground`, `calendar`, `callHistory`, `camera`, `contacts`, `diagnosticsInfo`, `email`, `location`, `messaging`, `microphone`, `motion`, `notifications`, `phone`, `radios`, `tasks`, `syncWithDevices`, `trustedDevices` .</span><span class="sxs-lookup"><span data-stu-id="fa7d3-143">Possible values are: `notConfigured`, `accountInfo`, `appsRunInBackground`, `calendar`, `callHistory`, `camera`, `contacts`, `diagnosticsInfo`, `email`, `location`, `messaging`, `microphone`, `motion`, `notifications`, `phone`, `radios`, `tasks`, `syncWithDevices`, `trustedDevices`.</span></span>|
|<span data-ttu-id="fa7d3-144">appPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="fa7d3-144">appPackageFamilyName</span></span>|<span data-ttu-id="fa7d3-145">String</span><span class="sxs-lookup"><span data-stu-id="fa7d3-145">String</span></span>|<span data-ttu-id="fa7d3-146">El nombre de la familia de paquete de una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-146">The Package Family Name of a Windows app.</span></span> <span data-ttu-id="fa7d3-147">Cuando se establece, se aplica el nivel de acceso a la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-147">When set, the access level applies to the specified application.</span></span>|
|<span data-ttu-id="fa7d3-148">appDisplayName</span><span class="sxs-lookup"><span data-stu-id="fa7d3-148">appDisplayName</span></span>|<span data-ttu-id="fa7d3-149">String</span><span class="sxs-lookup"><span data-stu-id="fa7d3-149">String</span></span>|<span data-ttu-id="fa7d3-150">El nombre de la familia de paquete de una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-150">The Package Family Name of a Windows app.</span></span> <span data-ttu-id="fa7d3-151">Cuando se establece, se aplica el nivel de acceso a la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-151">When set, the access level applies to the specified application.</span></span>|



## <a name="response"></a><span data-ttu-id="fa7d3-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa7d3-152">Response</span></span>
<span data-ttu-id="fa7d3-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-153">If successful, this method returns a `200 OK` response code and an updated [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fa7d3-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa7d3-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="fa7d3-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fa7d3-155">Request</span></span>
<span data-ttu-id="fa7d3-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-156">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/privacyAccessControls/{windowsPrivacyDataAccessControlItemId}
Content-type: application/json
Content-length: 176

{
  "accessLevel": "forceAllow",
  "dataCategory": "accountInfo",
  "appPackageFamilyName": "App Package Family Name value",
  "appDisplayName": "App Display Name value"
}
```

### <a name="response"></a><span data-ttu-id="fa7d3-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa7d3-157">Response</span></span>
<span data-ttu-id="fa7d3-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fa7d3-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 299

{
  "@odata.type": "#microsoft.graph.windowsPrivacyDataAccessControlItem",
  "id": "03b15556-5556-03b1-5655-b1035655b103",
  "accessLevel": "forceAllow",
  "dataCategory": "accountInfo",
  "appPackageFamilyName": "App Package Family Name value",
  "appDisplayName": "App Display Name value"
}
```





