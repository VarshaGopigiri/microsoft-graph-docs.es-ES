---
title: Tipo de recurso Contract
description: Representa una asociación existente que tiene el espacio empresarial asociado con un espacio empresarial del cliente.
ms.openlocfilehash: 7465a54c735b7c1e6f9d5ecb8bf79420b8de45c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090342"
---
# <a name="contract-resource-type"></a><span data-ttu-id="d8696-103">Tipo de recurso Contract</span><span class="sxs-lookup"><span data-stu-id="d8696-103">Contract resource type</span></span>

> <span data-ttu-id="d8696-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d8696-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d8696-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d8696-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d8696-106">Representa una asociación existente que tiene el espacio empresarial asociado con un espacio empresarial del cliente.</span><span class="sxs-lookup"><span data-stu-id="d8696-106">Represents an existing partnership that the partner tenant has with a customer tenant.</span></span>

> <span data-ttu-id="d8696-p102">**Importante:** Solo existe en los inquilinos asociados. Los inquilinos asociados son los inquilinos de Azure AD que pertenecen a los socios de Microsoft que forman parte de los programas [Proveedor de soluciones en la nube de Microsoft](https://partnercenter.microsoft.com/en-us/partner/programs), Office 365 Syndication o Microsoft Advisor.</span><span class="sxs-lookup"><span data-stu-id="d8696-p102">**Important:** Exists in partner tenants only. Partner tenants are Azure AD tenants that belong to Microsoft partners who are either part of [Microsoft Cloud Solution Provider](https://partnercenter.microsoft.com/en-us/partner/programs), Office 365 Syndication, or Microsoft Advisor partner programs.</span></span>

## <a name="methods"></a><span data-ttu-id="d8696-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d8696-109">Methods</span></span>

| <span data-ttu-id="d8696-110">Método</span><span class="sxs-lookup"><span data-stu-id="d8696-110">Method</span></span>   | <span data-ttu-id="d8696-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8696-111">Return Type</span></span> | <span data-ttu-id="d8696-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8696-112">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="d8696-113">Obtener contrato</span><span class="sxs-lookup"><span data-stu-id="d8696-113">Get contract</span></span>](../api/contract-get.md) | <span data-ttu-id="d8696-114">Contrato</span><span class="sxs-lookup"><span data-stu-id="d8696-114">Contract</span></span> |<span data-ttu-id="d8696-115">Lea las propiedades de un objeto de un contrato específico.</span><span class="sxs-lookup"><span data-stu-id="d8696-115">Read properties of a specific contract object.</span></span> |
|[<span data-ttu-id="d8696-116">Enumerar contratos</span><span class="sxs-lookup"><span data-stu-id="d8696-116">List contracts</span></span>](../api/contract-list.md) | <span data-ttu-id="d8696-117">Colección de contratos</span><span class="sxs-lookup"><span data-stu-id="d8696-117">Contract collection</span></span> | <span data-ttu-id="d8696-118">Lista de contratos de los inquilinos asociados.</span><span class="sxs-lookup"><span data-stu-id="d8696-118">List of contracts in the partner tenant.</span></span> |

