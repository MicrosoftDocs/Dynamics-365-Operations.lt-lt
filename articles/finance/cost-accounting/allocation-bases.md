---
title: Paskirstymo bazės
description: Šiame straipsnyje pateikiama informacija apie paskirstymo bazes. Paskirstymo bazės yra pagrindiniai kaštų apskaitos komponentai ir dažniausiai naudojami paskirstant pridėtines išlaidas.
author: AndersGirke
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMAllocationBaseDetail, CAMFormulaAllocationBaseDetail, CAMAllocationBasePreview, CAMAllocationBase, CAMCostAllocationRule, CAMPredefinedMemberAllocationBase
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223174
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 138a1a101610fc0f18ef3d8d2d3d336e5a48a1da
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894090"
---
# <a name="allocation-bases"></a>Paskirstymo bazės 

[!include [banner](../includes/banner.md)]

Paskirstymo bazė yra pagrindas, kuriuo remdamasi kaštų apskaita paskirsto pridėtines išlaidas. Paskirstymo bazė gali būti tam tikras kiekis, pvz., mašinos darbo valandų skaičius, suvartotų kilovatvalandžių (kWh) skaičius, užimamas plotas kvadratinėmis pėdomis. Paskirstymo bazės dažniausiai naudojamos sukuriamoms atsargoms priskiriant pridėtines išlaidas. Pvz., IT skyrius paskirsto išlaidas pagal kiekviename skyriuje naudojamų kompiuterių skaičių.

Yra trijų tipų kaštų apskaitos paskirstymo bazės:

- Iš anksto nustatytos dimensijos nario paskirstymo bazės
- Hierarchijos paskirstymo bazės
- Formulės paskirstymo bazės

## <a name="predefined-dimension-member-allocation-bases"></a>Iš anksto nustatytos dimensijos nario paskirstymo bazės

Iš anksto nustatytos dimensijų narių paskirstymo bazės sukuriamos automatiškai, kai sukuriamas vieno iš toliau nurodytų tipų dimensijos narys.

- Statistinės dimensijos nariai
- Savikainos elemento dimensijos nariai

> [!NOTE]
> Savikainos elemento dimensijos nario pagrindu sudarytos iš anksto nustatytos dimensijų narių paskirstymo bazės atsižvelgia tik į duomenų šaltinio tiekėjo, pvz., didžiosios knygos arba biudžeto pateiktas reikšmes.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>1 pavyzdys: kaip paskirstymo bazę naudokite savikainos elemento dimensijos narį
Šiame pavyzdyje nurodoma, kaip sukurti savikainos paskirstymo taisyklę, kad savikainos elementą 10002 (darbuotojo draudimą) būtų galima paskirti į savikainos elementą 10001 (atlyginimai) įrašomam likučiui. Paskirstymo taisyklė nustatoma pagal kiekvieno skyriaus atlyginimų ir bendros atlyginimų sumos koeficientą. (Būtina peržiūrėti!)

DK sąskaitų planas nurodomas toliau paaiškintu būdu.

| Sąskaitų planas | Korespondentinė sąskaita, subsąskaita | aprašymas        | Pagrindinės sąskaitos tipas |
|------------------|--------------|--------------------|-------------------|
| Bendrai naudojama           | 10001        | Atlyginimai           | Išlaidos           |
| Bendrai naudojama           | 10002        | Darbuotojo draudimas | Išlaidos           |

Nurodykite savikainos elemento dimensiją ir sukonfigūruokite duomenų jungtį. Importavus duomenis kaštų apskaitoje sukuriami toliau nurodyti įrašai.

**Savikainos elemento dimensijos nariai**

| Savikainos elemento dimensijos pavadinimas | Savikainos elementas |  aprašymas       | Tipas    |
|-----------------------------|--------------|--------------------|---------|
| Savikainos elementai               | 10001        | Atlyginimai           | Pagrindinis |
| Savikainos elementai               | 10002        | Darbuotojo draudimas | Pagrindinis |

