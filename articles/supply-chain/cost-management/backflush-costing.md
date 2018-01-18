---
title: "Įkainojimas atvirkštine tvarka"
description: "Šioje temoje pristatoma įkainojimo atvirkštine tvarka koncepcija, naudojama „Lean manufacturing”."
author: cvocph
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9fe717752da4c697cf0d896c0d40832330f0d118
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="backflush-costing"></a>Įkainojimas atvirkštine tvarka

[!include[banner](../includes/banner.md)]


Šioje temoje pristatoma įkainojimo atvirkštine tvarka koncepcija, naudojama „Lean manufacturing”. 

„Lean manufacturing” įkainojimas gamybos eigai leidžia naudoti išlaidų kaupimo metodą, vadinamą įkainojimu atvirkštine tvarka. Taikant įkainojimo atvirkštine tvarka metodą suvartojamos tiesioginės medžiagos yra kaupiamos gamybos eigos nebaigtos gamybos (NG) išlaidų sąskaitoje. Naudojama standartinių išlaidų atsargų modelių grupė. Iš gamybos eigos gauti produktai išskaičiuojami iš NG pagal jų standartines išlaidas. Pagrindinis skirtumas tarp įkainojimo atvirkštine tvarka ir standartinių išlaidų yra tas, kad taikant įkainojimą atvirkštine tvarka neapskaičiuojami „kanban” arba galutinio produkto nuokrypiai. Šiuo atveju nuokrypiai apskaičiuojami pagal gamybos eigą per tam tikrą laikotarpį. Remiantis šiuo metodu pristatoma tiksli „Lean“ sąvoka medžiagų suvartojimo ataskaitoms pateikti. Paimtiems medžiagų kiekiams skirta ataskaita „kanban” ar gamybos užsakyme nepateikiama. Šiuo atveju visi paketai arba sandėliavimo vienetai suskirstomi į gamybos eigos etapus. Po to, kai paketai arba sandėliavimo vienetai užregistruojami kaip tušti, jie deklaruojami kaip suvartoti. Galima naudoti papildomą suvartojimą atsižvelgiant į [gamybos eigos konfigūraciją](../production-control/lean-manufacturing-modeling-lean-organization.md). Prieš naudojant papildomą suvartojimą organizacijos turi sudaryti sąlygas, kad gamybos eigos NG neliktų medžiagų. Naudojant periodinį įkainojimą atvirkštine tvarka, galiojanti NG vertė nustatoma į laikotarpio pabaigą. Šis nustatymas pagrįstas „kanban“ sandėliavimo vienetais ir „kanban“ užduoties būsena. Galiojančių ir faktinių NG verčių pagal išlaidų grupę ir prekę nuokrypiai apskaitomi bei rodomi kaip nuokrypiai.

## <a name="configuring-backflush-costing"></a>Įkainojimo atvirkštine tvarka konfigūravimas
Norėdami įgalinti įkainojimą, turite atlikti toliau nurodytą sąranką:

