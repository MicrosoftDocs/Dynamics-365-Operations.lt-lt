---
title: Esamo svorio produktų apdorojimas naudojant sandėlio valdymą
description: Šioje temoje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje atliekamas darbas.
author: perlynne
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy, TMSLoadBuildWorkbench, WHSCatchWeightTagRegistration, WHSCatchWeightTagFullDimDiscrepancies, WHSCatchWeightTagChangeWeightDropDownDialog, WHSCatchWeightLinkWorkLineTagDropDownDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 3882e40b4083f9246a03db3078cae8e18bec3c1e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808923"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Esamo svorio produktų apdorojimas naudojant sandėlio valdymą

[!include [banner](../includes/banner.md)]

## <a name="feature-exposure"></a>Funkcijos įjungimas

Norėdami naudoti sandėlio valdymą esamo svorio produktams apdoroti, turite naudoti licencijos konfigūracijos raktą, kad įjungtumėte funkciją. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**. Tada skirtuke **Konfigūracijos raktai** išplėskite **Prekyba \> Sandėlio ir transportavimo valdymas**, tada pasirinkite žymės langelį **Esamas svoris sandėlyje**.

> [!NOTE]
> Licencijos konfigūracijos raktas **Sandėlio ir transportavimo valdymas** ir licencijos konfigūracijos raktai **Apdoroti paskirstymą \> Esamas svoris** turi būti įjungti. Norėdami nustatyti esamo svorio konfigūracijos raktus, taip pat turite įjungti funkciją naudodami darbo sritį **Funkcijų valdymas**. Pagrindinė funkcija, kurią reikia įjungti, yra **Esamo svorio produktų apdorojimas naudojant sandėlio valdymą**. Dvi susijusios, bet papildomos funkcijos, kurias galbūt norėsite įjungti, yra **Esamo svorio produktų atsargų būsenos keitimai** ir **Naudoti esamas esamo svorio žymes pranešant, kad gamybos užsakymai yra baigti**.

Įjungus licencijos konfigūracijos raktą, kurdami išleistą produktą galite pasirinkti **Esamas svoris**. Išleistą produktą taip pat galima susieti su saugojimo dimensijų grupe, kurios parametras **Naudoti sandėlio valdymo procesus** yra pasirinktas.

Prieš naudodami produktą sandėlio valdyme turite atlikti kai kuriuos pagrindinius konkretaus produkto esamo svorio sąrankos veiksmus.

- Nustatykite nominalų svorio konvertavimą tarp esamo svorio vienetais (dėžė) ir atsargų vieneto (kilogramas \[kg\]) kaip vieneto konvertavimo aprašo dalį.
- Nurodykite mažiausio ir didžiausio svorio nuokrypius kaip esamo svorio vieneto sąrankos dalį.
- Nustatykite vienetų sekų grupę, kurioje esamo svorio vienetas apibrėžiamas kaip mažiausias sandėliavimo vienetas (SKU).
- Nustatykite esamo svorio prekių tvarkymo strategiją.