**Iš anksto nustatytos dimensijos nario paskirstymo bazės** 

| Vardas  | aprašymas        | Savikainos elemento dimensija |
|-------|--------------------|------------------------|
| 10001 | Atlyginimai           | Savikainos elementai          |
| 10002 | Darbuotojo draudimas | Savikainos elementai          |

Didžiojoje knygoje užregistruoti toliau nurodyti įrašai.

- Įrašus, kuriuose nurodoma pagrindinė atlyginimų sąskaita, pateikia algalapio sistema ir jie užregistruojami išlaidų centruose.
- Darbuotojo draudimo išlaidos neautomatiniu būdu užregistruojamos numatytajame išlaidų centre.

| Ataskaitinė data | Išlaidų centras |  aprašymas        | Korespondentinė sąskaita, subsąskaita |  aprašymas       | Suma, išreikšta apskaitos valiuta |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 2017-01-03      | CC001       | Personalas                  | 10001        | Atlyginimai           | 2,000.00                      |
| 2017-01-03      | CC002       | FI                  | 10001        | Atlyginimai           | 5 000,00                      |
| 2017-01-03      | CC003       | AP                  | 10001        | Atlyginimai           | 3 000,00                      |
| 2017-01-03      | CC099       | Numatytasis išlaidų centras | 10002        | Darbuotojo draudimas | 1000,00                      |

Apdorojus didžiosios knygos šaltinio duomenis kaštų apskaitoje sukuriami toliau nurodyti įrašai.

**Savikainos įrašai**

| Išlaidų objektas |  aprašymas        | Savikainos elementas  |  aprašymas       | Savikainos veikimo būdas   |Suma|Ataskaitinė data|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | Personalas                  | 10001         | Atlyginimai           | Nesuklasifikuota    |2,000.00|  2017-01-03    |
| CC002       | FI                  | 10001         | Atlyginimai           | Nesuklasifikuota    |5 000,00|     2017-01-03         |
| CC003       | AP                  | 10001         | Atlyginimai           | Nesuklasifikuota    |3 000,00|      2017-01-03        |
| CC099       | Numatytasis išlaidų centras | 10002         | Darbuotojo draudimas | Nesuklasifikuota    |1000,00|      2017-01-03       |

Šiame supaprastintame pavyzdyje sukuriama išlaidų paskirstymo taisyklė, kad būtų galima paskirti su į savikainos elementą 10001 (atlyginimai) įrašomu likučiu susijusį savikainos elementą 10002 (darbuotojo draudimas).

**Savikainos paskirstymo taisyklė**

| Savikainos objekto dimensijų hierarchijos mazgas | Savikainos elemento dimensijų hierarchijos mazgas | Savikainos veikimo būdas | Paskirstymo bazė |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Nesuklasifikuota  | 10001           |

**Atlikti pridėtinių išlaidų skaičiavimą**

Savikainos elementą 10001 (atlyginimai) pritaikius kaip paskirstymo bazę pridėtinių išlaidų skaičiavimo rezultatas yra toks.

| Išlaidų objektas | aprašymas | Reikšmė |   Paskirstymo koeficientas         | Suma |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | Personalas          | 2 000     | (2 000 ÷ 10 000) × 1 000,00 | 200,00 |
| CC002       | FI          | 5 000     | (5 000 ÷ 10 000) × 1 000,00 | 500,00 |
| CC003       | AP          | 3.000     | (3 000 ÷ 10 000) × 1 000,00 | 300,00 |

**Žurnalas**

| Žurnalas | Žurnalo tipas                          | Ataskaitinis kalendorinis laikotarpis | Metai | Laikotarpis   | Versija                                                                 |
|---------|---------------------------------------|------------------------|------|----------|---------------------------------------------|
| 00001   | Išlaidų paskirstymo skaičiavimo žurnalas | Finansiniai                 | 2017 | 1 laikotarpis | Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis |

**Savikainos objekto likučio žurnalo įrašai**

