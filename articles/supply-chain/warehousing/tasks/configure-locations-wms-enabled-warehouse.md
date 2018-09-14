--- 
title: "Sandėlio, kuriame veikia WMS, vietų konfigūravimas"
description: "Šiame vadove aprašoma, kaip konfigūruoti naujo sandėlio, kuriame veikia WMS (sandėlio, kuriame naudojami patobulinti sandėlio valdymo procesai) vietos nustatymą."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1082c86361180db84bb2b5c0b8158816f76a219e
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Sandėlio, kuriame veikia WMS, vietų konfigūravimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame vadove aprašoma, kaip konfigūruoti naujo sandėlio, kuriame veikia WMS (sandėlio, kuriame naudojami patobulinti sandėlio valdymo procesai) vietos nustatymą. Šį procesą paprastai atlieka sandėlio vadovas. Šią vadovą galite paleisti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Galioja išankstinė sąlyga, kad turėtumėte sukonfigūruotą bent vieną vietą.


## <a name="create-a-new-warehouse"></a>Naujo sandėlio kūrimas
1. Eikite į Sandėliai.
2. Spustelėkite Naujas.
3. Lauke Sandėlis surinkite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Teritorija surinkite reikšmę.
6. Išplėskite arba sutraukite sekciją Sandėlis.
7. Nustatykite parinkties Naudoti sandėlio valdymo procesus padėtį Taip.
    * Šis nustatymas leidžia vykdyti išankstinius sandėliavimo procesus, naudojant sandėlio darbą ir mobiliuosius įrenfinius.  
8. Uždarykite puslapį.

## <a name="define-a-location-format"></a>Vietos formato nustatymas
1. Eikite į Vietos formatai.
    * Vietų formatai yra vardų sistema, naudojama siekiant sukurti unikalius ir nuoseklius sandėlyje naudojamų skirtingoms vietos talpyklos padėtims skirtus pavadinimus. Kaip vietos formatą gali būti naudinga naudoti skyriklius, kad būtų lengviau nustatyti vietos komponentus, pavyzdžiui, perėjimo numerį. Šiame pavyzdyje mes sukursime pavadinimą su keturiais komponentais. Šie komponentai gali būti, pavyzdžiui, perėjimas, stelažas, lentyna ir talpykla.  
2. Spustelėkite Naujas.
3. Lauke Vietos formatas įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Segmento aprašas įveskite reikšmę.
    * Čia aprašoma, ką nurodo vietos pavadinimo pirmasis komponentas. Pavyzdžiui, tai gali būti Perėjimas.  
6. Lauke Ilgis įveskite skaičių.
    * Nustatoma, kiek simbolių turi būti šioje vietos pavadinimo dalyje. Atkreipkite dėmesį, iš viso pavadinime negali būti daugiau negu 10 simbolių, įskaitant skyriklius.  
7. Lauke Skyriklis įveskite reikšmę.
    * Taip nurodoma, koks simbolis naudojamas tarp pirmojo ir antrojo pavadinimo komponento.  
8. Spustelėkite Naujas.
9. Lauke Segmento aprašas įveskite reikšmę.
10. Lauke Ilgis įveskite skaičių.
11. Lauke Skyriklis įveskite reikšmę.
12. Spustelėkite Naujas.
13. Lauke Segmento aprašas įveskite reikšmę.
14. Lauke Ilgis įveskite skaičių.
15. Lauke Skyriklis įveskite reikšmę.
16. Spustelėkite Naujas.
17. Lauke Segmento aprašas įveskite reikšmę.
18. Lauke Ilgis įveskite skaičių.
19. Spustelėkite Įrašyti.
20. Uždarykite puslapį.

## <a name="define-location-types"></a>Vietų tipų nustatymas
1. Eikite į Vietos tipai.
    * Vietų tipus galima naudoti kaip filtravimo parinktis, kad būtų galima kontroliuoti skirtingus sandėlio valdymo procesus. Tam, kad galėtumėte apibrėžti siuntimo sandėlio valdymo procesą, turite sukurti bent jau išdėstymo ir galutinės siuntimo vietos tipus.  
