---
title: Pareigybės
description: Šioje temoje aprašomi konceptualūs elementai, kuriuos gali turėti pareigos. Joje taip pat pateikiami pavyzdžiai, kurie parodo, kaip galite naudoti šiuos elementus jūsų organizacijoje.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c8311df31326faeadd280585115338317b19125d54f3a526b4ccc6ef6684ad2c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754757"
---
# <a name="positions"></a>Pareigybės

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomi konceptualūs elementai, kuriuos gali turėti pareigos. Joje taip pat pateikiami pavyzdžiai, kurie parodo, kaip galite naudoti šiuos elementus jūsų organizacijoje.

Prieš kurdami pareigas, turite nustatyti užduotį. Kai kurie pareigų duomenys, pavyzdžiui, kompensacijos regionas, darbuotojo priskyrimas, pareigų trukmė ir ataskaitų ryšiai, turi įsigaliojimo datą.

## <a name="general-information"></a>Bendroji informacija

Kai kuriate pareigas, privalote pasirinkti užduotį. Ši informacija bus automatiškai užpildyta iš jūsų pasirinktos užduoties:

- Aprašas
- Kreipinys
- Pilno etato ekvivalentas
- Užduočių grupė

Pareigų pavadinimas naudojamas darbuotojo pareigoms nurodyti. (Darbuotojui pateiktas pavadinimas nėra naudojamas.) Todėl pareigų pavadinimus reikėtų standartizuoti kuo įmanoma labiau.

> [!NOTE]
> Darbuotojo negalima paskirti į pareigas ankstesnę dieną nei galima priskyrimo data.
>
> Puslapio **Bendrinami Žmogiškųjų išteklių parametrai** skirtuke **Pareigos** esantis parametras kontroliuoja darbuotojo priskyrimo elgseną. Pasirinkite vieną iš šių reikšmių:
>
> - **Visada** – galima priskirti darbuotojus naujoms pareigoms kuriant pareigas. Sukūrus pareigas **Galima priskirti** data ir laikas bus automatiškai nustatyti į sukūrimo datą ir laiką skirtuke **Bendra**, esančiame puslapyje **Pareigos**.
> - **Niekada** – negalima priskirti darbuotojų naujoms pareigoms kuriant pareigas. Jei pasirenkate šią parinktį, turite atidaryti **Pareigų** puslapį kiekvienoms naujoms pareigoms, kai jos tampa galimos. Tada skirtuke **Bendra** įveskite **Galima priskyrimui** datą, kad įgalintumėte darbuotojo priskyrimą. Jei pasirinksite šią parinktį, darbuotojo priskyrimo data bus nustatyta kaip **Niekada** pagal numatytuosius nustatymus, kai bandysite priskirti darbuotoją.

## <a name="position-duration"></a>Pareigų trukmė

Kiekvienos pareigos galioja tam tikrą laiko tarpą, kuris vadinamas trukme. Pavyzdžiui, vasaros pareigos gali trukti nuo 2021 m. gegužės 1 d. iki 2021 m. rugpjūčio 31 d. Aktyvavimo data yra data, kai pareigos sistemoje yra aktyvios. Atsistatydinimo data yra data, kai pareigos sistemoje nebėra aktyvios.

Nepamirškite, kad nei galima priskyrimo data, nei darbuotojo priskyrimo data negali būti prieš aktyvinimo datą. Pareigos nėra laikomos aktyviomis, neatėjus aktyvavimo datai. Be to, darbuotojo paskyrimas negali tęstis ilgiau po išėjimo į pensiją datos.

## <a name="reports-to-position"></a>Ataskaitų teikimas pareigų atstovui

Pareigos yra svarbus žemesnio organizacijos hierarchijos lygio elementas. **Pareigų** puslapyje galite nurodyti pareigų atskaitingumo ryšius. Priskyrę darbuotoją pareigoms, kurios atskaitingos kitoms pareigoms, sukuriate atskaitingumo ryšį tarp šitoms dviems pareigoms priskirtų darbuotojų. Pavyzdžiui, pareigos 000220 atsiskaito 000300 pareigoms. Kim Akers priskirta pareigoms 000220, o Sanjay Patel priskirtas pareigoms 000300. Todėl Kim Akers atsiskaito Sanjay Patel.

> [!TIP]
> Ataskaitos pagal pareigas naudojamos visoje sistemoje, norint nustatyti, kas yra darbuotojo vadovas. Ankstesniame pavyzdyje, jei sistemoje vadovo vaidmuo priskirtas Sanjay Patel, jis matys Kim Akers kaip tiesioginę ataskaitą Vadovo savitarnoje. Ataskaitų ryšiai taip pat gali būti naudojami kuriant darbo eigos maršruto taisykles ir kontrolinio sąrašo užduotis.

## <a name="relationships"></a>Ryšiai

Jeigu jūsų organizacija naudoja matricos hierarchiją arba kitą pasirinktinę hierarchiją, galite nustatyti pareigų hierarchijų tipus. Tada galite įtraukti ataskaitų ryšius į kiekvieno nustatyto hierarchijos tipo pareigas. Pavyzdžiui, Lori Penor yra „Adventure Works“ generalinė direktorė ir yra priskirta pareigoms **Generalinis direktorius**. Lori valdo produkto, skirto valymui atlikti, vystymą. Jai reikia buhalterio, kuris padėtų jai su finansais. Todėl ji įdarbino Kim Akers buhalterės pareigoms užimti. Kim tiesiogiai atsiskaito Sanjay Patel, tačiau ji taip pat bendradarbiauja su Lori Penor atlikdama užduotis, susijusias su finansine produkto vystymo sritimi.

Remiantis anksčiau pateiktu pavyzdžiu, Kim Akers ir Lori Penor darbo santykiams nustatyti turėtumėte atlikti toliau išvardytas užduotis:

1. Sukurti pasirinktinį pareigų hierarchijos tipą, pavadinimu **Valdiklis**, kad būtų sukurta hierarchija, apimanti pareigas, kurių atstovai atsakingi už darbą su valdiklių valymo produktu.
2. Nustatykite **Generalinio direktoriaus** pareigas kaip pareigas, kurioms Kim yra atskaitinga **Elektroninio prietaiso** hierarchijoje.
3. Peržiūrėti pareigų atskaitingumo struktūrą naudojant pareigų hierarchiją. Jei naudojate keletą pareigų hierarchijų, galite peržiūrėti kiekvieno tipo hierarchiją pareigų hierarchijoje. Jūs taip pat galite ieškoti pareigų pagal pareigų ID arba darbuotojo, kuris yra priskirtas toms pareigoms, vardą ir pavardę. Pareigų hierarchija priklauso nuo organizacijos hierarchijos.

## <a name="labor-union"></a>Profesinė sąjunga

Galite įrašyti, ar pareigoms yra reikalinga sąjungos sutartis bei naudojamą profesinę sąjungą. Be to, galite susieti sutartį su juridiniu subjektu.

## <a name="financial-dimensions"></a>Finansinės dimensijos

Kai kuriate finansinę pareigų dimensiją, turite nurodyti juridinį subjektą. Galite pasirinkti numatytąsias dimensijas kiekvienai dimensijai atskirai. Kitu atveju galite pasirinkti paskirstymo šabloną, automatiškai užpildantį numatytąsias dimensijas. Paskirstymo šablonas taip pat suteikia parinktį paskirstyti sumas keliose dimensijų reikšmėse.