-   **Nustatyti gamybos grupės ir gamybos eigos NG sąskaitas.** Gamybos eigos NG sąskaitos nurodomos gamybos grupėje. Gamybos eigos įkainojimo atvirkštine tvarka nuokrypiai apskaičiuojami kaip NG vertės skirtumas prieš pradedant ir užbaigus vykdyti kiekvienos gamybos eigos įkainojimą atvirkštine tvarka. Todėl kiekvienai gamybos eigai rekomenduojame sukurti NG sąskaitą.
-   **Priskirti išlaidų kategoriją išteklių grupei.** Išlaidų kategoriją turite priskirti darbo elemento vykdymo laiko kategorijai. Norėdami nustatyti nuokrypius pagal veiklą, kiekvienam darbo elementui turite sukurti išlaidų kategoriją. Sąrankos ir kiekio išlaidų kategorijos į „lean manufacturing“ įkainojimą neįtraukiamos. Išteklių grupės NG sąskaitų taikant įkainojimą atvirkštine tvarka nepaisoma. Subrangos veiklos paslaugoms išlaidų kategorijos nurodyti nereikia. Šiuo atveju naudojama aktyviai paslaugai priskirta išlaidų grupė.
-   **Priskirti išlaidų grupes.** Norėdami įgalinti gamybos eigos išlaidų įnašo segmentavimą, išlaidų grupes turite priskirti pagal išlaidų grupės tipą:
    -   **Tiesioginių medžiagų išlaidų grupė** – tiesioginėms medžiagoms reikalinga išlaidų grupė, kuria identifikuojama įkainoti skirta medžiagų kategorija. Šioje išlaidų grupėje įgalinamas sujungtas išlaidų rodinys, NG ir tiesioginių medžiagų nuokrypiai.
    -   **Tiesioginės gamybos išlaidų grupė** – tiesioginės gamybos išlaidų grupėje fiksuojamas veiklos išteklių tiesioginių išlaidų įnašas į gamybos eigą. Šioje išlaidų grupėje įgalinamas sujungtas išlaidų rodinys, NG ir tiesioginės gamybos išlaidų nuokrypiai.
    -   **Netiesioginių išlaidų grupė** – netiesioginių išlaidų grupė reikalinga norint apskaičiuoti netiesioginių išlaidų įnašą į gamybos eigą. Šioje išlaidų grupėje įgalinamas sujungtas išlaidų rodinys, NG ir netiesioginių išlaidų nuokrypiai.
    -   **Tiesioginių užsakomųjų paslaugų išlaidų grupė** – paslaugų išlaidų grupėje įgalinamas sujungtas priskirtų išlaidų rodinys ir NG, taip pat nustatomi subrangos paslaugų išlaidų nuokrypiai.
    -   **Galutinių produktų išlaidų grupė** – galutiniams produktams reikalinga išlaidų grupė, kuria identifikuojama įkainoti skirta produktų kategorija. Šioje išlaidų grupėje įgalinamas sujungtas išlaidų rodinys, NG ir produktų kategorijos nuokrypiai. Standartinės produktų išlaidos apskaičiuojamos naudojant išlaidų skaičiavimą pagal komplektavimo specifikaciją (KS), taip pat pagal gamybos eigos ir „kanban” taisykles arba maršrutą.

### <a name="costing-sheet"></a>Įkainojimo lapas

Naudojant įkainojimo lapą modeliuojama įmonės išlaidų struktūra, kuriama pagal išlaidų grupes išlaidoms klasifikuoti. Įkainojimo lapas gali būti įvairių formų. Jame rodoma išlaidų informacija pagal įkainojimo lapui sukurtą struktūrą. Įkainojimo lape taip pat galima apibrėžti netiesioginėms išlaidoms apskaičiuoti naudojamą formulę. Skaičiavimo formulė gali būti pagrįsta kiekiu, svoriu, tūriu arba verte.

-   **Nustatyti įkainojimo versiją.** Įkainojimo versijoje įmonė nustato, kaip tvarkyti išlaidas. Įkainojimo versiją gali sudaryti standartinių išlaidų įrašų rinkinys arba suplanuotų išlaidų įrašų rinkinys atsižvelgiant į įkainojimo tipą, kuris priskirtas įkainojimo versijai. Įkainojimo versija, naudojama norint įkainoti „lean manufacturing“, turi būti pagrįsta standartinėmis išlaidomis.
-   **Patvirtintiems produktams priskirkite atsargų modelio grupę.** Visus su gamybos eiga susijusius produktus būtina priskirti atsargų modelio grupei, kuri naudoja **Standartinių išlaidų** atsargų modelio grupę. Standartinės išlaidos tvarkomos pagal vietą ir aktyvinimo datą. Naudojant bendruosius produktus galima pasirinkti atsargų modelio grupę, jeigu išlaidos tvarkomos pagal produkto variantą arba bendrąjį produktą.
-   **Iš esmės, subrangos paslaugos yra neinventorizuotos.** Atsargų modelio grupės naudojant subrangos veiklas nėra. Norėdami teisingai įkainoti subrangos veiklą, turite įsitikinti, kad aptarnavimo veikla priklauso atsargų modelio grupei, kurioje atsargų strategija nustatyta į **Laikomas produktas = netinkamas**.

