---
title: „Regulatory Configuration Services (RCS)” – globalizacijos funkcijos
description: Šioje temoje aiškinama, kaip pasinaudoti „Microsoft Regulatory Configuration Services (RCS)” ir Visuotine saugykla, kad sukurtumėte ir pasinaudotumėte globalizacijos funkcijomis.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: b701e6bfa14ac30e02bfe79666963db4ee657302
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002798"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>„Regulatory Configuration Services (RCS)” – globalizacijos funkcijos

[!include [banner](../includes/banner.md)]

Galite naudoti „Microsoft Regulatory Configuration Services (RCS)“, norėdami sukurti globalizacijos funkciją, naudojamą globalizacijos paslaugose, pavyzdžiui, el. sąskaitų faktūrų išrašymo paslaugai. RCS leidžia atlikti šias užduotis:

- Nurodyti susijusius funkcijos komponentus.
- Valdyti funkcijos ciklą naudojant funkcijos būseną.
- Sukurti funkciją, kurią galima naudoti apibrėžtose aplinkose.
- Bendrinti funkciją su kitomis organizacijomis.

Šios procedūros paaiškina, kaip vartotojas RCS gali pridėti globalizacijos funkciją ir susijusius komponentus, atnaujinti funkcijos būseną ir padaryti šią funkciją prieinamą, kad ji galėtų būti naudojama globalizacijos paslaugose.

Prieš atlikdami procedūras, turite atlikti veiksmus, susijusius su šiomis užduotimis:

- Prisijungti prie savo RCS.
- Sukurti ir aktyvuoti konfigūracijos teikėją. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Savo „Finance and Operations” programoje, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Jei jūsų įmonei RCS aplinka neparengta, pasirinkite **Regulatory services – Konfigūracija** ir vykdykite instrukcijas, kad ją parengtumėte.

> [!NOTE]
> Jei RCS aplinka jūsų įmonei jau parengta, pasiekite ją naudodami puslapio URL ir pasirinkdami prisijungimo parinktį.

## <a name="turn-on-the-globalization-features"></a>Įjunkite Globalizacijos funkcijas

