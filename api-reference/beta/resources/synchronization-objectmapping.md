---
title: tipo de recurso objectMapping
description: Define cómo se debe sincronizar un objeto determinado desde el directorio de origen al directorio de destino. En particular, que define cómo el objeto en el directorio de origen debe coincidir con un objeto de directorio de destino, ¿qué (si hay alguno) filtros de ámbito se debe utilizar para decidir si queremos aprovisionar un objeto determinado, y cómo los atributos de objeto deben transformarse continuas desde origen al directorio de destino.
localization_priority: Normal
ms.openlocfilehash: 21e996b72be7df93c86f9e5f78a0033c9203cd2c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851754"
---
# <a name="objectmapping-resource-type"></a><span data-ttu-id="b2b20-104">tipo de recurso objectMapping</span><span class="sxs-lookup"><span data-stu-id="b2b20-104">objectMapping resource type</span></span>

> <span data-ttu-id="b2b20-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2b20-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2b20-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2b20-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b2b20-107">Define cómo se debe sincronizar un objeto determinado desde el directorio de origen al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="b2b20-107">Defines how a given object should be synchronized from source directory to target directory.</span></span> <span data-ttu-id="b2b20-108">En particular, que define cómo el objeto en el directorio de origen debe coincidir con un objeto de directorio de destino, ¿qué (si hay alguno) filtros de ámbito se debe utilizar para decidir si queremos aprovisionar un objeto determinado, y cómo los atributos de objeto deben transformarse continuas desde origen al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="b2b20-108">In particular, it defines how object in source directory should be matched with an object in target directory, what (if any) scoping filters should be used to decide if we want to provision a given object, and how object attributes should be transformed going from source to target directory.</span></span>

