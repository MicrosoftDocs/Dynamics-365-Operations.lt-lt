---
title: "Sandėlio konfigūracija"
description: "Šiame straipsnyje paaiškinta, kaip konfigūruoti sandėlį. Pateikiama informacija apie tai, kaip įgalinti sandėlio maketą ir sandėlio procesus."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-10-30 12 - 52 - 43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 437f2348603db432df6d7589e4043d8145c52a1e
ms.lasthandoff: 03/30/2017


---

# <a name="warehouse-configuration"></a>Sandėlio konfigūracija

Šiame straipsnyje paaiškinta, kaip konfigūruoti sandėlį. Pateikiama informacija apie tai, kaip įgalinti sandėlio maketą ir sandėlio procesus.

**Pastaba.** Šis straipsnis taikomas funkcijoms **Sandėlio valdymo** modulyje (patobulintas sandėliavimas). Jis nėra taikomas sandėlio funkcijoms **Atsargų valdymo** modulyje.

## <a name="warehouse-layout"></a>Sandėlio išdėstymas
Sandėlio valdymo sistema programoje „Microsoft Dynamics 365 for Operations‟ suteikia lanksčių būdų, kaip apibrėžti savo sandėlio išdėstymą, siekiant patenkinti kintančius poreikius, kad galėtumėte pasiekti optimalų sandėlio efektyvumą.

-   Galite nustatyti aukšto prioriteto ir žemo prioriteto saugojimo sritis, kad prekės būtų išdėstytos optimaliai.
-   Savo sandėlį galite padalinti į zonas, kad būtų galima patenkinti įvairius saugojimo poreikius, pvz., temperatūros reikalavimus ar įvairius prekių apyvartos koeficientus.
-   Nurodyti sandėlio vietas galite bet kokiu lygiu (pvz., teritorijos, sandėlo, perėjimo, stelažo, lentynos ir talpyklos padėties).
-   Grupuoti vietas galite naudodami fizinių pajėgumų apribojimo nuostatas.
-   Kontroliuoti, kaip prekės saugomos ir paimamos, galite pagal užklausomis apibrėžtas taisykles.

Norėdami naudoti „Microsoft Dynamics 365 for Operations‟ sandėlio valdymo funkcijas, turite sukurti sandėlį ir leisti jam taikyti labiau patobulinto ar specializuoto sandėlio valdymo veiklas. **Sandėlių** puslapyje pasirinkite parinktį **Naudoti sandėlio valdymo procesus**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Zonų grupės, zonos, vietų tipai ir vietos

Sandėlio išdėstymo įgalinimo proceso dalis yra apibrėžti sandėlio zonų grupes ir zonas, vietų profilius, vietų tipus bei vietas.

-   **Zonų grupės** – loginis arba fizinis sandėlio zonų grupavimas.
-   **Zonos** – loginis arba fizinis sandėlio vietų grupavimas.
-   **Vietų profiliai** – loginis arba fizinis vietų, kurių tos pačios sandėlio vietų proceso strategijos (pvz., ten gali būti saugomas skirtingų prekių numerių derinys ir taikomi tie patys fizinių pajėgumų apribojimai), grupavimas.
-   **Vietų tipai** – loginis arba fizinis sandėlio vietų grupavimas. Pavyzdžiui, galite sukurti vietos tipą visoms išdėstymo vietoms. Privalomosios nuostatos **Sandėlio valdymo parametrų** puslapyje yra laikino sandėliavimo vietų tipų ir galutinės siuntimo vietos tipo apibrėžimo pagrindas.
-   **Vietos** – žemiausias vietos informacijos lygis. Vietos naudojamos sekti, kur sandėlyje saugomos ir paimamos turimos atsargos.

Objektai, kuriuos kuriate norėdami apibrėžti sandėlio išdėstymą, naudojami užklausose, kurias nustatote darbo šablonuose, taip sandėlyje apdorojant darbo užsakymus. Todėl apibrėždami zonas, vietų tipus ir t. t. atsižvelkite į tai, kaip skirtingiems procesams naudojamos skirtingos sandėlio sritys. Be to, atsižvelkite į tokius konkrečios srities veiksnius kaip fizinės charakteristikos. Pavyzdžiui, gali būti sričių, kur jūs galite naudoti tik tam tikro tipo šakiniai krautuvai. Arba, jei jūsų įmonė turi gamybos ir gatavų prekių per toje pačioje patalpoje, galbūt norėsite sukurti vieno sandėlio Dynamics 365 operacijoms bet tada atskirti šių dviejų operacijų dvi zonos grupių kūrimas. Duoti savo subjektai aprašomuosius pavadinimus, kad nesunku atpažinti juos, kai jas naudojate šabloną užklausose.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Vietų sandėliavimo apribojimai, vietų profiliai ir fiksuotos paėmimo vietos

