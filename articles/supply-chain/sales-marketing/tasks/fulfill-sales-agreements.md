---
title: Pardavimo sutarčių vykdymas
description: Ši procedūra nurodo, kaip įvykdyti pardavimo sutartį, su ja susiejus pardavimo užsakymus.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fca2f8777f5ce3b6a96be7fcab4f011aefd9d80b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991769"
---
# <a name="fulfill-sales-agreements"></a>Pardavimo sutarčių vykdymas

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip įvykdyti pardavimo sutartį, su ja susiejus pardavimo užsakymus. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Prieš paleisdami šį vadovą, įsitikinkite, kad turite galiojančią „Produkto vertės įsipareigojimas“ tipo pardavimo sutartį. Taip pat galite paleisti užduočių vadovą, pavadintą „Kurti pardavimo sutartis“.  




## <a name="release-a-sales-order-from-the-agreement"></a>Išleisti pardavimo užsakymą iš sutarties
1. Eikite į Pardavimas ir rinkodara > Pardavimo sutartys > Pardavimo sutartys.
2. Sąraše atidarykite sutartį, pagal kurią norite išleisti užsakymą.
3. Srityje Veiksmas spustelėkite Pardavimo sutartis.
4. Spustelėkite išleidimo užsakymas.
    * Kaip nurodo tekstas puslapio Kurti paleidimo viršuje, informacija, reikalinga pardavimo užsakymo eilutėse skirsis atsižvelgiant į tai, ar sutartis yra pagrįsta kiekiu ar verte.  
    * Šiame vadove pateikiamos sutarties tipas „Produkto vertės įsipareigojimas“. Todėl šio puslapio skyrius Eilutės yra tuščias. Jei įsipareigojimas pagrįstas kiekiu, eilutės informacija nukopijuojama iš sutarties.  
5. Spustelėkite Kurti.
    * Pranešimas informuoja, kad pardavimo užsakymas sukurtas. Kadangi užsakyme eilučių nėra, turite įtraukti užsakymo eilučių informaciją, norėdami užbaigti išleidimo procesą.   
6. Uždarykite puslapį.
7. Uždarykite puslapį.
8. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
9. Sąraše raskite ir atidarykite užsakymą, kuris ankstesnėje užduotyje buvo sukurtas kaip užsakymo išleidimo rezultatas.
10. Spustelėkite Pridėti eilutę.
11. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
12. Lauke Prekės numeris, įveskite arba pasirinkite prekę, kuri nurodyta susijusioje pardavimo sutartyje.
13. Lauke Kiekis įveskite skaičių.
    * Įsitikinkite, kad įvedate kiekį, su kuriuo grynoji suma bus mažesnė nei susijusios pardavimo sutarties vertė.  
    * Atkreipkite dėmesį, kad dėl to, jog pardavimo užsakymas yra susietas su sutartimi, sutartas nuolaidos procentas taikomas užsakymo eilutei.  
14. Spustelėkite eilutę „Atnaujinti“.
15. Spustelėkite „Pridėta“.
    * Puslapyje Pridėta sutartis rodomas ID ir sutarties, iš kurios eilutė išleista, sąlygos.  
16. Uždarykite puslapį.
17. Veiksmų srityje spustelėkite Bendra.
18. Spustelėkite Pridėta pardavimo sutartis.
19. Išplėskite skyrių Eilutės informacija.
20. Spustelėkite skirtuką Įvykdymas.
    * Skirtuke Įvykdymas rodoma suvestinė visų pardavimo užsakymo eilučių, kurios susietos su šiuo įsipareigojimo, jų įvykdymo būsena ir suma arba kiekis, kuris dar nepaleistas.   
21. Uždarykite puslapį.
22. Uždarykite puslapį.
23. Uždarykite puslapį.

## <a name="apply-sales-agreement-in-the-order-process"></a>Taikyti pardavimo sutartį užsakymo procese
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite klientą, nurodyta pardavimo sutartyje.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite skyrių Bendra.
7. Lauke Pardavimo sutarties ID spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Spustelėkite Taip.
10. Spustelėkite GERAI.
11. Sąraše pažymėkite pasirinktą eilutę.
12. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
13. Lauke Prekės numeris, įveskite arba pasirinkite prekę, kuri nurodyta susijusioje pardavimo sutartyje.
14. Sąraše spustelėkite saitą pasirinktoje eilutėje.
15. Spustelėkite Įrašyti.
16. Veiksmų srityje spustelėkite Paimti ir pakuoti.
17. Spustelėkite Registruoti važtaraštį.
18. Išplėskite skyrių Parametrai.
19. Lauke Registravimas pasirinkite Taip.
20. Spustelėkite GERAI.
21. Spustelėkite GERAI.
22. Veiksmų srityje spustelėkite Bendra.
23. Spustelėkite Pridėta pardavimo sutartis.
24. Spustelėkite skirtuką Įvykdymas.

