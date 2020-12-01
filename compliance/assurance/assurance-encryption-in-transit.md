---
title: Шифрование для транзитного обмена данными
description: В этой статье приводится краткое описание того, как корпорация Майкрософт шифрует данные клиентов корпорации Майкрософт 365 в транзитном месте.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d1587e4bc315f99dc554158500638645606fbcec
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507874"
---
# <a name="encryption-for-data-in-transit"></a>Шифрование для транзитного обмена данными

Помимо защиты данных клиентов, корпорация Майкрософт использует технологии шифрования для защиты данных клиентов при их транзитном переносе. Данные находятся в пути:

- Когда клиентский компьютер обменивается данными с сервером Microsoft;
- при взаимодействии Microsoft Server с другим сервером корпорации Майкрософт; с
- Когда сервер Microsoft Exchange взаимодействуют с сервером, отличным от Microsoft (например, Exchange Online доставляет электронную почту на сторонний сервер электронной почты).

Обмен данными между центрами обработки данных между серверами Майкрософт выполняется по протоколу TLS или IPsec, а все серверы, подключенные к клиентам, согласовывают безопасный сеанс с помощью протокола TLS с клиентскими компьютерами (например, Exchange Online использует протокол TLS 1,2 с 256-разрядным шифром) (проверка подлинности FIPS 140-2 уровня 2). (См. [технические сведения о шифровании](https://docs.microsoft.com/microsoft-365/compliance/technical-reference-details-about-encryption) список комплектов шифров TLS, поддерживаемых Office 365.) Это относится к протоколам, используемым клиентами, таким как Outlook, Skype для бизнеса, Microsoft Teams и Outlook в Интернете (например, HTTP, POP3 и т. д.).

Общедоступные сертификаты выдаются по протоколу Microsoft IT SSL с помощью Ссладмин, внутреннего средства Майкрософт для защиты конфиденциальности передаваемых данных. Все сертификаты, выданные корпорацией Майкрософт, имеют значение не менее 2048 бит, а для обеспечения соответствия требованиям Вебтруст требуется Ссладмин, чтобы сертификаты выдавались только общедоступным IP-адресам, принадлежащим корпорации Майкрософт. Все IP-адреса, которые не удовлетворяют этому критерию, направляются через процесс исключения.

Все детали реализации, такие как используемая версия протокола TLS, включена ли функция пересылки безопасной (Федерации), порядок комплектов шифров и т. д. доступно в открытых источниках. Одним из способов просмотра этих сведений является использование стороннего веб-сайта, например [куалис](https://www.ssllabs.com). Ниже приведены ссылки на страницы автоматизированного теста из Куалис, отображающие сведения о следующих службах:

- [Портал Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype для бизнеса (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype для бизнеса (Интернет)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Для Exchange Online Protection URL-адреса различаются в зависимости от имен клиентов; Тем не менее, все клиенты могут тестировать Microsoft 365 с помощью **Microsoft-COM.mail.Protection.Outlook.com**.