| Ataskaitinė data | Išlaidų objektas | aprašymas         | Savikainos elementas | aprašymas        | Savikainos veikimo būdas |  Suma  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 2017-01-31      | CC099       | Numatytasis išlaidų centras | 10002        | Darbuotojo draudimas | Nesuklasifikuota  | 1000,00 |

**Savikainos įrašai**

| Išlaidų objektas |  aprašymas        | Savikainos elementas |    aprašymas     | Savikainos veikimo būdas | Suma    | Ataskaitinė data |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Numatytasis išlaidų centras | 10002        | Darbuotojo draudimas | Nesuklasifikuota  | -1,000.00 | 2017-01-31      |
| CC001       | Personalas                  | 10002        | Darbuotojo draudimas | Nesuklasifikuota  | 200,00    | 2017-01-31      |
| CC002       | FI                  | 10002        | Darbuotojo draudimas | Nesuklasifikuota  | 500,00    | 2017-01-31      |
| CC099       | AP                  | 10002        | Darbuotojo draudimas | Nesuklasifikuota  | 300,00    | 2017-01-31      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>2 pavyzdys: kaip paskirstymo bazę naudokite statistinės dimensijos narį

Statistinės dimensijos narius galima naudoti kaip paskirstymo bazes nustatant strategijas ar pranešant apie nepinigines sąnaudas pagal savikainos objektus. Statistinės dimensijos narius galite kurti rankiniu būdu arba importuoti juos iš failo naudodami duomenų importavimo / eksportavimo valdymo įrankį.

**Statistinės dimensijos nariai**

| Statistinės dimensijos pavadinimas | Statistinis elementas | aprašymas               | Vienetas |
|----------------------------|---------------------|---------------------------|------|
| Statistiniai elementai       | FTE                 | Darbuotojai, dirbantys visą darbo dieną       | Vnt.   |
| Statistiniai elementai       | Elektros energija         | Elektros energijos suvartojimas   | kwh  |

Įrašius statistinės dimensijos narį iš anksto nustatytose dimensijų narių paskirstymo bazėse sukuriamas atitinkamas įrašas.

**Iš anksto nustatytos dimensijos nario paskirstymo bazės**

| Vardas        | aprašymas             | Statistinio elemento dimensija |
|-------------|-------------------------|-------------------------------|
| FTE         | Darbuotojai, dirbantys visą darbo dieną     | Statistiniai elementai          |
| Elektros energija | Elektros energijos suvartojimas | Statistiniai elementai          |

Statistinės priemonės gali būti paimtos iš įvairių šaltinių:

- Elektros energijos suvartojimas gali būti matuojamas naudojant įvairiose įmonės vietose įrengtus skaitiklius.
- Lentelėse nurodomos statistinės priemonės. Pavyzdžiui, lentelėje HcmEmployment pateikiamas visų darbuotojų ir išlaidų centrų, kuriuose jie dirba, sąrašas.

| Vardas       | Išlaidų centras |  aprašymas  | Darbininko tipas |
|------------|-------------|----|-------------|
| Darbuotojas A | CC001       | Personalas | Darbuotojas    |
| Darbuotojas B | CC002       | FI | Darbuotojas    |
| Darbuotojas C | CC002       | FI | Darbuotojas    |
| Darbuotojas D | CC003       | AP | Darbuotojas    |
| Darbuotojas F | CC003       | AP | Darbuotojas    |

> [!NOTE]
> Visas lenteles, kuriose nurodomos finansinės dimensijos, galima naudoti kaip statistinių priemonių šaltinius.

Naudodama toliau nurodytus duomenų ryšius kaštų apskaita palaiko statistinių priemonių rinkinį.

- Duomenų importavimo / eksportavimo valdymo įrankis
- Statistinės priemonės

Norint gauti statistines priemones iš sistemos, būtinas statistinės priemonės teikimo įrankio šablonas. Norėdami gauti daugiau informacijos, žr. statistinių priemonių teikimo įrankio šabloną. (Kai bus įrašytas šis straipsnis, bus įrašytas saitas.)

