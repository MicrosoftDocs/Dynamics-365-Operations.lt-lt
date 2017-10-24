--- 
title: "Min.–maks. papildymo proceso nustatymas"
description: "Šia procedūra paaiškinama, kaip nustatyti naują papildymo procesą, kuris naudoja minimalaus / maksimalaus papildymo strategiją."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>Min.–maks. papildymo proceso nustatymas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra paaiškinama, kaip nustatyti naują papildymo procesą, kuris naudoja minimalaus / maksimalaus papildymo strategiją. Kai atsargos nukris žemiau minimalaus lygio, papildyti tai vietai bus sukurtas darbas. Šia procedūra taip pat rodoma, kaip naudojant fiksuotas paėmimo vietas leisti papildyti sandėlį, net jei atsargos nukrenta žemiau minimalaus lygio, ir kaip įgalinti reguliarų papildymo proceso vykdymą, naudojant paketinę užduotį. Šias užduotis paprastai turėtų atlikti sandėlio vadovas. Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF, naudodami pastabų reikšmių pavyzdžius, arba ją galite vykdyti su savo duomenimis. Jei naudojate savo duomenis, įsitikinkite, kad turite sandėlį, kuriame galima atlikti sandėlio valdymo procesus.


## <a name="create-a-fixed-picking-location"></a>Fiksuotos paėmimo vietos kūrimas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlis > Fiksuotos vietos.
    * Tai – neprivaloma min.–maks. papildymo užduotis, tačiau, jei naudojate fiksuotą paėmimo vietą, taip atsargas galima papildyti net jei jos nukrenta žemiau minimalaus lygio, nes sistema gali nustatyti, kurias prekes reikia papildyti, net jei jų nelikę.  
2. Spustelėkite Naujas.
3. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti prekę A0001.  
4. Lauke Teritorija įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti 2-ąją vietą.  
5. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti 24-ąjį sandėlį.  
6. Lauke Vieta įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti CP-003.  
7. Uždarykite puslapį.

## <a name="create-a-replenishment-location-directive"></a>Papildymo vietos nurodymo kūrimas
1. Pasirinkite Sandėlio valdymas > Nustatymai > Vietos nurodymai.
    * Vietos nurodymai naudojami nustatyti, iš kur atliekant papildymo procesą reikėtų imti prekes.  
2. Lauke Darbo užsakymo tipas pasirinkite Papildymas.
3. Spustelėkite Naujas.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Darbo tipas pasirinkite 'Paimti'.
6. Lauke Teritorija įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti 2-ąją vietą.  
7. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti 24-ąjį sandėlį.  
8. Spustelėkite Įrašyti.
9. Spustelėkite Naujas.
10. Sąraše pažymėkite pasirinktą eilutę.
11. Lauke Galutinis kiekis įveskite skaičių.
    * Pavyzdžiui, galite nustatyti 9999.  
12. Pažymėkite žymės langelį Leisti skaidyti.
    * Jei pasirinksite šią parinktį, atliekant darbo kūrimo procesą, darbo eilučių kiekius bus galima išskaidyti keliose vietose.  
13. Spustelėkite Įrašyti.
14. Spustelėkite Naujas.
15. Sąraše pažymėkite pasirinktą eilutę.
16. Lauke Pavadinimas surinkite reikšmę.
17. Spustelėkite Įrašyti.
18. Spustelėkite Redaguoti užklausą.
    * Šią užklausą galite redaguoti ir į ją įtraukti apribojimų, kad atsargas būtų galima pasirinkti atliekant papildymo procesą. Pavyzdžiui, gali būti, kad atsargas reikėtų naudoti tik iš sandėlio sandėliavimo vietos.  
19. Spustelėkite GERAI.
20. Uždarykite puslapį.

## <a name="create-a-replenishment-work-template"></a>Papildymo darbo šablono kūrimas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.
    * Darbo šablonas naudojamas valdyti sistemai – kaip reikia kurti min. / maks. papildymo darbą. Turi būti bent paėmimo ir padėjimo darbo šablono eilutė. Kol nebus įvesta visa būtina informacija, bus rodoma, kad darbo šablonas netinkamas.  
2. Lauke Darbo užsakymo tipas pasirinkite Papildymas.
3. Spustelėkite Naujas.
4. Lauke „Darbo šablonas“ įveskite reikšmę.
5. Spustelėkite Įrašyti.
6. Spustelėkite Naujas.
7. Lauke Darbo tipas pasirinkite 'Paimti'.
8. Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.
    * Tai turėtų būti darbo klasė, susijusi su papildymu. Jei naudojate USMF, pasirinkite Papildyti.  
9. Spustelėkite Naujas.
10. Sąraše pažymėkite pasirinktą eilutę.
11. Lauke Darbo tipas pasirinkite „Padėjimas“.
12. Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.
13. Spustelėkite Įrašyti.
14. Uždarykite puslapį.

## <a name="create-a-new-replenishment-template"></a>Naujo papildymo šablono kūrimas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Papildymas > Papildymo šablonai.
    * Papildymo šablonas naudojamas apibrėžti, kurias prekes, kiekius ir vietą reikia papildyti.  
