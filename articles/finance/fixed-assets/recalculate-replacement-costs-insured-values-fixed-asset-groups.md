---
title: Perskaičiuoti ilgalaikio turto grupių atkuriamąją vertę ir draudimo sumas
description: Šiame straipsnyje paaiškinamas ilgalaikio turto atkuriamosios vertės ir draudimo sumų atnaujinimo procesas.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9dd04072b4845fe5df2a918b64ba1835ea584dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187112"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Perskaičiuoti ilgalaikio turto grupių atkuriamąją vertę ir draudimo sumas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinamas ilgalaikio turto atkuriamosios vertės ir draudimo sumų atnaujinimo procesas.

Reguliariai galite būti informuojami, kad pasikeitė tam tikros ilgalaikio turto atkuriamosios arba draudimo išlaidos. Pavyzdžiui, vadybininkas gali jus informuoti, kad infliacija praėjusiais metais siekė 3 proc., todėl viso ilgalaikio turto atkuriamąją vertę reikia padidinti 3 procentais. 

Nors puslapyje **Ilgalaikis turtas** galite redaguoti tam tikro ilgalaikio turto atkuriamąją vertę ir draudimo sumą, šioms visos turto grupės vertėms atnaujinti iš karto galite naudoti puslapį **Atnaujinti atkuriamąsias vertes ir draudimo sumas**. Ši informacija paaiškina, kaip atnaujinti ilgalaikio turto grupių arba konkretaus grupių turto vertes.

## <a name="how-values-are-updated"></a> Kaip atnaujinamos vertės
Norėdami perskaičiuoti ilgalaikio turto grupių atkuriamąją vertę ir draudimo sumą, turite nurodyti procentą, kuriuo turi būti pakeistos esamos atkuriamosios vertės ir draudimo sumos, tada atlikti periodinį atnaujinimą, kad vertės būtų perskaičiuotos. Procentas nurodomas puslapio **Ilgalaikio turto grupės** laukuose **Atkuriamosios vertės koeficientas** ir **Draudimo sumos koeficientas**. Nors šie koeficientai nurodomi ilgalaikio turto grupei, kai naudojate puslapį **Atnaujinti atkuriamąsias vertes ir draudimo sumas**, galite pasirinkti perskaičiuoti atkuriamąją vertę ir draudimo sumą tik tam tikram grupės ilgalaikiam turtui. 

Kai turto atkuriamajai vertei ir draudimo sumai perskaičiuoti naudojate puslapį **Atnaujinti atkuriamąsias vertes ir draudimo sumas**, naudojamos toliau nurodytos formulės.

-   \[(Turto grupės atkuriamosios vertės koeficientas / 100) + 1\] \* Esama turto atkuriamoji vertė
-   \[(Turto grupės draudimo sumos koeficientas / 100) + 1\] \* Esama turto draudimo suma

> [!NOTE] 
> Kai naudojate puslapį **Atnaujinti atkuriamąsias vertes ir draudimo sumas**, atnaujinama ir ilgalaikio turto atkuriamoji vertė, ir draudimo suma; negalite nurodyti, kad būtų atnaujinama tik viena vertė. Norėdami, kad viena vertė išliktų nepakitusi naujinant kitą vertę, kaip koeficientą puslapyje **Ilgalaikio turto grupės** įveskite 0 (nulį). Jei koeficientas lygus nuliui paliekamas tuščias, skaičiavimas atnaujinimo metu praleidžiamas. Ilgalaikio turto balansinė vertė ir grynoji balansinė vertė periodinio naujinimo metu nėra paveikiamos. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Kaip naudoti datą, norint pasirinkti, kurias prekes naujinti
Pagal numatytąjį nustatymą naujinimo proceso metu atnaujinamas pasirinktas turtas, kuris nebuvo atnaujintas šią dieną, bet galėjo būti atnaujintas ankstesnėmis dienomis. Pavyzdžiui, &lt; dabartinė data reiškia „iki šiandien“. Puslapyje **Atnaujinti atkuriamąsias vertes ir draudimo sumas** spustelėję mygtuką **Pasirinkti** galite pakeisti datą. Jūsų nurodomi datos kriterijai yra palyginami su paskutinio turto periodinio naujinimo data (puslapio **Ilgalaikis turtas** laukas **Paskutinis periodinis sumos / vertės atnaujinimas**). Kiekvieną kartą sėkmingai atnaujinus ilgalaikio turto atkuriamąją vertę arba draudimo sumą, laukas **Paskutinis periodinis sumos / vertės atnaujinimas** yra automatiškai atnaujinamas dabartine data. 

