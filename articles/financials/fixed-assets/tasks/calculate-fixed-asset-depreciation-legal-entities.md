--- 
title: "Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas"
description: "Šioje procedūroje rodoma, kaip nustatyti ir vykdyti kelių juridinių subjektų nusidėvėjimo procesą."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: lt-lt
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ilgalaikio turto nusidėvėjimą tarp juridinių subjektų galima vykdyti vienu veiksmu. Šioje procedūroje rodoma, kaip nustatyti ir vykdyti kelių juridinių subjektų procesą. Joje naudojamas buhalterio vaidmuo.  

Šiame įraše naudojama demonstracinė įmonė USMF.


Papildoma veiksmų (16) užduotis: visos įmonės nusidėvėjimo vykdymo žurnalų nustatymas. 

1. Pirmiausia turite nustatyti atskiro juridinio subjekto žurnalus, kurie bus naudojami atliekant visos įmonės nusidėvėjimo vykdymą. Eikite į Ilgalaikis turtas > Nustatymas > Ilgalaikio turto parametrai. 
2. Išplėskite ilgalaikio turto pasiūlymų skyrių. 
3. Sukurkite įrašą su žurnalo pavadinimu, kuris bus naudojamas kiekviename juridinio subjekto registravimo sluoksnyje. Jei nusidėvėjimo knygos neregistruojamos didžiojoje knygoje, kartu su susietu žurnalu reikia pasirinkti registravimo sluoksnį Nėra. Spustelėkite Pridėti. 
4. Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę. 
5. Lauke Žurnalo pavadinimas įveskite arba pasirinkite reikšmę. 
6. Žurnalo nustatymą pakartokite kiekvieno juridinio subjekto parametrų puslapyje Ilgalaikis turtas. 

Papildoma užduotis: nusidėvėjimo apskaičiavimas

1. Norėdami pradėti nusidėvėjimo vykdymą tarp juridinių subjektų, pasinaudokite puslapiu Kurti nusidėvėjimo pasiūlymą. Pasirinkite Ilgalaikis turtas > Žurnalo įrašai > Kurti nusidėvėjimo pasiūlymą. 
2. Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę. 
3. Pagal numatytąsias nuostatas, bus naudojamas ilgalaikio turto parametruose nurodytas žurnalo pavadinimas. Šioje parinktyje galima keisti kiekvieno esamo juridinio subjekto pavadinimą. 
4. Lauke Pabaigos data įveskite datą. 
5. Pasirinkite juridinių subjektų, kurie bus įtraukti į nusidėvėjimo vykdymą. Sąraše bus rodomi tik ilgalaikio turto parametrų puslapyje pateikti ilgalaikio turto pasiūlymams nustatyti žurnalai. 
6. Kai ši parinktis įgalinta, sukūrus nusidėvėjimo žurnalų parinktis Registruoti žurnalus juos užregistruos automatiškai. Nepasirinkus šios parinkties žurnalai bus sukurti, bet neužregistruoti, todėl prieš juos registruodami galėsite peržiūrėti išsamią informaciją. Lauke Registruoti žurnalus pasirinkite Taip. 
7. Filtravimo laukai apima visą šiam nusidėvėjimo vykdymui pasirinktų juridinių subjektų ilgalaikį turtą, grupes ir knygas. 
8. Parinktis Paketinis vykdymas įgalinta pagal numatytuosius nustatymus. Kai ši parinktis įgalinta, nusidėvėjimo žurnalo kūrimas ir registravimas bus vykdomi fone. 
9. Spustelėkite Kurti žurnalą. 
10. Atitinkamuose juridiniuose subjektuose sukurtus nusidėvėjimo žurnalus reikia peržiūrėti. Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.

