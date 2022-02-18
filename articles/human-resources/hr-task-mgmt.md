---
title: Užduočių tvarkymas
description: Šioje temoje paaiškinamos užduočių valdymo funkcijos, pasiekiamos Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e1eb75f807d84f088cf3dd139eb094aa76618
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087222"
---
# <a name="task-management"></a>Užduočių tvarkymas

[!INCLUDE [PEAP](../includes/peap-1.md)]

Užduočių valdymas leidžia kurti užduotis, kurias reikia atlikti norint įdarbinti (įmontuotus), atleisti (išorėje) ir perkelti (pereinant) darbuotojus. Užduočių valdymas naudoja kontrolinių sąrašų sąvoką. Kontrolinis sąrašas yra įtraukimo, išjungimo ar perėjimo užduočių sąrašas. Užduočių valdymas naudoja kontrolinius sąrašus užduotims grupuoti ir priskirti asmenims ar grupėms. Įjungimo, išjungimo ir perėjimų kontrolinio sąrašo funkcijos yra panašios.

## <a name="checklist-overview"></a>Kontrolinio sąrašo apžvalga

Kontrolinis sąrašas yra užduočių grupė. Kontroliniai sąrašai suteikia galimybę lanksčiai grupuoti užduotis ir juos galima naudoti pakartotinai (pavyzdžiui, kai samdote papildomų darbuotojų). Galite sukurti tiek kontrolinių sąrašų, kiek jums reikia, ir galite priskirti tas pačias užduotis keliems kontroliniams sąrašams.

### <a name="examples"></a>Pavyzdžiai

Toliau pateikti pavyzdžiai parodo, kaip kontrolinius sąrašus galima naudoti prisijungimo procese. Tačiau, kadangi įjungimo, išjungimo ir perėjimų kontrolinio sąrašo funkcijos yra panašios, informacija taip pat taikoma išjungimo ir perėjimo procesams.

Priėmimo proceso metu žmogiškųjų išteklių (HR) specialistai gali kurti užduotis, kurios seka ateinančių ir neseniai priimtų darbuotojų priėmimo eigą. Kadangi priėmimo procesas gali skirtis, priklausomai nuo darbuotojo padėties ar geografinės padėties, galite sukurti kelis priėmimo kontrolinius sąrašus, kad atitiktumėte skirtingas įdarbinimo situacijas.

**1 pavyzdys**

Kiekvienas darbuotojas, pasamdytas Jungtinėse Valstijose, turi atlikti tokias užduotis kaip mokesčių išskaičiavimo formas. Tačiau tokios užduotys, kaip įmonės automobilio paskyrimas, gali būti taikomos tik vykdomojo lygio darbuotojams. Tokiu atveju galima sukurti du kontrolinius sąrašus: **JAV įsikūrę darbuotojai** ir **Tik vykdomieji asmenys**. Tada, kai Jungtinėse Valstijose pasamdomas vidutinio lygio vadovas, **JAV įsikūrę darbuotojai** pasirinktas kontrolinis sąrašas. Tačiau kai Jungtinėse Valstijose samdomas vadovas, atrenkami abu kontroliniai sąrašai, siekiant užtikrinti, kad būtų atliktos visos būtinos įdarbinimo užduotys.

**2 pavyzdys**

Įmonėje dirba ir sezoniniai darbuotojai, ir nuolatiniai etatiniai darbuotojai. Nors kai kurios užduotys (pvz., naujo darbuotojo atvykimo laiko patikrinimas) taikomos abiejų tipų darbuotojams, kai kurios papildomos užduotys taikomos tik nuolatiniams visą darbo dieną dirbantiems darbuotojams. Tokiu atveju galite sudaryti du kontrolinius sąrašus. Abu kontroliniai sąrašai apima užduotis, kurios taikomos tiek sezoniniams, tiek nuolatiniams visą darbo dieną dirbantiems darbuotojams, tačiau tik vienas kontrolinis sąrašas apima užduotis, kurios yra būdingos nuolatiniams visą darbo dieną dirbantiems darbuotojams.

## <a name="task-management-workspace"></a>Užduočių valdymo darbo sritis

