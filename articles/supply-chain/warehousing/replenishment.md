---
title: Papildymo apžvalga
description: Šiame straipsnyje aprašomos papildymo strategijos, skirtos sandėliams, kuriuose naudojama sandėlio valdymo funkcija.
author: Mirzaab
ms.date: 02/19/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSReplenishmentTemplates, WHSInventFixedLocation, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "90043"
- intro-internal
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 075e74845eb8e0363cdb706f1f3af0dc9cfddfaa
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069189"
---
# <a name="replenishment-overview"></a>Papildymo apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos papildymo strategijos, skirtos sandėliams, kuriuose naudojama sandėlio valdymo funkcija. Šiame straipsnyje pateikiama informacija netaikoma sandėliavimo sprendimą, kuris yra atsargų valdymas.

Galima naudoti tolesnes papildymo strategijas.

- **Papildymas pagal bangos poreikį** – naudojantis šia strategija sukuriamas išsiunčiamų užsakymų arba krovinių papildymo darbas, jei bangai kuriant darbą nėra atsargų. Pavyzdžiui, jei apdorojant bangą nėra pardavimo užsakymui reikalingo kiekio, gali būti sukurtas papildymo darbas.
- **Min. / maks. papildymas** – pagal šią strategiją, norint nustatyti, kada reikia papildyti vietas, naudojami sandėliavimo minimumo ir maksimumo limitai. Pagal prekės ir vietos kriterijus nustatomos papildymui reikalingos atsargos. Min. / maks. papildymo šablonai yra pagrindinis mechanizmas, skirtas palaikyti optimalų prekių kiekį išrinkimo vietose. Siekiant užtikrinti, kad yra pakankamai atsargų, kurias galima paimti bangos poreikiui patenkinti, kaip priedą tarp min. / maks. papildymo ciklų galima naudoti poreikio papildymą.
- **Krovinio poreikio papildymas** – šia strategija susumuojamas kelių krovinių poreikis ir sukuriamas papildymo darbas, kurio reikia siekiant pripildyti atitinkamas paėmimo vietas atsargų. Ši strategija padeda užtikrinti, kad sukuriamus krovinius galima galima paimti sandėlyje, kai jie išleidžiami.
- **Skubus papildymas** – jei nepavyksta paskirstyti vietos nurodymo eilutės su papildymo šablonu, šia strategija atsargos papildomos prieš vykdant bangą. 

Naudojant visas keturias strategijas papildymo darbas kuriamas pagal papildymo šabloną.

## <a name="wave-demand-replenishment"></a>Bangos poreikio papildymas
Bangos poreikio papildymas sukuria papildymo darbą pagal poreikį, jei bangai kuriant darbą nėra reikiamo gamybos užsakymų, „kanban“ signalų, išsiunčiamų užsakymų arba krovinių kiekio. Papildymo šablone yra informacija apie prekės kriterijus, matavimo vienetus, poreikio padidėjimą ir vietą. 

Vietos nurodymai naudojami siekiant nustatyti, kurią vietą reikia papildyti. Šiuos vietų nurodymus susieti su papildymo šablonu galima naudojant lauką **Nurodymo kodas**. Jei laukas **Nurodymo kodas** nenustatytas, teikiamos užklausos siekiant nustatyti, kurį vietos nurodymą naudoti. Atkreipkite dėmesį, kad jei papildymo šablone nurodymo kodas nenurodytas, o vietos nurodymas turi nurodymo kodą, vietos nurodymo bus nepaisoma, net jei užklausa dėl vietos nurodymo yra teisinga. Paėmimo vietų nurodymai naudojami siekiant nustatyti, kur gauti atsargų papildymui. 

Be to, kurdami šabloną, bangos šablone turite nurodyti kai kuriuos papildymo parametrus. Bangos šablone turi būti bangos veiksmas, skirtas papildymui, kuris vykdomas, tik jei prekės nepavyksta sėkmingai paskirstyti. Šis papildymo bangos veiksmas naudoja bangos veiksmo kodą, kad nustatytų, kurį papildymo šabloną naudoti. Turite užtikrinti ne tik tai, kad šablone būtų papildymo bangos veiksmas, bet ir tai, kad bangos šablono dalyje **Metodai** yra pažymėta parinktis **Papildyti**. 

Puslapyje **Papildymo šablonas** yra žymės langelis **Leisti poreikio bangai naudoti nerezervuotus kiekius**. Pažymėkite šį žymės langelį, jei poreikio papildymas turi galėti išskaičiuoti nerezervuotus kiekius iš darbo, sugeneruoto iš pasirinkto papildymo šablono. Norėdami, kad poreikio papildymo šablonai naudotų šią logiką, šį žymės langelį pažymėkite prie kiekvieno esamo papildymo šablono. Kai sandėlyje prireikia papildyti poreikį, ši bus išskaičiuojama ir esamo papildymo darbo su nerezervuotais kiekiais, jei darbas atsirado iš papildymo šablonų su pažymėtu žymės langeliu **Leisti bangos poreikiui naudoti nerezervuotus kiekius**.