**Statistinės priemonės teikimo įrankio šablonai**

| Vardas  | Funkcija | Šaltinio lentelė  | Sumos laukas      | Datos laukas     |
|-------|----------|---------------|----------------|----------------|
| FTE | Skaič.    | HcmEmployment | Netaikoma | Netaikoma |

Apdorojus statistinės priemonės šaltinio duomenis kaštų apskaitoje bus sukurti toliau nurodyti įrašai.

**Statistiniai įrašai**

| Išlaidų objektas | aprašymas      | Ataskaitinė data | Statistinės dimensijos narys | aprašymas         | Reikšmė |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personalas               | 2017-01-31      | FTE                        | Darbuotojai, dirbantys visą darbo dieną | 1,00      |
| CC002       | FI               | 2017-01-31      | FTE                        | Darbuotojai, dirbantys visą darbo dieną | 2,00      |
| CC003       | AP               | 2017-01-31      | FTE                        | Darbuotojai, dirbantys visą darbo dieną | 2,00      |

Toliau pateikiamas išlaidų paskirstymo taisyklės pavyzdys, kai FTE iš anksto nustatyta dimensijos nario paskirstymo bazė priskiriama kaip paskirstymo bazė.

| Išlaidų objektas | aprašymas  | Reikšmė | Paskirstymo koeficientas |
|-------------|------|-----------|-------------------|
| CC001       | Personalas   | 1,00      | (1/5) × suma    |
| CC002       | FI   | 2,00      | (2/5) × suma    |
| CC003       | AP   | 2,00      | (2/5) × suma    |

Importuotų statistinių priemonių duomenų objektą galite naudoti norėdami importuoti statistines priemones į kaštų apskaitą. Taip pat galite naudoti duomenų importavimo / eksportavimo valdymo įrankį. Programoje „Excel“ elektros energijos suvartojimas įrašomas toliau nurodytu būdu.

| Ataskaitinė data | Dimensijos narys | Reikšmė | Šaltinio identifikatorius |
|-----------------|------------------|-----------|-------------------|
| 2017-01-31      | CC001            | 2,450.00  | Elektros energija       |
| 2017-01-31      | CC002            | 4,100.00  | Elektros energija       |
| 2017-01-31      | CC003            | 15,000.00 | Elektros energija       |

Apdorojus statistinės priemonės šaltinio duomenis kaštų apskaitoje bus sukurti toliau nurodyti įrašai.

**Statistiniai įrašai**

| Išlaidų objektas | Pavadinimas / vardas ir (arba) pavardė   | Apskaitos data | Statistinės dimensijos narys |    aprašymas          | Reikšmė |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personalas | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 2,450.00  |
| CC002       | FI | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 4,100.00  |
| CC003       | AP | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 15,000.00 |

Toliau pateikiamas išlaidų paskirstymo taisyklės pavyzdys, kai iš anksto nustatyta elektros energijos dimensijos nario paskirstymo bazė priskiriama kaip paskirstymo bazė.

| Išlaidų objektas | aprašymas  | Reikšmė | Paskirstymo koeficientas          |
|-------------|------|-----------|----------------------------|
| CC001       | Personalas   | 2,450.00  | (2 450 ÷ 21 550) × suma  |
| CC002       | FI   | 4,100.00  | (4 100 ÷ 21 550) × suma  |
| CC003       | AP   | 15,000.00 | (15 000 ÷ 21 550) × suma |

## <a name="hierarchy-allocation-bases"></a>Hierarchijos paskirstymo bazės

Pritaikydami išlaidų objekto dimensijų hierarchijos mazgą esamai paskirstymo bazei išlaidų buhalteriai gali rankiniu būdu sukurti hierarchijos paskirstymo bazes. Tokiu būdu galite apriboti pradinės iš anksto nustatytos dimensijos nario paskirstymo bazės diapazoną. Vieną iš anksto nustatytą dimensijos nario paskirstymo bazę galima naudoti kuriant kelias hierarchijos paskirstymo bazes. Diapazonai gali būti išlaikomi ir su hierarchijos paskirstymo baze susietoje išlaidų objekto dimensijos hierarchijoje.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Pavyzdys: hierarchijos paskirstymo bazės pagal visą dieną organizacijoje dirbančius darbuotojus
Toliau pateikiamas išlaidų objekto dimensijos hierarchijos, kurią galima sukurti norint aprašyti supaprastintą organizaciją, pavyzdys.

