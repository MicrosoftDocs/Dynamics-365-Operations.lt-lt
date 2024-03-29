---
title: Centralizuotų mokėjimų sudengimo apžvalga
description: Šiame straipsnyje aprašomas centralizuotų Microsoft Dynamics 365 finansų mokėjimų sudengimas.
author: angelad116
ms.date: 11/22/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "222414"
- intro-internal
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42c359edbe49af151ac76c9873c0d429bbe1ca12
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804232"
---
# <a name="settlement-overview-for-centralized-payments"></a>Centralizuotų mokėjimų sudengimo apžvalga

[!include [banner](../includes/banner.md)]

Organizacijos, sudarytos iš kelių juridinių subjektų, gali kurti ir valdyti mokėjimus naudodamos juridinį subjektą, kuris tvarko visus mokėjimus. Todėl tos pačios operacijos nereikia įvesti keliuose juridiniuose subjektuose ir yra sutaupoma laiko supaprastinant mokėjimo pasiūlymo procesą, atsiskaitymo procesą, atvirų operacijų redagavimą ir centralizuotų mokėjimų uždarytų operacijų redagavimą. 

Kai kliento arba tiekėjo mokėjimas įvedamas viename juridiniame subjekte ir sudengiamas su SF, kuri buvo įvesta kitame juridiniame subjekte, kiekvienam juridiniam subjektui automatiškai sukuriamas tinkamas sudengimas, „mokėti iki“ ir „mokėti nuo“ operacijos. Sudengimo įrašas sukuriamas kiekvienam SF ir mokėjimo deriniui. Kiekvienam sudengimo įrašui priskiriamas naujas kvito numeris, pagrįstas mokėjimo kvito numeracijos serija, nurodyta klientų puslapyje **Gautinų sumų parametrai** ir tiekėjų puslapyje **Mokėtinų sumų parametrai**. 

Jei papildomi sudengimo įrašai sukuriami mokėjimo nuolaidoms, užsienio valiutos kurso pasikeitimas, centų skirtumams, permokėjimams arba neprimokėjimams, jie priskiriami vėlesnei mokėjimo arba SF operacijos datai. Jeigu sudengimas vyksta po to, kai mokėjimas užregistruotas, sudengimo įrašai naudoja sudengimo registravimo datą, nurodytą puslapyje **Atvirų operacijų sudengimas**.

## <a name="posting-types-transaction-types-and-default-descriptions"></a>Registravimo tipai, operacijų tipai ir numatytieji aprašai

Vidinės įmonės sudengimo kvito operacijose naudojami vidinės įmonės sudengimo registravimo tipas, vidinės įmonės klientų sudengimo ir vidinės įmonės tiekėjo sudengimo operacijų tipai. Operacijos tipo operaciją galima nustatyti puslapyje **Numatytieji aprašai**. 

Šie operacijų tipai galimi vienos įmonės ir visų įmonių sudengimams:

-   Atsiskaitymas
-   Mokėjimo nuolaida
-   Užsienio valiutos kurso pasikeitimas (įskaitant įvykdytus ir neįvykdytus užsienio valiutos kurso pasikeitimus)
-   Centų skirtumas
-   Permokėjimas/neprimokėjimas

Taip pat galite nustatyti numatytuosius vidinės įmonės sudengimo kvitų aprašus.

## <a name="currency-exchange-gains-or-losses"></a>Pelnas ir nuostolis dėl valiutos kurso

Su operacija saugomas valiutos kursas, naudojamas kliento arba tiekėjo operacijoms. Dėl valiutos kurso realizuotas pelnas arba patirtas nuostolis užregistruojamas SF juridiniame subjekte arba mokėjimo juridiniame subjekte, atsižvelgiant į mokėjimo juridinio subjekto puslapio **Vidinės įmonės apskaita** lauke **Registruoti valiutos kurso pelną arba nuostolį** pasirinktą parinktį. Šiuose pavyzdžiuose naudojamos tokios valiutos:
-   Mokėjimo apskaitos valiuta: EUR
-   SF apskaitos valiuta: USD
-   Mokėjimo operacijos valiuta: DKK
-   SF operacijos valiuta: CAD

