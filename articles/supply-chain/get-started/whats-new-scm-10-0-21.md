---
title: Peržiūros versija Dynamics 365 Supply Chain Management 10.0.21 (2021 m. spalis)
description: Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Supply Chain Management“ 10.0.21 versijos funkcijos.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42d296cb0402b5e96f23d628f08a28fb35683d5f
ms.sourcegitcommit: 5a44eb4f555bf5ee0b1293f0ecdc37ee8b53aa24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/17/2021
ms.locfileid: "7391213"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Peržiūros versija Dynamics 365 Supply Chain Management 10.0.21 (2021 m. spalis)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje pristatomos funkcijos, kurios yra naujos arba pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.21 peržiūros versijoje. Šios versijos komponavimo numeris yra 10.0.960 ir jis pasiekiamas tokius būdu:

- **Peržiūrėti leidimą:** 2021 m. rugpjūčio mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2021 m. rugsėjo mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2021 m. spalio mėn.

## <a name="known-deployment-issue"></a>Žinomas diegimo problema

Kai IaaS diegiamas 10.0.21 paleidimas, galite gauti tokį diegimo įspėjimą:

**Įspėjimo kodas:** 95017

**Perspėjimo pranešima:** Scenarijaus \[SetupDiagnostics\] nepavyko pagal VM

Nepaisant įspėjimo, diegimas bus veikia. Tačiau gali kilti tokių problemų, kurios gali kilti „Lifecycle Services“ (LCS):

- **Aplinkos stebėjimo** puslapyje **Rodoma išsamios versijos informacija** nebus rodoma saito rodinyje, todėl negalėsite matyti konkrečių jūsų aplinkoje įdiegtų modulių versijų. Be šių duomenų gali nepavykti įdiegti vėlesnių svarbių pataisų, nes procesas, kuris taiko svarbias pataisas, naudoja šį duomenis, kad galėtų patikrinti, ar yra įvykdytos būtinos modulio versijos sąlygos. Kadangi PEAP/Peržiūros versijos gamybos metu naudoti neįmanoma arba taikyti svarbių pataisų, poveikis turėtų būti mažiausias.
- **Veikimo metrikos** ir **Indekso analizės** skirtukai **Aplinkos stebėjimo** puslapyje, apačioje SQL žinių srityje, nerodo jokių duomenų. Visos kitos **Aplinkos stebėjimo** savybės veiks taip, kaip numatyta.
- **Pilnas sistemos diagnostikos** puslapis nebus pasiekiamas. Susiję duomenys apie naktinio surinkėjo veiklos būseną ir jos taisyklių aptiktos problemos taip pat nebus rodomos.

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos šiame leidime. Priemonės *stulpelyje* pateikiami saitai [į paleidimo](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) planą, kur matysite oficialias kiekvienos priemonės paleidimo datas. Stulpelyje *Daugiau informacijos* pateikiama išsami informacija ir (arba) nuorodos į susijusius dokumentus.

