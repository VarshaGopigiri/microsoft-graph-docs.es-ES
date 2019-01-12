---
title: tipo de recurso educationIdentitySynchronizationConfiguration
description: Clase base abstracta para todas las configuraciones school datos perfil identidad sincronización. Las clases derivadas definen el comportamiento para la sincronización de identidades. Los siguientes son los tipos derivados.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 6d9841d4957d5330fc966f60a24582e101831b6c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969033"
---
# <a name="educationidentitysynchronizationconfiguration-resource-type"></a><span data-ttu-id="99395-105">tipo de recurso educationIdentitySynchronizationConfiguration</span><span class="sxs-lookup"><span data-stu-id="99395-105">educationIdentitySynchronizationConfiguration resource type</span></span>

> <span data-ttu-id="99395-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99395-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99395-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99395-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="99395-108">Clase base abstracta para todas las configuraciones school datos perfil identidad sincronización.</span><span class="sxs-lookup"><span data-stu-id="99395-108">Abstract base class for all school data profile identity synchronization configurations.</span></span> <span data-ttu-id="99395-109">Las clases derivadas definen el comportamiento para la sincronización de identidades.</span><span class="sxs-lookup"><span data-stu-id="99395-109">The derived classes define the behavior for synchronizing identities.</span></span> <span data-ttu-id="99395-110">Los siguientes son los tipos derivados.</span><span class="sxs-lookup"><span data-stu-id="99395-110">The following are the derived types.</span></span>

## <a name="derived-types"></a><span data-ttu-id="99395-111">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="99395-111">Derived types</span></span>
| <span data-ttu-id="99395-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="99395-112">Type</span></span> | <span data-ttu-id="99395-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="99395-113">Description</span></span> | 
|:-|:-|
| [<span data-ttu-id="99395-114">**educationIdentityMatchingConfiguration**</span><span class="sxs-lookup"><span data-stu-id="99395-114">**educationIdentityMatchingConfiguration**</span></span>](educationidentitymatchingconfiguration.md) | <span data-ttu-id="99395-115">Use este tipo para que coincida con las cuentas de usuario existentes en Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="99395-115">Use this type to match existing user accounts in Azure Active Directory (Azure AD).</span></span> |
| [<span data-ttu-id="99395-116">**educationIdentityCreationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="99395-116">**educationIdentityCreationConfiguration**</span></span>](educationidentitycreationconfiguration.md) | <span data-ttu-id="99395-117">Use este tipo para crear nuevas cuentas de usuario en Azure AD.</span><span class="sxs-lookup"><span data-stu-id="99395-117">Use this type to create new user accounts in Azure AD.</span></span> |
