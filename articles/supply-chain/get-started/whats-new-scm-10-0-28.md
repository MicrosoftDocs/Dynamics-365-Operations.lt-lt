---
title: Naujienos ir pakeitimai „Dynamics 365 Supply Chain Management” 10.0.28 (2022 m. rugpjūtis)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos programoje Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 5cca06517fbdcbdae6e54c106b113a83851240c8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334782"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Naujienos ir pakeitimai „Dynamics 365 Supply Chain Management” 10.0.28 (2022 m. rugpjūtis)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos funkcijos, kurios yra naujos arba pakeistos "Microsoft Dynamics 365 Supply Chain Management " 10.0.28 versijoje. Ši versija turi versijos 10.0.1264 versiją ir yra pasiekiama šiame grafike:

- **Peržiūros versijos išleidimas:** 2022 m. gegužė
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2022 m. liepa
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. liepa

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šį straipsnį.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Atsargos ir logistika | [Įkainoti išlaidų integravimo objektai trečiosios šalies krovinių ekspeditoriams](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Gabenimo išlaidų objektų peržiūra](../landed-cost/landed-cost-entities-overview.md) | Įgalinta pagal numatytuosius nustatymus |
| Planuojama | [Žaliavų poreikių planavimas pagal paklausą (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Poreikio valdomas medžiagų poreikių planavimo peržiūra](../master-planning/planning-optimization/ddmrp-overview.md) | Priemonių valdymas:<br>*(Peržiūros versija) Planavimo optimizavimo DDMRP* |
| Planuojama | [Galima pateikti atsargos planavimo optimizavimo palaikymas (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [Apskaičiuoti pardavimo užsakymo pristatymo datas naudojant CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | Priemonių valdymas:<br>*(Peržiūros versija) Planavimo optimizavimo CTP* |
| Planuojama | [Laikymo trukmės planavimo optimizavimo palaikymas](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [Produktų, kurių laikymo laikas ribotas, bendrasis planavimas](../master-planning/planning-optimization/shelf-life.md) | Įgalinta pagal numatytuosius nustatymus |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti bet kurią iš šių priemonių, tai turite atlikti funkcijų [valdymo metu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Atsargų ir sandėlio valdymas | Įjungti vidinės įmonės teikiamą informaciją, kad būtų rodomas tik ne nulinis turimas kiekis | Ši priemonė leidžia pasirinkti, ar prekės, kurių kiekis lygus nuliui, turėtų būti įtrauktos į vidinės įmonės turimo kiekio sąrašą. Šią pasirinktį **galite** kontroliuoti naudodami vidinės įmonės turimo sąrašo parametre, kurį ši funkcija įtraukia į atsargų ir sandėlio valdymo parametrų puslapį, **nerodyti prekių, kurių kiekis turi būti** nulinis. |
| Atsargų ir sandėlio valdymas | (Indija) Taikant perdavimo kainos taisykles, nepaisykite vietos, kai parinktis „Iš sandėlio kodo“ nustatyta kaip „Visi“ | <p>Ši funkcija taikoma tik Indijoje lokalizavimui. Dėl to atsargų perkėlimų prekių perkėlimo kainų nustatymo procesas yra svarbesnis.</p><p>Perkėlimo kainas galite nustatyti sukonfigūruodami kiekvieną prekę su perkėlimo kainų taisyklėmis. Vienas būdas atlikti šią konfigūraciją yra įtraukti taisyklės eilutę, kur lauko **Iš sandėlio** kodas reikšmė yra *Visi*. Šis parametras nurodo, kad eilutės nustatyta perkėlimo kaina turi būti taikoma neatsižvelgiant į sandėlį, iš kur paimta prekė. Įgalinus šią funkciją, perkėlimo kainų taisyklės, kuriose lauke **Iš** sandėlio kodo nustatyta kaip Visi *, nepaisys* parametro **Vietos**. Todėl taisyklė bus taikoma nepaisant perkėlimo užsakyme nurodytos vietos. Taip greičiausiai tikimasi, nes vieta saugojimo dimensijų hierarchijoje yra žemiau sandėlio.</p><p>Be šios funkcijos sistema tai taikys šio tipo taisykles tik tada, kai perkėlimo užsakymo vieta tiksliai atitiks vietą, nustatytą taisyklei. (Jei taisyklei nustatyta tuščia vieta, sistema tai taikys taisyklę tik perkėlimo užsakymams, kurie taip pat turi tuščią vietos reikšmę.)</p> |
| Atsargų ir sandėlio valdymas | Turimų atsargų ataskaitos duomenų valymas | Ši priemonė leidžia išvalyti duomenis, kurie naudojami kuriant turimų atsargų *ataskaitų saugojimo* ataskaitas. |
| Gamybos kontrolė | Priskirkite projekto veiklas paslaugų sutarties ir paslaugų užsakymo eilutėms | Ši priemonė įtraukia lauką, pavadintą **Projekto** veikla, į aptarnavimo sutartį ir aptarnavimo užsakymo eilutes, kad galėtumėte nustatyti jų projekto veiklą. Ši funkcija padės išvengti blokavimo klaidų, kai registruojate aptarnavimo valdymo projektų žurnalus, kuriuose reikalaujama nustatyti projekto veiklą.  |
| Sandėlio valdymas | Administratoriaus arba panašių patikimų vartotojų perkėlimo eilutės išrinkimo rankiniu būdu paslauga | Ši funkcija leidžia administratoriams rankiniu būdu išrinkti atsargų operacijas, susijusias su perkėlimo eilutėmis. Šios eilutės apima eilutes, kurios jau išleistos į sandėlį. Administratoriai šį paėmimą turi atlikti tik išskirtiniais atvejais, pvz., kai sistema yra sugadintos būsenos. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme arba pastebimai atnaujinome šiuos žinyno straipsnius. Šie straipsniai nebūtinai susiję su naujomis funkcijomis, kurios buvo pridėtos prie šio leidimo, kaip išvardyta ankstesniuose skyriuose. Tačiau jos gali padėti gauti daugiau informacijos apie esamas funkcijas.

| Funkcijos sritis | Nauji arba atnaujinti straipsniai |
|---|---|
| Kaštų valdymas | [Fiksuota gavimo kaina](../cost-management/fixed-receipt-price.md) |
| Kaštų valdymas | [Atsargų įkainojimo dažnai užduodami klausimai](../cost-management/inventory-costing-faq.md) |
| Kaštų valdymas | [Registruoti apskaitos principų išlaidų sąskaitoje](../cost-management/post-to-charge-account-accounting-principle.md) |
| Atsargų valdymas | [Atsargų operacijos išsami informacija](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.28 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.28 versijos (2022 m. birželio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md) platformos naujinimus.

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.28 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>"Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas](/dynamics365-release-plan/2022wave1/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Straipsnyje [pašalintos arba pasenusios Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funkcijos aprašomos priemonės, kurios buvo arba yra suplanuotos pašalinti arba pasenusios tiekimo grandinės valdymui.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant bet kokią priemonę iš produkto, [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) pranešimai dėl nušalinimo bus pereiti prie pašalintų arba pasenusių funkcijų 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

