---
title: Kintamosios atlyginimo dalies planų kūrimas
description: Šiame straipsnyje aprašyti komponentai, kurie turi būti nustatyti prieš naudojant kintamąją atlyginimo dalį ir įtraukiant darbuotojus į kintamosios atlyginimo dalies planą.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f2f51a095a23b651dca645b14e652519f20037e2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070565"
---
# <a name="create-variable-compensation-plans"></a>Kintamosios atlyginimo dalies planų kūrimas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kintamąją atlyginimo dalį sudaro nepastovus darbuotojo darbo užmokestis, pvz., premijos ar premijų akcijos. Šiame straipsnyje paaiškinama, kaip nustatyti komponentus, reikalingus kintamajam atlyginimui, ir įtraukti darbuotoją į kintamosios atlyginimo dalies planą.

Jūsų darbuotojų kintamosios atlyginimo dalies sumų skaičiavimas gali būti paremtas į keliais veiksniais, pvz., darbuotojo rezultatais, darbuotojo kompensacijos lygiu ir padalinio rezultatais.

## <a name="variable-compensation-components"></a>Kintamosios atlyginimo dalies komponentai
### <a name="create-compensation-types"></a>kompensacijos tipų sukūrimas

**Kintamosios atlyginimo dalies tipai** yra būtinas komponentas. **Kintamosios atlyginimo dalies tipai** aprašo jūsų organizacijos teikiamas kintamosios atlyginimo dalies rūšis. Jie taip pat leidžia nurodyti, ar kompensacija bus mokama grynaisiais pinigais, ar nepinigine forma, pvz., akcijomis.

### <a name="describe-vesting-rules"></a>Paskirstymo taisyklių aprašymas

Pasirinktinai įmonės gali nustatyti **Paskirstymo taisykles**. **Paskirstymo taisyklės** aprašo, kaip per laiką turi būti paskirstyta kintamoji premija. Pavyzdžiui, paskirstymo taisyklė gali skelbti, kad darbuotojas kitus ketverius metus kiekvienais metais gaus 25 procentų nuo savo visos premijos. Paskirstymo taisyklės yra tik informacinės.

## <a name="variable-compensation-plans"></a>Kintamųjų atlyginimo dalių planai
**Kintamosios atlyginimo dalies planas** apima įtrauktų darbuotojų kintamosios atlyginimo dalies taisykles, skaičiavimo metodus ir numatytąsias skaičiavimo reikšmes. Kai kuriate kintamosios atlyginimo dalies planą, turite nustatyti kintamosios atlyginimo dalies tipą. Kintamosios atlyginimo dalies tipas nustato, ar sistema kaip premiją skaičiuoja valiutos sumą, ar vienetų skaičių. 

Apribokite **prieigą prie pasirinktų vaidmenų** parametrų apriboja prieigą prie kompensavimo plano iki pasirinktų saugos vaidmenų, kurie buvo priskirti tam personalo planui. Pavyzdžiui, kai kuriate atlyginimų planus, kurie skirti vadovams ir neturėtų būti matomi visiems personalo vaidmenims, galite naudoti šį parametrą prieigai prie šių atlyginimo planų apriboti. 

Taip pat turite nustatyti skaičiavimo metodą:

-   **Momentinis** – kintamosios premijos apskaičiavimas paremtas pastoviąja atlyginimo dalimi, kurią darbuotojas turėjo tam tikrą dieną. Ta diena nurodoma proceso įvykyje, kai apdorojamos naujos kompensacijų sumos.
-   **Sudėtinis** – apskaičiuojama premijos suma kiekvienam unikaliam pastoviosios atlyginimo dalies užmokesčio tarifui, kuris buvo taikomas darbuotojui tarp ciklo pradžios dienos ir ciklo pabaigos dienos apdorojimo įvykio metu. Tada tarifai sudedami – taip sudaroma galutinė premija. Pvz., ciklo metu darbuotojas perkeltas į kitas pareigas, kurioms taikomas skirtingas darbo užmokesčio tarifas. Tokiu atveju kintamosios dalies premija koreguojama pagal laiką, kurį darbuotojui buvo taikomas kiekvienas užmokesčio tarifas.

Kintamosios dalies premijos sumą gali sudaryti procentas nuo darbuotojo reguliaraus pagrindinio darbo užmokesčio arba nustatytas vienetų skaičius.

