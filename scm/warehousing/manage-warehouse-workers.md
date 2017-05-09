---
title: "Sandėlio darbuotojų valdymas"
description: "Šiame straipsnyje aprašoma, kaip „Microsoft Dynamics AX“ galite naudoti, norėdami valdyti ir stebėti darbą, kurį atlieka jūsų sandėlių darbuotojai."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: b63ec70a7d02d23ccdc9fd295a65431ac6b012ba
ms.lasthandoff: 03/31/2017


---

# <a name="manage-warehouse-workers"></a>Sandėlio darbuotojų valdymas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašoma, kaip „Microsoft Dynamics AX“ galite naudoti, norėdami valdyti ir stebėti darbą, kurį atlieka jūsų sandėlių darbuotojai.

Jei naudojate sandėlio valdymo funkcijas, visos sandėlio darbuotojų operacijos yra vadinamos *darbu*. Darbas, pvz., paėmimas, perkėlimas ir turimų atsargų skaičiavimas, yra registruojamas naudojant mobiliuosius įrenginius. Prieš atlikdamas darbą sandėlio darbuotojas turi būti susietas su personalo darbuotoju. Su kiekviena sąskaita **Darbuotojas** gali būti susieti keli sandėlio darbo vartotojai. Tie darbo vartotojai gali dirbti skirtinguose sandėliuose ir gali turėti skirtingų lygių prieigą prie įvairių mobilių įrenginių meniu. Sandėlio darbo vartotojai gali būti laikomi keliais pasirinkto darbuotojo užsiregistravimais. Kiekvienas darbo vartotojas turi numatytąjį sandėlį ir jam taikomos konkrečios darbo eigos, atsižvelgiant į tam darbo vartotojui pasiekiamus meniu elementus. 

Norėdami kurti naują darbo vartotoją, puslapio **Darbuotojai** skirtuko **Bendra** lauke **Sandėliai** spustelėkite **Darbuotojas**. Turite nurodyti vartotojo ID, vartotojo vardą, numatytąjį sandėlį ir meniu pavadinimą. Šis meniu įkeliamas, kai vartotojas prisijungia prie sandėlio mobiliųjų įrenginių portalo, ir jį naudojant galima pasirinkti, prie kurių meniu elementų vartotojas turės prieigą. 

Konkrečios darbo eigos taip pat gali būti nurodytos kaip kiekvieno darbo vartotojo sąrankos dalis. Pavyzdžiui, galite naudoti lauką **Yra ciklų skaičiavimo prižiūrėtojas**, norėdami nurodyti, ar skaičiavimo operacijos metu vartotojas gali apdoroti ciklo skaičiavimo nesutapimų koregavimus, ar šiuos koregavimus pirmiausia turi peržiūrėti kitas asmuo.

## <a name="defining-labor-standards"></a>Darbo standartų nustatymas
Puslapyje **Darbo standartai** galima nustatyti skaičiavimo metodus, sistema naudoja numatomam laikui, kurį tam tikro tipo darbas turėtų trukti, apskaičiuoti. Šį aprašą galima nustatyti bendrame arba konkrečiame lygyje. Pavyzdžiui, galite nurodyti laiką, reikalingą konkretaus vieneto aprašo pardavimo užsakymo išrinkimui pagal svorį apdoroti, kai naudojamas konkretus išrinkimo procesas. Taip pat išrenkamų turimų atsargų padėjimo operacijos laiką galite įrašyti naudodami kitą skaičiavimo metodą. 

Norėdami suaktyvinti jūsų nustatytus darbo standartus, kiekviename sandėlyje, kuriame tie standartai turi būti naudojami, turite pasirinkti parinktį **Leisti darbo standartus**.

## <a name="monitoring-and-controlling-warehouse-work"></a>Sandėlio darbo stebėjimas ir valdymas
Puslapyje **Visi darbai** galima stebėti ir prižiūrėti visus suplanuotus, vykdomus ir baigtus darbus. Šiame puslapyje galima naujinti įvairius procesus, pavyzdžiui, sandėlio darbo vartotojų priskyrimus ir darbo prioritetus. Taip pat galima detalizuoti informaciją, susijusią su darbo antrašte ir darbo eilutėmis, siekiant suprasti numatytus arba baigtus darbo procesus. 

Jei įjungsite parinktį **Darbo standartai**, galėsite peržiūrėti apskaičiuotą numatytą darbo laiką. Tada, vykdant darbą, taip pat bus rodomas kiekvienos darbo operacijos faktinis laikas. Tokiu būdu galima palyginti numatomo laiko skaičiavimus su faktiniu laiku. 

Be to, numatomą laiką galite naudoti taisyklėse, skirtose darbui automatiškai skaidyti, kai darbas kuriamas. Tokiu būdu galima paskirstyti darbo apkrovą, atsižvelgiant į numatytą užduočių atlikimo laiką. 

Laiko, reikalingo darbo elementams apdoroti, analizė gali padėti gerinti sandėlio darbuotojų efektyvumą. Vykdant analizę gali praversti toliau nurodytos ataskaitos.

-   **Darbas pagal vartotoją** – šioje ataskaitoje rodomas darbuotojų efektyvumas, atsižvelgiant į faktinį ir numatomą laiką.
-   **Darbas pagal darbo operacijos tipą** – šią ataskaitą galima naudoti norint ištirti konkrečių sandėlio procesų neefektyvumą. Pvz., pastebite, kad perkėlimo užsakymų paėmimai šią savaitę trunka ilgiau nei ankstesnes savaites. Tada šią informaciją galite naudoti tolimesniame tyrime.