Pavyzdys 

Vakar 5 procentais atnaujinote transporto priemonių, biuro baldų ir pastatų grupių atkuriamąją vertę ir laikote, kad šis turtas yra tiksliai atnaujintas. Norėdami šį turtą pašalinti, kai šiandien naujinate visą kitą ilgalaikį turtą, lauke **Paskutinis periodinis sumos / vertės atnaujinimas** įveskite užvakar dienos datą (&lt; vakar diena), nes paskutinis grupių **Transporto priemonės**, **Biuro baldai** ir **Pastatai** naujinimas vyko už jūsų nurodytų datos kriterijų ribų.

## <a name="cumulative-effect-of-each-update"></a> Kiekvieno naujinimo kaupiamasis poveikis
Kiekvienas naujinimas turi kaupiamąjį poveikį. Todėl savo naujinimus reikėtų planuoti atidžiai. Pavyzdžiui, jei antradienį visą turtą padidinsite 3 procentais, tada penktadienį padidinsite biuro baldus 4 procentais, biuro baldų vertė iš viso padidės 7,12 procento.

## <a name="scenario"></a>Scenarijus
Jūsų vadybininkas jums praneša apie tokius ilgalaikio turto pokyčius:
-   Padidinti viso ilgalaikio turto, išskyrus kompiuterius, atkuriamąją vertę 3,25 procento.
-   Visų biuro baldų atkuriamąją vertę padidinti papildomai 1 procentu.
-   Visų kompiuterių atkuriamąją vertę ir draudimo sumą sumažinti 10 procentų.

Galima atlikti toliau nurodytus keitimus.
1.  Puslapyje **Ilgalaikio turto grupės** visoms ilgalaikio turto grupėms, išskyrus grupę **Biuro baldai** ir **Kompiuteriai**, lauke **Atkuriamosios vertės koeficientas** įveskite 3,25, o lauke **Draudimo sumos koeficientas** įveskite 0.
2.  Grupės **Biuro baldai** lauke **Atkuriamosios vertės koeficientas** įveskite 4,25, o lauke **Draudimo sumos koeficientas** įveskite 0.
3.  Grupės **Kompiuteriai** lauke **Atkuriamosios vertės koeficientas** įveskite –10, o lauke **Draudimo sumos koeficientas įveskite** –10.
4.  Puslapyje **Atnaujinti atkuriamąsias vertes ir draudimo sumas** spustelėkite **Gerai**, norėdami perskaičiuoti visą ilgalaikį turtą.

Kitą dieną vadybininkas jus informuoja, kad kompiuterių vertė sumažėjo 8 procentais, o ne 10, todėl reikia pataisyti atkuriamąsias vertes ir draudimo sumas. Klaidą galima pataisyti vienu iš šių dviejų būdų:
-   Neautomatiškai keiskite kiekvieno ilgalaikio turto grupės **Kompiuteriai** ilgalaikio turto laukų **Draudimo suma** ir **Atkuriamoji vertė** reikšmes puslapyje **Ilgalaikis turtas**. Apskaičiuokite ir rankiniu būdu įveskite vertes, jei pradinę sumą sumažinote 8 procentais. Taikant šį metodą puslapio **Atnaujinti atkuriamąsias vertes ir draudimo sumas** naudoti nereikia.
-   Įveskite grupės **Kompiuteriai** atkuriamosios vertės ir draudimo sumos koeficientus puslapio **Ilgalaikio turto grupės** laukuose **Atkuriamosios vertės koeficientas** ir **Draudimo sumos koeficientas**. Tada bus atkurta turto pradinė vertė (prieš 10 procentų sumažinimą) ir taikykite pradinės vertės sumažinimą 8 procentais. Tada naudokite puslapį **Atnaujinti atkuriamąsias vertes ir draudimo sumas**, kad perskaičiuotumėte reikšmes pagal įvestus koeficientus.

> [!NOTE]  
> Koeficiento –10 negalima atšaukti įvedant teigiamą koeficientą 10 (arba koeficientą 2: –10 ir –8 skirtumas), nes sumos nebus apskaičiuotos taip, kaip tikitės. 





