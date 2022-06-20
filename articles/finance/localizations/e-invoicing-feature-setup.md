---
title: Darbas su funkcijų nustatymais
description: Šiame straipsnyje paaiškinama, kaip nustatyti elektroninių SF išrašymo priemones.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 23466a53bb8ba597503aaa12d41395fc82b9f14e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904331"
---
# <a name="work-with-feature-setups"></a>Darbas su funkcijų nustatymais

[!include [banner](../includes/banner.md)]

Nustatyti elektroninių failų generavimo ir kitus apdorojimo veiksmus (pavyzdžiui, skaitmeniniu būdu pasirašant failus, teikiant juos vyriausybės žiniatinklio tarnybai ir gaunant atsakymą arba juos saugant), nustatyti apdorojimo pardavimo galimybes, taikomumo taisykles ir kintamuosius elektroninių SF išrašymo funkcijoms.

Nustatymo informacija sujungiama į priemonių nustatymo *sąvoką* ir gali būti sukurta, panaikinta, pakoreguota. Taip pat galima peržiūrėti užbaigtų elektroninių SF išrašymo priemonių versijų informaciją.

Galite sukurti tiek priemonių nustatymo elementų, kiek jums reikia norint nustatyti skirtingus elektroninių failų generavimo, apdorojimo ir gavimo scenarijus. Nors šių priemonių nustatymo elementai turi nepriklausomai apdorojamus veiksmus ir vykdymo sąlygas, jie sukuriami kaip vienos elektroninių SF išrašymo funkcijos dalis ir perima jos vykdymo ciklą ir diegimo procesą.

## <a name="add-a-feature-setup"></a>Įtraukti priemonių nustatymą

1. Prisijungti prie savo reguliavimo kongigūravimo paslaugų (RCS) paskyros.
2. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
3. Elektroninių SF **išrašymo priemonių** puslapyje pasirinkite elektroninių SF išrašymo priemonės versiją, kurios būsena **Juodraštis**.
4. Skirtuke **Nustatymai** pasirinkite **Įtraukti**.
5. Išplečiamajame **dialogo lange** Kurti priemonių nustatymą, laukų **grupėje** Naujas pasirinkite vieną iš šių pasirinkčių:
 
    - **Pasirinktinis** nustatymas – sukurkite naują funkcijos nustatymą, kuriame būtų tušti kanalai, tuščias pardavimo galimybių sąrašas, tuščia dalis pritaikymo taisyklėms ir numatytasis kintamųjų rinkinys, atsižvelgiant į nustatymo tipą.
    - **Iš priemonių nustatymo** – kurti kitos priemonės nustatymo, kaip dabartinės elektroninių SF išrašymo priemonės, kopiją.

6. Jei paskutiniame **veiksme** pasirinkote pasirinktinę nustatymo pasirinktį, įveskite priemonės nustatymo elemento pavadinimą ir aprašymą, **tada** nustatymo tipo laukų grupėje pasirinkite vieną iš šių pasirinkčių:

    - **Apdorojamos pardavimo** galimybės – pasirinkite šią pasirinktį, norėdami generuoti ir apdoroti siunčiamus elektroninius dokumentus. Sistema sukuria tuščią šio nustatymo tipo pardavimo galimybių sąrašo apdorojimą, tuščią skyrių taikymo taisyklėms ir numatytąjį kintamųjų rinkinį. Negalėsite dirbti su gaunamų elektroninių dokumentų kanalais.
    - **Duomenų kanalas** – Microsoft Dynamics pasirinkite šią pasirinktį, norėdami nustatyti gaunamų elektroninių dokumentų gavimo iš vieno iš apibrėžtų kanalų procesą ir perduoti juos tiesiogiai į 365 finansus Dynamics 365 Supply Chain Management arba be papildomų veiksmų. Šiuo sąrankos tipu sistema sukuria iš anksto nustatytą duomenų kanalų parametrų sąrašą, tuščią pritaikymo taisyklių skyrių ir numatytųjų kintamųjų rinkinį. Į apdorojimo pardavimo galimybes negalėsite įtraukti jokių veiksmų.
    - **Duomenų kanalas ir apdorojimo pardavimo** galimybės – šis nustatymo tipas panašus į duomenų **kanalo** nustatymo tipą. Tačiau prieš perduodami finansų arba tiekimo grandinės valdymui elektroninį dokumentą, galite nustatyti papildomus veiksmus apdorojimo pardavimo galimybėse.