Išeigos produktų atveju skaičiuojant išlaidas pagal gamybos eigą, reikia, kad būtų tvarkomos su subrangos veiklomis susijusių paslaugų standartinės išlaidos. Paslaugoms priskirta išlaidų grupė naudojama siekiant nustatyti subrangos veiklos išlaidų nuokrypius.

## <a name="cost-calculation-for-lean-manufacturing"></a>„Lean manufacturing” išlaidų skaičiavimas
Iš gamybos eigos tiekiamų produktų atveju KS skaičiavimas turi būti pagrįstas maršruto versija arba gamybos eiga. Naudojant KS skaičiavimą apskaičiuojamos produkto išlaidos ir susijusių išteklių bei medžiagų, kurių reikia norint kurti produktą, paskirstymas. Atskaitymas iš gamybos eigos NG sąskaitos atliekamas naudojant produkto paskirstymą pagal prekę ir išlaidų grupę.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Gamybos eiga pagrįstas skaičiavimas

„Lean manufacturing”, skirtas „Microsoft Dynamics 365 for Finance and Operations”, su maršrutais nesusijęs. Iš gamybos eigos tiekiamų produktų išlaidų skaičiavimas gali būti pagrįstas pačia gamybos eiga. Kad galėtumėte apskaičiuoti, reikia sukurti iš gamybos eigos tiekiamo produkto „kanban” taisyklę. Jei produktą galima tiekti iš kelių gamybos eigų toje pačioje nuo skaičiavimo datos vietoje, pasirinkite KS skaičiavimo gamybos eigą. Puslapyje **Numatytoji gamybos eiga** galite konfigūruoti numatytąją kiekvienos prekės gamybos eigą. Jei nustatytos kelios to paties produkto, esančio toje pačioje nuo skaičiavimo datos veikiančioje gamybos eigoje, „kanban” taisyklės, skaičiuojant pasirenkama aktyvi pirmoji „kanban“ taisyklė.

### <a name="calculation-that-is-based-on-the-route"></a>Maršrutu pagrįstas skaičiavimas

Maršrutu pagrįstas skaičiavimas yra kaip skaičiavimas, pagrįstas gamybos eiga. Tačiau maršrutu pagrįsto skaičiavimo atveju nenaudojama įkainojimui skirta „Lean manufacturing” funkcija. Maršrute reikia naudoti išteklių grupių išteklių reikalavimus. Siekiant išvengti sisteminių nuokrypių, jame taip pat reikia naudoti tuos pačius darbo elementus ar bent jau tas pačias išlaidų kategorijas. Taip pat turėtumėte vengti sąrankos ir kiekio išlaidų kategorijų. Jos nepadės detaliau apskaičiuoti išlaidų paskirstymo nei „Lean manufacturing” išlaidų nurašymas. Norėdami nustatyti, kurią parinktį (gamybos eigos ar maršruto) naudodami skaičiuosite išlaidas, atsižvelkite į išlaidų paskirstymo rezultatus. Dabar teikiamoje versijoje rodoma mažiau nuokrypių, todėl tai yra geresnė pasirinktis. „Lean manufacturing” aplinkoje, kurioje produktas tiekiamas naudojant vieną gamybos eigą ir vieną „kanban” taisyklę, gamybos eiga pagrįstas skaičiavimas greičiausiai yra tikslesnis. Naudojant produktą, kurį toje pačioje vietoje gali pateikti „Lean manufacturing” ir gamybos užsakymai arba kuriame gali būti kelios gamybos eigos ar kelios tos pačios eigos „kanban“ taisyklės, skaičiavimas gali būti tikslesnis, jeigu jis pagrįstas maršruto versija, specialiai skirta išlaidoms, o ne gamybos užsakymams skaičiuoti. Norint apskaičiuoti produktus, susijusius su subranga, reikia naudoti gamybos eigos skaičiavimą. „Microsoft Dynamics 365 for Finance and Operations” išlaidų modeliuose, skirtuose gamybos užsakymų subrangai ir „Lean manufacturing” subrangai, naudojami du skirtingi metodai. „Lean manufacturing” yra naujas išlaidų grupės tipas **Tiesioginės užsakomosios paslaugos**, skirtas subrangos paslaugų išlaidoms skaičiuoti.

