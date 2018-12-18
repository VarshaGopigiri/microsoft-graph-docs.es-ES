---
title: Crear androidManagedStoreAppConfigurationSchema
description: Crear un nuevo objeto androidManagedStoreAppConfigurationSchema.
author: tfitzmac
ms.openlocfilehash: 6e8cb3cc56eb1e6f0cded7539b86aea24194fba1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327737"
---
# <a name="create-androidmanagedstoreappconfigurationschema"></a><span data-ttu-id="3b136-103">Crear androidManagedStoreAppConfigurationSchema</span><span class="sxs-lookup"><span data-stu-id="3b136-103">Create androidManagedStoreAppConfigurationSchema</span></span>

> <span data-ttu-id="3b136-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b136-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b136-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b136-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3b136-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3b136-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3b136-107">Crear un nuevo objeto [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) .</span><span class="sxs-lookup"><span data-stu-id="3b136-107">Create a new [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3b136-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3b136-108">Prerequisites</span></span>
<span data-ttu-id="3b136-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b136-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3b136-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3b136-111">Permission type</span></span>|<span data-ttu-id="3b136-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3b136-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3b136-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3b136-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3b136-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b136-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="3b136-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3b136-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3b136-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b136-116">Not supported.</span></span>|
|<span data-ttu-id="3b136-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3b136-117">Application</span></span>|<span data-ttu-id="3b136-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b136-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3b136-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b136-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidManagedStoreAppConfigurationSchemas
```

## <a name="request-headers"></a><span data-ttu-id="3b136-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b136-120">Request headers</span></span>
|<span data-ttu-id="3b136-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b136-121">Header</span></span>|<span data-ttu-id="3b136-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3b136-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3b136-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3b136-123">Authorization</span></span>|<span data-ttu-id="3b136-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3b136-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3b136-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3b136-125">Accept</span></span>|<span data-ttu-id="3b136-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3b136-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3b136-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b136-127">Request body</span></span>
<span data-ttu-id="3b136-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidManagedStoreAppConfigurationSchema.</span><span class="sxs-lookup"><span data-stu-id="3b136-128">In the request body, supply a JSON representation for the androidManagedStoreAppConfigurationSchema object.</span></span>

<span data-ttu-id="3b136-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidManagedStoreAppConfigurationSchema.</span><span class="sxs-lookup"><span data-stu-id="3b136-129">The following table shows the properties that are required when you create the androidManagedStoreAppConfigurationSchema.</span></span>

|<span data-ttu-id="3b136-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3b136-130">Property</span></span>|<span data-ttu-id="3b136-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b136-131">Type</span></span>|<span data-ttu-id="3b136-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b136-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3b136-133">id</span><span class="sxs-lookup"><span data-stu-id="3b136-133">id</span></span>|<span data-ttu-id="3b136-134">String</span><span class="sxs-lookup"><span data-stu-id="3b136-134">String</span></span>|<span data-ttu-id="3b136-135">Clave de la entidad a la que corresponde el esquema del nombre del paquete Android para la aplicación</span><span class="sxs-lookup"><span data-stu-id="3b136-135">Key of the entity the Android package name for the application the schema corresponds to</span></span>|
|<span data-ttu-id="3b136-136">exampleJson</span><span class="sxs-lookup"><span data-stu-id="3b136-136">exampleJson</span></span>|<span data-ttu-id="3b136-137">Binario</span><span class="sxs-lookup"><span data-stu-id="3b136-137">Binary</span></span>|<span data-ttu-id="3b136-138">Matriz de bytes codificada UTF8 que contiene la cadena JSON de ejemplo conforme a este esquema que muestra cómo configurar los ajustes de esta aplicación</span><span class="sxs-lookup"><span data-stu-id="3b136-138">UTF8 encoded byte array containing example JSON string conforming to this schema that demonstrates how to set the configuration for this app</span></span>|
|<span data-ttu-id="3b136-139">schemaItems</span><span class="sxs-lookup"><span data-stu-id="3b136-139">schemaItems</span></span>|<span data-ttu-id="3b136-140">colección de [androidManagedStoreAppConfigurationSchemaItem](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschemaitem.md)</span><span class="sxs-lookup"><span data-stu-id="3b136-140">[androidManagedStoreAppConfigurationSchemaItem](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschemaitem.md) collection</span></span>|<span data-ttu-id="3b136-141">Colección de elementos donde cada uno representa una opción de configuración con nombre en el esquema</span><span class="sxs-lookup"><span data-stu-id="3b136-141">Collection of items each representing a named configuration option in the schema</span></span>|



## <a name="response"></a><span data-ttu-id="3b136-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b136-142">Response</span></span>
<span data-ttu-id="3b136-143">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b136-143">If successful, this method returns a `201 Created` response code and a [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3b136-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b136-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="3b136-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b136-145">Request</span></span>
<span data-ttu-id="3b136-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b136-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAppConfigurationSchemas
Content-type: application/json
Content-length: 805

{
  "@odata.type": "#microsoft.graph.androidManagedStoreAppConfigurationSchema",
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

### <a name="response"></a><span data-ttu-id="3b136-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b136-147">Response</span></span>
<span data-ttu-id="3b136-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3b136-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





