---
title: Bendrai naudojamų parametrų konfigūravimas
description: Šioje temoje paaiškinama, kaip juridiniuose subjektuose nustatyti personalo parametrus.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 039d8e2100824921d568c013fe3e113e1b091979
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729104"
---
# <a name="configure-shared-parameters"></a>Bendrai naudojamų parametrų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Turite nustatyti bendrai naudojamus įrašų, kurie bendrai naudojami įmonėse, pvz., pareigų **įrašų,** parametrus. Šioje temoje paaiškinama, kaip juridiniuose subjektuose nustatyti personalo parametrus.

Kai kurie įrašų tipai, pvz., **·** Pareigų įrašai, yra bendrai naudojami įmonėse. Šiems įrašams reikia nustatyti bendrai naudojamus parametrus. Pvz., **personalo bendrinamų** parametrų puslapis naudojamas siekiant nustatyti juridinių subjektų personalo parametrus. 

Puslapyje **Bendrai naudojami personalo parametrai** parametrai sugrupuoti į sritis pagal jų funkcijas. 

### <a name="settings"></a>Nustatoma
Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje. Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją. Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**. Norėdami nurodyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, eikite į Personalo **valdymo saitų** &gt; **·** &gt; **nustatymo** &gt; **identifikavimo** tipus. Galite įvesti paprastą kodą ir aprašymą. 

Numeracijų skirtuke galite pasirinkti numeracijas, naudojamas šiuose įrašuose: Personalo numeris, Pareigos, Vartotojo užklausos **·** **·** **·** **·** ID, **I-9** dokumentas, **·** Pretendento, Diskusijos, Išmokos **·** **ID** **·** ir Personalo veiksmas (jei šis įrašo tipas įgalintas). Norėdami tvarkyti numeravimo nuorodas ir kodus, naudokite sąrašo puslapį **Numeracijos**. Norėdami rasti šį puslapį, naudokite puslapio ieškos funkciją. 

Skirtuke **Pareigos** nurodykite, ar pagal numatytuosius nustatymus naujas pareigas galima priskirti.

- **Visada** – galima priskirti darbuotojus naujoms pareigoms kuriant pareigas. Sukūrus pareigas **Galima priskirti** data ir laikas bus automatiškai nustatyti į sukūrimo datą ir laiką skirtuke **Bendra**, esančiame puslapyje **Pareigos**.
- **Niekada** – negalima priskirti darbuotojų naujoms pareigoms kuriant pareigas. Jei pasirenkate šią parinktį, turite atidaryti **Pareigų** puslapį kiekvienoms naujoms pareigoms, kai jos tampa galimos. Tada skirtuke **Bendra** įveskite **Galima priskyrimui** datą, kad įgalintumėte darbuotojo priskyrimą.

Skirtuke **Išplėstinė prieiga** galite apriboti prieigą prie kai kurių informacijos ar saitų:

- **Apriboti prieigą prie darbuotojo informacijos – pasirinkite šią funkciją, jei vartotojai gali peržiūrėti tik tų juridinių subjektų, prie kurių prieigą jie turi, darbuotojų, kurie dirba šiuose juridiniuose** subjektuose, informaciją.

    Pasirinkę šią funkciją, atlikite šiuos veiksmus, norėdami nustatyti atitinkamas kiekvieno vartotojo, kurio rodinys turi būti apribotas, teises:

    1. Puslapyje **Vartotojai** pasirinkite vartotoją.
    1. Pasirinkite vartotojo vaidmenį. Pasirinktis **Priskirti organizacijas** tampa galima.
    1. Pasirinkite **Priskirti organizacijas**.
    1. Naujame puslapyje pasirinkite **Suteikti prieigą prie konkrečių organizacijų atskirai**, o tada pasirinkite organizacijas, prie kurių vartotojas turi turėti prieigą.
    1. Su kiekvienu papildomu vartotojo vaidmeniu, įskaitant sistemos vartotojo vaidmenį, pakartokite 2–4 veiksmus.

    > [!NOTE]
    > Įmonės, prie kurių vartotojas turi prieigą, turi atitikti visus vartotojo vaidmenis.

- **Įgalinti visų įmonių kompensavimo rodinį** – kompensacija priskiriama darbuotojams pagal įdarbinimo juridinį subjektą. Kartais darbuotojas gali būti įdarbintas keliuose juridiniuose subjektuose tuo pačiu metu. Pasirinkus šią funkciją, kiekvieno juridinio subjekto kompensacija bus rodoma darbuotojų savitarnos ir vadybininko savitarnos paslauga reikalaujant **·** pakeisti **·** juridinius subjektus. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