Turite atsižvelgti į fizinį sandėlo išdėstymą: tiek nustatyti saugojimo pajėgumams (vietų sandėliavimo apribojimams ir vietų profiliams), tiek vėlgi mėginant pasiekti optimalių sandėlio procesų. 

Vietos gyvulių ribų padės užtikrinti, kad darbo nėra sukurta prašyti, kad atsargų perjungtos į vietą, kurios neturi fizinės vietos aprašą. Pavyzdžiui, jei kai kuriose vietose per sandėlį gali turėti tik vieną padėklą vietai, vieta Kojinė ribos gali būti įjungta. Į ** kiekis ** vertę galima nustatyti, kad **1**, ir ** vieneto ** vertę galima nustatyti **PL** profilis grupėje konkrečioje vietoje. 

Jei, norint kontroliuoti vietų pajėgumų apribojimus, reikia atlikti labiau išplėstinių skaičiavimų, galima naudoti vietų profilių nuostatas. Tokiu atveju, atliekant pajėgumų skaičiavimus, atsižvelgiama į svorį ir tūrį. 

Norint pasiekti optimalių išsiuntimo procesų, reikėtų įvertinti, ar reikia naudoti fiksuotas paėmimo vietas ir / arba pakavimo vietas. Dažnai papildymo iš sandėliavimo vietos į fiksuotas paėmimo vietas procesuose naudojamas minimalaus / maksimalaus papildymas, ir tame pačiame sandėlyje bei produktų variantams galima įgalinti kelias fiksuotas paėmimo vietas. Apsvarstykite, kokio lankstumo galėtumėte pasiekti, įgalindami paskirtąsias poreikio papildymo perviršio vietas, kurios naudojamos tik apdorojant bangos / krovinio papildymą.

### <a name="location-setup-wizard"></a>Vietos nustatymo vedlys

Norėdami greitai sukurti kaip sandėlio vietas, galite naudoti su ** vietos nustatymo ** vedlys. Vykdydami šį procesą, galite lengvai išlaikyti vietų pavadinimų formatą.

## <a name="warehouse-processes"></a>Sandėlio procesai
Svarbu, kad, atlikdami sandėlio konfigūraciją, sandėlio procesus įgalintumėte pagal verslo reikalavimus. Svarbiausi komponentai, kuriuos turite sukonfigūruoti, yra bangos šablonai, darbo šablonai, darbo telkiniai ir vietų nurodymai.

### <a name="wave-templates"></a>Bangos šablonai

Bangos šablonai padeda įgalinti siuntimo procesą „Išleisti į sandėlį‟. Vos tik išleidžiamos užsakymo eilutės (tiesiogiai iš šaltinio dokumentų, naudojant paketinių užduočių procesus arba naudojant jau sukurtus krovinius), naudojamos bangos šablono funkcijos. 

Galite sukurti trijų rūšių banga šablonai: **pristatymas**, **gamybos užsakymo**, ir **Kanban**. Parametrai yra naudojami nustatyti, kiek sistema turi automatiškai pereiti išvykstamasis darbas perdirbimo. Bangos šablonas pasirenkamas pagal bangos šablonų seką ir kriterijus, nurodytus šablone. Jei šablonas pateikiamas sekos viršuje, pirmiausia tikrinami to šablono kriterijai. Jei kriterijus galima patenkinti, bangos šablonas apdorojamas. Kitu atveju tikrinami kito šablono kriterijai ir t. t. Todėl naudinga bangos šablonų sekos sąrašo viršuje padėti šabloną su konkrečiausiais kriterijais, kad jis būtų apdorojamas pirmiausia. Pvz., šiandien norite apdoroti visą konkretaus vežėjo darbą, o kitų vežėjų darbo apdorojimą laikinai atidėti. Šiuo atveju aukščiau už kitus šablonus sekoje turėtų būti pateiktas bangos šablonas, kuriuo pasirenkamas to vežėjo darbas. Kitu atveju kitų vežėjų darbas gali būti apdorotas dar nebaigus to vežėjo darbo. 

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

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Konfigūruoti vietose WMS palaikantis sandėlyje (darbo vadovas)](https://ax.help.dynamics.com/en/wiki/configure-locations-in-a-wms-enabled-warehousing/)


