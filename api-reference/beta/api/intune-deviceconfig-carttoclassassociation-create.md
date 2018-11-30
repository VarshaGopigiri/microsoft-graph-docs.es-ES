---
title: Crear cartToClassAssociation
description: Crear un nuevo objeto cartToClassAssociation.
ms.openlocfilehash: 87e4a21a998e4226d429bfd92fca5560b9d716e3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090153"
---
# <a name="create-carttoclassassociation"></a><span data-ttu-id="8a6ac-103">Crear cartToClassAssociation</span><span class="sxs-lookup"><span data-stu-id="8a6ac-103">Create cartToClassAssociation</span></span>

> <span data-ttu-id="8a6ac-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a6ac-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8a6ac-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a6ac-107">Crear un nuevo objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .</span><span class="sxs-lookup"><span data-stu-id="8a6ac-107">Create a new [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a6ac-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8a6ac-108">Prerequisites</span></span>
<span data-ttu-id="8a6ac-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a6ac-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a6ac-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a6ac-111">Permission type</span></span>|<span data-ttu-id="8a6ac-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a6ac-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8a6ac-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a6ac-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8a6ac-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a6ac-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8a6ac-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a6ac-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8a6ac-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-116">Not supported.</span></span>|
|<span data-ttu-id="8a6ac-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a6ac-117">Application</span></span>|<span data-ttu-id="8a6ac-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8a6ac-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a6ac-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/cartToClassAssociations
```

## <a name="request-headers"></a><span data-ttu-id="8a6ac-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a6ac-120">Request headers</span></span>
|<span data-ttu-id="8a6ac-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a6ac-121">Header</span></span>|<span data-ttu-id="8a6ac-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8a6ac-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8a6ac-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a6ac-123">Authorization</span></span>|<span data-ttu-id="8a6ac-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8a6ac-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8a6ac-125">Accept</span></span>|<span data-ttu-id="8a6ac-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8a6ac-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a6ac-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a6ac-127">Request body</span></span>
<span data-ttu-id="8a6ac-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto cartToClassAssociation.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-128">In the request body, supply a JSON representation for the cartToClassAssociation object.</span></span>

<span data-ttu-id="8a6ac-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el cartToClassAssociation.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-129">The following table shows the properties that are required when you create the cartToClassAssociation.</span></span>

|<span data-ttu-id="8a6ac-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a6ac-130">Property</span></span>|<span data-ttu-id="8a6ac-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a6ac-131">Type</span></span>|<span data-ttu-id="8a6ac-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a6ac-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a6ac-133">id</span><span class="sxs-lookup"><span data-stu-id="8a6ac-133">id</span></span>|<span data-ttu-id="8a6ac-134">String</span><span class="sxs-lookup"><span data-stu-id="8a6ac-134">String</span></span>|<span data-ttu-id="8a6ac-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-135">Key of the entity.</span></span>|
|<span data-ttu-id="8a6ac-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8a6ac-136">createdDateTime</span></span>|<span data-ttu-id="8a6ac-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a6ac-137">DateTimeOffset</span></span>|<span data-ttu-id="8a6ac-138">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-138">DateTime the object was created.</span></span>|
|<span data-ttu-id="8a6ac-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8a6ac-139">lastModifiedDateTime</span></span>|<span data-ttu-id="8a6ac-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a6ac-140">DateTimeOffset</span></span>|<span data-ttu-id="8a6ac-141">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-141">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="8a6ac-142">version</span><span class="sxs-lookup"><span data-stu-id="8a6ac-142">version</span></span>|<span data-ttu-id="8a6ac-143">Int32</span><span class="sxs-lookup"><span data-stu-id="8a6ac-143">Int32</span></span>|<span data-ttu-id="8a6ac-144">Versión de la CartToClassAssociation.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-144">Version of the CartToClassAssociation.</span></span>|
|<span data-ttu-id="8a6ac-145">displayName</span><span class="sxs-lookup"><span data-stu-id="8a6ac-145">displayName</span></span>|<span data-ttu-id="8a6ac-146">String</span><span class="sxs-lookup"><span data-stu-id="8a6ac-146">String</span></span>|<span data-ttu-id="8a6ac-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-147">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="8a6ac-148">descripción</span><span class="sxs-lookup"><span data-stu-id="8a6ac-148">description</span></span>|<span data-ttu-id="8a6ac-149">String</span><span class="sxs-lookup"><span data-stu-id="8a6ac-149">String</span></span>|<span data-ttu-id="8a6ac-150">Descripción de la CartToClassAssociation proporcionada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-150">Admin provided description of the CartToClassAssociation.</span></span>|
|<span data-ttu-id="8a6ac-151">deviceCartIds</span><span class="sxs-lookup"><span data-stu-id="8a6ac-151">deviceCartIds</span></span>|<span data-ttu-id="8a6ac-152">Colección String</span><span class="sxs-lookup"><span data-stu-id="8a6ac-152">String collection</span></span>|<span data-ttu-id="8a6ac-153">Identificadores de carros de dispositivo que se asociará con clases.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-153">Identifiers of device carts to be associated with classes.</span></span>|
|<span data-ttu-id="8a6ac-154">classroomIds</span><span class="sxs-lookup"><span data-stu-id="8a6ac-154">classroomIds</span></span>|<span data-ttu-id="8a6ac-155">Colección String</span><span class="sxs-lookup"><span data-stu-id="8a6ac-155">String collection</span></span>|<span data-ttu-id="8a6ac-156">Identificadores de aulas que se asociará con carros de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-156">Identifiers of classrooms to be associated with device carts.</span></span>|



## <a name="response"></a><span data-ttu-id="8a6ac-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a6ac-157">Response</span></span>
<span data-ttu-id="8a6ac-158">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-158">If successful, this method returns a `201 Created` response code and a [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a6ac-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a6ac-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="8a6ac-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a6ac-160">Request</span></span>
<span data-ttu-id="8a6ac-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-161">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/cartToClassAssociations
Content-type: application/json
Content-length: 335

{
  "@odata.type": "#microsoft.graph.cartToClassAssociation",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "displayName": "Display Name value",
  "description": "Description value",
  "deviceCartIds": [
    "Device Cart Ids value"
  ],
  "classroomIds": [
    "Classroom Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="8a6ac-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a6ac-162">Response</span></span>
<span data-ttu-id="8a6ac-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a6ac-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 443

{
  "@odata.type": "#microsoft.graph.cartToClassAssociation",
  "id": "9bdc58dd-58dd-9bdc-dd58-dc9bdd58dc9b",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "displayName": "Display Name value",
  "description": "Description value",
  "deviceCartIds": [
    "Device Cart Ids value"
  ],
  "classroomIds": [
    "Classroom Ids value"
  ]
}
```





