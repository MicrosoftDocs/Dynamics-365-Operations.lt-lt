---
title: Min.–maks. papildymo proceso nustatymas
description: Šia procedūra paaiškinama, kaip nustatyti naują papildymo procesą, kuris naudoja minimalaus / maksimalaus papildymo strategiją.
author: perlynne
ms.date: 10/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence, WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12e5cc0bec937df45a3930aabeca0011723960e5532088c69a11074cf2d046a3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780875"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Min.–maks. papildymo proceso nustatymas

[!include [banner](../../includes/banner.md)]

Šia procedūra paaiškinama, kaip nustatyti naują papildymo procesą, kuris naudoja minimalaus / maksimalaus papildymo strategiją. Kai atsargos nukris žemiau minimalaus lygio, papildyti tai vietai bus sukurtas darbas. Šia procedūra taip pat rodoma, kaip naudojant fiksuotas paėmimo vietas leisti papildyti sandėlį, net jei atsargos nukrenta žemiau minimalaus lygio, ir kaip įgalinti reguliarų papildymo proceso vykdymą, naudojant paketinę užduotį. Šias užduotis paprastai turėtų atlikti sandėlio vadovas. Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF, naudodami toliau pateiktus reikšmių pavyzdžius, arba ją galite vykdyti su savo duomenimis. Jei naudojate savo duomenis, įsitikinkite, kad turite sandėlį, įgalintą sandėlio valdymo procesams.


## <a name="create-a-fixed-picking-location"></a>Fiksuotos paėmimo vietos kūrimas
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Sandėlis > Fiksuotos vietos**. Tai – neprivaloma min.–maks. papildymo užduotis, tačiau, jei naudojate fiksuotą paėmimo vietą, taip atsargas galima papildyti net jei jos nukrenta žemiau minimalaus lygio, nes sistema gali nustatyti, kurias prekes reikia papildyti, net jei jų nelikę.
2. Spustelėkite **Naujas**.
3. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti elementą „A0001“.  
4. Lauke **Teritorija** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti svetainę „2“.  
5. Lauke **Sandėlis** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti sandėlį „24“.  
6. Lauke **Vieta** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti „CP-003“.  
7. Uždarykite puslapį.

## <a name="create-a-replenishment-location-directive"></a>Papildymo vietos nurodymo kūrimas
1. Eikite į **Sandėlio valdymas > Sąranka > Vietos nurodymai**. Vietos nurodymai naudojami nustatyti, iš kur atliekant papildymo procesą reikėtų imti prekes.
2. Lauke **Darbo užsakymo tipas** pasirinkite Papildymas.
3. **Veiksmų srityje** spustelėkite **Nauja**.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Darbo tipas** pasirinkite Paimti.
6. Lauke **Teritorija** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti svetainę „2“.  
7. Lauke **Sandėlis** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti sandėlį „24“.  
8. Spustelėkite **Įrašyti**.
9. Dalyje **Eilutės** spustelėkite **Nauja**.
10. Sąraše pažymėkite pasirinktą eilutę.
11. Lauke **Galutinis kiekis** įveskite skaičių. Pavyzdžiui, galite nustatyti 9999.  
12. Pažymėkite žymės langelį **Leisti skaidyti**. Jei pasirinksite šią parinktį, atliekant darbo kūrimo procesą, darbo eilučių kiekius bus galima išskaidyti keliose vietose.  
13. Spustelėkite **Įrašyti**.
14. Dalyje **Vietos nurodymo veiksmai** spustelėkite **Naujas**.
15. Sąraše pažymėkite pasirinktą eilutę.
16. Lauke **Pavadinimas** įveskite reikšmę.
17. Spustelėkite **Įrašyti**.
18. Dalyje **Veiksmų sritis** spustelėkite **Redaguoti užklausą**. Šią užklausą galite redaguoti ir į ją įtraukti apribojimų, kad atsargas būtų galima pasirinkti atliekant papildymo procesą. Pavyzdžiui, gali būti, kad atsargas reikėtų naudoti tik iš sandėlio sandėliavimo vietos.
19. Spustelėkite **Gerai**.
20. Uždarykite puslapį.

## <a name="create-a-replenishment-work-template"></a>Papildymo darbo šablono kūrimas
1. Eikite į **Sandėlio valdymas > Sąranka > Darbas > Darbo šablonai**. Darbo šablonas naudojamas valdyti sistemai – kaip reikia kurti min. / maks. papildymo darbą. Turi būti bent paėmimo ir padėjimo darbo šablono eilutė. Jei nebus užpildyta visa reikalinga informacija, darbo šablonas negalios. 
2. Lauke **Darbo užsakymo tipas** pasirinkite Papildymas.
3. **Veiksmų srityje** spustelėkite **Nauja**.
4. Lauke **Darbo šablonas** įveskite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Dalyje **Darbo šablono informacija** spustelėkite **Naujas**.
7. Lauke **Darbo tipas** pasirinkite Paimti.
8. Lauke **Darbo klasės ID** įveskite arba pasirinkite reikšmę. Tai turėtų būti darbo klasė, susijusi su papildymu. Jei naudojate USMF, pasirinkite „Papildyti“.  
9. Dalyje **Darbo šablono informacija** spustelėkite **Naujas**.
10. Sąraše pažymėkite pasirinktą eilutę.
11. Lauke **Darbo tipas** pasirinkite „Padėjimas“.
12. Lauke **Darbo klasės ID** įveskite arba pasirinkite reikšmę.
13. Spustelėkite **Įrašyti**.
14. Uždarykite puslapį.