-   Pasirinkite parinktį **Pagrindo procentas**, kad įvestumėte numatytąjį procentą, ir nurodykite, ar pagrindas turi būti darbuotojo fiksuotas darbo užmokesčio tarifas, ar darbuotojo kompensacijos lygio kontrolinis taškas. Kompensacijos lygis nustatytas pagal darbuotojo užduotį. Vienas iš kompensacijos struktūros atskaitos taškų gali būti nustatytas kaip pastoviosios atlyginimo dalies plano kontrolinis taškas. Bus naudojamas darbuotojo užduoties kompensacijos lygis ir jis bus sutikrinamas su kontroliniu tašku, kuris įtrauktas į darbuotojo pastoviosios atlyginimo dalies planą, kad nustatytų darbuotojo kompensacijos lygio kontrolinio taško sumą. Tada kontrolinio taško suma bus naudojama vietoj darbuotojo fiksuoto darbo užmokesčio tarifo kaip premijos pagrindas.
-   Pasirinkite parinktį **Vienetų skaičius**, kad įvestumėte numatytąjį vienetų skaičių, kiekvieno vieneto vertę ir vieneto vertės valiutą, jei kompensacijos plano premija mokama ne grynaisiais pinigais (pvz., 200 akcijų, kurių kiekvienos vertė 40 USD), arba tiesiog vienetų skaičių, jei kompensacijos plano premija mokama grynaisiais pinigais. Grynaisiais pinigais mokamos premijos atveju darbuotojas gaus nurodytą skaičių vienetų valiutos, kuri naudojama jo pastoviosios atlyginimo dalies plane (pvz., 500 vienetų po 1 USD). Galima naudoti tiesioginio ryšio valdymą nurodant, ar yra tiesioginis ryšys tarp vienetų skaičiaus ir vieneto vertės. Kuriant grynaisiais pinigais pagrįstą kintamosios atlyginimo dalies planą pagal vienetų skaičių, automatiškai užfiksuojama šios parinkties reikšmė **Taip**, o vieneto vertė yra **1,0000**.

**Samdos taisyklė** nurodo, ar visi darbuotojai turi gauti tokį patį padidėjimą, neatsižvelgiant į jų pasamdymo dieną(**Samdos taisyklė**  =  **Nėra**), ar darbuotojai turi gauti procentą nuo premijos, atsižvelgiant į jų darbo trukmę per ciklą (**Samdos taisyklė** =  **Procentas**). 

**Svertas** koreguoja darbuotojo premiją pagal darbuotojo padalinio rezultatus. Kiekvieno padalinio rezultatų matavimą galima nustatyti puslapyje **Padaliniai** srityje **Susijusios formos** &gt; **Kompensacija** &gt; **Rezultatai**. Premija, kurią gauna to padalinio darbuotojai, priklauso nuo lauko **Pasiekto tikslo procentas** reikšmės, kuri rodo padalinio rezultatus.

-   Jei departamento rezultatai siekia 100 procentų, to padalinio darbuotojams skiriama premija apskaičiuojama pagal procentą, nurodytą lauke **Išmoka 100 %**.
-   Jei padalinio rezultatai viršija 100 procentų, sistema prideda procentą, nurodytą lauke **Po 1 % virš tikslo**, prie procento, nurodyto lauke **Išmoka 100 %**, kol bus pasiekta lauke **Didžiausia leistina išmoka** nurodyta reikšmė.
-   Jei padalinio rezultatai nesiekia 100 procentų, sistema atima procentą, nurodytą lauke **Po 1 % žemiau tikslo**, iš procento, nurodyto lauke **Išmoka 100 %**, kol bus pasiekta lauke **Mažiausia leistina išmoka** nurodyta reikšmė.

**Leistinų nuokrypių lygiai** gali būti nustatyti ribinių reikšmių procentinėms dalims, kad pasirodytų įspėjamasis pranešimas, jei dėl sverto procentas nebepatektų į ribinių reikšmių intervalą. 

Pagal numatytuosius parametrus padalinys, kuris priskirtas prie darbuotojo pareigų, naudojamas darbuotojo premijoms. Tačiau kai kurių darbuotojų premijos gali priklausyti nuo keleto padalinių rezultatų. Tokiu atveju skirtingus padalinius ir premijos, kuri priskiriama kiekvieno padalinio rezultatams, procentą galima nustatyti registruojant darbuotoją kintamosios atlyginimo dalies kompensacijai. Daugiau informacijos ieškokite kitame skyriuje „Kintamosios atlyginimo dalies registravimas“. 

Svertas naudojamas tik tada, jei vykdant kompensacijos procesą pasirenkama **Mokėti už rezultatus**. 

Skirtukas **Lygio nepaisymai** leidžia nepaisyti premijos numatytojo procento arba vienetų skaičiaus, priklausomai nuo darbuotojo kompensacijos lygio. Jei **Įgalinti lygių nepaisymą** nustatyta reikšmė **Taip** darbuotojams, kurie yra registruoti į kintamosios atlyginimo dalies planą, darbuotojo užduoties lygs bus palyginamas su nepaisymų lentelės lygiais, kad būtų nustatytas to lygio procentas arba vienetų skaičius. Jei lygio nepaisymų lentelėje lygio nerandama, naudojamas numatytasis procentas arba vienetų skaičius iš skirtuko **Bendra**. Procento ir vienetų skaičiaus taip pat galima nepaisyti įtraukiant darbuotoją į kintamosios atlyginimo dalies planą.

