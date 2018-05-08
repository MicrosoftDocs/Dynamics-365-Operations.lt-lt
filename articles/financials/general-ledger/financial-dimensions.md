---
title: "Finansinės dimensijos"
description: "Šioje temoje aprašomi įvairūs finansinių dimensijų tipai ir tai, kaip jie nustatomi."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a>Finansinės dimensijos

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinami įvairūs finansinių dimensijų tipai ir tai, kaip jie nustatomi.

Naudokite puslapį **Finansinės dimensijos** kurdami finansines dimensijas, kurias galite naudoti kaip sąskaitų planų sąskaitos segmentus. Yra dviejų tipų finansinės dimensijos: pasirinktinės dimensijos ir objekto remiamos dimensijos. Pasirinktinės dimensijos yra bendrai naudojamos juridinių subjektų, o vertes įveda ir tvarko vartotojai. Objekto remiamų dimensijų vertės nurodomos kitur sistemoje, pvz., dalyse Klientai ar Parduotuvių objektai. Kai kurios objekto remiamos dimensijos yra bendrai naudojamos keliuose juridiniuose subjektuose, o kitos būdingos konkrečiai įmonei. 

Sukūrę finansines dimensijas, naudokite puslapį **Finansinių dimensijų reikšmės**, kad kiekvienai finansinei dimensijai priskirtumėte papildomų ypatybių. 

Kaip juridinių subjektų atitikmenis galite naudoti finansines dimensijas. Naudojant „Microsoft Dynamics 365 for Finance and Operations“ juridinių subjektų kurti nereikia. Tačiau finansinės dimensijos nėra skirtos patenkinti juridinių subjektų veiklos ar verslo poreikius. Susijusių vienetų apskaitos funkcija programoje „Finance and Operations“ yra skirta tik apskaitos įrašams, kuriuos sukuria kiekviena operacija. 

Prieš nustatydami finansines dimensijas kaip juridinius subjektus, įvertinkite savo verslo procesus toliau nurodytose srityse ir nustatykite, ar šis nustatymas veiks jūsų organizacijoje:

- Inventorizacijos
- Pardavimai ir pirkimai tarp finansinių dimensijų ir juridiniai subjektai
- PVM skaičiavimas ir atskaitomybė
- Veiklos ataskaitos

Štai keletas apribojimų:

- PVM funkciją galite naudoti tik su juridiniais subjektais, o ne su finansinėmis dimensijomis.
- Į kai kurias ataskaitas finansinės dimensijos neįtraukiamos. Todėl, norint parengti ataskaitą pagal finansinę dimensiją, gali tekti modifikuoti ataskaitas.

## <a name="custom-dimensions"></a>Pasirinktinės dimensijos

Norėdami kurti vartotojo nustatomą finansinę dimensiją, lauke  **Naudoti vertes iš** pasirinkite  **&lt; Pasirinktinė dimensija &gt;**. Taip pat galite nurodyti sąskaitos šabloną, ribojantį informacijos, kurią galite įvesti kaip dimensijos reikšmes, kiekį ir tipą. Galite įvesti simbolius, kurie išlieka vienodi visose dimensijos reikšmėse, pvz., raides arba brūkšnelį (-). Taip pat galite įvesti skaičiaus ženklus (\##) ir konjunkcijos ženklus (&) kaip vietos rezervavimo ženklus vietoj raidžių ir skaitmenų, kurie bus skirtingi kaskart sukūrus dimensijos reikšmę. Naudokite skaičiaus ženklą (\#) kaip skaitmens vietos rezervavimo ženklą, o konjunkcijos ženklą (&) – kaip raidės vietos rezervavimo ženklą. Formato šablono lauką galima naudoti tik lauke **Naudoti vertes iš** pasirinkus parinktį **&lt; Pasirinktinė dimensija &gt;**.

**Pavyzdys**

Norėdami apriboti dimensijos reikšmę iki raidžių „CC“ ir trijų skaitmenų, įveskite **CC-\#\#\#** kaip formato šabloną.

## <a name="entity-backed-dimensions"></a>Objekto remiamos dimensijos

Norėdami sukurti objekto remiamą finansinę dimensiją, lauke **Naudoti vertes iš** pasirinkite sistemos nurodytą objektą, kuriuo bus pagrįsta finansinė dimensija. Tada pagal tą objektą sukuriamos finansinės dimensijos reikšmės. Pavyzdžiui, norėdami sukurti projektų dimensijų reikšmes, pasirinkite **Projektai**. Po to sukuriamos kiekvieno projekto pavadinimo dimensijos reikšmės. Puslapyje **Finansinių dimensijų reikšmės** rodomos objekto vertės. Jei šios vertės yra konkrečios įmonės, puslapyje taip pat rodoma įmonė.

## <a name="activating-dimensions"></a>Dimensijų aktyvinimas

Kai suaktyvinate finansinę dimensiją, lentelė atnaujinama, kad būtų įtrauktas finansinės dimensijos pavadinimas. Panaikintos dimensijos pašalinamos. Dimensijos vertes galite įvesti prieš aktyvindami finansinę dimensiją. Tačiau, kol finansinė dimensija nesuaktyvinama, jos naudoti negalima. Pavyzdžiui, kol finansinė dimensija suaktyvinta, finansinės dimensijos į sąskaitos struktūrą įtraukti negalima. Kai spustelite **Aktyvinti**, visos dimensijos atnaujinamos ir rodomi būsenos pakeitimai. 

## <a name="translations"></a>Vertimai

Puslapyje **Teksto vertimas** galite įvesti pasirinktos finansinės dimensijos tekstą įvairiomis kalbomis. Puslapyje **Pagrindinės sąskaitos vertimas** galite įvesti pagrindinės sąskaitos tekstą įvairiomis kalbomis. 

## <a name="legal-entity-overrides"></a>Juridinio subjekto nepaisymai

Ne visos dimensijos galioja visiems juridiniams subjektams. Be to, kai kurios dimensijos gali būti tinkamos tik tam tikrą laikotarpį. Tokiais atvejais skyrių **Juridinio subjekto nepaisymas** galite naudoti norėdami nurodyti, kuriose įmonėse dimensijos turi būti sustabdytos, kas jų savininkas ir kurį laikotarpį dimensija yra aktyvi.

## <a name="deleting-financial-dimensions"></a>Finansinių dimensijų naikinimas

Siekiant išlaikyti duomenų integralumą, finansines dimensijas retai kada galima panaikinti. Bandant panaikinti finansinę dimensiją atsižvelgiama į šiuos kriterijus:

- Ar finansinė dimensija buvo naudojama bet kokiose užregistruotose arba neužregistruotose operacijose ar bet kokio tipo dimensijų verčių derinyje?
- Ar finansinė dimensija naudojama bet kokioje aktyvioje sąskaitos struktūroje, išplėstinės taisyklės struktūroje arba finansinių dimensijų rinkinyje?
- Ar finansinė dimensija yra numatytojo finansinės dimensijos integracijos formato dalis?
- Ar finansinė dimensija buvo nustatyta kaip numatytoji dimensija?

Teigiamai atsakius į bent vieną iš pirmiau pateiktų klausimų dimensijos panaikinti negalima.


Daugiau informacijos ieškokite šiose temose:
- [Apibrėžti finansines dimensijas](tasks/define-financial-dimensions.md)
- [Prižiūrėti finansinės dimensijos numatytuosius šablonus](tasks/maintain-financial-dimension-default-templates.md)

