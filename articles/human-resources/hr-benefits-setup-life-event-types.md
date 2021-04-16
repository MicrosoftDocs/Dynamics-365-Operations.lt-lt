---
title: Gyvenimo įvykių tipų konfigūravimas
description: „Microsoft Dynamics 365 Human Resources“ vartotojų gyvenimo įvykių tipai, apibrėžiantys įvykius, kurie tinka darbuotojų išmokų registracijai atnaujinti.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44aecf003432bf803b5658f1eb89298d03f53423
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805639"
---
# <a name="configure-life-event-types"></a>Gyvenimo įvykių tipų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Dynamics 365 Human Resources“ vartotojų gyvenimo įvykių tipai, apibrėžiantys įvykius, kurie tinka darbuotojų išmokų registracijai atnaujinti. Pavyzdžiui, santuoka ar vaiko gimimas. Kiekvienas gyvenimo įvykio tipo ID gali būti susietas tik su vienu gyvenimo įvykio tipu. Pavyzdžiui, jei sukūrėte gyvenimo įvykio ID pavadinimu „Adreso pasikeitimas“, kuris yra susietas su gyvenimo įvykio tipu „Darbuotojo adreso pasikeitimas“, negalite sukurti kito ID pavadinimu „Darbuotojo adreso pasikeitimas“, ir susieti jį su gyvenimo įvykio tipu „Darbuotojo adreso pasikeitimas“. 