The **Užduočių valdymas** darbo srityje pateikiamos visos užduotys, kurios buvo priskirtos asmenims prisijungimo, išjungimo ir perėjimo procesuose. Norėdami peržiūrėti proceso užduotis, viršutiniame kairiajame kampe pasirinkite atitinkamą skirtuką: **Prisijungimas**, **·**, arba **Perėjimai**. Pagal numatytuosius nustatymus tik HR specialistai gali pasiekti **Užduočių valdymas** darbo vieta.

The **Prisijungimas** skirtuke yra a **Greitai prasidės** sąrašas, kuriame rodomi atvykstantys darbuotojai ir a **Neseniai samdomi asmenys** sąrašas, kuriame rodomi neseniai pasamdyti darbuotojai. Abiejuose sąrašuose galite pasirinkti tik vieną darbuotoją. Kai pasirenkate darbuotoją, visos užduotys, susijusios su to darbuotojo priėmimu, rodomos dešinėje puslapio pusėje. The **Prisijungimas** skirtuke taip pat yra an **Visos užduotys** sąrašas, kuriame rodomos visos užduotys visiems ateinantiems ar neseniai pasamdytiems darbuotojams. Galiausiai jame yra uždelstų užduočių sąrašas ir dabartiniam vartotojui priskirtų užduočių sąrašas.

The **Atsikratymas** Skirtuke yra darbuotojų, kurie išeina iš įmonės, sąrašas ir darbuotojų, kurie jau išėjo iš įmonės, sąrašas. Abiejuose sąrašuose galite pasirinkti tik vieną darbuotoją. Kai pasirenkate darbuotoją, rodomos visos užduotys, susijusios su to darbuotojo pašalinimu iš darbo. The **Atsikratymas** skirtuke taip pat yra an **Visos užduotys** sąrašas, kuriame rodomos visos užduotys visiems išeinantiems ar išeinantiems darbuotojams. Galiausiai jame yra uždelstų užduočių sąrašas ir dabartiniam vartotojui priskirtų užduočių sąrašas.

The **Perėjimai** skirtuke yra an **Visos užduotys** sąrašas, kuriame rodomos visos užduotys visiems darbuotojams, kurie keis pareigas arba neseniai pakeitė pareigas. Taip pat yra uždelstų užduočių sąrašas ir dabartiniam vartotojui priskirtų užduočių sąrašas.

Visuose trijuose skirtukuose personalo padėjėjai ir vadovai gali atlikti šias veiklas:

- Taikykite darbuotojui kontrolinį sąrašą.
- Atnaujinkite užduoties būseną.
- Iš naujo priskirti užduotį.
- Atnaujinkite užduoties terminą.

> [!NOTE]
> Pagal numatytuosius nustatymus, **Prisijungimas** skirtuke rodomi darbuotojai, kurie buvo įdarbinti per pastarąsias septynias dienas. Norėdami pakeisti šį nustatymą, **Žmogiškųjų išteklių parametrai** puslapyje, esančiame **Generolas** skirtuke **Neseniai samdomi asmenys** lauke įveskite laiko tarpą. Informacija, esanti **Neseniai samdomi asmenys** sąrašas gali būti rodomas tam tikram dienų, mėnesių ar metų skaičiui. Pavyzdžiui, norėdami peržiūrėti darbuotojų, kurie buvo įdarbinti per pastarąsias 14 dienų, sąrašą, nustatykite **Laikotarpis** laukas į **14** ir **Vienetas** laukas į **Dienos**.
>
> Ant **Žmogiškųjų išteklių parametrai** puslapyje, taip pat galite atnaujinti išeinančių ir išeinančių darbuotojų sąrašų, kurie rodomi **Atsikratymas** skirtukas.
>
> Šie nustatymai taip pat taikomi **Personalo valdymas** darbo vieta.

## <a name="setting-up-tasks"></a>Užduočių nustatymas

Galite kurti užduotis atskirai ir pakartotinai panaudoti jas keliuose kontroliniuose sąrašuose. Norėdami sukurti užduotį, **Prisijungimo sąranka** puslapyje, esančiame **Užduotys** skirtuką, pasirinkite **Nauja**.

