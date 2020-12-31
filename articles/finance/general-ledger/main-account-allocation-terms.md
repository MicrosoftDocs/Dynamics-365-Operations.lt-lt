---
title: Paskirstymo sąlygos
description: Šioje temoje pateikiama informacija apie priskyrtimo sąlygų pagrindinėje paskyroje naudojimą.
author: rachel-profitt
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 637e12f0deaa53811093a8745bc74dbc19e34f6b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445906"
---
# <a name="allocation-terms"></a>Paskirstymo sąlygos

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie priskyrtimo sąlygų pagrindinėje paskyroje naudojimą. Skirstymo sąlygos yra naudojamas skirstyti sumas per daugelį buhalterijos paskyros derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.

Kiekvieno priskyrimo sąlygos, kurias sukuriate pagrindinėje paskyroje nustato kupono procentą, kuris bus priskirtas prie vieno šaltinio pagrindinės paskyros ir finansinių dimensijų derinio. Taip pat, jūs nustatote paskirties pagrindinę paskyrą ir finansines dimensijas, kuriose suma bus priskirta. 

Jums nustatant šaltinio finansines dimensijas priskyrimui, jūs galite pasirinkti kiekvieną konkrečią ar nekonkrečią dimensiją. Konkreti dimensija reiškia, kad finansinė diimensija šaltinio perlaidai turi atitikti pasirinktą dimensiją. Jums pasirinkus nekonkrečią, ji rodo, kad bet kuri vertė finansinei dimensijai gali prisidėti prie atitikmens.

Kai nustatote paskirties buhalterinę paskyrą priskyrimo sąlygai, turite nurodyti pagrindinę paskyrą, kuriai priskiriate sumą. Galite naudoti tą pačią pagrindinę paskyrą, kurioje šaltinio perlaida yra publikuota arba kitą pagrindinę paskyrą. Jei ta pati paskyra yra naudojama, perspėjimas rodomas išsaugant įrašą. Taip pat, siekiant nustatyti pagrindinę paskyrą, jūs taip pat privalote nustatyti paskirties dimensijas. Kiekvienai dimensijai galite nurodyti, ar norite išlaikyti šaltinio finansinės dimensijos vertę ar ją pakeisti. Jei pasirenkate ne, tuomet privalote pasirinkti naują vertę finansinei dimensijai. Jei pasirenkate taip, jokia papildoma informacija yra nenurodoma ir sistema išlaikys originalias finansines dimensijas jums publikuojant.

Nėra jokio paskyrimo sąlygų skaičiaus apribojimo, kurias galite įtraukti į pagrindinę paskyrą; nepaisant to, priskiriamų procentų suma priskyrimo sąlygoje negali viršyti 100. Galite sukurti priskyrimą mažiau nei 100 procentų, jei originalaus kupono sumos dalis turi likti šaltinio finansinėse dimensijose. Priskyrimo sąlygos tuomet gali būti įtraukiamos į pagrindinę paskyrą kaip teisinio subjekto viršijimas. Jei naudojate bendrintą paskyros diagramą, priskyrimo sąlygos turi būti nustatytos kiekvienam teisiniam subjektui. Prieigai prie **Priskyrimo sąlygų** mygtuko, pirmiausia turite pasirinkti **Priskyrimo** žymima laukelį teisinio subjekto viršijimui.

## <a name="allocation-term-example"></a>Paskirstymo sąlygų pavyzdys
Jūs nustatėte kaštų centrą savo organizacijai pavadintai KORPORACIJA, kurios numeris yra 000. Kai sąskaitos yra publikuotos komunalinėms išlaidoms, jos yra užkoduojamos į šį KOROPORACIJOS kaštų centrą. Jūsų bendrovė nustatė taisyklę, kad visos komunalinės išlaidos turi būti priskiriamos procentais į visus atskirus kaštų centrus. Kitos finansinės dimensijos skyriui ir verslo padaliniui liks tokios pačios.

