---
title: Crear windowsPrivacyDataAccessControlItem
description: Crear un nuevo objeto windowsPrivacyDataAccessControlItem.
author: tfitzmac
ms.openlocfilehash: 262f6866c37d3ed624916189a25ce5a5b5fd0634
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337684"
---
# <a name="create-windowsprivacydataaccesscontrolitem"></a><span data-ttu-id="4772b-103">Crear windowsPrivacyDataAccessControlItem</span><span class="sxs-lookup"><span data-stu-id="4772b-103">Create windowsPrivacyDataAccessControlItem</span></span>

> <span data-ttu-id="4772b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4772b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4772b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4772b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4772b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4772b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4772b-107">Crear un nuevo objeto [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4772b-107">Create a new [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4772b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4772b-108">Prerequisites</span></span>
<span data-ttu-id="4772b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4772b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4772b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4772b-111">Permission type</span></span>|<span data-ttu-id="4772b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4772b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4772b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4772b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4772b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4772b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4772b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4772b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4772b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4772b-116">Not supported.</span></span>|
|<span data-ttu-id="4772b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4772b-117">Application</span></span>|<span data-ttu-id="4772b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4772b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4772b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4772b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/privacyAccessControls
```

## <a name="request-headers"></a><span data-ttu-id="4772b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4772b-120">Request headers</span></span>
|<span data-ttu-id="4772b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4772b-121">Header</span></span>|<span data-ttu-id="4772b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4772b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4772b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4772b-123">Authorization</span></span>|<span data-ttu-id="4772b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4772b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4772b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4772b-125">Accept</span></span>|<span data-ttu-id="4772b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4772b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4772b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4772b-127">Request body</span></span>
<span data-ttu-id="4772b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsPrivacyDataAccessControlItem.</span><span class="sxs-lookup"><span data-stu-id="4772b-128">In the request body, supply a JSON representation for the windowsPrivacyDataAccessControlItem object.</span></span>

<span data-ttu-id="4772b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsPrivacyDataAccessControlItem.</span><span class="sxs-lookup"><span data-stu-id="4772b-129">The following table shows the properties that are required when you create the windowsPrivacyDataAccessControlItem.</span></span>

|<span data-ttu-id="4772b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4772b-130">Property</span></span>|<span data-ttu-id="4772b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4772b-131">Type</span></span>|<span data-ttu-id="4772b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4772b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4772b-133">id</span><span class="sxs-lookup"><span data-stu-id="4772b-133">id</span></span>|<span data-ttu-id="4772b-134">String</span><span class="sxs-lookup"><span data-stu-id="4772b-134">String</span></span>|<span data-ttu-id="4772b-135">La clave de WindowsPrivacyDataAccessControlItem.</span><span class="sxs-lookup"><span data-stu-id="4772b-135">The key of WindowsPrivacyDataAccessControlItem.</span></span>|
|<span data-ttu-id="4772b-136">accessLevel</span><span class="sxs-lookup"><span data-stu-id="4772b-136">accessLevel</span></span>|[<span data-ttu-id="4772b-137">windowsPrivacyDataAccessLevel</span><span class="sxs-lookup"><span data-stu-id="4772b-137">windowsPrivacyDataAccessLevel</span></span>](../resources/intune-deviceconfig-windowsprivacydataaccesslevel.md)|<span data-ttu-id="4772b-138">Esto indica un nivel de acceso para la categoría de datos de privacidad a la que se le dará la aplicación especificada a.</span><span class="sxs-lookup"><span data-stu-id="4772b-138">This indicates an access level for the privacy data category to which the specified application will be given to.</span></span> <span data-ttu-id="4772b-139">Los valores posibles son: `notConfigured`, `forceAllow`, `forceDeny` y `userInControl`.</span><span class="sxs-lookup"><span data-stu-id="4772b-139">Possible values are: `notConfigured`, `forceAllow`, `forceDeny`, `userInControl`.</span></span>|
|<span data-ttu-id="4772b-140">dataCategory</span><span class="sxs-lookup"><span data-stu-id="4772b-140">dataCategory</span></span>|[<span data-ttu-id="4772b-141">windowsPrivacyDataCategory</span><span class="sxs-lookup"><span data-stu-id="4772b-141">windowsPrivacyDataCategory</span></span>](../resources/intune-deviceconfig-windowsprivacydatacategory.md)|<span data-ttu-id="4772b-142">Esto indica una categoría de datos de privacidad al que se aplicará el control de acceso específico.</span><span class="sxs-lookup"><span data-stu-id="4772b-142">This indicates a privacy data category to which the specific access control will apply.</span></span> <span data-ttu-id="4772b-143">Los valores posibles son: `notConfigured`, `accountInfo`, `appsRunInBackground`, `calendar`, `callHistory`, `camera`, `contacts`, `diagnosticsInfo`, `email`, `location`, `messaging`, `microphone`, `motion`, `notifications`, `phone`, `radios`, `tasks`, `syncWithDevices`, `trustedDevices` .</span><span class="sxs-lookup"><span data-stu-id="4772b-143">Possible values are: `notConfigured`, `accountInfo`, `appsRunInBackground`, `calendar`, `callHistory`, `camera`, `contacts`, `diagnosticsInfo`, `email`, `location`, `messaging`, `microphone`, `motion`, `notifications`, `phone`, `radios`, `tasks`, `syncWithDevices`, `trustedDevices`.</span></span>|
|<span data-ttu-id="4772b-144">appPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="4772b-144">appPackageFamilyName</span></span>|<span data-ttu-id="4772b-145">String</span><span class="sxs-lookup"><span data-stu-id="4772b-145">String</span></span>|<span data-ttu-id="4772b-146">El nombre de la familia de paquete de una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4772b-146">The Package Family Name of a Windows app.</span></span> <span data-ttu-id="4772b-147">Cuando se establece, se aplica el nivel de acceso a la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="4772b-147">When set, the access level applies to the specified application.</span></span>|
|<span data-ttu-id="4772b-148">appDisplayName</span><span class="sxs-lookup"><span data-stu-id="4772b-148">appDisplayName</span></span>|<span data-ttu-id="4772b-149">String</span><span class="sxs-lookup"><span data-stu-id="4772b-149">String</span></span>|<span data-ttu-id="4772b-150">El nombre de la familia de paquete de una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4772b-150">The Package Family Name of a Windows app.</span></span> <span data-ttu-id="4772b-151">Cuando se establece, se aplica el nivel de acceso a la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="4772b-151">When set, the access level applies to the specified application.</span></span>|



## <a name="response"></a><span data-ttu-id="4772b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4772b-152">Response</span></span>
<span data-ttu-id="4772b-153">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4772b-153">If successful, this method returns a `201 Created` response code and a [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4772b-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4772b-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="4772b-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4772b-155">Request</span></span>
<span data-ttu-id="4772b-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4772b-156">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/privacyAccessControls
Content-type: application/json
Content-length: 250

{
  "@odata.type": "#microsoft.graph.windowsPrivacyDataAccessControlItem",
  "accessLevel": "forceAllow",
  "dataCategory": "accountInfo",
  "appPackageFamilyName": "App Package Family Name value",
  "appDisplayName": "App Display Name value"
}
```

### <a name="response"></a><span data-ttu-id="4772b-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4772b-157">Response</span></span>
<span data-ttu-id="4772b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4772b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