Arba galite pridėti užduotis tiesiai į kontrolinį sąrašą. Norėdami įtraukti užduotį į kontrolinį sąrašą, **Prisijungimo sąranka** puslapyje, esančiame **Kontrolinis sąrašas** skirtuke, sukurkite naują kontrolinį sąrašą, kad pridėtumėte užduotį, arba pridėkite užduotį prie esamo kontrolinio sąrašo.

> [!NOTE]
> Jei užduotį įtrauksite tiesiai į kontrolinį sąrašą, negalėsite jos pakartotinai panaudoti kituose kontroliniuose sąrašuose.

Šioje lentelėje aprašomi laukai, kurie galimi, kai kuriate užduotį bet kuriuo metodu.

| Laukas           | Aprašymas |
|-----------------|-------------|
| Užduotis            | Įveskite užduoties pavadinimą. |
| Aprašymas     | Įveskite užduoties aprašymą. |
| Pasirinktina        | Nurodykite, ar užduotis yra neprivaloma ir yra tik informacinė. |
| Užduoties saitas       | Įveskite išorinio tinklalapio arba konkretaus programos puslapio, kuriame vartotojas turėtų atlikti užduotį, URL. Norėdami gauti daugiau informacijos, žr [Užduočių nuorodos](#task-links) skyrius. |
| Priskyrimo tipas | Užduotys gali būti priskirtos konkrečiam darbuotojui, pareigoms ar pareigybių grupei, paveikto darbuotojo vadovui (ty darbuotojui, kuris dalyvauja priėmimo, pašalinimo ar perėjimo procese) arba paveiktam darbuotojui. Pasirinkite užduoties tipą. Norėdami gauti daugiau informacijos, žr [Užduočių tipai](#assignment-types) skyrius. |
| Priskirta     | Pasirinkite konkretų darbuotoją, pareigas arba pareigybių grupę, kuriai norite priskirti užduotį. |
| Kontaktinis asmuo  | Nurodykite asmenį, į kurį reikėtų kreiptis, jei kyla klausimų dėl užduoties. |
| Termino įskaitymas | Nurodykite dienų skaičių prieš arba po įjungimo, nutraukimo arba perėjimo datos, kada turi būti atlikta užduotis. Norėdami gauti daugiau informacijos, žr [Užduočių terminai ir laukas Termino datos poslinkis](#task-due-dates-and-the-due-date-offset-field) skyrius. |
| Instrukcijos    | Įveskite užduoties atlikimo instrukcijas. Norėdami gauti daugiau informacijos, žr [Instrukcijos](#instructions) skyrius. |

### <a name="task-links"></a>Užduočių nuorodos

Užduoties nuoroda suteikia nuorodą į išorinį tinklalapį arba puslapį „Dynamics 365“ programoje. Galite nurodyti užduoties nuorodą, jei asmuo, kuriam priskirta užduotis, turėtų eiti į konkretų tinklalapį arba konkretų puslapį „Dynamics 365“ programoje, kad atliktų tą užduotį. Kai kuriate užduoties nuorodą, galite pasirinkti vieną iš šių parinkčių:

- **Meniu elementas** – Jei pasirinksite šią parinktį, bus rodomas visų „Dynamics 365“ programos puslapių sąrašas. Sąraše pasirinkite puslapį.
- **URL** – Jei pasirenkate šią parinktį, įveskite tinklalapio, į kurį norite patekti asmeniui, kuriam priskirta užduotis, URL. Nurodytas puslapis gali būti puslapis, kuris nėra „Dynamics 365“ programos dalis.
- **Darbuotojo detalės** – Jei pasirenkate šią parinktį, pasirinkite vieną iš šių parinkčių:

    - **Darbuotojo savitarnos veiksmai** – Ši parinktis rodo galimų puslapių sąrašą **Darbuotojų savitarna**. Naudokite jį, jei užduotį, kuri buvo paskirta įtrauktam darbuotojui, reikia atlikti **Darbuotojų savitarna**. Pavyzdžiui, jei norite, kad darbuotojas įvestų savo asmeninę kontaktinę informaciją, pasirinkite **Darbuotojo savitarnos veiksmai**, tada pasirinkite **Asmeninės detalės&gt; Asmeninė informacija**.
    - **Darbuotojų valdymo veiksmai** – Ši parinktis rodo puslapių, susijusių su darbuotojo įrašu, bet darbuotojui nepasiekiamų, sąrašą. Pavyzdžiui, jei norite, kad užduoties savininkas įvestų informaciją, būdingą įdarbintam darbuotojui, pvz., informaciją apie kompensaciją, pasirinkite **Darbuotojų valdymo veiksmai**, tada pasirinkite **Kompensacija&gt; Fiksuota kompensacija**.

### <a name="assignment-types"></a>Užduočių tipai

Kai darbuotojas priimamas į darbą, atleidžiamas iš darbo ar perkeliamas, galima pasirinkti vieną ar daugiau kontrolinių sąrašų. Pasirinkus kontrolinį sąrašą ir užbaigus įdarbinimo, nutraukimo ar perkėlimo procesą, sukuriamos užduotys ir priskiriamos vartotojams, kad būtų galima stebėti pažangą.

Kai sukuriama užduotis, ji priskiriama konkrečiam vartotojui. Vartotojas, kuriam priskirta užduotis, priklauso nuo to užduočiai pasirinkto priskyrimo tipo. Toliau pateikiamos reikšmės **Užduoties tipas** laukas:

- **Darbininkas** – Paskirti užduotį konkrečiam darbuotojui. Pasirinkę šią reikšmę, pasirinkite darbuotoją **Priskirtas** lauke.
- **Padėtis** – Priskirkite užduotį konkrečiai pozicijai. Pasirinkę šią reikšmę, pasirinkite poziciją **Priskirtas** lauke.

    Pavyzdžiui, IT inžinierius visada bus atsakingas už nešiojamojo kompiuterio paruošimą naujam darbuotojui. Tokiu atveju kurdami nešiojamojo kompiuterio konfigūravimo užduotį pasirinkite **Padėtis** kaip priskyrimo tipą, tada pasirinkite **IT inžinierius** kaip padėtis. Tada, kai samdomas darbuotojas ir priskiriamas kontrolinis sąrašas, nešiojamojo kompiuterio konfigūravimo užduotis priskiriama tam darbuotojui, kuris tuo metu, kai įvedamas nuomos veiksmas, yra IT inžinieriaus pareigas.

- **Grupė** – Priskirkite užduotį pareigybių grupei (užduočių grupei). Pasirinkę šią reikšmę, pasirinkite grupę **Priskirtas** lauke. Norėdami gauti daugiau informacijos, žr [Užduočių grupių nustatymas (pasirenkama)](#setting-up-assignment-groups-optional) skyrius.
- **Vadovas** – Paskirti užduotį priimamo, atleidžiamo ar perkeliamo darbuotojo vadovui.

    > [!IMPORTANT]
    > Pritaikius kontrolinį sąrašą, jei samdomam, atleistam ar perkeltam darbuotojui šiuo metu nėra priskirta jokia pareigybė, vadovas negali būti nustatytas. Tokiu atveju užduotis priskiriama kontrolinio sąrašo savininkui. Norėdami gauti daugiau informacijos, žr [Kontrolinių sąrašų sudarymas](#setting-up-checklists) skyrius.

- **Darbuotojas** – Paskirti darbuotoją, kuris priimamas į darbą, atleidžiamas iš darbo ar perkeliamas.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Užduočių terminai ir laukas Termino datos poslinkis

Užduočių terminai yra pagrįsti darbo pradžios data, nutraukimo data arba pereinamojo laikotarpio data. Kai kurios užduotys turi būti baigtos iki darbuotojo pradžios datos, o kitos užduotys gali būti baigtos vėliau. Kai apibrėžiate užduotį, nustatote **Termino įskaitymas** lauke, kad nurodytumėte terminą, susietą su pradžios data, nutraukimo data arba perėjimo data. Pavyzdžiui, IT inžinierius turi paruošti nešiojamąjį kompiuterį naujam darbuotojui likus dviem dienoms iki to darbuotojo darbo pradžios. Tokiu atveju, kurdami nešiojamojo kompiuterio konfigūravimo užduotį, nustatykite **Termino įskaitymas** laukas į **-2**. Tada, jei darbuotojo darbo pradžia yra gegužės 5 d., užduotis bus atlikta gegužės 3 d.

> [!NOTE]
> Sukūrus užduotį, terminai gali būti koreguojami.

Mokėjimo datos apskaičiuojamos pagal kalendorių, susietą su kontroliniu sąrašu. Norėdami gauti daugiau informacijos, žr [Kontrolinių sąrašų sudarymas](#setting-up-checklists) skyrius.

### <a name="instructions"></a>Instrukcijos

Sudėtingoms užduotims gali prireikti kelių veiksmų arba asmuo, kuris atlieka užduotį, gali pateikti papildomos informacijos. Viduje konors **Instrukcijos** lauke, galite įvesti instrukcijas arba papildomą informaciją, kuri padės asmeniui, kuriam pavesta atlikti užduotį, ją atlikti.

## <a name="setting-up-checklists"></a>Kontrolinių sąrašų sudarymas

Kontrolinis sąrašas yra užduočių grupė. Galite sukurti tiek kontrolinių sąrašų, kiek jums reikia, ir galite priskirti tas pačias užduotis keliems kontroliniams sąrašams. Kai kuriate kontrolinį sąrašą, nurodote savininką ir kalendorių.

Jei **Užduoties tipas** nustatytas užduoties laukas **Padėtis**, **·**, arba **Grupė**, tačiau pagal užduoties tipą negalima išvesti konkretaus asmens, užduotis bus priskirta kontrolinio sąrašo savininkui. Štai keletas situacijų, kai užduotys bus priskirtos kontrolinio sąrašo savininkui, pavyzdžiai:

- Priimamam ar atleidžiamam darbuotojui pareigos neskiriamos. Kadangi darbuotojas neturi pareigų, jo vadovas negali būti nustatytas.
- The **Užduoties tipas** laukas nustatytas į **Padėtis**, tačiau užduoties sukūrimo metu pareigoms nėra priskirtas joks darbuotojas. Pavyzdžiui, **Nešiojamojo kompiuterio sąranka** užduotis priskirta pozicijos numeriui 000876 (**Techninės pagalbos specialistas**). Tuo metu, kai darbuotojas priimamas į darbą, joks darbuotojas nėra priskirtas 000876 pareigoms. Todėl kontrolinio sąrašo savininkui bus sukurta užduotis.
- The **Užduoties tipas** laukas nustatytas į **Grupė**, tačiau tuo metu, kai sukuriama užduotis, į grupės pareigas nėra priskirtas joks darbuotojas.

Kontroliniam sąrašui nurodytas kalendorius naudojamas skaičiuojant užduočių, kurios yra to kontrolinio sąrašo dalis, terminą. Darbo ir ne darbo dienos nustatomos kalendoriaus sąrankoje. Skaičiuojant užduočių atlikimo terminą įskaitomos darbo dienos, neįskaitomos nedarbo dienos. Į nedarbo dienas įeina savaitgaliai ir švenčių dienos. 

Nustačius kalendorių, jis susiejamas su kontrolinio sąrašo šablonu. Tokiu būdu kiekvienos kontrolinio sąrašo užduoties terminas apskaičiuojamas taip pat. Galite nustatyti kelis kalendorius, bet su kiekvienu kontroliniu sąrašu galima susieti tik vieną kalendorių.

## <a name="setting-up-assignment-groups-optional"></a>Užduočių grupių nustatymas (pasirenkama)

Kartais už užduotį atsakinga asmenų grupė. Pavyzdžiui, IT darbuotojų grupė gali būti atsakinga už nešiojamųjų kompiuterių paruošimą naujam darbui.

Norėdami nustatyti užduočių grupę, atlikite šiuos veiksmus.

1. Ant **Grupinė užduotis** puslapį, pasirinkite **Nauja**.
1. Įveskite pavadinimą (pvz.**IT nešiojamas kompiuteris**) ir grupės aprašymą.
1. Pasirinkite **Įrašyti**.
1. Ant **Nariai** FastTab, pasirinkite **Papildyti**.
1. Viduje konors **Pozicijos** lauke, pasirinkite visas pareigybes, kurios yra atsakingos už užduotį.

Sukūrus užduočių grupę, ją galima pasirinkti, kai sukuriama užduotis. Norėdami pasirinkti konkrečią užduoties grupę, turite pasirinkti **Grupė** viduje konors **Užduoties tipas**. Tada jūsų sukurtą grupę bus galima pasirinkti **Priskirtas** lauke.

> [!IMPORTANT]
> Jei užduotis priskirta grupei, užduotis pažymima kaip **Užbaigta** kai vienas asmuo iš grupės jį užbaigia. Užduotys sukuriamos nuomos, nutraukimo ar perėjimo metu. Jie sukurti vartotojams, kurie priskirti pareigoms, kurios yra įtrauktos į grupę.

## <a name="setting-up-task-groups-optional"></a>Užduočių grupių nustatymas (pasirenkama)

Priėmimo, išjungimo ar perėjimo procesas gali apimti daug užduočių. Kad visas reikalingas užduotis būtų lengviau priskirti kontroliniam sąrašui, galite sukurti pasirenkamas užduočių grupes, kad suskirstytumėte susijusias užduotis į kategorijas. Pavyzdžiui, personalo, IT ir darbo užmokesčio skyriai turi atlikti konkrečias užduotis, kad priimtų naują darbuotoją. Todėl sukuriate šias užduočių grupes: **HR**, **·**, ir **Darbo užmokestis**. Tada kurdami užduotį galėsite su ja susieti vieną iš tų užduočių grupių.

Kai norite įtraukti užduotį į kontrolinį sąrašą, galite filtruoti užduočių sąrašą pagal užduočių grupę, kuriai priskirta norima užduotis. Pavyzdžiui, kurdami kontrolinio sąrašo šabloną, galite filtruoti sąrašą taip, kad tik IT užduotys, priskirtos **IT** rodoma užduočių grupė. Todėl galite užtikrinti, kad pasirinktos tik atitinkamos IT užduotys.

## <a name="using-checklists"></a>Kontrolinių sąrašų naudojimas

Kai darbuotojas yra įdarbinamas, atleidžiamas iš darbo ar perkeliamas, galima pasirinkti vieną ar daugiau kontrolinių sąrašų. Užduočių terminai ir darbuotojų priskyrimai sukuriami pasibaigus įdarbinimo, nutraukimo ar perėjimo procesui. Pavyzdžiui, kai pasirenkate **Samdyti** arba **Išnuomokite ir pridėkite išsamią informaciją** mygtuką, užduotys sukuriamos asmenims, atsižvelgiant į užduoties tipą.

Kiekvienai užduočiai priskiriamas terminas, pridedant arba atimant termino atskyrimą nuo darbuotojo pradžios datos. Norėdami gauti daugiau informacijos, žr [Užduočių terminai ir laukas Termino datos poslinkis](#task-due-dates-and-the-due-date-offset-field) skyrius.

Jei naudojate personalo veiksmus, užduotys sukuriamos, kai **Užbaigti** mygtukas pasirinktas arba veiksmas patvirtintas.

Viduje konors **Užduočių valdymas** Darbo srityje galite pritaikyti darbuotojui kontrolinį sąrašą, pasirinkę darbuotoją paprasto sąrašo puslapyje arba išsamios informacijos puslapyje, tada pasirinkę **Taikyti kontrolinį sąrašą**. Vertė **Taikinio data** laukas bus naudojamas užduočių terminui apskaičiuoti. Paprastai tikslinė data turi atitikti darbuotojo įdarbinimo, nutraukimo ar perėjimo datą.

Taip pat galite pritaikyti kontrolinį sąrašą darbuotojui atidarę jo **Darbininkas** puslapį ir pasirenkant **Kontroliniai sąrašai** meniu.

## <a name="completing-tasks"></a>Užduočių atlikimas

Ant **Darbuotojų savitarna** puslapyje, darbuotojas gali peržiūrėti visas jam priskirtas užduotis. Už kiekvieną paskirtą užduotį **Užduotis**, **·**, **·**, ir **Kontaktinis asmuo** rodomos reikšmės. Be to, atlikdamas kiekvieną užduotį darbuotojas gali atidaryti susietą išorinį tinklalapį arba susijusį puslapį „Dynamics 365“ programoje.

Užduotys gali būti pažymėtos kaip **Vykdoma**, **·**, arba **Užbaigta**. Jei užduotis buvo priskirta grupei, ji bus pažymėta kaip **Užbaigta** kai vienas asmuo iš grupės jį užbaigia.

Užduotys taip pat gali būti perskirstytos.
