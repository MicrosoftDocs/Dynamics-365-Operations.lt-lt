---
title: Sandėlio konfigūracijos apžvalga
description: Šiame straipsnyje paaiškinta, kaip konfigūruoti sandėlį. Pateikiama informacija apie tai, kaip įgalinti sandėlio maketą ir sandėlio procesus.
author: perlynne
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11554"
- intro-internal
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 091eb23397ed8f8efb50db6acba956fc49ef5a044a7d5fcc9d1e3201a68d54fe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755911"
---
# <a name="warehouse-configuration-overview"></a>Sandėlio konfigūracijos apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip konfigūruoti sandėlį. Pateikiama informacija apie tai, kaip įgalinti sandėlio maketą ir sandėlio procesus.

> [!NOTE]
> Šis straipsnis taikomas funkcijoms **Sandėlio valdymas** modulyje (patobulintas sandėliavimas). Jis nėra taikomas sandėlio funkcijoms **Atsargų valdymo** modulyje.

## <a name="warehouse-layout"></a>Sandėlio išdėstymas
Sandėlio valdymo sistema programoje „Supply Chain Management“ suteikia lanksčių būdų, kaip apibrėžti savo sandėlio išdėstymą, siekiant patenkinti kintančius poreikius, kad galėtumėte pasiekti optimalų sandėlio efektyvumą.

-   Galite nustatyti aukšto prioriteto ir žemo prioriteto saugojimo sritis, kad prekės būtų išdėstytos optimaliai.
-   Savo sandėlį galite padalinti į zonas, kad būtų galima patenkinti įvairius saugojimo poreikius, pvz., temperatūros reikalavimus ar įvairius prekių apyvartos koeficientus.
-   Nurodyti sandėlio vietas galite bet kokiu lygiu (pvz., teritorijos, sandėlio, perėjimo, stelažo, lentynos ir talpyklos padėties).
-   Grupuoti vietas galite naudodami fizinių pajėgumų apribojimo nuostatas.
-   Kontroliuoti, kaip prekės saugomos ir paimamos, galite pagal užklausomis apibrėžtas taisykles.

Norėdami naudoti „Supply Chain Management‟ sandėlio valdymo funkcijas, turite sukurti sandėlį ir leisti jam taikyti labiau patobulinto ar specializuoto sandėlio valdymo veiklą. **Sandėlių** puslapyje pasirinkite parinktį **Naudoti sandėlio valdymo procesus**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Zonų grupės, zonos, vietų tipai ir vietos

Sandėlio išdėstymo įgalinimo proceso dalis yra apibrėžti sandėlio zonų grupes ir zonas, vietų profilius, vietų tipus bei vietas.

-   **Zonų grupės** – loginis arba fizinis sandėlio zonų grupavimas.
-   **Zonos** – loginis arba fizinis sandėlio vietų grupavimas.
-   **Vietų profiliai** – loginis arba fizinis vietų, kurių tos pačios sandėlio vietų proceso strategijos (pvz., ten gali būti saugomas skirtingų prekių numerių derinys ir taikomi tie patys fizinių pajėgumų apribojimai), grupavimas.
-   **Vietų tipai** – loginis arba fizinis sandėlio vietų grupavimas. Pavyzdžiui, galite sukurti vietos tipą visoms išdėstymo vietoms. Privalomosios nuostatos **Sandėlio valdymo parametrų** puslapyje yra laikino sandėliavimo vietų tipų ir galutinės siuntimo vietos tipo apibrėžimo pagrindas.
-   **Vietos** – žemiausias vietos informacijos lygis. Vietos naudojamos sekti, kur sandėlyje saugomos ir paimamos turimos atsargos.