## <a name="material-consumption"></a>Medžiagų suvartojimas
NG suvartojus medžiagas iš atsargų, medžiagų išlaidos įtraukiamos į NG išlaidų grupės faktines standartines išlaidas. Ši operacija vyksta tokiomis sąlygomis:

-   „Kanban” išdavimai registruojami į „kanban” paėmimo eilutes, kad būtų atnaujintos atsargos.
-   Perkėlimo užduotys baigtos, kad būtų atnaujintos atsargos paimant, bet ne gaunant (medžiagų perkėlimas iš atsargų į NG).

## <a name="receiving-products-from-the-production-flow"></a>Produktų gavimas iš gamybos eigos
Produktai gaunami iš gamybos eigos tokiomis sąlygomis:

-   Proceso užduotys baigtos, kad **Atnaujinti atsargas gaunant** būtų nustatyta į **Taip**.
-   Perkėlimo užduotys baigtos, kad būtų atnaujintos atsargos gaunant, tačiau **Nustatyta atnaujinti atsargas paimant** į **Ne** (perkelti iš NG į atsargas). Naudodami šią parinktį galite gauti bet kurių produktų iš gamybos eigos neatsižvelgiant į KS ir maršruto konfigūraciją. Vykstant procesui tiesiog sekami faktiniai srautai. Šią parinktį geriausia naudoti šalutiniams ir sudėtiniams produktams gauti arba nurašyti iš gamybos eigos ir atitinkamai gamybos eigos NG išlaidų balansui taisyti.

Iš gamybos eigos gauti produktai išskaičiuojami iš NG.

## <a name="products-in-wip"></a>NG produktai
Norėdami valdyti medžiagas, neužbaigtus ir pagamintus produktus, kurie yra NG dalis, „Microsoft Dynamics 365 for Finance and Operations” „Lean manufacturing” NG modelyje galite naudoti „kanban” sandėliavimo vieneto būseną.

-   **Priskirta** – „kanban” galima suvartoti medžiagas, apskaitomas NG.
-   **Gauta** – jei „kanban“ nurodoma paskutinė veikla, kur **Atnaujinti atsargas gaunant** nustatyta į **Ne**, tai pateikiamas visas produkto sandėliavimo vienetas arba neužbaigtas produktas, kuris neužregistruotas į atsargas.

Įsidėmėkite, kad NG medžiagos turimų atsargų apžvalgose nematomos. Tačiau jos matomos „kanban“ kiekio apžvalgose.

## <a name="consuming-products-in-wip"></a>NG produktų suvartojimas
NG produktai suvartojami, kai ištuštinami atitinkami „kanban“ sandėliavimo vienetai. Tuščias „kanban” signalas nesukuria aktyvios įkainojimo operacijos, tačiau pradės veikti vykdant kitą įkainojimą atvirkštine tvarka. Ištuštinti „kanban” sandėliavimo vienetai daugiau neapskaitomi kaip turimos atsargos ir todėl apskaičiuojami kaip tuo laikotarpiu suvartoti.

### <a name="automatic-empty-registration"></a>Automatinė tuščia registracija

Suplanuotus arba įvykių „kanban” galima nustatyti „kanban” taisyklėje kaip automatinę tuščią registraciją:

-   **Gavus sandėliavimo vienetus** – pagal numatytuosius suplanuotų „kanban” nustatymus baigus paskutinę „kanban” užduotį medžiagos paskelbiamos suvartotomis. Esant fiksuoto kiekio „kanban“, ši parinktis rekomenduojama tik vienos talpyklos „kanban”, kadangi kortelė grąžinama į poreikio šaltinį, kai tik galutinėje paskirties vietoje gaunamas „kanban”.
-   **Užregistravus šaltinio reikalavimą** – šią parinktį galima naudoti tik įvykio „kanban”, kuri yra numatytoji jų parinktis. NG atveju ši parinktis naudinga, jei NG švari, nes NG komponentų „kanban” ištuštinami automatiškai ir todėl paruošus pirminį „kanban” suvartojami iš NG.

