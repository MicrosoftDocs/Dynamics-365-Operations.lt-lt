---
title: Kurti naują projektą
description: Šioje temoje pateikiama informacija apie tai, kaip kurti naują projektą.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760613"
---
# <a name="create-a-new-project"></a>Kurti naują projektą

[!include [banner](../includes/banner.md)]

Norėdami sukurti naują projektą, atlikite toliau nurodytus veiksmus.

1. Puslapyje **Projektų valdymas** pasirinkite **Naujas projektas** ir įveskite tolesnes reikšmes.

    - **Projekto tipas:** Laiko ir medžiagų.
    - **Projekto pavadinimas:** XYZ atnaujinimas, 2 etapas.
    - **Projekto grupė:** TM\_WIP
    - **Projekto sutarties ID:** 00000002.

2. Pasirinkite **Kurti projektą**.

## <a name="assign-a-resource-to-a-project"></a>Ištekliaus priskyrimas projektui

1. Puslapyje **Darbuotojai**, sąraše **Darbuotojai** pasirinkite darbuotojo, kurio kompetencijas nustatėte anksčiau, įrašą ir jį atidarykite.
2. Veiksmų srityje, skirtuke **Projektas**, grupėje **Nustatymas** pasirinkite **Priskirti projektus**.
3. Puslapio **Išteklių tikrinimo projekto priskyrimai** skirtuko **Projektai** lauke **Įtraukti projektą į pasirinktus projektus** taikykite filtrą projektui **XYZ atnaujinimas, 2 etapas**.
4. Srityje **Likę projektai** pasirinkite projektą ir, pasirinkdami rodyklės mygtuką, jį įtraukite į sritį **Pasirinkti projektai**.

Taip pat galite pagal poreikį ištekliui priskirti kategorijų. Kategorijos tipas gali būti **Išlaidos** arba **Įplaukos**. Kategorijos tipą nustato jūsų organizacija. Jei ištekliui kategorijų nepriskirta, „Finance“ suranda numatytąją išlaidų ir įplaukų valandos kainų kategoriją.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projekto išteklių ir vaidmenų charakteristikų nustatymas

Naudodamas projektų išteklių funkcijas projekto vadovas gali kurti reikiamus projekto vaidmenis. Vaidmenys gali būti naudojami, jei rezervuojant išteklius vis dar nežinomi patvirtinti ištekliai. Vaidmenis galima laikinai rezervuoti kaip planuotus išteklius, kad būtų galima vykdyti kitus projekto planavimo etapus.

[![Vaidmens pavyzdys](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarijus:** „Contoso‟ buvo pasamdyta atlikti laiko ir medžiagų projektui su patvirtinta chartija. Jaunesnysis projektų vadovas vis dar nustatinėja projekto sritį. Išteklių vadovas šiuo metu identifikuoja konkrečius išteklius, kurie bus rezervuoti naujojo projekto darbui. Dėl projekto svarbos projekto rėmėjas kaip vieno iš vaidmenų pageidavo vaidmens Vyresnysis projektų vadovas. Išteklių vadovas turi gauti naująjį išteklių ir apibrėžti vaidmenį sistemoje – tam atvejui, jei, planuojant projektą, jaunesniajam projektų vadovui prireiktų informacijos apie išteklius.

Tolesniais veiksmais rodoma, kaip išteklių vadovas gali nustatyti Vyresniojo projektų vadovo vaidmenį ir susieti su juo išteklių charakteristikas. Vėliau vaidmenį galima naudoti ieškant turimų išteklių, kurie atitinka reikiamas išteklių kompetencijas.

1. Puslapyje **Nustatyti vaidmenis** pasirinkite **Naujas** ir įveskite tolesnes reikšmes.

    - **Vaidmens ID:** Vyresnysis projektų vadovas.
    - **Aprašas:** Vyresnysis projektų vadovas.

2. Pasirinkite **Kurti**.
3. Pasirinkite vaidmenį **Vyresnysis projektų vadovas**, tada – **Konfigūruoti charakteristikas**.
4. Lauke **Charakteristikų tipas** pasirinkite **Įgūdis**.
5. Lauke **Pasiekiamos charakteristikos** įveskite ieškotiną įgūdį.
6. Lauke **Charakteristikos tipas** pasirinkite **Sertifikatas**.
7. Lauke **Pasiekiamos charakteristikos** įveskite ieškotino sertifikato tipą.

## <a name="assign-a-project-resource-to-a-project"></a>Projekto ištekliaus priskyrimas projektui

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.
2. Skirtuke **Projekto komanda ir planavimas** pasirinkite **Įtraukti**.
3. Lauke **Vaidmuo** pasirinkite **Komandos narys**.
4. Pasirinkite **Rezervuoti kalendoriuje**.
5. Puslapyje **Išteklių pasiekiamumas** pasirinkite **Rodinio parametrai**.
6. Puslapyje **Koreguoti rodinio parametrus** įveskite tolesnes reikšmes.

    - **Datų intervalo rodinio formatas:** Diena.
    - **Rodyti užimtumo aprašus:** Taip.
    - **Rodyti likusį pajėgumą:** Taip.

7. Išteklių sąraše pasirinkite išteklių.
8. Pasirinkite **Tiksliai planuoti užimtumą** ir **Visas pajėgumas**.

## <a name="assign-a-resource-to-a-default-role"></a>Ištekliaus priskyrimas numatytajam vaidmeniui

Norint padėti projektų ar išteklių vadovams, galima dar labiau detalizuoti projektui galimus rezervuoti išteklius. Numatytąjį vaidmenį galima susieti su esamu ištekliumi arba naujai gautu ištekliumi. Pavyzdžiui, kai Danielis buvo priimtas į darbą, jo patirtis ir įgūdžiai buvo tinkami verslo analitiko vaidmeniui. Išteklių vadovas priskyrė šį vaidmenį kaip numatytąjį Danielio vaidmenį. Todėl išteklių vadovas Danielį pridėjo į verslo analitikų, kurie gali dirbti su projektais, telkinį.

Rezervuodami išteklius projektų vadovai gali filtruoti vaidmenų išteklius, kurie gali dirbti su projektais. Kai panaudodami išteklius vadovai atlieka kelių kriterijų sprendimų analizę, šią informaciją jie gali naudoti kaip vieną iš kriterijų. Jie taip pat gali į filtrą įtraukti kitų išteklių charakteristikų ir ieškoti išteklių, turinčių konkrečių įgūdžių, išsilavinimą ir patirties konkrečiam projektui atlikti.

**Scenarijus:** pradėtas patvirtintas projektas ir projekto planavimo etape kaip planuoti ištekliai buvo rezervuotas vyresniojo projekto vadovo vaidmuo. Išteklių vadovas gavo išteklių užimti vyresniojo projekto vadovo vaidmeniui.

1. Puslapyje **Išteklių sąrašas** pasirinkite **Danielis Goldschmidtas**.
2. Puslapyje **Ištekliaus vaidmuo** pasirinkite **Naujas** ir įveskite tolesnes reikšmes.

    - **Įsigalioja:** įveskite dabartinę datą.
    - **Galiojimo pabaiga:** įveskite **Niekada**.
    - **Vaidmuo:** įveskite **Vyresnysis projektų vadovas**.

3. Pasirinkite **Įrašyti** ir uždarykite puslapį.
4. Skirtuke **Kompetencijos** pridėkite įgūdį **ProjektVald** ir sertifikatą **PMP**.
