---
title: Bendrai naudojamų parametrų konfigūravimas
description: Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f57c9613ba04ebb3748699105469586c27d66131c062d1af286b24199c4be7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723652"
---
# <a name="configure-shared-parameters"></a>Bendrai naudojamų parametrų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.

Kai kurių tipų įrašai, pvz., pareigų įrašai, yra bendrai naudojami keliose įmonėse. Šiems įrašams reikia nustatyti bendrai naudojamus parametrus. Pavyzdžiui, galite naudoti puslapį **Bendrai naudojami personalo parametrai** kelių juridinių subjektų personalo parametrams nustatyti. 

Puslapyje **Bendrai naudojami personalo parametrai** parametrai sugrupuoti į sritis pagal jų funkcijas. 

### <a name="settings"></a>Nustatoma
Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje. Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją. Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**. Norėdami nustatyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, spustelėkite **Personalo valdymas** &gt; **skirtuką Saitai** &gt; **Sąranka** &gt; **Identifikavimo tipai**. Galite įvesti paprastą kodą ir aprašymą. 

Skirtuke **Numeracijos** galite pasirinkti numeracijas, naudojamas šiuose įrašuose: darbuotojo numeryje, pareigose, vartotojo užklausos ID, I-9 dokumente, pretendente, diskusijoje, išmokos ID ir personalo veiksme (jei šis įrašo tipas suaktyvintas). Norėdami tvarkyti numeravimo nuorodas ir kodus, naudokite sąrašo puslapį **Numeracijos**. Norėdami rasti šį puslapį, naudokite puslapio ieškos funkciją. 

Skirtuke **Pareigos** nurodykite, ar pagal numatytuosius nustatymus naujas pareigas galima priskirti.

- **Visada** – galima priskirti darbuotojus naujoms pareigoms kuriant pareigas. Sukūrus pareigas **Galima priskirti** data ir laikas bus automatiškai nustatyti į sukūrimo datą ir laiką skirtuke **Bendra**, esančiame puslapyje **Pareigos**.
- **Niekada** – negalima priskirti darbuotojų naujoms pareigoms kuriant pareigas. Jei pasirenkate šią parinktį, turite atidaryti **Pareigų** puslapį kiekvienoms naujoms pareigoms, kai jos tampa galimos. Tada skirtuke **Bendra** įveskite **Galima priskyrimui** datą, kad įgalintumėte darbuotojo priskyrimą.

Skirtuke **Išplėstinė prieiga** galite apriboti prieigą prie kai kurių informacijos ar saitų:

- **Apriboti prieigą prie darbuotojo informacijos** – įjunkite šią funkciją, jei vartotojai turėtų galėti peržiūrėti tik tų juridinių subjektų, prie kurių prieigą jie turi, ir darbuotojų, kurie dirba šiuose juridiniuose subjektuose, informaciją.

    Įjungę šią funkciją, turite atlikti šiuos veiksmus, kad nustatytumėte atitinkamas teises kiekvienam vartotojui, kurio rodinį reikia apriboti:

    1. Puslapyje **Vartotojai** pasirinkite vartotoją.
    1. Pasirinkite vartotojo vaidmenį. Pasirinktis **Priskirti organizacijas** tampa galima.
    1. Pasirinkite **Priskirti organizacijas**.
    1. Naujame puslapyje pasirinkite **Suteikti prieigą prie konkrečių organizacijų atskirai**, o tada pasirinkite organizacijas, prie kurių vartotojas turi turėti prieigą.
    1. Pakartokite 2-4 veiksmus kiekvienam kitam vartotojo turimam vaidmeniui, įskaitant sistemos vartotojo vaidmenį.

    > [!NOTE]
    > Įmonės, prie kurių vartotojas turi prieigą, turi atitikti visus vartotojo vaidmenis.

- **Įgalinti visų įmonių kompensavimo rodinį** – kompensacija priskiriama darbuotojams pagal įdarbinimo juridinį subjektą. Kartais darbuotojas gali būti įdarbintas keliuose juridiniuose subjektuose tuo pačiu metu. Kai ši funkcija įjungta, kompensacija kiekvienam juridiniam subjektui bus rodoma darbuotojų savitarnoje ir vadovo savitarnoje be būtinybės keisti juridinius subjektus. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