### <a name="currency-calculations"></a>Valiutos skaičiavimai

Kai viename juridiniame subjekte įvesta SF sudengiama su kitame juridiniame subjekte įvestu mokėjimu, mokėjimo operacijos valiuta (DKK) konvertuojama atliekant tris tolesnius veiksmus.
1.  Konvertuojama į su mokėjimu susijusios apskaitos valiutą (EUR), taikant mokėjimo juridinio subjekto valiutos kursą.
2.  Konvertuojama į SF apskaitos valiutą (USD).
3.  Konvertuojama į SF operacijos valiutą (CAD), taikant SF juridinio subjekto valiutos kursą.

Konvertavimo procese naudojami mokėjimo datą galiojantys valiutos kursai. Jeigu mokėjimo suma SF operacijos valiuta (CAD) lygi SF sumai (CAD), laikoma, kad SF iki galo apmokėta. 

Kai puslapis **Atvirų operacijų sudengimas** atidaromas iš mokėjimų žurnalo, kuriame mokėjimo suma neįvesta, sudengtina suma apskaičiuojama pagal SF, kurios pasirinktos sudengti puslapyje **Atvirų operacijų sudengimas**. Sudengtina suma konvertuojama trimis veiksmais:
1.  Konvertuojama į SF apskaitos valiutą (USD), taikant SF juridinio subjekto valiutos kursą, galiojusį mokėjimo datą.
2.  Konvertuojama į mokėjimo apskaitos valiutą (EUR), taikant SF juridinio subjekto valiutos kursą, galiojusį mokėjimo datą.
3.  Konvertuojama į mokėjimo operacijos valiutą (DKK).

Uždarius puslapį **Atvirų operacijų sudengimas** gauta mokėjimo suma perkeliama į mokėjimų žurnalo eilutę.

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Pelno arba nuostolio, patirto dėl skirtingų apskaitos valiutų, registravimas

Jeigu gaunamas valiutos kurso pelnas arba patiriamas nuostolis, jis registruojamas juridiniame subjekte, kuris nurodytas mokėjimo juridinio subjekto puslapio **Vidinės įmonės apskaita** lauke **Registruoti valiutos kurso pelną arba nuostolį**. Pelno arba nuostolio suma konvertuojama į juridinio subjekto, kuriame užregistruota pelno arba nuostolio suma, apskaitos valiutą, taikant nustatytą to juridinio subjekto valiutos kursą.

## <a name="cash-discounts"></a>Mokėjimo nuolaidos

Mokėjimo nuolaidos, generuojamos visų įmonių sudengimo metu, užregistruojamos SF juridiniame subjekte arba mokėjimo juridiniame subjekte, atsižvelgiant į mokėjimo juridinio subjekto puslapio **Vidinės įmonės apskaita** lauke **Registruoti mokėjimo nuolaidą** pasirinktą parinktį. SF juridiniame subjekte generuojama atitinkama sudengimo operacija.

## <a name="overpayments-and-underpayments"></a>Permokėjimas ir neprimokėjimas

Leistini permokėjimo / neprimokėjimo ir centų skirtumo nuokrypiai nustatomi atsižvelgiant į su mokėjimu susijusį juridinį subjektą (permokėjimui) ir SF juridinį subjektą (neprimokėjimui). Naudojama registravimo sąskaita nustatoma naudojant klientų puslapio **Gautinų sumų parametrai** lauko **Mokėjimo nuolaidų administravimas** parametrą ir tiekėjų puslapio **Mokėtinų sumų parametrai** lauko **Mokėjimo nuolaidų administravimas** parametrą.