Daugiau informacijos žr. [Esamo svorio prekių nustatymas ir tvarkymas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Operacijos koregavimai

Kadangi į sandėlį patenkančių atsargų svoris gali skirtis nuo atsargų svorio, nurodyto jas išduodant iš sandėlio, esamo svorio produktų apdorojimas turi koreguoti atsargas.

> [!NOTE]
> Mobiliojo įrenginio veikla suaktyvins operacijų koregavimą tik tada, jei elemento esamo svorio elemento „Outbound“ svorio nuokrypio tvarkymo strategija yra **Leisti svorio nuokrypį**.

### <a name="example-1"></a>1 pavyzdys

Gamybos proceso **Skelbti baigtu** metu numerio lentelės, kurioje yra aštuonios esamo svorio produkto dėžės, gaunamas svoris užfiksuotas kaip 80,1 kg. Tada numerio lentelė yra saugoma pagamintų prekių srityje ir saugojimo laikotarpiu ji praranda šiek tiek svorio.

Vėliau vykdant pardavimo užsakymo išrinkimo procesą tos pačios numerio lentelės svoris užfiksuotas kaip 79,8 kg. Todėl sistemoje dabar egzistuoja svorio skirtumai kaip faktinių dimensijų rinkinio dalis.

Šiuo atveju sistema automatiškai koreguoja skirtumus registruodama operaciją, skirtą trūkstamam 0,3 kg.

### <a name="example-2"></a>2 pavyzdys

Apraše produktas nustatytas toleruoti minimalų 8 kg svorį ir maksimalų 12 kg svorį esamo svorio vienete **Dėžė**.

Jūs turite dvi produkto dėžes ir jų užregistruotas svoris yra 16 kg. Jei sandėlio darbuotojas paima ir pasveria vieną iš dėžių, o užfiksuotas svoris yra 9 kg, likusi dėžė svers 7 kg. Tačiau, kadangi 7 kg yra mažesnis nei minimalus svoris, sistema atlieka automatinį koregavimą, kad padidintų turimų atsargų svorį 1 kg.

Norėdami nustatyti sąskaitas, kuriose registruojami šie koregavimai, pasirinkite **Išlaidų valdymas \> DK integracijos strategijos \> Registravimas**. Tada skirtuke **Atsargos** nurodykite tolesnes sąskaitas.

- Svėrimo nuostolių sąskaita
- Svėrimo pelno sąskaita

## <a name="catch-weight-item-handling-policy"></a>Esamo svorio prekių sandėliavimo strategija

Esamo svorio prekės tvarkymo strategija apibrėžia du pirminius sandėlio valdymo prekių srautus: kada užfiksuojamas prekių svoris ir kaip jis užfiksuojamas.

Galite nurodyti, kada apdorojant pardavimo ir perkėlimo užsakymus skaičiuojamas svoris. Svoris gali būti fiksuojamas per vieną iš tolesnių procesų.

- **Paėmimas** – svoris užfiksuojamas pirminio darbo užsakymo eilučių paėmimo metu.
- **Pakavimas** – svoris užfiksuojamas neautomatinio pakavimo metu. (Prekes turite siųsti į pakavimo vietą.)

Jei faktinis svoris fiksuojamas pakavimo vietoje konteinerio pakavimo procesų metu, sandėlio darbuotojai nėra paraginami fiksuoti svorį išrinkimo darbo metu. Vietoje to vidutinis faktinių atsargų svoris yra naudojamas kaip paimtų atsargų, keliaujančių į pakavimo zoną, svoris. Ši koncepcija taikoma ir esamo svorio elementams, kurie sekami žymėmis. Žymėmis sekamoms prekėms šie parametrai nurodo, kada žymė užfiksuota. Žymė gali būti fiksuojama paėmimo metu naudojant mobilųjį įrenginį arba rankinio pakavimo metu.

> [!NOTE]
> Kadangi parinktis **Pakavimas** suaktyvina atsargų atnaujinimą į vidutinį paimtą svorį, gali atsirasti neatitikimas, dėl kurio gali būti pakoreguotas esamo svorio pelnas / nuostolis arba atsirasti skirtumas tarp turimų atsargų svorio ir esamo svorio žymės svorio.

Vykdant vidaus sandėlio valdymo procesus, pvz., skaičiavimo ir koregavimo taisymus, galite nurodyti, ar svoris turi būti fiksuojamas. Jei nefiksuojamas, naudojamas nominalus svoris. Kitos parinktys leidžia fiksuoti svorį pagal esamo svorio vienetą ir pagal skaičiavimo kiekį.

Taip pat galite nurodyti, kaip svoris skaičiuojamas. Viename iš dviejų pagrindinių srautų esamo svorio žymės yra stebimos ir naudojamos svoriui fiksuoti. Kitame sraute esamo svorio žymės nesekamos.

- **Taip** – prekė naudoja esamo svorio žymes. Kiekvienos žymės numeris nurodo vieną esamo svorio vienetą (dėžė), ir su žyme susiejami svoris bei kita informacija. Vykdant siuntimo procesus naudojamas svoris, kuris yra susietas su žyme.
- **Ne** – prekė nenaudoja esamo svorio žymių. Gaunamų ir siunčiamų prekių svėrimo procesai pagrįsti faktiniu svoriu, kuris užfiksuojamas kiekvieno proceso metu.

Esamo svorio žymių sekimo procesas gali būti taikomas prekėms, kurių svoris saugojimo laikotarpiu nepasikeis. Svoris bus užfiksuojamas tik gavimo sandėlio proceso metu. Siuntimo proceso metu esamo svorio žymės bus tik nuskaitytos, o su žymėmis susieti svoriai bus naudojami apdorojant siunčiamas operacijas.

Kitas svarbus parametras, susijęs su esamo svorio žymių apdorojimu, yra **Esamo svorio žymės dimensijos sekimo metodas**. Žymės gali būti iš dalies sekamos arba visiškai sekamos. Jei žymė yra iš dalies sekama, joje sekamos produkto dimensijos, sekimo dimensijos ir atsargų būsena. Jei žymė yra visiškai sekama, joje sekamos produkto dimensijos, sekimo dimensijos ir **visos** saugojimo dimensijos.

Be to, kai prekė yra sekama pagal žymę, yra parametras **Siunčiamo žymės fiksavimo metodas**. Šį parametrą galima nustatyti taip, kad visada būtumėte įspėti apie siuntimo operacijų žymę mobiliajame įrenginyje. Taip pat galite nustatyti parametrą, kad būtumėte įspėti apie žymes tik tada, kai jų reikia. Pavyzdžiui, atsargose duotoje numerio lentelėje yra penkios esamo svorio žymės ir nurodėte, kad iš numerio lentelės norite paimti visas penkias žymes. Tokiu atveju, jei parametras **Siunčiamo žymės fiksavimo metodas** nustatytas kaip **Įspėti apie žymę, kai reikia**, penkios žymės automatiškai paimamos. Nereikia nuskaityti kiekvienos žymės. Jei parametras nustatytas kaip **Visada įspėti apie žymę**, turite nuskaityti kiekvieną žymę, net jei paimtos visos penkios žymės.

> [!NOTE]
> Paprastai, žymės fiksuojamos ir atnaujinamos tik iš mobiliojo įrenginio meniu elementų. Nepaisant to, yra keli scenarijai, pagal kuriuos žymės fiksuojamos kur nors kitur (pavyzdžiui, iš rankinio pakavimo stoties). Tačiau paprastai, mobiliojo įrenginio meniu elementai turėtų būti naudojami visose sandėlio veiklose, jei naudojamos žymės.

### <a name="how-to-capture-catch-weight"></a>Kaip užfiksuoti esamą svorį

**Kai naudojamas esamo svorio žymės sekimas**,, žymė visada turi būti sukurta ir priskirta kiekvienam gaunamam esamo svorio vienetui, o kiekviena žymė visada turi būti susieta su svoriu.

Pvz., **Dėžė** yra esamo svorio vienetas ir jūs gaunate vieną aštuonių dėžių padėklą. Šiuo atveju turi būti sukurtos aštuonios unikalios esamo svorio žymės, o svoris turi būti susietas su kiekviena žyme. Priklausomai nuo gaunamų prekių esamo svorio žymės, galima užfiksuoti visų aštuonių dėžių svorį ir paskirstyti vidutinį svorį kiekvienai dėžei arba galima užfiksuoti unikalų kiekvienos dėžės svorį.
Mobiliojo įrenginio meniu elemente su įjungtu procesu naudojant funkciją **Naudoti esamas esamo svorio žymes pranešant, kad gamybos užsakymai yra baigti**, atsargos atnaujinamos atsižvelgiant į esamą esamo svorio žymės informaciją. Todėl sandėlio valdymo mobiliųjų įrenginių programėlė neragina užfiksuoti esamo svorio žymių duomenis, priklausančius gamybos ataskaitai kaip užbaigtą operaciją.

**Kai esamo svorio žymės sekimas nenaudojamas**, svorį galima užfiksuoti kiekviename dimensijų rinkinyje (pvz., ir kiekvienoje numerio lentelėje ir sekimo dimensijoje). Taip pat svoris gali būti užfiksuotas sujungtu lygiu, pvz., kaip penkių numerių lentelių (padėklų) svoris.

Taikant metodus, skirtus fiksuoti siuntimo svorį, parinktis **Pagal esamo svorio vienetą** leidžia nurodyti, kad svėrimas turi būti atliktas su kiekvienu esamo svorio vienetu (pavyzdžiui, kiekviena dėže). Parinktis **Pagal paėmimo vienetą** leidžia nustatyti, kad svoris turi būti fiksuojamas pagal kiekį, kuris bus paimtas (pavyzdžiui, trys dėžės). Atkreipkite dėmesį, kad, jei bus naudojama parinktis **Neužfiksuotas**, gamybos eilutės išrinkimo ir vidinio judėjimo procesų metu bus naudojamas vidutinis svoris.

Keli svorio fiksavimo metodai apibrėžiami pagal esamo svorio prekių tvarkymo strategiją. Kiekvieną svorio fiksavimo metodo parametrą naudoja įvairios operacijos. Šioje lentelėje apibendrinama, kuriuos parametrus naudoja operacijos.

| Metodas                                     | Operacija                                |
|--------------------------------------------|--------------------------------------------|
| Siunčiamo svorio fiksavimo metodas           | Pardavimo paėmimas, perdavimo paėmimas            |
| Gamybos paėmimo svorio fiksavimo metodas | Gamybos paėmimas, gamybos sunaudojimas |
| Perkėlimo svorio fiksavimo metodas           | Judėjimas                                   |
| Kada fiksuoti svorį pataisymą       | Koregavimai, skaičiavimas                      |
| Skaičiuojamo svorio fiksavimo metodas           | Inventorizacija                                   |
| Sandėlio perdavimo svorio fiksavimo metodas | Perkėlimas sandėlyje                         |

Siekiant apsaugoti sandėlio valdymo išrinkimo procesus, kad, fiksuojant svorius, nereikėtų koreguoti esamo svorio pelno / nuostolio, galite naudoti siunčiamo svorio nuokrypio metodą. Siunčiamo svorio nuokrypio metodas taikomas naudojant šiuos mobiliojo įrenginio procesus: pardavimo paėmimas, perdavimo paėmimas, gamybos paėmimas, judėjimas, skaičiavimas ir sandėlio perdavimai. Galite naudoti parinktį **Apriboti svorio nuokrypį**, jei esamo svorio prekės, kai ji saugoma sandėlyje, svoris svyruoja, ir jeigu nereikia koreguoti esamo svorio pelno / nuostolio. Galite naudoti parinktį **Leisti svorio nuokrypį**, jei svoris gali svyruoti ir jei reikia pakoreguoti esamo svorio pelną / nuostolius, kai įrašomas svorio svyravimas.

## <a name="unsupported-scenarios"></a>Nepalaikomi scenarijai

Ne visos darbo eigos palaiko esamo svorio produktų apdorojimą naudojant sandėlio valdymą. Šiuo metu taikomi toliau nurodyti apribojimai. Jie taikomi visoms esamo svorio prekėms, neatsižvelgiant į tai, ar jos pažymėtos.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Esamo svorio produktų konfigūravimas vykdant sandėlio valdymo procesus

- Palaikomas tik esamo svorio produktų formulės apdorojimas (ne KS).
- Esamo svorio produktų negalima susieti su sekimo dimensijų grupe naudojant dimensiją Savininkas.
- Esamo svorio produktų negalima naudoti kaip paslaugų.
- Esamo svorio produktus galima naudoti kaip „laikomus produktus“ tik kaip prekių modelių grupės dalį.
- Esamo svorio produktų negalima naudoti kartu su sekimo funkcija „Aktyvūs pardavimo procese“.
- Esamo svorio produktų negalima naudoti kartu su serijos numerių fiksavimo funkcija. Todėl produktai negali būti perkelti iš „tuščio“ į serijos numerį paėmimo / pakavimo proceso metu.
- Esamo svorio produktų negalima naudoti kartu su serijos numerių registravimo prieš vartojimą funkcija.
- Esamo svorio produktų, kurių variantai įjungti, negalima naudoti kartu su varianto matavimo vienetų konvertavimo funkcija.
- Esamo svorio produktai negali būti pažymėti kaip prekybos „produktų rinkinys“.
- Esamo svorio produktai gali būti naudojami tik su vienetų sekų grupe, kuriai priskirti esamo svorio sandėliavimo vienetai ir kurios žemiausia seka yra esamo svorio vienetas.
- Jei produktai yra esamo svorio atsargų vienetą galima konvertuoti į esamo svorio vienetą, jei konvertavimo metu generuojamas nominalus kiekis, kuris yra didesnis nei 1.
- Esamo svorio produktų brūkšninių kodų sąranka nepalaiko kintamo svorio sąrankos.

### <a name="order-processing"></a>Užsakymų apdorojimas

- Išankstinio siuntimo pranešimas (ASN / pakavimo struktūros) nepalaiko svorio informacijos.
- Užsakymo kiekis turi būti tvarkomas pagal esamo svorio vienetą.

### <a name="inbound-warehouse-processing"></a>Gaunamų prekių sandėliavimo apdorojimas

- Gaunant numerių lenteles svoriai turi būti priskirti registruojant, nes svorio informacija nepalaikoma kaip išankstinio siuntimo pranešimo dalis. Kai naudojami esamo svorio žymių procesai, žymės numeris turi būti neautomatiškai priskirtas kiekvienam esamo svorio vienetui.
- Gaunamas kokybės patikrinimo darbas nepalaikomas su esamo svorio produktais. Jei sukonfigūruotas, kokybės patikrinimo darbas bus praleistas.

### <a name="inventory-and-warehouse-operations"></a>Atsargų ir sandėlio žurnalų operacijos

- Neautomatinis sulaikymo užsakymų kūrimas nepalaikomas naudojant esamo svorio produktus.
- Neautomatinis su atviru darbu susijusių atsargų perkėlimas nepalaikomas naudojant esamo svorio produktus.
- Numerio lentelės įkėlimas norint inicijuoti sandėlio atsargas nepalaikomas naudojant esamo svorio produktus.
- Partijų balansavimo procesai nepalaikomi naudojant esamo svorio produktus.
- Neigiamų faktinių atsargų tvarkymas nepalaikomas naudojant esamo svorio produktus.
- Atsargų žymėjimas nepalaikomas naudojant esamo svorio produktus.

### <a name="outbound-warehouse-processing"></a>Siunčiamų prekių sandėliavimo apdorojimas

- Klasterio paėmimo funkcija nepalaikoma naudojant esamo svorio produktus.
- Paėmimo ir pakavimo sandėlio apdorojimas nepalaikoma naudojant esamo svorio produktus.
- Pagauto svorio produktams, darbo šablone nenustatytas darbas negali būti vykdomas automatiškai.
- Naudojant esamo svorio produktus, sistema nepalaiko rankinio pakavimo vietos apdorojimo, kai supakuoto konteinerio paėmimo darbas kuriamas uždarius konteinerius.
- Nuoseklaus vienetų nuskaitymo funkcija nepalaikoma naudojant esamo svorio produktus.

### <a name="production-processing"></a>Gamybos apdorojimas

- Naudojant esamo svorio produktus palaikomi tik formulės produktų paketiniai užsakymai.
- Naudojant esamo svorio produktus „Kanban“ funkcija nepalaikoma.
- Naudojant esamo svorio produktus serijos numeriai negali būti užregistruoti prieš suvartojimą.
- Naudojant esamo svorio produktus numerių lentelių atšaukimo iš gamybos funkcija nepalaikoma.
- Naudojant esamo svorio produktus skelbimas baigtu gali būti registruojamas pagal serijos numerį.

### <a name="transportation-management-processing"></a>Transportavimo valdymo apdorojimas

- Naudojant esamo svorio produktus krovinio kūrimo darbo sritis nepalaikoma.
- Naudojant esamo svorio produktus transportavimo užklausos eilutės nepalaikomos.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Kiti esamo svorio produktų apdorojimo naudojant sandėlio valdymą apribojimai ir elgsena

- Išrinkimo procesų metu, kai vartotojas nėra raginamas nustatyti sekimo dimensijas, svorio priskyrimas atliekamas pagal vidutinį svorį. Taip atsitinka, kai, pvz., sekimo dimensijų derinys naudojamas toje pačioje vietoje ir, kai vartotojas apdoroja paėmimą, vietoje lieka tik viena sekimo dimensijos reikšmė.
- Kai atsargos rezervuotos esamo svorio produktui, kuris sukonfigūruotas sandėlio valdymo procesuose, rezervavimas atliekamas remiantis nustatytu minimaliu svoriu, net jei šis kiekis yra vėliausias turimų atsargų sandėliavimo kiekis. Ši elgsena skiriasi nuo prekių, kurios nesukonfigūruotos sandėlio valdymo procesuose, elgsenos. Šiam apribojimui yra viena išimtis. Gamybos paėmimui, kai esamo svorio produkto, kuris valdomas pagal serijos numerį, paskutinis sutvarkytas kiekis yra paimamas, naudojamas faktinis svoris.
- Procesai, kurie naudoja svorį kaip pajėgumo skaičiavimų dalį (bangos ribinės reikšmės, maksimalios darbo pertraukos, maksimalūs konteineriai, vietos apkrovos pajėgumas ir t. t.), nenaudoja faktinio atsargų svorio. Vietoje to procesai yra pagrįsti nurodytu faktiniu produkto sandėliavimo svoriu.
- Įprastai, naudojant esamo svorio produktus, prekybos funkcija nepalaikoma.
- Esamo svorio produktams, atsargų būsena negali būti atnaujinta iš **Sandėlio būsenos keitimas**.

### <a name="catch-weight-tags"></a>Esamo svorio žymės

Esamo svorio žymę galima sukurti naudojant sandėlio valdymo mobiliųjų įrenginių programėlės procesą, ją galima rankiniu būdu sukurti formoje **Sandėlio valdymas > Užklausos ir ataskaitos > Esamo svorio žymė** arba naudojant duomenų objekto procesą. Jei esamo svorio žymė susieta su gaunamo šaltinio dokumento eilute, pvz., pirkimo užsakymo eilute, žymė bus užregistruota. Jei eilutė naudojama siuntimo apdorojimui, žymė bus atnaujinta kaip išsiųsta. Galite peržiūrėti visus retrospektyvinius esamo svorio žymės registracijos įvykius naudodami **Esamo svorio žymės registravimo** parinktį, esančią puslapyje **Esamo svorio žymė**.

Norėdami rankiniu būdu atnaujinti esamo svorio žymės svorio reikšmę, galite naudoti parinktį **Keisti žymės užfiksuotą svorį**. Įsidėmėkite, kad turimų atsargų svoris nebus koreguojamas kaip šio neautomatinio proceso dalis, tačiau galite lengvai naudoti puslapį **Turimų esamo svorio pažymėtų elementų neatitikimai** norėdami peržiūrėti visus neatitikimus tarp esamų aktyvių esamo svorio žymų ir dabartinių atsargų.

Kitos rankinio naudojimo parinktys **Registruoti žymę** šaltinio dokumento eilutei ir **Registruoti darbą** pagal esamą sandėlio darbą.

Be apribojimų, kurie šiuo metu taikomi esamo svorio produktams, pažymėti esamo svorio produktai turi kitus šiuo metu taikomus apribojimus.

- Visi neautomatiniai atsargų naujinimai (t. y. naujinimai, atliekami nenaudojant mobiliojo įrenginio) turi apimti atitinkamus neautomatinius naujinimus į susijusias esamo svorio žymes, nes šie naujinimai nėra atliekami automatiškai. Pavyzdžiui, rankiniu būdu pakoreguoti žurnalai atnaujins atsargas, o ne susijusias esamo svorio žymes.
- Norėdami parodyti papildymo darbo judėjimą, turite rankiniu būdu atnaujinti esamo svorio žymes. Taip yra todėl, kad sistema negali užfiksuoti svorio, kai apdorojamas papildymo darbas, todėl įrašo vidutinį svorį.
- Mišrios numerio lentelės gavimas šiuo metu nepalaikomas su pažymėtomis esamo svorio prekėmis.
- Pardavimo grąžinimo užsakymo apdorojimas gali įrašyti esamo svorio žymes. Tačiau procesas nepatvirtina, kad grąžinta žymė yra ta pati žymė, kuri iš pradžių buvo išsiųsta pardavimo užsakymui.
- Mobiliojo įrenginio meniu elementas, kuriame yra **Registruoti medžiagų sunaudojimą** veiklos kodas, šiuo metu nepalaiko esamo svorio žymių įrašymo.
- Nors yra palaikomi žymėtų esamo svorio prekių skaičiavimo procesai, jie yra riboti. Pavyzdžiui, galite naudoti mobiliojo įrenginio parinktis, skirtas skaičiuoti pažymėtas esamo svorio prekes, tada naudojamas vidutinis svoris. Tačiau esamo svorio žymės nėra automatiškai atnaujinamos naudojant skaičiavimo operaciją. Užbaigus skaičiavimo operaciją, esamo svorio žymės turi būti atnaujintos rankiniu būdu, kad atitiktų atsargas. Jei prekės, kurių pradžioje nebuvo vietoje, įtraukiamos į tą vietą, naudojamas nominalus svoris.
- Numerio lentelės konsolidavimas šiuo metu nepalaiko pažymėtų esamo svorio prekių.
- Atšaukimo darbo funkcija nepalaikoma esamo svorio prekėms, kurios sekamos pagal žymės numerį.

> [!NOTE]
> Ankstesnė informacija apie esamo svorio žymes galioja, tik jei esamo svorio produktui taikomas esamo svorio žymės dimensijos sekimo metodas, pagal kurį visiškai sekama (tai yra, jei parametras **Esamo svorio žymės dimensijos sekimo metodas** esamo svorio prekių tvarkymo strategijoje nustatytas kaip **Produkto dimensijos, sekimo dimensijos ir visos saugojimo dimensijos**). Jei esamo svorio prekė tik iš dalies sekama pagal žymę (tai yra, parametras **Esamo svorio žymės dimensijos sekimo metodas** esamo svorio prekių tvarkymo strategijoje nustatytas kaip **Produkto dimensijos, sekimo dimensijos ir atsargų būsena**), taikomi papildomi apribojimai Kadangi šiuo atveju prarastas matomumas tarp žymės ir atsargų, kai kurie papildomi scenarijai nepalaikomi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]