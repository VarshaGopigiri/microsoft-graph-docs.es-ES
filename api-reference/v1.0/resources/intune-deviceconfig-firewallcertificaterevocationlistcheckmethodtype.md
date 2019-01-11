---
title: tipo de enumeración firewallCertificateRevocationListCheckMethodType
description: Valores posibles para firewallCertificateRevocationListCheckMethod
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2beee8f7c4f049aa1918b7e1516c3ce586a8cad0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839952"
---
# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a><span data-ttu-id="882a9-103">tipo de enumeración firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="882a9-103">firewallCertificateRevocationListCheckMethodType enum type</span></span>

> <span data-ttu-id="882a9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="882a9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="882a9-105">Valores posibles para firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="882a9-105">Possible values for firewallCertificateRevocationListCheckMethod</span></span>
## <a name="members"></a><span data-ttu-id="882a9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="882a9-106">Members</span></span>
|<span data-ttu-id="882a9-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="882a9-107">Member</span></span>|<span data-ttu-id="882a9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="882a9-108">Value</span></span>|<span data-ttu-id="882a9-109">Description</span><span class="sxs-lookup"><span data-stu-id="882a9-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="882a9-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="882a9-110">deviceDefault</span></span>|<span data-ttu-id="882a9-111">0</span><span class="sxs-lookup"><span data-stu-id="882a9-111">0</span></span>|<span data-ttu-id="882a9-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="882a9-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="882a9-113">none</span><span class="sxs-lookup"><span data-stu-id="882a9-113">none</span></span>|<span data-ttu-id="882a9-114">1</span><span class="sxs-lookup"><span data-stu-id="882a9-114">1</span></span>|<span data-ttu-id="882a9-115">No comprobar la lista de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="882a9-115">Do not check certificate revocation list</span></span>|
|<span data-ttu-id="882a9-116">intento de</span><span class="sxs-lookup"><span data-stu-id="882a9-116">attempt</span></span>|<span data-ttu-id="882a9-117">2</span><span class="sxs-lookup"><span data-stu-id="882a9-117">2</span></span>|<span data-ttu-id="882a9-118">Intente la comprobación de CRL y permitir que un certificado sólo si el certificado está confirmado por la comprobación de</span><span class="sxs-lookup"><span data-stu-id="882a9-118">Attempt CRL check and allow a certificate only if the certificate is confirmed by the check</span></span>|
|<span data-ttu-id="882a9-119">requerir</span><span class="sxs-lookup"><span data-stu-id="882a9-119">require</span></span>|<span data-ttu-id="882a9-120">3</span><span class="sxs-lookup"><span data-stu-id="882a9-120">3</span></span>|<span data-ttu-id="882a9-121">Requerir una comprobación CRL correcta antes de permitir que un certificado</span><span class="sxs-lookup"><span data-stu-id="882a9-121">Require a successful CRL check before allowing a certificate</span></span>|



