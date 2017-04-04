---
title: "Naudoti peržvalgos surasti informaciją"
description: "Microsoft Dynamics 365 operacijoms, daugelyje sričių turi paieška, kuri gali padėti jums lengvai rasti tinkamą ir norimą reikšmę. Peržvalgų, kad šie valdikliai paprastesnių ir padaryti daugiau produktyvių vartotojai buvo pridėta keletas patobulinimų. Šioje temoje, jūs sužinosite apie šias naujas ieškos funkcijas ir gaus šiek tiek naudingų patarimų, kurie padės optimalaus iš peržvalgų sistemoje."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Naudoti peržvalgos surasti informaciją

Microsoft Dynamics 365 operacijoms, daugelyje sričių turi paieška, kuri gali padėti jums lengvai rasti tinkamą ir norimą reikšmę. Peržvalgų, kad šie valdikliai paprastesnių ir padaryti daugiau produktyvių vartotojai buvo pridėta keletas patobulinimų. Šioje temoje, jūs sužinosite apie šias naujas ieškos funkcijas ir gaus šiek tiek naudingų patarimų, kurie padės optimalaus iš peržvalgų sistemoje.  

<a name="responsive-lookups"></a>Reaguoja peržvalgas
------------------

Ankstesnėse versijose, Dynamics 365 operacijoms, kai bendrauja su ieškos valdiklio, vartotojas turėtų atskirai imatės veiksmų atidaryti išskleidžiamąjį meniu. Tai galėjo būti įvesdami žvaigždutė (\*) filtruoti pagal dabartinę vertę kontrolės peržvalgos valdiklį, spustelėdami mygtuką meniu, arba naudojant į **Alt**+**žemyn** spartieji klaviatūros klavišai. Peržvalgos kontrolė buvo pakeistos vienu iš šių būdų, siekiant geriau suderinti su interneto praktiką:

-   Peržvalgos išskleidžiamajame meniu dabar atsidarys automatiškai po šiek tiek pristabdyti įvedėti su išskleidžiamajame meniu turinys filtruojamas pagal ieškos valdiklio reikšmę.
    -   Atkreipkite dėmesį, kad senų elgesio automatinio atidarymo dropdown įvedę žvaigždutė (\*) buvo pasenusios.
-   Po to, kai peržvalgos išskleidžiamajame meniu yra atidarytas, šių įvyks:
    -   Žymiklis liks ieškos valdiklio (o ne dėmesio perkėlimas į išplečiamojo meniu), galima toliau keisti valdiklio reikšme. Tačiau, vartotojas gali naudotis į **rodyklė aukštyn** ir **žemyn** keisti eilučių išskleidžiamajame meniu ir įveskite išplečiamajame meniu pasirinkite dabartinės eilutės.
    -   Išskleidžiamajame meniu turinys bus pakoreguoti pateikus pakeitimus į ieškos valdiklio reikšmę.

Pavyzdžiui, Įsivaizduokite peržvalgos laukas, vadinamas **City**. 

Kai dėmesys yra į **City** srityje, galite pradėti ieškoti miesto, kurį norite įvesdami kelias raides, pvz., "pulkininkas."  Po to, kai nustosite rinkti tekstą, peržvalgos atsidarys automatiškai, filtruojamas, kad tų miestų, kurie prasideda "pulkininkas". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Šiuo metu, žymeklis yra dar peržvalgos lauke. Jei jūs ir toliau rašyti, reikšmė yra "colum", peržvalgos turinys automatiškai koreguoti siekiant atspindėti naujausius kontrolės reikšmė. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Nors dėmesys vis dar ieškos valdiklio, jūs taip pat galite naudoti su **rodyklė aukštyn** ar **žemyn** klavišus pažymėkite eilutę, kurią norite pasirinkti. Jei paspausite **Enter** pary¹kint± eilutê, atrenkamos iš peržvalgos ir atnaujins valdiklio reikšme. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Rašyti daugiau nei ID
Įvedant duomenis, tai natūralu, kad vartotojai galėtų identifikuoti ūkio subjektas, pvz., klientas ar tiekėjas, pagal pavadinimą, o ne atstovauja ūkio subjekto identifikatorių. Dabartiniame Dynamics 365 operacijoms, daugelio (bet ne visuose) o peržvalgos funkcija dabar leidžia kontekstinė duomenų įvedimo. Ši galinga funkcija leidžia vartotojo ID arba atitinkamą pavadinimą įvedate ieškos valdiklio. 