| Hierarchijos pavadinimas | Mazgo lygis 0 | Mazgo lygis 1 | Mazgo lygis 2 | Dimensijos nariai |
|----------------|--------------|--------------|--------------|-------------------|
| Organizacija   | Vadovas          | CFO          | FICO         | CC001             |
| Organizacija   | Vadovas          | CFO          | Personalas           | CC002             |
| Organizacija   | Vadovas          | TS          | AP           | CC003             |

FTE iš anksto nustatytoje dimensijos nario paskirstymo bazėje, kuri buvo sukurta ankstesniame skyriuje, pateikiami toliau nurodyti įrašai.

**Statistiniai įrašai**

| Išlaidų objektas | aprašymas  | Ataskaitinė data | Statistinės dimensijos narys | aprašymas | Reikšmė |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personalas   | 2017-01-31      | FTE                        | Darbuotojai, dirbantys visą darbo dieną | 1,00      |
| CC002       | FI   | 2017-01-31      | FTE                        | Darbuotojai, dirbantys visą darbo dieną | 2,00      |
| CC003       | AP   | 2017-01-31      | FTE                        | Darbuotojai, dirbantys visą darbo dieną | 2,00      |

Išlaidos turi būti paskirstytos organizacijos vyriausiajam finansininkui (CFO) ataskaitingiems išlaidų centrams. Pripažįstama, kad teisingas paskirstymo koeficientas yra visą dieną dirbančių darbuotojų (FTE) skaičius pagal išlaidų centrą.

**Hierarchijos paskirstymo bazės**

| Vardas                  | Paskirstymo bazė | Savikainos objekto dimensijų hierarchija | Savikainos objekto dimensijų hierarchijos mazgas |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| CFO dirbančių FTE skaičius | FTE           | Organizacija                    | CFO                                  |

Naudodamiesi peržiūros funkcija galite patikrinti sukurtą hierarchijos paskirstymo bazę pagal statistinius įrašus sistemoje.

**Paskirstymo bazės informacija**

| Išlaidų objektas | aprašymas  |  Reikšmė |
|-------------|------|------------|
| CC001       | Personalas   | 1,00       |
| CC002       | FI   | 2,00       |

Toliau pateikiamas išlaidų paskirstymo taisyklės pavyzdys, kai CFO hierarchijos paskirstymo bazės FTE skaičius priskiriamas kaip paskirstymo bazė.

| Išlaidų objektas | aprašymas  | Reikšmė | Paskirstymo koeficientas |
|-------------|------|-----------|-------------------|
| CC001       | Personalas   | 1,00      | (1/3) × suma    |
| CC002       | FI   | 2,00      | (2/3) × suma    |

## <a name="formula-allocation-bases"></a>Formulės paskirstymo bazės

Naudodami formulės paskirstymo bazes galite nustatyti išplėstines formules, kad sukurtumėte teisingą paskirstymo bazę. Formulės paskirstymo bazes galite sukurti rankiniu būdu.

Kai kuriate formulės paskirstymo bazę, pasirenkate, kuri statistinė dimensija ir išlaidų elemento dimensija turėtų būti formulės bazė. Iš pirmiau pasirinktų dimensijų gautas paskirstymo bazes galima naudoti formulės paskirstymo bazėje.

> [!NOTE]
> Pirmiau nustatytas formulės paskirstymo bazes galima naudoti norint apibrėžti naują formulės paskirstymo bazę.

Kurdami formulės paskirstymo bazės koeficientus kuriate pseudonimą ir susiejate jį su paskirstymo baze arba konstanta. Po to šie pseudonimai naudojami nurodant formulę.

