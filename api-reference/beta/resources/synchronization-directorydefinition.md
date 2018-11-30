---
title: tipo de recurso directoryDefinition
description: Proporciona la información de motor de sincronización sobre un directorio y sus objetos. Este recurso indica al motor de sincronización, por ejemplo, que el directorio tiene objetos con nombre de **usuario** y **grupo**, los atributos que se admiten para los objetos y los tipos de dichos atributos. En orden para el objeto y el atributo a participar en las reglas de sincronización y las asignaciones de objetos, debe definirse como parte de la definición de Active directory.
ms.openlocfilehash: ddc32237efc18d43da23d815aea00ee01b2650be
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090681"
---
# <a name="directorydefinition-resource-type"></a><span data-ttu-id="73773-105">tipo de recurso directoryDefinition</span><span class="sxs-lookup"><span data-stu-id="73773-105">directoryDefinition resource type</span></span>

> <span data-ttu-id="73773-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="73773-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="73773-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="73773-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="73773-108">Proporciona la información de motor de sincronización sobre un directorio y sus objetos.</span><span class="sxs-lookup"><span data-stu-id="73773-108">Provides the synchronization engine information about a directory and its objects.</span></span> <span data-ttu-id="73773-109">Este recurso indica al motor de sincronización, por ejemplo, que el directorio tiene objetos con nombre de **usuario** y **grupo**, los atributos que se admiten para los objetos y los tipos de dichos atributos.</span><span class="sxs-lookup"><span data-stu-id="73773-109">This resource tells the synchronization engine, for example, that the directory has objects named **user** and **group**, which attributes are supported for those objects, and the types for those attributes.</span></span> <span data-ttu-id="73773-110">En orden para el objeto y el atributo a participar en [las reglas de sincronización](synchronization-synchronizationrule.md) y [las asignaciones de objetos](synchronization-objectmapping.md), debe definirse como parte de la definición de Active directory.</span><span class="sxs-lookup"><span data-stu-id="73773-110">In order for the object and attribute to participate in [synchronization rules](synchronization-synchronizationrule.md) and [object mappings](synchronization-objectmapping.md), they must be defined as part of the directory definition.</span></span>

