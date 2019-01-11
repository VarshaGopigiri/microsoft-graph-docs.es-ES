---
title: tipo de recurso educationIdentitySynchronizationConfiguration
description: Clase base abstracta para todas las configuraciones school datos perfil identidad sincronización. Las clases derivadas definen el comportamiento para la sincronización de identidades. Los siguientes son los tipos derivados.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: c04233dd7f0383d238f0a7e7245e9451fb764be6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869065"
---
# <a name="educationidentitysynchronizationconfiguration-resource-type"></a><span data-ttu-id="30407-105">tipo de recurso educationIdentitySynchronizationConfiguration</span><span class="sxs-lookup"><span data-stu-id="30407-105">educationIdentitySynchronizationConfiguration resource type</span></span>

> <span data-ttu-id="30407-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30407-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30407-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30407-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="30407-108">Clase base abstracta para todas las configuraciones school datos perfil identidad sincronización.</span><span class="sxs-lookup"><span data-stu-id="30407-108">Abstract base class for all school data profile identity synchronization configurations.</span></span> <span data-ttu-id="30407-109">Las clases derivadas definen el comportamiento para la sincronización de identidades.</span><span class="sxs-lookup"><span data-stu-id="30407-109">The derived classes define the behavior for synchronizing identities.</span></span> <span data-ttu-id="30407-110">Los siguientes son los tipos derivados.</span><span class="sxs-lookup"><span data-stu-id="30407-110">The following are the derived types.</span></span>

## <a name="derived-types"></a><span data-ttu-id="30407-111">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="30407-111">Derived types</span></span>
| <span data-ttu-id="30407-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="30407-112">Type</span></span> | <span data-ttu-id="30407-113">Description</span><span class="sxs-lookup"><span data-stu-id="30407-113">Description</span></span> | 
|:-|:-|
| [<span data-ttu-id="30407-114">**educationIdentityMatchingConfiguration**</span><span class="sxs-lookup"><span data-stu-id="30407-114">**educationIdentityMatchingConfiguration**</span></span>](educationidentitymatchingconfiguration.md) | <span data-ttu-id="30407-115">Use este tipo para que coincida con las cuentas de usuario existentes en Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="30407-115">Use this type to match existing user accounts in Azure Active Directory (Azure AD).</span></span> |
| [<span data-ttu-id="30407-116">**educationIdentityCreationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="30407-116">**educationIdentityCreationConfiguration**</span></span>](educationidentitycreationconfiguration.md) | <span data-ttu-id="30407-117">Use este tipo para crear nuevas cuentas de usuario en Azure AD.</span><span class="sxs-lookup"><span data-stu-id="30407-117">Use this type to create new user accounts in Azure AD.</span></span> |
