---
title: „Dynamics 365 Supply Chain Management” peržiūros versija 10.0.26 (2022 m. gegužės mėnesis)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.26 funkcijos.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 2b39eef816aaa383f0f8cbf1b2c308a6eafebd8f
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524443"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10026-may-2022"></a>„Dynamics 365 Supply Chain Management” peržiūros versija 10.0.26 (2022 m. gegužės mėnesis)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje pateikiamos priemonės, kurios yra naujos arba pakeistos "Microsoft Dynamics 365 Supply Chain Management preview" versijoje 10.0.26. Šios versijos komponavimo numeris yra 10.0.1192 ir jis pasiekiamas tokius būdu:

- **Peržiūros versijos išleidimas:** 2022 m. kovas
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2022 m. balandis
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. gegužė

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Galime atnaujinti šią temą, kad būtų įtraukti funkcijų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Atsargos ir logistika | [Turimų atsargų matomumo užklausa, kad būtų palaikomos patobulintos sandėlio valdymo prekės](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | Jau greitai | Priemonių valdymas:<br>*Įgalinti sandėlio prekes atsargų matomumo skiltyje* |
| Atsargos ir logistika | [Prieinamų atsargų matomumo priedo atsargos](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Turimų atsargų matomumo grafikai ir prieinamos atsargos](../inventory/inventory-visibility-available-to-promise.md) | Įgalina aptarnavimo konfigūracija |
| Gamyba | [Gamybos laiko vykdymo sąsajos esamo svorio elementai](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Kaip darbuotojai naudoja gamybos vietos vykdymo sąsają](../production-control/production-floor-execution-use.md) | Priemonių valdymas:<br>*(Peržiūros versija) Ataskaita apie esamo svorio prekes iš gamybos vietos vykdymo sąsajos* |
| Gamyba | Mano užduočių skirtukas gamybos vietos vykdymo sąsajoje <!-- KFM: Add link to release plan when available --> | [Kaip darbuotojai naudoja gamybos vietos vykdymo sąsają](../production-control/production-floor-execution-use.md) | Priemonių valdymas:<br>*Mano užduočių skirtukas gamybos vietos vykdymo sąsajoje* |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti bet kurią iš šių priemonių, tai turite atlikti funkcijų [valdymo metu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Paraiškos | Registruoti užregistruotus atsargose laikomų produktų kiekius ir atsargose nelaikomų produktų likučius kvituose bei tiekėjo sąskaitose faktūrose | Ši funkcija keičia, kaip registruojami ne atsargose produktų kiekiai (pvz., paslaugos), kai apdorojamos tiekėjo SF ir atvežimo siuntos pagal pirkimo užsakymus. Ši funkcija *modifikuoja* *užregistruoto* kiekio ir paslaugų kiekio parinkties elgseną registruojant gavimo kvitus ir tiekėjo SF, pakeisdami ją taip, kad atitiktų užregistruoto kiekio ir ne atsargose produktų parinkties elgseną, jau pateiktą registruojant pardavimo važtaraščių kiekius.<br><br>Kai registruojate *produkto* gavimo kvitą arba tiekėjo SF naudodami pasirinktį Užregistruotas kiekis ir paslaugų kiekis, sistema užregistruoja užregistruotą atsargose produktų kiekį ir užregistruoja likutį nesu atsargose neturių produktų (įskaitant paslaugas ir ne paslaugas). Be šios priemonės sistema vis tiek registruoja registruotą atsargose esančių produktų kiekį (įskaitant paslaugas, sukonfigūruotas kaip atsargose atsargose) bet visada registruoja visą ne atsargose esančių aptarnavimo produktų kiekį (*ir* nepaiso ne paslaugų tipo produktų). |
| Paraiškos | Sinchronizuoti stebėjimo dimensijas vidinės įmonės pardavimo ir pirkimo užsakymų eilutėse | Ši funkcija leidžia kontroliuoti, ar serijos ir paketo numerio sekimo dimensijos sinchronizuojamos tarp vidinės įmonės pardavimo ir pirkimo užsakymo eilučių. Ji įtraukia naujus parametrus į klientų **ir** **tiekėjų** vidinės įmonės nustatymo puslapio pirkimo užsakymo strategijas **ir** pardavimo užsakymų strategijų skirtukus. Ji taip pat atnaujina kelių susijusių, artimų parametrų pavadinimus.<br><br>Jei naudojate išplėstinį sandėlio valdymą (WMS), žinokite, kad ši funkcija sinchronizuos paketo ir serijos numerius tik tada, kai tos dimensijos yra virš vietos paskirties rezervavimo hierarchijoje. |
| Produkto informacijos valdymas | Išvalyti produkto atributų vertes | Ši funkcija įtraukia periodinę **užduotį**, pavadintą Valyti produkto atributų vertes, kurios valo produkto atributo verčių įrašus, kurie nebeatitinka jokio produkto per produkto kategoriją. |
| Atsargų ir sandėlio valdymas | (Rusija) Užkirstas kelias neatitikimams išduodant pirkimo užsakymų, apimančių WMS prekes, GTD | Ši funkcija skirta tik rusiškai lokalizacijai. Neleidžiama vykdyti neatitikimų išduodant Rusijos muitinės deklaravimo numerius (GTD) importo pirkimo užsakymams, kuriuose yra prekių, įgalintų išplėstinį sandėliavimą (WMS). GTD išdavimo procesas pakeičia kai kurias atsargų dimensijų vertes susijusiose į pasirinktinį žurnalą įtrauktų SF atsargų operacijose, dėl to gali nesutapti pirkimo užsakymo darbo įrašai ir pirkimo atsargų operacijos. Kai ši funkcija įgalinta, GTD išdavimo procesas sugeneruoja koregavimo darbą, dėl to tokie nesutapimai yra pašalinama. |
| Sandėlio valdymas | Išplėstiniai GS1 brūkšninių kodų analizatoriai | Ši funkcija įtraukia išplėstinį GS1 simbolių duomenų analizatorių. Naujas analizatorius įdiegia GS1 bendrosios specifikacijos algoritmą, naudojamą GS1 simboliams išanalizuoti, ir pateikia bendresnio duomenų tikrinimo procesą. |
| Sandėlio valdymas | Nauji krovinio planavimo darbo srityje puslapiai | Įtraukia du naujus krovinio planavimo darbo vietos puslapius: **gaunamo krovinio planavimo darbo srityje** **ir siunčiamo krovinio planavimo darbo srityje**. |
| Sandėlio valdymas | Programa „Warehouse Management“ – tuščia GTD vertė | Ši funkcija skirta tik rusiškai lokalizacijai. Joje darbuotojai, naudojantys sandėlio valdymo mobiliąją programą, prireikus gali palikti Rusijos muitinės deklaracijų numerius (GTD) tuščius. Jei GTD sekimo dimensija nustatyta taip, kad būtų leidžiamos tuščios vertės, sistema priims tuščias ATSARGŲ operacijų, kurios turimos turimos atsargos, GTD vertes. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme ir reikšmingai atnaujinome tolesnes pagalbos temas. Šios temos nebūtinai susijusios su naujomis funkcijomis, kurios buvo pridėtos prie šio leidimo, kaip išvardyta ankstesniuose skyriuose. Tačiau jos gali padėti gauti daugiau informacijos apie esamas funkcijas.

| Funkcijos sritis | Naujos arba atnaujintos temos |
|---|---|
| Kaštų valdymas | Atnaujinti pavyzdžiai ir diagramos buvo pridėti prie kiekvienos iš šių temų:<ul><li>[FIFO su faktine verte ir žymėjimu](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO su faktine verte ir žymėjimu](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO data su faktine verte ir žymėjimu](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Einamoji vidutinė savikaina](../cost-management/running-average-cost-price.md)</li><li>[Svertinis vidurkis su faktine verte ir žymėjimu](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |
| Paraiškos | [Pirkimo užsakymo eilutės duomenų nesutapimai](../troubleshooting/procurement/purchase-order-line-data-issues.md) |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.26 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.26 versijos platformos naujinimus (2022 m. gegužės mėn.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md)).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.26 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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