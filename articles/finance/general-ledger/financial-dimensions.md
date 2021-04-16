---
title: Finansinės dimensijos
description: Šioje temoje aprašomi įvairūs finansinių dimensijų tipai ir tai, kaip jie nustatomi.
author: aprilolson
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e931a6c1f7b43711995ebd3aac772e270baebfea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819630"
---
# <a name="financial-dimensions"></a>Finansinės dimensijos

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinami įvairūs finansinių dimensijų tipai ir tai, kaip jie nustatomi.

Naudokite puslapį **Finansinės dimensijos** kurdami finansines dimensijas, kurias galite naudoti kaip sąskaitų planų sąskaitos segmentus. Yra dviejų tipų finansinės dimensijos: pasirinktinės dimensijos ir objekto remiamos dimensijos. Pasirinktinės dimensijos yra bendrai naudojamos juridinių subjektų, o vertes įveda ir tvarko vartotojai. Objekto remiamų dimensijų vertės nurodomos kitur sistemoje, pvz., dalyse Klientai ar Parduotuvių objektai. Kai kurios objekto remiamos dimensijos yra bendrai naudojamos keliuose juridiniuose subjektuose, o kitos būdingos konkrečiai įmonei.

Sukūrę finansines dimensijas, naudokite puslapį **Finansinių dimensijų reikšmės**, kad kiekvienai finansinei dimensijai priskirtumėte papildomų ypatybių.

Kaip juridinių subjektų atitikmenis galite naudoti finansines dimensijas. Jums nereikia kurti juridinių subjektų programoje „Dynamics 365 Finance“. Tačiau finansinės dimensijos nėra skirtos patenkinti juridinių subjektų veiklos ar verslo poreikius. Susijusių vienetų apskaitos funkcija programoje „Finance“ yra skirta tik apskaitos įrašams, kuriuos sukuria kiekviena operacija.

Prieš nustatydami finansines dimensijas kaip juridinius subjektus, įvertinkite savo verslo procesus toliau nurodytose srityse ir nustatykite, ar šis nustatymas veiks jūsų organizacijoje:

- Inventorizacijos
- Pardavimai ir pirkimai tarp finansinių dimensijų ir juridiniai subjektai
- PVM skaičiavimas ir atskaitomybė
- Veiklos ataskaitos

Štai keletas apribojimų:

- PVM funkciją galite naudoti tik su juridiniais subjektais, o ne su finansinėmis dimensijomis.
- Į kai kurias ataskaitas finansinės dimensijos neįtraukiamos. Todėl, norint parengti ataskaitą pagal finansinę dimensiją, gali tekti modifikuoti ataskaitas.

## <a name="custom-dimensions"></a>Pasirinktinės dimensijos

Norėdami kurti vartotojo nustatomą finansinę dimensiją, lauke **Naudoti vertes iš** pasirinkite **Pasirinktinė dimensija**.

