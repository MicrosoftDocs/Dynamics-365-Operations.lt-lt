---
title: "Kintamosios atlyginimo dalies planų kūrimas"
description: "Kintamąją atlyginimo dalį sudaro nepastovus darbuotojo darbo užmokestis, pvz., premijos ar premijų akcijos. Šioje temoje aprašoma komponentus, kurie turi būti nustatyta prieš jūs galite naudoti kintamosios atlyginimo dalies ir registruotis darbuotojų kintamosios atlyginimo dalies plano."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Kintamosios atlyginimo dalies planų kūrimas

Kintamąją atlyginimo dalį sudaro nepastovus darbuotojo darbo užmokestis, pvz., premijos ar premijų akcijos. Šiame straipsnyje aprašyti komponentai, kurie turi būti nustatyti prieš naudojant kintamąją atlyginimo dalį ir įtraukiant darbuotojus į kintamosios atlyginimo dalies planą.

Jūsų darbuotojų kintamosios atlyginimo dalies sumų skaičiavimas gali būti paremtas į keliais veiksniais, pvz., darbuotojo rezultatais, darbuotojo kompensacijos lygiu ir padalinio rezultatais.

## <a name="variable-compensation-components"></a>Kintamosios atlyginimo dalies komponentai
### <a name="create-compensation-types"></a>kompensacijos tipų sukūrimas

**Kintamosios atlyginimo dalies tipai **yra būtinas komponentas. Kintamosios atlyginimo dalies tipai leidžia aprašyti jūsų organizacijos teikiamas kintamosios atlyginimo dalies rūšis. Jie taip pat leidžia nurodyti, ar kompensacija bus mokama grynaisiais pinigais, ar nepinigine forma, pvz., akcijomis.

### <a name="describe-vesting-rules"></a>Paskirstymo taisyklių aprašymas

Pasirinktinai įmonės gali nustatyti **paskirstymo taisykles**. Teisių suteikimo taisykles apibūdinti kaip kintamosios premijos turėtų būti paskirstyti per tam tikrą laiką. Pvz., teisių perdavimo taisyklė gali nurodyti, kad darbuotojas gaus 25 procentus savo bendrą apdovanojimą kasmet ateinančius ketverius metus. Teisių perdavimo taisyklės yra tik informacinio pobūdžio.

## <a name="variable-compensation-plans"></a>Kintamųjų atlyginimo dalių planai
**Kintamosios atlyginimo dalies planas** apima įtrauktų darbuotojų kintamosios atlyginimo dalies taisykles, skaičiavimo metodus ir numatytąsias skaičiavimo reikšmes. Kai kuriate kintamosios atlyginimo dalies planą, turite nustatyti kintamosios atlyginimo dalies tipą. Kintamosios atlyginimo dalies tipas nurodo, ar sistema apskaičiuoja sumą valiuta arba vienetų skaičius, kai. Taip pat turite nustatyti skaičiavimo metodą:

-   **Kuriuo metu** – kintamoji premija skaičiuojama remiantis ilgalaikio kompensaciją, kad darbuotojas turėjo tam tikrą dieną. Šios datos yra nurodytas proceso atveju, kai tvarkomi naują kompensacijų.
-   **Sudėtinis** – apskaičiuojama premijos suma kiekvienam unikaliam pastoviosios atlyginimo dalies užmokesčio tarifui, kuris buvo taikomas darbuotojui tarp ciklo pradžios dienos ir ciklo pabaigos dienos apdorojimo įvykio metu. Tarifai yra pridedami kartu nustatyti galutinis sprendimas sudaryti sutartį. Pvz., ciklo metu, darbuotojas perkeltas į kitą vietą, kad turėjo skirtingus mokėjimo koeficientą. Tokiu atveju kintamosios dalies premija koreguojama pagal laiką, kurį darbuotojui buvo taikomas kiekvienas užmokesčio tarifas.

Kintamosios dalies premijos sumą gali sudaryti procentas nuo darbuotojo reguliaraus pagrindinio darbo užmokesčio arba nustatytas vienetų skaičius.