<span data-ttu-id="b2b20-109">Las asignaciones de objetos son la parte principal de la [regla de sincronización](synchronization-synchronizationrule.md) y se actualizan como parte del [esquema de sincronización](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="b2b20-109">Object mappings are the main part of the [synchronization rule](synchronization-synchronizationrule.md) and are updated as part of [synchronization schema](synchronization-synchronizationschema.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b2b20-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2b20-110">Properties</span></span>

| <span data-ttu-id="b2b20-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2b20-111">Property</span></span>      | <span data-ttu-id="b2b20-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2b20-112">Type</span></span>      | <span data-ttu-id="b2b20-113">Description</span><span class="sxs-lookup"><span data-stu-id="b2b20-113">Description</span></span>    |
|:--------------|:----------|:---------------|
|<span data-ttu-id="b2b20-114">attributeMappings</span><span class="sxs-lookup"><span data-stu-id="b2b20-114">attributeMappings</span></span>  |<span data-ttu-id="b2b20-115">colección de [attributeMapping](synchronization-attributemapping.md)</span><span class="sxs-lookup"><span data-stu-id="b2b20-115">[attributeMapping](synchronization-attributemapping.md) collection</span></span>    | <span data-ttu-id="b2b20-116">Las asignaciones de atributo definen qué atributos para asignar el objeto de origen en el objeto de destino y cómo debe fluyen.</span><span class="sxs-lookup"><span data-stu-id="b2b20-116">Attribute mappings define which attributes to map from the source object into the target object and how they should flow.</span></span> <span data-ttu-id="b2b20-117">Un número de funciones está disponible para admitir la transformación de los valores de origen original.</span><span class="sxs-lookup"><span data-stu-id="b2b20-117">A number of functions are available to support the transformation of the original source values.</span></span>|
|<span data-ttu-id="b2b20-118">enabled</span><span class="sxs-lookup"><span data-stu-id="b2b20-118">enabled</span></span>        |<span data-ttu-id="b2b20-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="b2b20-119">Boolean</span></span>    |<span data-ttu-id="b2b20-120">Cuando `true`, esta asignación de objeto se procesará durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="b2b20-120">When `true`, this object mapping will be processed during synchronization.</span></span> <span data-ttu-id="b2b20-121">Cuando `false`, se omitirá esta asignación de objeto.</span><span class="sxs-lookup"><span data-stu-id="b2b20-121">When `false`, this object mapping will be skipped.</span></span>|
|<span data-ttu-id="b2b20-122">flowTypes</span><span class="sxs-lookup"><span data-stu-id="b2b20-122">flowTypes</span></span>      |<span data-ttu-id="b2b20-123">objectFlowType</span><span class="sxs-lookup"><span data-stu-id="b2b20-123">objectFlowType</span></span>    |<span data-ttu-id="b2b20-124">Qué tipos de flujo están habilitados para esta asignación de objeto.</span><span class="sxs-lookup"><span data-stu-id="b2b20-124">Which flow types are enabled for this object mapping.</span></span> <span data-ttu-id="b2b20-125">`Add`crea nuevos objetos en el directorio de destino, `Update` modifica los objetos existentes, y `Delete` desactiva los usuarios existentes.</span><span class="sxs-lookup"><span data-stu-id="b2b20-125">`Add` creates new objects in the target directory, `Update` modifies existing objects, and `Delete` deprovisions existing users.</span></span> <span data-ttu-id="b2b20-126">El valor predeterminado es `Add, Update, Delete`.</span><span class="sxs-lookup"><span data-stu-id="b2b20-126">The default is `Add, Update, Delete`.</span></span> |
|<span data-ttu-id="b2b20-127">metadatos</span><span class="sxs-lookup"><span data-stu-id="b2b20-127">metadata</span></span>       |<span data-ttu-id="b2b20-128">colección de metadataEntry</span><span class="sxs-lookup"><span data-stu-id="b2b20-128">metadataEntry collection</span></span>    |<span data-ttu-id="b2b20-129">Propiedades de extensión adicionales.</span><span class="sxs-lookup"><span data-stu-id="b2b20-129">Additional extension properties.</span></span> <span data-ttu-id="b2b20-130">A menos que se mencionan explícitamente, no se deben cambiar los valores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="b2b20-130">Unless mentioned explicitly, metadata values should not be changed.</span></span>|
|<span data-ttu-id="b2b20-131">name</span><span class="sxs-lookup"><span data-stu-id="b2b20-131">name</span></span>           |<span data-ttu-id="b2b20-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2b20-132">String</span></span>     |<span data-ttu-id="b2b20-133">Fácil de usar el nombre de la asignación del objeto.</span><span class="sxs-lookup"><span data-stu-id="b2b20-133">Human-friendly name of the object mapping.</span></span>|
|<span data-ttu-id="b2b20-134">scope</span><span class="sxs-lookup"><span data-stu-id="b2b20-134">scope</span></span>          |[<span data-ttu-id="b2b20-135">filter</span><span class="sxs-lookup"><span data-stu-id="b2b20-135">filter</span></span>](synchronization-filter.md)     |<span data-ttu-id="b2b20-136">Define un filtro que se utilizará al decidir si se debe aprovisionar un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="b2b20-136">Defines a filter to be used when deciding whether a given object should be provisioned.</span></span> <span data-ttu-id="b2b20-137">Por ejemplo, es posible que desee sólo los usuarios de aprovisionamiento que se encuentran en los Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="b2b20-137">For example, you might want to only provision users that are located in the US.</span></span>|
|<span data-ttu-id="b2b20-138">sourceObjectName</span><span class="sxs-lookup"><span data-stu-id="b2b20-138">sourceObjectName</span></span>           |<span data-ttu-id="b2b20-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2b20-139">String</span></span>     |<span data-ttu-id="b2b20-140">Nombre del objeto en el directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="b2b20-140">Name of the object in the source directory.</span></span> <span data-ttu-id="b2b20-141">Debe coincidir con el nombre del objeto de la [definición del directorio](synchronization-directorydefinition.md)de origen.</span><span class="sxs-lookup"><span data-stu-id="b2b20-141">Must match the object name from the source [directory definition](synchronization-directorydefinition.md).</span></span>|
|<span data-ttu-id="b2b20-142">targetObjectName</span><span class="sxs-lookup"><span data-stu-id="b2b20-142">targetObjectName</span></span>           |<span data-ttu-id="b2b20-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2b20-143">String</span></span>     |<span data-ttu-id="b2b20-144">Nombre del objeto en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="b2b20-144">Name of the object in target directory.</span></span> <span data-ttu-id="b2b20-145">Debe coincidir con el nombre del objeto de la [definición del directorio](synchronization-directorydefinition.md)de destino.</span><span class="sxs-lookup"><span data-stu-id="b2b20-145">Must match the object name from the target [directory definition](synchronization-directorydefinition.md).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b2b20-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b2b20-146">JSON representation</span></span>

<span data-ttu-id="b2b20-147">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b2b20-147">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.objectMapping"
}-->

```json
{
  "attributeMappings": [{"@odata.type": "microsoft.graph.attributeMapping"}],
  "enabled": true,
  "flowTypes": "String",
  "metadata": [{"@odata.type": "microsoft.graph.metadataEntry"}],
  "name": "String",
  "scope": {"@odata.type": "microsoft.graph.filter"},
  "sourceObjectName": "String",
  "targetObjectName": "String"
}
```

## <a name="json-example"></a><span data-ttu-id="b2b20-148">Ejemplo JSON</span><span class="sxs-lookup"><span data-stu-id="b2b20-148">JSON Example</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.objectMapping"
}-->

