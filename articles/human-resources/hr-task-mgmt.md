---
title: Užduočių tvarkymas
description: Šiame straipsnyje paaiškinama užduočių valdymo funkcija, kurią galima naudoti "Microsoft"Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c567f6d74e6ff87a72ff3b8663ca3a291dff3abb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897870"
---
# <a name="task-management"></a>Užduočių tvarkymas

[!INCLUDE [PEAP](../includes/peap-1.md)]

Užduočių valdymas leidžia sukurti užduotis, kurias reikia atlikti norint samdyti (ant darbo), atleisti (ofboard) ir perkelti (perėjimo) darbuotojus. Užduočių valdymas naudoja kontrolinių sąrašų sąvoką. Kontrolinis sąrašas yra apie inboarding, offboarding arba perėjimo užduotis. Užduočių valdymas naudoja kontrolinius sąrašus, norėdami sugrupuoti užduotis ir priskirti jas asmenims ar grupėms. Kontrolinio sąrašo funkcijos, skirta inžine tikinimo, perėjimo ir perėjimo funkcijai yra panašios.

## <a name="checklist-overview"></a>Kontrolinio sąrašo peržiūra

Kontrolinis sąrašas yra užduočių grupė. Kontroliniai sąrašai suteikia jums lankstų būdą grupuoti užduotis ir jas galima pakartotinai naudoti (pavyzdžiui, pasamdę papildomus darbuotojus). Galite sukurti tiek kontrolinių sąrašų, kiek jums reikia, ir tas pačias užduotis galite priskirti keliems kontroliniams sąrašui.

### <a name="examples"></a>Pavyzdžiai

Toliau pateikti pavyzdžiai rodo, kaip gali būti naudojami kontroliniai sąrašai ins linijose. Tačiau, kadangi kontrolinio sąrašo funkcijos yra panašios, kad būtų galima pereiti į lentas, ir pereiti, informacija taip pat taikoma perėjimo ir perėjimo procesams.

Personalo (personalo) darbuotojai kaip informacijos gavimo proceso dalį gali sukurti užduotis, kurios seka gaunamų ir neseniai pasamdyti darbuotojų inboarding eigą. Kadangi inboarding procesas gali skirtis, atsižvelgiant į darbuotojo pareigas arba geografinę vietovę, galite sukurti kelis inboarding kontrolinius sąrašus, kad galėtumėte talpinti skirtingas samdos situacijas.

**1 pavyzdys**

Kiekvienas DARBUOTOJAS, pasamdęs JAV, turi atlikti užduotis, pvz., užpildyti išskaitomo mokesčio formas. Tačiau užduotys, pvz., įmonės automobilio priskyrimas, gali būti taikomos tik vadovo lygio darbuotojams. Šiuo atveju gali būti sukurti du ins linijos kontroliniai sąrašai: **tik JAV darbuotojai** **ir vadovai**. Tada, kai jav pasamdyti vidurio lygio vadybininkas, **pasirenkamas JAV darbuotojų** kontrolinis sąrašas. Tačiau kai vadovas pasamdomas JUNGTINĖSe Valstijose, abu kontroliniai sąrašai parenkami, siekiant užtikrinti, kad visos reikiamos inboarding užduotys bus baigtos.

**2 pavyzdys**

Įmonėje yra ir sezoniniai darbuotojai, ir nuolatiniai darbuotojai, dirbantys visą darbo dieną. Nors kai kurios užduotys (pvz., naujo darbuotojo atvykimo laiko patikrinimas) taikomos abiejų tipų darbuotojams, kai kurios papildomos užduotys taikomos tik nuolat dirbantiems darbuotojams. Tokiu atveju galite sukurti du kontrolinius sąrašus. Abu kontroliniai sąrašai apima užduotis, kurios taikomos ir sezoniniams, ir įprastus darbuotojus, tačiau tik viename kontroliniame sąraše yra užduotys, kurios yra įprastos visą darbo dieną dirbantiems darbuotojams.

## <a name="task-management-workspace"></a>Užduočių valdymo darbo sritis

