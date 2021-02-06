---
title: GDPR для локальных общих папок
description: Узнайте, как обеспечить соблюдение требований Общего регламента по защите данных (GDPR) в локальных общих папках Windows Server.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
ms.openlocfilehash: 6a6b1fdeac71bfcca68391cbc10ec75be0e18410
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121888"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a><span data-ttu-id="94a74-103">GDPR для локальных общих папок Windows Server</span><span class="sxs-lookup"><span data-stu-id="94a74-103">GDPR for on-premises Windows Server file shares</span></span>

<span data-ttu-id="94a74-104">Основной рекомендуемый подход для общих папок:</span><span class="sxs-lookup"><span data-stu-id="94a74-104">The basic recommended approach for file shares is:</span></span>

-   <span data-ttu-id="94a74-105">Используйте Azure Information Protection для пометки конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="94a74-105">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="94a74-106">Используйте сканер Azure Information Protection для поиска данных.</span><span class="sxs-lookup"><span data-stu-id="94a74-106">Use Azure Information Protection scanner to find data.</span></span>

<span data-ttu-id="94a74-107">Рекомендуемый подход для общих папок включает следующие действия:</span><span class="sxs-lookup"><span data-stu-id="94a74-107">The recommended approach for files shares includes these steps:</span></span>

1.  <span data-ttu-id="94a74-108">**Установите и настройте сканер Azure Information Protection.**</span><span class="sxs-lookup"><span data-stu-id="94a74-108">**Install and configure Azure Information Protection scanner.**</span></span>

    -   <span data-ttu-id="94a74-109">Выберите необходимые типы конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="94a74-109">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="94a74-110">Укажите необходимые локальные и сетевые папки.</span><span class="sxs-lookup"><span data-stu-id="94a74-110">Specify local folders and network shares to use.</span></span>

2.  <span data-ttu-id="94a74-111">**Выполните цикл обнаружения.**</span><span class="sxs-lookup"><span data-stu-id="94a74-111">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="94a74-112">Запустите сканер в режиме обнаружения и проверьте обнаруженные данные.</span><span class="sxs-lookup"><span data-stu-id="94a74-112">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="94a74-113">При необходимости оптимизируйте условия и типы конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="94a74-113">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="94a74-114">Оцените ожидаемое воздействие автоматического применения меток.</span><span class="sxs-lookup"><span data-stu-id="94a74-114">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="94a74-115">**Запустите сканер Azure Information Protection для применения меток к соответствующим документам**.</span><span class="sxs-lookup"><span data-stu-id="94a74-115">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="94a74-116">**Для защиты:**</span><span class="sxs-lookup"><span data-stu-id="94a74-116">**For protection:**</span></span>

    -   <span data-ttu-id="94a74-117">Настройте правила защиты от потери данных в Exchange, чтобы защитить документы с нужной меткой.</span><span class="sxs-lookup"><span data-stu-id="94a74-117">Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    -   <span data-ttu-id="94a74-118">Обязательно используйте разрешения, чтобы ограничить доступ к файлам.</span><span class="sxs-lookup"><span data-stu-id="94a74-118">Be sure to use permissions to limit who can access files.</span></span>

5.  <span data-ttu-id="94a74-119">**Интегрируйте журналы Windows Server со средством SIEM для мониторинга.**</span><span class="sxs-lookup"><span data-stu-id="94a74-119">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    -   <span data-ttu-id="94a74-p101">Чтобы находить персональные данные для запросов субъектов данных, используйте сканер Azure Information Protection. Вы также можете включить обход общих папок в настройках поиска SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="94a74-p101">To find personal data for data subject requests, use Azure Information Protection scanner. You can also configure SharePoint Server search to crawl file shares.</span></span>

<span data-ttu-id="94a74-122">Дополнительные сведения об использовании сканера Azure Information Protection для поиска и пометки персональных данных см. в разделе [Развертывание сканера AIP](/azure/information-protection/deploy-aip-scanner).</span><span class="sxs-lookup"><span data-stu-id="94a74-122">For more information on using Azure Information Protection scanner to find and label personal data, see [Deploy AIP Scanner](/azure/information-protection/deploy-aip-scanner).</span></span>

<span data-ttu-id="94a74-p102">Сведения о настройке сканера в соответствии с условиями и использовании типов конфиденциальной информации для защиты от потери данных (DLP) в Office 365 см. в статье [Как настроить условия для автоматической и рекомендуемой классификации с помощью Azure Information Protection](/information-protection/deploy-use/configure-policy-classification). Обратите внимание, что новые типы конфиденциальной информации Office 365 не сразу станут доступны для использования в сканере. Кроме того, в нем невозможно использовать пользовательские типы конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="94a74-p102">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>
