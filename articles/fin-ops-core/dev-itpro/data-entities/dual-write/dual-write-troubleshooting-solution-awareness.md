---
title: Trikčių, susijusių su sprendimo supratimu, šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su sprendimo supratimu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 7f1a6e424996201ecae1b624c13cfc573745dc0a
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997283"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Trikčių, susijusių su sprendimo supratimu, šalinimas

[!include [banner](../../includes/banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su sprendimo supratimu.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="error-on-the-dual-write-page"></a>Dvigubo rašymo funkcijos puslapyje įvyko klaida

**Dvigubo rašymo** funkcijos puslapyje galite gauti klaidos pranešimų, panašių į toliau pateiktą pavyzdį:

*Objektas pavadinimu 'msdyn\_dualwriteentitymap' su namemapping='Logical' nebuvo rastas MetadataCache.*

Norėdami išspręsti šią problemą, įsitikinkite, kad „Common Data Service” įdiegtas dvigubo rašymo funkcijos pagrindinis sprendimas. Dvigubo rašymo funkcijos pagrindinis sprendimas yra būtinas siekiant suprasti sprendimą.