Šiuo pavyzdžiu, nauja priskyrimų sąlyga bus sukurta komunalinių išlaidų pagrindinei paskyrai. Viena eilutė bus sukurta vienam kaštų centrui su priskiriamais procentais. **Pasirinkimo kriterijai** šaltinio finansinėms dimensijoms kiekvienai eilutei bus **Konkretų** skirti **Kaštų centrui** ir vertė bus nustatyta į 000: KOROPORACIJA. Skyriui ir verslo padaliniui,**Pasirinkimo kriterijai** bus **Nekonkretūs**.

Skyriuje **Paskirties buhalterijos paskyra** „FastTab“, pagrindinė paskyra bus ta pati komunalinių išlaidų paskyra ir **Šaltinio finansinių dimensijų palaikymas** bus nustatytas į **Taip** **Verslo padaliniui** ir **Skyriui.** **Palikti šaltinio finansinias dimensijas** bus nustatyta į **Ne** ir skirta **Kaštų centrui** ir pasirinkta vertė bus kiekvienam atitinkamam kaštų centrui, prie kurio priskiriate vertes. Jei esama trijų kaštų centrų, prie kurių priskiriamos išlaidos, tuomet trys priskyrimo sąlygų įrašai bus sukurti. Vienintelis skirtumas tarp visų priskyrimo sąlygų kaštų centre yra tas, kad jis yra nurodytas paskirties buhalterijos paskyroje.

## <a name="create-an-allocation-term-on-a-main-account"></a>Sukurti priskyrimo sąlygą pagrindinėje paskyroje

1. **Naršymo juostoje**, eikite į **Moduliai > Bendra buhalterija > Paskyrų diagrama > Paskyros > Pagrindinės paskyros**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. „FastTab“ **Juridinių subjektų viršijimas** pasirinkite **Įtraukti**.
4. Pasirinkite **Bendrovę** ir tuomet pasirinkite **Įtraukti**.
5. Pasirinkite **Priskyrimo** žymimą laukelį.
6. Pasirinkite **Priskyrimo sąlygos** .
7. Pasirinkite **Redaguoti** tam, kad keistumėte nustatytuosius įrašus ar pasirinktumėte **Naują** įrašo įtraukimui.
8. **Procento** laukelyje, įveskite kupono perlaidų procentą, kurį norite priskirti.
9. **Finansinių dimensijų šaltinyje** „FastTab“, **Kriterijų pasirinkimas** kiekvienai finansiniai dimensijai, pasirinkite parinktį.
    - Jei pasirenkate **Konkretus**, tuomet pasirinkite finansinės dimensijos vertę iškrentančiame laukelyje dešinėje.
    - Jei pasirenkate **Nekonkretus**, jokios papildomos informacijos yra nereikalaujama finansinei dimensijai.
10. **Paskirties buhalterijos** paskyros „FastTab“ **Į paskyrą** laukelyje, pasirinkite pagrindinę paskyrą, kurioje norite priskirti kupono perlaidos procentus.
11. **Laikyti šaltinio finansines dimensijas** kiekvienai finansinei dimensijai, pasirinkite parinktį.
    - Jei pasirenkate **Ne**, tuomet pasirinkite finansinės dimensijos vertę iškrentančiame laukelyje dešinėje, kuriame norite priskirti kupono transakciją.
    - Jei pasirenkate **Ne**, tuomet jokia papildoma informacija yra nereikalaujama. Sistema laikys vertę originaliame kupone publikuojant priskyrimą.
12. Pakartokite 7-11 žingsnius kiekvienam papildomam priskyrimui. Visų priskyrimų suma yra rodoma **Bendro procento** laukelyje. Ši suma negali viršyti 100.
13. Uždarykite visus puslapius.

>[!NOTE] 
> Galite pasirinktinai naudoti **Kopijavimo** mygtuką tam, kad dublikuotumėte pasirinktą skirstymą.

Kai skirstymo sąlygos yra sukuriamos pagrindinėje paskyroje, sistema automatiškai publikuoja naują kuponą, kai kuponas yra publikuojamas ir atitinka šaltinio finansines dimensijas skirstymo sąlygose.