Sukūrę gyvenimo įvykių tipus, turite susieti juos su planų tipais. Daugiau informacijos žr. dalyje [Planų tipų kūrimas](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Sukūrę gyvenimo įvykio tipą, turite susieti jį su plano tipų. Daugiau informacijos žr. dalyje [Planų tipų kūrimas](hr-benefits-setup-life-event-types.md).

## <a name="create-a-life-event-type"></a>Kurti gyvenimo įvykio tipą

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Gyvenimo įvykių tipai**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Gyvenimo įvykio tipo ID** | Unikalus gyvenimo įvykio tipo identifikatorius. |
   | **Aprašymas** | Gyvenimo įvykio tipo aprašas. |
   | **Gyvenimo įvykio tipas** | Katalizatorius, skirtas atnaujinti darbuotojo išmokų registravimą. Gyvenimo įvykių sąrašą rasite toliau esančiame skyriuje [Gyvenimo įvykiai](hr-benefits-setup-payment-frequencies.md?life-events). |

4. Pasirinkite **Įrašyti**.

## <a name="view-attached-plans"></a>Peržiūrėti pridėtus planus

Galite peržiūrėti planų, pridėtų prie pasirinkto gyvenimo įvykio tipo, sąrašą. Gyvenimo įvykiai pridedami prie plano tipo, o planų tipai siejami su planu. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Gyvenimo įvykių tipai**.

2. Pasirinkite **Veiksmai**.

3. Pasirinkite **Pridėti planai**.

## <a name="life-events"></a>Gyvenimo įvykiai

Kurdami gyvenimo įvykio tipą galite rinktis iš šių gyvenimo planų:

| Gyvenimo įvykis | Vieta | Paleidiklis |
| --- | --- | --- |
| **Šeimyninės padėties pasikeitimas** | Darbuotojas > Profilis > Asmeninė informacija > Šeiminė padėtis| Šeimyninės padėties pasikeitimas |
| **Įdarbinimo būsenos pasikeitimas** | <ul><li>Darbuotojas > Įdarbinimas</li><li>Įdarbinimo retrospektyvos puslapis</li></ul> | Įdarbinimo būsenos pasikeitimas |
| **Darbuotojo adreso pasikeitimas** | <ul><li>Darbininkas > Profilis > Adresai </li><li>Darbininkas > Asmeninė informacija > Asmeniniai kontaktai > Adresas</li></ul> Įtrauktas, redaguotas ar panaikintas adresas |
| **Priklausomojo pasikeitimas** | <ul><li>Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Įtraukti arba naikinti priklausomąjį</li><li>Darbuotojų savitarna</li></ul> | Įtrauktas ar panaikintas priklausomasis. Asmeninio kontakto ryšys turi būti vaikas, sutuoktinis, civilinis partneris arba buvęs sutuoktinis. Atnaujinant datą **Galioja nuo** aktyvinamas gyvenimo įvykis. Jei neatnaujinsite šios datos, gyvenimo įvykis nebus aktyvintas. |
| **Gimimas ar įvaikinimas (priklausomasis)** | <ul><li>Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį</li><li>Darbuotojų savitarna</li></ul> | Pildomas laukas **Įvaikinimo data**. Reikia nurodyti vaiko gimimo datą. |
| **Padengimo praradimas (sutuoktinis / civilinis partneris)** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Padengimo praradimas | Asmeninio kontakto dalyje pasirenkama **Padengimo praradimas** ir **Įsigaliojimo data** |
| Partnerio užimtumo pasikeitimas | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Įdarbintas. | <ul><li>Sukuriamas priklausomojo išsamios informacijos įrašas ir laukas **Asmeninis kontaktas įdarbintas** nustatytas kaip „Taip“</li><li>Laukas **Asmeninis kontaktas įdarbintas** (taip arba ne)</li></ul> |
| **Atostogos (sutuoktinis / civilinis partneris)** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Atostogos | <ul><li>Sukuriamas priklausomojo išsamios informacijos įrašas ir užpildomas laukas **EhrLOAEffectiveDate**</li><li>Pasikeitė **personPrivateDetails.EhrIsLOA** (taip arba ne)</li><li>Pasikeitė **personPrivateDetails.EhrLOAEffectiveDate**</li></ul> |
| **Padengimo (pareigų) pasikeitimas** | <ul><li>Darbininkas > Pareigų priskyrimas > Darbininko pareigų priskyrimas</li><li>Pareigos > Pareigos</li></ul> | <ul><li>Pareigų pasikeitimas darbininko pareigų priskyrimo įrašuose</li><li>Darbininko priskyrimo pareigoms pasikeitimas</li></ul> |
| **Sveikatos draudimas (darbuotojas / priklausomasis)** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Sveikatos draudimo įsigaliojimo data | Automatiškai neaktyvinama, kai asmeninis kontaktas įveda įsigaliojimo datą. |
| **Teismo paskirta parama** | Darbuotojas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Priklausomasis > Court ordered support (QMSCO/QDRO) ir galiojimo datos | Nesuaktyvina jokių automatinių naujinimų. Neturi poveikio tinkamumui; įrašo gyvenimo įvykį. |
| **Mirė** | Darbininkas > Profilis > Asmeninė informacija > Mirties data | Įvesta mirties data |
| **Draudimo įrodymai** | <ul><li>Darbininkas > Darbininkas > Versijos > įdarbinimo retrospektyvos > Datos tvarkytuvas > Išmokos informacija</li><li> Darbininkas > Įdarbinimas > Išmokos informacija > Patikrinimo data</li></ul> | <ul><li>Darbininkas įveda patvirtinimo datą</li><li>Darbuotojas nustato lauką „EvidenceOfInsurability“ kaip **Taip**</li></ul> |
| **Gavėjas** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai | Įtraukiamas asmeninis kontaktas ir pildomi laukai **Gavėjas** ir **Įsigaliojimo data**. Asmeninis kontaktas turi būti tokio tipo: **vaikas**, **sutuoktinis**, **civilinis partneris**, **brolis ar sesuo**, **FamilyContact**, **OtherContact**, **vienas iš tėvų**, **BeneficiaryEstate**, **BeneficiaryOrg** arba **BeneficiaryTrust**. |
| **Darbuotojo sveikatos draudimas** | Darbininkas > Darbininkas > Versijos > įdarbinimo retrospektyvos > Datos tvarkytuvas > Išmokos informacija | <ul><li>Pasikeitė **EhrMedicareEligibilityDate**</li><li>**MedicareEligibile** nustatyta kaip **Taip**</li></ul> |
| **Gimtadienis** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Gimimo data | Gimimo data įtraukiama arba atnaujinama (ne po to, kai buvo atliktas gyvenimo įvykio keitimo apdorojimas). Pavyzdys. Jei einant į Sąranka > Išmokos > Asmeninio kontakto tinkamumo parinktys, laukas **Asmeninio kontakto tinkamumo parinktys** vaikui nustatomas kaip „Amžius: 26 m.“ ir personalo administratorius vykdo gyvenimo įvykio keitimo apdorojimą bet kada po to, kai priklausomajam suėjo 26 m., rodomas pranešimas, įspėjantis, kad priklausomasis nebedengiamas. |
| **Darbininko tinkamumo pasikeitimas (taikoma ne tik JAV)** | <ul><li>Darbuotojas > Įdarbinimas</li><li>Darbininkas > Darbininkas > Versijos > Įdarbinimo retrospektyva</li></ul> | <ul><li>Darbuotojo tipo, įdarbinimo kategorijos arba penkių vartotojo apibrėžiamų tinkamumo laukų pasikeitimas</li><li>Lauko **HcmEmploymentDetail.EhrEmploymentType** pasikeitimai (apdorojami, kai *pasikeičia* įdarbinimo informacijos įrašai, neapdorojami, kai atsiranda *naujų* įdarbinimo įrašų, pvz., pakartotinis samdymas ar atleidimas)</li></ul> |
| **Naujo tinkamumo perrašymas (taikoma ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Planai > Išmokos > Tinkamumo taisyklės perrašymas | Naudoti gyvenimo įvykių apdorojimą | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Tinkamumo taisyklės perrašymo pasikeitimas (taikoma ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Planai > Išmokos > Tinkamumo taisyklės perrašymas | Naudoti gyvenimo įvykių apdorojimą (fiksuojami tik tinkamumo taisyklės perrašymo laukų **ValidFrom** ir **ValidTo** pasikeitimai) |
| **Tinkamumo taisyklės perrašymo galiojimo pabaiga (taikoma ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Planai > Išmokos > Tinkamumo taisyklės perrašymas | Naudoti gyvenimo įvykio keitimo apdorojimą. Pavyzdžiui, jeigu redaguojate plano tinkamumo taisyklės perrašymo galiojimo pabaigą kaip šiandien 17.00 val., bet koks laikas po 17.00 val. arba kitos dienos, o tada vykdote gyvenimo įvykio pasikeitimo apdorojimą, rodomas pranešimas, nurodantis, kad tinkamumo taisyklės perrašymo galiojimas baigėsi. |
| **Naujas išmokos planas (taikomas ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Planai > Naujas | <ul><li>Tinkamumo pasirinktys įtraukiamos į dabartinį planą</li><li>Pridedamas naujas planas su pridėtomis tinkamumo parinktimis</li></ul></br></br>Personalo darbuotojai turėtų vykdyti šio egzemplioriaus gyvenimo įvykio tinkamumo apdorojimą. |
| **Tinkamumo taisyklės pasikeitimas (taikoma ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Taisyklės / parinktys > Tinkamumo taisyklės | Naudoti gyvenimo įvykio tinkamumo apdorojimą. Registruojama, kai pasikeitė šios įrašų **EhrBenefitEligibilityRule** reikšmės: **UseEmplCategory**, **UseEmplStatus** arba **UseEmplType**. Atnaujinamos tik tos gyvenimo įvykių operacijos, kurios jau yra taikomos pasikeitusiai taisyklei arba tinkamumo kriterijui. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]