2. Spustelėkite Naujas.
3. Lauke „Vietos tipas“ įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Uždarykite puslapį.

## <a name="define-location-profile"></a>Vietos šablono nustatymas
1. Eikite į Vietos šablonai.
    * Vietos šablonų apibrėžimas yra labai svarbus. Sugrupuotų vietų pajėgumą galima kontroliuoti čia, taip pat galima kontroliuoti, su kokiomis atsargomis susijusios strategijos bus išsaugotos ir kaip jos bus išsaugotos. Vietų šablonus galima naudoti kaip filtravimo parinktis, kad būtų galima kontroliuoti skirtingus sandėlio valdymo procesus. Norėdami įjungti sandėlio valdumo procesus, turite sukurti bent jau vartotojo vietos profilį.  
2. Spustelėkite Naujas.
3. Lauke Vietos šablono ID įveskite vertę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Vietos formatas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke Vietos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Pažymėkite arba atžymėkite žymės langelį Leisti įvairias atsargų būsenas.
    * Įgalinkite šią pasirinktį, jei norite leisti įvairias atsargų būsenos vertes, kurios bus naudojamos šio vietos šablono grupuojamose vietose.  
12. Pažymėkite arba atžymėkite žymės langelį Nepaisyti paketo dienų taisyklių.
    * Įgalinkite šią pasirinktį, norėdami nepaisyti taisyklės tiek dienų, kiek skirsis atsargų paketo galiojimo datos, kad galėtumėte maišyti šiai taisyklei nepaklūstančius atsargų paketus.  
13. Pažymėkite arba išvalykite žymės langelį Leisti ciklo skaičiavimą.
    * Įgalinkite šią pasirinktį, jei norite leisti apdoroti ciklo skaičiavimo procesą visose šio vietos šablono grupuojamose vietose.  
14. Išplėskite arba sutraukite sekciją Dimensijos.
    * Dimensijų skirtukas leidžia nustatyti parametrus ir metodus, kuriais naudodamiesi galite tiksliai apskaičiuoti kiekvienos vietos pajėgumą.  
15. Uždarykite puslapį.

## <a name="enable-warehouse-management-parameters"></a>Sandėlio valdymo parametrų įgalinimas
1. Eikite į Sandėlio valdymo parametrai.
    * Tam, kad būtų galima apdoroti sandėlio darbą, turite nustatyti vartotojo vietos šablono išdėstymo vietos tipo parametrus ir galutinės siuntimo vietos tipą. Kai siuntimo procesas baigiasi jūsų nurodytu galutinės siuntimo vietos tipu, susijusių siunčiamų operacijų būsena atnaujinama į „Paimta“.  
2. Išplėskite arba sutraukite sekciją Vietos šablonai.
3. Lauke Vartotojo vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Išplėskite arba sutraukite sekciją Vietų tipai.
6. Lauke Surinkimo vietos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke Galutinės siuntimo vietos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše spustelėkite saitą pasirinktoje eilutėje.
10. Uždarykite puslapį.

## <a name="define-warehouse-zone-groups"></a>Sandėlio zonų grupių nustatymas
1. Eikite į Sandėlio zonų grupės.
    * Sandėlio zonas galima naudoti kaip parinkčių filtrus, kad būtų galima kontroliuoti skirtingus sandėlio valdymo procesus. Prieš nurodydami zoną turite sukurti zonų grupę.  
2. Spustelėkite Naujas.
3. Lauke Zonų grupės ID įveskite vertę.
4. Lauke Zonų grupės pavadinimas įveskite vertę.
5. Uždarykite puslapį.

## <a name="define-warehouse-zones"></a>Sandėlio zonų nustatymas
1. Eikite į Zonos.
2. Spustelėkite Naujas.
3. Lauke Zonos ID įveskite vertę.
4. Lauke Zonos pavadinimas įveskite vertę.
5. Lauke Zonų grupės ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Uždarykite puslapį.

