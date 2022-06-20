---
title: „Dynamics 365 Supply Chain Management“ peržiūra 10.0.27 (2022 m. liepa)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos programoje Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: a91f2cdae0fed75f07d6cae86d24aeedfca80e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844502"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>„Dynamics 365 Supply Chain Management“ peržiūra 10.0.27 (2022 m. liepa)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiamos priemonės, kurios yra naujos arba pakeistos "Microsoft Dynamics 365 Supply Chain Management preview" versijoje 10.0.27. Ši versija turi versijos 10.0.1227 versiją ir yra pasiekiama šiame grafike:

- **Vertinimo versijos leidimas:** 2022 m. balandžio mėn.
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2022 m. birželis
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. liepa

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šį straipsnį.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Atsargos ir logistika | [Atsargų paskirstymas pagal atsargų matomumo priedą](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [„Inventory Visibility“ atsargų paskirstymas](../inventory/inventory-visibility-allocation.md) | Įgalinta pagal numatytuosius nustatymus |
| Gamyba | Gamybos vietos vykdymo sąsajos rodinys „Mano diena“ | [Kaip darbuotojai naudoja gamybos laiko vykdymo sąsają](../production-control/production-floor-execution-use.md) ir [rodyti atostogų balansus gamybos laiko vykdymo sąsajoje](../production-control/production-floor-execution-payroll-stats.md) | Priemonių valdymas:<br>*Gamybos vietos vykdymo sąsajos rodinys „Mano diena“* |
| Planuojama | [Subrangos planavimo optimizavimo palaikymas](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Gamybos subrangos darbų valdymas](../production-control/manage-subcontract-work-production.md) | Įgalinta pagal numatytuosius nustatymus |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti bet kurią iš šių priemonių, tai turite atlikti funkcijų [valdymo metu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Bendrasis planavimas | Kurdami planuojamą perkėlimo užsakymą, atsižvelkite į atsargų parengimo laiką | Kai sukuriamas *suplanuotas* perkėlimo užsakymas, dėl šios funkcijos sistema turi atsižvelgti į atsargų vykdymo laiką, kuris nurodytas prekės numatytuosiuose užsakymo parametruose, kai jis apskaičiuoja suplanuoto perkėlimo užsakymo gavimo datą pristatymo datos valdymo nustatymui kaip vieneto Nėra arba Pardavimo *tipas* vykdymo laiką. Kai nurodomas perkėlimo vykdymo laikas, jo vertė bus naudojama apskaičiuojant gavimo datą, o transportavimo dienų nebus paisoma. |
| Paraiškos | Numatytoji brokerio sutarties mokesčių informacija tiekėjo sąskaitos faktūros eilutėse | Ši priemonė pristato logiką, kaip brokerio **sutarties** **tiekėjo SF eilutėse** nustatyti numatytąsias PVM ir prekės PVM laukų vertes. Ši logika taikoma tik tada, kai brokerio sutarties eilutėje mokesčių tipas yra DK / DK. Prekės PVM grupės numatytoji vertė bus arba iš brokerio tarpininkavimo įsigijimo kategorijos (jei nustatyta), arba iš išlaidų tipo. PVM grupė naudos numatytąją vertę iš tiekėjo sąskaitos. |
| Paraiškos | Apriboti pirkimo užsakymo eilučių skaičių kiekvienai paketinei užduočiai | Ši funkcija padeda optimizuoti sistemos našumą, kai registruojami patvirtinimai ir produkto gavimo kvitai. Naujas parametras, pavadintas Eilutės **kiekvienai užduočiai** **,** **pridedamas prie įsigijimo ir tiekimo parametrų puslapio skirtuko** Pristatymas. Šis naujas parametras leidžia riboti pirkimo užsakymo eilučių, kurias kiekvienas paketinis užduoties procesas, skaičių. Dėl to gali apsisaugoti nuo didelių paketinių užduočių lėtėja sistemos veikimą. |
| Produkto informacijos valdymas | Automatiškai įvesti produkto atributų vertes | Ši funkcija įtraukia periodinę užduotį, kuri pavadinta Automatiškai *įvesti produkto atributo vertes*. Ši nauja periodinė užduotis sukuria trūkstamus atributų, kurie susieti su produktais per produkto kategoriją, produkto atributo vertės įrašus. |
| Gamybos kontrolė | Papildoma konfigūracija gamybos vietos vykdymo sąsajoje | <p>Ši funkcija įtraukia šias pasirinktis į gamybos laiko **konfigūravimo vykdymo** puslapį:</p><ul><li>**Automatiškai atidaryti pradžios dialogo langą,** kai baigiama ieškoti – kai ši pasirinktis įgalinta, užduoties pradžios dialogo langas atidaromas automatiškai, **kai** darbuotojai užduočiai rasti naudoja ieškos juostą.</li><li>**Automatiškai atidaryti ataskaitos eigos dialogo** langą užbaigiant iešką – kai ši pasirinktis įgalinta, užduoties ataskaitos eigos dialogo langas atidaromas automatiškai, **kai** darbuotojai užduočiai rasti naudoja ieškos juostą.</li><li>**Numatytasis likęs kiekis ataskaitos eigos dialogo** lange – kai ši pasirinktis įgalinta, ataskaitos eigos dialogo lange rodomas likęs kiekis, **kuris** turi būti nurodytas gamybos užduoties ataskaitoje.</li></ul><p>Daugiau informacijos rasite Gamybos laiko [vykdymo sąsajos konfigūravimas](../production-control/production-floor-execution-configure.md).</p> |
| Gamybos kontrolė | Gamybos komandos gamybos vietos vykdymo sąsajoje | <p>Kai tai pačiai gamybos užduočiai priskirti keli darbuotojai, jie dabar gali paskirti vieną darbuotoją bandomuoju. Likę darbuotojai automatiškai tampa to darbuotojo asistentais. Gautai komandai užduoties būseną turi užregistruoti tik vadovas, o laiko įrašai taikomi visiems komandos nariams. Ši priemonė taip pat palaiko scenarijų, kuris vadinamas pagalbiniu *ištekliumi*. Tokiu atveju darbuotojas gali registruotis kaip kito darbuotojo asistentas, kuris tampa naujai sukurtos grupės vadu.</p><p>Daugiau informacijos rasite kaip darbuotojai [naudoja gamybos laiko vykdymo sąsają](../production-control/production-floor-execution-use.md).</p> |
| Gamybos kontrolė | Pranešti apie prekių planavimą gamybos vietos vykdymo sąsajoje | Ši funkcija supaprastina paketinių užsakymų ataskaitų procesą, siekiant gamybos laiko vykdymo sąsajoje planuoti prekes. Kai kuriamas *produktų*, kurių gamybos tipas yra Planavimo prekė, paketinis užsakymas, galima pranešti apie baigtą tik to paketinio užsakymo sudėti visus produktus ir pagal produktus. Paketiniai prekių planavimo užsakymai paprastai naudojami išsamūsems procesams, kai žaliavų produktas išsiškaiomas į kelis išsamūs produktus, palaikyti. Kai darbuotojas planavimo prekę praneša apie paketinį užsakymą kaip baigtą, **ataskaitos** eigos dialogo lange bus rodomi tik sudėtiiniai ir paketiniai produktai. Anksčiau ji taip pat parodė planavimo prekę, o ši elgsena gali apsaugoti darbuotojus. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme arba pastebimai atnaujinome šiuos žinyno straipsnius. Šie straipsniai nebūtinai susiję su naujomis funkcijomis, kurios buvo pridėtos prie šio leidimo, kaip išvardyta ankstesniuose skyriuose. Tačiau jos gali padėti gauti daugiau informacijos apie esamas funkcijas.

| Funkcijos sritis | Nauji arba atnaujinti straipsniai |
|---|---|
| Kaštų valdymas | [Svertinio vidurkio data su faktinės vertės įtraukimu ir žymėjimu](../cost-management/weighted-average-date.md) |
| Paskirstyta taip pat topologija | [Išbandykite skalės vienetus paskirstytoje hibridinėje topologijoje](../cloud-edge/cloud-edge-try-out.md) |
| Dvigubas rašymas | [Sinchronizavimas su „Supply Chain Management“ kainodaros mechanizmu pareikalavus](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Sandėlio valdymas | [Išleisti į sandėlį](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.27 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.27 versijos (2022 m. birželio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md) platformos naujinimus.

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.27 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

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
