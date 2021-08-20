---
title: Mokėjimų priežiūros nustatymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti mokėjimų priežiūros funkcijas.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2e06da265271e2148804c51abc7cd9ffc29a3e20e73dda3a1a23966f0e6586e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769823"
---
# <a name="set-up-collections"></a>Mokėjimų priežiūros nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti mokėjimų priežiūros funkcijas. Kai naudojatės mokėjimais, turite užbaigti kai kuriuos priežiūros nustatymo veiksmus. Taip pat yra tam tikrų pasirinktinių galimybių, įskaitant klientų telkinius ir mokėjimų priežiūros komandas. 

- Skirstymo pagal terminus laikotarpio apibrėžimai
- Skirstymo pagal terminus momentinės kopijos
- Žurnalų pavadinimai
- Nurašymo operacijų priežasties kodas
- Mokėjimų priežiūros agentai
- Nurašymo sąskaita
- Informacija apie lėšų trūkumą
- „Outlook“ nuostatos puslapio **Mokėjimai** naudotojams
- El. pašto adresai

Šie punktai išsamiau aptariami likusioje šios temos dalyje. 

## <a name="set-up-aging-period-definitions"></a>Nustatyti skirstymo pagal terminus laikotarpių apibrėžimus

Nustatykite skirstymo pagal terminus laikotarpio apibrėžtį. Skirstymo pagal terminus laikotarpio apibrėžtis apibrėžia stulpelius, kurie rodomi **Pagal terminus suskirstytų balansų**, **Surinkimo veiklų** ir **Surinkimo atvejų** sąrašo puslapiuose. Ji taip pat apibrėžia laikotarpius, kurie rodomi **Surinkimo** puslapyje. Jei nustatytas klientų telkinys, naudojamas telkiniui skirtas skirstymo pagal terminus laikotarpis. Jei telkiniai nenustatyti, naudojama numatytoji skirstymo pagal terminus laikotarpio apibrėžtis, nurodyta puslapyje **Gautinų sumų parametrai**. Jei nenurodyta jokia numatytoji skirstymo pagal terminus laikotarpio apibrėžtis, naudojama pirmoji puslapyje **Skirstymo pagal terminus laikotarpio apibrėžtys** nurodyta skirstymo pagal terminus laikotarpio apibrėžtis.

## <a name="create-an-aging-snapshot"></a>Skirstymo pagal terminus momentinės kopijos kūrimas
Sukurkite skirstymo pagal terminus momentinės kopijos įrašus visiems klientams arba klientams, esantiems klientų telkinyje. Skirstymo pagal terminus momentinės kopijos informacija rodoma **Pagal terminus suskirstytų balansų** sąrašo puslapyje ir **Surinkimo** puslapyje. Prieš naudodami sąrašo puslapį turite sukurti skirstymo pagal laikotarpius momentinę kopiją. Sąrašo puslapyje informacija rodoma tik tiems klientams, kuriems buvo sukurta skirstymo pagal terminus momentinė kopija.

## <a name="optional-set-up-customer-pools"></a>Pasirinktinai: nustatyti klientų telkinius
Galite nustatyti klientų telkinius, kurie atitinka klientų grupes. Galite naudoti klientų telkinius kaip kliento informacijos, rodomos **Surinkimo** sąrašo puslapiuose, puslapyje **Surinkimas** arba kuriant skirstymo pagal terminus momentines kopijas, filtrus.

## <a name="optional-create-a-collections-team"></a>Pasirinktinai: kurti mokėjimų priežiūros komandą
Jei jūsų organizacijoje keli žmonės užsiima mokėjimų priežiūra, galite nustatyti mokėjimų priežiūros komandą. Komandą galite pasirinkti **Gautinų sumų parametrų** puslapyyje. Jei nesukuriate surinkimo komandos, ji sukuriama automatiškai, kai puslapyje **Surinkimo agentas** nustatote surinkimo agentus.

## <a name="set-up-a-collections-case-category"></a>Nustatyti mokėjimų priežiūros atvejo kategoriją
Norėdami organizuoti mokėjimų priežiūros komandos darbą naudodami atvejus, nustatykite atvejo kategorijos tipą **Mokėjimai**. Šios sąrankos reikia tik jei puslapyje **Mokėjimai** norite naudoti atvejų funkcijas.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Nustatyti žurnalų pavadinimus (atsiskaitymas, nurašymas ir NSF)
Nustatykite žurnalų pavadinimus, kurie naudojami, kai **Surinkimo** puslapyje apdorojamos operacijos. Šis apdorojimas apima operacijos sudengimą, operacijos nurašymą ir lėšų trūkumo (NSF) mokėjimo apdorojimą.

