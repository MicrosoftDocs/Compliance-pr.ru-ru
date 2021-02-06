---
title: Элементы управления доступом microsoft 365 yammer для предприятий
description: В этой статье содержится краткая сводка по средствам контроля корпоративного доступа Yammer в производственной среде.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120368"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="fde26-103">Элементы управления доступом yammer для предприятий</span><span class="sxs-lookup"><span data-stu-id="fde26-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="fde26-104">Физический и логический доступ к производственной среде Yammer ограничен небольшим набором людей (инфраструктурой и операциями).</span><span class="sxs-lookup"><span data-stu-id="fde26-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="fde26-105">Как и другие инженеры Microsoft 365, инженеры Yammer не имеют постоянного доступа к данным клиентов.</span><span class="sxs-lookup"><span data-stu-id="fde26-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="fde26-106">Доступ необходимо запрашивать с помощью системы управления доступом на основе утверждения, аналогичной системе управления доступом на основе утверждения, аналогичной системе lockbox с ограниченным количеством утвержденных.</span><span class="sxs-lookup"><span data-stu-id="fde26-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="fde26-107">Утвержденные проверяют запрос (например, проверяют, является ли запрос допустимым в зависимости от необходимости, бизнес-дела, времени и т. д.), а затем утверждают или отоают запрос.</span><span class="sxs-lookup"><span data-stu-id="fde26-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="fde26-108">Если запрос утвержден, доступ к JIT предоставляется в течение определенного и ограниченного времени.</span><span class="sxs-lookup"><span data-stu-id="fde26-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="fde26-109">После превышения времени доступа срок действия доступа автоматически истекает.</span><span class="sxs-lookup"><span data-stu-id="fde26-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="fde26-110">Как и в других службах Microsoft 365, для доступа к производственной среде Yammer используется многофакторная проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="fde26-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="fde26-111">Весь доступ и история команд связаны с пользователем и регулярно регистрируются и просматриваются командой безопасности Yammer.</span><span class="sxs-lookup"><span data-stu-id="fde26-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="fde26-112">Дополнительные сведения об администрировании и управлении Yammer см. в справке для [администраторов Yammer.](/yammer/yammer-landing-page)</span><span class="sxs-lookup"><span data-stu-id="fde26-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>