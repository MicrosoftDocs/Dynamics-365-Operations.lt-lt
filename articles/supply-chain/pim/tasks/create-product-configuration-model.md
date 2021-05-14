---
title: Kurti produkto konfigūracijos modelį
description: Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921370"
---
# <a name="create-a-product-configuration-model"></a>Kurti produkto konfigūracijos modelį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip kurti produkto konfigūracijos modelį ir įvesti pagrindinę informaciją, pvz., atributus ir pakomponenčius. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-product-model"></a>Produkto modelio kūrimas

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Pasirinkite **Naujas**.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Lauke **Aprašo laukas** surinkite reikšmę.
1. Lauke **Sprendimo priemonės** strategija pasirinkite pasirinktį.
    * Sprendimo priemonės strategija nustato, kaip tvarkomi produktų konfigūravimo pagal apribojimus modelio apribojimai. Šis pasirinkimas gali turėti įtakos produkto konfigūracijos modelio našumui.  
1. Lauke **Pavadinimas** įveskite reikšmę.
    * Šakninis komponentas nurodo produkto konfigūracijos modelį, tačiau jį galima naudoti kituose produkto modeliuose.  
1. Pasirinkite **Gerai**.
1. Lauke **Pakartotinai naudoti** konfigūracijas pasirinkite pasirinktį.
    * Jei pakartotinis konfigūracijos parametras yra nustatytas į Taip, sistema patikrins, ar yra identiškų konfigūracijų po kiekvieno konfigūracijos seanso ir pakartotinai jas naudos, jei ras tikslų atitikimą.  

## <a name="add-attributes"></a>Įtraukti atributų

1. Išplėskite skyrių **Atributai**.
2. Pasirinkite **Įtraukti**.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Sprendimo priemonės** pavadinimas įveskite vertę.
    * Produkto konfigūravimo priemonė apribojimo sprendimo priemonė naudoja Sprendimo priemonės pavadinimą. Jame negali būti tarpų arba specialiųjų simbolių, išskyrus _ (pabraukimo brūkšnys).  
6. Lauke **Aprašo laukas** surinkite reikšmę.
    * Aprašo tekstas rodomas konfigūracijos vartotojui ir todėl gali padėti pasirenkant tinkamą atributo vertę.  
7. Lauke **Atributo tipas** įveskite arba pasirinkite vertę.
    * Atributo tipas nustato, kurios vertės yra galimos atributui.  
8. Pažymėkite **Įtraukti į pakartotinį naudojimą** laukelį.
    * Ši pasirinktis galima tik tokiu atveju, jei pasirinkta pasirinktis Pakartotinai naudoti konfigūracijas. Įtraukiant atributą į pakartotinio naudojimą žymės langelį reiškia, kad šis atributas bus svarstomas, kai sistema ieškos tikslaus atitikimo.  

## <a name="add-subcomponents"></a>Įtraukti pakomponenčius

1. Išplėskite skyrių **Pakomponenčiai**.
2. Pasirinkite **Įtraukti**.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Sprendimo priemonės** pavadinimas įveskite vertę.
6. Lauke **Aprašo laukas** surinkite reikšmę.
7. Lauke **Komponentas** įveskite arba pasirinkite vertę.
    * Kiekvienas pakomponentis turi nurodyti į komponento aprašą. Šis dizainas palaiko pakartotinio naudojimo komponentus ir užtikrina, kad nustačius komponentą, jį galima naudoti daugelyje produkto modelių.  
8. Pasirinkite **Įrašyti**.
9. Pasirinkite **BOM eilutės** informaciją.
    * KS eilutės informacijos forma leidžia vartotojui pasirinkti reikiamas pakomponenčio ypatybes. Kiekvienai ypatybei gali būti suteikta fiksuota vertė arba ji gali būti susieta su atributu. Susiejus su atributu, bus gautos skirtingos KS eilutės ypatybės vertės, atsižvelgiant į konfigūracijos pasirinkimą.  
10. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
    * Kiekvienas pakomponentis nurodo konfigūruojamą bendrąjį produktą su konfigūravimo pagal apribojimus technologija. Nuoroda pateikiama pagal prekės numerį.  
11. Pažymėkite **Nustatyti** laukelį.
12. Lauke **Skaičiavimas** pasirinkite **Taip**.
    * Nustačius skaičiavimo pasirinktį užtikrinama, kad produktas bus įtrauktas vykdant šio produkto savikainos skaičiavimą.  
13. Pasirinkite skirtuką **Nustatymas**.
14. Pažymėkite **Nustatyti** laukelį.
15. Lauke **Kiekis** įveskite skaičių.
    * Kiekio laukas nustato, kiek šio produkto bus suvartota sukonfigūruotam produktui.  
16. Pažymėkite **Nustatyti** laukelį.
17. Lauke **Pagal serijas** įveskite skaičių.
18. Pasirinkite **Gerai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]