---
title: Atsargų perkėlimas su susietu darbu modulyje Sandėlio valdymas
description: Naudodami atsargų judėjimą, galite nuspręsti, kuriems sandėlio darbininkams leidžiama perkelti rezervuotas atsargas.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d996886a90037f288e839c54c8c9d932cabb21f19f2aef1552ca82b192c96a51
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736556"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Atsargų perkėlimas su susietu darbu modulyje Sandėlio valdymas

[!include [banner](../includes/banner.md)]

Naudodami atsargų judėjimą, galite nuspręsti, kuriems sandėlio darbininkams leidžiama perkelti rezervuotas atsargas. Tai suteikia lankstumo reguliuojamuosiuose sandėliuose, kuriuose galite nuspręsti neleisti darbininkui pasirinkti naujos paėmimo darbo paėmimo vietos, kuri jau sukurta. Tai taip pat suteikia sandėlio vadovui galimybę kontroliuoti, kokias galimybes turėtų turėti mažiau patyrę darbininkai.

Lanksčiau valdyti sandėlio darbininkų kasdienes operacijas gali būti naudinga tokiais atvejais:

## <a name="scenario-1"></a>1 scenarijus

Įmonė turi gana nedidelę gavimo sritį, kuri perpildyta padėklais ir dėžėmis, kurios turi būti atidėtos. Šią dieną laukiama didelės siuntos, todėl gaunamų prekių klerkas nusprendžia išvalyti gavimo sritį perkeliant dalį padėklų į antrinę gavimo išdėstymo sritį.

## <a name="scenario-2"></a>2 scenarijus

Patyręs sandėlio darbininkas pastebi sandėlyje galimybę konsoliduoti prekes vienoje vietoje, užuot jas išskirsčius mažais kiekiais į tris vietas netoliese. Darbininkas nori konsoliduoti kiekį perkeldamas prekes iš kiekvienos iš šių vietų į tą pačią vietą ir naudojant tą pačią numerio lentelę.

## <a name="scenario-3"></a>3 scenarijus

Padėklas laukia siuntos išdėstymo vietoje, pvz., STAGE01, kuri yra netoli BAYDOOR01. Tačiau, pasikeitus planams, suplanuotas sunkvežimio atvykimas į BAYDOOR04. Siunčiantis klerkas tai žino ir turi užtikrinti, kad sunkvežimiui nereikėtų laukti, kol bus pakrautas iš STAGE01. Siunčiantis klerkas nusprendžia perkelti tos siuntos prekes iš STAGE01 į STAGE04, kuri yra arčiau naujosios paskirties vietos.

### <a name="current-limitations"></a>Dabartiniai apribojimai

Darbo rezervavimai, kuriuos galite perkelti, yra pardavimo užsakymas, perkėlimo užsakymo išdavimas, perkėlimo užsakymo gavimas, pirkimo užsakymas ir papildymo darbas.

Prekių perkėlimas yra apribotas siekiant išvengti darbo eilučių skaidymo. Tai reiškia, kad jei turite darbo eilutę 100 vnt. A prekių iš vietos Loc1, negalėsite perkelti tik 30 vnt. A prekių iš tos į kitą vietą. Dėl to esama darbo eilutė būtų suskaidyta į 30 ir 70, nes dabar skiriasi vietos.

Išdėstymo scenarijų atveju, kai numerio lentelė, iš kurios perkeliate prekes, arba numerio lentelė, į kurią perkeliate prekes, nustatytos kaip darbo užsakymo paskirties LP, leidžiama perkelti tik visą LP, kad nebūtų padalinta paskirties LP.

Šiuo metu palaikomas tik ad hoc perkėlimas. Tai reiškia, kad negalėsite perkelti rezervuotų atsargų, perkeldami pagal šabloninio mobiliojo įrenginio meniu elementus.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Teisės atskiriems darbininkams perkelti rezervuotas atsargas nustatymas

Darbininkui, kuriam turėtų būti leidžiama perkelti rezervuotas atsargas, pasirinkite žymės langelį **Leisti perkelti su darbu susietas atsargas**, esantį **Sandėlio valdymas \> Sąranka \> Darbininkas**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
