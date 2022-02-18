---
title: Atostogų ir neatvykimų plano kūrimas
description: Šioje temoje aprašoma, kaip sukurti atostogų planus Dynamics 365 Human Resources įvairių rūšių atostogoms.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9267b4d4025ef0e5cec2d3e995785a6291c850e5
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070255"
---
# <a name="create-a-leave-and-absence-plan"></a>Atostogų ir neatvykimų plano kūrimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Atostogų ir neatvykimo planų, skirtų kiekvienam jūsų siūlomam atostogų tipui, nustatymas programoje „Dynamics 365 Human Resources“. Atostogų ir neatvykimų planai gali būti kaupiami skirtingu dažnumu, pvz., kas metus, kas mėnesį arba kas pusę mėnesio. Planus taip pat galima apibrėžti kaip subsidiją, kai vienas kaupimas įvyksta tam tikrą datą. Pavyzdžiui, galite sukurti planą, pagal kurį kasmet bus suteikiamos švenčių dienos.

Pakopiniai atostogų planai leidžia darbuotojams gauti išmokų, pagrįstų tuo, kiek laiko jie praleido organizacijoje. Pakopiniai planai įgalina automatinę registraciją papildomoms išmokų valandoms gauti.

Galite nurodyti maksimalią perkėlimo sumą ar minimalų likutį, siekdami užtikrinti, kad darbuotojai naudotų tik savo sukauptas išmokų valandas.

Pavyzdžiui, naudodami pakopinį planą, galite suteikti 80 valandų apmokamų atostogų (PTO) išmoką naujiems darbuotojams. Tada galite suteikti 120 valandų po 60 darbo mėnesių.

Taip pat galite kurti pareigomis grindžiamas atostogų išmokas, pvz., tik vadovams taikomas išmokų valandas.

## <a name="create-a-leave-plan"></a>Kurti atostogų planą

1. Puslapyje **Atostogų ir neatvykimų planai** pasirinkite **Kurti naują planą**.

2. Dalyje **Išsami informacija**, įveskite plano **pavadinimą**, **pradžios datą**, **aprašą** ir **atostogų tipą**.

Jei funkcija **Konfigūruoti kelis atostogų tipus, skirtus vienam atostogų ir neatvykimų planui** įjungta, atostogų tipai bus konfigūruojami skirtuke **Kaupimo grafikas**, o ne dalyje **Išsami informacija**. Galite nustatyti atostogų tipą kiekvienam kaupimo grafiko lentelės įrašui. Be to, kai ši funkcija įjungta, reikia naudoti naujus duomenų objektus, skirtus integravimams ar kitiems scenarijams, kai reikia naudoti objektus. 

Naujieji objektai:

- Atostogų ir neatvykimo banko operacija V2
- Atostogų ir neatvykimų registracijos V2
- Atostogų ir neatvykimų plano pakopos V2
- Atostogų ir neatvykimų plano V2
- Prašymo išleisti iš darbo prašymas V2

 > [!IMPORTANT]
   > Įgalinę šią funkciją, negalėsite jos išjungti.