Užduočių **valdymo darbo** srityje išvardijamos visos užduotys, kurios buvo priskirtos asmenims, kurie yra inboarding, offboarding ir perėjimo procesuose. Norėdami peržiūrėti proceso užduotis, viršutiniame kairiajame kampe pasirinkite atitinkamą skirtuką: **Įterpimas,** **įterpimas į kitą, perėjimai** **.** Numatyta, kad tik personalo specialistai gali pasiekti užduočių **valdymo darbo** sritį.

Skirtuke **Inboarding** pateikiamas pradžios **sąrašas** **, kuriame rodomi gaunami darbuotojai, ir nesenų** samdos sąrašas, kuriame rodomi neseniai pasamdyti darbuotojai. Abiejuose sąrašuose galite pasirinkti tik vieną darbuotoją. Pasirinkus darbuotoją, dešinėje puslapio pusėje rodomos visos su tuo darbuotojo darbo metu susijusios užduotys. Įterpimo **skirtuke** taip pat pateikiamas **visų užduočių** sąrašas, kuriame pateikiamos visos gaunamų arba neseniai pasamdyti darbuotojų užduotys. Galiausiai joje pateikiamas vėluojamų užduočių sąrašas ir dabartiniam vartotojui priskirtų užduočių sąrašas.

Skirtuke **Offboarding** pateikiamas darbuotojų, kurie išeina iš įmonės, sąrašas ir darbuotojų, kurie jau išėjo iš įmonės, sąrašas. Abiejuose sąrašuose galite pasirinkti tik vieną darbuotoją. Pasirinkus darbuotoją rodomos visos su tuo darbuotojo darbo parinktimi susijusios užduotys. Įterpimo **skirtuke** taip pat pateikiamas **visų užduočių** sąrašas, kuriame rodomos visos užduotys, kurias turi atlikti visi išeidami arba išeidami darbuotojai. Galiausiai joje pateikiamas vėluojamų užduočių sąrašas ir dabartiniam vartotojui priskirtų užduočių sąrašas.

Skirtuke **Perėjimo** yra sąrašas **Visos užduotys**, parodytos visos užduotys visiems darbuotojams, kurie keis pareigas ar kurie ką tik pakeitė pareigas. Taip pat yra vėluojamų užduočių sąrašas ir dabartiniam vartotojui priskirtų užduočių sąrašas.

Visuose trijuose skirtukuose personalo asistentai ir vadybininkai gali atlikti šią veiklą:
- Taikyti kontrolinį sąrašą darbuotojui
- Užduoties būsenos atnaujinimas
- Užduoties pakartotinis priskirti
- Atnaujinti užduoties terminą

> [!NOTE]
> Pagal numatytuosius nustatymus **skirtuke Inboarding** rodomi darbuotojai, pasamdyti per paskutines septynias dienas. Norėdami pakeisti šį parametrą **, skirtuko Bendra** puslapyje Personalo **parametrai** lauke **Naujausi** samdiniai įveskite laiko tarpą. Naujausių samdos **sąrašų informacija** gali būti rodoma tam tikrą dienų, mėnesių ar metų skaičių. Pavyzdžiui, norėdami peržiūrėti darbuotojų, kurie buvo pasamdyti per paskutines 14 dienų, sąrašą, **·** **nustatykite laikotarpio lauką 14**, o vieneto **lauke** – Dienos.**·**
> Personalo parametrų **puslapyje**, jūs taip pat **galite atnaujinti išėjimo ir išėjimo darbuotojų sąrašų, kurie rodomi skirtuke Darbo sritis, datų diapazoną** . Šie parametrai taip pat taikomi personalo **valdymo darbo** sritimi.

## <a name="setting-up-tasks"></a>Užduočių nustatymas

Galite sukurti užduotis atskirai ir pakartotinai naudoti jas keliuose kontroliniuose sąraše. Norėdami sukurti užduotį, puslapio **Inboarding setup** skirtuke **Užduotys** pasirinkite **Nauja**.

Taip pat galite pridėti užduotis tiesiogiai į kontrolinį sąrašą. Norėdami įtraukti užduotį į kontrolinį sąrašą, **skirtuko Kontrolinis sąrašas puslapyje Inboarding setup** **sukurkite** naują kontrolinį sąrašą, kad įtraukumėte užduotį, arba įtraukite užduotį į esamą kontrolinį sąrašą.

