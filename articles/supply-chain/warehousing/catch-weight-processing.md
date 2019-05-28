---
title: Esamo svorio produktų apdorojimas naudojant sandėlio valdymą
description: Šioje temoje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje atliekamas darbas.
author: perlynne
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 14f2c6eb3baf0de65de3b72e10b42b03a8c6b21a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536715"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Esamo svorio produktų apdorojimas naudojant sandėlio valdymą

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/pivate-preview-banner.md)]


## <a name="feature-exposure"></a>Funkcijos įjungimas

Norėdami naudoti sandėlio valdymą esamo svorio produktams apdoroti, turite naudoti licencijos konfigūracijos raktą, kad įjungtumėte funkciją. (Pasirinkite **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**. Tada skirtuke **Konfigūracijos raktai** išplėskite **Prekyba \> Sandėlio ir transportavimo valdymas**, tada pasirinkite žymės langelį **Esamas svoris sandėlyje**).

> [!NOTE]
> Licencijos konfigūracijos raktas **Sandėlio ir transportavimo valdymas** ir licencijos konfigūracijos raktai **Apdoroti paskirstymą \> Esamas svoris** turi būti įjungti.

Įjungus licencijos konfigūracijos raktą, kurdami išleistą produktą galite pasirinkti **Esamas svoris**. Išleistą produktą taip pat galima susieti su saugojimo dimensijų grupe, kurios parametras **Naudoti sandėlio valdymo procesus** yra pasirinktas.

Prieš naudodami produktą sandėlio valdyme turite atlikti kai kuriuos pagrindinius konkretaus produkto esamo svorio sąrankos veiksmus.

- Nustatykite nominalų svorio konvertavimą tarp esamo svorio vienetais (dėžė) ir atsargų vieneto (kilogramas \[kg\]) kaip vieneto konvertavimo aprašo dalį.
- Nurodykite mažiausio ir didžiausio svorio nuokrypius kaip esamo svorio vieneto sąrankos dalį.
- Nustatykite vienetų sekų grupę, kurioje esamo svorio vienetas apibrėžiamas kaip mažiausias sandėliavimo vienetas (SKU).
- Nustatykite esamo svorio prekių tvarkymo strategiją.