7. Jei paskutiniame veiksme **pasirinkote** **duomenų** kanalą arba duomenų kanalą ir apdorojimo pardavimo galimybių parinktį, **lauke** Pasirinkti duomenų kanalą turite pasirinkti kanalą, su kurį bus integruojama.
8. Pasirinkite **Kurti**.

Sukūrę priemonės nustatymą, norėdami jį sukonfigūruoti galite **pasirinkti** Redaguoti.

## <a name="edit-a-feature-setup"></a>Redaguoti priemonės nustatymą

Atsižvelgiant į priemonių nustatymo tipą, galite konfigūruoti siunčiamų elektroninių failų generavimo procesą ir pateikti juos išoriniams kanalams, ar gauti gaunamus dokumentus ir perduoti juos į jūsų finansų arba tiekimo grandinės valdymo programą.

### <a name="data-channel"></a>Duomenų kanalas

Duomenų *kanalas priima* elektroninį failą ir arba jį apdoroja, arba tiesiogiai perduoda finansų ar tiekimo grandinės valdymui. Ši pasirinktis negalima pardavimo galimybių tipo Apdorojimo funkcijų **nustatymuose**.

Norėdami nustatyti duomenų kanalą, įveskite kanalo pavadinimą. Tada nurodykite parametrus pagal pasirinktą kanalo tipą. Duomenų kanalo identifikatorius turi nurodyti kintamąjį, kuris sukurtas specialiai duomenų kanalui identifikuoti. Jis bus naudojamas kaip nuoroda finansų arba tiekimo grandinės valdymo srityje.

Skirtuke **Priedai turite** nurodyti filtrų rinkinį, kad būtų gauti konkretūs failai iš kanalo. Galite sukurti kelias eilutes, jei tikitės, kad failai turės skirtingus failo vardo plėtinius, arba jei failai turi būti apdorojami kitaip, atsižvelgiant į failo vardą. Toliau pateikiami pagrindiniai parametrai:

- **Pavadinimas** – įveskite failo pavadinimą, kurį sistema nurodys apdorojimo metu. Finansų ir tiekimo grandinės valdymo programose galėsite matyti failus pateikimo žurnale.
- **Filtras** – nurodykite filtrą, kad pasirinktumėte failus.
- **Pasirinktinai** – jei šis žymės langelis išvalytas, failas yra būtinas. Šiuo atveju sistema rodys klaidos pranešimą, jei kanaluose nėra failų, kurie atitinka filtrą. Šis parametras taikomas el. laiškams.

Jei kanalas yra pašto dėžutė, o gaunamame el. laiške yra keli priedai, galite konfigūruoti taisykles, apibrėžia skirtas nustatyti, kaip tarnyba turi tvarkyti priedus. Tarnyba gali apsvarstyti kiekvieną priedą kaip atskirą elektroninę SF arba laikyti vieną priedą kaip pagrindinę SF, o visus kitus priedus – kaip priedus.

### <a name="processing-pipeline"></a>Apdorojimo srautas

Apdorojamos *pardavimo* galimybės yra veiksmų *rinkinys*, kuris nuosekliai vykdomas tol, kol jie sėkmingai baigiami. Galite naudoti apdorojimo pardavimo galimybes, kad nustatyti elektroninių failų generavimo procesą ir atlikti kitus veiksmus (pavyzdžiui, skaitmeniniu būdu pasirašo failus, pateikti juos išorinėms žiniatinklio tarnyboms ir išanalizuoti atsakymą, gauti ir apdoroti gaunamuosius dokumentus).

Veiksmų sąrašas yra iš anksto apibrėžtas. Norėdami nurodyti veiksmų derinį **,** kuris **logiškai** apibrėžia reikiamą dokumentų pateikimo ar gavimo procesą, galite naudoti mygtukus Naujas ir Naikinti.

Veiksmų tvarka yra svarbi. Tvarką galite koreguoti naudodami mygtukus Aukštyn **ir** **Žemyn**.

Kiekvienas veiksmas turi parametrų rinkinį, kurį galite konfigūruoti arba koreguoti. Konkretus parametrų rinkinys priklauso nuo veiksmo tipo.