Objektai, kuriuos kuriate norėdami apibrėžti sandėlio išdėstymą, naudojami užklausose, kurias nustatote darbo šablonuose, taip sandėlyje apdorojant darbo užsakymus. Todėl apibrėždami zonas, vietų tipus ir t. t. atsižvelkite į tai, kaip skirtingiems procesams naudojamos skirtingos sandėlio sritys. Be to, atsižvelkite į tokius konkrečios srities veiksnius kaip fizinės charakteristikos. Pavyzdžiui, gali būti sričių, kuriose galite naudoti tik tam tikro tipo krautuvą. Arba jei tos pačios jūsų įmonės patalpos naudojamos ir gamybai, ir pagamintoms prekėms, galbūt norėsite programoje „Supply Chain Management“ sukurti vieną sandėlį, tačiau tada sukurti dvi zonų grupes ir tokiu būdu šias dvi operacijas atskirti. Objektams suteikite aprašomuosius pavadinimus – tuomet šablonų užklausose naudojant objektus bus lengva juos identifikuoti.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Vietų sandėliavimo apribojimai, vietų profiliai ir fiksuotos paėmimo vietos

Turite atsižvelgti į fizinį sandėlio išdėstymą: tiek nustatyti saugojimo pajėgumams (vietų sandėliavimo apribojimams ir vietų profiliams), tiek mėginant pasiekti optimalių sandėlio procesų. 

Taikant vietų sandėliavimo apribojimus užtikrinama, kad sukūrus darbą atsargas bus prašoma padėti ne į tokią vietą, kuri būtų fiziškai nepajėgi jų sutalpinti. Pavyzdžiui, jei tam tikrose sandėlio vietose galima sandėliuoti tik po vieną padėklą, tuomet galima įjungti vietų sandėliavimo apribojimus. Konkrečioje vietų profilių grupėje **Kiekio** reikšmę galima nustatyti į **1**, o **Vieneto** reikšmę galima nustatyti į **PL**. 

Jei, norint kontroliuoti vietų pajėgumų apribojimus, reikia atlikti labiau išplėstinių skaičiavimų, galima naudoti vietų profilių nuostatas. Tokiu atveju, atliekant pajėgumų skaičiavimus, atsižvelgiama į svorį ir tūrį. 

Norint pasiekti optimalių išsiuntimo procesų, reikėtų įvertinti, ar reikia naudoti fiksuotas paėmimo vietas ir / arba pakavimo vietas. Dažnai papildymo iš sandėliavimo vietos į fiksuotas paėmimo vietas procesuose naudojamas minimalaus / maksimalaus papildymas, ir tame pačiame sandėlyje bei produktų variantams galima įgalinti kelias fiksuotas paėmimo vietas. Apsvarstykite, kokio lankstumo galėtumėte pasiekti, įgalindami paskirtąsias poreikio papildymo perviršio vietas, kurios naudojamos tik apdorojant bangos / krovinio papildymą.

### <a name="location-setup-wizard"></a>Vietos nustatymo vedlys

Norėdami greitai sandėlyje sukurti vietų, galite naudoti **Vietos sąrankos** vedlį. Vykdydami šį procesą, galite lengvai išlaikyti vietų pavadinimų formatą.

## <a name="warehouse-processes"></a>Sandėlio procesai
Svarbu, kad, atlikdami sandėlio konfigūraciją, sandėlio procesus įgalintumėte pagal verslo reikalavimus. Svarbiausi komponentai, kuriuos turite sukonfigūruoti, yra bangos šablonai, darbo šablonai, darbo telkiniai ir vietų nurodymai.

### <a name="wave-templates"></a>Bangos šablonai

Bangos šablonai padeda įgalinti siuntimo procesą „Išleisti į sandėlį‟. Vos tik išleidžiamos užsakymo eilutės (tiesiogiai iš šaltinio dokumentų, naudojant paketinių užduočių procesus arba naudojant jau sukurtus krovinius), naudojamos bangos šablono funkcijos. 

Galite kurti trijų toliau nurodytų tipų bangos šablonus. 
-   **Siuntimas**
-   **Gamybos užsakymas**
-   **Kanban** 

