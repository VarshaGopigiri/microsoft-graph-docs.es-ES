---
title: Tipo de recurso Contract
description: Representa una asociación existente que tiene el espacio empresarial asociado con un espacio empresarial del cliente.
ms.openlocfilehash: 5058ea32946df677596dfb0e4502c6f9d4145ec2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028741"
---
# <a name="contract-resource-type"></a><span data-ttu-id="223b9-103">Tipo de recurso Contract</span><span class="sxs-lookup"><span data-stu-id="223b9-103">Contract resource type</span></span>
<span data-ttu-id="223b9-104">Representa una asociación existente que tiene el espacio empresarial asociado con un espacio empresarial del cliente.</span><span class="sxs-lookup"><span data-stu-id="223b9-104">Represents an existing partnership that the partner tenant has with a customer tenant.</span></span>

> <span data-ttu-id="223b9-p101">**Importante:** Solo existe en los inquilinos asociados. Los inquilinos asociados son los inquilinos de Azure AD que pertenecen a los socios de Microsoft que forman parte de los programas [Proveedor de soluciones en la nube de Microsoft](https://partnercenter.microsoft.com/en-us/partner/programs), Office 365 Syndication o Microsoft Advisor.</span><span class="sxs-lookup"><span data-stu-id="223b9-p101">**Important:** Exists in partner tenants only. Partner tenants are Azure AD tenants that belong to Microsoft partners who are either part of [Microsoft Cloud Solution Provider](https://partnercenter.microsoft.com/en-us/partner/programs), Office 365 Syndication, or Microsoft Advisor partner programs.</span></span>

## <a name="methods"></a><span data-ttu-id="223b9-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="223b9-107">Methods</span></span>

| <span data-ttu-id="223b9-108">Método</span><span class="sxs-lookup"><span data-stu-id="223b9-108">Method</span></span>   | <span data-ttu-id="223b9-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="223b9-109">Return Type</span></span> | <span data-ttu-id="223b9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="223b9-110">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="223b9-111">Obtener contrato</span><span class="sxs-lookup"><span data-stu-id="223b9-111">Get contract</span></span>](../api/contract-get.md) | <span data-ttu-id="223b9-112">Contrato</span><span class="sxs-lookup"><span data-stu-id="223b9-112">Contract</span></span> |<span data-ttu-id="223b9-113">Lea las propiedades de un objeto de un contrato específico.</span><span class="sxs-lookup"><span data-stu-id="223b9-113">Read properties of a specific contract object.</span></span> |
|[<span data-ttu-id="223b9-114">Enumerar contratos</span><span class="sxs-lookup"><span data-stu-id="223b9-114">List contracts</span></span>](../api/contract-list.md) | <span data-ttu-id="223b9-115">Colección de contratos</span><span class="sxs-lookup"><span data-stu-id="223b9-115">Contract collection</span></span> | <span data-ttu-id="223b9-116">Lista de contratos de los inquilinos asociados.</span><span class="sxs-lookup"><span data-stu-id="223b9-116">List of contracts in the partner tenant.</span></span> |