-   Pasirinkite parinktį **Pagrindo procentas**, kad įvestumėte numatytąjį procentą, ir nurodykite, ar pagrindas turi būti darbuotojo fiksuotas darbo užmokesčio tarifas, ar darbuotojo kompensacijos lygio kontrolinis taškas. Kompensacijos dydis nustatomas darbuotojo darbas. Vienas iš atskaitos taškai, nuo atlygio sistema gali būti nustatyti kaip kontroliniam taškui pastoviųjų atlyginimo dalių plano. Sistema naudoja kompensavimo lygį nuo darbuotojo darbo ir kryžminę nuorodą su kontrolės punktas, kuris pateikiamas darbuotojo pastoviųjų atlyginimo dalių plano rasti kontrolės taškų suma už darbuotojo kompensacijos lygis. Kontrolės taškų suma bus tada būti remiamasi vietoj darbuotojo fiksuoto užmokesčio tarifas sudarymo.
-   Pasirinkite parinktį** Vienetų skaičius**, kad įvestumėte numatytąjį vienetų skaičių, kiekvieno vieneto vertę ir vieneto vertės valiutą, jei kompensacijos plano premija mokama ne grynaisiais pinigais (pvz., 200 akcijų, kurių kiekvienos vertė 40 USD), arba tiesiog vienetų skaičių, jei kompensacijos plano premija mokama grynaisiais pinigais. Už grynųjų pinigų skyrimo, darbuotojas gaus nurodytą skaičių investicinių vienetų, ta valiuta, kuri naudojama jo arba jos pastoviųjų atlyginimo dalių plano (pvz., 500 vnt., 1 USD). Valdiklio ryšį galima nurodyti, ar nėra tiesiogiai vienas prie vieno kartografavimo vienetų skaičių ir vieneto vertės. Kurdami kintamosios atlyginimo dalies plano grynųjų pinigų plano naudojant vienetų skaičius, ši parinktis yra automatiškai užrakinta **taip**, kurių vieneto vertė yra **1.0000**.

Į **nuoma taisyklė** nustatymas leidžia jums nurodyti, ar visi darbuotojai turėtų gauti patį padidėjimo, neatsižvelgiant į datą, jos buvo išnuomotos (**nuoma taisyklė** = **nė vienas**), arba ar darbuotojai turėtų gauti apdovanojimas, kuris remiasi jų darbo ciklo metu stažą procentas (**nuoma taisyklė** = **proc**). 

**Sverto** leidžia jums reguliuoti darbuotojo apdovanojimą, pagal departamento darbuotojo našumą. Veiklos rodikliai gali būti nustatytas departamentus į **departamentų** puslapyje, kaip **susijusių formų**&gt;**kompensacijos**&gt;**veiklos**. Apdovanojimas, kad šio skyriaus darbuotojų gauti priklauso nuo vertės, **pasiekto tikslo procentas** laukas, kuriame nurodomas padalinio veiklos:

-   Jei departamento rezultatai siekia 100 procentų, to padalinio darbuotojams skiriama premija apskaičiuojama pagal procentą, nurodytą lauke** Išmoka 100 %**.
-   Jei padalinio rezultatai viršija 100 procentų, sistema prideda procentą, nurodytą lauke **Po 1 % virš tikslo**, prie procento, nurodyto lauke **Išmoka 100 %**, kol bus pasiekta lauke **Didžiausia leistina išmoka** nurodyta reikšmė.
-   Jei padalinio rezultatai nesiekia 100 procentų, sistema atima procentą, nurodytą lauke **Po 1 % žemiau tikslo**, iš procento, nurodyto lauke **Išmoka 100 %**, kol bus pasiekta lauke **Mažiausia leistina išmoka** nurodyta reikšmė.

Galite nustatyti procentų ribinių reikšmių** leistinų nuokrypių lygius**, kad pasirodytų įspėjamasis pranešimas, jei dėl sverto procentas nebepatektų į ribinių reikšmių intervalą. 

Pagal numatytuosius nustatymus sistema ieško skyriaus, kuris yra nustatytas darbuotojo pozicijos. Vis dėlto apdovanojimą už kai kurie darbuotojai gali priklausyti bei kelių skyrių veiklos. Šiuo atveju, įvairių tarnybų ir apdovanojimas, kuris priskiriamas kiekvienas padalinys veiklos dalis gali būti nustatyta ant darbuotojo kintamosios atlyginimo dalies registravimą. Norėdami gauti daugiau informacijos, žr. skiltį "kintamosios atlyginimo dalies registravimą", kad taip. 

Svertas naudojamas tik tada, jei vykdant kompensacijos procesą pasirenkama **Mokėti už rezultatus**. 

Su **lygių parametrų pakeitimus** skirtukas leidžia nepaisyti šios premijos numatytasis procentas ar vienetais, pagal darbuotojo kompensacijos lygį. Jei **įjungti pakeičia lygiai** yra lygi **taip** darbuotojams, kurie mokosi kintamosios atlyginimo dalies plano, sistema užima lygį nuo darbuotojo darbas, ir tada jos ieško lygių perrašo lentelės nustatyti, koks procentas arba skaičius už tą lygį. Jei lygis yra ne rasti lygį panaikina lentelėje, numatytasis procentas arba skaičius iš to **bendrojo** skirtukas naudojamas. Vienetų skaičius ir procentinė dalis taip pat gali būti svarbesni darbuotojo įtraukimui į kintamosios atlyginimo dalies plano.

