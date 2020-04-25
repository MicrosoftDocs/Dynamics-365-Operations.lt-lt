---
title: Kurti produkto konfigūracijos modelį
description: Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9577005fb4fc016670713c36e40263ff30030caf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203769"
---
# <a name="create-a-product-configuration-model"></a>Kurti produkto konfigūracijos modelį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-product-model"></a>Produkto modelio kūrimas
1. Spustelėkite Produkto varianto modelio aprašą.
2. Spustelėkite Produkto konfigūracijos modeliai.
3. Spustelėkite Naujas.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Aprašas įveskite reikšmę.
6. Lauke Sprendimo priemonės strategija pasirinkite pasirinktį.
    * Sprendimo priemonės strategija nustato, kaip tvarkomi produktų konfigūravimo pagal apribojimus modelio apribojimai. Šis pasirinkimas gali turėti įtakos produkto konfigūracijos modelio našumui.  
7. Lauke Pavadinimas surinkite reikšmę.
    * Šakninis komponentas nurodo produkto konfigūracijos modelį, tačiau jį galima naudoti kituose produkto modeliuose.  
8. Spustelėkite GERAI.
9. Lauke Pakartotinai naudoti konfigūracijas pasirinkite pasirinktį.
    * Jei pakartotinis konfigūracijos parametras yra nustatytas į Taip, sistema patikrins, ar yra identiškų konfigūracijų po kiekvieno konfigūracijos seanso ir pakartotinai jas naudos, jei ras tikslų atitikimą.  

## <a name="add-attributes"></a>Įtraukti atributų
1. Išplėskite skyrių Atributai.
2. Spustelėkite Pridėti.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Sprendimo priemonės pavadinimas įveskite vertę.
    * Produkto konfigūravimo priemonė apribojimo sprendimo priemonė naudoja Sprendimo priemonės pavadinimą. Jame negali būti tarpų arba specialiųjų simbolių, išskyrus _ (pabraukimo brūkšnys).  
6. Lauke Aprašas įveskite reikšmę.
    * Aprašo tekstas rodomas konfigūracijos vartotojui ir todėl gali padėti pasirenkant tinkamą atributo vertę.  
7. Lauke Atributo tipas įveskite arba pasirinkite vertę.
    * Atributo tipas nustato, kurios vertės yra galimos atributui.  
8. Pažymėkite žymės langelį Įtraukti į pakartotinį naudojimą.
    * Ši pasirinktis galima tik tokiu atveju, jei pasirinkta pasirinktis Pakartotinai naudoti konfigūracijas. Įtraukiant atributą į pakartotinio naudojimą žymės langelį reiškia, kad šis atributas bus svarstomas, kai sistema ieškos tikslaus atitikimo.  

## <a name="add-subcomponents"></a>Įtraukti pakomponenčius
1. Išplėskite skyrių Pakomponenčiai.
2. Spustelėkite Pridėti.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Sprendimo priemonės pavadinimas įveskite vertę.
6. Lauke Aprašas įveskite reikšmę.
7. Lauke Komponentas įveskite arba pasirinkite vertę.
    * Kiekvienas pakomponentis turi nurodyti į komponento aprašą. Šis dizainas palaiko pakartotinio naudojimo komponentus ir užtikrina, kad nustačius komponentą, jį galima naudoti daugelyje produkto modelių.  
8. Spustelėkite Įrašyti.
9. Spustelėkite KS eilutės informacija.
    * KS eilutės informacijos forma leidžia vartotojui pasirinkti reikiamas pakomponenčio ypatybes. Kiekvienai ypatybei gali būti suteikta fiksuota vertė arba ji gali būti susieta su atributu. Susiejus su atributu, bus gautos skirtingos KS eilutės ypatybės vertės, atsižvelgiant į konfigūracijos pasirinkimą.  
10. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Kiekvienas pakomponentis nurodo konfigūruojamą bendrąjį produktą su konfigūravimo pagal apribojimus technologija. Nuoroda pateikiama pagal prekės numerį.  
11. Pažymėkite žymės langelį Nustatyti.
12. Lauke Skaičiavimas pasirinkite Taip.
    * Nustačius skaičiavimo pasirinktį užtikrinama, kad produktas bus įtrauktas vykdant šio produkto savikainos skaičiavimą.  
13. Spustelėkite skirtuką Nustatymas.
14. Pažymėkite žymės langelį Nustatyti.
15. Lauke Kiekis įveskite skaičių.
    * Kiekio laukas nustato, kiek šio produkto bus suvartota sukonfigūruotam produktui.  
16. Pažymėkite žymės langelį Nustatyti.
17. Lauke Gaminių kiekiui įveskite skaičių.
18. Spustelėkite GERAI.