Taigi „kanban” sandėliavimo vienetai gali būti priskirti (= vykdomi), gauti (= užpildyti) arba ištuštinti. Dalinio ištuštinimo nėra. Todėl norint įgalinti tikslią suvartojimo registraciją svarbu apriboti „kanban” produktų kiekius taip, kad jų būtų mažiau nei tuo laikotarpiu suvartota. Produktai, kurie perkeliami į darbo laiko paslaugą dideliais paketais, apimančiais reikiamas dienas ar savaites, neturėtų būti suvartojami NG. Todėl šiuos produktus reikia saugoti kaip atsargas.

## <a name="backflush-costing"></a>Įkainojimas atvirkštine tvarka
Norėdami periodiškai įvertinti NG ir sukurti laikotarpio pabaigos būseną, pagal kurią skaičiuojami medžiagų, darbo ir netiesioginių išlaidų nuokrypiai, turėtumėte vykdyti įkainojimą atvirkštine tvarka. Apskaičiuoti nuokrypiai registruojami nuokrypių sąskaitose. Vykdant įkainojimą atvirkštine tvarka visos juridinio subjekto gamybos eigos naudojamos tam pačiam paketui paleisti. Kai įkainojimas atvirkštine tvarka vykdomas kaip paketas, apdorojimas gali būti kelių gijų gamybos eigos. Atvirkštinės tvarkos laikotarpis apibrėžiamas pabaigos data. Data, kada buvo vykdomas įkainojimo atvirkštine tvarka skaičiavimas, registruoti naujų operacijų negalima. Dabartinės datos įkainojimo atvirkštine tvarka vykdyti iš anksto (dieną prieš tai) negalima. Atliekami toliau nurodyti įkainojimo atvirkštine tvarka veiksmai.

1.  Nepanaudotus gamybos eigos kiekius nustatykite iki laikotarpio pabaigos datos. Užbaigę vykdyti įkainojimą atvirkštine tvarka, nepanaudotus kiekius įkainojimo vykdymo data galite peržiūrėti dialogo lange **Nepanaudoti kiekiai**.
2.  Apskaičiuokite gamybos eigos grynąjį realizuotą sunaudojimą tuo laikotarpiu.
3.  Išvalykite NG iš realizuoto išteklių suvartojimo ir produktų.
4.  Apskaičiuokite to laikotarpio gamybos nuokrypius nuo standartinių išlaidų. **Suvartoti to laikotarpio komponentai:**
    -   Finansiškai atnaujinkite tuo laikotarpiu gamybos eigos suvartotų medžiagų grynuosius realizuotus kiekius. Sistemoje apdorojamas „pirmasis į, pirmasis iš“ (FIFO) atskirų atsargų operacijų užsakymas taip, kad gamybos eigos faktiškai atnaujintos operacijos būtų finansiškai atnaujinamos, kol bus pasiekti to laikotarpio grynieji realizuoti kiekiai.
    -   Operacijos finansiškai išskaidomos tiksliems suvartojimo kiekiams susieti.
    -   NG gamybos eigos nepanaudoti kiekiai lieka faktiškai atnaujintos būsenos.

    **Baigti to laikotarpio gamybos kiekiai:**
    -   Finansiškai atnaujinkite to laikotarpio baigtų kiekių atsargų operacijas.

    **Konvertavimo išlaidos:**
    -   Taikytinos konvertavimo išlaidų operacijos (maršruto operacijos), įrašytos tuo laikotarpiu, yra finansiškai atnaujinamos.
    -   Visos tiesioginės gamybos išlaidos yra finansiškai atnaujinamos. Visos tuo laikotarpiu atliktos „kanban” proceso užduotys yra kaupiamos.
    -   Visos tuo laikotarpiu apskaičiuotos netiesioginės suvartotų medžiagų išlaidos apskaičiuojamos ir išskaičiuojamos iš NG. Likusios netiesioginės išlaidos registruojamos kaip nuokrypis.

5.  Apskaičiuokite gamybos nuokrypius nuo standartinių išlaidų. Nuokrypis apskaičiuojamas pagal išlaidų grupę.