## <a name="variable-compensation-enrollment"></a>Kintamosios atlyginimo dalies registravimas
### <a name="determine-who-is-eligible-for-the-plan"></a>Nustatykite, kas turi teisę gauti planą

Kai esate pasirengę įtraukti darbuotojus į kintamosios atlyginimo dalies planą, pirmasis žingsnis yra nuspręsti, kas turi teisę gauti plane nurodytą kompensaciją. Kol nenustatysite tinkamumo, negalėsite priskirti plano nė vienam darbuotojui. Norėdami nustatyti tinkamumą, atidarykite puslapį **Tinkamumo taisyklės**, kad sukurtumėte naują tinkamumo jūsų planui taisyklę, tada apibrėžkite kriterijus, kuriuos darbuotojas turi atitikti, kad būtų tinkamas šiam kompensacijos planui. Galite riboti tinkamumą pagal padalinį, profesinę sąjungą, kompensacijos regioną (vietą), užduotį, užduoties tipą ir (arba) kompensacijos lygį. Darbuotojai gali būti įtraukti į kompensacijos planą tik tada, jei jie atitinka **visus** kriterijus, nustatytus tinkamumo taisyklėje. 

**Pastaba:** tinkamumo taisyklės nustato teisę tiek į pastoviosios, tiek į kintamosios atlyginimo dalies planą. Tinkamumo taisyklė naudoja šiuos užduoties, pareigų ir darbuotojo įrašų laukus, kad nustatytų, ar darbuotojas turi teisę į kompensacijos planą:

-   Puslapyje **Užduotis**:
    -   Lauką **Užduotis**
    -   Laukus **Funkcija** ir **Užduoties tipas** skirtuke **Užduočių klasifikacija**
    -   Lauką **Lygis** skirtuke **Kompensacija**
-   Puslapyje **Pareigos**: laukus **Padalinys** ir **Kompensacijų regionas**
-   Dėl į **darbuotojų** puslapis: informacija apie profsąjungas, susieta su darbuotoju pagal **asmeninę informaciją**&gt;**profsąjungų** apie į *** darbuotojo *** tab

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Registracijos į kintamosios atlyginimo dalies planą leidimas

Puslapyje **Kintamosios atlyginimo dalies planai** nustatykite parinkties **Leisti registraciją** reikšmę **Taip**, kad tinkami darbuotojai galėtų būti įtraukti į planą.

### <a name="enroll-the-employee"></a>Darbuotojo įtraukimas

Dabar galite įtraukti darbuotojus į kintamosios atlyginimo dalies planą. Norėdami įtraukti darbuotoją, eikite į puslapį **Darbuotojai** ir pasirinkite darbuotoją. Tada į veiksmų sritį, spustelėkite **kompensacijos**&gt;**kintamojo planas registracijos**. 

**Pastaba:** kintamosios atlyginimo dalies plane **Registracija** turi būti nustatyta reikšmė **Taip**. Į **planas** lauke rodoma tik į tuos planus, kad darbuotojas turi teisę, atsižvelgiant į tinkamumo taisykles, nustatytas už tuos planus. Jei tinkamumo taisyklė yra ne plano, ne darbuotojai galės gauti šį planą. 

Įsitikinkite, kad į **įsigaliojimo data** laukas yra nustatytas tinkamai. Jeigu kintamosios atlyginimo dalies plano naudoja ir **kompozicinių** skaičiavimo metodas, į registracijos įsigaliojimo gali būti laikomas darbuotojo apdovanojimą skaičiavimo metu. 

Galite naudoti su **nepaiso** tab Norėdami perrašyti tam tikras reikšmes darbuotojo. Pvz., jei **nuoma taisyklė** yra lygi **procentų** planą, ir įvairių nuomos data turėtų būti naudojamas per darbuotojo nuoma procentinę dalį apskaičiuojant, galite nustatyti nuomos dienos su **samdos taisyklių data** lauke. Taip pat galite perrašyti arba į **premijos procentas** vertę arba **vienetų skaičius** vertės konkretaus darbuotojo, atsižvelgiant į plano parametrus. Šių vertybių bus atsižvelgta dar nuoma taisyklė, eksploatacines savybes ir kitus parametrus pagal planą. 

**Organizacinius pakeitimus** yra naudojami pagrindo, darbuotojo apdovanojimą bei vienas ar daugiau skyrių veiklos. Procentas yra skiriami įvairiais padaliniais reikia viso 100 procentų. Laikomas darbuotojo individualius veiklos rezultatus. Šie parametrai yra naudojami tik tada, jei **mokėti už spektaklį** yra pažymėtas, kai kompensaciją vykdymas paleidžiamas.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kompensacijų planai](compensation-plans.md)


