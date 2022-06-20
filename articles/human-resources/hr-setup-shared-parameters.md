---
title: Bendrai naudojamų parametrų konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0d8dbca302d90cc402feb4715a6fcc2b935d8b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906188"
---
# <a name="configure-shared-parameters"></a>Bendrai naudojamų parametrų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Turite nustatyti bendrai naudojamus įrašų, kurie bendrai naudojami įmonėse, pvz., pareigų įrašų **,** parametrus. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.

Kai kurie įrašų tipai, pvz. **, Pareigų** įrašai, yra bendrai naudojami įmonėse. Šiems įrašams reikia nustatyti bendrai naudojamus parametrus. Pvz., personalo **bendrinamų parametrų** puslapis naudojamas siekiant nustatyti juridinių subjektų personalo parametrus. 

Puslapyje **Bendrai naudojami personalo parametrai** parametrai sugrupuoti į sritis pagal jų funkcijas. 

### <a name="settings"></a>Nustatoma
Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje. Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją. Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**. Norėdami nurodyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, eikite į Personalo valdymo **saitų** &gt; **nustatymo** &gt; **identifikavimo** &gt; **tipus.** Galite įvesti paprastą kodą ir aprašymą. 

**Numeracijų skirtuke galite pasirinkti numeracijas, naudojamas šiuose įrašuose:** **personalo numeris, pareigos,** **vartotojo užklausos ID**, **I-9 dokumentas**, **·** **pretendento,** diskusijos **,** išmokos **ID** **ir personalo veiksmas (jei šis įrašo tipas įgalintas).** Norėdami tvarkyti numeravimo nuorodas ir kodus, naudokite sąrašo puslapį **Numeracijos**. Norėdami rasti šį puslapį, naudokite puslapio ieškos funkciją. 

Skirtuke **Pareigos** nurodykite, ar pagal numatytuosius nustatymus naujas pareigas galima priskirti.

- **Visada** – galima priskirti darbuotojus naujoms pareigoms kuriant pareigas. Sukūrus pareigas **Galima priskirti** data ir laikas bus automatiškai nustatyti į sukūrimo datą ir laiką skirtuke **Bendra**, esančiame puslapyje **Pareigos**.
- **Niekada** – negalima priskirti darbuotojų naujoms pareigoms kuriant pareigas. Jei pasirenkate šią parinktį, turite atidaryti **Pareigų** puslapį kiekvienoms naujoms pareigoms, kai jos tampa galimos. Tada skirtuke **Bendra** įveskite **Galima priskyrimui** datą, kad įgalintumėte darbuotojo priskyrimą.

Skirtuke **Išplėstinė prieiga** galite apriboti prieigą prie kai kurių informacijos ar saitų:

- **Apriboti prieigą prie darbuotojo** informacijos – pasirinkite šią funkciją, jei vartotojai gali peržiūrėti tik tų juridinių subjektų, prie kurių prieigą jie turi, darbuotojų, kurie dirba šiuose juridiniuose subjektuose, informaciją.

    Pasirinkę šią funkciją, atlikite šiuos veiksmus, norėdami nustatyti atitinkamas kiekvieno vartotojo, kurio rodinys turi būti apribotas, teises:

    1. Puslapyje **Vartotojai** pasirinkite vartotoją.
    1. Pasirinkite vartotojo vaidmenį. Pasirinktis **Priskirti organizacijas** tampa galima.
    1. Pasirinkite **Priskirti organizacijas**.
    1. Naujame puslapyje pasirinkite **Suteikti prieigą prie konkrečių organizacijų atskirai**, o tada pasirinkite organizacijas, prie kurių vartotojas turi turėti prieigą.
    1. Su kiekvienu papildomu vartotojo vaidmeniu, įskaitant sistemos vartotojo vaidmenį, pakartokite 2–4 veiksmus.

    > [!NOTE]
    > Įmonės, prie kurių vartotojas turi prieigą, turi atitikti visus vartotojo vaidmenis.

- **Įgalinti visų įmonių kompensavimo rodinį** – kompensacija priskiriama darbuotojams pagal įdarbinimo juridinį subjektą. Kartais darbuotojas gali būti įdarbintas keliuose juridiniuose subjektuose tuo pačiu metu. Pasirinkus šią funkciją, kiekvieno juridinio subjekto kompensacija **bus** **rodoma darbuotojų savitarnos ir vadybininko savitarnos** paslauga reikalaujant pakeisti juridinius subjektus. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