<span data-ttu-id="73773-111">En general, el predeterminado [esquema de sincronización](synchronization-synchronizationschema.md) proporcionado como parte de la [plantilla de sincronización](synchronization-synchronizationtemplate.md) definirá los objetos usados con más frecuencia y los atributos de ese directorio.</span><span class="sxs-lookup"><span data-stu-id="73773-111">In general, the default [synchronization schema](synchronization-synchronizationschema.md) provided as part of the [synchronization template](synchronization-synchronizationtemplate.md) will define most commonly used objects and attributes for that directory.</span></span> <span data-ttu-id="73773-112">Sin embargo, si el directorio admite la adición de atributos personalizados, es posible que desee expandir la definición predeterminada con sus propios objetos personalizados o atributos.</span><span class="sxs-lookup"><span data-stu-id="73773-112">However, if the directory supports the addition of custom attributes, you might want to expand the default definition with your own custom objects or attributes.</span></span> <span data-ttu-id="73773-113">Para obtener más información, vea [Configurar la sincronización con los atributos personalizados](synchronization-configure-with-custom-target-attributes.md) y [Configure la sincronización con los atributos de extensión de Active directory](synchronization-configure-with-directory-extension-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="73773-113">For more information, see [Configure synchronization with custom attributes](synchronization-configure-with-custom-target-attributes.md) and [Configure synchronization with directory extension attributes](synchronization-configure-with-directory-extension-attributes.md).</span></span>

<span data-ttu-id="73773-114">Definiciones de Active Directory se actualizan como parte del [esquema de sincronización](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="73773-114">Directory definitions are updated as part of the [synchronization schema](synchronization-synchronizationschema.md).</span></span>

## <a name="properties"></a><span data-ttu-id="73773-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73773-115">Properties</span></span>

| <span data-ttu-id="73773-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73773-116">Property</span></span>      | <span data-ttu-id="73773-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="73773-117">Type</span></span>      | <span data-ttu-id="73773-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="73773-118">Description</span></span>    |
|:--------------|:----------|:---------------|
|<span data-ttu-id="73773-119">id</span><span class="sxs-lookup"><span data-stu-id="73773-119">id</span></span>           |<span data-ttu-id="73773-120">String</span><span class="sxs-lookup"><span data-stu-id="73773-120">String</span></span>     |<span data-ttu-id="73773-121">Identificador de directorio.</span><span class="sxs-lookup"><span data-stu-id="73773-121">Directory identifier.</span></span> <span data-ttu-id="73773-122">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="73773-122">Not nullable.</span></span>|
|<span data-ttu-id="73773-123">metadatos</span><span class="sxs-lookup"><span data-stu-id="73773-123">metadata</span></span>       |<span data-ttu-id="73773-124">colección de metadataEntry</span><span class="sxs-lookup"><span data-stu-id="73773-124">metadataEntry collection</span></span>    |<span data-ttu-id="73773-125">Propiedades de extensión adicionales.</span><span class="sxs-lookup"><span data-stu-id="73773-125">Additional extension properties.</span></span> <span data-ttu-id="73773-126">A menos que se mencionan explícitamente, no se deben cambiar los valores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="73773-126">Unless mentioned explicitly, metadata values should not be changed.</span></span>|
|<span data-ttu-id="73773-127">name</span><span class="sxs-lookup"><span data-stu-id="73773-127">name</span></span>           |<span data-ttu-id="73773-128">String</span><span class="sxs-lookup"><span data-stu-id="73773-128">String</span></span>     |<span data-ttu-id="73773-129">Nombre del directorio.</span><span class="sxs-lookup"><span data-stu-id="73773-129">Name of the directory.</span></span> <span data-ttu-id="73773-130">Debe ser único en el [esquema de sincronización](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="73773-130">Must be unique within the [synchronization schema](synchronization-synchronizationschema.md).</span></span> <span data-ttu-id="73773-131">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="73773-131">Not nullable.</span></span>|
|<span data-ttu-id="73773-132">objetos</span><span class="sxs-lookup"><span data-stu-id="73773-132">objects</span></span>        |<span data-ttu-id="73773-133">colección de [objectDefinition](synchronization-objectdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="73773-133">[objectDefinition](synchronization-objectdefinition.md) collection</span></span>    |<span data-ttu-id="73773-134">Colección de objetos compatible con el directorio.</span><span class="sxs-lookup"><span data-stu-id="73773-134">Collection of objects supported by the directory.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="73773-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73773-135">JSON representation</span></span>

<span data-ttu-id="73773-136">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="73773-136">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directoryDefinition"
}-->

```json
{
  "id": "String",
  "name": "String",
  "objects": [{"@odata.type": "microsoft.graph.objectDefinition"}]
}

```

## <a name="json-example"></a><span data-ttu-id="73773-137">Ejemplo JSON</span><span class="sxs-lookup"><span data-stu-id="73773-137">JSON Example</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directoryDefinition"
}-->

```json
{
    "id": "8ffa6169-f354-4751-9b77-9c00765be92d",
    "name": "salesforce.com",
    "objects": [
        {
            "attributes": [
                {
                    "anchor": true,
                    "name": "Id",
                    "type": "String"
                },
                {
                    "name": "IsActive",
                    "required": true,
                    "type": "Boolean"
                },
                {
                    "mutability": "ReadWrite",
                    "name": "Alias",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "CompanyName",
                    "type": "String"
                },
                {
                    "name": "CommunityNickname",
                    "type": "String"
                },
                {
                    "name": "Email",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "EmailEncodingKey",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "LanguageLocaleKey",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "FirstName",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "LastName",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "LocaleSidKey",
                    "required": true,
                    "type": "String"
                },
                {
                    "metadata": [
                        {
                            "key": "LinkTypeName",
                            "value": "PermissionSetAssignment"
                        },
                        {
                            "key": "LinkPropertyNames",
                            "value": "[\"PermissionSetId\"]"
                        }
                    ],
                    "name": "PermissionSets",
                    "referencedObjects": [
                        {
                            "referencedObjectName": "PermissionSet"
                        }
                    ],
                    "type": "Reference"
                },
                {
                    "name": "ProfileId",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "ProfileName",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "TimeZoneSidKey",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "Username",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "UserPermissionsCallCenterAutoLogin",
                    "required": true,
                    "type": "Boolean"
                },
                {
                    "name": "UserPermissionsMarketingUser",
                    "required": true,
                    "type": "Boolean"
                },
                {
                    "name": "Street",
                    "type": "String"
                },
                {
                    "name": "City",
                    "type": "String"
                },
                {
                    "name": "Division",
                    "type": "String"
                },
                {
                    "name": "EmployeeNumber",
                    "type": "String"
                },
                {
                    "name": "State",
                    "type": "String"
                },
                {
                    "name": "PostalCode",
                    "type": "String"
                },
                {
                    "name": "Country",
                    "type": "String"
                },
                {
                    "name": "Department",
                    "type": "String"
                },
                {
                    "name": "MobilePhone",
                    "type": "String"
                },
                {
                    "name": "Phone",
                    "type": "String"
                },
                {
                    "name": "Title",
                    "type": "String"
                },
                {
                    "name": "FederationIdentifier",
                    "required": true,
                    "type": "String"
                },
                {
                    "name": "ManagerId",
                    "referencedObjects": [
                        {
                            "referencedObjectName": "User"
                        }
                    ],
                    "type": "Reference"
                },
                {
                    "name": "UserRoleId",
                    "referencedObjects": [
                        {
                            "referencedObjectName": "UserRole"
                        }
                    ],
                    "type": "Reference"
                }
            ],
            "metadata": [
                {
                    "key": "IsSoftDeletionSupported",
                    "value": "false"
                },
                {
                    "key": "ConnectorDataStorageRequired",
                    "value": "false"
                },
                {
                    "key": "IsSynchronizeAllSupported",
                    "value": "false"
                }
            ],
            "name": "User"
        }
    ],
    "metadata": []
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryDefinition resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->