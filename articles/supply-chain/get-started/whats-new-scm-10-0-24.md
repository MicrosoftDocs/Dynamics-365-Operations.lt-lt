---
title: Kas nauja ar pasikeitė „Dynamics 365 Supply Chain Management“ 10.0.24 (2022 m. vasario mėn.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.24 funkcijos.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: a254e20dd7fcc29ca520282b4bf9fcd903e4de58
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087555"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Kas nauja ar pasikeitė „Dynamics 365 Supply Chain Management“ 10.0.24 (2022 m. vasario mėn.)

[!include [banner](../includes/banner.md)]

Ši tema išvardyja funkcija, kurios yra naujos arba pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.24 versijoje. Šios versijos komponavimo numeris yra 10.0.1084 ir jis pasiekiamas tokius būdu:

- **Išleidimo peržiūra:** 2021 m. gruodžio mėn
- **Bendras leidimo prieinamumas (savaiminis naujinimas):** 2022 m. sausio mėnuo
- **Bendras leidimo prieinamumas (automatinis naujinimas):** 2022 m. vasario mėnuo

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Galime atnaujinti šią temą, kad būtų įtraukti funkcijų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Paskirstyta taip pat topologija | [Patobulintas sandėlio vykdymo darbo krūvis masto vienetuose](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Sandėlio valdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams](../cloud-edge/cloud-edge-workload-warehousing.md) | Įgalinta pagal numatytąjį nustatymą. |
| Paskirstyta taip pat topologija | [Pradėkite gamybos užsakymą dėl sandėlio valdymo darbo krūvio debesies ir krašto masto vienetui](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [Gamybos vykdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams](../cloud-edge/cloud-edge-workload-manufacturing.md) | Funkcijų valdymas (*Pradėkite gamybos užsakymą dėl sandėlio valdymo darbo krūvio debesies ir krašto masto vienetui*)  |
| Planuojama | [Planavimo optimizavimo palaikymas, susijęs su pakartotinio užsakymo marža ir išdavimo marža](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Laiko rezervai](../master-planning/planning-optimization/safety-margins.md) | Įgalinta pagal numatytąjį nustatymą. |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti kurią nors iš šių funkcijų, turite tai padaryti [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Gamybos kontrolė | Gamybos užsakymų medžiagų pasiekiamumo pareikalavus patikra | Ši funkcija leidžia greičiau atidaryti **Gamybos užsakymai išleisti** puslapį, kurį galite rasti iš **Gamybinių grindų valdymas** darbo vieta. Be šios funkcijos, sistema automatiškai patikrina, ar yra prieinamos medžiagos visiems išvardytiems gamybos užsakymams, kai tik atidarote puslapį, o tai gali užtrukti daug laiko, jei turite daug užsakymų. Kai ši funkcija įjungta, sistema pateikia įrankių juostos mygtuką, kurį galite naudoti norėdami pradėti tik pasirinktų užsakymų medžiagų patikrą ir tada, kai to reikia. |
| Gamybos kontrolė | (Peržiūros versija) Registruokite medžiagų suvartojimą gamybos vietos vykdymo sąsajoje (ne WMS) | Ši funkcija leidžia darbuotojams naudoti gamybos grindų vykdymo sąsają medžiagų suvartojimui, partijų numeriams ir serijos numeriams registruoti. Ši funkcija palaiko tik tuos elementus, kuriems neleidžiama naudoti išplėstinių sandėlio procesų (WMS). Ateityje numatomas elementų, kuriuose įgalinta WMS, palaikymas.<p>Kai kurie gamintojai, ypač perdirbimo pramonės įmonės, turi aiškiai registruoti sunaudotos medžiagos kiekį kiekvienai partijai arba gamybos užsakymui. Pavyzdžiui, darbuotojai gali naudoti svarstykles, kad pasvertų darbo metu sunaudotos medžiagos kiekį. Siekdamos užtikrinti visišką medžiagų atsekamumą, šios organizacijos taip pat turi registruoti, kurių partijų numeriai buvo sunaudoti gaminant kiekvieną produktą. |
| Gamybos kontrolė | Pranešti, kai bus baigta su sandėlio valdymo darbo krūviu debesies ir briaunos skalės įrenginyje | Ši funkcija leis darbuotojams naudoti Sandėlio valdymo programą mobiliesiems, kad praneštų apie gamybos arba partijos užsakymą kaip baigtą, kai programa veikia pagal sandėlio valdymo darbo krūvį debesies arba krašto masto vienete. Daugiau informacijos žr [Praneškite kaip baigtą ir padėkite ant mastelio vieneto](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Sandėlio valdymas | Nauji apkrovos planavimo darbastalio puslapiai | Įgalinami du nauji apkrovos planavimo darbastalio puslapiai: **Įeinančios apkrovos planavimo darbastalis** ir **Išeinančių apkrovų planavimo darbastalis**. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme ir reikšmingai atnaujinome tolesnes pagalbos temas. Šios temos nebūtinai susijusios su naujomis funkcijomis, kurios buvo pridėtos prie šio leidimo, kaip išvardyta ankstesniame skyriuje. Tačiau jos gali padėti gauti daugiau informacijos apie esamas funkcijas.

| Funkcijos sritis | Naujos arba atnaujintos temos |
|---|---|
| Kaštų valdymas | [Atsargų vertės ataskaitos](../cost-management/inventory-value-report-storage.md) |
| Kaštų valdymas | [Atsargų vertės ataskaitos pavyzdžiai ir logika](../cost-management/inventory-value-report-examples.md) |
| Bendrasis planavimas | [Datos ir laiko parametrai, naudojami „Planning Optimization“](../master-planning/planning-optimization/date-time-used.md) |
| Bendrasis planavimas | [Poreikio prognozavimo nustatymas](../master-planning/demand-forecasting-setup.md) |
| Bendrasis planavimas | [Pakankamų atsargų žurnalo naudojimas mažiausiam prekių padengimui atnaujinti](../master-planning/safety-stock-journal.md) |
| Gamybos kontrolė | [Gamybos vietos vykdymo sąsajos tinkinimas](../production-control/production-floor-execution-customize.md) |
| Gamybos kontrolė | [Gamybos vietos vykdymo sąsajos stilius](../production-control/production-floor-execution-styles.md) |
| Pardavimas ir rinkodara | [Pardavimo istorijos valymo našumo patobulinimai](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Sandėlio valdymas | [Mobiliojo įrenginio vartotojų paskyros](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Programų „Finance and Operations“ platformos naujiniai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.24 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr [„Finance and Operations“ programų 10.0.24 versijos platformos naujiniai (2022 m. vasario mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.24 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>"Dynamics 365" ir pramonės debesys: 2021 išleidimo bangos 2 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2021 išleidimo bangos 2 planas](/dynamics365-release-plan/2021wave2/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Temoje [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) aprašomos „Supply Chain Management“ funkcijos, kurios yra pašalintos, yra suplanuotos pašalinti arba yra pasenusios.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant iš produkto bet kokią funkciją, pranešimas apie nebenaudojimą bus paskelbtas [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) temoje 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