| Aprašymas | Žurnalo tipas     |
|-------------|------------------|
| Atsiskaitymas  | Kliento mokėjimas |
| Nurašymas   | Kasdienis            |
| NSF         | Kliento mokėjimas |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Nustatyti nurašymo operacijų priežasties kodą
Nustatykite numatytąjį priežasties kodą, naudojamą, kai **Surinkimo** puslapyje nurašomos operacijos. Kodą galite keisti nurašymo proceso metu.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Nustatyti el. pašto priedų aplanką ir kurti el. laiškų šablonus
Jei puslapio **Surinkimas** siųsite el. laiškus su „Microsoft Excel“ priedais, tokiems laiškams galite sukurti pasirinktinių el. laiškų šablonų.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Nustatyti gautinų sumų parametrus, taikomus surinkimui
Nustatykite gautinų sumų parametrus, rodomus **Surinkimo** skirtuke.

## <a name="optional-set-up-collections-agents"></a>Pasirinktinai: nustatyti mokėjimų priežiūros agentus
Jei jūsų organizacijoje keli žmonės užsiima mokėjimų priežiūra, galite nustatyti mokėjimų priežiūros agentus. Surinkimo agentas yra darbuotojas, kuris yra nustatytas kaip naudotojas puslapyje **Naudotojų ryšiai**. Galite surinkimo agentams priskirti klientų telkinius, (klientų užklausas), kad jiems padėtumėte organizuoti savo darbą. Surinkimo agentai pridedami į komandą, kuri pasirenkama **Gautinų sumų parametrų** puslapyje. Jei tame puslapyje komanda nepasirenkama, automatiškai sukuriama nauja komanda pavadinimu **Surinkimas** ir į šią komandą pridedami surinkimo agentai.

## <a name="set-up-a-writeoff-account"></a>Nustatyti nurašymo sąskaitą
Nustatykite nurašymo sąskaitą, kuri bus naudojama didžiosios knygos nurašymo įraše nurašius operaciją. Ši sąskaita yra saugoma kliento registravimo profilyje.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Nustatyti banko sąskaitų NSF informaciją
Atnaujinkite banko sąskaitas, kad jos naudotų tinkamą žurnalą, kai **Surinkimo** puslapyje identifikuojami NSF mokėjimai. **Valiutos valdymo** skirtuke, **NSF mokėjimų žurnalo** lauke pasirinkite mokėjimų žurnalą.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Nustatyti „Outlook“ nuostatas puslapio Surinkimas naudotojams
Kad darbuotojai galėtų kurti operacijas arba siųsti el. laiškus naudodami puslapį **Surinkimas**, turite patikrinti, ar pasirinktas **„Microsoft Outlook“ sinchronizavimo** konfigūracijos raktas ir ar tie darbuotojai gali naudotis „Outlook“ sinchronizavimo funkcija.

## <a name="set-up-email-and-addresses"></a>El. pašto adreso ir adresų nustatymas
Norėdami susisiekti su klientais ir pardavėjais dėl mokėjimų problemų, galite naudoti el. paštą ir siųsti el. laiškus iš puslapio **Mokėjimai**. 

### <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Nustatyti el. pašto adreso parametrus, taikomus mokėjimų priežiūros klientų kontaktams
Nustatykite kliento kontaktų el. pašto adresus, kad galėtumėte siųsti el. laiškus tiems kontaktams iš puslapio **Mokėjimai**. Surinkimo kontaktas yra naudojamas kaip numatytasis kontaktas puslapyje **Surinkimas**. Galite nustatyti klientui skirtą išrašo gavimo adresą, jei išrašų adresas turi skirtis nuo pagrindinio adreso. 

Kliento **Kredito ir surinkimo** „FastTab‟, **Surinkimo kontakto** lauke pasirinkite kliento organizacijos asmenį, kuris dirba su jūsų surinkimo agentu. Šis asmuo yra naudojamas kaip numatytasis kontaktas puslapyje **Surinkimas** ir jam siunčiami el. laiškai. 

> [!NOTE] 
> Jei kliento surinkimo kontaktas nenurodytas, naudojamas pagrindinis kliento kontaktas. Jie pagrindinis kontaktas nenurodytas, el. laiškai siunčiami pirmu puslapyje **Kontaktai** nurodytu adresu.

### <a name="set-up-email-settings-for-salespeople"></a>Nustatyti el. pašto parametrus, taikomus pardavėjams
Nustatykite pardavėjų el. pašto adresus, kad galėtumėte siųsti el. laiškus pardavėjams iš puslapio **Mokėjimai**. Nustatykite kiekvieno pardavimo atstovo el. paštą adresą kiekvienoje pardavimo komisinių grupėje. Pardavimo atstovas, prie kurio pasirinkta parinktis **Kontaktas**, yra numatytasis pardavėjas, kuriam siunčiami el. laiškai. 

Jei pardavimo atstovas nenurodytas, naudojamas pagrindinis kliento organizacijos pardavėjas. Jei pagrindinis pardavėjas nenurodytas, el. laiškai siunčiami pirmam puslapyje nurodytam pardavėjui.


Daugiau informacijos ieškokite šiose temose:

 - [Kurti priminimo laiškų seką](tasks/create-collection-letter-sequence.md)

 - [Apdoroti priminimo laiškus](tasks/process-collection-letters.md)

 - [Peržiūrėti mokėjimų priežiūros informaciją](tasks/review-collections-information.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]