Norėdami nurodyti savo formulę, galite naudoti toliau nurodytus operatorius.

| Simboliai | Tekstas           |
|---------|----------------|
| ( )     | Skliausteliai    |
| \<      | Mažiau negu   |
| \>      | Daugiau negu    |
| +       | Priedas       |
| –       | Atimtis    |
| \*      | Daugyba |

Tradiciniai **IF** (jeigu) sakiniai nepalaikomi. Tačiau galite sukurti sakinius ir patikrinti, ar jie teisingi.

| Sakinys | Tikrinimas | Rezultatas |
|-----------|------------|--------|
| a \> b    | Teisinga       | 1      |
| a \> b    | Netinkama      | 0      |

### <a name="example-1-a-simple-formula"></a>1 pavyzdys: paprasta formulė

Sąskaitos už suvartotą elektros energiją dažnai sudarytos iš dviejų dalių:

- Fiksuotas mokestis už prisijungimą prie tinklelio
- Išlaidos, susijusios su suvartojimu pagal kWh

Iš anksto nustatyta elektros energijos dimensijos nario paskirstymo bazė jau nurodyta ir joje pateikiamos toliau išvardytos reikšmės.

**Statistiniai įrašai**

| Išlaidų objektas | Vardas | Ataskaitinė data | Statistinės dimensijos narys | aprašymas             | Reikšmė |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personalas   | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 2,450.00  |
| CC002       | FI   | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 4,100.00  |
| CC003       | AP   | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 15,000.00 |

Jei fiksuotas mokestis dabar turi būti tolygiai paskirstytas elektros energiją vartojantiems išlaidų objektams, paskirstydami išlaidas turite dvi galimybes:

- Sukurti naują iš anksto nustatytą fiksuotos elektros energijos paskirstymo bazę, o po to kiekvienam elektros energiją vartojusiam išlaidų objektui taikyti statistinę priemonę 1,00.
- Sukurti fiksuotos elektros energijos formulės paskirstymo bazę, kuri naudotųsi jau sistemoje nurodyta iš anksto nustatyta elektros energijos paskirstymo baze. Ši parinktis naudinga tuo, kad į kaštų apskaitą turi būti įkeliami tik vieno elektros energijos statistinės dimensijos nario duomenys.

**Formulės paskirstymo bazė** 

| Vardas              | Savikainos elemento dimensija | Statistinė dimensija | Formulė |
|-------------------|------------------------|-----------------------|---------|
| Fiksuota elektros energija |                        | Statistiniai elementai  |         |

Prieš užpildydami laukelį **Formulė** turite nurodyti formulėje naudotiną pseudonimą.

**Formulės paskirstymo bazės koeficientai**

| Pseudonimas | Pastovus | Paskirstymo bazė |
|-------|----------|-----------------|
| a     |          | Elektros energija     |
| b     | 0,01     |                 |

Atkreipkite dėmesį, kad kaip konstanta 0 (nulis) nepalaikomas.

**Formulės paskirstymo bazė**

| Vardas              | Savikainos elemento dimensija | Statistinė dimensija | Formulė |
|-------------------|------------------------|-----------------------|---------|
| Fiksuota elektros energija |                        | Statistiniai elementai  | a \> b  |

Naudodamiesi peržiūros funkcija galite patikrinti sukurtą formulės paskirstymo bazę pagal statistinius įrašus sistemoje.

**Paskirstymo bazės informacija**

| Išlaidų objektas | aprašymas  | Formulė           | Reikšmė |
|-------------|------|-------------------|-----------|
| CC001       | Personalas   | 2 450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4 100,00 \> 0,01  | 1,00      |
| CC003       | AP   | 15 000,00 \> 0,01 | 1,00      |

Toliau pateikiamas išlaidų paskirstymo taisyklės pavyzdys, kai elektros energijos formulės paskirstymo bazė priskiriama kaip paskirstymo bazė.

**Išlaidų objektų dydžio paskirstymo koeficientas**

