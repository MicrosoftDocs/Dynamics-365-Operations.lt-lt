---
title: Išmokų plano kūrimas
description: Nustatykite išmokų planus programoje „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bcbf4c1a7f136e5563bf1210b6c09228dad95dea
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429256"
---
# <a name="create-a-benefits-plan"></a>Išmokų plano kūrimas

Šiame straipsnyje pateikiama, kaip nustatyti išmokų planus programoje „Dynamics 365 Human Resources“.

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Išmokų planai**.

2. Pasirinkite **Naujas**.

3. Skirtuke **Bendra** įveskite šių laukų reikšmes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Planas.** | Unikalus plano identifikatorius. |
   | **Aprašymas** | Plano aprašas. |
   | **Plano tipas** | Sukūrę naują planą turite nurodyti plano tipą. Plano tipas yra konkrečių išmokų tipų aukščiausio lygio grupavimas. Kiekvienas plano tipas nurodo, ar darbuotojas gali registruotis į kelis to tipo planus, nurodo, ar kontaktai yra gavėjai ar priklausomieji, ir apibrėžia draudimo parinktis. Galite kurti naujus pasirinktinius plano tipus, kad būtų patenkinti jūsų išmokų pasiūlymų poreikiai. Pagrindiniai išmokų planų tipai yra tokie: <ul><li>401 000</li><li>ADD</li><li>Odontologija</li><li>„Fitness“</li><li>FSA</li><li>Gyvenimas</li><li>LTD</li><li>Sveikata</li><li>PTO</li><li>STD</li><li>Vizija</li></ul> |
   | **Plano tipo kodas** | Plano tipo plano tipo kodas. |
   | **Programa** | Nurodo programą, kuriai pasirinktinai priskiriamas planas. |
   | **Grupavimas** | Nurodo grupavimą, kuriam pasirinktinai priskiriamas planas. |
   | **Meistras** | Nurodo, ar planas yra pagrindinis planas, esantis jam priskirtame grupavime. |
   | **Būsena** | Rodoma dabartinė išmokų plano būsena. Numatytoji reikšmė yra Aktyvusis. Pakeitus būseną į Neaktyvusis, plane nebus galima pasirinkti per registraciją. |
   | **Galiojimo pradžios data ir laikas** | Plano pradžios data ir laikas. Numatytoji vertė yra dabartinė sistemos data. |
   | **Galiojimo pabaigos data ir laikas** | Plano pabaigos data ir laikas (būsena nustatyta kaip Neaktyvusis). Numatytoji reikšmė yra 2154-12-31, kuri reiškia, kad niekada. |