Daugumą šių funkcijų reikia įjungti naudojant [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad galėtumėte jomis naudotis. Kai kurios išvardytos funkcijos vis dar yra peržiūros versijos, o kitos funkcijos jau gali būti prieinamos bendrai.

| Funkcijos sritis | Funkcija | Daugiau informacijos |
|---|---|---|
| Atsargos&nbsp;ir&nbsp;logistika | [Visuotinė atsargų apskaita yra Dynamics 365 Supply Chain Management papildinys.](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Visuotinės atsargų apskaitos pagrindinis puslapis](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Atsargos&nbsp;ir&nbsp;logistika | [Registruoti turimų atsargų koregavimus naudojant kodus, prijungtus prie korespondentinės sąskaitos](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Atsargų skaičiavimo priežasčių kodai](../warehousing/reason-codes-for-counting-journals.md) |
| Atsargos&nbsp;ir&nbsp;logistika | [Pardavimo pasiūlyme nurodyta duomenų eksportavimo politika](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Pasirinkite ar nurodytų duomenų pakeitimai į kitą papildomą eksportavimą nebus įtraukti susiję pardavimo pasiūlymai (ar eilutės). Jei pasirinksite neįvesti šių pasiūlymų ar eilučių, jūsų papildomi eksportavimai bus atlikti daug greičiau.<br><br>Ši funkcija įtraukia parametrą, vadinamą **Praleisti pardavimo pasiūlymą nurodomomis duomenimis** į **Gautinų sumų parametrai** puslapį. |
| Atsargos&nbsp;ir&nbsp;logistika | [Nuskaityti brūkšninius kodus sandėlyje naudojant GS1 formato standartus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 brūkšniniai kodai ir QR kodai](../warehousing/gs1-barcodes.md) |
| Atsargos&nbsp;ir&nbsp;logistika | [Švelniai atsargų matomumo priedo rezervavimas](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Atsargų matomumo rezervavimai](../inventory/inventory-visibility-reservations.md) |
| Atsargos&nbsp;ir&nbsp;logistika | [Grąžinimo valdymo atskaitymo ir esamo svorio patobulinimai](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Atskaitymų valdymas, naudojant atskaitymų darbo sritį](../rebate-management/deduction-workbench.md )<br><br>[Grąžinimų apdorojimas, peržiūra ir registravimas](../rebate-management/process-review-post.md)<br><br>[Grąžinimų valdymo sandoriai](../rebate-management/rebate-management-deals.md) |
| Atsargos&nbsp;ir&nbsp;logistika | [Sandėlio programos veiksmo instrukcijos](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [„Warehouse Management“ mobiliųjų įrenginių programėlės veiksmų pavadinimų ir instrukcijų tinkinimas](../warehousing/mobile-app-titles-instructions.md) |
| Atsargos&nbsp;ir&nbsp;logistika | [Įkrovimo išlaidų darbo pertraukos ir sekimo naujinimai](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Naujinti atidėjimo stebėjimą](../landed-cost/update-tracking-putaway.md )<br><br>[Tranzito prekių apdorojimas](../landed-cost/in-transit-processing.md) |
| Bendrasis planavimas | [Planavimo optimizavimo neigiamos dienos](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Leistinas uždelsimo nuokrypis (neigiamos dienos)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip). Jei norite naudoti bet kurią iš šių funkcijų, turite ją tiesiogiai įgalinti [Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funkcijos sritis | Funkcijos&nbsp;pavadinimas&nbsp;funkcijos&nbsp;valdyme | Daugiau informacijos |
|---|---|---|
| Kaštų valdymas | Išsami informacija apie atsargų uždarymo eigą | Ši peržiūros priemonė leidžia išsamiai peržiūrėti atsargų uždarymo eigą. |
| Paraiškos | Užkirsti kelią bendro biudžeto rezervavimų pereikvojimui, kai darbo eigoje yra kelios pirkimo paraiškos | Ši peržiūros funkcija pagerina klaidų tikrinimą, kai vartotojai pateikia ir patvirtina pirkimo paraiškas, kurios viršija bendrojo biudžeto rezervavimo eilutės likusį balansą. Tai padeda išvengti bendrųjų biudžeto rezervavimų pervartojimo, kai darbo eigoje yra kelios pirkimo paraiškos. |
| Gamybos kontrolė | Rodyti visą serijos, paketo ir valstybinį numerius gamybos aukšto vykdymo sąsajoje | Ši funkcija gamybos laiko vykdymo sąsajoje pagerina serijos, paketo ir numerio lentelės numerių sąrašų peržiūros patirtį. Kortelės rodinio rodymo pakeitimai, naudojant ribotą simbolių skaičių, sąrašo rodinyje, kuriame yra pakankamai vietos, kad būtų galima parodyti visas vertes. Sąrašas taip pat siūlo galimybę ieškoti konkrečių skaičių. |
| Pardavimas ir rinkodara | Apribokite pardavimo užsakymų, kuriuos galima pasirinkti registruoti, skaičių | Ši funkcija leidžia apibrėžti didžiausią pardavimo užsakymų, kuriuos galima pasirinkti registruojant patvirtinimus, išrinkimo dokumentus, važtaraščius ir SF iš pardavimo užsakymų sąrašo puslapio, skaičių. Jis įgalinamas automatiškai. Priemonė prideda parametrą, vadinamą **Maks. pardavimo užsakymų skaičiumi**, kad būtų galima registruoti puslapyje **Gautinų sumų** parametrai. Naujo nustatymo numatytoji vertė yra *100*. Priemonė padeda pagerinti pardavimo užsakymų sąrašo puslapio našumą, kai pasirenkamas pardavimo užsakymų jau skaičius. Tai neturi įtakos pardavimų užsakymų, kuriuos galima apdoroti periodine užduotimi, skaičiumii. |
| Sandėlio valdymas | Atskirti atidėjimo darbą nuo ASN | Ši funkcija yra būtina norint siųsti ir gauti išankstinius siuntimo pranešimus (ASN), kai naudojate sandėlio valdymo darbo krūvį svarstyklių vienetais (kaip paskirstytos kokybės topologijos dalį). Ji prideda naują duomenų bazės lentelę, skirtą saugoti informaciją apie atidėtą darbą. Anksčiau ši informacija buvo saugoma lentelėse, naudojamose ir ASN. |
| Sandėlio valdymas | Atkarpos mišrūs vienetai | Leidžia sistemai atsekite prekes į vietas, kuriose yra įvairūs vienetai (pvz., tiek dėžės, tiek ir aplankalai). Kiekvienoje laiko atminties šablono eilutėje ši funkcija leidžia pasirinkti, ar eilutė turėtų atsekti prekes į skirtingų vienetų, ar į vienodo vieneto vietas. |
| Sandėlio valdymas | Naudokite greitesnę API, jei norite uždaryti / iš naujo atidaryti konteinerius pakavimo stotyje | Kai ši peržiūros funkcija įgalinta, atsargų operacijos, susijusios su konteineriais, sukuriamos naudojant naują nesvarbų svorio procesą, kuris padidina konteinerių uždarymo ar atidarymo iš naujo našumą rankinio pakavimo stoties apdorojimo metu. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme ir reikšmingai atnaujinome tolesnes pagalbos temas. Jos nebūtinai yra susijusios su naujomis funkcijomis įtrauktomis į šį leidimą, kaip aprašyta ankstesniame skyriuje, bet gali padėti jums gauti daugiau iš esančių funkcijų.

| Funkcijos sritis | Naujos arba atnaujintos temos |
|---|---|
| Bendrasis planavimas | [Atsargų prognozės](../master-planning/inventory-forecast.md) |
| Bendrasis planavimas | [Planavimo optimizavimo nenaudojami parametrai](../master-planning/planning-optimization/not-used-parameters.md) |
| Bendrasis planavimas | [Papildymo metodai ir kiekio modifikavimas](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Bendrasis planavimas | [Planavimas su neribotu pajėgumu](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Bendrasis planavimas | [Plano retrospektyvos ir planavimo žurnalų peržiūra](../master-planning/planning-optimization/plan-history-logs.md) |
| Sandėlio valdymas | [Konteinerių pakavimo strategijos](../warehousing/container-packing-strategy-overview.md) |
| Sandėlio valdymas | [Ciklo skaičiavimo scenarijų pavyzdžiai](../warehousing/cycle-counting-scenarios.md) |
| Sandėlio valdymas | [Gaunamų ASN importavimas naudojant V2 duomenų objektą](../warehousing/import-asn-v2-data-entity.md) |
| Sandėlio valdymas | [Pardavimo ir perkėlimo užsakymų surinkimo viršijimas](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Sandėlio valdymas | [Bangos žymos spausdinimo bangos metu planavimas](../warehousing/configure-task-based-wave-label-printing.md) |
| Sandėlio valdymas | [Kas nauja ar pasikeitė „Warehouse Management Mobile App” programėlėje](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>„Finance and Operations” programų platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.21 versijoje yra platformos naujinimų. Dėl daugiau informacijos, žr. [Platformos naujinimas 10.0.21 „Finance and Operations“ programų versijai (2021 m. spalio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.21 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

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