Pavyzdžiui, Įsivaizduokite, **kliento sąskaita** lauko kuriant pardavimo užsakymo. Šiame lauke rodoma į **abonemento ID** nes pirkėjas, tačiau vartotojas paprastai norėtų patekti yra **abonemento pavadinimas** vietoj, **abonemento ID** šiame lauke, kai kuriate pardavimo užsakymas, pvz., "Miško didmeninės" vietoj "JAV-003."

Jei vartotojas pradėjo atvykti į **abonemento ID** į ieškos valdiklio, išplečiamajame meniu būtų automatiškai atidaromi kaip aprašyta ankstesnėje sekcijoje ir vartotojui būtų rodomas peržvalgos kaip parodyta žemiau.

[![Kai įvedama kliento paskyros ID kontekstinė peržvalgos](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Tačiau, vartotojas taip pat dabar galite įvesti pradžios yra **abonemento pavadinimas** taip pat. Jei tai yra aptinkamas, vartotojas matys šių peržvalgos. Pranešimas, **pavadinimas** skiltis perkeliama į būti pirmas stulpelis, peržvalgos, ir kaip peržvalgos rūšiuoti ir filtruoti pagal, **pavadinimas** stulpelio.

[![Kontekstinė peržvalgos, kai įvedama kliento vardas](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Naudojant tinklelio stulpelių antraščių daugiau Išplėstinis filtravimas ir rūšiavimas
Peržvalgos patobulinimai, aptarė du dažniai labai pagerinti vartotojo galimybė naršyti peržvalgos, remiantis "prasideda" paieškos eilutes su **ID** ar **pavadinimas** lauko peržvalgos. Vis dėlto yra situacijų, kuriose daugiau papildomų filtravimo (arba rūšiavimo) yra reikia rasti teisingą eilutę. Šiais atvejais vartotojas turi naudoti filtravimo ir rūšiavimo parinktys tinklelio stulpelių antraščių viduje peržvalgos. Pavyzdžiui, Įsivaizduokite darbuotoją į pardavimo užsakymo eilutę kam reikia rasti teisę "lynas" produktu. Įvesdami "kabelis", **prekės numeris** valdymo nėra naudinga, nes šiuo metu nėra produktų pavadinimus, kurie prasideda "kabelis." 

![emptyitemlookup](./media/emptyitemlookup.png) 

Vietoj to, vartotojas turi išvalyti ieškos valdiklio reikšmė, atidaryti ieškos išplečiamajame meniu ir Filtruoti išskleidžiamąjį meniu naudojant tinklelį stulpelio antraštę, kaip parodyta žemiau. Pele (arba touch) vartotojas gali tiesiog spustelėkite arba palieskite bet kurio stulpelio antraštę, naudotis filtravimo ir rūšiavimo parinktis skiltyje. Klaviatūros vartotojas, vartotojas tiesiog reikia paspausti **Alt**+**žemyn****rodyklė** antrą kartą, jei norite perkelti židinį į išplečiamojo meniu, po kurio vartotojas gali į teisingą stulpelio skirtuką, ir tada paspauskite **Ctrl**+**G** atidaryti tinklelio stulpelių antraštės išskleidžiamajame meniu. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Po to filtras buvo pritaikytas (žr. paveikslėlį žemiau), vartotojas gali rasti ir pasirinkite eilutę kaip įprasta. 

![filtereditemlookup](./media/filtereditemlookup.png)