## <a name="properties"></a><span data-ttu-id="223b9-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="223b9-117">Properties</span></span>
| <span data-ttu-id="223b9-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="223b9-118">Property</span></span>   | <span data-ttu-id="223b9-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="223b9-119">Type</span></span> | <span data-ttu-id="223b9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="223b9-120">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="223b9-121">contractType</span><span class="sxs-lookup"><span data-stu-id="223b9-121">contractType</span></span>|<span data-ttu-id="223b9-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="223b9-122">String</span></span>|<span data-ttu-id="223b9-123">Tipo de contrato.</span><span class="sxs-lookup"><span data-stu-id="223b9-123">Type of contract.</span></span><br><br><span data-ttu-id="223b9-124">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="223b9-124">Possible values are:</span></span><br> <span data-ttu-id="223b9-p102">*SyndicationPartner* - socio que tan solo revende y administra O365 e Intune para este cliente. Revenden y dan soporte a sus clientes.</span><span class="sxs-lookup"><span data-stu-id="223b9-p102">*SyndicationPartner* - Partner that exclusively resells and manages O365 and Intune for this customer. They resell and support their customers.</span></span><br> <span data-ttu-id="223b9-p103">*BreadthPartner*: socio que tiene la capacidad de proporcionar soporte administrativo a este cliente. En cambio, no se le permite revender a los clientes.</span><span class="sxs-lookup"><span data-stu-id="223b9-p103">*BreadthPartner* - Partner has the ability to provide administrative support for this customer. However, the partner is not allowed to resell to the customer.</span></span><br><span data-ttu-id="223b9-p104">*ResellerPartner*: socio que es similar a un socio de distribución ("syndication partner"), salvo que el socio no tenga acceso exclusivo a un inquilino. En el caso de la distribución, el cliente no puede comprar suscripciones adicionales directas de Microsoft u otros socios.</span><span class="sxs-lookup"><span data-stu-id="223b9-p104">*ResellerPartner* - Partner that is similar to a syndication partner, except that the partner doesn’t have exclusive access to a tenant. In the syndication case, the customer cannot buy additional direct subscriptions from Microsoft or from other partners.</span></span>|
|<span data-ttu-id="223b9-131">customerId</span><span class="sxs-lookup"><span data-stu-id="223b9-131">customerId</span></span>|<span data-ttu-id="223b9-132">Guid</span><span class="sxs-lookup"><span data-stu-id="223b9-132">Guid</span></span>|<span data-ttu-id="223b9-p105">El identificador único para el inquilino del cliente al que hace referencia esta asociación. Corresponde a la propiedad del id. del recurso de organización del inquilino del cliente.</span><span class="sxs-lookup"><span data-stu-id="223b9-p105">The unique identifier for the customer tenant referenced by this partnership. Corresponds to the id property of the customer tenant's organization resource.</span></span> |
|<span data-ttu-id="223b9-135">defaultDomainName</span><span class="sxs-lookup"><span data-stu-id="223b9-135">defaultDomainName</span></span>|<span data-ttu-id="223b9-136">String</span><span class="sxs-lookup"><span data-stu-id="223b9-136">String</span></span>|<span data-ttu-id="223b9-p106">Una copia del nombre de dominio predeterminado del inquilino del cliente. La copia se realiza cuando se establece la asociación con el cliente. No se actualiza automáticamente si el nombre de dominio predeterminado del inquino del cliente cambia.</span><span class="sxs-lookup"><span data-stu-id="223b9-p106">A copy of the customer tenant's default domain name. The copy is made when the partnership with the customer is established. It is not automatically updated if the customer tenant's default domain name changes.</span></span>|
|<span data-ttu-id="223b9-140">displayName</span><span class="sxs-lookup"><span data-stu-id="223b9-140">displayName</span></span>|<span data-ttu-id="223b9-141">String</span><span class="sxs-lookup"><span data-stu-id="223b9-141">String</span></span>|<span data-ttu-id="223b9-p107">Una copia del nombre que se muestra del inquilino del cliente. La copia se realiza cuando se establece la asociación con el cliente. No se actualiza automáticamente si el nombre que se muestra del inquino del cliente cambia.</span><span class="sxs-lookup"><span data-stu-id="223b9-p107">A copy of the customer tenant's display name. The copy is made when the partnership with the customer is established. It is not automatically updated if the customer tenant's display name changes.</span></span>|
|<span data-ttu-id="223b9-145">id</span><span class="sxs-lookup"><span data-stu-id="223b9-145">id</span></span>|<span data-ttu-id="223b9-146">String</span><span class="sxs-lookup"><span data-stu-id="223b9-146">String</span></span>| <span data-ttu-id="223b9-p108">El identificador único del socio. Clave, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="223b9-p108">The unique identifier for the partnership. Key, read-only</span></span> |

## <a name="relationships"></a><span data-ttu-id="223b9-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="223b9-149">Relationships</span></span>
<span data-ttu-id="223b9-150">Ninguno</span><span class="sxs-lookup"><span data-stu-id="223b9-150">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="223b9-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="223b9-151">JSON representation</span></span>
<span data-ttu-id="223b9-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="223b9-152">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.contract"
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