```json
{
    "attributeMappings": [
        {
            "defaultValue": "True",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": {
                "expression": "Not([IsSoftDeleted])",
                "name": "Not",
                "parameters": [
                    {
                        "key": "source",
                        "value": {
                            "expression": "[IsSoftDeleted]",
                            "name": "IsSoftDeleted",
                            "parameters": [],
                            "type": "Attribute"
                        }
                    }
                ],
                "type": "Function"
            },
            "targetAttributeName": "IsActive"
        },
        {
            "defaultValue": null,
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": {
                "expression": "Mid([userPrincipalName], 1, 8)",
                "name": "Mid",
                "parameters": [
                    {
                        "key": "source",
                        "value": {
                            "expression": "[userPrincipalName]",
                            "name": "userPrincipalName",
                            "parameters": [],
                            "type": "Attribute"
                        }
                    },
                    {
                        "key": "start",
                        "value": {
                            "expression": "\"1\"",
                            "name": "1",
                            "parameters": [],
                            "type": "Constant"
                        }
                    },
                    {
                        "key": "length",
                        "value": {
                            "expression": "\"8\"",
                            "name": "8",
                            "parameters": [],
                            "type": "Constant"
                        }
                    }
                ],
                "type": "Function"
            },
            "targetAttributeName": "Alias"
        },
        {
            "defaultValue": null,
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": {
                "expression": "[mail]",
                "name": "mail",
                "parameters": [],
                "type": "Attribute"
            },
            "targetAttributeName": "Email"
        },
        {
            "defaultValue": "ISO-8859-1",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": null,
            "targetAttributeName": "EmailEncodingKey"
        },
        {
            "defaultValue": "en_US",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": null,
            "targetAttributeName": "LanguageLocaleKey"
        },
        {
            "defaultValue": null,
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": {
                "expression": "[givenName]",
                "name": "givenName",
                "parameters": [],
                "type": "Attribute"
            },
            "targetAttributeName": "FirstName"
        },
        {
            "defaultValue": ".",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": {
                "expression": "[surname]",
                "name": "surname",
                "parameters": [],
                "type": "Attribute"
            },
            "targetAttributeName": "LastName"
        },
        {
            "defaultValue": "en_US",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": {
                "expression": "Replace([preferredLanguage], \"-\", , , \"_\", , )",
                "name": "Replace",
                "parameters": [
                    {
                        "key": "source",
                        "value": {
                            "expression": "[preferredLanguage]",
                            "name": "preferredLanguage",
                            "parameters": [],
                            "type": "Attribute"
                        }
                    },
                    {
                        "key": "Find",
                        "value": {
                            "expression": "\"-\"",
                            "name": "-",
                            "parameters": [],
                            "type": "Constant"
                        }
                    },
                    {
                        "key": "Replacement",
                        "value": {
                            "expression": "\"_\"",
                            "name": "_",
                            "parameters": [],
                            "type": "Constant"
                        }
                    }
                ],
                "type": "Function"
            },
            "targetAttributeName": "LocaleSidKey"
        },
        {
            "defaultValue": "Chatter Free User",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": {
                "expression": "SingleAppRoleAssignment([appRoleAssignments])",
                "name": "SingleAppRoleAssignment",
                "parameters": [
                    {
                        "key": "source",
                        "value": {
                            "expression": "[appRoleAssignments]",
                            "name": "appRoleAssignments",
                            "parameters": [],
                            "type": "Attribute"
                        }
                    }
                ],
                "type": "Function"
            },
            "targetAttributeName": "ProfileName"
        },
        {
            "defaultValue": "America/Los_Angeles",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": null,
            "targetAttributeName": "TimeZoneSidKey"
        },
        {
            "defaultValue": null,
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 1,
            "source": {
                "expression": "[userPrincipalName]",
                "name": "userPrincipalName",
                "parameters": [],
                "type": "Attribute"
            },
            "targetAttributeName": "Username"
        },
        {
            "defaultValue": "False",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": null,
            "targetAttributeName": "UserPermissionsCallCenterAutoLogin"
        },
        {
            "defaultValue": "False",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": null,
            "targetAttributeName": "UserPermissionsMarketingUser"
        },
        {
            "defaultValue": "False",
            "exportMissingReferences": false,
            "flowBehavior": "FlowWhenChanged",
            "flowType": "Always",
            "matchingPriority": 0,
            "source": null,
            "targetAttributeName": "UserPermissionsOfflineUser"
        }
    ],
    "enabled": true,
    "flowTypes": "Add, Update, Delete",
    "metadata": [
        {
            "key": "IsCustomerDefined",
            "value": "false"
        },
        {
            "key": "DisableMonitoringForChanges",
            "value": "false"
        },
        {
            "key": "Disposition",
            "value": "\"Normal\""
        },
        {
            "key": "ExcludeFromReporting",
            "value": "false"
        },
        {
            "key": "EscrowBehavior",
            "value": "\"Default\""
        },
        {
            "key": "Unsynchronized",
            "value": "false"
        }
    ],
    "name": "Synchronize Azure Active Directory Users to salesforce.com",
    "scope": null,
    "sourceObjectName": "User",
    "targetObjectName": "User"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "objectMapping resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
