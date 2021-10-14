---
title: Kas nauja ar pasikeitė 10.0.19 „Dynamics 365 Supply Chain Management” versijoje (2021 m. birželis)
description: Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Supply Chain Management“ 10.0.19 versijos funkcijos.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7c8994a11c9d1d90fd8b66b17900248f941e307b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579789"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Kas nauja ar pasikeitė 10.0.19 „Dynamics 365 Supply Chain Management” versijoje (2021 m. birželis)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.19 versijos funkcijos. Šios versijos komponavimo numeris yra 10.0.837 ir jis pasiekiamas tokius būdu:

- **Vertinimo versijos leidimas:** 2021 m. balandžio mėn.
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2021 m. birželis
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2021 m. birželis

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos šiame leidime. Priemonės *stulpelyje* pateikiami saitai [į paleidimo](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) planą, kur matysite oficialias kiekvienos priemonės paleidimo datas. Stulpelyje *Daugiau informacijos* pateikiama išsami informacija ir (arba) nuorodos į susijusius dokumentus.

Daugumą šių funkcijų reikia įjungti naudojant [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad galėtumėte jomis naudotis.

| Funkcijos sritis | Funkcija | Daugiau informacijos |
|---|---|---|
| Atsargos&nbsp;ir&nbsp;logistika | [Patvirtinti ir įrašyti tiekėjo pateiktą banko informaciją](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Tiekėjo banko sąskaitos informacijos priežiūra](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Atsargos ir logistika | [Kontaktinio asmens duomenų objekto eksportavimo optimizavimas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Įgalinus šią funkciją, dėl nurodytų duomenų pakeitimų, susiję kontaktai nebus įtraukti į kitą didėjantį eksportavimą. Išjungus šią funkciją, dėl nurodytų duomenų pakeitimų, susiję kontaktai bus įtraukti į kitą didėjantį eksportavimą. |
| Atsargos ir logistika | [Sandėlio vykdymo galimybių papildantys patobulinimai su skalės vienetais](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Pranešimų procesoriaus pranešimai](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Sandėlio atsargų koregavimas](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Sandėlio valdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Atsargos ir logistika | [Pardavimo pasiūlymo puslapio laukų Dokumento įžanga ir Dokumento išvada peržvalgos funkcija](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Ši funkcija prideda peržvalgos funkciją laukams **Dokumento įžanga** ir **Dokumento išvada**, esantiems **Pardavimų pasiūlymo** puslapyje.<br><br>Pagal numatytuosius nustatymus ši funkcija įjungta. |
| Atsargos ir logistika | [Sandėlio vykdymas su kraštų skalės vienetais pasirinktoje aparatūroje](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Įdiekite „Edge" skalės vienetus pasirinktoje aparatūroje naudodami LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Gamyba | [Gamybos su kraštų skalės vienetais pasirinktoje aparatūroje](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Įdiekite „Edge" skalės vienetus pasirinktoje aparatūroje naudodami LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planuojama | Užklausa pagrįstas suplanuoto užsakymo virtimas | [Galutinai suplanuoti užsakymai](../master-planning/planning-optimization/planned-order-firming.md) |
| Produkto informacijos valdymas | [Siūlomų variantų puslapio patobulinimai](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Iš anksto apibrėžtų produkto variantų kūrimas](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip). Jei norite naudoti bet kurią iš šių funkcijų, turite ją tiesiogiai įgalinti [Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funkcijos sritis | Funkcijos&nbsp;pavadinimas&nbsp;funkcijos&nbsp;valdyme | Daugiau informacijos |
|---|---|---|
| Pardavimas ir rinkodara | Pardavimų retrospektyvos valymo efektyvumo patobulinimai | Pardavimų retrospektyvos valymas gali ilgai užtrukti, jei jis nedažnai vykdomas aplinkose, kuriose yra didelis pardavimų naujinimų kiekis. Siekiant sumažinti trukmę ir pagerinti patikimumą, ši funkcija išskaido valymą į paketus, kurie paleidžiami ribotam laikui. Ten, kur įmanoma, duomenų bazės galimybės bus sverto, kad valymo metu būtų sumažintas užrakinimas ir būtų išvengta operacinių lentelių prijungimo. |
| Pardavimas ir rinkodara | Atnaujinti pageidaujamą gavimo datą su patvirtinimo data vidinės įmonės užsakymams | Ši funkcija leidžia jums kontroliuoti, kas atsitiks pardavimo ir pirkimo datų laukų reikšmėms, kai naudojamas vidinės įmonės tiesioginis pristatymas. Galite pasirinkti tai, ar sistema atnaujins pageidaujamas datas, ar praleis jų atnaujinimą. Jei praleisite atnaujinimą, pageidaujamos datos atspindės kliento pageidavimus. Jei įgalinate atnaujinimą, pageidaujamos datos (naudojant pristatymo datos valdiklį) tik iš pradžių nurodo tai, ko prašė klientas. Pristatymo datos valdiklis, skirtingas nei *Nėra*, nepaisys to, ko iš pradžių buvo pareikalauta. Šią parinktį galite nustatyti naudodami naują nustatymą **Atnaujinti pageidaujamą gavimo datą Patvirtinta data**, esantį vidinės įmonės tiekėjo arba kliento nustatymuose.<br><br>Jei funkcija išjungta, sistema perrašys pageidaujamą gavimo datą pradiniame pardavimo užsakyme remdamasi pristatymo datos valdymo taisykle, tačiau pageidaujama siuntimo data liks nepakeista. |
| Sandėlio valdymas | Suapvalinti kiekius iki artimiausio pardavimo vieneto išleidžiant į sandėlį | Ši funkcija įtraukia parinktį, kuri gali riboti užsakymų kiekius išleidimo į sandėlį metu. Kai ji įgalinta, užsakymo kiekiai bus suapvalinti iki artimiausio pilno pardavimo vieneto, o užsakymų, kurių kiekiai yra mažesni nei vieno pardavimo vienetas, išleidimas bus atmestas. |
| Sandėlio valdymas | Visos organizacijos bangos metodas „Planuoti darbo kūrimą“ | Įgalinus šią funkciją, bangos metodas *Darbo kūrimo grafikas* bus sukonfigūruojamas veikti lygiagrečiai visuose juridiniuose subjektuose. Taip pat bus paveikti keli papildomi parametrai. Išsamią informaciją rasite [Darbo kūrimo planavimas bangos metu](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme ir reikšmingai atnaujinome tolesnes pagalbos temas. Jos nebūtinai yra susijusios su naujomis funkcijomis įtrauktomis į šį leidimą, kaip aprašyta ankstesniame skyriuje, bet gali padėti jums gauti daugiau iš esančių funkcijų.

| Funkcijos sritis | Naujos arba atnaujintos temos |
|---|---|
| Inžinerinių pakeitimų valdymas | [Inžinerinių pakeitimų valdymo DUK](../engineering-change-management/change-management-faq.md) |
| Paraiškos | [Kategorijų užklausos iš tiekėjų](../procurement/category-requests-from-vendors.md) |
| Produkto informacijos valdymas | [Matavimo vieneto valdymas](../pim/tasks/manage-unit-measure.md)<br><br>[Produkto konfigūracijos modelio skaičiavimai](../pim/config-model-calculations.md) |
| Gamybos kontrolė | [Bendra užduočių ID numerių seka](../production-control/unified-job-ids.md) |
| Transportavimo valdymas | [LTL klasės](../transportation/ltl-class.md)<br><br>[NMFC kodai](../transportation/nmfc-codes.md) |
| Sandėlių valdymas, bangos kūrimas ir apdorojimas | [Bangos kūrimas ir apdorojimas](../warehousing/wave-processing.md)<br><br>[Sandėlio parametrai bangos apdorojimui](../warehousing/wave-warehouse-parameters.md)<br><br>[Bangos šablonai](../warehousing/wave-templates.md)<br><br>[Bangos paskirstymas](../warehousing/wave-allocation-method.md)<br><br>[Darbo kūrimo bangos metu planavimas](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Krovimas į konteinerius](../warehousing/wave-containerization.md)<br><br>[Bangos vykdymo pranešimai](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>„Finance and Operations” programų platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.19 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, skaitykite [„Finance and Operations” programų 10.0.19 versijos platformos naujinimai (2021 m. birželis)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.19 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

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
