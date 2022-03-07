---
title: Gyvenimo įvykių tipų konfigūravimas
description: „Microsoft Dynamics 365 Human Resources“ vartotojų gyvenimo įvykių tipai, apibrėžiantys įvykius, kurie tinka darbuotojų išmokų registracijai atnaujinti.
author: andreabichsel
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 821e11d6ee22cb560b3d23017c7c332f80d41c18
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057651"
---
# <a name="configure-life-event-types"></a>Gyvenimo įvykių tipų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Dynamics 365 Human Resources“ vartotojų gyvenimo įvykių tipai, apibrėžiantys įvykius, kurie tinka darbuotojų išmokų registracijai atnaujinti, tokių kaip santuokos ar vaiko gimimo. Kiekvienas gyvenimo įvykio tipo ID gali būti susietas tik su vienu gyvenimo įvykio tipu. Pavyzdžiui, jei sukūrėte gyvenimo įvykio ID pavadinimu „Adreso pasikeitimas“, kuris yra susietas su gyvenimo įvykio tipu „Darbuotojo adreso pasikeitimas“, negalite sukurti kito ID pavadinimu „Darbuotojo adreso pasikeitimas“, ir susieti jį su gyvenimo įvykio tipu „Darbuotojo adreso pasikeitimas“. Jei gyvenimo įvykio tipas nėra susietas su plano tipu, gyvenimo įvykio tipas neišjungs gyvenimo įvykio. Daugiau informacijos žr. dalyje [Planų tipų kūrimas](hr-benefits-setup-plan-types.md).

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
| **Įdarbinimo būsenos pasikeitimas** | Darbuotojas > Įdarbinimas<br>Įdarbinimo retrospektyvos puslapis | Jei darbuotojo įdarbinimo informacija jau yra išsami, sukūrus naują įdarbinimo informaciją, kurios įdarbinimo būsena skiriasi, bus suaktyvinamas gyvenimo įvykis.  Esamos įdarbinimo informacijos atnaujinimas su skirtinga įdarbinimo būsena taip pat suaktyvins visą įvykį.  |
| **Darbuotojo adreso pasikeitimas** | Darbininkas > Profilis > Adresai<br>Darbininkas > Asmeninė informacija > Asmeniniai kontaktai > Adresas | Adreso pakeitimas. Adresas turi būti pirminis, kad būtų suaktyvinamas gyvenimo įvykis. |
| **Priklausomojo pasikeitimas** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai<br>Darbuotojų savitarna | Pridėti asmeninį kontaktą, nurodantį jį kaip priklausomą ir nurodantį **galioja** nuo. Atnaujinkite asmeninio kontakto priklausomojo **informaciją, tinkamą** informacijai. Asmeninio kontakto ryšys turi būti vaikas, sutuoktinis, civilinis partneris arba buvęs sutuoktinis.  |
| **Gimimas ar įvaikinimas (priklausomasis)** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai<br>Darbuotojų savitarnos paslauga > Redaguoti asmeninę informaciją > Asmeniniai kontaktai | **Gimimo** data arba registravimo data pridedama arba **atnaujinama**. Reikia **nurodyti** vaiko gimimo datą. |
| **Padengimo praradimas (sutuoktinis / civilinis partneris)** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Padengimo praradimas | Asmeninio kontakto dalyje pasirenkama **Padengimo praradimas** ir **Įsigaliojimo data** |
| Partnerio užimtumo pasikeitimas | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Įdarbintas | Kuriamas asmeninis kontaktas ir **nustatomas** Parametras **Įdarbina kaip** Taip. Asmeninio kontakto atnaujinimas ir įdarbinimo **keitimas**.  |
| **Atostogos (sutuoktinis / civilinis partneris)** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Atostogos | Nurodyta asmeninio kontakto **sukurta ir Atostogų įsigaliojimo** data. Asmeninio **kontakto atostogų laikas** atnaujintas. Asmeninio **kontakto atostogų laiko** įsigaliojimo data atnaujinama.  |
| **Padengimo (pareigų) pasikeitimas** | Darbininkas > Pareigų priskyrimas > Darbininko pareigų priskyrimas<br>Pareigos > Pareigos | Pareigų pasikeitimas darbininko pareigų priskyrimo įrašuose. Darbininko priskyrimo pareigoms pasikeitimas. |
| **Padengimo (atlyginimo) pasikeitimas** | Darbininkas > Kompensacija > Fiksuotas planas<br>Darbuotojas > Asmeninė informacija > Išmokų metinis atlyginimas | Jei išmokų valdymas > Personalo bendrinami parametrai > Išmokos > Išmokų metinis atlyginimas neįgalintas, atnaujinimas Darbuotojas > Kompensacija > Fiksuotas planas sukurs gyvenimo įvykį. Jei išmokų valdymas > Personalo bendrinami parametrai > Išmokos > Išmokų metinis atlyginimas neįgalintas, atnaujinimas Darbuotojas > Asmeninė informacija > Metinės algos priedai sukurs gyvenimo įvykį. |
| **Sveikatos draudimas (darbuotojas / priklausomasis)** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Išsami informacija apie priklausomąjį > Sveikatos draudimo įsigaliojimo data | Pridedant arba **atnaujinant asmeninio** kontakto įsigaliojimo datą, sukuriamas šis gyvenimo įvykis. |
| **Teismo paskirta parama** | Darbuotojas > Profilis > Asmeninė informacija > Asmeniniai kontaktai > Priklausomasis > Court ordered support (QMSCO/QDRO) ir galiojimo datos | Kuriant asmeninį kontaktą, bus sukurtas gyvenimo įvykis, jei **Teismo sprendimo tarnyba** yra **Taip**. Teismo sprendimo pagalbos arba teismo sprendimo galiojimo pabaigos datos atnaujinimas **suaktyvins** ir **visą** įvykį. |
| **Mirė** | Darbininkas > Profilis > Asmeninė informacija > Mirties data | Įvesta ar naujinta mirties data. |
| **Draudimo įrodymai** | Darbininkas > Darbininkas > Versijos > įdarbinimo retrospektyvos > Datos tvarkytuvas > Išmokos informacija | **Nustatytas tinkamumo naudoti į** Taip **įrodymas**. **Apibrėžta tinkamumo naudoti tikinimo** data. |
| **Gavėjas** | Darbininkas > Profilis > Asmeninė informacija > Asmeniniai kontaktai | Įtraukiamas asmeninis kontaktas ir pildomi laukai **Gavėjas** ir **Įsigaliojimo data**. Asmeninio kontakto tipas turi būti **Vaikas**, **Sutuoktinis**, **Partneris**, **Giminė**, **Šeimos kontaktas**, **Kitas kontaktas** ar **Tėvas**. |
| **Darbuotojo sveikatos draudimas** | Darbininkas > Darbininkas > Versijos > įdarbinimo retrospektyvos > Datos tvarkytuvas > Išmokos informacija | **Atitinkama medicinos priežiūra** nustatyta kaip **Taip**. Pasikeitė **Medicinos priežiūros atitinkamumo data**. |
| **Gimtadienis** | Išmokų valdymas > Gyvenimo įvykio pakeitimo apdorojimas | Šie gyvenimo įvykiai sukuriami iš **gyvenimo įvykio pakeitimo** apdorojimo. Proceso metu analizuoja pasirinktą laikotarpį bei juridinį subjektą ir surandami susiję darbuotojai. Jis apskaičiuoja jų paskutinį gimtadienį ir sukuria gimtadienio gyvenimo įvykį, jei jis dar nebuvo sukurtas. |
| **Darbininko tinkamumo pasikeitimas (taikoma ne tik JAV)** | Darbuotojas > Įdarbinimas<br>Darbininkas > Darbininkas > Versijos > Įdarbinimo retrospektyva | Sukuria gyvenimo įvykį, kai:<br><ul><li>Kuriamas naujas įdarbin employment, ankstesnis įdarbinta ir pasikeičia darbuotojo tipas.</li><li>Naujos įdarbinimo išsamios informacijos sukūrimas, kai esama ankstesnės įdarbinimo informacijos ir įdarbinimo rūšis ar kategorijos keitimai.</li><li>Apibrėžiamas įdarbinimo įrašo ir kito darbuotojo tipo atnaujinimas.</li><li>Nurodomas įdarbinimo informacijos įrašas ir kitas įdarbinimo tipas arba kategorija.</li></ul> |
| **Naujo tinkamumo perrašymas (taikoma ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Planai > Išmokos > Tinkamumo taisyklės perrašymas | Naudoti gyvenimo įvykių apdorojimą<br>Kuriamas naujas išmokos plano tinkamumo nepaisys darbuotojas, suaktyvina šį gyvenimo įvykį.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Tinkamumo taisyklės perrašymo pasikeitimas (taikoma ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Planai > Išmokos > Tinkamumo taisyklės perrašymas | Atnaujinamas **tinkamas nuo išmokų plano arba jis galioja iki išmokų plano tinkamumo** **nepaisymo**, suaktyvina šį gyvenimo įvykį. |
| **Tinkamumo taisyklės perrašymo galiojimo pabaiga (taikoma ne tik JAV)** | Išmokų valdymas > Gyvenimo įvykio pakeitimo apdorojimas  | Šie gyvenimo įvykiai sukuriami iš **gyvenimo įvykio pakeitimo** apdorojimo. Proceso metu analizuoja pasirinktą laikotarpį bei juridinį subjektą ir surandami susiję išmokų plano atitinkamumo viršijimai. Jis sukuria gyvenimo įvykius, jei nepaisymai nebegalioja. |
| **Naujas išmokos planas (taikomas ne tik JAV)** | Išplėstiniai žmogiškieji ištekliai > Išmokos > Planai > Naujas | Tinkamumo pasirinktys įtraukiamos į dabartinį planą. Pridedamas naujas planas su pridėtomis tinkamumo parinktimis.</br></br>Personalo darbuotojai turėtų vykdyti šio egzemplioriaus gyvenimo įvykio tinkamumo apdorojimą. |
| **Tinkamumo taisyklės pasikeitimas (taikoma ne tik JAV)** | Išmokų valdymas > Tinkamumo taisyklės | Naudoti gyvenimo įvykio tinkamumo apdorojimą. Registruojama, kai pasikeitė šios įrašų **BenefitEligibilityRule** reikšmės: **UseEmplCategory**, **UseEmplStatus** arba **UseEmplType**. Atnaujinamos tik tos gyvenimo įvykių operacijos, kurios jau yra taikomos pasikeitusiai taisyklei arba tinkamumo kriterijui. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]