4. Skirtuke **Konfigūracija** nurodykite šių laukų vertes, atsižvelgdami į kuriamo plano tipą:

   | Plano tipas | Laukas | Aprašymas |
   | --- | --- | --- |
   | Sveikatos priežiūra (sveikatos, dantų, regos, HMO) | COBRA | Nurodo, ar planas yra tinkamas, remiantis COBRA (konsoliduotojo bendrojo biudžeto derinimo įstatymu). |
   | Sveikatos priežiūra (sveikatos, dantų, regos, HMO) | HIPAA | Nurodo, ar planas yra tinkamas, remiantis HIPAA (sveikatos draudimo portatyvumo ir atskaitomybės aktu). |
   | <ul><li>Sveikatos priežiūra (sveikatos, dantų, regos, HMO)</li><li>Kita (PTO, „Fitness“)</li><li>Kitos</li><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li><li>Santaupos (pvz., „401 (k)“)</li><li>FSA</li></ul> | Prieš skaičiuojant mokesčius tinkamas | Nurodo, ar, prieš taikant mokesčius, galima į planą mokėti įnašus. |
   | <ul><li>Sveikatos priežiūra (sveikatos, dantų, regos, HMO)</li><li>Kita (PTO, „Fitness“)</li><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li><li>Santaupos (pvz., „401 (k)“)</li><li>FSA</li></ul> | Registruoti tinkamą mokestį | Nurodo, ar, pritaikius mokesčius, galima į planą mokėti įnašus. |
   | <ul><li>Sveikatos priežiūra (sveikatos, dantų, regos, HMO)</li><li>Kita (PTO, „Fitness“)</li><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li><li>Santaupos (pvz., „401 (k)“)</li><li>FSA</li></ul> | Bendraautorius | Nurodo, kas įneša į planą – darbuotojai, darbdaviai arba abi grupės. |
   | <ul><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li></ul> | Minimalus padengimas | Mažiausia draudimo suma, būtina planui. |
   | <ul><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li></ul> | Maksimalus padengimas | Didžiausia draudimo suma, būtina planui. |
   | <ul><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li></ul> | Naudoti padengimo didinimą | Nurodo, ar patvirtinti, kad draudimo suma atitinka tinkamą papildančiąją sumą. |
   | <ul><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li></ul> | Papildančioji suma | Papildančioji draudimo suma, būtina planui. Pavyzdžiui, jei papildančioji suma yra 1 000, darbuotojui negali būti 200 500 $ draudimo suma, jis turėtų apvalinti iki 201 000 $ arba sumažinti iki 200 000 $. |
   | <ul><li>Ilgalaikė negalia</li><li>ADD („Basic life“, „Voluntary life“)</li></ul> | Papildančioji kryptis | Nurodo, kaip apvalinti (į didžiąją arba mažąją pusę), kai padengimo suma neatitinka papildomosios sumos vertės. |
   | ADD („Basic life“, „Voluntary life“) | Draudžiamumo įrodymai | Nurodo, ar darbuotojas turi pateikti draudžiamumo įrodymą. |
   | ADD („Basic life“, „Voluntary life“) | Suma | Suma apskaitos valiuta. Šis laukas aktyvus tik tada, jei pažymėtas žymės langelis Draudžiamumo įrodymai. |
   | <ul><li>Santaupos (pvz., „401 (k)“)</li><li>FSA</li></ul> | Mažiausias metinis įnašas | Mažiausia įnašo suma, būtina planui. |
   | <ul><li>Santaupos (pvz., „401 (k)“)</li><li>FSA</li></ul> | Didžiausias metinis įnašas | Didžiausia įnašo suma, būtina planui. |
   | Santaupos (pvz., „401 (k)“) | Darbdavio maksimali metinė suma | Didžiausia suma, kurią darbdavys gali įnešti į darbuotojo santaupų planą išmokos laikotarpiu. Norėdami naudoti šį lauką, turite pažymėti žymės langelį Darbdavio atitiktis. |
   | Santaupos (pvz., „401 (k)“) | Darbdavio atitiktis | Nurodo, ar darbdavys įneša į darbuotojo santaupų planą. |
   | Santaupos (pvz., „401 (k)“) | Darbdavio atitikties procentinė dalis | Darbuotojo įnašo, kurį turi atitikti darbdavys, procentinė dalis. |
   | Santaupos (pvz., „401 (k)“) | Darbdavio atitikties viršutinė riba | Didžiausia procentinė dalis, kurią atitiks darbdavys. Pavyzdžiui, jei darbdavys atitiks 100 % darbuotojo įmokų iki 6 % nuo darbuotojo atlyginimo, darbdavio atitikties viršutinė riba yra 6 %. |

5. Skirtuke **Sąranka** įveskite šių laukų reikšmes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Leisti / tęsti registraciją** | Nurodo, ar darbuotojai gali registruotis į planą, jei jie atitinka tinkamumo reikalavimus.</br></br>Jei tai nustatyta kaip Ne, planas nebus pasiekiamas darbuotojams, kai apdorojate tinkamumą. |
   | **Automatinė registracija iš ankstesnių metų** | Nurodo, ar automatiškai įtraukti į planą reikalavimus atitinkantį darbuotoją, jei jis buvo įtrauktas praėjusiais metais. |
   | **Automatinė registracija pagal numatytuosius nustatymus** | Nurodo, ar pagal numatytuosius parametrus žymėti registracijos planą. Planas nėra privalomas,tad darbuotojas gali pakeisti numatytąjį žymėjimą. |
   | **Registruotis nebegalima** | Nurodo, ar riboti planą tik atitinkamiems darbuotojams, kurie buvo įregistruoti į planą praėjusiais metais. |
   | **Privalomas planas** | Nurodo, ar automatiškai registruoti į planą darbuotojus. Darbuotojai negali pakeisti registracijos pasirinkimo. |
   | **Sudarymo data** | Data, kada planas buvo sukurtas įmonėje. |
   | **Tiekėjo sąskaita** (išmokos tiekėjas) | Tiekėjas, kuriam įmonė moka priemokas už planą. |
   | **Pavadinimas** (išmokų tiekėjas) | Tiekėjo pavadinimas. |
   | **Tiekėjo nuoroda** (išmokos tiekėjas) | Tiekėjo plano nuoroda. Pavyzdžiui, įmonės grupės plano numeris. |
   | **Alternatyvi nuoroda** (išmokos tiekėjas) | Tiekėjo alternatyvi plano nuoroda. Pavyzdžiui, įmonės sąskaitos numeris. |
   | **Valiuta** (išmokos tiekėjas) | Valiuta, naudojama mokant įmokas tiekėjui. |
   | **Išlaidų sąskaita** (išmokos tiekėjas) | Didžiosios knygos sąskaita, kuri naudojama kaip plano įmokų išlaidų sąskaita. |
   | **Tiekėjo sąskaita** (išmokų administratorius) | Tiekėjas, kuriam įmonė moka už plano administravimą. Jeigu planas yra savarankiškai administruojamas, palikite šį lauką tuščią. |
   | **Pavadinimas** (išmokų administratorius) | Išmokų administratoriaus tiekėjo vardas ir (arba) pavardė. |
   | **Tiekėjo nuoroda** (išmokų administratorius) | Administratoriaus tiekėjo nuoroda į planą. |
   | **Alternatyvi nuoroda** (išmokų administratorius) | Administratoriaus tiekėjo alternatyvi nuoroda į planą. |
   | **Valiuta** (išmokų administratorius) | Valiuta, naudojama mokant išmokų administratoriui. |
   | **Išlaidų sąskaita** (išmokų administratorius) | DK sąskaita, kuri naudojama kaip išlaidų sąskaita išlaidoms, susijusioms su plano administravimu. |

