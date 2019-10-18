---
title: Projektų ištekliai
description: Šioje temoje pateikiama informacija apie projektų išteklius.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174540"
---
# <a name="project-resourcing"></a>Projektų ištekliai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie projektų išteklius.

Projektų planavimo etape vienas iš iššūkių, su kuriais susiduria projektų vadovai ir išteklių vadovai, yra išteklių paskirstymas, kurio metu jie turi nustatyti ir projekto darbui rezervuoti teisingą išteklių. Programoje „Dynamics 365 Finance“ projektų išteklių galimybės jums leidžia apibrėžti vaidmenis, laikomus laikinais ištekliais, kuriuos galima rezervuoti konkrečiam įtraukimui ar įtraukimo daliai. Naudodami šį išteklių parinkimo tipą projektų vadovai ir išteklių vadovai gali atlikti tolesnes užduotis.

- Apibrėžti vaidmenį, turintį reikiamas kompetencijas, kad būtų lengva suderinti išteklius.
- Naudojant vaidmenis apibrėžti pradinį įtraukimo grafiką, paremtą rezervuotais ištekliais.
- Pagal projektui priskirtus vaidmenis ir išteklius įvertinti išlaidas bei nustatyti pradinį biudžetą.
- Naudojant vaidmenis įvertinti, kiek išteklių reikia rezervuoti kiekvienam įtraukimui.
- Įvertinti, kiek išteklių reikia visam projekto ciklui.
- Naudojant pradinius išteklių priskyrimus parengti darbo paskirstymo struktūrą (WBS).

