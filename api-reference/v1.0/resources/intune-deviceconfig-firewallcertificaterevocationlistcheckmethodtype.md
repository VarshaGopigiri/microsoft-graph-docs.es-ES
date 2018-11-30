---
title: tipo de enumeración firewallCertificateRevocationListCheckMethodType
description: Valores posibles para firewallCertificateRevocationListCheckMethod
ms.openlocfilehash: b6a7d702b1156598387c204d9e42b15f3066598d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031340"
---
# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a><span data-ttu-id="1eee7-103">tipo de enumeración firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="1eee7-103">firewallCertificateRevocationListCheckMethodType enum type</span></span>

> <span data-ttu-id="1eee7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1eee7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1eee7-105">Valores posibles para firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="1eee7-105">Possible values for firewallCertificateRevocationListCheckMethod</span></span>
## <a name="members"></a><span data-ttu-id="1eee7-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1eee7-106">Members</span></span>
|<span data-ttu-id="1eee7-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="1eee7-107">Member</span></span>|<span data-ttu-id="1eee7-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1eee7-108">Value</span></span>|<span data-ttu-id="1eee7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1eee7-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1eee7-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="1eee7-110">deviceDefault</span></span>|<span data-ttu-id="1eee7-111">0</span><span class="sxs-lookup"><span data-stu-id="1eee7-111">0</span></span>|<span data-ttu-id="1eee7-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="1eee7-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="1eee7-113">ninguno</span><span class="sxs-lookup"><span data-stu-id="1eee7-113">none</span></span>|<span data-ttu-id="1eee7-114">1</span><span class="sxs-lookup"><span data-stu-id="1eee7-114">1</span></span>|<span data-ttu-id="1eee7-115">No comprobar la lista de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="1eee7-115">Do not check certificate revocation list</span></span>|
|<span data-ttu-id="1eee7-116">intento de</span><span class="sxs-lookup"><span data-stu-id="1eee7-116">attempt</span></span>|<span data-ttu-id="1eee7-117">2</span><span class="sxs-lookup"><span data-stu-id="1eee7-117">2</span></span>|<span data-ttu-id="1eee7-118">Intente la comprobación de CRL y permitir que un certificado sólo si el certificado está confirmado por la comprobación de</span><span class="sxs-lookup"><span data-stu-id="1eee7-118">Attempt CRL check and allow a certificate only if the certificate is confirmed by the check</span></span>|
|<span data-ttu-id="1eee7-119">requerir</span><span class="sxs-lookup"><span data-stu-id="1eee7-119">require</span></span>|<span data-ttu-id="1eee7-120">3</span><span class="sxs-lookup"><span data-stu-id="1eee7-120">3</span></span>|<span data-ttu-id="1eee7-121">Requerir una comprobación CRL correcta antes de permitir que un certificado</span><span class="sxs-lookup"><span data-stu-id="1eee7-121">Require a successful CRL check before allowing a certificate</span></span>|