6. Skirtuke **Filtrai** filtruokite pagal savo poreikius. Galite filtruoti pagal šiuos laukus:

   - **Verslo struktūros vienetas**
   - **Skyrius**
   - **Juridinis subjektas**
   - **Vieta**
   - **Pozicija**

7. Skirtuke **Tinkamumo taisyklės** nurodykite šių laukų reikšmes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Eilutės numeris** | Tinkamumo taisyklės eilutės numeris. |
   | **Tinkamumo taisyklė** | Tinkamumo taisyklė, taikoma išmokų planui. Ši tinkamumo taisyklė bus taikoma atitinkamai veiksmo tipui ir susieta su nurodytu draudimo laukimo laikotarpiu ir lengvatomis. |
   | **Veiksmo tipas** | Veiksmas, skirtas tinkamumo taisyklei taikyti: išmokų registracija arba išmokų galiojimo pabaigos data. |
   | **Padengimo laukimo laikotarpis** | Reišmė iš formos Laukimo laikotarpiai. Nuo draudimo laukimo laikotarpio priklauso, kokį dienų ar mėnesių skaičių darbuotojas lauks išmokų padengimo arba išmokų galiojimo pabaigos pagal tinkamumo taisyklės ir veiksmo tipo kriterijus. |
   | **Atskaitymo laukimo laikotarpis** | Reišmė iš formos Laukimo laikotarpiai. Nuo lengvatų laukimo laikotarpio priklauso, kokį dienų ar mėnesių skaičių darbuotojas lauks išmokų atskaitymo nuo jų atlyginimo pagal tinkamumo taisyklės ir veiksmo tipo kriterijus. |

8. Pasirinkite **Įrašyti**.

## <a name="view-enrolled-workers"></a>Užregistruotų darbininkų peržiūra

Galite peržiūrėti darbininkus, užregistruotus pasirinktame išmokų plane.

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Išmokų planai**.

2. Pasirinkite **Užregistruoti darbininkai**.

## <a name="attach-coverage-options"></a>Pridėti padengimo parinktis

Galite įtraukti draudimo parinktis į pasirinktą išmokų planą. Pridėjus draudimo parinkčių galima nustatyti tarifų ir atskaitymų sąranką kartu su draudimo parinktimi.  Pavyzdys: Jei naudojamas gydymo planas, vartotojas pasirinks šeimos draudimo parinktį.  Tada jiems reikės pasirinkti su susijusio plano šeimos tarifą (nustatytą sąrankoje Tarifas) ir susijusio plano lengvatą (nustatytą tarifo sąrankoje). Taip nustatomos darbdavio ir darbuotojo išlaidos pasirinktam draudimui. Tada pakartosite šį procesą darbuotojo + 1 draudimui arba darbuotojo draudimui.

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Išmokų planai**.

2. Pažymėkite **Pridėti draudimo parinktis**.

## <a name="override-eligibility-rules"></a>Tinkamumo taisyklių perrašymas

Galite įtraukti darbininkų į planą kaip tinkamumo taisyklių išimtis. Kiekvienas pridėtas darbininkas turi teisę gauti išmokų planą.

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Išmokų planai**.

2. Pažymėkite **Tinkamumo taisyklės perrašymas**.

## <a name="view-attached-periods"></a>Pridėtų laikotarpių peržiūra

Galite peržiūrėti galimų išmokų laikotarpių sąrašą.

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Išmokų planai**.

2. Pažymėkite **Laikotarpiai**.

## <a name="view-plan-information"></a>Informacijos apie planą peržiūra

Galite pateikti plano aprašą, kad darbuotojams būtų lengviau rinktis išmokas. Čia įvesta informacija apie planą rodoma darbuotojo savitarnos paslaugoje, kai užvedamas žymiklis virš plano draudimo parinkčių sąraše.

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Išmokų planai**.

2. Pasirinkite **Informacija apie planą**.

## <a name="view-flex-credit-programs"></a>Peržiūrėti lanksčiųjų kreditų programas

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Išmokų planai**.

2. Pasirinkite **Lanksčiųjų kreditų programos**.