| Išlaidų objektas | Vardas | Reikšmė |  Paskirstymo koeficientas |
|-------------|------|-----------|--------------------|
| CC001       | Personalas   | 1,00      | (1/3) × suma     |
| CC002       | FI   | 1,00      | (1/3) × suma     |
| CC003       | AP   | 1,00      | (1/3) × suma     |

### <a name="example-2-an-advanced-formula"></a>2 pavyzdys: išplėstinė formulė
Šiame pavyzdyje išlaidos už suvartotą elektros energiją turėtų būti apskaičiuotos ne tik pagal faktines elektros sąnaudas kWh. Vadovybė nori įgyvendinti mažesnį elektros energijos vartojimą skatinančią iniciatyvą. 

| Taisyklė              | Tarifas | 
|-------------------|------|
| a <= 10000,00 kWh | 0.75 |
| a > 10000,00 kWh  | 1.15 |

Sukuriama nauja elektros energijos suvartojimo formulės paskirstymo bazė.

**Formulės paskirstymo bazė**

| Vardas              | Savikainos elemento dimensija | Statistinė dimensija | Formulė |
|-------------------|------------------------|-----------------------|---------|
| Elektros energijos suvartojimas |                        | Statistiniai elementai  |         |

Prieš užpildydami laukelį **Formulė** turite nurodyti formulėje naudotiną pseudonimą.

**Formulės paskirstymo bazės koeficientai**

| Pseudonimas | Pastovus  | Paskirstymo bazė |
|-------|-----------|-----------------|
| a     |           | Elektros energija     |
| b     | 10.000,00 |                 |
| c     | 0.75      |                 |
| d     | 1.15      |                 |

**Formulės paskirstymo bazė**

| Vardas              | Savikainos elemento dimensija | Statistinė dimensija | Formulė                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Fiksuota elektros energija |                        | Statistiniai elementai  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Naudodamiesi peržiūros funkcija galite patikrinti sukurtą formulės paskirstymo bazę pagal statistinius įrašus sistemoje.

**Paskirstymo bazės informacija**

| Išlaidų objektas |  Pavadinimas / vardas ir (arba) pavardė  | Formulė                                                                                                                             | Reikšmė |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | HR | ((2 450,00 \> 10 000,00) × ((10 000,00 × 0,75) + (2 450,00 – 10 000,00) × 1,15)) + ((2 450,00 \<= 10 000,00) × 2 450,00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4 100,00 \> 10 000,00) × ((10 000,00 × 0,75) + (4 100,00 – 10 000,00) × 1,15)) + ((4 100,00 \<= 10 000,00) × 4 100,00 × 0,75)     | 3,075.00  |
| CC003       | AP | ((15 000,00 \> 10 000,00) × ((10 000,00 × 0,75) + (15 000,00 – 10 000,00) × 1,15)) + ((15 000,00 \<= 10 000,00) × 15 000,00 × 0,75) | 1,3250.00 |

Įdėmiau panagrinėkime CC003 (IT) formulę:

((15 000,00 \> 10 000,00) × ((10 000,00 × 0,75) + (15 000,00 – 10 000,00) × 1,15)) + ((15 000,00 \<= 10 000,00) × 15 000,00 × 0,75) = 13 250,00

(1 × (7 500,00 + 5 000,00 × 1,15)) + (0 × 15 000,00 × 0,75)            

1 × 7 500,00 + 5 750,00 + 0 

Toliau pateikiamas išlaidų paskirstymo taisyklės pavyzdys, kai fiksuota elektros energijos formulės paskirstymo bazė priskiriama kaip paskirstymo bazė.


| Išlaidų objektas | aprašymas | Reikšmė |        Paskirstymo koeficientas         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     Personalas      | 1,837.50  | (1 837,50 ÷ 18 162,50) × suma  |
|    CC002    |     FI      | 3,075.00  | (3 075,00 ÷ 18 162,50) × suma  |
|    CC003    |     AP      | 13,250.00 | (13 250,00 ÷ 18 162,50) × suma |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