1. Savo RCS egzemplioriuje pasirinkite **Funkcijos valdymo** plytelę.
2. **Funkcijų valdymo** darbo srityje sąraše pasirinkite **Globalizacijos funkcijos** ir pasirinkite **Įjungti dabar**.

    ![Globalizacijos funkcijos Funkcijų valdyme](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globalizacijos funkcijos

Norėdami naudoti Globalizacijos funkciją, pirmiausia turite ją importuoti iš Visuotinės saugyklos ir sukurti savo versiją. Yra du būdai, kaip pridėti Globalizacijos funkcijas:

- Pridėkite išvestinę funkciją, pagrįstą esama funkcija, kuri buvo publikuota ar bendrai naudojama.
- Pridėkite naują funkciją, kurią sukūrėte nuo pradžių.

## <a name="access-globalization-features"></a>Prieiga prie Globalizacijos funkcijų

1. Įsitikinkite, kad **Globalizacijos funkcijos** funkcija yra įjungta Funkcijų valdyme, kaip aprašyta anksčiau šioje temoje.
2. Atverkite naują **Globalizacijos funkcijos** darbo sritį, o tada dalyje po **Funkcijos** pasirinkite **El. SF išrašymas** plytelę.

    ![Visuotinių funkcijų darbo sritis](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    **El. SF išrašymo funkcijos** puslapis atvertas.

    ![El. sąskaitų faktūrų išrašymo funkcijų puslapis](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Įtraukite išvestinę Globalizacijos funkciją

Galite pridėti naują Globalizacijos funkciją išvesdami ją iš esamos, kuri buvo publikuota ar bendrai naudojama.

1. Pasirinkite **Importuoti**, kad atvertumėte **Importuoti funkciją iš Visuotinės saugyklos** puslapio.

    ![Importuokite funkciją š Visuotinės saugyklos puslapio](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Pasirinkite **Sinchronizuoti**, kad gautumėte naujausias funkcijas.

    Sinchronizuotame sąraše yra funkcijų, kurias galite naudoti, nes jas publikavo „Microsoft ” arba dėl to, kad kitas konfigūracijos teikėjas bendrino jas su jumis.

    ![Sinchronizuotas funkcijų sąrašas](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Sąraše pasirinkite importuotinas funkcijas ir pasirinkite **importuoti**. Gausite pranešimą, kai atrinktos funkcijos bus sėkmingai importuotos.

    ![Sėkmingo importavimo pranešimas](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Pasirinkite **Įtrauki**, tada išplečiamojo dialogo lango lauke pasirinkite **Pagrįstas esama versija** parinktį.
5. Įveskite funkcijos pavadinimą ir aprašymą.
6. Galimų funkcijų sąraše pasirinkite pagrindinę funkcijos versiją ir pasirinkite **Kurti priemonę**.

    ![Išvestos funkcijos pridėjimas](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Jūsų pridėta funkcija sukuriama ir jos būsena yra **Juodraštis**.

    ![Išvestinė funkcija, turinti Juodraščio būseną](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Peržiūrėkite funkcijų komponentus, kad nustatytumėte, kurie naujiniai yra reikalingi:

    - Peržiūrėkite konfigūracijas, jei jums reikia tinkinti Elektroninių ataskaitų (ER) formatus ir jų susiejimą su formato priskyrimais, skirtais funkcijos versijai.
    - Peržiūrėkite sąranką, jei jums reikia tinkinti **Veiksmai** skirtuką, **Taikymo taisyklės** skirtuką arba **Kintamieji** skirtuką funkcijos versijai.

8. **Versijos** skirtuke pasirinkite **Įsigalioja nuo** datą ir įveskite aprašą, jei **Aprašas** laukas yra tuščias.
9. Pasirinkite **Pakeisti būseną**, kad užbaigtumėte funkciją. Baigtos funkcijos gali būti prieinamos tam tikrai aplinkai, kad jos galėtų būti naudojamos Globalizacijos paslaugose arba jos gali būti paskelbtos Visuotinėje saugykloje.

> [!NOTE]
> Funkcijos, turinčios **Funkcijos versijos būsena** vertę **Paskelbta**, gali būti bendrinamos su išorinėmis organizacijomis.

## <a name="add-a-new-globalization-feature"></a>Įtraukite naują Globalizacijos funkciją

Galite pridėti naują Globalizacijos funkciją sukurdami ją nuo pradžių.

1. **Importuoti funkciją iš Visuotinės saugyklos** puslapyje pasirinkite **Pridėti**, tada išplečiamojo dialogo lango lauke pasirinkite **Nauja funkcija** parinktį.
2. Įveskite funkcijos pavadinimą ir aprašymą.
3. Pasirinkite **Sukurti funkciją**.

    ![Naujos funkcijos įtraukimas](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. **Versijos** skirtuke pasirinkite **Įsigalioja nuo** datą ir pasirinkite **Keisti būseną**, kad baigtumėte funkciją. Baigtos funkcijos gali būti prieinamos tam tikrai aplinkai, kad jos galėtų būti naudojamos Globalizacijos paslaugose arba jos gali būti paskelbtos Visuotinėje saugykloje.

> [!NOTE]
> Funkcijos, turinčios **Funkcijos versijos būsena** vertę **Paskelbta**, gali būti bendrinamos su išorinėmis organizacijomis.

## <a name="feature-component-overview"></a>Funkcijos komponento apžvalga

Globalizacijos funkcijos susideda iš kelių komponentų:

- **Versija** – šis komponentas palaiko funkcijų ciklo valdymą ir leidžia vartotojams valdyti skirtingas funkcijos versijas.
- **Konfigūracijos** – šis komponentas leidžia vartotojams valdyti, peržiūrėti ir redaguoti ER formatus ir formatų susiejimus.
- **Sąrankos** – šis komponentas leidžia globalizacijos paslaugų vartotojams, pavyzdžiui, el. SF paslaugos, tvarkyti susijusios funkcijos versijos sąranką. Todėl jis palaiko lanksčią bendravimo ir atsakymų taisyklių konstrukciją.
- **Aplinka** – šis komponentas leidžia globalizacijos paslaugų vartotojams, pvz., elektroninių SF paslaugos, valdyti aplinką, kurioje naudojama funkcijos versijos sąranka, ir suteikti autorizavimą vartotojams, kurie turės prieigą prie jos.
- **Organizacijos** – šis komponentas leidžia vartotojams bendrinti funkciją su išorinėmis organizacijomis.

## <a name="configuring-feature-components"></a>Funkcijos komponentų konfigūracija

### <a name="version-and-status"></a>Versija ir būsena

Versija naudojama Globalizacijos funkcijos ciklo valdymui valdyti.

Būsena gali būti keičiama **Būsena** lauke **Versija** skirtuke. Galimos šios būsenos:

- **Juodraštis** – funkcija gali būti redaguojama tik tada, kai ji yra šios būsenos.
- **Baigta** – funkcija ir visi susiję komponentai buvo užbaigti (baigti) ir jų negalima redaguoti.
- **Publikuota** – funkcija ir visi susiję komponentai publikuoti Visuotinėje saugykloje.
- **Bendrinta** – funkcija ir visi susiję komponentai buvo bendrinti su išorinėmis organizacijomis.
- **Įjungta** – funkcija ir visi susiję komponentai buvo įjungti Globalizacijos paslaugai, pvz., el. sąskaitų faktūrų išrašymo paslauga, naudoti.

> [!NOTE]
> Funkcijos turi būti nuosekliai perkeltos per kai kurias būsenas. Todėl ne kiekviena būsena gali būti pasiekiama kiekviename ciklo etape.

### <a name="configurations"></a>Konfigūracijos

Toliau nurodyti veiksmai galimi šioms konfigūracijoms:

- **Peržiūrėti** – peržiūrėkite paryškintas funkcijų konfigūracijas, kurias nereikia atnaujinti.
- **Redaguoti** – sukurkite pasirinktos konfigūracijos juodraštinę versiją, kad galėtumėte redaguoti formatą arba formatuoti susiejimą Formato dizaino įrankyje.
- **Naikinti** – sunaikinkite pasirinktą funkcijos konfigūraciją.
- **Pritaikyti kitoje vietoje** – pritaikykite funkciją kitam. Daugiau informacijos rasite [Pritaikykite Globalizacijos funkcijas kitoje vietoje](#rebase) skyriuje, aptartame vėliau šioje temoje.

### <a name="setups"></a>Nustatymai

Toliau nurodyti veiksmai galimi funkcijos sąrankai:

- **Pridėti** – sukurkite naują funkcijos sąranką. Ši funkcijos sąranka gali būti išvesta iš esamos funkcijos sąrankos arba sukurta nuo pradžių.
- **Naikinti** – sunaikinkite pasirinktą funkcijos sąranką.
- **Peržiūrėti** – peržiūrėkite paryškintą funkcijos sąranką, kurią nereikia keisti.
- **Redaguoti** – kurkite, sunaikinkite arba modifikuokite trijų pagrindinių funkcijos sąrankos komponentų atributus:

    - Veiksmai ir jų parametrai
    - Taikymo taisyklės
    - Kintamieji

![Funkcijos versijos sąrankos puslapis](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Aplinkos

Toliau nurodyti veiksmai galimi aplinkoms:

- **Įjungti** – pasirinktai funkcijos versijai pasirinkite publikuotą aplinką ir pasirinkite **Įsigalioja nuo** datą, kada ji turėtų būti prieinama. Daugiau informacijos rasite [Konfigūruokite aplinkas aktyvavimui](#configureenvironment) skyriuje, aptartame vėliau šioje temoje.
- **Atšaukti** – pašalinkite aplinką funkcijos sąrankai.

### <a name="organizations"></a>Organizacijos

Atlikite šiuos veiksmus, kad bendrintumėte Globalizacijos funkciją su išorine organizacija.

1. **El. sąskaitų faktūrų išrašymo funkcijos** puslapyje pasirinkite funkciją ir funkcijos versiją, kurią norite bendrinti.
2. **Organizacijos** skirtuke pasirinkite **Bendrinti su**, tada išplečiamajame dialogo lange įveskite organizacijos domeno pavadinimą.
3. Pasirinkite **Bendrinti**.

    ![Funkcijos bendrinimas su organizacija](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Funkcija bendrinama su pasirinkta organizacija ir ji prieinama tai organizacijai Visuotinėje saugykloje. Iš ten funkcija gali būti importuojama į organizacijos egzempliorių RCS arba „Dynamics 365 Finance”, kad ja galima būtų naudotis.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Pritaikykite išvestines Globalizacijos funkcijas kitoje vietoje

Galite pritaikyti išvestinę Globalizacijos funkciją kitoje vietoje naujai arba atnaujintai pagrindinei funkcijos versijai. Tokiu būdu pakeitimai, atlikti pagrindinėje versijoje, gali būti automatiškai atnaujinti. Atnaujintą pagrindinę funkcijos versiją sukuria pirminės konfigūracijos teikėjas, ji publikuojama arba bendrinama.

![Atnaujinta pagrindinės funkcijos versija](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Pavyzdžiui, jei norite pritaikyti jūsų sukurtą išvestinę funkcijos versiją kitoje vietoje, pirmiausia turite gauti naujausią šios funkcijos versiją importuodami ją iš Visuotinės saugyklos.

1. **El. sąskaitų faktūrų išrašymo funkcijos** puslapyje pasirinkite **Importuoti**.
2. Pasirinkite **Sinchronizuoti**, kad gautumėte naujausias funkcijas.
3. Funkcijų sąraše pasirinkite funkcijas, kurias norite importuoti, ir tada pasirinkite **Importuoti**.

    ![Naujausios funkcijos versijos importavimas](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Funkcijų sąraše pasirinkite funkciją, kurią norite pritaikyti kitoje vietoje.
5. **Versija** skirtuke pasirinkite **Nauja**, kad sukurtumėte juodraštinę versiją.

    ![Nauja juodraštinė versija sukurta](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Pasirinkite **Pritaikyti kitoje vietoje**.
7. Dialogo lange **Pritaikyti kitoje vietoje** pasirinkite naujausią funkcijos versiją, kurią norite pritaikyti kitoje vietoje.

    ![Pritaikymo kitoje vietoje dialogo langas](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Pasirinkite **Gerai**.
9. Peržiūrėkite funkcijos komponentus ir atlikite būtinus pakeitimus.
10. Pasirinkite **Pakeisti būseną**, kad užbaigtumėte pritaikytą kitoje vietoje funkciją. Kai pritaikymas kitoje vietoje baigiamas, galite atlikti papildomus veiksmus. Pavyzdžiui, galite publikuoti funkciją ir ją padaryti prieinamą naudojimui Globalizacijos paslaugose.

    ![Funkcijos būsena atnaujinta į Baigta](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Konfigūruoti aplinkas, skirtas Globalizacijos funkcijoms

Globalizacijos paslaugų vartotojai gali valdyti aplinką, kad nustatytų Globalizacijos funkciją ir suteiktų autorizavimą kitiems vartotojams, kurie turės prieigą prie jos.

1. **Globalizacijos funkcijos** darbo srityje, o tada dalyje po **Aplinkos** pasirinkite **El. SF išrašymas** plytelę.

    ![Globalizacijos funkcijų darbo sritis](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Pasirinkite **Pagrindiniai saugyklos parametrai** ir pasirinkite **Nauja**, kad sukurtumėte „Azure Key Vault” slaptažodį.
3. Įveskite pagrindinės saugyklos aprašą ir tada **Pagrindinės saugyklos URl** lauke įveskite URL, identifikuojantį Pagrindinės saugyklos šaltinį, esantį „Azure”.
4. **Sertifikatai** „FastTab” pasirinkite **Pridėti**, kad pridėtumėte sertifikatą, ir įveskite kiekvieno sertifikato pavadinimą ir aprašą.

    ![Pridėtas sertifikatas](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Pasirinkite **Nauja**, kad sukurtumėte naują aplinką.
6. Įveskite pavadinimą, aprašą ir bendrintos prieigos parašo atpažinimo ženklo slaptažodį, reikalingą saugojimui.
7. **Vartotojai**„FastTab” pasirinkite **Nauja**, kad pridėtumėte vartotoją, kuriam bus suteikta teisė pasiekti šią aplinką.
8. Įveskite vartotojo ID ir el. pašto adresą.
9. Pakartokite 7 ir 8 žingsnius, jei norite pridėti daugiau vartotojų.
10. Pasirinkite **Publikuoti**, kad publikuotumėte aplinką.

    ![Publikuota aplinka](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]