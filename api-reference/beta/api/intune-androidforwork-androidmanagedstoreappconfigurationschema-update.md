---
title: Actualizar androidManagedStoreAppConfigurationSchema
description: Actualizar las propiedades de un objeto androidManagedStoreAppConfigurationSchema.
ms.openlocfilehash: e762a909db958b62d1128ff1dae178181124990c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084285"
---
# <a name="update-androidmanagedstoreappconfigurationschema"></a><span data-ttu-id="a74b3-103">Actualizar androidManagedStoreAppConfigurationSchema</span><span class="sxs-lookup"><span data-stu-id="a74b3-103">Update androidManagedStoreAppConfigurationSchema</span></span>

> <span data-ttu-id="a74b3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a74b3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a74b3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a74b3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a74b3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a74b3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a74b3-107">Actualizar las propiedades de un objeto [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) .</span><span class="sxs-lookup"><span data-stu-id="a74b3-107">Update the properties of a [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a74b3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a74b3-108">Prerequisites</span></span>
<span data-ttu-id="a74b3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a74b3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a74b3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a74b3-111">Permission type</span></span>|<span data-ttu-id="a74b3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a74b3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a74b3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a74b3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a74b3-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a74b3-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a74b3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a74b3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a74b3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a74b3-116">Not supported.</span></span>|
|<span data-ttu-id="a74b3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a74b3-117">Application</span></span>|<span data-ttu-id="a74b3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a74b3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a74b3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a74b3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidManagedStoreAppConfigurationSchemas/{androidManagedStoreAppConfigurationSchemaId}
```

## <a name="request-headers"></a><span data-ttu-id="a74b3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a74b3-120">Request headers</span></span>
|<span data-ttu-id="a74b3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a74b3-121">Header</span></span>|<span data-ttu-id="a74b3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a74b3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a74b3-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a74b3-123">Authorization</span></span>|<span data-ttu-id="a74b3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a74b3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a74b3-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a74b3-125">Accept</span></span>|<span data-ttu-id="a74b3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a74b3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a74b3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a74b3-127">Request body</span></span>
<span data-ttu-id="a74b3-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) .</span><span class="sxs-lookup"><span data-stu-id="a74b3-128">In the request body, supply a JSON representation for the [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) object.</span></span>

<span data-ttu-id="a74b3-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="a74b3-129">The following table shows the properties that are required when you create the [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md).</span></span>

|<span data-ttu-id="a74b3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a74b3-130">Property</span></span>|<span data-ttu-id="a74b3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a74b3-131">Type</span></span>|<span data-ttu-id="a74b3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a74b3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a74b3-133">id</span><span class="sxs-lookup"><span data-stu-id="a74b3-133">id</span></span>|<span data-ttu-id="a74b3-134">String</span><span class="sxs-lookup"><span data-stu-id="a74b3-134">String</span></span>|<span data-ttu-id="a74b3-135">Clave de la entidad a la que corresponde el esquema del nombre del paquete Android para la aplicación</span><span class="sxs-lookup"><span data-stu-id="a74b3-135">Key of the entity the Android package name for the application the schema corresponds to</span></span>|
|<span data-ttu-id="a74b3-136">exampleJson</span><span class="sxs-lookup"><span data-stu-id="a74b3-136">exampleJson</span></span>|<span data-ttu-id="a74b3-137">Binario</span><span class="sxs-lookup"><span data-stu-id="a74b3-137">Binary</span></span>|<span data-ttu-id="a74b3-138">Matriz de bytes codificada UTF8 que contiene la cadena JSON de ejemplo conforme a este esquema que muestra cómo configurar los ajustes de esta aplicación</span><span class="sxs-lookup"><span data-stu-id="a74b3-138">UTF8 encoded byte array containing example JSON string conforming to this schema that demonstrates how to set the configuration for this app</span></span>|
|<span data-ttu-id="a74b3-139">schemaItems</span><span class="sxs-lookup"><span data-stu-id="a74b3-139">schemaItems</span></span>|<span data-ttu-id="a74b3-140">colección de [androidManagedStoreAppConfigurationSchemaItem](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschemaitem.md)</span><span class="sxs-lookup"><span data-stu-id="a74b3-140">[androidManagedStoreAppConfigurationSchemaItem](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschemaitem.md) collection</span></span>|<span data-ttu-id="a74b3-141">Colección de elementos donde cada uno representa una opción de configuración con nombre en el esquema</span><span class="sxs-lookup"><span data-stu-id="a74b3-141">Collection of items each representing a named configuration option in the schema</span></span>|



## <a name="response"></a><span data-ttu-id="a74b3-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a74b3-142">Response</span></span>
<span data-ttu-id="a74b3-143">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a74b3-143">If successful, this method returns a `200 OK` response code and an updated [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a74b3-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a74b3-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="a74b3-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a74b3-145">Request</span></span>
<span data-ttu-id="a74b3-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a74b3-146">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAppConfigurationSchemas/{androidManagedStoreAppConfigurationSchemaId}
Content-type: application/json
Content-length: 725

{
  "exampleJson": "ZXhhbXBsZUpzb24=",
  "schemaItems": [
    {
      "@odata.type": "microsoft.graph.androidManagedStoreAppConfigurationSchemaItem",
      "schemaItemKey": "Schema Item Key value",
      "displayName": "Display Name value",
      "description": "Description value",
      "defaultBoolValue": true,
      "defaultIntValue": 15,
      "defaultStringValue": "Default String Value value",
      "defaultStringArrayValue": [
        "Default String Array Value value"
      ],
      "dataType": "integer",
      "selections": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ]
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="a74b3-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a74b3-147">Response</span></span>
<span data-ttu-id="a74b3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a74b3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 854

{
  "@odata.type": "#microsoft.graph.androidManagedStoreAppConfigurationSchema",
  "id": "db86c34a-c34a-db86-4ac3-86db4ac386db",
  "exampleJson": "ZXhhbXBsZUpzb24=",
  "schemaItems": [
    {
      "@odata.type": "microsoft.graph.androidManagedStoreAppConfigurationSchemaItem",
      "schemaItemKey": "Schema Item Key value",
      "displayName": "Display Name value",
      "description": "Description value",
      "defaultBoolValue": true,
      "defaultIntValue": 15,
      "defaultStringValue": "Default String Value value",
      "defaultStringArrayValue": [
        "Default String Array Value value"
      ],
      "dataType": "integer",
      "selections": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ]
    }
  ]
}
```





