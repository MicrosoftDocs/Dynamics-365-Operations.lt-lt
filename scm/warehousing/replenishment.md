---
title: Papildymas
description: "Šioje temoje aprašomos papildymo strategijos, skirtos sandėliams, kuriuose naudojamos modulio Sandėlio valdymas funkcijos."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: c3bbf35b98416cbc3feca2b0d01015a79cdb2659
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017

---

# <a name="replenishment"></a>Papildymas

[!include[banner](../includes/banner.md)]


Šioje temoje aprašomos papildymo strategijos, skirtos sandėliams, kuriuose naudojamos modulio Sandėlio valdymas funkcijos. Ši informacija netaikoma sandėliavimo sprendimui, kuris prieinamas modulyje Atsargų valdymas. Galima naudoti tolesnes papildymo strategijas.

-   **Papildymas pagal bangos poreikį** – naudojantis šia strategija sukuriamas išsiunčiamų užsakymų arba krovinių papildymo darbas, jei bangai kuriant darbą nėra atsargų. Pavyzdžiui, jei apdorojant bangą nėra pardavimo užsakymui reikalingo kiekio, gali būti sukurtas papildymo darbas.
-   **Min. / maks. papildymas** – pagal šią strategiją, norint nustatyti, kada reikia papildyti vietas, naudojami sandėliavimo minimumo ir maksimumo limitai. Pagal prekės ir vietos kriterijus nustatomos papildymui reikalingos atsargos. Min. / maks. papildymo šablonai yra pagrindinis mechanizmas, skirtas palaikyti optimalų prekių kiekį išrinkimo vietose. Siekiant užtikrinti, kad yra pakankamai atsargų, kurias galima paimti bangos poreikiui patenkinti, kaip priedą tarp min. / maks. papildymo ciklų galite naudoti poreikio papildymą.
-   **Krovinio poreikio papildymas** – šia strategija susumuojamas kelių krovinių poreikis ir sukuriamas papildymo darbas, kurio reikia siekiant pripildyti atitinkamas paėmimo vietas atsargų. Ši strategija padeda užtikrinti, kad sukuriamus krovinius būtų galima paimti sandėlyje, kai jie išleidžiami.

Naudojant visas tris strategijas papildymo darbas kuriamas pagal papildymo šabloną.

## <a name="wave-demand-replenishment"></a>Bangos poreikio papildymas

Bangos poreikio papildymas sukuria papildymo darbą pagal poreikį, jei bangai kuriant darbą nėra reikiamo gamybos užsakymų, „kanban‟ signalų, išsiunčiamų užsakymų arba krovinių kiekio. Papildymo šablone yra informacija apie prekės kriterijus, matavimo vienetus, poreikio padidėjimą ir vietą. 

Vietos nurodymai naudojami siekiant nustatyti, kurią vietą reikia papildyti. Šiuos vietų nurodymus susieti su papildymo šablonu galima naudojant lauką **Nurodymo kodas**. Jei laukas **Nurodymo kodas** nenustatytas, teikiamos užklausos siekiant nustatyti, kurį vietos nurodymą naudoti. Atkreipkite dėmesį, kad jei papildymo šablone nurodymo kodas nenurodytas, o vietos nurodymas turi nurodymo kodą, vietos nurodymo bus nepaisoma, net jei užklausa dėl vietos nurodymo yra teisinga. Paėmimo vietų nurodymai naudojami siekiant nustatyti, kur gauti atsargų papildymui. 

Be to, kurdami šabloną, bangos šablone turite nurodyti kai kuriuos papildymo parametrus. Bangos šablone turi būti bangos veiksmas, skirtas papildymui, kuris vykdomas tik jei prekės nepavyksta paskirstyti. Šis papildymo bangos veiksmas naudoja bangos veiksmo kodą, kad nustatytų, kurį papildymo šabloną naudoti. Turite užtikrinti ne tik tai, kad šablone būtų papildymo bangos veiksmas, bet ir tai, kad bangos šablono sekcijoje **Metodai** būtų pažymėta parinktis **Papildyti**. 