Daugiau informacijos žr. [Esamo svorio prekių nustatymas ir tvarkymas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Operacijos koregavimai

Kadangi į sandėlį patenkančių atsargų svoris gali skirtis nuo atsargų svorio, nurodyto jas išduodant iš sandėlio, esamo svorio produktų apdorojimas turi koreguoti atsargas.

**1 pavyzdys**

Gamybos proceso **Skelbti baigtu** metu numerio lentelės, kurioje yra aštuonios esamo svorio produkto dėžės, gaunamas svoris užfiksuotas kaip 80,1 kg. Tada numerio lentelė yra saugoma pagamintų prekių srityje ir saugojimo laikotarpiu ji praranda šiek tiek svorio.

Vėliau vykdant pardavimo užsakymo išrinkimo procesą tos pačios numerio lentelės svoris užfiksuotas kaip 79,8 kg. Todėl sistemoje dabar egzistuoja svorio skirtumai kaip faktinių dimensijų rinkinio dalis.

Šiuo atveju sistema automatiškai koreguoja skirtumus registruodama operaciją, skirtą trūkstamam 0,3 kg.

**2 pavyzdys**

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

Jei faktinis svoris fiksuojamas pakavimo vietoje konteinerio pakavimo procesų metu, sandėlio darbuotojai nebus paraginti fiksuoti svorį išrinkimo darbo metu. Vietoje to vidutinis faktinių atsargų svoris bus naudojamas kaip paimtų atsargų, keliaujančių į pakavimo zoną, svoris.

Vykdant vidaus sandėlio valdymo procesus, pvz., skaičiavimo ir koregavimo taisymus, galima nurodyti, ar svoris turi būti fiksuojamas. Jei nefiksuojamas, naudojamas nominalus svoris.

Taip pat galite nurodyti, kaip svoris skaičiuojamas. Viename iš dviejų pagrindinių srautų esamo svorio žymės yra stebimos ir naudojamos svoriui fiksuoti. Kitame sraute esamo svorio žymės nesekamos.

- **Taip** – prekė naudoja esamo svorio žymes. Kiekvienos žymės numeris nurodo vieną esamo svorio vienetą (dėžė), ir su žyme susiejami svoris bei kita informacija. Vykdant siuntimo procesus naudojamas svoris, kuris yra susietas su žyme.
- **Ne** – prekė nenaudoja esamo svorio žymių. Gaunamų ir siunčiamų prekių svėrimo procesai pagrįsti faktiniu svoriu, kuris užfiksuojamas kiekvieno proceso metu.

Esamo svorio žymių sekimo procesas gali būti taikomas prekėms, kurių svoris saugojimo laikotarpiu nepasikeis. Svoris bus užfiksuojamas tik gavimo sandėlio proceso metu. Siuntimo proceso metu esamo svorio žymės bus tik nuskaitytos, o su žymėmis susieti svoriai bus naudojami apdorojant siunčiamas operacijas.

### <a name="how-to-capture-catch-weight"></a>Kaip užfiksuoti esamą svorį

Kai naudojamas esamo svorio žymės sekimas, žymė visada turi būti sukurta ir priskirta kiekvienam gaunamam esamo svorio vienetui, o kiekviena žymė visada turi būti susieta su svoriu.

Pvz., **Dėžė** yra esamo svorio vienetas ir jūs gaunate vieną aštuonių dėžių padėklą. Šiuo atveju turi būti sukurtos aštuonios unikalios esamo svorio žymės, o svoris turi būti susietas su kiekviena žyme. Priklausomai nuo gaunamų prekių esamo svorio žymės, galima užfiksuoti visų aštuonių dėžių svorį ir paskirstyti vidutinį svorį kiekvienai dėžei arba galima užfiksuoti unikalų kiekvienos dėžės svorį.

Kai esamo svorio žymės sekimas nenaudojamas, svorį galima užfiksuoti kiekviename dimensijų rinkinyje (pvz., ir kiekvienoje numerio lentelėje ir sekimo dimensijoje). Taip pat svoris gali būti užfiksuotas sujungtu lygiu, pvz., kaip penkių numerių lentelių (padėklų) svoris.

Nustatydami siunčiamo svorio fiksavimo metodus galite nurodyti, ar sveriamas kiekvienas esamo svorio vienetas (t. y. kiekviena dėžė), ar svoris skaičiuojamas pagal kiekį, kuris bus paimtas (pavyzdžiui, trys dėžės). Atkreipkite dėmesį, kad, jei bus naudojama parinktis **Neužfiksuotas**, gamybos eilutės išrinkimo ir vidinio judėjimo procesų metu bus naudojamas vidutinis svoris.

Siekiant apriboti sandėlio valdymo išrinkimo procesus, kad, fiksuojant svorius, nereikėtų koreguoti esamo svorio pelno / nuostolio, galima naudoti siunčiamo svorio nuokrypio metodą.

## <a name="supported-scenarios"></a>Palaikomi scenarijai

Ne visos darbo eigos palaiko esamo svorio produktų apdorojimą naudojant sandėlio valdymą. Šiuo metu taikomi toliau nurodyti apribojimai.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Esamo svorio produktų konfigūravimas vykdant sandėlio valdymo procesus

- Jei produktai yra esamo svorio, prekių saugojimo dimensijų grupės negalima keisti (kad būtų galima naudoti jiems skirtus sandėlio valdymo procesus).
- Palaikomas tik esamo svorio produktų formulės apdorojimas (ne KS).
- Esamo svorio produktų negalima susieti su sekimo dimensijų grupe naudojant dimensiją Savininkas.
- Esamo svorio produktų negalima naudoti kaip paslaugų.
- Esamo svorio produktus galima naudoti kaip „laikomus produktus“ tik kaip prekių modelių grupės dalį.
- Esamo svorio produktų negalima naudoti kartu su sekimo funkcija „Aktyvūs pardavimo procese“.
- Esamo svorio produktų negalima naudoti kartu su serijos numerių fiksavimo funkcija. Todėl produktai negali būti perkelti iš „tuščio“ į serijos numerį paėmimo / pakavimo proceso metu.
- Esamo svorio produktų negalima naudoti kartu su serijos numerių registravimo prieš vartojimą funkcija.
- Esamo svorio produktų, kurių variantai įjungti, negalima naudoti kartu su varianto matavimo vienetų konvertavimo funkcija.
- Esamo svorio produktai negali būti pažymėti kaip mažmeninės „prekybos rinkinys“.
- Esamo svorio produktai gali būti naudojami tik su vienetų sekų grupe, kuriai priskirti esamo svorio sandėliavimo vienetai ir kurios žemiausia seka yra esamo svorio vienetas.
- Jei produktai yra esamo svorio atsargų vienetą galima konvertuoti į esamo svorio vienetą, jei konvertavimo metu generuojamas nominalus kiekis, kuris yra didesnis nei 1.
- Esamo svorio produktų brūkšninių kodų sąranka nepalaiko kintamo svorio sąrankos.
 
### <a name="order-processing"></a>Užsakymų apdorojimas

- Išankstinio siuntimo pranešimas (ASN / pakavimo struktūros) nepalaiko svorio informacijos.
- Užsakymo kiekis turi būti tvarkomas pagal esamo svorio vienetą.
 
### <a name="inbound-warehouse-processing"></a>Gaunamų prekių sandėliavimo apdorojimas

- Gaunant numerių lenteles svoriai turi būti priskirti registruojant, nes svorio informacija nepalaikoma kaip išankstinio siuntimo pranešimo dalis. Kai naudojami esamo svorio žymių procesai, žymės numeris turi būti neautomatiškai priskirtas kiekvienam esamo svorio vienetui.
 
### <a name="inventory-and-warehouse-operations"></a>Atsargų ir sandėlio žurnalų operacijos

- Neautomatinis sulaikymo užsakymų kūrimas nepalaikomas naudojant esamo svorio produktus.
- Neautomatinis su darbu susijusių atsargų perkėlimas nepalaikomas naudojant esamo svorio produktus.
- Numerių lentelių konsolidavimas nepalaikomas naudojant esamo svorio produktus.
- Sandėlio atsargų būsenos pakeitimai kaip periodinės užduoties dalis nepalaikomi naudojant esamo svorio produktus.
- Užklausos apibrėžti atsargų būsenos pakeitimai nepalaikomi naudojant esamo svorio produktus. (Kokybės užsakymo atsargų būsenos pakeitimai taip pat palaikomi.)
- Naudojant esamo svorio produktus atsargų būsena negali būti pakeista iš puslapio **Turimos atsargos pagal vietą**.
- Naudojant esamo svorio produktus, atsargų būsena negali būti pakeista kaip sandėlio programos perkėlimo darbo dalis.
- Numerio lentelės įkėlimas norint inicijuoti sandėlio atsargas nepalaikomas naudojant esamo svorio produktus.
- Partijų balansavimo procesai nepalaikomi naudojant esamo svorio produktus.
- Neigiamų faktinių atsargų tvarkymas nepalaikomas naudojant esamo svorio produktus.
- Atsargų žymėjimas nepalaikomas naudojant esamo svorio produktus.
 
### <a name="outbound-warehouse-processing"></a>Siunčiamų prekių sandėliavimo apdorojimas

- Klasterio paėmimo funkcija nepalaikoma naudojant esamo svorio produktus.
- Paėmimo ir pakavimo sandėlio apdorojimas nepalaikoma naudojant esamo svorio produktus.
- Darbas negali būti baigtas iš puslapio **Darbas** naudojant esamo svorio produktus.
- Darbas, nurodytas darbo šablone, gali būti vykdomas automatiškai naudojant esamo svorio produktus.
- Darbo atšaukimo funkcija nepalaikoma naudojant esamo svorio produktus.
- Naudojant esamo svorio produktus nepalaikomas neautomatinis pakavimo vietos apdorojimas, kai darbas kuriamas uždarius konteinerius.
- Nuoseklaus vienetų nuskaitymo funkcija nepalaikoma naudojant esamo svorio produktus.
 
### <a name="production-processing"></a>Gamybos apdorojimas

- Naudojant esamo svorio produktus palaikomi tik formulės produktų paketiniai užsakymai.
- Naudojant esamo svorio produktus „Kanban“ funkcija nepalaikoma.
- Naudojant esamo svorio produktus serijos numeriai negali būti užregistruoti prieš suvartojimą.
- Naudojant esamo svorio produktus numerių lentelių atšaukimo funkcija nepalaikoma.
- Naudojant esamo svorio produktus skelbimas baigtu gali būti registruojamas pagal serijos numerį.

### <a name="transportation-management-processing"></a>Transportavimo valdymo apdorojimas

- Naudojant esamo svorio produktus krovinio kūrimo darbo sritis nepalaikoma.
- Naudojant esamo svorio produktus transportavimo užklausos eilutės nepalaikomos.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Kiti esamo svorio produktų apdorojimo naudojant sandėlio valdymą apribojimai ir elgsena

- Išrinkimo procesų metu, kai vartotojas nėra raginamas nustatyti sekimo dimensijas, svorio priskyrimas atliekamas pagal vidutinį svorį. Taip atsitinka, kai, pvz., sekimo dimensijų derinys naudojamas toje pačioje vietoje ir, kai vartotojas apdoroja paėmimą, vietoje lieka tik viena sekimo dimensijos reikšmė.
- Kai atsargos rezervuotos esamo svorio produktui, kuris sukonfigūruotas sandėlio valdymo procesuose, rezervavimas atliekamas remiantis nustatytu minimaliu svoriu, net jei šis kiekis yra vėliausias turimų atsargų sandėliavimo kiekis. Ši elgsena skiriasi nuo prekių, kurios nesukonfigūruotos sandėlio valdymo procesuose, elgsenos.
- Procesai, kurie naudoja svorį kaip pajėgumo skaičiavimų dalį (bangos ribinės reikšmės, maksimalios darbo pertraukos, maksimalūs konteineriai, vietos apkrovos pajėgumas ir t. t.), nenaudoja faktinio atsargų svorio. Vietoje to procesai yra pagrįsti nurodytu faktiniu produkto sandėliavimo svoriu.
- Įprastai naudojant esamo svorio produktus mažmeninės prekybos funkcija nepalaikoma.
 
### <a name="catch-weight-tags"></a>Esamo svorio žymės

Šiuo metu esamo svorio žymių funkcija palaikoma tik vykdant toliau nurodytus scenarijus.

- Apdorojant pirkimo užsakymo sandėlio programos gavimą.
- Kai apdorojamas krovinio gavimas naudojant sandėlio programą.
- Jei numerio lentelės gavimas susijęs su pirkimo užsakymo kroviniu, svorio priskyrimo reikalaujama gavimo proceso metu. Tačiau jei gaunamas perkėlimo užsakymas, naudojamas perkėlimo užsakymo siuntos duomenų svoris.
- Jei gaunamos perkėlimo užsakymo prekės ir eilutės, jos gaunamos iš ne sandėlio valdymo proceso sandėlio.
- Apdorojant pardavimo grąžinimo užsakymo gavimą galima įrašyti esamo svorio žymes, tačiau apdorojimas nebus patvirtintas, jei žymės yra tos pačios žymės, kurios buvo iš pradžių atsiųstos konkrečioje pardavimo užsakymo eilutėje.
- Apdorojant pakeistą atsargų būseną naudojant sandėlio programą.
- Kai vykdomas sandėlio perkėlimas naudojant sandėlio programą.
- Kai apdorojamas gavimo ir siuntimo koregavimas naudojant sandėlio programą.
- Kai apdorojamas pardavimo ir perkėlimo užsakymų išrinkimo darbas. (Atkreipkite dėmesį, kad esamo svorio žymių negalima įrašyti vykdant gamybos komponentų paėmimą.)
- Kai paimti kiekiai atimami iš krovinio eilučių, nepriklausomai nuo to, ar naudojami konteineriai.
- Kai produktai supakuojami į konteinerius pakavimo stotyje.
- Kai konteineriai atidaromi iš naujo.
- Kai formulės produktai skelbiami baigtais naudojant sandėlio programą.
- Kai transportavimo kroviniai apdorojami naudojant sandėlio programą.

Esamo svorio žymę galima sukurti naudojant sandėliavimo programos procesą, rankiniu būdu sukurti formoje arba sukurti naudojant duomenų objekto procesą. Jei esamo svorio žymė bus susieta su gaunamo šaltinio dokumento eilute, pvz., pirkimo užsakymo eilute, žymė bus užregistruota. Jei eilutė yra naudojama siuntimui apdoroti. Žymė bus atnaujinta kaip išsiųsta.