3. Skirtuke **Kaupimai** nustatykite sukauptas sumas. Kaupimai nustato, kada ir kaip dažnai darbuotojui suteikiamos atostogos. Šiame etape nustatoma strategija, nusakanti, kada turi būti teikiami kaupimai, ir atostogų išmokų skirstymo strategija.

   1. Pasirinkite reikšmę išplečiamajame lauke **Kaupimo dažnumas**:

      - Kasdienis
      - Savaitinis
      - Kas dvi savaites
      - Kas pusę mėnesio
      - Mėnesinis
      - Kas ketvirtį
      - Kas pusmetį
      - Kasmet
      - Jokia

   2. Pasirinkite parinktį išplečiamajame lauke **Kaupimo laikotarpio pagrindas**, kad nustatytumėte pradžios datas, naudojamas kaupimo laikotarpiams apskaičiuoti:

      | Kaupimo laikotarpio pagrindas | Aprašymas |
      | --- | --- |
      | **Plano pradžios data** | Kaupimo laikotarpio pradžios data yra data, nuo kurios planas yra pasiekiamas. |
      | **Konkrečiam darbuotojui taikoma data** | Kaupimo laikotarpio pradžios data priklauso nuo darbuotojo įvykio:</br><ul><li>Pasirinktinis (turite nurodyti kiekvienos atskiros registracijos kaupimo datos pagrindą)</li><li>Jubiliejaus data</li><li>Pradinio įdarbinimo data</li><li>Paaukštinimo data</li><li>Patikslinta darbininko darbo pradžios data</li><li>Darbininko darbo pradžios data</li></ul> |

   3. Pasirinkite parinktį išplečiamajame lauke **Kaupimo premijos data**:

      - **Kaupimo laikotarpio pabaigos data** – darbuotojui bus skirtas laisvas laikas suteikimo laikotarpio paskutinę dieną. Tam, kad būtų sukaupta teisinga suma, kaupimo procesas turi apimti visą laikotarpį. Pavyzdžiui, jei kaupimo laikotarpis yra nuo 2020 m. sausio 1 d. iki 2020 m. sausio 31 d., turite vykdyti 2020 m. vasario 1 d. kaupimą, kad įtrauktumėte sausį.

      - **Kaupimo laikotarpio pradžios data** – darbuotojui bus skirtas laisvas laikas suteikimo laikotarpio pirmą dieną.

   4. Pasirinkite parinktį išplečiamajame lauke **Kaupimo strategija užregistruojant darbuotoją**. Ši vertė nurodo, kaip apskaičiuoti kaupimą, kai darbuotojas registruojamas kaupimo laikotarpio viduryje.

      - **Proporcingai paskirstytas** – datų intervalas nuo užregistravimo datos iki pradžios datos naudojamas siekiant nustatyti dienų skirtumas. Šis skirtumas taikomas, kai apdorojami kaupimai.

      - **Visas kaupimas** – visa sukaupta suma, atsižvelgiant į pakopą, skiriama pirmojo kaupimo apdorojimo metu.

      - **Nėra kaupimo** – jokio kaupimo neskiriama iki kito kaupimo laikotarpio.

   5. Pasirinkite parinktį išplečiamajame lauke **Kaupimo strategija išregistruojant darbuotoją**. Ši vertė nurodo, kaip apskaičiuoti kaupimą, kai darbuotojas išregistruojamas kaupimo laikotarpio viduryje.

      - **Proporcingai paskirstytas** – datų intervalas nuo užregistravimo datos iki pradžios datos naudojamas siekiant nustatyti dienų skirtumas. Šis skirtumas taikomas, kai apdorojami kaupimai.

      - **Visas kaupimas** – visa sukaupta suma, atsižvelgiant į pakopą, skiriama pirmojo kaupimo apdorojimo metu.

      - **Nėra kaupimo** – jokio kaupimo neskiriama iki kito kaupimo laikotarpio.