- **Veiksmas** – pasirinkti veiksmo tipą.
- **Veiksmo** pavadinimas – įvesti veiksmo pavadinimą. Šis pavadinimas bus rodomas pateikimo žurnaluose ir finansų ir tiekimo grandinės valdymo programų pranešimuose.
- **Aprašas** – pateikite išsamesnės informacijos apie proceso veiksmo paskirtį.
- **Įgalinti kartojimo** funkciją – jei pažymėsite šį žymės langelį, **·** **galėsite pasirinkti veiksmą veiksmo kartojimo lauke ir konfigūruoti papildomus parametrus skirtuke Kartojimo** parametrai.

    Kartojimo funkcija leidžia konfigūruoti tarnybos elgseną, jei negalima paleisti konkretaus veiksmo. Pavyzdžiui, jei išorinė žiniatinklio tarnyba, prie kurios bandote prisijungti, nereaguoja, galite nurodyti, kiek kartų sistema turėtų iš naujo bandyti prisijungti, kokiu intervalu ir nuo to, kokio veiksmo apdorojimo pardavimo galimybėse.

- **Eksportavimo** rezultatai – galite pažymėti šį žymės langelį vienam *apdorojimo* pardavimo galimybių veiksmui. Elektroninis failas, kurį veiksmas sukuria finansų arba tiekimo grandinės valdymo programoje, tada gali būti eksportuojamas iš **elektroninių dokumentų pateikimo žurnalo** puslapio.

### <a name="applicability-rules"></a>Taikymo taisyklės

*Taikymo taisyklės yra* konfigūruojamos sąlygos, kurios suteikia kontekstą elektroninių SF išrašymo funkcijoms paleisti naudojant elektroninių SF išrašymo galimybių rinkinį.
Verslo dokumentai, kurie pateikti iš finansų ar tiekimo grandinės valdymo į elektroninį SF išrašymą, neturi aiškios nuorodos, kuri įgalina elektroninių SF išrašymo galimybę, nustatytą iškviesti tam tikrą elektroninių SF išrašymo priemonės versiją ir tam tikrą priemonės nustatymo prekę apdoroti pateikimą. Tačiau, kai verslo dokumentas tinkamai sukonfigūruotas, jame yra reikalingi elementai, kurie įgalins elektroninių SF išrašymą, siekiant nustatyti, kuri elektroninių SF išrašymo priemonės versija ir apdorojamos pardavimo galimybės turi būti pasirinktos ir paleidžiamos.

Taikymo taisyklės įgalina elektroninių SF išrašymo paslaugą rasti tikslias elektroninių SF išrašymo priemones, kurios turi būti naudojamos pateikimui apdoroti. Norint rasti tinkamas funkcijas, **pateikti** verslo dokumento konteksto laukai yra sugretinti su taikomumo taisyklių sąlygomis.

Taikymo taisykles galima atlikti šiais būdais:

- Pasirinkite **Nauja**, norėdami į taikymo taisyklių rinkinį įtraukti naują sąlygą.
- Norėdami **panaikinti sąlygą**, pasirinkite Naikinti.
- Pasirinkite kelis įrašus ir naudokite mygtuką Grupė **arba** Išgrupuoti **·**, norėdami sukurti prekių ar loginių išrašų derinį. Pavyzdžiui, pasirinkite eilutes, kurias norite grupuoti, tada pasirinkite sąlygą **Grupė**. Kai sąlygos grupuojamos, į tinklelį įtraukiamas naujas stulpelis. Šis stulpelis nurodo sugrupuotos sąlygos loginį operatorių. Palaikomi šie operatorių tipai:

    - Equal
    - Not equal
    - Daugiau nei / mažiau nei
    - Daugiau arba lygu / mažiau arba lygu
    - Susideda iš
    - Prasideda

    > [!NOTE]
    > Kai išgrupuojate sąlygą, visada pradėkite nuo giliausio grupavimo lygio.

### <a name="variables"></a>Kintamieji

*Kintamieji* suteikia daugiau lankstumo nustatant apdorojimo pardavimo galimybes ir duomenų srautą tarp veiksmų. Galite nurodyti kintamąjį kai kuriuose veiksmo parametruose, norėdami laikinai saugoti duomenis ar elektroninius failus. Kai kurie kintamieji naudojami duomenims tarp finansų arba tiekimo grandinės valdymo programų ir elektroninių SF išrašymo paslaugos perduoti.

