---
title: Naujienos ir pakeitimai „Dynamics 365 Supply Chain Management” 10.0.20 (2021 m. rugpjūtis)
description: Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Supply Chain Management“ 10.0.20 versijos funkcijos.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1aada0d3ebe80e1efb92815c6d429ed5638dabdbac165aa09be1ca281c51b255
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773518"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Naujienos ir pakeitimai „Dynamics 365 Supply Chain Management” 10.0.20 (2021 m. rugpjūtis)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.20 versijos funkcijos. Šios versijos komponavimo numeris yra 10.0.886 ir jis pasiekiamas tokius būdu:

- **Peržiūros versijos išleidimas:** 2021 m. gegužė
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2021 m. liepa
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2021 m. rugpjūtis

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos šiame leidime. Priemonės *stulpelyje* pateikiami saitai [į paleidimo](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) planą, kur matysite oficialias kiekvienos priemonės paleidimo datas. Stulpelyje *Daugiau informacijos* pateikiama išsami informacija ir (arba) nuorodos į susijusius dokumentus.

Daugumą šių funkcijų reikia įjungti naudojant [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad galėtumėte jomis naudotis.

| Funkcijos sritis | Funkcija | Daugiau informacijos |
|---|---|---|
| Atsargos&nbsp;ir&nbsp;logistika | [Pardavimo užsakymo informacijos našumo gerinimas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Dėl šios funkcijos vartotojo sąsaja reaguoja greičiau atidarant pardavimo užsakymus, ypač užsakymus, kuriuose yra daug eilučių. |
| Gamyba | [Proceso automatizavimo srautų iškvietimas kokybės užsakymams kurti](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Proceso automatizavimo srautų iškvietimas kokybės užsakymams kurti](../production-control/process-automation-quality-orders.md ) |
| Gamyba | [Patobulinta gamybos vietos vykdymo gamybinė sąsaja](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Gamybos vietos vykdymo sąsajos konfigūravimas](../production-control/production-floor-execution-configure.md) |
| Produkto informacijos valdymas | [Formulių ir jų ingredientų pakeitimų valdymas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Formulių ir jų ingredientų pakeitimų valdymas](../engineering-change-management/manage-formula-changes.md) |
| Produkto informacijos valdymas | [Produkto parengties patikros](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Produkto parengtis](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip). Jei norite naudoti bet kurią iš šių funkcijų, turite ją tiesiogiai įgalinti [Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funkcijos sritis | Funkcijos&nbsp;pavadinimas&nbsp;funkcijos&nbsp;valdyme | Daugiau informacijos |
|---|---|---|
| Bendrasis planavimas | Vienu metu vykdomas pakoreguotos poreikio prognozės įgaliojimas | Ši funkcija leidžia lygiagrečiai autorizuoti pakoreguotą poreikio prognozę iš **Pakoreguotos poreikio prognozės** puslapio. Šios funkcijos tikslas yra padidinti efektyvumą, kai autorizuojate didelį skaičių prognozių. Autorizuodamas vartotojas gali nurodyti **Gijų skaičių** autorizavimo dialogo lange. |
| Bendrasis planavimas | (Peržiūros versija) Paketais valdomas tvirtinimas ir konsolidacija suplanuotiems nesupakuotiems ir supakuotiems paketiniams užsakymams | Ši funkcija leidžia naudoti paketines užduotis tvirtinant ir konsoliduojant suplanuotus nesupakuotus ir supakuotus užsakymus. |
| Gamybos kontrolė | Kopijuoti bendruosius maršrutus | Ši funkcija pagerina kopijavimo maršruto funkciją, leidžiančią vartotojams kopijuoti maršrutus, kurie nėra konkretūs prekei. Ji įgalina sistemą atnaujinti visą reikiamą informaciją (pavyzdžiui, svetainę, maršruto grupę, išteklių reikalavimus ir įvairius laikus) po to, kai maršruto kopijavimo funkcija buvo panaudota perrašyti maršrutui, dar nepriskirtam prie prekės. |
| Gamybos kontrolė | Atnaujinti susijusius išteklių reikalavimus, kai keičiama maršruto operacija | Ši funkcija leidžia sistemai atnaujinti susijusius išteklių reikalavimus, kai vartotojas pakeičia esamo maršruto veiksmo operaciją. |
| Produkto informacijos valdymas | Išankstinis komplektavimo specifikacijos ataskaitos apdorojimas, kad nesibaigtų skirtasis laikas | Dėl šios funkcijos komplektavimo specifikacijos ataskaita bus apdorota iš anksto. Taip išvengsite skirtojo laiko problemų, kai ataskaitoje bus didelė duomenų apkrova. |
| Paraiškos | Įjungti su įsigijimu susijusių darbo eigų nustatymą iš naujo | Ši peržiūros versijos funkcija leidžia jums iš naujo nustatyti šias darbo eigas į juodraščio būseną: Pirkimo užsakymo, Tiekėjo keitimo ir Pirkimo paraiškų. |
| Transportavimo valdymas | Įjungti tiekėjo SF žurnalo kūrimą, kai atmetama transportavimo sąskaita | Įgalinus šią funkciją, atitinkamas tiekėjo SF žurnalas bus sukurtas tik derinimo tikslais, kai naudojate mokėjimo tiekėjui parinktį. Kitu atveju, sąskaitos faktūros žurnalas visada bus sukurtas. |
| Sandėlio valdymas | Patvirtinti šablonus, pasirinktus papildymo užduotims | Ši funkcija padeda užtikrinti, kad nustatydami papildymo užduotį, vartotojai pasirinktų galiojančius papildymo šablonus. Tai neleidžia vartotojams kurti papildymo užduoties be šablono ir pasirinkti *Bangos poreikio* tipo šablonų, neleidžiančių kurti jokio papildymo darbo ir kurių apdorojimas gali ilgai užtrukti. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme ir reikšmingai atnaujinome tolesnes pagalbos temas. Jos nebūtinai yra susijusios su naujomis funkcijomis įtrauktomis į šį leidimą, kaip aprašyta ankstesniame skyriuje, bet gali padėti jums gauti daugiau iš esančių funkcijų.

| Funkcijos sritis | Naujos arba atnaujintos temos |
|---|---|
| Inžinerinių pakeitimų valdymas | [Produkto gyvavimo ciklo būsenos ir perlaidos](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Atsargų valdymas | [Atsargų matomumo papildinys](../inventory/inventory-visibility.md)<br><br>[Kokybės ir neatitikimo valdymo peržiūra](../inventory/quality-management-processes.md) (įskaitant visas susijusias kokybės valdymo temas) |
| Paraiškos | [Tiekėjo sertifikavimo priežiūra](../../finance/public-sector/manage-vendor-certification.md) |
| Gamybos kontrolė | [Gamybos vietos vykdymo sąsajos stilius](../production-control/production-floor-execution-styles.md) |
| Sandėlio valdymas | [„Warehouse Management” mobiliųjų įrenginių programėlės veiksmų piktogramų ir pavadinimų priskyrimas](../warehousing/step-icons-titles.md)<br><br>[Atidėtas atsargų perkėlimo neautomatinis apdorojimas](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>„Finance and Operations” programų platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.20 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [„Finance and Operations” programų 10.0.20 versijos platformos naujinimai (2021 m. liepos mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.20 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>„Dynamics 365“: 2021 m. 1-os leidimo bangos planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Peržiūrėkite [„Dynamics 365“: 2021 m. 1-os leidimo bangos planas](/dynamics365-release-plan/2021wave1/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Temoje [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) aprašomos „Supply Chain Management“ funkcijos, kurios yra pašalintos, yra suplanuotos pašalinti arba yra pasenusios.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant iš produkto bet kokią funkciją, pranešimas apie nebenaudojimą bus paskelbtas [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) temoje 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
