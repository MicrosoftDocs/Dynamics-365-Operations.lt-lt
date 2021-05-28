---
title: Sandėlio paketo ir serijos rezervavimo hierarchijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti dažnas klaidas, su kuriomis galite susidurti dirbdami su rezervavimo hierarchijomis, naudojančiomis paketo arba serijos dimensijas.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022551"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Sandėlio paketo ir serijos rezervavimo hierarchijų trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti dažnas klaidas, su kuriomis galite susidurti dirbdami su rezervavimo hierarchijomis, naudojančiomis paketo arba serijos dimensijas.

Dėl išsamesnės informacijos, žr. [Lanksti sandėlio lygmens matmenų rezervacijos politika](flexible-warehouse-level-dimension-reservation.md).

Prekės rezervavimo hierarchija diktuoja saugojimo dimensijų, kurios turi būti užpildytos poreikio užsakymo vietos priskyrimui, reikalavimą. Šios dimensijos gali būti apibūdinamos kaip *dimensijos aukščiau vietos* visoms dimensijoms, kurios turi būti užpildytos prieš priskiriant vietą, ir *dimensijos žemiau vietos* toms dimensijoms, kurios gali būti paskirstytos po to, kai poreikio užsakymui buvo priskirta vieta. Šios rezervavimo hierarchijos taip pat žinomos kaip *paketas aukščiau* ir *paketas žemiau* rezervavimo hierarchijos arba *serija aukščiau* ir *serija žemiau* rezervavimo hierarchijos.

Atsargas galima sėkmingai paskirstyti tik tada, jei dimensijose aukščiau vietos nėra tarpų. Pavyzdžiui, rezervavimo hierarchijoje *paketas aukščiau* tikitės, jog dimensijos **Saitas,** **Sandėlis** ir **Paketo numeris** bus nurodytos poreikio užsakyme. Jeigu trūksta bet kurios iš šių dimensijų, paskirstymo procesas nepavyks. Priešingai, *paketas žemiau* ar *serija žemiau* rezervavimo hierarchijoje paketo arba serijos numeris gali būti nurodytas poreikio užsakyme, tačiau jis nebūtinas paskirstymo procesui.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Gaunu tolesnį klaidos pranešimą: „Tam kad būtų priskirtos prie bangos, krovinio eilutės turi nurodyti dimensijas virš vietos. Norėdami priskirti šias dimensijas, rezervuokite ir iš naujo sukurkite krovinio eilutę."

### <a name="issue-description"></a>Problemos aprašas

Jums naudojant prekę, turinčią *paketas aukščiau* rezervavimo hierarchiją, puslapyje **Krovinio planavimo darbo sritis** esanti komanda **Išleisti į sandėlį** neveikia, jeigu bandote išleisti krovinį daliniam kiekiui. Gaunate šį klaidos pranešimą ir joks darbas nesukuriamas daliniam kiekiui.

Tačiau, kai naudojate prekę, turinčią *paketas žemiau* rezervavimo hierarchiją, galite išleisti krovinį daliniam kiekiui iš **Krovinio planavimo darbo srities** puslapio.

### <a name="issue-cause"></a>Problemos priežastis

Kai dimensija yra virš **Vietos** dimensijos rezervacijos hierarchijoje, ji turi būti nurodytas prieš išleidimą į sandėlį. Daliniai kiekiai negali būti išleisti, jei viena ar kelios dimensijos virš **Vietos** nenurodyti.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Automatinio rezervavimo raginimas įvesti paketo numerį yra suaktyvinamas, net jei yra galimų atsargų.

### <a name="issue-description"></a>Problemos aprašas

Kai naudojate prekę, turinčią *paketas aukščiau* rezervavimo hierarchiją sandėlyje, kuriame neįgalinti sandėlio procesai ir įgalintas automatinis rezervavimas, yra rodomas automatinio rezervavimo raginimas įvesti paketo numerį, net jeigu tik vienas paketas yra galimas paėmimui.

Tačiau, kai naudojate tą pačią prekę sandėlyje, kuriame įgalinti sandėlio procesai, automatinio rezervavimo raginimas nėra rodomas.

### <a name="issue-cause"></a>Problemos priežastis

Jei rezervavimo hierarchija apibrėžta kaip *paketas aukščiau* ar *serija aukščiau*, nurodyta dimensija (**Paketo numeris** arba **Serijos numeris**) visada turi būti nurodyta poreikio užsakymuose. Sandėlio procesai gali sugebėti užpildyti informaciją, jei yra vienas paketas ar serijos numeris. Tačiau, kadangi sandėlis nėra įgalintas sandėlio procesams, vartotojas visada turi nurodyti visas dimensijas, esančias virš **Vietos**.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Intervalo šablonai, turintys atsižvelgti į turimas atsargas intervalo kriterijų, neatsižvelgia į dabartines turimas atsargas, skirtas įjungto paketo prekėms.

Daugiau informacijos rasite [Sandėlio intervalas](warehouse-slotting.md).

### <a name="issue-description"></a>Problemos aprašas

Intervalo šablonai, turintys *Atsižvelgti į turimas atsargas* intervalo kriterijų, neatsižvelgia į dabartines turimas atsargas, skirtas *paketas aukščiau* prekėms. Jie atsižvelkite į jas tik tuo atveju, jei pardavimo užsakymo eilutėje nurodytas paketo numeris.

Tačiau, kai naudojate *paketas žemiau* prekes, laikoma, kad dabartinės turimos atsargos yra tikėtinos.

### <a name="issue-cause"></a>Problemos priežastis

Intervalo šablono antraštę galima nurodyti *Užsakyta*, *Rezervuota* arba *Išleista* poreikio strategijoms. Poreikio strategijai *Užsakyta* taikomi tie patys rezervavimo hierarchijos reikalavimai, kurie taikomi ir rezervavimo arba išleidimo į sandėlio procesams. Todėl prekių, turinčių *paketas aukščiau* ir *serija žemiau* rezervavimo hierarchijas, poreikio užsakyme (pardavimo arba perkėlimo) turi būti nurodytas paketo arba serijos numeris. Taip pat, galima naudoti poreikio strategiją *Rezervuota* pasirinkti paketo arba serijos numerį prieš generuojant sandėlio intervalo poreikį.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