2. Spustelėkite Naujas.
3. Lauke Papildymo šablonas įveskite reikšmę.
    * Šablonui suteikite pavadinimą, nurodantį, kad jis skirtas min. / maks. papildymui.  
4. Lauke Aprašas įveskite reikšmę.
5. Pažymėkite žymės langelį Leisti poreikio bangai naudoti nerezervuotus kiekius.
    * Jei pasirenkate šią parinktį, atliekant bangos bangos paklausos papildymą galima vartoti kiekius, kurie yra susiję su min. / maks. papildymu. Pavyzdžiui, tai gali būti naudinga, jei min. / maks. papildymo darbas apdorojamas ne iš karto, kad nebūtų sukurta nereikalingo paklausos papildymo darbo.  
6. Spustelėkite Naujas.
7. Lauke Sekos numeris įveskite skaičių.
8. Lauke Aprašas įveskite reikšmę.
9. Sąraše pažymėkite pasirinktą eilutę.
10. Lauke Papildymo vienetas įveskite arba pasirinkite reikšmę.
    * Pvz., pasirinkite vnt. Šis parametras yra privalomas. Juo galima nurodyti papildymo darbo matavimo vienetą, kuris skiriasi nuo nurodyto šio šablono mažiausio ir didžiausio atsargų lygio vieneto.  
11. Lauke Darbo šablonas įveskite arba pasirinkite reikšmę.
    * Pasirinkite darbo šabloną, kurį sukūrėte anksčiau.  
12. Lauke Mažiausias kiekis įveskite skaičių.
    * Pasirinkite mažiausią kiekį, kuris turėtų paleisti papildymą. Pavyzdžiui, nustatykite 50. Šį kiekį galima palikti nustatytą į nulį – jei papildote fiksuotą vietą ir parinktis Papildyti tuščias fiksuotas vietas nustatyta į Taip. Taip pat rekomenduojame pasirinkti parinktį Papildyti atsargas tik fiksuotose vietose, kad procesas būtų našesnis.  
13. Lauke Didžiausias kiekis įveskite skaičių.
    * Pavyzdžiui, nustatykite 100.  
14. Lauke Vienetas įveskite arba pasirinkite reikšmę.
    * Priskirkite mažiausio ir didžiausio kiekių vienetą. Pavyzdžiui, nustatykite „vnt.‟.  
15. Pažymėkite žymės langelį Papildyti tuščias fiksuotas vietas.
    * Pažymėkite šį žymės langelį, kad fiksuotas vietas papildytumėte, kai jos tuščios. Kitu atveju bus papildytos tik vietos, kuriose yra turimas kiekis.  
16. Pažymėkite žymės langelį Papildyti atsargas tik fiksuotose vietose.
17. Spustelėkite Pasirinkite produktus.
    * Tai yra vieta, kurioje galima apibrėžti, kuriuos produktus reikėtų papildyti. Jei pasirinkta parinktis Fiksuotos paėmimo vietos, tas vietas taip pat turite apibrėžti šioje užklausoje. Galima naudoti konkrečių variantų užklausas ir konkrečių produktų užklausas.  
18. Pasirinkite eilutę Prekės.
19. Lauke Kriterijai surinkite reikšmę.
    * Pasirinkite prekes, kurias reikėtų papildyti fiksuotose vietose. Pavyzdžiui, įveskite A*, kad pasirinktumėte visus prekių numerius, prasidedančius A.  
20. Spustelėkite Pridėti.
    * Įtraukite objektą Vieta (nebent jis jau yra), kad galėtumėte nustatyti, jog papildymo darbas turėtų būti atliekamas tik fiksuotose paėmimo vietose, esančiose konkrečioje sandėlio vietoje.  
21. Sąraše pažymėkite pasirinktą eilutę.
22. Lauką Lentelė nustatykite į Vietos.
23. Lauke Laukas pasirinkite Vietos profilio ID.
24. Lauke Kriterijai įveskite arba pasirinkite reikšmę.
25. Spustelėkite GERAI.
26. Uždarykite puslapį.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Nustatymas, kad papildymo procesas būtų vykdomas kaip paketinė užduotis
1. Pasirinkite Sandėlio valdymas > Papildymas > Papildymai.
    * Puslapyje Papildymai galima nustatyti, kad papildymas būtų vykdomas kaip paketinė užduotis, arba reikalauti, kad jis būtų pradedamas rankiniu būdu.  
2. Spustelėkite Filtras.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Kriterijai įveskite arba pasirinkite reikšmę.
5. Spustelėkite Gerai.
6. Išplėskite dalį Vykdyti fone.
7. Parinktį Paketinis vykdymas nustatykite į Taip.
8. Spustelėkite Pasikartojimas.
9. Pasirinkite parinktį Nėra pabaigos datos.
10. Nustatykite pasikartojimo modelį.
    * Pavyzdžiui, pasirinkite Dienos.  
11. Spustelėkite GERAI.
12. Spustelėkite GERAI.


