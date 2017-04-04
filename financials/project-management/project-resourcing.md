---
title: "Projektų ištekliai"
description: "Šioje temoje pateikta informacija apie projekto finansavimą."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Projektų ištekliai

Šioje temoje pateikta informacija apie projekto finansavimą.

Vienas iš uždavinių projekto vadovams ir išteklių vadovais metu projekto planavimo etapas – išteklių paskirstymą, kur jie turi nustatyti ir užsakyti tinkamą išteklių dirbti su projektu. Microsoft Dynamics 365 operacijoms, išteklių pajėgumus projektams leidžia jums apibrėžti vaidmenis, yra traktuojami kaip laikinas išteklių, kuris gali būti skirtas konkrečių įdarbinant, arba dalis, įsipareigojimas. Naudodami šį išteklių parinkimo tipą projektų vadovai ir išteklių vadovai gali atlikti tolesnes užduotis.

-   Apibrėžti vaidmenį, turintį reikiamas kompetencijas, kad būtų lengva suderinti išteklius.
-   Naudodami vaidmenų pradinio įjungimo grafiką, pagrįstą rezervuoti išteklius.
-   Pagal projektui priskirtus vaidmenis ir išteklius įvertinti išlaidas bei nustatyti pradinį biudžetą.
-   Naudokite vaidmenų skaičius išteklių rezervavimas, kurie yra reikalingi kiekvienam įsipareigojimui.
-   Įvertinti, kiek išteklių reikia visam projekto ciklui.
-   Naudojant pradinius išteklių priskyrimus parengti darbo paskirstymo struktūrą (WBS).