-    **·** **Jei** mokėjimo nuolaidos administravimo parametras yra konkretus arba jei parametras nespecifinis ir taikoma mokėjimo nuolaida užregistruojama skirtinguose juridiniuose subjektuose, kurie nėra permokėjimo, naudojama automatinė kliento mokėjimo nuolaidos, tiekėjo mokėjimo nuolaidos arba centų skirtumo sąskaita apskaitos valiuta. Šias sąskaitas galite nurodyti puslapyje **Automatinių operacijų sąskaitos**.
-    **Jei** mokėjimo nuolaidos administravimo parametras nespecifinis ir mokėjimo nuolaida užregistruota tame pačiame juridiniame subjekte kaip permokėjimas (mokėjimo juridinis subjektas ir SF juridinis subjektas yra tokie patys), mokėjimo nuolaidos sąskaita pakoreguota. Pavyzdžiui, jei 100,00 sumos SF, kurios galima mokėjimo nuolaida yra 3,00, sudengiama su mokėjimu, kurio suma 98,00, mokėjimo nuolaidos sąskaita pakoreguojama (1,00). Grynoji nuolaidos suma yra 2,00.
-    **Jei** mokėjimo nuolaidos administravimo parametras nespecifinis, mokėjimo nuolaida užregistruojama tame pačiame juridiniame subjekte kaip permokėjimas, o permokėjimas arba neprimokėjimas sudengtas su keliomis SF, kurioms taikomos mokėjimo nuolaidos, pakoregama paskutinės SF mokėjimo nuolaidos sąskaita.

Jei mokėjimo nuolaidos administravimo pasirinkimas **nespecifinis**, nespecifinis mokėjimo sudengimo taisyklės taikomos tik tokiose situacijose:
-   Yra permokėjimas.
-   Permokėjimas sudengtas su viena arba daugiau SF, kuriose taikoma mokėjimo nuolaida.
-   Mokėjimo nuolaida užregistruota tame pačiame juridiniame subjekte kaip permokėjimas.

Visais kitais atvejais permokėjimai ir neprimokėjimai registruojami automatinėje kliento mokėjimo nuolaidos, tiekėjo mokėjimo nuolaidos arba skirtumo centais apskaitos valiuta sąskaitoje.

## <a name="sales-tax"></a>PVM
PVM operacijos išlieka juridiniame subjekte, kurioje pirmą kartą užregistruotos. 

Jei PVM buvo užregistruotas išankstiniam apmokėjimui, visų įmonių sudengimas grąžina išankstinio apmokėjimo PVM į išankstinio apmokėjimo juridinį subjektą. SF juridinio subjekto mokesčiai lieka SF juridiniame subjekte.

## <a name="financial-dimensions"></a>Finansinės dimensijos
Kliento mokėjimams „mokėti iki“ ir „mokėti nuo“ operacijos mokėjimo juridiniame subjekte naudoja finansines dimensijas, kurios iš sudengto mokėjimo nustatytos gautinų sumų suminėje sąskaitoje. SF juridiniame subjekte „mokėti iki“ ir „mokėti nuo“ operacijos naudoja finansines dimensijas, kurios gautinų sumų suminėje sąskaitoje nustatytos naudojant sudengiamą SF. 

Tiekėjo mokėjimams „mokėti iki“ ir „mokėti nuo“ operacijos mokėjimo juridiniame subjekte naudoja finansines dimensijas, kurios iš sudengto mokėjimo nustatytos mokėtinų sumų suminėje sąskaitoje. SF juridiniame subjekte „mokėti iki“ ir „mokėti nuo“ operacijos naudoja finansines dimensijas, kurios mokėtinų sumų suminėje sąskaitoje nustatytos naudojant sudengiamą SF.

## <a name="withholding-tax"></a>Išskaitomas mokestis
Tiekėjo kodas, susietas su SF, naudojamas norint nustatyti, ar išskaitomas mokestis turėtų būti skaičiuojamas. Jei išskaitomas mokestis pritaikomas, jis apskaičiuojamas juridiniame subjekte, kuris susietas su SF. Jei juridiniame subjekte naudojamos skirtingos valiutos, naudojamas su SF susieto juridinio subjekto valiutos kursas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
