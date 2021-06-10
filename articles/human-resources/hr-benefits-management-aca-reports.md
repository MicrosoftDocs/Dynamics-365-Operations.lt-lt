---
title: Kurti prieinamą priežiūros akto ataskaits išmokų valdyme
description: Šioje temoje aprašoma, kaip išmokų valdymas padeda jums sekti informaciją pateiktą formoje 1095-B ir formoje 1095-C prieinamos priežiūros akto (ACA) darbuotojo mandatui.
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1417232baeaf03721bd0b25cc3f9fd5f750c65d5
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052270"
---
# <a name="generate-aca-reports-in-benefits-management"></a>Kurti ACA ataskaitas išmokų valdymą

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Išmokų valdymas padeda jums sekti informaciją pateiktą formoje 1095-B ir formoje 1095-C prieinamos priežiūros akto (ACA) darbuotojo mandatui. Kaip ACA ataskaitų pajėgumai, sena **Išmokų** darbo sritis, ši funkcija taikimoa tik juridiniams asmenims JAV.

Norėdami naudoti šią funkciją, turite pirma įjungti **Papildomų išmokų valdymas**. Dėl daugiau informacijos, įskaitant svarbius konfliktus apie išmokų valdymą, žr. [Įjungti ar išjungti išmokų valdymą](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Galite naudoti ACA ataskaitas tik iš **Išmokų valdymo** darbo srities ar senos **Išmokų** darbo srities, ne iš abiejų. Pavyzdžiui, jei perjungiate į išmokų valdymą, ACA ataskaitos bus prieinamos tik iš **Išmokų valdymo** darbo srities, ne iš senos **Išmokų** darbo srities.
>
> Jei perjungsite į išmokų valdymą įtraukimo metų viduryjė, turite tiksliai konfigūruoti darbuotojo duomenis visiems metams išmokų valdyme. Tokiu būdu, užtikrinsite, kad gausite tikslią ataskaitos informaciją už visus metus.

## <a name="getting-started"></a>Darbo pradžia

Norėdami sekti informaciją 1095 formoms, pirmiausia sukurkite vieną ir daugiau išlaikomos priežiūros aprėpties grupių. Šios grupės nurodo šią informaciją:

- Aprėpties pasiūlymas pateiktas darbuotojui
- Darbuotojo dalis mažiausių kaštų mėnesio premijos, jei kaštai viršija federalinį skurdo lygį
- Saugus uostas naudojamas darbuotojo, jei taikomas

Išlaiikymo priežiūros aprėpties grupės jums padeda valdyti šią informaciją keliems darbuotojų įrašams, kurie turi tokią pačią sąlygą. Galite nesunkiai priskirti grupes vienam ar keliems darbuotojams.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Kurti ar redaguoti išlaikomos priežiūros aprėpties grupę

1. Darbo srityje **Išmokų valdymas** rinkitės **Išlaikymo priežiūros aprėpties grupė**.

    ![Rinkitės išlaikomos priežiūros aprėpties grupę](./media/hr-benefits-management-aca-coverage-group.png)

2. Rinkitės **Nauja** tam, kad sukurtumėtė nauja išlaikymo priežiūros aprėpties grupę arba **Redaguotumėte** siekiant keisti esančią grupę.

    ![Rinktis naują ar redaguoti](./media/hr-benefits-management-aca-new.png)

3. Užpildykite toliau nurodytus laukus.

    | Laukas | aprašymas |
    |---|---|
    | Pavadinimas / vardas ir (arba) pavardė | Įvesti grupės pavadinimą. |
    | aprašymas | Įveskite grupės aprašą. |
    | Draudimo pasiūlymas | Aprėptis siūloma darbuotojams, jų sutuoktiniams ar partneriams ir jų išlaikytiniams. |
    | Darbuotojui tenkanti išlaidų dalis | Suma, už kurią atsakingas darbuotojas. |
    | Taikomas 4980H skyrius dėl saugaus prieglobsčio | 4980H saugaus uosto ar perlaidos atleidimo kodas. |
    | Plano pradžios mėnuo | Rinktis kalendorinį mėnesį, kai jūsų išmokos plano metai prasideda. |
    | Grupė galioja nuo | Pirmoji data, kada įsigalioja įrašas. |
    | Grupė galioja iki | Paskutinė data, kada galioja įrašas. Jei nėra galiojimo pabaigos datos, įveskite **Niekada**. |

    ![Kurti aprėpties grupę](./media/hr-benefits-management-aca-new-group.png)

4. Pasirinkite **Įrašyti**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Priskirti kelis darbuotojus išlaikymo priežiūros aprėpties grupei

1. Darbo srityje **Išmokų valdymas** rinkitės **Išlaikymo priežiūros aprėpties grupė**.
2. Rinktis grupę siekiant priskirti darbuotojus.
3. Rinktis **Masinis priskyrimas**.

    ![Rinktis Masinis priskyrimas](./media/hr-benefits-management-aca-mass-assignment.png)

4. Rinktis darbuotojus sąraše ir tuomet rinktis **Priskirti**.

    ![Priskirti pasirinktus darbuotojus grupei](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Išlaikyti kelias aprėpties parinkties versijas

Galite išlaikyti kelias bet kurios aprėpties grupės versijas. Kai kas nors keičiasi jūsų organizacijoje arba siūlomose išmokoste, galite laikyti grupės informaciją naujintą be poreikio kurti naują grupę ar paskirti iš naujo darbuotjous jai.

Jums sukūrus išlaikytinos priežiūros aprėpties grupę, galite priskirti masiškai darbuotojus jai. Galite ir atskirai priskirti darbuotojus grupėms ir nurodyti,ar ACA informacija yra sekama ir pranešama.

Jei neturite sekti ir pranešti ACA informacijos darbuotojui, galite nustatyti **Pranešti aprėptį** parinktį į **Ne**. Pavyzdžiui, jums gali reikėti ne viso etato darbuotojų, kuriems nereikia ACA pranešimų.

### <a name="override-default-values-for-an-employee"></a>Viršyti nustatytas darbuotojui vertes

Darbuotojams, kurie turi priskirtą išlaikymo priežiūros aprėpties grupę, galite keisti tolesnes parinktis bet kuriems mėnesiams, kuriems reikia kitų verčių:

- Draudimo pasiūlymas
- Darbuotojui tenkanti išlaidų dalis
- Taikomas 4980H skyrius dėl saugaus prieglobsčio

> [!NOTE]
> 2020 ACA ataskaitoms, turite pranešti darbo ir namų ZIP kodus Formoje 1095-C. Vertės užpildomos automatiškai pagal esamas aktyvias vietas. Jei bet kuri vieta skiriasi bet kada metuose, turite viršyti vertę. **ZIP kodo** laukelis (eilutę 17) 1095-C ataskaitoje yra užpildomas tik, jei **Aprėpties siūlymas** kode yra **1L** iki **1Q**, kaip štai:
>
> - **1L, 1M, ar 1N:** Pagrindinės gyvenamosios vietos ZIP kodas
> - **1O, 1P, ar 1Q:** Pagrindinės darbo vietos ZIP kodas

Norėdami įvesti išlygas bet kurioms išlaikymo priežiūros aprėpties grupės vertėms, atlikite šiuos veiksmus.

1. **Žmogiškuosiuose ištekliuose** darbo srityje pasirinkite **Nuorodos** ir tuomet pasirinkite **Darbuotojai**.
2. Rinkitės darbuotoją sąraše.
3. Skirtuke **Įdarbinimas**, **Daugiau informacijos** skyriuje rinkitės **Išlaikymo priežiūros aprėpties grupė**.

    ![Keičiančios vienam darbuotojui parinktys](./media/hr-benefits-management-aca-change-single-employee.png)

4. Pasirinkite **Redaguoti**.
5. Kiekvienam mėnesiui, kuriam reikia keitimų, rinkitės **Viršyti numatytą** žymimą laukelį ir tada keiskite kitas vertes, kaip būtina.

    ![Numatytų verčių viršijimas](./media/hr-benefits-management-aca-override-default.png)

6. Pasirinkite **Įrašyti**.

## <a name="report-health-care-coverage"></a>Pranešti apie sveikatos priežiūros draudimą

Turite sekti visus darbuotojo išlaikomu, savarankiško sveikatos priežiūros draudimo atvejus pilno ir nepilno etato darbuotojams. Įtraukite visus darbuotojus, kartu su jų išlaikytiniais į 1095-C ataskaitą už mėnesius, kai jie buvo drausti.

Norėdami nurodyti, ar išmokų planas bus praneštas, atlikite šiuos veiksmus.

1. Darbo srityje **Išmokų valdymas** rinkitės **Išmokų planai**.
2. Pasirinkite išmokų planą, kurį pranešite.
3. Pasirinkite **Redaguoti**.
4. Rinkitės **Pranešti pagal prieinamų sevikatos priežiūros paslaugų akto** parinktį **Taip**.

    ![Sveikatos priežiūros draudimo ataskaitos](./media/hr-benefits-management-aca-report-coverage.png)

5. Pasirinkite **Įrašyti**.

Jei darbuotojas pasirenka sveikatos priežiūros apimtį išlaikytiniui, jo aprėpties laikotarpis nustatomas pagal datą, kai išlaikytinis buvo įtrauktas ar pašalintas. Aprėpties datos priklausiniams yra automatiškai skaičiuojamos pagal laikotarpį, kai išlaikytinis atitiko ir buvo aktyvus plane įsitraukimo metais.

## <a name="generate-1095-b-and-1095-c-forms"></a>Kurti 1095-B ir 1095-C formas

Galite taip pat kurti ACA 1095-B ir 1095-C formas produkte ir tada dalyti juos visiems savo darbuotojams. Galite elektroniniu būdu kurti formą 1095-C ir atitinkamą 1094-C perdavimo failą siekiant nusiųsti vidaus pajamų paslaugas (IRS).

1. Darbo srityje **Išmokų valdymas**, rinkitės **ACA 1095-B formą** ar **ACA 1095-C formą**.
2. Keiskite parametrus kaip reikia ir tada rinkitės **Gerai**.

    > [!NOTE]
    > Jei spausdinate 1095-C formas daugiau nei 500 darbuotojų, gausite daugiau nei vieną PDF failą. Rekomenduojame jums padidinti vertę **Maksimalus failo dydis megabaitais** laukelį **Dokumento valdymo parametrų** puslapyje iki **150**. (Tam, kad greitai atvertumėte tą puslapį, galitet naudoti paieškos laukelį naršymo juostoje.)
    >
    > ![Maksimalaus failo dydžio keitimas](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Norėdami patikrinti savo ataskaitų statusą ir jas peržiūrėti, naudokite paieškos laukelį naršymo juostoje, kad atvertumėte **Elektroninių ataskaitų darbų** puslapį.

    ![Elektroninių ataskaitų darbų puslapio paieška](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Rinkitės peržiūrimą ataskaitą ir tada rinkitės **Rodyti failus**.

    ![Failų rodymas](./media/hr-benefits-management-aca-show-files.png)

5. Pasirinkite **Atidaryti**.

    ![Failo atidarymas](./media/hr-benefits-management-aca-open-file.png)

6. Pranešimų juostoje, kuri pasirodo naršymo lango apačioje, atverkite zip failą ir tada rinkitės ataskaitą. Galite peržiūrėti ar spausdinti PDF failą.

    ![Pavyzdžio 1095-C forma](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>Peržiūrėti ACA aprėpties informaciją

**Darbuotojo prieinamų sveikatos priežiūros paslaugų** puslapis rodo šią informaciją:

- Darbuotojai priskirti kiekvienai aprėpties grupei
- Darbuotojai neturintys būti įtraukti į ataskaitą
- Nepriskirti darbuotojai

Norėdami peržiūrėti šią informaciją, imkitės tokių veiksmų.

1. Darbo srityje **Išmokų valdymas** rinkitės **Darbuotojo priežiūros aprėpties grupė**.
2. Laukelyje **Grupės pavadiimas** rinkitės grupę.

    ![Aprėpties ACA peržiūra](./media/hr-benefits-management-aca-view-coverage.png)

Jei bet kurios iš numatytų verčių prieinamų sveikatos priežiūros paslaugų grupė buvo viršyta, žvaigždutė pasirodo šalia pakeistos vertės. Jei vertės visiems 12 mėnesių yra tokios pačios ir jos nebuvo viršytos, vertė pasirodo **Visų 12 mėnesių** stulpelyje.

Galite peržiūrėti darbuotoją, kuris yra pažymėtas kaip ne ACA pranešamas ir kuris neturi formos 1095-C. Laukelyje **Filtruoti pagal** rinkitės **Ne ACA įtraukiamas į ataskaitą**.

Galite peržiūrėti darbuotojus, kurie nėra priskirti grupei ar kurie nėra priskirti pasibaigusiai grupei. Laukelyje **Filtruoti pagal** rinkitės **Nepriskirta ar pasibaigusi grupė**.

### <a name="export-to-excel"></a>Eksportuoti į Excel

Norėdami eksportuoti bet kokius sąrašus į „Microsoft Excel“, atlikite šiuos žingsnius.

1. Pasirinkite mygtuką **Atidaryti naudojant „Microsoft Office“**.
2. Rinkitės **HCM „Human Resources“ laikina lentelė vidaus vartojimui**.
3. Rinkitės **Atsisiųsti**.

### <a name="view-aca-reportable-dependents"></a>Peržiūrėti ACA ataskaitos išlaikytinius

Jums būtina pranešti apdraustus asmenis, nes suteikiate savarankišką draudimą, galite peržiūrėti visus išlaikytinius, kurie apdrausti išmokų planais ir pažymėti kaip **ACA pranešama**. Veiksmų juostoje rinkitės **Žiūrėti išlaikytinių draudimą**.

![Aprėpties išlaikytinio peržiūra](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Aprėpties informacija darbuotojo išlaikytiniams yra rodoma.

![Išlaikytinių draudimas](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Puslapis rodo tik išmokų planus, kurie pažymėti kaip **ACA pranešami**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]