Parametrai naudojami nustatant sistemos automatinio veikimo lygį, kuris bus taikomas apdorojant siuntimo darbą. Bangos šablonas pasirenkamas pagal bangos šablonų seką ir kriterijus, nurodytus šablone. Jei šablonas pateikiamas sekos viršuje, pirmiausia tikrinami to šablono kriterijai. Jei kriterijus galima patenkinti, bangos šablonas apdorojamas. Kitu atveju tikrinami kito šablono kriterijai ir t. t. Todėl naudinga bangos šablonų sekos sąrašo viršuje padėti šabloną su konkrečiausiais kriterijais, kad jis būtų apdorojamas pirmiausia. Pvz., šiandien norite apdoroti visą konkretaus vežėjo darbą, o kitų vežėjų darbo apdorojimą laikinai atidėti. Šiuo atveju aukščiau už kitus šablonus sekoje turėtų būti pateiktas bangos šablonas, kuriuo pasirenkamas to vežėjo darbas. Kitu atveju kitų vežėjų darbas gali būti apdorotas dar nebaigus to vežėjo darbo. 

Kiekviename bangos šablone turite nurodyti bangos apdorojimo metodus. Galimi metodai skiriasi – tai priklauso nuo bangos šablono tipo.

### <a name="work-templates"></a>Darbo šablonai

Apibrėžiant sandėlio valdymo darbo procesus, svarbų vaidmenį atlieka darbo šablonų apibrėžtys. Jos apibrėžia, koks ir kaip atliekamas darbas. Šablonuose taip pat gali būti krypties kodas, kuris nurodo į vietos nurodymą, kad būtų galima nustatyti, kur atliekamas darbas. Darbo šablonuose yra užklausa, kuri nurodo darbo kriterijus. Kiekviename šablone turi būti bent viena Paėmimo operacija ir viena Padėjimo operacija, kad būtų galima vykdyti pagrindinę turimų atsargų perkėlimo iš vienos vietos į kitą darbo operaciją. 

Jei kai kurių jūsų sandėlio operacijų darbą apdoroti turi gebėti keli darbuotojai, galbūt norėsite naudoti atsargų *laikino sandėliavimo* sąvoką ir darbo vykdymą išskirstyti skirtingoms darbo klasėms.

### <a name="work-pools"></a>Darbo telkiniai

Darbo telkiniai naudojami skirstant darbą į grupes. Pavyzdžiui, galite sukurti darbo telkinį, kuris apibūdina darbą, atliekamą konkrečioje sandėlio vietoje. Visų tipų, išskyrus skaičiavimą, darbo telkinius galite priskirti darbo šablonui. Atlikdami ciklo skaičiavimą, darbo telkinį galite priskirti toliau nurodytuose puslapiuose.

-   Ciklo skaičiavimo planai
-   Ciklo skaičiavimo ribinės reikšmės
-   Ciklų skaičiavimo darbas pagal vietą
-   Ciklų skaičiavimo darbas pagal prekę

Jei naudojate darbo šablonus darbui kurti, darbo telkinys automatiškai priskiriamas darbui. 

Jei tokia funkcija yra sukonfigūruota atitinkamame mobiliojo įrenginio meniu elemente, darbo telkinių ID taip pat galima naudoti norint apriboti darbo tipus, nukreipiamus konkrečiam sandėlio darbuotojui.

### <a name="location-directives"></a>Vietos nurodymai

Kaip galima spręsti iš pavadinimo, vietos nurodymai naudojami darbo operacijoms nukreipti į atitinkamas sandėlio vietas. Kitaip tariant, jie apibrėžia, kur paimti ir padėti. 

Kad būtų lengviau ir greičiau apibrėžti veiksmus, susietus su kiekviena vietos nurodymo eilute, naudokite vieną iš iš anksto apibrėžtų strategijų. Pvz., norėdami sandėlyje ieškoti laisvos vietos, galite naudoti strategiją **Tuščia vieta, kurioje negaunama darbo** arba galite naudoti siuntimo pardavimo išrinkimo strategiją **FEFO paketo rezervavimas**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sandėlio, kuriame veikia WMS, vietų konfigūravimas](tasks/configure-locations-wms-enabled-warehouse.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]