Puslapyje **Papildymo šablonas** yra žymės langelis **Leisti poreikio bangai naudoti nerezervuotus kiekius**. Jei norite leisti poreikio papildymui išskaičiuoti nerezervuotus kiekius iš darbo, sugeneruoto iš pasirinkto papildymo šablono, turite pažymėti šį žymės langelį. Norėdami, kad poreikio papildymo šablonai naudotų šią logiką, šį žymės langelį pažymėkite prie kiekvieno esamo papildymo šablono. Kai sandėlyje prireikia papildyti poreikį, ši bus išskaičiuojama ir esamo papildymo darbo su nerezervuotais kiekiais, jei darbas atsirado iš papildymo šablonų su pažymėtu žymės langeliu **Leisti bangos poreikiui naudoti nerezervuotus kiekius**.


Poreikio papildymo funkciją galima naudoti su pardavimo užsakymais, perkėlimo užsakymais, gamybos užsakymais ir „kanban‟ signalais. 

## <a name="minmax-replenishment"></a>Min. / maks. papildymas
Naudojant Min. / maks. papildymą, atsargos papildomos tarp didžiausios ir mažiausios nustatytos ribos. Paprastai šis procesas vykdomas vieną kartą per dieną, siekiant užtikrinti, kad prieš pradedant paėmimo procesą visos paėmimo vietos būtų užpildytos atsargomis iki didžiausios galimos ribos. 

Didžiausi ir mažiausi galimi kiekiai yra nustatomi papildymo šablone. Daugelis kitų šablono parametrų yra panašūs į parametrus tuose šablonuose, kurie naudojami bangos poreikio papildyme. Šablone turi būti po vieną eilutę kiekvienai prekei ir vietai. Kai pildote naudodami paketinę užduotį, „Finance and Operations“ eilučių išdėstymo tvarka įvertina, ar reikia pildyti. 

Atkreipkite dėmesį, kad naudojant min. / maks. papildymo strategiją negalima papildyti tuščios vietos, išskyrus atvejus, kai vieta yra nustatyta kaip fiksuota prekės vieta. Jei vieta, kurią reikia papildyti, nėra fiksuota vieta, neįmanoma nustatyti, kurią prekę papildyti. Todėl prieš vykdant papildymą vietoje turi būti bent šiek tiek turimo prekės kiekio.

## <a name="load-demand-replenishment"></a>Krovinio paklausos papildymas
Naudojant krovinio poreikio papildymo funkciją, susumuojamas kelių krovinių poreikis ir sukuriamas papildymo darbas, kurio reikia siekiant aktualias paėmimo vietas pripildyti atsargų. Krovinio poreikio papildymas labai panašus į bangos poreikio papildymą. Pagrindinis skirtumas yra tai, kaip ir kada krovinio poreikio papildymas ir bangos poreikio papildymas yra vykdomi. Kaip ir min. / maks. papildymas, krovinio poreikio papildymas vykdomas naudojant paketinę užduotį. Norėdami nustatyti paketinę užduotį, puslapyje **Krovinio poreikio papildymas** pasirinkite norimą naudoti papildymo šabloną ir nustatykite filtro užklausą, kad nurodytumėte, kurie kroviniai bus naudojami poreikiui nustatyti. Vietos užklausa nustato vietas, iš kurių bus paimamas bet koks galimas kiekis, siekiant patenkinti sukauptą krovinių poreikį.

## <a name="replenishment-prerequisites"></a>Papildymo būtinosios sąlygos
| Būtinoji sąlyga            | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prekė                    | Prekė privalo turėti įgalintus sandėlio valdymo procesus.                                                                                                                                                                                       |
| Sandėlis               | Sandėlis privalo turėti įgalintus sandėlio valdymo procesus. Norėdami įgalinti sandėlio valdymo procesus, puslapyje **Sandėliai** pasirinkite sandėlį, tada pasirinkite parinktį **Naudoti sandėlio valdymo procesus**. |
| Papildymo šablonai | Bent vieną papildymo šabloną reikia nustatyti min. / maks. papildymui, bangos poreikio papildymui arba krovinio poreikio papildymui.                                                                                                             |
| Vietos               | Vietos turi būti sukurtos ir prijungtos prie vietos šablono.                                                                                                                                                                                     |
| Vietos šablonai       | Vietos šablonai yra būtini, siekiant kurti vietas.                                                                                                                                                                                       |
| Vietos nurodymai     | Vietų nurodymai yra būtini, siekiant nukreipti darbą į vietas, kurias reikia papildyti, ir į vietas, iš kurių paimamos atsargos.                                                                                     |
| Darbo šablonai          | Tipo **Papildymas** darbo šablonas yra būtini, siekiant sukurti papildymo darbą, kad atsargas būtų galima perkelti į norimas vietas.                                                                                           |

