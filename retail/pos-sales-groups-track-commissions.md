---
title: "Stebėti Komisijos pos naudojant pardavimo grupes"
description: "Yra įprasta mažmeninių sekti pardavimai bendradarbis, kuris dirbo su klientu, teikti pagalbą, iki pardavimo, kryžminio pardavimo ir perdirbimo operacija."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Stebėti Komisijos pos naudojant pardavimo grupes

Yra įprasta mažmeninių sekti pardavimai bendradarbis, kuris dirbo su klientu, teikti pagalbą, iki pardavimo, kryžminio pardavimo ir perdirbimo operacija.

Pardavimo sekimą pardavimo atstovas yra priemonė Associates pardavimo sugebėjimus, o pardavimai pagal kasininko yra priemonė greičio ir efektyvumo. Pardavimai, stebimi pardavėja taip pat dažnai naudojami norint apskaičiuoti komisinių ar kitų paskatų.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Konfigūravimas darbuotojas prie pos pardavimo atstovas
Kai darbuotojas įtraukiamas į pardavimo grupę, jie pradeda naudotis Komisija ir gali būti identifikuojami kaip pardavimo atstovas sistemoje. Darbuotojų, kurie nėra įtraukti į pardavimo grupę nėra tinkami Komisijos ir nebus rodomas kaip pardavimo atstovas, pardavimo (PV) taškas. Pos, pardavimo atstovų sąrašo yra kilęs iš visų pardavimų grupes, kuriose yra bent vienas darbuotojas, priskirtos. Sąrašas yra rodomas pos pardavimų grupės ID ir pavadinimą derinys (ID: pavadinimas). Pardavimo grupe gali būti priskirtas darbuotojų palaikymo scenarijai, kai agentas pasirenka nustatyti prekybos atstovą POS eilutes automatiškai. Vartotojai gali pasirinkti iš pardavimų grupės, kad darbuotojas yra narys.

## <a name="functionality-profile-settings"></a>Funkciją profilio nustatymai
Yra keletas funkciją profilio nustatymai laikyti, kad bus nustatyti, srauto ir procesas, gamintojų organizacijoms, kurios dalyvauja prekybos atstovai.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Jei ši parinktis įjungta, POS bus automatiškai užpildyti operacijos eilutes su dabartinės kasininko pardavimo grupe. Jei kasininkas nėra numatytoji pardavimo grupė nenurodyta, nebus nustatyti reikšmės. Vartotojas gali dar rankiniu būdu nustatyti pardavimo grupę GO mygtuką tinklo mygtuką.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Ši parinktis yra trys galimos reikšmės: ** Nr ** – pasirinkus šią parinktį, vartotojas nebus būsite paraginti pasirinkti pardavimo grupę. Vertė dar gali būti nustatyti naudojant kasos darbo grupe pardavimo arba rankiniu būdu naudojant POS mygtuką tinklo mygtuką. **Pradėti operacijos** - Jei pasirinktas šis variantas, ir arba dėl **prie kasos** nėra įgalinta parinktis arba Dabartinis kasa neturi pardavimo grupe, vartotojo paprašys pasirinkti pardavimo grupę pradžioje kiekvieną sandorį. Pasirinkus pardavimo grupė iš šio raginimo bus numatytoji kitos eilutės pasirinktus pardavimų grupei. Vartotojas gali dar rankiniu būdu nustatyti pardavimo grupę GO mygtuką tinklo mygtuką. **Kiekvienai eilutei** - Jei pasirinktas šis variantas, ir arba dėl **prie kasos** nėra įgalinta parinktis arba Dabartinis kasa neturi pardavimo grupe, vartotojo paprašys pasirinkti pardavimo grupę įpylus kiekvieną eilutę. Vartotojas gali dar rankiniu būdu nustatyti pardavimų grupės POS mygtuką tinklo mygtuką. |
| **Reikalauti**                           | Ši parinktis taikoma tik, kai POS kompiuteris sukonfigūruotas reikalauti pardavimo atstovas. Jei įjungta, vartotojas turi pasirinkti pardavimo grupė prieš tęsdami. Kitaip, vartotojas bus pasiūlyta, bet gali atšaukti ir toliau be pasirinkimą. Pridėjus į eilutę, vartotojas, turintis pakankamas teises galėtų dar pašalinti pardavimo grupę iš eilutės. "Pardavimų atstovas reikalauja, kad" nėra įvykdytas šioje situacijoje.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Pardavimo atstovo informacijos rodymo ekrane POS operacijas
POS sandorio ekrano išdėstymas ir turinys yra konfigūruojama naudojant ekrano išdėstymas dizaineris ir jiems priskiriamas ekrano maketus į parduotuves, registrų ar darbuotojų. Į **pardavimo atstovą** lauką galima įtraukti į skirtuką eilučių gavimo srityje.  Tai bus rodomas kiekvienoje eilutėje nurodyta pardavimų grupės ID sandorio ekrane.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Pridedant pardavimo atstovas operacijų POS mygtuką tinkleliai
POS leidžia vartotojams nustatyti mygtukynų, kurios yra įtrauktos į ekrano išdėstymas suteikti prieigą prie POS operacijas. Tokias POS operacijas galima priskirti mygtukyno mygtukai, yra susijusios su pardavimo atstovais.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operacija**                             | **Description**                                                                                                                                                                                                                                                                              |
| Nustatyti pardavimo atstovą eilutėje          | Šis POS operacija rodo reikalavimus atitinkančių pardavimų grupių sąrašą (ID: pavadinimas) į parduotuvę. Pasirinkus pardavimo grupė iš šio sąrašo bus nustatyti reikšmę dabartinės operacijos eilutės.                                                                                                            |
| Išvalyti pardavimo atstovą eilutėje        | Operacijai POS pašalina esamą pardavimų grupės vertę iš dabartinės operacijos eilutės.                                                                                                                                                                                                  |
| Nustatyti pardavimo atstovas sandorį   | Šis POS operacija rodo reikalavimus atitinkančių pardavimų grupių sąrašą (ID: pavadinimas) į parduotuvę. Pasirinkus pardavimo grupė iš šio sąrašo bus nustatyti tokią numatytąją vertę apie šią operaciją. Bet esamas linijas be pardavimų grupei priskirtas bus nustatyti, taip pat vėliau papildomas eilutes. |
| Aišku pardavimo atstovas sandorį | Šis POS operacijos pašalina dabartinę numatytąją pardavimo vertė pagal dabartinį sandorį. Jis neturi įtakos jau operacijos eilutes.                                                                                                                             |

## <a name="calculating-commissions"></a>Apskaičiuoti komisiniai
Komisija apskaičiavo darbuotojams nurodyta pardavimo grupes ar ataskaitas registruoti arba pardavimo užsakymo registravimo metu. Komisinių suma nustatoma, remiantis darbuotojo komisinių dalį, kaip apibrėžta pardavimo grupę ir susiję Komisijos skaičiavimo parametrus klientų ir (arba) produktų operacijos.