**Papildymo vienetas** yra mažiausias vienetas, kurį galima papildyti. Tai turi būti sveikasis skaičius, kuris yra vieneto sudėtinis kiekis. Kuriant darbą, sistema suapvalins iki didžiausio galimo vieneto.

Poreikio papildymo funkciją galima naudoti su pardavimo užsakymais, perkėlimo užsakymais, gamybos užsakymais ir „kanban‟ signalais. 

## <a name="minmax-replenishment"></a>Min. / maks. papildymas
Naudojant Min. / maks. papildymą, atsargos papildomos tarp didžiausios ir mažiausios nustatytos ribos. Paprastai šis procesas vykdomas vieną kartą per dieną, siekiant užtikrinti, kad prieš pradedant paėmimo procesą visos paėmimo vietos būtų užpildytos atsargomis iki didžiausios galimos ribos. 

Didžiausi ir mažiausi galimi kiekiai yra nustatomi papildymo šablone. Daugelis kitų šablono parametrų yra panašūs į parametrus tuose šablonuose, kurie naudojami bangos poreikio papildyme. Šablone turi būti po vieną eilutę kiekvienai prekei ir vietai. Kai pildote naudodami paketinę užduotį, sistema pagal eilučių išdėstymo tvarką įvertina, ar reikia pildyti. 

Atkreipkite dėmesį, kad naudojant min. / maks. papildymo strategiją negalima papildyti tuščios vietos, išskyrus atvejus, kai vieta yra nustatyta kaip fiksuota prekės vieta. Jei vieta, kurią reikia papildyti, nėra fiksuota vieta, sistema negali nustatyti, kurią prekę reikia papildyti. Todėl prieš vykdant papildymą vietoje turi būti bent šiek tiek turimo prekės kiekio.

## <a name="load-demand-replenishment"></a>Krovinio paklausos papildymas
Naudojant krovinio poreikio papildymą, susumuojamas kelių krovinių poreikis ir sukuriamas papildymo darbas, kurio reikia siekiant pripildyti atitinkamas paėmimo vietas atsargų. Krovinio poreikio papildymas labai panašus į bangos poreikio papildymą. Pagrindinis skirtumas yra tai, kaip ir kada krovinio poreikio papildymas ir bangos poreikio papildymas yra vykdomi. Kaip ir min. / maks. papildymas, krovinio poreikio papildymas vykdomas naudojant paketinę užduotį. Norėdami nustatyti paketinę užduotį puslapyje **Krovinio poreikio papildymas** pasirinkite naudotiną papildymo šabloną ir nustatykite filtro užklausą, kad nurodytumėte, kurie kroviniai bus naudojami poreikiui nustatyti. Vietos užklausa nustato vietas, iš kurių bus paimamas bet koks galimas kiekis, siekiant patenkinti sukauptą krovinių poreikį.

## <a name="immediate-replenishment"></a>Skubus papildymas
Užuot poreikį sumuodami paskirstymo proceso pabaigoje ir papildymo procesą atlikdami pagal susumuotą kiekį, galite pritaikyti strategiją Skubus papildymas. Naudojant šią strategiją, atsargas galima papildyti iškart po to, kai nepavyksta paskirstyti vietos nurodymo eilutės. Todėl papildymo procesą galite nustatyti taip, kad jį ribotų konkretūs vienetai, ir kad jis naudotų nustatytus konkrečių vietų kiekius.

## <a name="replenishment-prerequisites"></a>Papildymo būtinosios sąlygos

|      Būtinoji sąlyga       |                                                                                                                                aprašymas                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Prekė           |                                                                                                        Prekė turi būti įgalinta sandėlio valdymo procesuose (WMS).                                                                                                        |
|        Sandėlis        | Sandėlis turi būti įgalintas sandėlio valdymo procesams (WMS). Norėdami įgalinti WMS sandėlį, sandėlio <strong></strong> puslapyje pasirinkite sandėlį, tada pasirinkite parinktį Naudoti <strong>sandėlio valdymo</strong> procesus. |
| Papildymo šablonai |                                                                   Bent vieną papildymo šabloną reikia nustatyti min. / maks. papildymui, bangos poreikio papildymui arba krovinio poreikio papildymui.                                                                   |
|        Vietos        |                                                                                                       Vietos turi būti sukurtos ir prijungtos prie vietos šablono.                                                                                                       |
|    Vietos šablonai    |                                                                                                        Vietos šablonai yra būtini, siekiant kurti vietas.                                                                                                        |
|   Vietos nurodymai   |                                                       Vietų nurodymai yra būtini, siekiant nukreipti darbą į vietas, kurias reikia papildyti, ir į vietas, iš kurių paimamos atsargos.                                                        |
|     Darbo šablonai      |                                                   Tipo <strong>Papildymas</strong> darbo šablonas yra būtini, siekiant sukurti papildymo darbą, kad atsargas būtų galima perkelti į norimas vietas.                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]