## <a name="properties"></a><span data-ttu-id="d8696-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8696-119">Properties</span></span>
| <span data-ttu-id="d8696-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8696-120">Property</span></span>   | <span data-ttu-id="d8696-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8696-121">Type</span></span> | <span data-ttu-id="d8696-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8696-122">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="d8696-123">contractType</span><span class="sxs-lookup"><span data-stu-id="d8696-123">contractType</span></span>|<span data-ttu-id="d8696-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="d8696-124">String</span></span>|<span data-ttu-id="d8696-125">Tipo de contrato.</span><span class="sxs-lookup"><span data-stu-id="d8696-125">Type of contract.</span></span><br><br><span data-ttu-id="d8696-126">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="d8696-126">Possible values are:</span></span><br> <span data-ttu-id="d8696-p103">*SyndicationPartner* - socio que tan solo revende y administra O365 e Intune para este cliente. Revenden y dan soporte a sus clientes.</span><span class="sxs-lookup"><span data-stu-id="d8696-p103">*SyndicationPartner* - Partner that exclusively resells and manages O365 and Intune for this customer. They resell and support their customers.</span></span><br> <span data-ttu-id="d8696-p104">*BreadthPartner*: socio que tiene la capacidad de proporcionar soporte administrativo a este cliente. En cambio, no se le permite revender a los clientes.</span><span class="sxs-lookup"><span data-stu-id="d8696-p104">*BreadthPartner* - Partner has the ability to provide administrative support for this customer. However, the partner is not allowed to resell to the customer.</span></span><br><span data-ttu-id="d8696-p105">*ResellerPartner*: socio que es similar a un socio de distribución ("syndication partner"), salvo que el socio no tenga acceso exclusivo a un inquilino. En el caso de la distribución, el cliente no puede comprar suscripciones adicionales directas de Microsoft u otros socios.</span><span class="sxs-lookup"><span data-stu-id="d8696-p105">*ResellerPartner* - Partner that is similar to a syndication partner, except that the partner doesn’t have exclusive access to a tenant. In the syndication case, the customer cannot buy additional direct subscriptions from Microsoft or from other partners.</span></span>|
|<span data-ttu-id="d8696-133">customerId</span><span class="sxs-lookup"><span data-stu-id="d8696-133">customerId</span></span>|<span data-ttu-id="d8696-134">Guid</span><span class="sxs-lookup"><span data-stu-id="d8696-134">Guid</span></span>|<span data-ttu-id="d8696-p106">El identificador único para el inquilino del cliente al que hace referencia esta asociación. Corresponde a la propiedad del id. del recurso de organización del inquilino del cliente.</span><span class="sxs-lookup"><span data-stu-id="d8696-p106">The unique identifier for the customer tenant referenced by this partnership. Corresponds to the id property of the customer tenant's organization resource.</span></span> |
|<span data-ttu-id="d8696-137">defaultDomainName</span><span class="sxs-lookup"><span data-stu-id="d8696-137">defaultDomainName</span></span>|<span data-ttu-id="d8696-138">String</span><span class="sxs-lookup"><span data-stu-id="d8696-138">String</span></span>|<span data-ttu-id="d8696-p107">Una copia del nombre de dominio predeterminado del inquilino del cliente. La copia se realiza cuando se establece la asociación con el cliente. No se actualiza automáticamente si el nombre de dominio predeterminado del inquino del cliente cambia.</span><span class="sxs-lookup"><span data-stu-id="d8696-p107">A copy of the customer tenant's default domain name. The copy is made when the partnership with the customer is established. It is not automatically updated if the customer tenant's default domain name changes.</span></span>|
|<span data-ttu-id="d8696-142">displayName</span><span class="sxs-lookup"><span data-stu-id="d8696-142">displayName</span></span>|<span data-ttu-id="d8696-143">String</span><span class="sxs-lookup"><span data-stu-id="d8696-143">String</span></span>|<span data-ttu-id="d8696-p108">Una copia del nombre que se muestra del inquilino del cliente. La copia se realiza cuando se establece la asociación con el cliente. No se actualiza automáticamente si el nombre que se muestra del inquino del cliente cambia.</span><span class="sxs-lookup"><span data-stu-id="d8696-p108">A copy of the customer tenant's display name. The copy is made when the partnership with the customer is established. It is not automatically updated if the customer tenant's display name changes.</span></span>|
|<span data-ttu-id="d8696-147">id</span><span class="sxs-lookup"><span data-stu-id="d8696-147">id</span></span>|<span data-ttu-id="d8696-148">String</span><span class="sxs-lookup"><span data-stu-id="d8696-148">String</span></span>| <span data-ttu-id="d8696-p109">El identificador único del socio. Clave, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8696-p109">The unique identifier for the partnership. Key, read-only</span></span> |

## <a name="relationships"></a><span data-ttu-id="d8696-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d8696-151">Relationships</span></span>
<span data-ttu-id="d8696-152">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d8696-152">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="d8696-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d8696-153">JSON representation</span></span>
<span data-ttu-id="d8696-154">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d8696-154">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.Contract"
}-->

```json
{
  "contractType": "String",
  "customerId": "Guid",
  "defaultDomainName": "String",
  "displayName": "String",
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Contract resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->