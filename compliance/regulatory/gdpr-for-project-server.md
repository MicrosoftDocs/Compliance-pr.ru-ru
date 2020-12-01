---
title: GDPR для Project Server
description: Узнайте, как обеспечить соблюдение требований общего регламента по защите данных (GDPR) в локальном развертывании Project Server.
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
ms.openlocfilehash: 5f753b5d522649575f92178e6f9c932d5ae4725f
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/30/2020
ms.locfileid: "49509004"
---
# <a name="gdpr-for-project-server"></a><span data-ttu-id="8f3df-103">GDPR для Project Server</span><span class="sxs-lookup"><span data-stu-id="8f3df-103">GDPR for Project Server</span></span>

<span data-ttu-id="8f3df-p101">Project Server использует специальные скрипты для экспорта и редактирования данных пользователя в Project Web App. Ниже описывается базовый процесс.</span><span class="sxs-lookup"><span data-stu-id="8f3df-p101">Project Server uses custom scripts to export and redact user data in Project Web App. The basic process is:</span></span>

1.  <span data-ttu-id="8f3df-106">Найдите сайты Project Web App в ферме.</span><span class="sxs-lookup"><span data-stu-id="8f3df-106">Find the Project Web App sites in your farm.</span></span>

2.  <span data-ttu-id="8f3df-107">Найдите на каждом сайте проекты, содержащие данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f3df-107">Find the projects in each site that contain the user.</span></span>

3.  <span data-ttu-id="8f3df-108">Экспортируйте и просмотрите нужные типы данных.</span><span class="sxs-lookup"><span data-stu-id="8f3df-108">Export and review the types of data that you want to review.</span></span>

4.  <span data-ttu-id="8f3df-109">Отредактируйте данные надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="8f3df-109">Redact data as needed.</span></span>

<span data-ttu-id="8f3df-110">Эти действия подробно рассматриваются в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="8f3df-110">These steps are covered in detail in the following articles:</span></span>

- [<span data-ttu-id="8f3df-111">Экспорт данных пользователя из Project Server</span><span class="sxs-lookup"><span data-stu-id="8f3df-111">Export user data from Project Server</span></span>](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [<span data-ttu-id="8f3df-112">Удаление данных пользователя из Project Server</span><span class="sxs-lookup"><span data-stu-id="8f3df-112">Delete user data from Project Server</span></span>](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


<span data-ttu-id="8f3df-p102">Обратите внимание, что Project Server основан на SharePoint Server и регистрирует события в журналах ULS SharePoint и базе данных использования. Дополнительные сведения см. в статье [GDPR для SharePoint Server](gdpr-for-sharepoint-server.md).</span><span class="sxs-lookup"><span data-stu-id="8f3df-p102">Note that Project Server is built on top of SharePoint Server and logs events to the SharePoint ULS logs and Usage database. See [GDPR for SharePoint Server](gdpr-for-sharepoint-server.md) for more information.</span></span>