Taip pat galite nurodyti sąskaitos šabloną, ribojantį informacijos, kurią galima įvesti kaip dimensijos reikšmes, kiekį ir tipą. Galite įvesti simbolius, kurie išlieka vienodi visose dimensijos reikšmėse, pvz., raides arba brūkšnelį (-). Taip pat galite įvesti skaičiaus ženklus (\##) ir konjunkcijos ženklus (&) kaip vietos rezervavimo ženklus vietoj simbolių, kurie kaskart sukūrus dimensijos reikšmę bus skirtingi. Naudokite skaičiaus ženklą (\#) kaip skaitmens vietos rezervavimo ženklą, o konjunkcijos ženklą (&) – kaip raidės vietos rezervavimo ženklą. Formato šablono lauką galima naudoti tik lauke **Naudoti vertes iš** pasirinkus parinktį **Pasirinktinė dimensija**.

**Pavyzdys**

Norėdami apriboti dimensijos reikšmę iki raidžių „CC“ ir trijų skaitmenų, įveskite **CC-\#\#\#** kaip formato šabloną.

## <a name="entity-backed-dimensions"></a>Objekto remiamos dimensijos

Norėdami sukurti objekto remiamą finansinę dimensiją, lauke **Naudoti vertes iš** pasirinkite sistemos nurodytą objektą, kuriuo bus pagrįsta finansinė dimensija. Tada pagal tą objektą sukuriamos finansinės dimensijos reikšmės. Pavyzdžiui, norėdami sukurti projektų dimensijų reikšmes, pasirinkite **Projektai**. Po to sukuriamos kiekvieno projekto pavadinimo dimensijos reikšmės. Puslapyje **Finansinių dimensijų reikšmės** rodomos objekto vertės. Jei šios vertės yra konkrečios įmonės, puslapyje taip pat rodoma įmonė.

## <a name="activating-dimensions"></a>Dimensijų aktyvinimas

Kai suaktyvinate finansinę dimensiją, lentelė atnaujinama, kad būtų įtrauktas finansinės dimensijos pavadinimas. Panaikintos dimensijos pašalinamos. Dimensijos vertes galite įvesti prieš aktyvindami finansinę dimensiją. Tačiau, kol finansinė dimensija nesuaktyvinama, jos naudoti negalima. Pavyzdžiui, kol finansinė dimensija suaktyvinta, finansinės dimensijos į sąskaitos struktūrą įtraukti negalima. Kai pasirenkate **Aktyvinti**, visos dimensijos atnaujinamos ir rodomi būsenos pakeitimai.

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

## <a name="default-dimension-values"></a>Numatytosios dimensijos reikšmės

Naujose dimensijose pagrindinių įrašų, pvz., kliento ir tiekėjo, vertes galite naudoti kaip numatytąsias vertes. Kuriant naujas dimensijas, dimensijos vertėse įvedamas tų pagrindinių įrašų ID. Pavyzdžiui, kuriant naują klientą kliento ID įvedamas kliento dimensijoje. Kuriant pardavimo užsakymus, SF ar kitus dokumentus, kuriems reikalingas kliento ID, naudojamos esamos numatytosios taisyklės, o kliento ID įtraukiamas į dokumentą.

Ši funkcija valdoma naudojant dimensijos parametrą. Šio parametro pavadinimas – **Kopijuoti vertes į šią dimensiją kiekviename sukurtame naujame DimensionName**, o **DimensionName** yra dimensijos pavadinimas. Pagal numatytuosius nustatymus ši funkcija išjungta. Tačiau bet kuriuo metu galima ją įjungti.

Jei dimensijos įrašai jau yra, įjungus funkciją atnaujinami pagrindiniai įrašai. Tačiau esami dokumentai ir operacijos neatnaujinami.

Jei naudojate šabloną kurdami pagrindinį įrašą, patikrinkite, ar bendrosios dimensijos šablono reikšmė yra tuščia. Pvz., jei kuriate klientus iš šablono, įsitikinkite, kad kliento dimensija šablone yra tuščia. Kai kuriate naują klientą, kliento dimensijos vertė bus numatytoji pagal naujo kliento numerį.  

## <a name="derived-dimensions"></a>Išvestiniai matmenys

Galite konfigūruoti dimensiją, kad įvedus tą dimensiją į dokumentą būtų automatiškai įvedama kitų dimensijų informacija. Pavyzdžiui, jei įvedate išlaidų centro vertę 10, į padalinio dimensiją gali būti automatiškai įvedama vertė **20**.

Dimensijų puslapyje galite nustatyti išvestines vertes.

1. Pasirinkite dimensiją, paskui pasirinkite **Išvestinės dimensijos**.

    Puslapyje **Išvestinės dimensijos** yra tinklelis. Pasirinktas dimensijos segmentas yra pirmasis šio tinklelio stulpelis.

2. Įtraukite segmentus, kurie turi būti išvesti. Kiekvienas segmentas rodomas kaip stulpelis.

Įveskite iš pirmajame stulpelyje esančios dimensijos turimų išvesti dimensijų kombinacijas. Pavyzdžiui, norėdami, kad išlaidų centras būtų naudojamas kaip dimensija, iš kurios išvestas skyrius ir vieta, įveskite išlaidų centro vertę 10, skyriaus vertę 20 ir vietos vertę 30. Tada, pagrindiniame įraše arba operacijos puslapyje įvedus išlaidų centro vertę 10, skyriaus vertė 20 ir vietos vertė 30 įvedamos pagal numatytuosius parametrus.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Esamų verčių su išvestinėmis dimensijomis nepaisymas
 
Pagal numatytuosius parametrus išvestinės dimensijos procesas nepanaikina esamų išvestinių dimensijų verčių. Pavyzdžiui, jei įvedate išlaidų centro vertę 10, bet neįvedama jokia kita dimensija, skyriaus vertė 20 ir vietos vertė 30 įvedamos pagal numatytuosius parametrus. Tačiau pakeitus išlaidų centrą jau nustatytos vertės nekeičiamos. Todėl pagrindiniuose įrašuose galite nustatyti numatytąsias dimensijas ir tos dimensijos nebus keičiamos išvestinėmis dimensijomis.

Galite keisti išvestinių dimensijų elgseną, kad būtų nepaisoma esamų verčių – puslapyje **Išvestinės dimensijos** pažymėkite žymės langelį **Pakeisti esamas dimensijų vertes su išvestinėmis vertėmis**. Jei šis laukas pažymėtas, galite įvesti dimensiją su išvestinėmis dimensijos vertėmis ir tos išvestinės dimensijos vertės panaikins visas esamas vertes. Remiantis ankstesniu pavyzdžiu, jei įvedate išlaidų centro vertę 10, bet neįvedama jokia kita dimensija, skyriaus vertė 20 ir vietos vertė 30 įvedamos pagal numatytuosius parametrus. Tačiau jei skyriaus vertė jau 50, o vietos vertė jau 60, vertės dabar pakeičiamos ir skyriaus vertė bus 20, o vietos vertė – 30.
 
Išvestinės dimensijos, kurioms naudojamas šis parametras, nustačius numatytąsias dimensijų vertes, automatiškai nepakeičia esamų numatytųjų dimensijų verčių. Dimensijų verčių bus nepaisoma tik puslapyje įvedus naują dimensijos vertę ir kai tame puslapyje yra išvestinių tos dimensijos verčių.

### <a name="preventing-changes-with-derived-dimensions"></a>Apsauga nuo pakeitimų naudojant išvestines dimensijas
 
Kai puslapyje **Išvestinių dimensijų puslapis** naudojantis funkcija **Įtraukti segmentą** įtraukiamas segmentas (kaip išvestinė dimensija), puslapio **Įtraukti segmentą** apačioje pateikiama parinktis, kad galėtumėte neleisti atlikti tos dimensijos keitimų išvedant ją puslapyje. Pagal numatytuosius parametrus ši parinktis išjungta, kad būtų leidžiama keisti išvestinės dimensijos vertes. Jei norite neleisti keisti dimensijos (ją išvedus), nustatymo parinktį pakeiskite į **Taip**. Pavyzdžiui, jei skyriaus dimensijos vertė išvedama iš išlaidų centro dimensijos vertės, naudojant parinkties **Neleisti keitimų** nuostatą **Taip**, skyriaus vertės keisti negalima. 
 
Naudojantis šia nuostata pakeitimus atlikti galima tuo atveju, jei dimensijos vertė tinkama, bet nepateikta išvestinių dimensijų sąraše. Pavyzdžiui, jei skyriaus vertė 20 išvedama iš išlaidų centro vertės 10 ir įvedate išlaidų centro vertę 10, tada negalėsite redaguoti skyriaus vertės 20. Tačiau jei įvedus išlaidų centro vertę 20 jos nėra išvestinių išlaidų centro dimensijų sąraše, tada galite redaguoti skyriaus vertę. 
 
Visais atvejais pritaikius išvestines dimensijų vertes vis tiek turi būti tikrinama, ar sąskaitos vertė ir visos dimensijų vertės atitinka sąskaitų struktūras. Jei puslapyje naudojant išvestines dimensijas nepavyksta jų patikrinti, norint naudoti šias dimensijas operacijose, būtina pakeisti išvestinių dimensijų vertes. 
 
„FastTab“ skirtuke **Finansinės dimensijos** pakeitus dimensijas, tos dimensijos, kuri pažymėta, kad nebūtų leidžiama atlikti jos pakeitimų, redaguoti nebus galima. Sąskaitą ir dimensijas įvedant į puslapio segmentuoto įrašo valdiklį, dimensijas redaguoti galima. Tačiau patraukus žymiklį nuo segmentuoto įrašo valdiklio ir perėjus prie kito lauko arba pradėjus vykdyti kitą veiksmą, bus tikrinama, ar sąskaita ir dimensijos atitinka išvestinių dimensijų sąrašo vertes ir sąskaitų struktūras, kad būtų galima užtikrinti, jog įvestos tinkamos vertės. 

### <a name="derived-dimensions-and-entities"></a>Išvestinės dimensijos ir objektai

Norėdami nustatyti išvestinių dimensijų segmentus ir vertes galite naudotis objektais.

- Išvestinių dimensijų objektas nustato toms dimensijoms naudojamas išvedamas dimensijas ir segmentus.
- Naudodamiesi išvestinių dimensijų vertės objektu galite importuoti turimas išvesti kiekvienos išvedamos dimensijos vertes.

Kai norint importuoti duomenis naudojamasi objektu, jei tas objektas importuoja dimensijas, importuojant taikomos išvestinės dimensijos taisyklės, nebent objektas nepaiso būtent tų dimensijų.

Daugiau informacijos ieškokite šiose temose:

- [Finansinių dimensijų apibrėžimas](tasks/define-financial-dimensions.md)
- [Prižiūrėti finansinės dimensijos numatytuosius šablonus](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]