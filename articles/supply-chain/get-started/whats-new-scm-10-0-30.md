---
title: „Dynamics 365 Supply Chain Management“ peržiūra 10.0.30 (2022 m. lapkritis)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos programoje Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 477b27bf77d2a3ef91a5c2d39f2dfb06d8ad4e59
ms.sourcegitcommit: 562ea02e1f7409f18ee1cc4750a838bff4381e91
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429129"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10030-november-2022"></a>„Dynamics 365 Supply Chain Management“ peržiūra 10.0.30 (2022 m. lapkritis)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiamos priemonės, kurios yra naujos arba pakeistos "Microsoft Dynamics 365 Supply Chain Management preview" versijoje 10.0.30. Ši versija turi versijos 10.0.1362 versiją ir yra pasiekiama šiame grafike:

- **Peržiūros leidimas:** 2022 m. rugsėjo mėn.
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2022 m. spalio mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. lapkričio mėn.

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šį straipsnį.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Gamyba | [Stebėti įrangą su jutiklio duomenų įžvalgomis](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Jutiklio duomenų tyrimų pagrindinis puslapis](../sensor-data-intelligence/sdi-home-page.md) | Priemonių valdymas:<br>*(Peržiūros versija) Jutiklio duomenų įžvalgos* |
| Sandėlio valdymas | „Warehouse Management“ mobiliųjų įrenginių programos kelių lygių apėjimas <!-- KFM: Add link when RP updates --> | [Mobiliojo įrenginio meniu elementų aplinkinių veiksmų konfigūravimas](../warehousing/warehouse-app-detours.md) | Priemonių valdymas:<br>*„Warehouse Management“ mobiliųjų įrenginių programos kelių lygių apėjimas* |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti bet kurią iš šių priemonių, tai turite atlikti funkcijų [valdymo metu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Gamybos kontrolė | Turimos gamybos užsakymų informacijos, kurią reikia pateikti puslapyje | Įtraukia turimų atsargų kiekio **stulpelį eilutės prekei gamybos užsakymų, kurie bus paleisti puslapyje, eilučių skyriuje**. |
| Transportavimo valdymas | Priskirti siuntas susijusiems maršruto segmentams | Ši funkcija leidžia sistemai tiksliau padalinti siuntos transportavimo išlaidas, įskaitant krovinius su keliomis siuntomis, pristatytais į įvairias segmento paskirties vietas viename maršrute. Kiekvieną siuntą ji priskiria labiausiai tinkamam maršruto segmentui, remiantis siuntos paskirties adresais ir segmentu. Tada priemonė apskaičiuoja kiekvienos siuntos transportavimo išlaidas kaip visos krovinio savikainos dalį, remiantis susijusiu siuntos svoriu, kiekiu, kiekiu ir nukeliaus atstumu. Ši funkcija taikoma tik siuntoms, valdooms naudojant modulį Transportavimo valdymas (TMS). |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.30 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.30 versijos (2022 m. lapkričio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md) platformos naujinimus. <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti informacijos apie klaidos pataisas, įtrauktas į visus naujinimus, kurie yra 10.0.29 versijos dalis, prisiregistruokite prie ciklo tarnybų (LCS) [ir peržiūrėkite žinių bazės straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>"Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 2 planas](/dynamics365-release-plan/2022wave2/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Straipsnyje [pašalintos arba pasenusios Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funkcijos aprašomos priemonės, kurios buvo arba yra suplanuotos pašalinti arba pasenusios tiekimo grandinės valdymui.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant bet kokią priemonę iš produkto, [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) pranešimai dėl nušalinimo bus pereiti prie pašalintų arba pasenusių funkcijų 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