## <a name="create-a-new-replenishment-template"></a>Naujo papildymo šablono kūrimas
1. Eikite į **Sandėlio valdymas > Sąranka > Papildymas > Papildymo šablonai**. Papildymo šablonas naudojamas apibrėžti, kurias prekes, kiekius ir vietą reikia papildyti.
2. **Veiksmų srityje** spustelėkite **Nauja**.
3. Lauke **Papildymo šablonas** įveskite reikšmę. Sukurkite šablono pavadinimą, nurodantį, kad jis yra skirtas „min / maks“ papildymams.  
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Pažymėkite žymės langelį **Leisti poreikio bangai naudoti nerezervuotus kiekius**. Jei pasirenkate šią parinktį, atliekant bangos bangos paklausos papildymą galima vartoti kiekius, kurie yra susiję su min. / maks. papildymu. Pavyzdžiui, tai gali būti naudinga, jei „min / maks“ papildymo darbai neapdorojami iš karto, kad būtų išvengta papildomo ir nereikalingo papildymo.
6. Dalyje **Darbo šablono informacija** spustelėkite **Naujas**.
7. Lauke **Sekos skaičius** įveskite skaičių.
8. Lauke **Aprašo laukas** surinkite reikšmę.
9. Sąraše pažymėkite pasirinktą eilutę.
10. Lauke **Papildymo vienetas** įveskite arba pasirinkite reikšmę. Pvz., pasirinkite vnt. Šis parametras yra privalomas. Juo galima nurodyti papildymo darbo matavimo vienetą, kuris skiriasi nuo nurodyto šio šablono mažiausio ir didžiausio atsargų lygio vieneto.
11. Lauke **Darbo šablonas** įveskite arba pasirinkite reikšmę. Pasirinkite darbo šabloną, kurį sukūrėte anksčiau.  
12. Lauke **Mažiausias kiekis** įveskite skaičių. Pasirinkite mažiausią kiekį, kuris turėtų paleisti papildymą. Pavyzdžiui, nustatykite 50. Jei papildote fiksuotą vietą ir parinktis **Papildyti tuščias fiksuotas vietas** nustatyta į „Taip“, šį nustatymą galite palikti nustatytą į 0. Taip pat rekomenduojame pasirinkti parinktį **Papildyti atsargas tik fiksuotose vietose**, kad procesas būtų našesnis.
13. Lauke **Didžiausias kiekis** įveskite skaičių. Pavyzdžiui, nustatykite 100.  
14. Lauke **Vienetas** įveskite arba pasirinkite reikšmę. Priskirkite mažiausio ir didžiausio kiekių vienetą. Pavyzdžiui, nustatykite „vnt.‟.  
15. Pažymėkite žymės langelį **Papildyti tuščias fiksuotas vietas**. Pažymėkite šį žymės langelį, kad fiksuotas vietas papildytumėte, kai jos tuščios. Kitu atveju bus papildytos tik vietos, kuriose yra turimas kiekis.
16. Pažymėkite žymės langelį **Papildyti atsargas tik fiksuotose vietose**.
17. Spustelėkite **Pasirinkti produktus**. Tai yra vieta, kurioje galima apibrėžti, kuriuos produktus reikėtų papildyti. Jei pasirinkta parinktis Fiksuotos paėmimo vietos, tas vietas taip pat turite apibrėžti šioje užklausoje. Galima naudoti konkrečių variantų užklausas ir konkrečių produktų užklausas.
18. Pasirinkite eilutę **Prekės**.
19. Lauke **Kriterijai** įveskite reikšmę. Pasirinkite prekes, kurias reikėtų papildyti fiksuotose vietose. Pavyzdžiui, įveskite A*, kad pasirinktumėte visus prekių numerius, prasidedančius A.
20. Spustelėkite **Pridėti**. Įtraukite objektą Vieta (nebent jis jau yra), kad galėtumėte nustatyti, jog papildymo darbas turėtų būti atliekamas tik fiksuotose paėmimo vietose, esančiose konkrečioje sandėlio vietoje.
21. Sąraše pažymėkite pasirinktą eilutę.
22. Lauke **Lentelė** nustatykite Vietos.
23. Lauke **Laukas** pasirinkite Vietos profilio ID.
24. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.
25. Spustelėkite **Gerai**.
26. Uždarykite puslapį.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Nustatymas, kad papildymo procesas būtų vykdomas kaip paketinė užduotis
1. Eikite į **Sandėlio valdymas > Papildymas > Papildymai**. Puslapis „Papildymai“ leidžia nustatyti papildymą, kad jis būtų vykdomas kaip paketinė užduotis, arba reikalauti, kad jis būtų paleistas rankiniu būdu.
2. Spustelėkite **Filtras**.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.
5. Spustelėkite **Gerai**.
6. Išplėskite skyrių **Vykdyti fone**.
7. Parinktyje **Paketinis vykdymas** nustatykite Taip.
8. Spustelėkite **Pasikartojimas**.
9. Pasirinkite parinktį **Nėra pabaigos datos**.
10. Nustatykite **pasikartojimo modelį**. Pavyzdžiui, pasirinkite Dienos.  
11. Spustelėkite **Gerai**.
12. Spustelėkite **Gerai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]