## <a name="variable-compensation-enrollment"></a>Kintamosios atlyginimo dalies registravimas
### <a name="determine-who-is-eligible-for-the-plan"></a>Nustatykite, kas turi teisę gauti planą

Kai esate pasirengę įtraukti darbuotojus į kintamosios atlyginimo dalies planą, pirmasis žingsnis yra nuspręsti, kas turi teisę gauti plane nurodytą kompensaciją. Kol nenustatysite tinkamumo, negalėsite priskirti plano nė vienam darbuotojui. Norėdami nustatyti tinkamumą, atidarykite puslapį **Tinkamumo taisyklės**, kad sukurtumėte naują tinkamumo jūsų planui taisyklę, tada apibrėžkite kriterijus, kuriuos darbuotojas turi atitikti, kad būtų tinkamas šiam kompensacijos planui. Galite riboti tinkamumą pagal padalinį, profesinę sąjungą, kompensacijos regioną (vietą), užduotį, užduoties tipą ir (arba) kompensacijos lygį. Darbuotojai gali būti įtraukti į kompensacijos planą tik tada, jei jie atitinka **visus** kriterijus, nustatytus tinkamumo taisyklėje. 

**Pastaba:** tinkamumo taisyklės nustato teisę tiek į pastoviosios, tiek į kintamosios atlyginimo dalies planą. Tinkamumo taisyklė naudoja šiuos užduoties, pareigų ir darbuotojo įrašų laukus, kad nustatytų, ar darbuotojas turi teisę į kompensacijos planą:

- Puslapyje **Užduotis**:
  -   Lauką **Užduotis**
  -   Laukus **Funkcija** ir **Užduoties tipas** skirtuke **Užduočių klasifikacija**
  -   Lauką **Lygis** skirtuke **Kompensacija**
- Puslapyje **Pareigos**: laukus **Padalinys** ir **Kompensacijų regionas**
- Puslapyje <strong>Darbuotojai</strong>: informacija apie profesines sąjungas, kurios susijusios su darbuotoju, srityje <strong>Asmeninė informacija</strong> &gt;  <strong>Profesinės sąjungos</strong> skirtuke *<strong><em>Darbuotojas</em></strong>*

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Registracijos į kintamosios atlyginimo dalies planą leidimas

Puslapyje **Kintamosios atlyginimo dalies planai** nustatykite parinkties **Leisti registraciją** reikšmę **Taip**, kad tinkami darbuotojai galėtų būti įtraukti į planą.

### <a name="enroll-the-employee"></a>Darbuotojo įtraukimas

Dabar galite įtraukti darbuotojus į kintamosios atlyginimo dalies planą. Norėdami įtraukti darbuotoją, eikite į puslapį **Darbuotojai** ir pasirinkite darbuotoją. Tada veiksmų srityje spustelėkite **Kompensacija** &gt; **Kintamosios dalies plano registracija**. 

**Pastaba:** kintamosios atlyginimo dalies plane **Registracija** turi būti nustatyta reikšmė **Taip**. Lauke **Planas** rodomi tik tie planai, kuriems darbuotojas yra tinkamas pagal tiems planams nustatytas tinkamumo taisykles. Jei planas neturi nustatytos tinkamumo taisyklės, į tokį planą negalės būti įtraukti jokie darbuotojai. 

Įsitikinkite, kad laukas **Įsigaliojimo data** nustatytas teisingai. Jei kintamosios atlyginimo dalies planas naudoja skaičiavimo metodą **Sudėtinis**, registracijos įsigaliojimo data gali būti laikoma darbuotojo premijos apskaičiavimo diena. 

Galite naudoti skirtuką **Nepaisymai**, kad nepaisytumėte konkrečių darbuotojo reikšmių. Pvz., jei plane **Samdos taisyklė** nustatyta reikšmė **Procentas**, o skaičiuojant darbuotojo samdos procentą turi būti naudojama kita samdos data, samdos datą galite nustatyti lauke **Samdos taisyklių data**. Taip pat galite nepaisyti konkretaus darbuotojo reikšmės **Premijos procentas** ar reikšmės **Vienetų skaičius**, atsižvelgiant į plano nustatymus. Samdos taisyklėje, rezultatų veiksniuose ir kituose plano nustatymuose į šias reikšmes vis tiek bus atsižvelgta. 

**Organizacijos struktūros nepaisymai** skirti nustatyti darbuotojo premiją pagal vieno ar daugiau padalinių rezultatus. Visiems padaliniams paskirstyta procentinė dalis iš viso turėtų sudaryti 100 procentų. Taip pat atsižvelgiama į individualius darbuotojo rezultatus. Šie nustatymai naudojami tik tada, jei vykdant kompensavimo procesą pažymėta parinktis **Mokėti už rezultatus**.





[!INCLUDE[footer-include](../includes/footer-banner.md)]