[![Projekto vykdymo trukmė](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Planuojant projektą suplanuotus išteklius galima pakeisti darbuotojams priskirtais ištekliais. Projekto vadovas taip pat gali bet kokiame projekto etape grįžti ir atnaujinti išteklių rezervavimus.

## <a name="set-up-project-resources"></a>Projektų išteklių nustatymas
Turite nustatyti kalendorių ir jį susieti su darbuotoju. Kalendorius naudojamas projektui planuoti ir projektui rezervuotų išteklių darbo laikui. Nustatydami kalendorių ir optimizuodami išteklius projektų vadovai gali koreguoti išteklių paskirstymą. Atsižvelgiant į kalendoriaus grafiką, ištekliams gali būti taikomi apribojimai. Puslapyje **Kalendoriai** galite nustatyti kalendorių.

Kai darbuotoją nustatote kaip projekto išteklių, galite pasirinkti iš įmonėje, kuriai nustatote išteklius, dirbančių darbuotojų. Taip pat galite pasirinkti iš kitų savo organizacijos įmonių darbuotojų. Šie darbuotojai vadinami vidiniais įmonės ištekliais.

Toliau nurodytose procedūrose paaiškinama, kaip savo įmonėje nustatyti darbuotoją kaip projekto išteklių ir kaip nustatyti vidinį įmonės projekto išteklių.

### <a name="set-up-a-worker-as-a-project-resource"></a>Darbuotojo nustatymas projekto ištekliumi

1. Puslapio **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotoją, kurį pridedate kaip projekto išteklių, ir atidarykite darbuotojo įrašą.
2. Veiksmų srityje pasirinkite **Projektas** &gt; **Sąranka** &gt; **Projekto sąranka**.
3. Pasirinkite kalendorių ir uždarykite puslapį.

Kaip išankstinio priskyrimo tipą taip pat galite nurodyti numatytuosius ištekliaus projektus. Išankstiniai priskyrimai gali būti naudojami, kai išteklių vadovas ar projekto vadovas iš anksto žino, su kuriais projektais dirbs išteklius. Išankstiniai priskyrimai taip pat gali būti paremti projekto rėmėjo ar kliento prašymu. Norėdami iš anskto priskirti projektą, puslapyje **Priskirti projektus**, skirtuke **Projektai**, sąraše **Likę projektai** pasirinkite atitinkamą projektą.

### <a name="set-up-an-intercompany-resource"></a>Vidinių įmonės išteklių nustatymas

Kai nustatote darbuotoją kaip vidinį įmonės išteklių, turite užbaigti sąranką tiek skolinančioje įmonėje, tiek besiskolinančioje įmonėje.

**Skolinančioje įmonėje**

1. Jei naudojate „Finance“, patikrinkite, ar pasirinkta skolinanti įmonė, o po to atlikite ankstesniame skyriuje nurodytą procedūrą „Darbuotojo nustatymas projekto ištekliumi“.
2. Puslapyje **Įmonės vidaus apskaita** pasirinkite **Naujas**.
3. Lauke **Juridinio subjekto ID** pasirinkite skolinančią įmonę. Atitinkamai užpildykite likusius laukus ir pasirinkite **Įrašyti**.
4. Puslapyje **Perkėlimo kaina** pasirinkite **Naujas**.
5. Lauke **Besiskolinantis juridinis subjektas** pasirinkite atitinkamą įmonę.
6. Norėdami besiskolinančiai įmonei paskolinti tik tą išteklių, kurį sukūrėte šio skyriaus pradžioje, lauke **Išteklius** pasirinkite sukurto ištekliaus pavadinimą. Norėdami, kad besiskolinančiai įmonei būtų prieinami visi ištekliai, lauką **Išteklius** palikite tuščią.
7. Puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Vidinė įmonė** parinktį **Įjungti vidinės įmonės išteklių planavimą ir tabelius** nustatykite kaip **Taip**.

**Besiskolinančioje įmonėje**

- Puslapyje **Išteklių sąrašas**, ieškos filtre įveskite sukurto skolinančiai įmonei skirto ištekliaus pavadinimą, kad patikrintumėte, ar pavadinimas įtrauktas į besiskolinančiai įmonei skirtą išteklių sąrašą.

## <a name="manage-resource-competencies"></a>Išteklių kompetencijų valdymas
Išteklių kompetencijos yra esminė išteklių valdymo dalis. Kompetencijas galima naudoti kaip atskaitos tašką nustatant išteklius, kurie turi tinkamą įgūdžių, išsilavinimo, sertifikatų ir projektų patirties balansą. Šią informaciją reikėtų nustatyti kiekvienam ištekliui ir ją reikėtų reguliariai atnaujinti. Tokiu būdu, kai, priskiriant projekto išteklius, suderinamos konkrečios išteklių kompetencijos, galite maksimizuoti pajėgumus.

[![Įgūdžių, sertifikatų, išsilavinimo ir projektų patirties pavyzdžiai](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Tolesnėmis procedūromis paaiškinama, kaip nustatyti kai kurias ištekliaus kompetencijas.

Norėdami nustatyti darbuotojo kompetencijas, galite naudoti arba srities Personalas sąrašo puslapį **Darbuotojai**, arba srities Projektų valdymas ir apskaita sąrašo puslapį **Ištekliai**. Tolesnėse procedūrose naudojamas srities Personalas sąrašo puslapis **Darbuotojai**.

### <a name="set-up-competencies-certificates"></a>Kompetencijų nustatymas: sertifikatai

1. Sąrašo puslapyje **Darbuotojai** pasirinkite darbuotojo, kurio sertifikatų informaciją norite pridėti, eilutę.
2. Veiksmų srityje, skirtuke **Darbuotojas**, grupėje **Kompetencijos** pasirinkite **Sertifikatai**.
3. Pasirinkite **Naujas**, tada lauke **Sertifikato tipas** pasirinkite **PMP**.
4. Lauke **Pradžios data** pasirinkite **2015-10-01**, tada – **Įrašyti**.

### <a name="set-up-competencies-skills"></a>Kompetencijų nustatymas: įgūdžiai

1. Sąrašo puslapyje **Darbuotojai** įsitikinkite, kad vis dar pasirinktas darbuotojas, kurį naudojote ankstesnėje procedūroje. Tada veiksmų srityje, skirtuke **Darbuotojas**, grupėje **Kompetencijos** pasirinkite **Įgūdžiai**.
2. Pasirinkite **Naujas**.
3. Lauke **Įgūdis** pasirinkite **Projektų valdymas**.
4. Lauke **Lygis** pasirinkite **5, ekspert.**.
5. Lauke **Lygio data** pasirinkite **2014-01-14**.
6. Lauke **Darbo patirties metai** įveskite **10**.
7. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-a-new-project"></a>Kurti naują projektą
1. Puslapyje **Projektų valdymas** pasirinkite **Naujas projektas** ir įveskite tolesnes reikšmes.

    - **Projekto tipas:** Laiko ir medžiagų.
    - **Projekto pavadinimas:** XYZ atnaujinimas, 2 etapas.
    - **Projekto grupė:** TM\_WIP
    - **Projekto sutarties ID:** 00000002.

2. Pasirinkite **Kurti projektą**.

### <a name="assign-a-resource-to-a-project"></a>Ištekliaus priskyrimas projektui

1. Puslapyje **Darbuotojai**, sąraše **Darbuotojai** pasirinkite darbuotojo, kurio kompetencijas nustatėte anksčiau, įrašą ir jį atidarykite.
2. Veiksmų srityje, skirtuke **Projektas**, grupėje **Nustatymas** pasirinkite **Priskirti projektus**.
3. Puslapio **Išteklių tikrinimo projekto priskyrimai** skirtuko **Projektai** lauke **Įtraukti projektą į pasirinktus projektus** taikykite filtrą projektui **XYZ atnaujinimas, 2 etapas**.
4. Srityje **Likę projektai** pasirinkite projektą ir, pasirinkdami rodyklės mygtuką, jį įtraukite į sritį **Pasirinkti projektai**.

Taip pat galite pagal poreikį ištekliui priskirti kategorijų. Kategorijos tipas gali būti **Išlaidos** arba **Įplaukos**. Kategorijos tipą nustato jūsų organizacija. Jei ištekliui kategorijų nepriskirta, „Finance“ suranda numatytąją išlaidų ir įplaukų valandos kainų kategoriją.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekto išteklių ir vaidmenų charakteristikų nustatymas

Naudodamas projektų išteklių funkcijas projekto vadovas gali kurti reikiamus projekto vaidmenis. Vaidmenys gali būti naudojami, jei rezervuojant išteklius vis dar nežinomi patvirtinti ištekliai. Vaidmenis galima laikinai rezervuoti kaip planuotus išteklius, kad būtų galima vykdyti kitus projekto planavimo etapus.

[![Vaidmens pavyzdys](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarijus:** „Contoso‟ buvo pasamdyta atlikti laiko ir medžiagų projektui su patvirtinta chartija. Jaunesnysis projektų vadovas vis dar nustatinėja projekto sritį. Išteklių vadovas šiuo metu identifikuoja konkrečius išteklius, kurie bus rezervuoti naujojo projekto darbui. Dėl projekto svarbos projekto rėmėjas kaip vieno iš vaidmenų pageidavo vaidmens Vyresnysis projektų vadovas. Išteklių vadovas turi gauti naująjį išteklių ir apibrėžti vaidmenį sistemoje – tam atvejui, jei, planuojant projektą, jaunesniajam projektų vadovui prireiktų informacijos apie išteklius.

Tolesniais veiksmais rodoma, kaip išteklių vadovas gali nustatyti Vyresniojo projektų vadovo vaidmenį ir susieti su juo išteklių charakteristikas. Vėliau vaidmenį galima naudoti ieškant turimų išteklių, kurie atitinka reikiamas išteklių kompetencijas.

1. Puslapyje **Nustatyti vaidmenis** pasirinkite **Naujas** ir įveskite tolesnes reikšmes.

    - **Vaidmens ID:** Vyresnysis projektų vadovas.
    - **Aprašas:** Vyresnysis projektų vadovas.

2. Pasirinkite **Kurti**.
3. Pasirinkite vaidmenį **Vyresnysis projektų vadovas**, tada – **Konfigūruoti charakteristikas**.
4. Lauke **Charakteristikų tipas** pasirinkite **Įgūdis**.
5. Lauke **Pasiekiamos charakteristikos** įveskite ieškotiną įgūdį.
6. Lauke **Charakteristikos tipas** pasirinkite **Sertifikatas**.
7. Lauke **Pasiekiamos charakteristikos** įveskite ieškotino sertifikato tipą.

### <a name="assign-a-project-resource-to-a-project"></a>Projekto ištekliaus priskyrimas projektui

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.
2. Skirtuke **Projekto komanda ir planavimas** pasirinkite **Įtraukti**.
3. Lauke **Vaidmuo** pasirinkite **Komandos narys**.
4. Pasirinkite **Rezervuoti kalendoriuje**.
5. Puslapyje **Išteklių pasiekiamumas** pasirinkite **Rodinio parametrai**.
6. Puslapyje **Koreguoti rodinio parametrus** įveskite tolesnes reikšmes.

    - **Datų intervalo rodinio formatas:** Diena.
    - **Rodyti užimtumo aprašus:** Taip.
    - **Rodyti likusį pajėgumą:** Taip.

7. Išteklių sąraše pasirinkite išteklių.
8. Pasirinkite **Tiksliai planuoti užimtumą** ir **Visas pajėgumas**.


### <a name="assign-a-resource-to-a-default-role"></a>Ištekliaus priskyrimas numatytajam vaidmeniui

Norint padėti projektų ar išteklių vadovams, galima dar labiau detalizuoti projektui galimus rezervuoti išteklius. Numatytąjį vaidmenį galima susieti su esamu ištekliumi arba naujai gautu ištekliumi. Pavyzdžiui, kai Danielis buvo priimtas į darbą, jo patirtis ir įgūdžiai buvo tinkami verslo analitiko vaidmeniui. Išteklių vadovas priskyrė šį vaidmenį kaip numatytąjį Danielio vaidmenį. Todėl išteklių vadovas Danielį pridėjo į verslo analitikų, kurie gali dirbti su projektais, telkinį.

Rezervuodami išteklius projektų vadovai gali filtruoti vaidmenų išteklius, kurie gali dirbti su projektais. Kai panaudodami išteklius vadovai atlieka kelių kriterijų sprendimų analizę, šią informaciją jie gali naudoti kaip vieną iš kriterijų. Jie taip pat gali į filtrą įtraukti kitų išteklių charakteristikų ir ieškoti išteklių, turinčių konkrečių įgūdžių, išsilavinimą ir patirties konkrečiam projektui atlikti.

**Scenarijus:** pradėtas patvirtintas projektas ir projekto planavimo etape kaip planuoti ištekliai buvo rezervuotas vyresniojo projekto vadovo vaidmuo. Išteklių vadovas gavo išteklių užimti vyresniojo projekto vadovo vaidmeniui.

1. Puslapyje **Išteklių sąrašas** pasirinkite **Danielis Goldschmidtas**.
2. Puslapyje **Ištekliaus vaidmuo** pasirinkite **Naujas** ir įveskite tolesnes reikšmes.

    - **Įsigalioja:** įveskite dabartinę datą.
    - **Galiojimo pabaiga:** įveskite **Niekada**.
    - **Vaidmuo:** įveskite **Vyresnysis projektų vadovas**.

3. Pasirinkite **Įrašyti** ir uždarykite puslapį.
4. Skirtuke **Kompetencijos** pridėkite įgūdį **ProjektVald** ir sertifikatą **PMP**.

## <a name="set-up-role-based-pricing"></a>Vaidmenimis paremtos kainodaros nustatymas
Galima nustatyti visas vaidmenų savikainas, pardavimo kainas ir perkėlimo kainas.

1. Puslapyje **Pardavimo kaina (valanda)** pasirinkite **Naujas** ir įveskite įsigaliojimo datą.
2. Stulpelyje **Vaidmuo** pasirinkite vaidmenį.
3. Stulpelyje **Kainodara** įveskite pasirinkto išteklių vaidmens kainą.

## <a name="form-a-project-team"></a>Projekto komandos sudarymas
Norėdamas naudoti vaidmenis, kurie buvo anksčiau nustatyti projekte, projekto vadovas tuos vaidmenis turi susieti su projektu. Projektui galima priskirti kelis vaidmenis. Kad būtų išvengta painiavos, rezervavimo metu šie vaidmenys automatiškai pažymimi. Pavyzdžiui, jei projekto vadovui reikia trijų programinės įrangos inžinierių, automatiškai sugeneruojami trys programinės įrangos inžinieriaus vaidmenys, kurių žymos – **1 programinės įrangos inžinierius**, **2 programinės įrangos inžinierius** ir **3 programinės įrangos inžinierius**. Jei anksčiau buvo nustatytos vaidmenų charakteristikos, ieškant ištekliaus jos taikomos kaip filtras. Pagal poreikį galima pridėti papildomų charakteristikų ir taip dar patikslinti iešką.

Taip pat galima tinkinti rodinio parametrus, kad būtų galima geriau matyti išteklių prieinamumą. Parinktimis galima nustatyti valandos, dienos, savaitės, mėnesio, ketvirčio ir metų prieinamumo rodymą. Taip pat galima parinktis rodyti turimą ir likusį išteklių pajėgumą. Ši parinktis naudinga valdant laiką, kai vertinamas turimas veikloms skirtas laikas ar išteklių prieinamumas.

Projekto vadovas puslapyje gali pasirinkti vaidmenį ir, jei turimas reikalavimą atitinkantis išteklius, pasirinkti rezervuoti išteklių vaidmeniui užimti. Atkreipkite dėmesį, kad šiame planavimo etape išteklių rezervuoti nereikia. Kai kuriate WBS, vaidmenis galite pakeisti darbuotojams priskirtais projekto ištekliais. Jei WBS vaidmenys pakeičiami darbuotojams priskirtais ištekliais, nustatant išteklius automatiškai atnaujinamas projekto komandos sąrašas ir planavimas.

[![Projekto komandos sąrašas tiek su vaidmenimis, tiek su faktiniais ištekliais](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projekto vadovas turi įvairių projekto ištekliaus rezervavimo parinkčių, pvz., **Likęs pajėgumas**, **Visas pajėgumas**, **Pajėgumo procentas** ir **Nurodyti valandas**. Pakitus išteklių priskyrimams, šias rezervavimo parinktis galima bet kuriuo metu atšaukti. Palaikomi du tolesni rezervavimo tipai.

- **Tikslus rezervavimas** – išteklių rezervavimas buvo patvirtintas įtraukimo darbui nurodytą trukmę.
- **Apytikslis rezervavimas** – išteklių rezervavimas buvo preliminariai nustatytas įtraukimo darbui nurodytą trukmę.

Tolesne procedūra paaiškinama, kaip sukurti projekto komandą.

### <a name="create-a-project-team"></a>Projekto komandos kūrimas

1. Sąrašo puslapyje **Visi projektai** pasirinkite projektą ir pasirinkite **Redaguoti**.
2. Skirtuke **Projekto komanda ir planavimas**, lauke **Grafiko pabaigos data** įveskite grafiko pradžios datą ir pridėkite vieną mėnesį. Pavyzdžiui, jei grafiko pradžios data yra 2017 m. birželio 24 d. (2017-06-24), įveskite **2017-07-24**.
3. Pasirinkite **Įtraukti**.
4. Srityje **Į projektą įtraukti vaidmenų**, lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
5. Pasirinkite **Būtinosios kompetencijos**.
6. Puslapyje **Pasirinkti charakteristikas** pagal numatytuosius parametrus pasirenkamos anksčiau jūsų nustatytos vyresniojo projektų vadovo vaidmens charakteristikos. Pasirinkite **Gerai**.
7. Puslapyje **Į projektą įtraukti vaidmenų**, lauke **Išteklių skaičius** įveskite **1**.
8. Lauke **Išteklius** peržvalga rodo visus išteklius, turinčius reikiamas kompetencijas. Pasirinkite **Danielis Goldschmidtas**, tada – **Kurti**.
9. Puslapyje **Projektas** pasirinkite **Įtraukti**.
10. Srityje **Į projektą įtraukti vaidmenų**, lauke **Vaidmuo** pasirinkite **Komandos narys**. Lauke **Išteklių skaičius** įveskite **5**.
11. Pasirinkite **Kurti**.
12. Puslapyje **Projektai** pasirinkite **Panaudoti išteklių**.

## <a name="resource-capacity-synchronization"></a>Išteklių pajėgumų sinchronizavimas
Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija būtų perduodama bei naudojama ir planuojant projekto išteklius. Jei kalendorius pakinta, procesais pagal poreikį atnaujinamas projekto išteklių planavimas. Šie procesai taip pat padeda gerinti našumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto. Todėl greičiau atnaujinama išteklių planavimo informacija. Rekomenduojame procesus planuoti kaip paketą, o ne po vieną. Kitu atveju atsiranda rizika, kad kažkas pamirš informacijos paskutinį sinchronizavimą apimančias datas. Jei apimančiosios datos nenaudojamos, sinchronizuojant datas gali atsirasti tarpų.

![Kalendoriaus sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sinchronizuoti išteklių pajėgumų sumavimus

Sinchronizavimo procesas skirtas sinchronizuoti visai išteklių kalendoriaus informacijai. Ši informacija apima pagrindinio kalendoriaus informaciją apie visus projekto išteklių kalendoriaus pajėgumo lentelės keitimus. Jei į projektą įtraukiama naujų išteklių, sinchronizavimas padeda užtikrinti, kad būtų prieinama atnaujinta kalendoriaus informacija. Šį sinchronizavimą galima atlikti bet kuriuo metu.

Rekomenduojame naudoti paketą. Parinktys galimos sinchronizuojant pajėgumų rezervavimus.

1. Pasirinkite **Projektų valdymas ir apskaita** &gt; **Laikotarpio** &gt; **Pajėgumo sinchronizavimas** &gt; **Sinchronizuoti išteklių pajėgumų sumavimus**.
2. Nustatykite tolesnėje lentelėje nurodytas parinktis.

    | Parinktis      | aprašymas |
    |-------------|-------------|
    | Laikotarpio kodas | Pasirenkama: pasirinkite didžiosios knygos datų intervalo kodą, kad nustatytumėte išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios ir pabaigos datas. |
    | Pradžios data  | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios datą. |
    | Pabaigos data    | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pabaigos datą. |

[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Vaidmenų WBS šablonuose nustatymas
Projektų vadovai gali nustatyti WBS šablonus, kuriuos jie gali taikyti kurdami naujų projektų WBS. Kurdami šabloną projektų vadovai gali įtraukti vaidmenų. Naudodami tolesnę procedūrą galite WBS šablonui priskirti vaidmenį. 

1. Pasirinkite **Projektų valdymas ir apskaita** &gt; **Nustatymas** &gt; **Projektai** &gt; **Darbo paskirstymo struktūrų šablonai**.
2. Prie pasirinkto WBS šablono pasirinkite **Išsami informacija**.
3. Sąraše pasirinkite užduotį, tada lauke **Vaidmuo** pasirinkite užduočiai priskirtiną vaidmenį.

### <a name="work-with-a-wbs"></a>Darbas su WBS

Galite sukurti naują WBS arba WBS galite nukopijuoti iš esamo WBS šablono. Priskirdamas vaidmenis naujoms WBS užduotims projekto vadovas gali lengvai valdyti išteklius. Vaidmenis galima pakeisti gavus išteklių arba identifikavus patvirtintą išteklių darbui su užduotimi. Toks lankstumas projektų vadovams leidžia atlikti tolesnes užduotis.

- Identifikuoti, kiek išteklių reikia WBS darbo paketams.
- Įvertinti projekto išlaidas.
- Nustatyti preliminarų biudžetą.
- Pagal vaidmenis ir išteklius įvertinti veiklos trukmę.
- Pagal turimą projektų informaciją kurti projektų valdymo planų.

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
<td>Naudodami su užduotimi susietus vaidmenis automatiškai įtraukite suplanuotų išteklių. „Finance‟ suplanuotų išteklių siūlo automatiškai, naudodama kelių kriterijų sprendimų analizę pagal vaidmenis. Kai nustatyti WBS užduočių vaidmenys bei pastangos (valandos) ir atlaisvinta struktūra, pasirinkite <strong>Automatiškai generuoti komandą</strong>. Reikiamas suplanuotų išteklių skaičius įtraukiamas į WBS ir skirtuką <strong>Projekto komanda ir planavimas</strong>.</td>
</tr>
<tr class="odd">
<td>Išteklius (išplečiamasis sąrašas)</td>
<td>Puslapyje <strong>Paleisti išteklių priskyrimą</strong> pagal nurodytą trukmę galite pasirinkti, ar išteklius planuoti tiksliai, ar apytiksliai. Galite koreguoti rodinio parametrus ir matyti bei nustatyti išteklių veiklų trukmę. Naudodami tolesnes parinktis, išteklius galite pasirinkti ir priskirti darbo paketų lygiu.
<ul>
<li><strong>Priimti</strong> – patvirtinti ištekliaus, priskirto užduočiai, keitimus.</li>
<li><strong>Atšaukti</strong> – atšaukti ištekliaus, priskirto užduočiai, keitimus.</li>
<li><strong>Priskirti automatiškai</strong> – automatiškai parenkamas ir pasirinktai užduočiai priskiriamas galimas personalo išteklius su atitinkamu vaidmeniu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.
2. Pasirinkite **Planas** &gt; **Veiklos** &gt; **Darbo paskirstymo struktūra**.
3. Pasirinkdami **Naujas** į WBS įtraukite tolesnes pirmo lygio veiklas.

    - Inicijavimas
    - Planavimas
    - Vykdoma
    - Stebėjimas ir valdymas
    - Artimas

4. Kaip parodyta tolesnėje iliustracijoje, nustatykite datas ir pastangas (valandas).

    [![Datų ir pastangų nustatymas](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pasirinkite užduoties eilutę **Inicijavimas**, tada lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
6. Pasirinkite **Publikuoti**.
7. Toje pačioje eilutėje, lauke **Išteklius** pasirinkite **Danielis Goldschmidtas**, o tada – **Patvirtinti**.
8. Pasirinkite užduoties eilutę **Planavimas**, tada lauke **Vaidmuo** pasirinkite **Verslo analitikas**.
9. Pasirinkite **Publikuoti**, tada – **Automatiškai generuoti komandą**.
10. Pasirodžiusiame pranešimo lange pasirinkite **Taip**.
11. Įsitikinkite, ar lauko **Išteklius** reikšmė yra **1 verslo analitikas**.
12. Atidarykite ištekliaus **1 verslo analitikas** peržvalgą ir pasirinkite **Paleisti išteklių priskyrimus**. Tada užduočiai parinkite darbuotoją.
13. Pasirinkite **Apytiksliai priskirti** &gt; **Visas pajėgumas**.

    > [!NOTE] 
    > Įspėjimo, kad nurodytas išteklius dabar yra 2, negaunate, nes išteklių skaičius lieka 1.

14. Puslapyje **Darbo paskirstymo struktūra** patikrinkite WBS išteklių priskyrimą ir pasirinkite **Įrašyti**.

## <a name="resource-fulfillment-for-planned-resources"></a>Suplanuotų išteklių panaudojimas
Projekto vadovas gali planuoti reikiamus projekto išteklių vaidmenis. Šiuos suplanuotus išteklius išteklių vadovas matys kaip užklausas puslapyje **Išteklių panaudojimas** ir jis gali priskirti faktinius išteklius.

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.
2. Pasirinkite **Projektas**, tada – **Redaguoti**.
3. Skirtuke **Projekto komanda ir planavimas** pasirinkite **Įtraukti**.
4. Dialogo lange **Įtraukti vaidmenis** pasirinkite vaidmenį **Programinės įrangos kūrėjas**.
5. Pasirinkite **Kurti** ir uždarykite projekto puslapį.
6. Puslapyje **Išteklių panaudojimas** prie projekto **XYZ atnaujinimas, 2 etapas** pasirinkite **1 programinės įrangos kūrėjas 1**.
7. Pasirinkite darbuotoją, tada – **Priskirti**.
8. Patikrinkite, ar pašalinta projekto **XYZ atnaujinimas, 2 etapas** eilutė **1 programinės įrangos kūrėjas**.
9. Skirtuke **Projekto komanda ir planavimas** prie projekto **XYZ atnaujinimas, 2 etapas** patikrinkite, ar darbuotojas, kurį pasirinkote atlikdami ankstesnį veiksmą, įtrauktas kaip **Programinės įrangos kūrėjas**.

## <a name="requests-for-project-resources"></a>Projektų išteklių užklausos
Projektų išteklių planavimo funkcija gali naudotis tik išteklių vadovai, norėdami platinti personalo išteklius įsipareigojimuose arba projektuose. Norėdami įjungti šią funkciją, atlikite toliau nurodytas užduotis arba patvirtinkite, kad jos atliktos.

- Nustatyti numeracijas.
- Nustatyti projektų valdymo ir apskaitos darbo eigas.
- Įjunkite išteklių užklausų darbo eigas.

Atlikę pirmiau nurodytas užduotis, galite atlikti reikiamas kitas užduotis.

- Sukurkite išteklių užklausą iš apytiksliai suplanuotų personalo išteklių.
- Stebėti išteklių užklausas.
- Vykdyti išteklių užklausas.
- Pateikti personalo ištekliaus iš WBS užklausą.
- Užregistruokite išteklius projektui nepateikdami personalo išteklių užklausos.

## <a name="monitor-project-teams"></a>Projekto komandų stebėjimas
1. Puslapyje **Visi projektai** pasirinkite projekto **XYZ atnaujinimas, 2 etapas** saitą **Projekto ID**.
2. „FastTab‟ **Projekto komanda ir planavimas** patikrinkite, ar išvardyti projekto ištekliai yra teisingi.