> [!NOTE]
> Jei užduotį įtraukiate tiesiogiai į kontrolinį sąrašą, negalite jos pakartotinai naudoti kituose kontroliniuose sąrašų.

Toliau pateiktoje lentelėje aprašomi laukai, kurie galimi, kai kuriate užduotį vienu iš šių metodų.

| Laukas           | Aprašymas |
|-----------------|-------------|
| Užduotis            | Įvesti užduoties pavadinimą. |
| Aprašymas     | Įvesti užduoties aprašymą. |
| Pasirinktina        | Nurodykite, ar užduotis yra pasirinktinė ir ar ji yra tik informacinė. |
| Užduoties saitas       | Įveskite išorinio tinklalapio URL arba konkretų puslapį programoje, kur vartotojas turėtų atlikti šią užduotį. Daugiau informacijos ieškokite užduoties saitų [skyriuje](#task-links). |
| Priskyrimo tipas | Užduotys gali būti priskirtos konkrečiam darbuotojui, pareigoms arba pareigų grupei, darbuotojo vadybininkui (t. y. darbuotojui, kuris yra atėjimo į darbą, darbo su darbo vietoje ar perėjimo proceso dalis) arba darbuotojui. Pasirinkite priskyrimo tipą. Daugiau informacijos rasite skyriuje Priskyrimo [tipai](#assignment-types). |
| Priskirta     | Pasirinkite konkretų darbuotoją, pareigas arba pareigų grupę, prie kurios norite priskirti užduotį. |
| Kontaktinis asmuo  | Nurodykite asmenį, su kuo turi būti susisiekta, jei yra klausimų apie užduotį. |
| Termino korespondavimas | Nurodyti dienų iki arba po įtraukimo į darbo sritį, atleidimo arba perėjimo, kurių terminas yra užduotis, skaičių. Daugiau informacijos rasite skyriuje Užduoties [terminų datos ir Termino korespondentinės sąskaitos](#task-due-dates-and-the-due-date-offset-field) skyrius. |
| Instrukcijos    | Įveskite užduoties baigimo instrukcijas. Daugiau informacijos rasite skyriuje [Instrukcijos](#instructions). |

### <a name="task-links"></a>Užduoties saitai

Užduoties saitas pateikia saitą į išorinį tinklalapį arba puslapį programoje "Dynamics 365". Galite nurodyti užduoties saitą, jei užduočiai priskirtas asmuo turi eiti į konkretų tinklalapį arba konkretų puslapį programoje "Dynamics 365", kad galėtų atlikti tą užduotį. Kurdami užduoties saitą, galite pasirinkti vieną iš šių pasirinkčių:

- **Meniu elementas** – jei pasirinksite šią pasirinktį, bus rodomas visų "Dynamics 365" programos puslapių sąrašas. Pasirinkite puslapį iš sąrašo.
- **URL – jei pasirinksite šią pasirinktį, įveskite tinklalapio, į kurį turėtų eiti asmuo, kuriam priskirta užduotis, URL**. Nurodytas puslapis gali būti puslapis, kuris nėra "Dynamics 365" programos dalis.
- **Darbuotojo informacija** – jei pasirinksite šią pasirinktį, pasirinkite vieną iš šių pasirinkčių:

    - **Darbuotojų savitarnos veiksmai** – ši pasirinktis rodo puslapių, kuriuos galima rasti darbuotojų savitarnoje **, sąrašą**. Naudokite šią užduotį, jeigu užduočiai, kuri buvo priskirta darbuotojui, turi būti atlikta darbuotojų **savitarnoje**. Pavyzdžiui, jei norite, kad darbuotojas įves savo asmeninę kontaktinę informaciją, **pasirinkite** Darbuotojo savitarnos veiksmai ir pasirinkite Asmeninės **informacijos&gt; asmeninė informacija**.
    - **Darbuotojo valdymo** veiksmai – ši parinktis rodo puslapių, susijusių su darbuotojo įrašu, sąrašą, bet neprieinami darbuotojui. Pvz., jeigu norite, kad užduoties savininkas turėtų įvesti informaciją, būsią darbo grupės darbuotojui, pvz., kompensavimo informaciją, **pasirinkite** Darbuotojo valdymo veiksmus, **&gt; tada pasirinkite Pastovioji atlyginimo dalis**.

### <a name="assignment-types"></a>Priskyrimo tipai

Kai darbuotojas pasamdyti, atleistas arba perduotas, gali būti pasirinktas vienas ar daugiau kontrolinių sąrašų. Kai pasirenkamas kontrolinis sąrašas ir baigiamas pasamdymo, atleidimo arba perkėlimo procesas, užduotys sukuriamos ir priskiriamos vartotojams, norint sekti eigą.

Sukūrus užduotį, ji priskiriama konkrečiam vartotojui. Vartotojas, kuriam priskirta užduotis, priklauso nuo tai užduočiai pasirinkto priskyrimo tipo. Priskyrimo tipo lauke galimos **šios** vertės:

- **Darbuotojas** – priskirkite užduotį tam konkrečiam darbuotojui. Pasirinkę šią vertę, lauke Priskirta **pasirinkite darbuotoją**.
- **Pareigos** – Priskirkite užduotį konkrečioms pareigose. Pasirinkę šią vertę, pasirinkite poziciją lauke **Priskirta**.

    Pavyzdžiui, IT inžinierius visada bus atsakingas už nešiojamojo kompiuterio parengimą naujam darbuotojui. Šiuo atveju, kurdami skreitinojo kompiuterio konfigūracijos užduotį, **kaip** priskyrimo tipą pasirinkite Pozicija, **tada kaip vietą pasirinkite IT inžinierių**. Tada, kai darbuotojas pasamdyti ir priskirtas kontrolinis sąrašas, skreitinojo kompiuterio konfigūracijos užduotis priskiriama tam, kuris darbuotojas yra IT inžinieriaus vietoje tuo metu, kai įvedamas samdos veiksmas.

- **Grupė** – priskirkite užduotį pareigų grupei (priskyrimo grupė). Pasirinkę šią vertę, lauke Priskirta pasirinkite **grupę**. Daugiau informacijos rasite skyriuje Priskyrimo [grupių nustatymas (Pasirinktinai](#setting-up-assignment-groups-optional)).
- **Vadybininkas** – priskirkite užduotį darbuotojo, kuris yra pasamdęs, atleistas ar perkeltas, vadybininkui.

    > [!IMPORTANT]
    > Kai taikomas kontrolinis sąrašas, jei jokia pareigos šiuo metu nėra priskirtos pasamdytiems, atleistiems arba perkeltiems darbuotojams, vadybininko nustatyti negalima. Šiuo atveju užduotis priskiriama kontrolinio sąrašo savininkui. Daugiau informacijos rasite kontrolinių [sąrašų nustatymo](#setting-up-checklists) skyriuje.

- **Darbuotojas** – priskirti darbuotoją, kuris yra pasamdęs, atleistas arba perduotas.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Užduoties terminų ir termino korespondentinės sąskaitos laukas

Užduoties terminai pagrįsti įdarbinimo pradžios data, atleidimo data arba perėjimo data. Kai kurios užduotys turi būti užbaigtos prieš darbuotojo darbo pradžios datą, o kitos užduotys gali būti užbaigtos po to. Apibrėždami užduotį, nustatykite **lauką** Termino korespondentinė data, norėdami nurodyti terminą, kuris susijęs su pradžios data, atleidimo data ar perėjimo data. Pavyzdžiui, IT inžinierius turi paruošti nešiojamąjį kompiuterį naujam darbuotojui praėjus dviem dienoms iki to darbuotojo darbo pradžios datos. Šiuo atveju, kai sukuriate skreitinuko konfigūracijos užduotį, nustatykite termino **korespondentinį** lauką - **2**. Tada, jei darbuotojo darbo pradžios data yra gegužės 5 d., užduotis bus gegužės 3 d.

> [!NOTE]
> Terminus galima koreguoti sukūrus užduotį.

Terminai skaičiuojami pagal kalendorių, susietą su kontroliniu sąrašu. Daugiau informacijos rasite kontrolinių [sąrašų nustatymo](#setting-up-checklists) skyriuje.

### <a name="instructions"></a>Instrukcijos

Kompleksinės užduotys gali reikalauti kelių žingsnių arba asmeniui, atliekančiam šią užduotį, gali reikėti pateikti papildomos informacijos. Instrukcijos lauke **galite** įvesti instrukcijas arba papildomą informaciją, kad būtų galima padėti užduočiai priskirtą asmenį jį užbaigti.

## <a name="setting-up-checklists"></a>Kontrolinių sąrašų nustatymas

Kontrolinis sąrašas yra užduočių grupė. Galite sukurti tiek kontrolinių sąrašų, kiek jums reikia, ir tas pačias užduotis galite priskirti keliems kontroliniams sąrašui. Kai kuriate kontrolinį sąrašą, nurodote savininką ir kalendorių.

Jei užduoties **priskyrimo** **tipo** laukas nustatytas kaip Pareigos, **·** **Vadybininkas** arba Grupė, tačiau joks konkretus asmuo negali būti išvestas iš priskyrimo tipo, užduotis bus priskirta kontrolinio sąrašo savininkui. Štai keletas situacijų, kai užduotys bus priskirtos kontrolinio sąrašo savininkui, pavyzdžių:

- Darbuotojui, kuris yra pasamdęs arba atleistas, nepriskirtos jokios pareigos. Darbuotojui nėra priskirta pareigų, todėl jo vadybininko nustatyti negalima.
- Priskyrimo **tipo** laukas nustatytas kaip **Pareigos**, tačiau tuo metu, kai užduotis kuriama, darbuotojui nepriskirtas joks darbuotojas. Pvz., **Setup Laptop užduotis** priskiriama pareigų numeriui 000876 (**techninio aptarnavimo specialisto**). Kai darbuotojas pasamdyti, jam nepriskirtas joks darbuotojas 000876. Todėl bus sukurta kontrolinio sąrašo savininko užduotis.
- Priskyrimo **tipo** laukas nustatytas kaip **Grupė**, tačiau tuo metu, kai užduotis kuriama, grupei nepriskirtas joks darbuotojas.

Kontroliniam sąrašui nurodytas kalendorius naudojamas skaičiuojant užduočių, kurios yra to kontrolinio sąrašo dalis, terminą. Darbo ir ne darbo dienos nustatytos kalendoriaus nustatyme. Darbo dienos įtraukiamos, kai skaičiuojamas užduočių terminas, o ne darbo dienos neįtraukiamos. Ne darbo dienos apima savaitgalius ir atostogas. 

Nustačius kalendorių, jis susietas su kontrolinio sąrašo šablonu. Tokiu būdu kiekvienos kontrolinio sąrašo užduoties terminas skaičiuojamas tuo pačiu būdu. Galite nustatyti kelis kalendorius, tačiau su kiekvienu kontroliniu sąrašu galima susieti tik vieną kalendorių.

## <a name="setting-up-assignment-groups-optional"></a>Priskyrimo grupių nustatymas (pasirinktinai)

Kartais už užduotį yra atsakinga asmenų grupė. Pavyzdžiui, IT darbuotojų grupė gali būti atsakinga už nešiojamųjų kompiuterių parengimą naujiems samdos darbuotojams.

Norėdami nustatyti priskyrimo grupę, atlikite šiuos veiksmus.

1. Grupės priskyrimo **puslapyje** pasirinkite **Naujas**.
1. Įveskite pavadinimą (pvz., **IT skreitinuks**) ir grupės aprašymą.
1. Pasirinkite **Įrašyti**.
1. Narių "**FastTab**" pasirinkite **Įtraukti**.
1. Pareigų lauke **pasirinkite** visas už šią užduotį atsakingas pareigas.

Sukūrus priskyrimo grupę, ją galima pasirinkti kuriant užduotį. Norėdami pasirinkti konkrečią užduoties grupę, turite pasirinkti **grupę priskyrimo** tipe **·**. Jūsų sukurtą grupę bus galima pasirinkti lauke **Priskirta**.

> [!IMPORTANT]
> Jei užduotis priskiriama grupei, užduotis pažymima kaip **Baigta**, kai vienas grupės asmuo ją užbaigia. Užduotys sukuriamos samdos, atleidimo arba perėjimo metu. Jie kuriami vartotojams, priskirtiems prie pareigų, įtrauktų į grupę.

## <a name="setting-up-task-groups-optional"></a>Užduočių grupių nustatymas (pasirinktinai)

Įjungus, iškuosepant ar pereinant į ėjimas į lentą gali būti įtraukta daug užduočių. Kad būtų lengviau kontroliniams sąrašui priskirti visas reikiamas užduotis, galite sukurti pasirinktines užduočių grupes, kurios skirstys susijusias užduotis į kategorijas. Pavyzdžiui, personalo, IT ir algalapio padaliniai turi atlikti konkrečias užduotis, kad pasamdyti naują darbuotoją. Todėl jūs sukuriate šias užduočių grupes: PERSONALAS **·**, **IT** ir **Algalapis**. Tada, kai sukuriate užduotį, galite su ja susieti vieną iš tų užduočių grupių.

Norėdami į kontrolinį sąrašą įtraukti užduotį, užduočių sąrašą galite filtruoti pagal užduočių grupę, prie kurios priskirta norima užduotis. Pavyzdžiui, kai sukuriate kontrolinio sąrašo šabloną, galite filtruoti sąrašą, kad būtų rodomi tik IT užduotys, priskirtos IT **užduočių** grupei. Todėl galite užtikrinti, kad bus pasirinktos tik atitinkamos IT užduotys.

## <a name="using-checklists"></a>Kontrolinių sąrašų naudojimas

Pasamdius, atleistą arba perdėjus darbuotoją, galima pasirinkti vieną ar daugiau kontrolinių sąrašų. Užduoties terminų datos ir darbuotojų priskyrimai sukuriami pasibaigus pasamdymo, atleidimo ar perėjimo procesui. Pavyzdžiui, kai pasirenkate samdos **arba samdos** **ir išsamios informacijos** pridėjimo mygtuką, užduotys sukuriamos asmenims pagal priskyrimo tipą.

Terminas priskiriamas kiekvienai užduočiai, pridedant arba atėmus mokėjimo terminą, kuris yra korespondentinis darbuotojo darbo pradžios datai. Daugiau informacijos rasite skyriuje Užduoties [terminų datos ir Termino korespondentinės sąskaitos](#task-due-dates-and-the-due-date-offset-field) skyrius.

Jei naudojate personalo veiksmus, užduotys sukuriamos, kai pasirenkamas **mygtukas** Baigti arba veiksmas patvirtinamas.

Užduočių valdymo **darbo** srityje galite darbuotojui taikyti kontrolinį sąrašą, pasirinkdami darbuotoją paprastojo sąrašo puslapyje arba informacijos puslapyje, tada pasirinkdami **Taikyti kontrolinį sąrašą**. Paskirties datos **lauko** vertė bus naudojama skaičiuojant užduočių terminą. Paprastai tikslinė data turėtų sutapti su darbuotojo samdos, atleidimo ar perėjimo data.

Taip pat galite taikyti darbuotojui kontrolinį sąrašą atidarydami **jo** darbuotojo puslapį ir **meniu pasirinkdami kontrolinius** sąrašus.

## <a name="completing-tasks"></a>Užduočių atlikimas

**Darbuotojų savitarnos puslapyje** darbuotojas gali peržiūrėti visas jam priskirtas užduotis. Rodomos kiekvienos priskirtos užduoties **,** užduoties **·**, aprašymo **·**, instrukcijų **ir kontaktinio** asmens vertės. Be to, kiekvienai užduočiai darbuotojas "Dynamics 365" programoje gali atidaryti susietą išorinį tinklalapį arba susietą puslapį.

Užduotys taip pat gali būti rodomos numatytoje skelbimų srityje. Norėdami rodyti užduotis numatytoje skelbimų srityje:
1. Eiti į vartotojo **parinktis – nuostatos – užduočių valdymas** 
2. Pasirinkite Rodyti užduotis **numatytoje skelbimų juostoje** kaip **On**.  

>[!Note] 
>Užduočių **valdymo funkcija** turi būti įjungta funkcijų valdymo **srityje**, kad parinktis būtų rodoma vartotojo **pasirinktyse**.

Užduotis galima pažymėti kaip **Vykdoma**, **Atšaukta arba** **Baigta**. Jei užduotis buvo priskirta grupei, ji bus pažymėta kaip **Baigta**, kai vienas grupės asmuo ją užbaigs.

Užduotis taip pat galima priskirti iš naujo.