4. Nustatykite kaupimo grafiką skirtuke **Kaupimo grafikas**. Kaupimo grafikas nustato:

   - Kaip darbuotojas kaupia atostogas
   - Kokias sumas darbuotojas sukaups
   - Kokios sumos bus perkeltos

   Galite kurti pakopas, kad laisvas laikas būtų skiriamas remiantis skirtingais lygiais.

   Jeigu turite už valandinį įkainį dirbančių darbuotojų, nedarbo laiką galite skirti pagal dirbtas valandas, o ne pagal pareigų ėjimo organizacijoje trukmę. Duomenys apie dirbtas valandas paprastai saugomi laiko ir lankomumo sistemoje. Galite importuoti įprastines darbo valandas ir viršvalandžius iš laiko ir lankomumo sistemos ir naudoti jas kaip darbuotojui skiriamos premijos pagrindą.
   
    1. Pasirinkite parinktį išplečiamajame lauke **Kaupimo tipas**:

      - **Darbo mėnesiai** – kaupimo grafikas grindžiamas darbo mėnesiais.

      - **Dirbtos valandos** – kaupimo grafikas grindžiamas darbo valandomis. Daugiau informacijos apie kaupimą, grindžiamą dirbtomis valandomis, žr. skyrių [Atostogų kaupimas, grindžiamas dirbtomis valandomis](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Daugiau informacijos apie kaupimo balansą, žr. skyrių [Atostogų kaupimas, grindžiamas dirbtomis valandomis](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Įveskite vertes kaupimo grafiko lentelėje:

      - **Dirbti mėnesiai** – mažiausias mėnesių, kuriuos darbuotojas turi dirbti norėdamas įgyti teisę į kaupimus, skaičius. Jeigu jums nereikia minimalios reikšmės, nustatykite šią reikšmę kaip 0.

      - **Dirbtos valandos** – mažiausias skaičius valandų, kurias darbuotojas turi dirbti per kaupimo laikotarpį norėdamas įgyti teisę į kaupimus. Jeigu jums nereikia minimalios reikšmės, nustatykite šią reikšmę kaip 0.

      - **Kaupimo suma** – valandų ar dienų, kurias darbuotojai sukaups per laikotarpį, suma. Laikotarpis paremtas kaupimo dažnumu.

      - **Minimalus balansas** – galite naudoti neigiamą minimalaus balanso vertę, jei darbuotojams leidžiama prašyti daugiau atostogų nei jie yra sukaupę.

      - **Maksimalus perkeliamas balansas** – apdorojant kaupimą koreguojami atostogų balansai, kurie viršija maksimalų perkėlimo balansą praėjus metams nuo pradžios datos.

      - **Paskirtoji suma** – pradinis skaičių valandų ar dienų, kurios paskiriamos darbuotojui, kai jis pirmą kartą įtraukiamas į atostogų planą. Suma nekaupiama kiekvieną kaupimo laikotarpį.
      
Jei funkcija **Konfigūruoti kelis atostogų tipus, skirtus vienam atostogų ir neatvykimų planui** įjungta, pasirinkite parinktį lauke **Atostogų tipas**. 

   > [!IMPORTANT]
   > Įgalinę šią funkciją, negalėsite jos išjungti.

Jei funkcija **Naudoti visos darbo dienos ekvivalentiškumą** įjungta, „Human Resources“ naudos pareigoms nustatytą visos darbo dienos ekvivalentiškumą (FTE), kad paskirstytų darbuotojo kaupimą. Pavyzdžiui, jei FTE yra 5, o kaupimo suma yra 10, darbuotojas sukaups 5. Šią funkciją galima naudoti tik įgalinus kelis atostogų tipus.  

5. Pasirinkite **Įrašyti**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Laisvo laiko kaupimas pagal išdirbtas valandas

Jeigu turite už valandinį įkainį dirbančių darbuotojų, nedarbo laiką galite skirti pagal dirbtas valandas, o ne pagal pareigų ėjimo organizacijoje trukmę. Duomenys apie dirbtas valandas paprastai saugomi laiko ir lankomumo sistemoje. Galite importuoti įprastines darbo valandas ir viršvalandžius iš laiko ir lankomumo sistemos ir naudoti jas kaip darbuotojui skiriamos premijos pagrindą.

Pasirinkus darbo valandas kaip kaupimo tipą, galite naudoti du kaupimui naudojamų valandų tipus: įprastinės valandos ir viršvalandžiai. Atliekant kaupimo pagal dirbtas valandas planų apdorojimą, norint nustatyti kaupiamas valandas, naudojamas kaupimo dažnis kartu su kaupimo laikotarpio pagrindu.

### <a name="annual-accrual-frequency"></a>Metinis kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Mėnesio kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Pusės mėnesio kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Savaitės kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Darbuotojui priskirti atostogų planai

Darbuotojui priskirtuose atostogų planuose rodomas planų pakopos pagrindas ir dirbtų valandų planų valandų tipas. Aktyviuose planuose taip pat rodomos faktinės kaupimo laikotarpiais nuo dabartinės datos dirbtos valandos.

### <a name="loading-data"></a>Įkeliami duomenys

Faktinės valandos gali būti importuojamos duomenų valdyme naudojant objektą **Atostogos ir nebuvimo darbe valandų skaičius**. Jei naudojate darbo laiko kalendorius, importavimas patikrina, ar įprastinių dirbtų valandų skaičius neviršija kalendoriuje suplanuotų dienos valandų skaičiaus. Importavimas taip pat patikrina, ar nurodytos dienos dirbtų valandų skaičius ne didesnis negu 24 valandos. 

Norint importuoti atostogų kaupimo procese naudojamas faktines valandas, reikalinga toliau nurodyta informacija:

- Darbuotojo numeris 
- Darbo dienos data
- Tipas
- Valandos

Viena data gali turėti tik po vieną kiekvieno iš visų su ja susietų tipų pavyzdį.

| Darbuotojo numeris       | Darbo dienos data           | Tipas                  | Valandos                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Įprastas               | 8                    |       
| 000337                | 8/7/2018             | Įprastas               | 8                    |
| 000337                | 8/7/2018             | Viršvalandžiai              | 3                    |
| 000337                | 8/8/2018             | Įprastas               | 8                    |
| 000337                | 8/7/2018             | Įprastas               | 8                    |
| 000337                | 8/9/2018             | Įprastas               | 8                    |

## <a name="enrollments-and-balances"></a>Registracijos ir balansai

### <a name="enrollment-date"></a>Registracijos data

Registracijos data nurodo, kada darbuotojas gali pradėti kaupti laisvą laiką. Pvz., jei darbuotojas įtraukiamas į atostogų planą 2018 m. birželio 15 dieną, jis negali kaupti jokio laisvo laiko iki 2018 m. birželio 15 d.

### <a name="current-balance"></a>Dabartinis balansas

Esamas balansas – tai atostogų laikas, kuris yra galimas prašant laisvo laiko. Ši suma apima kaupimus, patvirtintus prašymus ir koregavimus iki dabartinės datos.

### <a name="current-balance-examples"></a>Esamo balanso pavyzdžiai

#### <a name="annual-plan"></a>Metinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Metinis            | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. sausio 1 dieną (2019-01-01), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Pageidaujama suma | Esamas balansas (2019-01-01) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Esamas balansas (160) = sukaupta suma (200) – pageidaujama suma (40)

#### <a name="semimonthly-plan"></a>Pusmėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2018 m. gegužės 1 dieną (2018-05-01), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Pageidaujama suma | Esamas balansas (2019-01-01) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Esamas balansas (22) = sukaupta suma (5 x 6) – pageidaujama suma (8)

#### <a name="monthly-plan"></a>Mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2018 m. gegužės 1 dieną (2018-05-01), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Pageidaujama suma | Esamas balansas (2019-01-01) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Esamas balansas (7) = sukaupta suma (5 x 3) – pageidaujama suma (8)

### <a name="forecasted-balance"></a>Balanso prognozė

*Prognozuojamas balansas* yra atostogų suma, kuri bus galima tam tikrą dieną ateityje. Sukauptos sumos ir perkeliamų balansų koregavimai prognozuojami iki tos datos.

„Human Resources“ naudoja šią formulę:

Prognozuojamas pirmadienio balansas = esamas balansas – prašymai + sukaupta suma – perkeliamo balanso koregavimas

### <a name="forecasted-balance-examples"></a>Prognozuojamo balanso pavyzdžiai

#### <a name="annual-plan"></a>Metinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Metinis            | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. vasario 15 dieną (2019-02-15), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Dabartinis balansas | Prognozuojamas balansas (2019-02-15) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Prognozuojamas balansas (40) = sukaupta suma (20) + esamas balansas (40) – perkeliamo balanso koregavimas (20)

#### <a name="semimonthly-plan"></a>Pusmėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. vasario 15 dieną (2019-02-15), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Dabartinis balansas | Prognozuojamas balansas (2019-02-15) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Prognozuojamas balansas (35) = sukaupta suma (5 x 3) + esamas balansas (40) – perkeliamo balanso koregavimas (20)

#### <a name="monthly-plan"></a>Mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. vasario 15 dieną (2019-02-15), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Dabartinis balansas | Prognozuojamas balansas (2019-02-15) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Prognozuojamas balansas (30) = sukaupta suma (10 x 1) + esamas balansas (40) – perkeliamo balanso koregavimas (20)

### <a name="proration-balance-examples"></a>Proporcingo paskirstymo balanso pavyzdžiai

#### <a name="prorated-monthly-plan"></a>Proporcingai paskirstytas mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mėnesinis           | Plano pradžios data      |

**Rezultatai**

| Darbuotojas            | Tarnybos mėnesiai | Registracijos data | Pradžios data | Kaupimo suma | Kaupimo apdorojimas | Likutis |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Viso kaupimo mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mėnesinis           | Plano pradžios data      |

**Rezultatai**

| Darbuotojas            | Tarnybos mėnesiai | Registracijos data | Pradžios data | Kaupimo suma | Kaupimo apdorojimas | Likutis |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>„Nėra kaupimo“ mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mėnesinis           | Plano pradžios data      |

**Rezultatai**

| Darbuotojas            | Tarnybos mėnesiai | Registracijos data | Pradžios data | Kaupimo suma | Kaupimo apdorojimas | Likutis |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)
- [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md)
- [Atostogų ir neatvykimų kaupimo planai](hr-leave-and-absence-accrue.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