[![Projekto gyvavimo ciklo](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Kaip projekto planavimo pajamos, planuojami ištekliai gali būti pakeistas į darbuotojų išteklius. Projekto vadovas taip pat galite grįžti atgal ir atnaujinti aprūpinimo ištekliais rezervavimo metu projekto etapuose.

## <a name="set-up-project-resources"></a>Projektų išteklių nustatymas
Turite nustatyti kalendorių ir jį susieti su darbuotoju. Kalendorius yra naudojamas planuoti projekto ir projekto darbo laiko išteklių, kad yra saugomos. Nustatydami kalendorių ir optimizuodami išteklius projektų vadovai gali koreguoti išteklių paskirstymą. Atsižvelgiant į kalendoriaus grafiką, ištekliams gali būti taikomi apribojimai. Galite nustatyti kalendorių ant to **kalendorius** puslapis. 

Kai nustatote kaip projekto darbuotojas, galite pasirinkti iš darbuotojų, kurie dirba įmonėje, kuriai norite nustatyti išteklių arba galite pasirinkti darbuotojus iš kitų įmonių jūsų organizacijoje. Tai yra vidinės įmonės išteklius. Šios procedūros paaiškina, kaip nustatyti darbuotojo projekto išteklių jūsų įmonėje ir kaip nustatyti vidinės įmonės projekto išteklių.

### <a name="set-up-a-worker-as-a-project-resource"></a>Darbuotojo nustatymas projekto ištekliumi

1.  Dėl į **darbuotojų** puslapis, į **darbuotojų** sąrašą, pasirinkite darbuotoją, kad norite pridėti kaip projekto išteklius ir atidaryti darbuotojas įrašo.
2.  Į veiksmų sritį, spustelėkite **projekto**&gt;**nustatymo**&gt;**projekto nustatymas**.
3.  Pasirinkite kalendorių, ir tada uždaryti puslapį.

Kaip išankstinio priskyrimo tipą taip pat galite nurodyti numatytuosius ištekliaus projektus. Išankstiniai priskyrimai gali būti naudojami, kai išteklių vadovas ar projekto vadovas iš anksto žino, su kuriais projektais dirbs išteklius. Išankstiniai priskyrimai taip pat gali būti paremti projekto rėmėjo ar kliento prašymu. Norėdami iš anskto priskirti projektą, puslapyje **Priskirti projektus**, skirtuke **Projektai**, sąraše **Likę projektai** pasirinkite atitinkamą projektą.

### <a name="set-up-an-intercompany-resource"></a>Nustatyti vidinės įmonės išteklių

Kai nustatote darbuotojas kaip vidinės įmonės išteklių, turite užpildyti sąrankos skolinimo ir skolinimosi bendrovė. 

**Skolinimo įmonė:**

1.  Dynamics 365 operacijoms, patikrinkite, kad paskolų bendrovė yra pažymėtas, ir tada atlikite aukščiau, procedūrą "Nustatyti kaip projekto darbuotojas."
2.  Apsilankę ** DK **&gt; ** reg. nustat **&gt;**tvarkant vidinių įmonių apskaitą**. Click **New**.
3.  Į į ** juridinio asmens ID ** pasirinkite paskolų bendrovė. Užpildykite likusius laukelius atitinkamai, o tada spustelėkite **išskyrus**.
4.  Eiti į ** projektų valdymo ir apskaitos **&gt; ** sąrankos **&gt;**kainos ** &gt;**perdavimo kaina**.** **
5.  Dėl į ** perdavimo kaina ** formos, spustelėkite **New**, ir į ** skolinimosi juridinio asmens ** pasirinkite atitinkama kompanija.
6.  Jei norite tik paskolų palūkanų įmonės išteklius, kurį sukūrėte šį skyrių, pradžioje, **išteklių** pasirinkite išteklių, kuriuos sukūrėte pavadinimą. Jei norite, kad visi ištekliai bendrovėje taptų prieinama skolinimosi bendrovė, palikti to ** išteklių ** lauką tuščią.
7.  Eikite į ** projektų valdymo ir apskaitos **&gt; ** sąrankos **&gt;**projektų valdymo ir apskaitos parametrai**, ir į ** vidinės įmonės ** skirtuko lape nustatykite į ** vidinės įmonės išteklių planavimas ir grafikų ** lauko į **taip**.

**Skolinimosi įmonėje:**

1.  Eikite į **projektų valdymo ir apskaitos**&gt;**projekto išteklių**&gt;**išteklių sąrašą**.
2.  Ieškos filtras, įveskite išteklių, sukurtą ankstesnės procedūros dėl skolinimo bendrovės patikrinti, kad pavadinimas yra įtrauktas į išteklių sąrašą dėl skolintis bendrovės pavadinimas.

## <a name="manage-resource-competencies"></a>Išteklių kompetencijų valdymas
Išteklių kompetencijas yra esminė išteklių valdymas. Kompetencijas galima naudoti kaip atskaitos tašką nustatant išteklius, kurie turi tinkamą įgūdžių, išsilavinimo, sertifikatų ir projektų patirties balansą. Šią informaciją reikėtų nustatyti kiekvienam ištekliui ir ją reikėtų reguliariai atnaujinti. Tokiu būdu, kai, priskiriant projekto išteklius, suderinamos konkrečios išteklių kompetencijos, galite maksimizuoti pajėgumus. [![Įgūdžius, sertifikatus, švietimo ir projekto patirties pavyzdžiai](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Tolesnėmis procedūromis paaiškinama, kaip nustatyti kai kurias ištekliaus kompetencijas. 

Norėdami nustatyti darbuotojo kompetencijas, galite naudoti arba srities Personalas sąrašo puslapį **Darbuotojai**, arba srities Projektų valdymas ir apskaita sąrašo puslapį **Ištekliai**. Šios procedūros, kad **darbuotojų** puslapyje sąrašo žmogiškųjų išteklių yra naudojami.

### <a name="set-up-competencies-certificates"></a>Kompetencijų nustatymas: sertifikatai

1.  Sąrašo puslapyje **Darbuotojai** pasirinkite darbuotojo, kurio sertifikatų informaciją pridedate, eilutę.
2.  Veiksmų srityje, skirtuke **Darbuotojas**, grupėje **Kompetencijos** spustelėkite **Sertifikatai**.
3.  Spustelėkite **Naujas**.
4.  Lauke **Sertifikato tipas** pasirinkite **PMP**.
5.  Lauke **Pradžios data** pasirinkite **2015-10-01**.
6.  Spustelėkite **Įrašyti** ir uždarykite puslapį.

### <a name="set-up-competencies-skills"></a>Kompetencijų nustatymas: įgūdžiai

1.  Sąrašo puslapyje **Darbuotojai** įsitikinkite, kad vis dar pasirinktas darbuotojas, kurį naudojote ankstesnėje procedūroje. Tada veiksmų srityje, skirtuke **Darbuotojas**, grupėje **Kompetencijos** spustelėkite **Įgūdžiai**.
2.  Spustelėkite **Naujas**.
3.  Lauke **Įgūdis** pasirinkite **Projektų valdymas**.
4.  Lauke **Lygis** pasirinkite **5, ekspert.**.
5.  Lauke **Lygio data** pasirinkite **2014-01-14**.
6.  Lauke **Darbo patirties metai** įveskite **10**.
7.  Spustelėkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-a-new-project"></a>Kurti naują projektą
1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**darbo**&gt;**projektų valdymas**.
2.  Spustelėkite **Naujas projektas** ir įveskite tolesnes reikšmes.
    -   **Projekto tipas** - laiko ir medžiagų
    -   **Projekto pavadinimas** -XYZ atnaujinti 2 etapas
    -   **Projekto grupės** -TM\_ng
    -   **Projekto sutarties ID** -00000002
3.  Spustelėkite **Kurti projektą**.

### <a name="assign-a-resource-to-a-project"></a>Ištekliaus priskyrimas projektui

1.  Spustelėkite **žmogiškųjų išteklių**&gt;**darbuotojams**&gt;**darbuotojų**.
2.  Sąraše **Darbuotojai** pasirinkite darbuotojo, kurio kompetencijas nustatėte anksčiau, įrašą ir jį atidarykite.
3.  Veiksmų srityje, skirtuke **Projektas**, grupėje **Nustatymas** spustelėkite **Priskirti projektus**.
4.  Puslapyje **Išteklių tikrinimo projekto priskyrimai** spustelėkite skirtuką **Projektai**.
5.  – Į **projektą įtraukti į atrinktų projektų**, filtras su projektu, XYZ atnaujinti 2 etapas
6.  Srityje **Likę projektai** pasirinkite projektą ir, spustelėdami rodyklę, jį pridėkite į sritį **Pasirinkti projektai**.
7.  Uždarykite puslapį.

Jei reikia, ištekliui taip pat galima priskirti kategorijų. Kategorijos tipas gali būti Išlaidos arba Įplaukos. Jis priklauso nuo jūsų organizacijos. Jei šiuo metu nėra priskirtos kategorijos išteklių, Dynamics 365 operacijoms bus ieškoti numatytąją kategoriją valandą kainų, išlaidų ir pajamų.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekto išteklių ir vaidmenų charakteristikų nustatymas

Naudodamas projektų išteklių funkcijas projekto vadovas gali kurti reikiamus projekto vaidmenis. Vaidmenys gali būti naudojami, kai patvirtinta ištekliai yra dar nežinoma, kai užsakyti išteklių. Vaidmenys gali laikinai saugomos kaip planuojami ištekliai, kad jūs ir toliau projekto planavimo etapai. 

[![Pavyzdžiui, tam tikrą vaidmenį](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarijus:** „Contoso‟ buvo pasamdyta atlikti laiko ir medžiagų projektui su patvirtinta chartija. Jaunesnysis projektų vadovas vis dar nustatinėja projekto sritį. Išteklių vadovas šiuo metu yra nustatyti konkrečius išteklius, rezervavusių parengti naują projektą. Vienas iš vaidmenų, kad projekto rėmėjas paprašė, ypatingos svarbos projektu, pobūdis yra vyresnysis projektų vadovas. Išteklių vadovas turi įgyti naujų išteklių ir apibrėžti vaidmenį sistemoje, jaunesniojo projektų vadovo pareigos jei reikia ištekliaus informacija projekto planavimo metu. 

Šie veiksmai rodo kaip išteklių vadovas nustatyti vyresnysis projektų vadovo vaidmuo ir su juo susieti išteklių charakteristikų. Vėliau vaidmenį galima naudoti ieškant turimų išteklių, kurie atitinka reikiamas išteklių kompetencijas.

1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**nustatymo**&gt;**ištekliai**&gt;**Setup vaidmenis**.
2.  Spustelėkite **Naujas** ir įveskite tolesnes reikšmes.
    -   **Rolės ID** -vyresnysis projektų vadovas
    -   **Aprašymas** -vyresnysis projektų vadovas
3.  Spustelėkite **Kurti**.
4.  Pasirinkite vaidmenį **Vyresnysis projektų vadovas** ir spustelėkite **Konfigūruoti charakteristikas**.
5.  Lauke **Charakteristikų tipas** pasirinkite **Įgūdis**.
6.  Lauke **Pasiekiamos charakteristikos** įveskite ieškomą įgūdį.
7.  Lauke **Charakteristikos tipas** pasirinkite **Sertifikatas**.
8.  Lauke **Pasiekiamos charakteristikos** įveskite ieškotino sertifikato tipą.
9.  Spustelėkite **Gerai** ir uždarykite puslapį.

### <a name="assign-a-project-resource-to-a-project"></a>Projekto ištekliaus priskyrimas projektui

1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**bendras**&gt;**projektų**&gt;**visi projektai**, ir atidaryti su **XYZ atnaujinti 2 etapas** projekto.
2.  Skirtuke **Projekto komanda ir planavimas** spustelėkite **Pridėti**.
3.  Lauke **Vaidmuo** pasirinkite **Komandos narys**.
4.  Spustelėkite **Rezervuoti kalendoriuje**.
5.  Puslapyje **Išteklių pasiekiamumas** spustelėkite **Rodinio parametrai**.
6.  Puslapyje **Koreguoti rodinio parametrus** įveskite tolesnes reikšmes.
    -   **Formatuoti datos diapazonas rodinio** - per dieną
    -   **Rodyti prieinamumą aprašymai** - taip
    -   **Ekranas, likusi talpa** - taip
7.  Išteklių sąraše pasirinkite išteklių.
8.  Spustelėkite **sunku knyga**&gt;**pilna talpa**.
9.  Uždarykite puslapį.

### <a name="assign-a-resource-to-a-default-role"></a>Ištekliaus priskyrimas numatytajam vaidmeniui

Padėti projektų ir išteklių vadovų, jūs galite išgręžti žemyn daugiau išteklių, kuriuos galima užsisakyti projektą. Numatytąjį vaidmenį galima susieti su esamu ištekliumi arba naujai gautu ištekliumi. Pavyzdžiui, kai Daniel buvo pasamdytas, jis patirtį ir įgūdžius, kad galėtų užimti verslo analitikas. Išteklių vadovas priskirti šio vaidmens kaip Daniel numatytasis vaidmuo. Todėl išteklių vadovas įtraukti Daniel dėl verslo analitikai, kurie yra pasirengę dirbti su projektais. 

Metu išteklių rezervavimui, projektų vadovai filtruoti vaidmens išteklių, kurie yra pasirengę dirbti su projektais. Kai panaudodami išteklius vadovai atlieka kelių kriterijų sprendimų analizę, šią informaciją jie gali naudoti kaip vieną iš kriterijų. Jie taip pat gali į filtrą įtraukti kitų išteklių charakteristikų ir ieškoti išteklių, turinčių konkrečių įgūdžių, išsilavinimą ir patirties konkrečiam projektui atlikti. 

**Scenarijus:** patvirtintas projektas prasidėjo, ir vyresnysis projektų vadovo vaidmuo buvo saugomos kaip planuojama išteklių planavimo etape projekto metu. Išteklių vadovas gavo išteklių užimti vyresniojo projekto vadovo vaidmeniui.

1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**projekto išteklių**&gt;**išteklių sąrašą**.
2.  Sąraše **Išteklius** pasirinkite **Danielis Goldschmidtas**.
3.  Spustelėkite **projekto išteklių**&gt;**palaikyti**&gt;**išteklių vaidmuo**.
4.  Spustelėkite **Naujas** ir įveskite tolesnes reikšmes.
    -   **Veiksminga** - (dabartinė data)
    -   **Pabaigos** - niekada
    -   **Vaidmuo** -vyresnysis projektų vadovas
5.  Spustelėkite **Įrašyti** ir uždarykite puslapį.
6.  Skirtuke **Kompetencijos** pridėkite įgūdį **ProjektVald** ir sertifikatą **PMP**.

## <a name="set-up-role-based-pricing"></a>Vaidmenimis paremtos kainodaros nustatymas
Galima nustatyti visas vaidmenų savikainas, pardavimo kainas ir perkėlimo kainas.

1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**nustatymo**&gt;**kainas**&gt;**pardavimo kaina (valandos)**.
2.  Click **New**.
3.  Įveskite įsigaliojimo datą.
4.  Stulpelyje **Vaidmuo** pasirinkite vaidmenį.
5.  Stulpelyje **Kainodara** įveskite pasirinkto išteklių vaidmens kainą.

## <a name="form-a-project-team"></a>Suformuoti projekto komandą
Norėdami naudoti vaidmenų, kurie buvo anksčiau nustatyti projekte, projekto vadovas paskirkite vaidmenis projekte. Daug funkcijų gali būti priskirtos projektui ir Dynamics 365 operacijoms automatiškai žymi šiuos vaidmenis per užsakymo, kad būtų išvengta painiavos. Pavyzdžiui, jei projekto vadovas reikalauja trijų programinės įrangos inžinierių, trijų programinės įrangos inžinierius vaidmenys, kurie turi programinės įrangos inžinierius 1, programinės įrangos inžinierius 2 ir programinės įrangos inžinierius 3 kaip jų etiketes automatiškai generuojamos. Jei anksčiau buvo nustatytos vaidmenų charakteristikos, ieškant ištekliaus jos taikomos kaip filtras. Pagal poreikį galima pridėti papildomų charakteristikų ir taip dar patikslinti iešką. 

Taip pat galima tinkinti rodinio parametrus, kad būtų galima geriau matyti išteklių prieinamumą. Parinktimis galima nustatyti valandos, dienos, savaitės, mėnesio, ketvirčio ir metų prieinamumo rodymą. Taip pat galima parinktis rodyti turimą ir likusį išteklių pajėgumą. Ši parinktis naudinga valdant laiką, kai vertinamas turimas veikloms skirtas laikas ar išteklių prieinamumas. 

Projektų vadovas pasirinkti vaidmenį puslapyje ir tada, jei yra laisvų išteklių, kuris atitinka reikalavimą, pasirinkite rezervuoti išteklius, užimti. Atkreipkite dėmesį, kad lėšos neturi būti saugomos šiuo metu planavimo etape. Kai sukuriate tam WBS, galite pakeisti vaidmenis darbuotojų išteklius projekto. Jei vaidmenys pakeičiami dirba WBS išteklių, išteklių nustatymas automatiškai atnaujina projekto komandos sąrašas ir planavimas. 

[![Projekto komanda aukcione, kuris yra rolės ir faktinio lėšų](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projekto vadovas turi įvairių projekto ištekliaus rezervavimo parinkčių, pvz., **Likęs pajėgumas**, **Visas pajėgumas**, **Pajėgumo procentas** ir **Nurodyti valandas**. Pakitus išteklių priskyrimams, šias rezervavimo parinktis galima bet kuriuo metu atšaukti. Palaikomi du tolesni rezervavimo tipai.

-   **Sunku knygos** – išteklių rezervavimas buvo patvirtintas ir patvirtinta, kad dalyvavimas už nustatytos trukmės darbą.
-   **Minkštas knygos** – išteklių rezervavimas buvo preliminariai nustatyta, kad sužadėtuvių už nustatytos trukmės darbą.

Tolesne procedūra paaiškinama, kaip sukurti projekto komandą.

### <a name="create-a-project-team"></a>Projekto komandos kūrimas

1.  Sąrašo puslapyje **Visi projektai** pasirinkite projektą ir spustelėkite **Redaguoti**.
2.  Ant į **projekto komanda ir planavimo** skirtuke, be to **grafiko pabaigos data** įveskite grafiko pradžios data dar vieną mėnesį. Pavyzdžiui, jei grafiko pradžios data yra 2017 m. birželio 24 (24/06/2017), įveskite **24/07/2017**.
3.  Click **Add**.
4.  Srityje **Į projektą įtraukti vaidmenų**, lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
5.  Spustelėkite **Reikiamos kompetencijos**.
6.  Puslapyje **Pasirinkti charakteristikas** pagal numatytuosius parametrus pasirenkamos anksčiau jūsų nustatytos vyresniojo projektų vadovo vaidmens charakteristikos. Spustelėkite **GERAI**.
7.  Puslapyje **Į projektą įtraukti vaidmenų**, lauke **Išteklių skaičius** įveskite **1**.
8.  Lauke **Išteklius** peržvalga rodo visus išteklius, turinčius reikiamas kompetencijas. Pasirinkite **Danielis Goldschmidtas** ir spustelėkite **Kurti**.
9.  Puslapyje **Projektas** spustelėkite **Pridėti**.
10. Srityje **Į projektą įtraukti vaidmenų**, lauke **Vaidmuo** pasirinkite **Komandos narys**. Lauke **Išteklių skaičius** įveskite **5**.
11. Spustelėkite **Kurti**.
12. Puslapyje **Projektai** spustelėkite **Panaudoti išteklių**.

## <a name="resource-capacity-synchronization"></a>Išteklių pajėgumų sinchronizavimas
Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija būtų perduodama bei naudojama ir planuojant projekto išteklius. Jei kalendorius pakinta, procesais pagal poreikį atnaujinamas projekto išteklių planavimas. Šie procesai taip pat padeda gerinti našumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto, kad būtų greičiau atnaujinama išteklių planavimo informacija. Rekomenduojame procesus planuoti kaip paketą, o ne po vieną. Kitu atveju atsiranda rizika, kad kažkas pamirš informacijos paskutinį sinchronizavimą apimančias datas. Jei apimančiosios datos nenaudojamos, sinchronizuojant datas gali atsirasti tarpų.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendorių sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Sinchronizavimo procesas skirtas sinchronizuoti visai išteklių kalendoriaus informacijai. Ši informacija apima pagrindinio kalendoriaus informaciją apie visus projekto išteklių kalendoriaus pajėgumo lentelės keitimus. Jei nauji ištekliai pridedami projekto, sinchronizavimo padeda užtikrinti, kad atnaujintų kalendorių informacija yra prieinama. Šį sinchronizavimą galima atlikti bet kuriuo metu. 

Rekomenduojame naudoti paketą. Sinchronizuojant pajėgumų rezervavimus galimos parinktys.

-   Spustelėkite **projektų valdymo ir apskaitos**&gt;**periodinės**&gt;**pajėgumai sinchronizavimo**&gt;**sinchronizuoti išteklių pajėgumų roll-up**.

| Parinktis | aprašymas                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taip    | Visus išteklių duomenis sinchronizuoti su kalendoriaus ir pagrindinio kalendoriaus informacija bei pakeisti visą projekto išteklių pajėgumų kalendoriaus informaciją.                                                  |
| Ne     | Pagal datų intervalo kodą ir nurodytas pradžios bei pabaigos datas sinchronizuoti išteklių duomenis. Šia parinktimi esami duomenys nepašalinami ir atnaujinama tik naujai įtrauktų išteklių informacija. |

[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Vaidmenų WBS šablonuose nustatymas
Projektų vadovai gali nustatyti WBS šablonus, kuriuos jie gali taikyti kurdami naujų projektų WBS. Projektų vadovai gali įtraukti vaidmenis, kai jie sukurti šabloną. Naudokite šią procedūrą Norėdami priskirti vaidmenį WBS template.* * **

1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**nustatymo**&gt;**projektų**&gt;**dirbti suskirstymo struktūra šablonus**.
2.  Prie pasirinkto WBS šablono spustelėkite **Išsami informacija**.
3.  Sąraše pasirinkite užduotį, tada lauke **Vaidmuo** pasirinkite užduočiai priskirtiną vaidmenį.

### <a name="work-with-a-wbs"></a>Darbas su WBS

Galite sukurti naują WBS arba WBS galite nukopijuoti iš esamo WBS šablono. Priskirdamas vaidmenis naujoms WBS užduotims projekto vadovas gali lengvai valdyti išteklius. Vaidmenis galima pakeisti gavus išteklių arba identifikavus patvirtintą išteklių darbui su užduotimi. Toks lankstumas projektų vadovams leidžia atlikti tolesnes užduotis.

-   Identifikuoti, kiek išteklių reikia WBS darbo paketams.
-   Įvertinti projekto išlaidas.
-   Nustatyti preliminarų biudžetą.
-   Pagal vaidmenis ir išteklius įvertinti veiklos trukmę.
-   Pagal turimą projektų informaciją kurti projektų valdymo planų.

Siekiant geriau išnaudoti išteklių funkcijas, į WBS įtraukta papildomų parinkčių.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parinktis</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Išteklių priskyrimas</td>
<td>Peržiūrėkite priskirtus WBS užduočių išteklius, datas, valandų skaičių ir rezervavimo tipą.</td>
</tr>
<tr class="even">
<td>Automatiškai generuoti komandą</td>
<td>Naudodami su užduotimi susietus vaidmenis automatiškai įtraukite suplanuotų išteklių. Dinamika 365 operacijoms automatiškai pasiūlo planuojami ištekliai iš daugelio kriterijų sprendimo analizę, pagrįstą vaidmenis. Kai nustatyti WBS užduočių vaidmenys bei pastangos (valandos) ir atlaisvinta struktūra, spustelėkite <strong>Automatiškai generuoti komandą</strong>. Reikiamas suplanuotų išteklių skaičius įtraukiamas į WBS ir skirtuką <strong>Projekto komanda ir planavimas</strong>.</td>
</tr>
<tr class="odd">
<td>Išteklius (išplečiamasis sąrašas)</td>
<td>Puslapyje <strong>Paleisti išteklių priskyrimą</strong> pagal nurodytą trukmę galite pasirinkti, ar išteklius planuoti tiksliai, ar apytiksliai. Galite koreguoti rodinio parametrus ir matyti bei nustatyti išteklių veiklų trukmę. Naudodami tolesnes parinktis, išteklius galite pasirinkti ir priskirti darbo paketų lygiu.
<ul>
<li><strong>Priimti</strong> – patvirtinti ištekliaus, priskirto užduočiai, keitimus.</li>
<li><strong>Atšaukti</strong> – atšaukti ištekliaus, priskirto užduočiai, keitimus.</li>
<li><strong>Priskirti automatiškai</strong> – Ši parinktis pasirenka laisvų darbuotojų išteklių atitikimo vaidmenį į pažymėtą užduotį.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**projektų**&gt;**visi projektai**.
2.  Sąraše pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.
3.  Spustelėkite **planas**&gt;**veiklos**&gt;**darbo skirstymo struktūrą**.
4.  Spustelėdami **Naujas** į WBS įtraukite tolesnes pirmo lygio veiklas.
    -   Inicijavimas
    -   Planavimas
    -   Vykdoma
    -   Stebėjimas ir valdymas
    -   Artimas

5.  Nustatyti datų ir pastangų (valandomis), kaip parodyta šių ekrano. [![Nustatymo datos ir pastangų](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Pasirinkite užduoties eilutę **Inicijavimas**, tada lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
7.  Spustelėkite **Publikuoti**.
8.  Toje pačioje eilutėje, lauke **Išteklius** pasirinkite **Danielis Goldschmidtas**.
9.  Spustelėkite **Priimti**.
10. Pasirinkite užduoties eilutę **Planavimas**, tada lauke **Vaidmuo** pasirinkite **Verslo analitikas**.
11. Spustelėkite **Publikuoti**, tada spustelėkite **Automatiškai generuoti komandą**.
12. Pasirodžiusiame dialogo lange spustelėkite **Taip**.
13. Įsitikinkite, ar lauko **Išteklius** reikšmė yra **1 verslo analitikas**.
14. Atidarykite ištekliaus **1 verslo analitikas** peržvalgą ir spustelėkite **Paleisti išteklių priskyrimų formą**.
15. Užduočiai parinkite darbuotoją.
16. Spustelėkite **minkštas priskirti**&gt;**pilna talpa**.
17. Spustelėkite **Įrašyti** ir uždarykite puslapį. 

> [!NOTE] 
> Nenorite gauti įspėjimą, kad nurodyto ištekliaus dabar yra 2, todėl daug išteklių lieka 1.
18. Puslapyje **Darbo paskirstymo struktūra** patikrinkite WBS išteklių priskyrimą ir spustelėkite **Įrašyti**.

## <a name="resource-fulfillment-for-planned-resources"></a>Suplanuotų išteklių panaudojimas
Projekto vadovas gali planuoti reikiamus projekto išteklių vaidmenis. Šiuos suplanuotus išteklius išteklių vadovas matys kaip užklausas puslapyje **Išteklių panaudojimas** ir jis gali priskirti faktinius išteklius.

1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**projektų**&gt;**visi projektai**.
2.  Sąraše pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.
3.  Spustelėkite **Projektas**.
4.  Spustelėkite **Redaguoti**.
5.  Dėl į **projekto komanda ir planavimo** grupėje ** ** spustelėkite **pridėti**.
6.  Dialogo lange **Įtraukti vaidmenis** pasirinkite vaidmenį **Programinės įrangos kūrėjas**.
7.  Spustelėkite **Kurti**.
8.  Uždarykite projekto puslapį.
9.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**projekto išteklių**&gt;**išteklių vykdyti**.
10. Prie projekto **XYZ atnaujinimas, 2 etapas** pasirinkite **1 programinės įrangos kūrėjas**.
11. Pasirinkite darbuotoją ir spustelėkite **Priskirti**.
12. Patikrinkite, ar pašalinta projekto **XYZ atnaujinimas, 2 etapas** eilutė **1 programinės įrangos kūrėjas**.
13. Skirtuke **Projekto komanda ir planavimas** prie projekto **XYZ atnaujinimas, 2 etapas** patikrinkite, ar darbuotojas, kurį pasirinkote atlikdami 11 veiksmą, įtrauktas kaip **Programinės įrangos kūrėjas**.

## <a name="requests-for-project-resources"></a>Prašymai dėl projekto išteklių
Projekto išteklių planavimo funkciją palaiko tik išteklių vadovais paskirstyti darbuotojų išteklius užduočių ar projektų. Norėdami įgalinti šią funkciją, atlikite nurodytas užduotis arba patikrinti, kad jie buvo atlikti.

-   Nustatyti numeracijas.
-   Projektų valdymo ir apskaitos darbo eigos nustatymas.
-   Įgalinti išteklių prašymą darbo eigą.

Turite patikrinti arba baigė aukščiau užduotis, galėsite atlikti šias užduotis reikia.

-   Kurti išteklių prašymą minkštas užsakymas darbuotojų išteklius.
-   Stebėti išteklių prašymus.
-   Įvykdyti išteklių prašymus.
-   WBS prašyti darbuotojų išteklius.
-   Užsakyti išteklių be prašymą dėl darbuotojų išteklių projektą.

## <a name="monitor-project-teams"></a>Monitoriaus projekto komandos
1.  Spustelėkite **projektų valdymo ir apskaitos**&gt;**projektų**&gt;**visi projektai**.
2.  Projektų sąraše spustelėkite projekto **XYZ atnaujinimas, 2 etapas** saitą **Projekto ID**.
3.  „FastTab‟ **Projekto komanda ir planavimas** patikrinkite, ar išvardyti projekto ištekliai yra teisingi.