## <a name="create-locations-using-the-location-setup-wizard"></a>Vietų kūrimas naudojant vietos nustatymo vedlį
1. Eikite į Vietos nustatymo vedlys.
2. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke Zonos ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke Vietos šablono ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Sąraše pažymėkite pasirinktą eilutę.
12. Lauke Nuo numerio įveskite numerį.
    * Laukuose Nuo numerio ir Iki numerio nurodoma, kiek vietų bus sukurta. Pvz., jei visoms keturioms vietos formato eilutėms Nuo numerio nurodote 1, o Iki numerio – 3, bus sukurta 81 vieta (3x3x3x3).  
13. Lauke Iki numerio įveskite numerį.
14. Sąraše raskite ir pasirinkite norimą įrašą.
15. Lauke Nuo numerio įveskite numerį.
16. Lauke Iki numerio įveskite numerį.
17. Sąraše raskite ir pasirinkite norimą įrašą.
18. Lauke Nuo numerio įveskite numerį.
19. Lauke Iki numerio įveskite numerį.
20. Sąraše raskite ir pasirinkite norimą įrašą.
21. Lauke Nuo numerio įveskite numerį.
22. Lauke Iki numerio įveskite numerį.
23. Spustelėkite Kurti.

## <a name="create-locations-manually"></a>Vietų kūrimas rankiniu būdu
1. Eikite į Vietos.
    * Galima lengvai rankiniu būdu kurti sandėlio vietas. Vietos pavadinimo ir vietos šablono ID reikšmės yra privalomos.  
2. Spustelėkite Naujas.
3. Lauke Sandėlis surinkite reikšmę.
4. Lauke Vieta surinkite reikšmę.
    * Atkreipkite dėmesį, kad čia jūs kuriate naują vietą, todėl reikia įvesti naują unikalų pavadinimą, o ne pasirinkti vieną iš esamų.  
5. Lauke Vietos šablono ID įveskite vertę.
6. Uždarykite puslapį.

## <a name="define-pack-size-categories"></a>Paketų dydžių kategorijų nustatymas
1. Eikite į Paketų dydžių kategorijos.
    * Paketo dydžio kategorijas galima naudoti norint grupuoti prekes, kurių paketų dydžiai panašūs. Šiame pavyzdyje paketo dydžio kategorija bus naudojama norint kontroliuoti pajėgumą konkrečiose sandėlio paėmimo vietose. Atkreipkite dėmesį, kad paketo dydžio kategorijos ID turi būti priskirtas prie išleisto produkto objekto, kad jį būtų galima panaudoti kaip sandėliavimo limitų apdorojimo dalį.  
2. Spustelėkite Naujas.
3. Lauke Paketo dydžio kategorijos ID įveskite vertę.
4. Lauke Paketo dydžio kategorijos pavadinimas įveskite vertę.
5. Uždarykite puslapį.

## <a name="define-location-stocking-limits"></a>Vietos sandėliavimo apribojimų apibrėžimas
1. Eikite į Vietų sandėliavimo limitai.
    * Vietos sandėliavimo limitai padeda norint įsitikinti, kad sukūrus darbą atsargas būtų prašoma padėtį ne į tokią vietą, kuri būtų fiziškai nepajėgi jų sutalpinti.  
2. Spustelėkite Naujas.
3. Lauke Sandėlis surinkite reikšmę.
4. Lauke Vietos šablono ID įveskite vertę.
5. Lauke Paketo dydžio kategorijos ID įveskite vertę.
6. Lauke Kiekis įveskite skaičių.
7. Spustelėkite Įrašyti.
8. Uždarykite puslapį.

## <a name="define-fixed-picking-locations"></a>Fiksuotų paėmimo vietų nustatymas
1. Eikite į Fiksuotos vietos.
    * Galite nurodyti kiekvienam produktui arba produkto variantui naudotinas vietas. Galima sukurti keletą to paties produkto, esančio tame pačiame sandėlyje, fiksuotų vietų.  
2. Spustelėkite Naujas.
3. Lauke Prekės numeris surinkite reikšmę.
4. Lauke Sandėlis surinkite reikšmę.
5. Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Uždarykite puslapį.


