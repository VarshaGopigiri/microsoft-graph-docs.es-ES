---
title: tipo de recurso agreementFile
description: Representa un términos personalizable del archivo del contrato de uso que administra un inquilino con Azure Active Directory (AD Azure). Contiene los metadatos sobre el archivo del contrato (por ejemplo, el nombre, el idioma, y si éste es el archivo de forma predeterminada).
ms.openlocfilehash: f099715fd25fbae9d7b2a94d6de841b8766c30e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086947"
---
# <a name="agreementfile-resource-type"></a><span data-ttu-id="71657-104">tipo de recurso agreementFile</span><span class="sxs-lookup"><span data-stu-id="71657-104">agreementFile resource type</span></span>

> <span data-ttu-id="71657-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71657-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71657-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71657-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="71657-107">Representa un términos personalizable del archivo del contrato de uso que administra un inquilino con Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="71657-107">Represents a customizable terms of use agreement file that a tenant manages with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="71657-108">Contiene los metadatos sobre el archivo del contrato (por ejemplo, el nombre, el idioma, y si éste es el archivo de forma predeterminada).</span><span class="sxs-lookup"><span data-stu-id="71657-108">It contains metadata about the agreement file (for example, the name, the language, and whether it is the default file).</span></span>

<!--
## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get agreementFile](../api/agreementfile-get.md) | [agreementFile](agreementfile.md) | Read properties and relationships of an **agreementFile** object. |
| [Update](../api/agreementfile-update.md) | [agreementFile](agreementfile.md) | Update an **agreementFile** object. |
| [Delete](../api/agreementfile-delete.md) | None | Delete an **agreementFile** object. |
-->

## <a name="properties"></a><span data-ttu-id="71657-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71657-109">Properties</span></span>
| <span data-ttu-id="71657-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71657-110">Property</span></span>     | <span data-ttu-id="71657-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="71657-111">Type</span></span>        | <span data-ttu-id="71657-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="71657-112">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="71657-113">fileData</span><span class="sxs-lookup"><span data-stu-id="71657-113">fileData</span></span>|[<span data-ttu-id="71657-114">agreementFileData</span><span class="sxs-lookup"><span data-stu-id="71657-114">agreementFileData</span></span>](agreementfiledata.md)|<span data-ttu-id="71657-115">Datos que representan las condiciones de usar un documento PDF.</span><span class="sxs-lookup"><span data-stu-id="71657-115">Data representing the terms of use PDF document.</span></span> <span data-ttu-id="71657-116">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71657-116">Read-only.</span></span>|
|<span data-ttu-id="71657-117">fileName</span><span class="sxs-lookup"><span data-stu-id="71657-117">fileName</span></span>|<span data-ttu-id="71657-118">String</span><span class="sxs-lookup"><span data-stu-id="71657-118">String</span></span>|<span data-ttu-id="71657-119">Nombre del archivo de contrato (por ejemplo, TOU.pdf).</span><span class="sxs-lookup"><span data-stu-id="71657-119">Name of the agreement file (for example, TOU.pdf).</span></span> <span data-ttu-id="71657-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71657-120">Read-only.</span></span>|
|<span data-ttu-id="71657-121">id</span><span class="sxs-lookup"><span data-stu-id="71657-121">id</span></span>|<span data-ttu-id="71657-122">String</span><span class="sxs-lookup"><span data-stu-id="71657-122">String</span></span>|<span data-ttu-id="71657-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71657-123">Read-only.</span></span>|
|<span data-ttu-id="71657-124">isDefault</span><span class="sxs-lookup"><span data-stu-id="71657-124">isDefault</span></span>|<span data-ttu-id="71657-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="71657-125">Boolean</span></span>|<span data-ttu-id="71657-126">Indica si este es el archivo del contrato de forma predeterminada si ninguna de las referencias culturales coincide con la preferencia de cliente.</span><span class="sxs-lookup"><span data-stu-id="71657-126">Indicates whether this is the default agreement file if none of the cultures matches the client preference.</span></span> <span data-ttu-id="71657-127">Si ninguno de los archivos están marcado como predeterminada, el primero de ellos se tratará como el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="71657-127">If none of the files are marked as default, the first one will be treated as the default.</span></span> <span data-ttu-id="71657-128">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71657-128">Read-only.</span></span>|
|<span data-ttu-id="71657-129">language</span><span class="sxs-lookup"><span data-stu-id="71657-129">language</span></span>|<span data-ttu-id="71657-130">String</span><span class="sxs-lookup"><span data-stu-id="71657-130">String</span></span>|<span data-ttu-id="71657-131">Referencia cultural del archivo de contrato en el formato languagecode2-país/regioncode2.</span><span class="sxs-lookup"><span data-stu-id="71657-131">Culture of the agreement file in the format languagecode2-country/regioncode2.</span></span> <span data-ttu-id="71657-132">languagecode2 es un código de dos letras en minúsculas proveniente de ISO 639-1.</span><span class="sxs-lookup"><span data-stu-id="71657-132">languagecode2 is a lowercase two-letter code derived from ISO 639-1.</span></span> <span data-ttu-id="71657-133">país/regioncode2 se deriva de ISO 3166 y normalmente consta de dos letras en mayúsculas, o una etiqueta de idioma BCP 47 (por ejemplo, en-US).</span><span class="sxs-lookup"><span data-stu-id="71657-133">country/regioncode2 is derived from ISO 3166 and usually consists of two uppercase letters, or a BCP-47 language tag (for example, en-US).</span></span> <span data-ttu-id="71657-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71657-134">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="71657-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="71657-135">Relationships</span></span>
<span data-ttu-id="71657-136">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="71657-136">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="71657-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="71657-137">JSON representation</span></span>

<span data-ttu-id="71657-138">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="71657-138">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementFile"
}-->

```json
{
  "fileData": {"@odata.type": "microsoft.graph.agreementFileData"},
  "fileName": "String",
  "id": "String (identifier)",
  "isDefault": true,
  "language": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreementFile resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
