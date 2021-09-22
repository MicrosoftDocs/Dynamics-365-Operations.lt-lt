---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. rugpjūčio 23 d.
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. rugpjūčio 23 d.
author: marcelbf
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c9ee0206bd77a8a2ec42501d64e83077baef09
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441680"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. rugpjūčio 23 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Microsoft Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4419 komponavimo versijai.

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema | Aprašas |
| --- | --- | --- |
| 594066 | Kontaktinės informacijos panaikinti negalima | Kai pasirenkate naikinti darbuotojo kontaktinės informacijos įrašą, panaikinamas kitas nei pasirinktas įrašas kontaktinės informacijos įrašas. |
| 611339 | Įtraukus personalizavimą banko sąskaita nepaiso filtro ir išrena pirmą įrašą | Įtraukus personalizaciją banko sąskaitų sąrašas paleidžia personalizavimo užklausą po to, kai paleidžiama duomenų šaltinio užklausa, todėl užklausa surenką viršutinį įrašą neatsižvelgiant į darbuotoją, kurio informacija peržiūrima. |
| 591806 | Neteisingai apskaičiuotos termino užduotys | Terminai netinkamai apskaičiuojami, kai yra tokios sąlygos: sukurti kontroliniai sąrašai naudoja kalendorių, kuris naudoja išplėstą laiko intervalą (pvz., nuo 2005 iki 2050 m.), o vartotojo nuostatos naudoja kitą laiko juostą, nei centrinis standartinis laikas. |   
| 592749 | Darbuotojų savitarnoje atostogų **balansas neteisingas** | Jei darbuotojas įdarbino daugiau nei viename juridiniame subjekte ir įjungtas visų įmonių atostogų rodinys, atostogų balansas gali būti neteisingas. |
| 603133 | Netikėtas perspėjimas reikalaujant išjungti laiką | Jei prašote išjungti laiką, užpildę **pusės dienų** lauką prieš lauką **Suma** gausite netikėtą įspėjimą. |
| 606546 | Pasirinkti lauką, kad jis nebūtų matomas per patvirtintą laiką | Žymės langelis, norint pasirinkti keletą patvirtintų atostogų užklausų, nematomas. |
| 597059 | Darbuotojas nematomas **atostogų ir neatvykimų įmonės kalendoriuje** | Darbuotojas nematomas **atostogų ir neatvykimų įmonės kalendoriuje** jei taikomas datų diapazonas apima bet kurią dieną, kurios atostogų prašymas buvo atmestas. |


## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie tai, kaip įjungti ar išjungtas funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md)|
| Įgalinti neatvykimų vadovą valdyti atostogas | [Įgalinti neatvykimų vadovą valdyti atostogas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Naudodami šį leidimą mes atnaujiname neatvykimo vadybininko darbo srities rodinį. Daugiau informacijos žr. [Konfigūruoti nebuvimo vadovo vaidmenį](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigūruoti priedo reikalavimus atostogų tipui | [Konfigūruoti priedo reikalavimus atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Konfigūruoti atostogų vienetus kiekvienam atostogų tipui | [Konfigūruoti atostogų vienetus kiekvienam atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui | [Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Parengta mokėti](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Jau greitai

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Informacija |
| --- | --- |
| Platformos atnaujinimas 10.0.21 (45) | Platformos atnaujinimo atmetimas 10.0.21 yra suplanuotas pasirodyti su nauju leidimu 2021 m. spalio 4 d. Dėl daugiau informacijos, žr. [Platformos atnaujinimas „Finance and Operations“ programos 10.0.21 versijai (2021 m. spalio mėn.)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
