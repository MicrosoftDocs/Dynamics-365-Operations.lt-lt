---
title: Peržiūra, Dynamics 365 Supply Chain Management 10.0.28 (2022 m. rugpjūčio mėn.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.28 funkcijos.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 306ff9be80c7a7a947b9132e3c9b4b9ec799b265
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813180"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Peržiūra, Dynamics 365 Supply Chain Management 10.0.28 (2022 m. rugpjūčio mėn.)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje pateikiamos priemonės, kurios yra naujos arba pakeistos "Microsoft Dynamics 365 Supply Chain Management preview" versijoje 10.0.28. Ši versija turi versijos 10.0.1264 versiją ir yra pasiekiama šiame grafike:

- **Peržiūros versijos išleidimas:** 2022 m. gegužė
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2022 m. liepa
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. liepa

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šią temą, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šią temą.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Atsargos ir logistika | [Įkainoti išlaidų integravimo objektai trečiosios šalies krovinių ekspeditoriams](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Įkrautų išlaidų objektų peržiūra](../landed-cost/landed-cost-entities-overview.md) | Įgalinta pagal numatytuosius nustatymus |
| Planuojama | [Laikymo trukmės planavimo optimizavimo palaikymas](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Jau greitai <!-- KFM: Vendor is preparing this. Expected May 20. --> | Įgalinta pagal numatytuosius nustatymus |

<!-- KFM: Confirm status of this feature:
| Planning | [Demand Driven Material Requirements Planning (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | Coming soon | Feature management:<br>*(Preview) DDMRP for Planning Optimization* | -->

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti bet kurią iš šių priemonių, tai turite atlikti funkcijų [valdymo metu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Atsargų ir sandėlio valdymas | Įgalinti vidinės įmonės atsargų kiekį, kad būtų rodomas tik ne nulinis kiekis | Ši priemonė leidžia pasirinkti, ar prekės, kurių kiekis lygus nuliui, turėtų būti įtrauktos į vidinės įmonės turimo kiekio sąrašą. Šią pasirinktį **galite** kontroliuoti naudodami vidinės įmonės turimo sąrašo parametre, kurį ši funkcija įtraukia į atsargų ir sandėlio valdymo parametrų puslapį, **nerodyti prekių, kurių kiekis turi būti** nulinis. |
| Atsargų ir sandėlio valdymas | (Indija) Taikant perdavimo kainos taisykles, nepaisykite vietos, kai parinktis „Iš sandėlio kodo“ nustatyta kaip „Visi“ | <p>Ši funkcija taikoma tik Indijoje lokalizavimui. Dėl to atsargų perkėlimų prekių perkėlimo kainų nustatymo procesas yra svarbesnis.</p><p>Perkėlimo kainas galite nustatyti sukonfigūruodami kiekvieną prekę su perkėlimo kainų taisyklėmis. Vienas būdas atlikti šią konfigūraciją yra įtraukti taisyklės eilutę, kur lauko **Iš sandėlio** kodas reikšmė yra *Visi*. Šis parametras nurodo, kad eilutės nustatyta perkėlimo kaina turi būti taikoma neatsižvelgiant į sandėlį, iš kur paimta prekė. Įgalinus šią funkciją, perkėlimo kainų taisyklės, kuriose lauke **Iš** sandėlio kodo nustatyta kaip Visi *, nepaisys* parametro **Vietos**. Todėl taisyklė bus taikoma nepaisant perkėlimo užsakyme nurodytos vietos. Taip greičiausiai tikimasi, nes vieta saugojimo dimensijų hierarchijoje yra žemiau sandėlio.</p><p>Be šios funkcijos sistema tai taikys šio tipo taisykles tik tada, kai perkėlimo užsakymo vieta tiksliai atitiks vietą, nustatytą taisyklei. (Jei taisyklei nustatyta tuščia vieta, sistema tai taikys taisyklę tik perkėlimo užsakymams, kurie taip pat turi tuščią vietos reikšmę.)</p> |
| Atsargų ir sandėlio valdymas | Turimų atsargų ataskaitos duomenų valymas | Ši priemonė leidžia išvalyti duomenis, kurie naudojami kuriant turimų atsargų *ataskaitų saugojimo* ataskaitas. |
| Gamybos kontrolė | Priskirkite projekto veiklas paslaugų sutarties ir paslaugų užsakymo eilutėms | Ši priemonė įtraukia lauką, pavadintą **Projekto** veikla, į aptarnavimo sutartį ir aptarnavimo užsakymo eilutes, kad galėtumėte nustatyti jų projekto veiklą. Ši funkcija padės išvengti blokavimo klaidų, kai registruojate aptarnavimo valdymo projektų žurnalus, kuriuose reikalaujama nustatyti projekto veiklą.  |
| Sandėlio valdymas | Administratoriaus arba panašių patikimų vartotojų perkėlimo eilutės išrinkimo rankiniu būdu paslauga | Ši funkcija leidžia administratoriams rankiniu būdu išrinkti atsargų operacijas, susijusias su perkėlimo eilutėmis. Šios eilutės apima eilutes, kurios jau išleistos į sandėlį. Administratoriai šį paėmimą turi atlikti tik išskirtiniais atvejais, pvz., kai sistema yra sugadintos būsenos. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme arba pastebimai atnaujinome šias žinyno temas. Šios temos nebūtinai susijusios su naujomis funkcijomis, kurios buvo pridėtos prie šio leidimo, kaip išvardyta ankstesniuose skyriuose. Tačiau jos gali padėti gauti daugiau informacijos apie esamas funkcijas.

| Funkcijos sritis | Naujos arba atnaujintos temos |
|---|---|
| Kaštų valdymas | [Fiksuota gavimo kaina](../cost-management/fixed-receipt-price.md) |
| Kaštų valdymas | [Atsargų įkainojimo dažnai užduodami klausimai](../cost-management/inventory-costing-faq.md) |
| Kaštų valdymas | [Registruoti mokesčių sąskaitos apskaitos principu](../cost-management/post-to-charge-account-accounting-principle.md) |
| Atsargų valdymas | [Atsargų operacijų informacija](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.28 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.28 versijos (2022 m. birželio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md) platformos naujinimus.<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.28 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>"Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas](/dynamics365-release-plan/2022wave1/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Temoje [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) aprašomos „Supply Chain Management“ funkcijos, kurios yra pašalintos, yra suplanuotos pašalinti arba yra pasenusios.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant iš produkto bet kokią funkciją, pranešimas apie nebenaudojimą bus paskelbtas [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) temoje 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
