---
title: „Dynamics 365 Supply Chain Management“ peržiūra 10.0.22 (2021 m. lapkritis)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.22 funkcijos.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4aac62b36cd271e1c5fc3bcbbfdd785963fc368
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2021
ms.locfileid: "7484077"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>„Dynamics 365 Supply Chain Management“ peržiūra 10.0.22 (2021 m. lapkritis)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje pristatomos funkcijos, kurios yra naujos arba pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.22 peržiūros versijoje. Šios versijos komponavimo numeris yra 10.0.995 ir jis pasiekiamas tokius būdu:

- **Peržiūros leidimas:** 2021 m. rugsėjo mėn.
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2021 m. spalio mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2021 m. lapkričio mėn.

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Priemonės *stulpelyje* pateikiami saitai [į paleidimo](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) planą, kur matysite oficialias kiekvienos priemonės paleidimo datas. Stulpelyje *Daugiau informacijos* pateikiama išsami informacija ir (arba) nuorodos į susijusius dokumentus. Norėdami nustatyti, kaip įjungti funkciją, žr. stulpelį *Įgalinta pagal*. Daugiau informacijos kaip naudoti funkcijų valdymą žr. [Funkcijos valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Galime atnaujinti šią temą, kad būtų įtraukti funkcijų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė |
|---|---|---|---|
| Planuojama | [Pajėgumų paskirstymo planavimo optimizavimo palaikymas](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Planavimas su išteklių pasirinkimu pagal pajėgumą](../master-planning/planning-optimization/capability-based-scheduling.md) | Funkcijos valdymas (*Neribotas pajėgumo planavimas Planavimo optimizavimui*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip). Jei norite naudoti bet kurią iš šių funkcijų, turite ją tiesiogiai įgalinti [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

| Funkcijos sritis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Kaštų valdymas | Kurti susijusius standartinių išlaidų apvalinimo perkainojimo kvitus | <p>Kai atliekamas atsargų finansinis registravimas (pvz., pardavimo užsakymo SF arba atsargų operacija), dėl šios funkcijos sistema sukuria atskirą kvitą, susijusį su standartinių išlaidų apvalinimo perkainojimu ir prideda jį prie finansinio registravimo kvito kaip susijęs kvitas.</p><p>Be šios priemonės, sistema įrašo standartinius išlaidų apvalinimo perkainojimus tą patį kvito registravimą. Dėl tokio veikimo būdo kartais gali kilti nesuderinamos datos informacijos, nes perkainojimas naudoja seansą arba sistemos datą, o finansiniai registravimas naudoja registravimo datą.</p> |
| Paskirstyta taip pat topologija | *(Funkcijos valdyti nereikia.)* | <p>Šis leidimas išplečia siuntimo krovinio planavimo galimybes sandėlio valdymo darbo krūviui debesies ir kraštų skalės vienetams.</p><p>Daugiau informacijos rasite [Sandėlio valdymo darbo krūviai debesies ir briaunos skalės vienetams](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Inžinerinių pakeitimų valdymas | Inžinierinių produktų variantų generavimas | <p>Ši priemonė leidžia sugeneruoti kelis inžinerijos produkto variantus, pagrįstus jo spalva, dydžiu, stilius ar konfigūracijos dimensijomis.</p><p>Daugiau informacijos ieškokite gamybos [produktų variantų gener kuriuos galima generuoti](../engineering-change-management/engineering-variants.md).</p> |
| Atsargų ir sandėlio valdymas | Inventoriaus matomumo integravimas su rezervavimo poslinkiu | <p>Šią funkciją galima įgalinti tik įjungus *atsargų matomumo integravimo* funkciją. Ji suteikia funkcijų, koresponduojanti rezervavimus, kurie atliekami atsargų matomumo metu.</p><p>Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](../inventory/inventory-visibility-reservations.md).</p> |
| Pardavimas ir rinkodara | Apribokite pardavimo užsakymų, kuriuos galima pasirinkti registruoti, skaičių | <p>Ši funkcija yra automatiškai įjungta. Priemonė prideda parametrą, laukelyje vadinamą **Maks. pardavimo užsakymų skaičiumi**, kad būtų galima registruoti puslapyje **Gautinų sumų** parametrai. Šis laukelis leidžia apibrėžti didžiausią pardavimo užsakymų, kuriuos galima pasirinkti registruojant patvirtinimus, išrinkimo dokumentus, važtaraščius ir SF iš pardavimo užsakymų sąrašo puslapio, skaičių. Numatytoji vertė yra *100*.</p><p>Priemonė padeda pagerinti pardavimo užsakymų sąrašo puslapio našumą, kai pasirenkamas pardavimo užsakymų jau skaičius. Tai neturi įtakos pardavimų užsakymų, kuriuos galima apdoroti periodine užduotimi, skaičiumii.</p> |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme ir reikšmingai atnaujinome tolesnes pagalbos temas. Šios temos nebūtinai susijusios su naujomis funkcijomis, kurios buvo pridėtos prie šio leidimo, kaip išvardyta ankstesniame skyriuje. Tačiau jos gali padėti gauti daugiau informacijos apie esamas funkcijas.

| Funkcijos sritis | Naujos arba atnaujintos temos |
|---|---|
| Inžinerinių pakeitimų valdymas | [Inžinerijos pakeitimų valdymo apžvalga](../engineering-change-management/product-engineering-overview.md) dabar pateikia visas susijusias, pasirinktines funkcijas, galimas funkcijų valdymui |
| Bendrasis planavimas | [Poreikio prognozavimo nustatymas](../master-planning/demand-forecasting-setup.md) |
| Bendrasis planavimas | [Grynieji poreikiai ir iškvietimo informacija naudojant planavimo optimizavimą](../master-planning/planning-optimization/net-requirements.md) |
| Sandėlio valdymas | [Išleisti į sandėlį](../warehousing/release-to-warehouse-process.md) pateikiama išsami viso išleidimo į sandėlį proceso apžvalga |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>„Finance and Operations” programų platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.22 versijoje yra platformos naujinimų. Dėl daugiau informacijos, žr. [Platformos naujinimas 10.0.22 „Finance and Operations“ programų versijai (2021 m. lapkričio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.22 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

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