Numatyta, kad sistema sukuria kelis kintamuosius. Pavyzdžiui, kintamajame BusinessDocumentDataModel **yra verslo duomenys, esantys "JavaScript Object Notation" (JSON) struktūroje,** kuri gaunama iš susijusios programos pateikimo proceso metu.

Galimi šie kintamųjų tipai:

- **Konstanta** – konteineris, skirtas laikiniesiems duomenims, naudojamims pardavimo galimybių veiksmams apdoroti, saugoti.
- **Iš kliento** – kintamojo turinys įgyjamas iš "Dynamics 365" kliento, kai vykdomas pateikimo procesas.
- **Klientui** – kintamojo turinį "Dynamics 365" klientas gali importuoti, kai vykdomas pateikimo procesas.
- **Duomenų tipas** – pasirinkti kintamajame saugomos informacijos duomenų tipą.

### <a name="parameters"></a>Parametrai

Parinktis **Išjungti verslo duomenis** yra naudojama optimizuoti verslo duomenų mokamo krovinio, kuris gaunamas iš finansų arba tiekimo grandinės valdymo programos elektroninio dokumentų pateikimo metu, struktūrą. Optimizavimas padeda sumažinti duomenis, kurie patenka į elektroninių SF išrašymo paslaugą, kad būtų toliau transformuoti į reikiamą elektroninį failą. Numatytoji reikšmė yra **Ne**.

- **Taip** – finansų arba tiekimo grandinės valdymas nusiųs SF modelio arba finansinio modelio (Brazilijos) **struktūros**, apibrėžtos elektroninių ataskaitų modulyje, JSON **·** **failą**. Visi modelio elementai užpildomi programos verslo duomenimis, nepaisant galutinės elektroninio failo struktūros. Modeliuose paprastai būna daugiau verslo duomenų, nei reikalauja paskirties failo struktūra, ir šiam duomenims generuoti programoje gali būti daugiau laiko. Retais atvejais **, kai** norite generuoti skirtingus išvesties failus vienoje elektroninio SF išrašymo priemonėje ir priemonės nustatyme, reikia šios pasirinkties vertės Taip. Vertė Taip **naudinga**, kai trikčių šalinimo scenarijai, elektroninių failų struktūra ir verslo duomenų užbaigtumas.
- **Ne** – finansų arba tiekimo grandinės valdymas pirmą kartą iškies paslaugą be jokių verslo duomenų. Šio skambučio paskirtis yra gauti informacijos apie elektroninių ataskaitų (ER) konfigūraciją, kuri bus naudojama elektroninio failo transformacijai apdorojimo pardavimo galimybėse. Ši informacija grąžinama programai, kuri naudoja ją verslo duomenų, kuriuos reikia įtraukti į SF modelio arba finansinio modelio (Brazilijos) struktūros **JSON** **failą**, subgrupui nustatyti. Šios pasirinkties **vertė** padeda sumažinti verslo duomenų, kuriuos programa pateikia tarnybai, kiekį, nes programa gali pateikti tik verslo duomenis, kurie būtini norint sėkmingai sugeneruoti elektroninį failą.

### <a name="validate-a-feature-setup"></a>Priemonės nustatymo patikrinimo duomenys

Galite paleisti tikrinimą, kad būtų tikrinamas visos konfigūracijos vientisumas. Pavyzdžiui, jei privalomas veiksmo parametras buvo paliktas tuščias, tikrinimas aptinka šį nenuoseklumą ir jūs gaunate perspėjimo pranešimą.

- **Priemonės versijos nustatymo** puslapyje, veiksmų srityje, **pasirinkite Tikrinti**.

## <a name="delete-a-feature-setup"></a>Priemonės nustatymo naikinimas

1. Elektroninių SF **išrašymo priemonių puslapyje** pasirinkite elektroninės SF išrašymo priemonės versiją, kurios būsena **Juodraštis**.
2. Skirtuke **Nustatymai** pasirinkite **Naikinti**.
3. Pasirodame pranešimų lauke pasirinkite Taip **,** kad patvirtintumėte, jog norite panaikinti priemonės nustatymą.
