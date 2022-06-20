---
title: Tiekimo grafikas
description: Šiame straipsnyje pateikiama informacija apie tiekimo grafiko puslapį ir jo galimybes.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0e3937dd4cffc464f38b5770674364579bdb06d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851745"
---
# <a name="supply-schedule"></a>Tiekimo grafikas

[!include [banner](../includes/banner.md)]

Puslapyje **Tiekimo grafikas** pateikiama išsami produktų ar produktų šeimos tiekimo ir poreikio apžvalga. Informacija yra filtruojama pagal vietą, bendrąjį planą ir laikotarpius. Šį puslapį taip pat galite naudoti naujiems užsakymams kurti, modifikuoti esamus suplanuotus užsakymus ir paleisti bendrąjį planavimą.

## <a name="open-the-supply-schedule-page"></a>Tiekimo grafiko puslapio atidarymas

Puslapį **Tiekimo grafikas** galite atidaryti bet kuriuo iš šių būdų:

- Eikite į **Bendrasis planavimas \> Bendrasis planavimas \> Tiekimo grafikas**. Dialogo lange **Modifikuoti filtrą** nurodykite ieškomus planą ir produktą įvesdami filtrų reikšmes į pateikiamus laukus. (Likusioje šio straipsnio dalyje jūsų įvedamos filtro vertės vadinamos "filtru" arba "dabartiniu filtru". Baigę pasirinkite **Gerai**.
- Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**. Pasirinkite arba atidarykite produktą. Tada veiksmų srities skirtuko **Planas** grupėje **Peržiūrėti** pasirinkite **Tiekimo grafikas**.
- Eikite į **Bendrasis planavimas \> Nustatymas \> Poreikio prognozė \> Prekės paskirstymo raktai**. Pasirinkite prekės paskirstymo raktą, kuris naudojamas kaip produktų šeima. Tada veiksmų srityje pasirinkite **Tiekimo grafikas**.
- Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Suplanuoti užsakymai**. Pasirinkite ar atidarykite suplanuotą užsakymą. Tada veiksmų srities skirtuko **Peržiūrėti** grupėje **Peržiūrėti** pasirinkite **Tiekimo grafikas**.

> [!NOTE]
> Kai atidarote **Tiekimo grafiko** puslapį iš produkto, produktų šeimos arba suplanuoto užsakymo, nereikia įvesti filtrų reikšmių. Sistema naudos numatytąjį laikotarpio šabloną.

## <a name="use-the-supply-schedule-page"></a>Tiekimo grafiko puslapio naudojimas

**Tiekimo grafiko** puslapį sudaro viršutinė dalis, „FastTab” **Laikotarpio pabaigos atsargos**, papildomas „FastTab”, kuris tampa matomas pagal viršutinėje dalyje pasirinktą eilutę ir „FactBox” sritį. (Norėdami atidaryti „FactBox” sritį ir peržiūrėti „FactBox”, pasirinkite **Susijusi informacija** dešiniajame puslapio krašte.)

### <a name="upper-section"></a>Viršutinė dalis

Viršutinėje **Tiekimo grafiko** puslapio dalyje yra tinklelis, kuriame rodomi šie produktų arba produktų šeimos duomenys. Šie duomenys yra išskaidomi pagal laikotarpius, kuriuos apibrėžia **Laikotarpio šablono** reikšmė iš filtro.

- **Laikotarpio pradžios atsargos** – ši eilutė rodo numatomą atsargų balansą laikotarpio pradžioje, jei sistemoje įvyksta visi užsakymai.
- **Laikotarpio pabaigos atsargos** – ši eilutė rodo numatomą atsargų balansą laikotarpio pabaigoje, jei sistemoje įvyksta visi užsakymai.
- **Iškviestos laikotarpio pabaigos atsargos** – šioje eilutėje rodoma atsargų, kurios yra iškviestos pagal ateities poreikį, suma laikotarpio pabaigoje.
- **Laikotarpio grynasis tiekimas** – šioje eilutėje rodomas skirtumas tarp tiekimo ir poreikio konkrečiu laikotarpiu.
- **Minimalios atsargos** – šis mazgas rodo produkto arba produktų šeimos saugos atsargas. Jei norite išplėsti arba sutraukti šį mazgą, pasirinkite jį, o tada pasirinkite **Išplėsti** arba **Sutraukti** įrankių juostoje. Šis mazgas rodomas tik tada, kai yra produktų ar produktų šeimos saugos atsargos.
- **Poreikis** – šis mazgas rodo produktų arba produktų šeimos poreikį. Poreikis yra grupuojamas pagal operacijos tipą. Jei norite išplėsti arba sutraukti šį mazgą, pasirinkite jį, o tada pasirinkite **Išplėsti** arba **Sutraukti** įrankių juostoje. Poreikio operacijų tipai apima pardavimo, perkėlimų ir atsargų žurnalus. Šis mazgas rodomas tik tada, kai yra produktų ar produktų šeimos poreikis.
- **Tiekimas** – šis mazgas rodo produktų arba produktų šeimos tiekimą. Tiekimas yra grupuojamas pagal operacijos tipą. Jei norite išplėsti arba sutraukti šį mazgą, pasirinkite jį, o tada pasirinkite **Išplėsti** arba **Sutraukti** įrankių juostoje. Tiekimo operacijų tipai yra gamyba, pirkimas ir perkėlimai. Šis mazgas rodomas tik tada, kai yra produktų ar produktų šeimos tiekimas.

Daugelis galimų įrankių juostos mygtukų, „FactBox” ir „FastTab” rodinių priklauso nuo jūsų pasirinkimų viršutinėje dalyje. Paprastai operacijos tipą pasirinksite pažymėdami vieną iš eilučių, esančių po **Tiekimo** arba **Poreikio** mazgu. Tada pasirinkite laikotarpį pažymėdami konkretų pasirinktos eilutės stulpelį.

Įrankių juosta, esanti virš tinklelio viršutinėje **Tiekimo grafiko** puslapio dalyje, pateikia šiuos mygtukus:

- **Išplėsti/Sutraukti** – išplėskite arba sutraukite pasirinktą mazgą, pavyzdžiui, **Poreikio** mazgą, **Tiekimo** mazgą ir jų antrinius mazgus. (Mazguose rodomas **\[+\]** arba **\[-\]** prefiksas, nurodantis, ar jie šiuo metu yra sutraukti, ar išplėsti.)
- **Naujas** – atidaromas meniu, kuriame kiekviena komanda savo ruožtu atidaro dialogo langą arba puslapį, kuriame į pasirinkimą galite įtraukti konkretų prekės tipą. Galimos komandos apima **Prognozės tiekimą**, **Suplanuotą užsakymą**, **Suplanuotą „kanban”**, **Naują gamybos užsakymą**, **Pirkimo užsakymą** ir **Perkėlimo užsakymą**.
- **Bendrasis planavimas** – vykdyti bendrąjį planavimą. Atsiranda dialogo langas, kuriame galite nurodyti vykdytiną planą. Pagal numatytuosius nustatymus lauke **Bendrasis planas** nustatytas atitikti dabartinį filtrą.
- **Maks. ataskaita baigta** – atidarykite **Maks. ataskaita baigta** puslapį produktui, apibrėžtam dabartiniame filtre.
- **Atnaujinti suplanuotus užsakymus** – atidarykite **Suplanuotų užsakymų** puslapį, kuriame rodomi dabartiniame filtre apibrėžti produktų arba produktų šeimos suplanuoti užsakymai.
- **Lygis** – paskirstyti suplanuotus užsakymus pagal pasirodžiusio dialogo lango parametrus.
- **Medžiagų plano strategija pagal vietą** – atidarykite **Prekės apimties** puslapį produktui, apibrėžtam dabartiniame filtre.
- **„Kanban” taisyklė** – atidarykite **„Kanban” taisyklių** produktui, apibrėžtam dabartiniame filtre.

### <a name="fasttabs"></a>„FastTab” skirtukai

Puslapyje **Tiekimo grafikas** gali būti šie „FastTab”:

- **Laikotarpio pabaigos atsargos** – šis „FastTab” rodo laikotarpio pabaigos atsargų duomenis grafiniu formatu.
- **Tiekimo šablonas** – šis „FastTab” rodo tiekimo duomenis grafiniu formatu. Jis tampa matomas, kai pasirenkate **Tiekimo** mazgą arba eilutę žemiau jo viršutinėje dalyje.
- **Suvestinė** – šiame „FastTab” rodoma suvestinės informacija, susijusi su viršutinėje dalyje pasirinktu operacijos tipu. Pavyzdžiui, jei pasirenkate **Pardavimai** po **Poreikio** mazgu, šis „FastTab” rodo laukus, susijusius su pardavimo užsakymais, pavyzdžiui, **Pageidaujamos pardavimo užsakymo eilutės** arba **Bendra suma**. Jei pasirenkate **Gamybos užsakymai** po **Tiekimo** mazgo antriniu mazgu **Gamyba**, šiame „FastTab” bus rodomi laukai, susiję su gamybos užsakymais, pavyzdžiui, **Suplanuoti gamybos užsakymai** arba **Iš viso suplanuota**. Lauko reikšmės priklauso nuo laikotarpio, kurį pasirinkote viršutinėje dalyje. 
- **\[Operacijos tipas\] - \[Laikotarpis\]** – šiame „FastTab” rodomi viršutinėje dalyje pasirinkto operacijos tipo ir laikotarpio užsakymai. „FastTab” pavadinimas atspindi tuos pasirinkimus. Pavyzdžiui, jį galite pavadinti **Pardavimo užsakymai – Žurnalas** arba **Gamybos užsakymai – 37 savaitė**.

### <a name="action-pane"></a>Veiksmų sritis

Toliau nurodyti mygtukai galimi Veiksmų srityje:

- **Modifikuoti filtrą** – atidarykite **Modifikuoti filtrą** dialogo langą, kuriame galite atnaujinti filtro reikšmes ir tada iš naujo atidarykite **Tiekimo grafiko** puslapį, kuris atspindi atnaujintus filtro parametrus.
- **Rodyti atidėjimus** – pažymėkite susijusias eilutes viršutinėje dalyje, jei yra atidėtas to operacijos tipo užsakymas.

### <a name="factbox-pane"></a>FactBox sritis

Norėdami atidaryti „FactBox” sritį ir peržiūrėti „FactBox”, pasirinkite **Susijusi informacija** dešiniajame puslapio krašte. Šias „FactBox” galima rasti **Tiekimo grafiko** puslapyje:

- **Prekės informacija** – šiame „FactBox” rodoma pagrindinė informacija apie produktą, apibrėžtą dabartiniame filtre. Laukas tuščias, jei apibrėžėte produktų šeimą filtre.
- **Veiksmai** – šiame „FactBox” rodomi viršutinėje dalyje pasirinktų operacijos tipo užsakymų veiksmai.
- **Atidėjimai** – šiame „FactBox” rodomi viršutinėje dalyje pasirinktų operacijos tipo užsakymų atidėjimai.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
