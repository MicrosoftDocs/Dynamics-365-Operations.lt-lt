--- 
title: "Reikiamų konfigūracijų kūrimas elektroninėse ataskaitose (ER), norint importuoti duomenis iš išorinio failo"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti elektroninių ataskaitų (ER) konfigūracijas norėdamas importuoti duomenis iš išorinio failo į „Dynamics 365 for Finance and Operations“, „Enterprise” leidimo programą."
author: NickSelin
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7cdc02d147a0446d7e1f3c9a55304602774820bf
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-required-configurations-to-import-data-from-an-external-file-for-electronic-reporting-er"></a>Reikiamų konfigūracijų kūrimas elektroninėse ataskaitose (ER), norint importuoti duomenis iš išorinio failo

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti elektroninių ataskaitų (ER) konfigūracijas norėdamas importuoti duomenis iš išorinio failo į „Dynamics 365 for Finance and Operations“, „Enterprise” leidimo programą. Šiame pavyzdyje kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti užduočių vadovo „ER: konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“ veiksmus.“ Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį. Be to, naudodami nuorodas į elektroninių ataskaitų apžvalgos temą (https://go.microsoft.com/fwlink/?linkid=852550), turite atsisiųsti ir įrašyti vietoje šiuos failus: 1099model.xml, 1099format.xml, 1099entries.xml, 1099entries.xlsx.

    * ER įmonių vartotojams suteikia galimybę konfigūruoti išorinių duomenų failų importavimo į lenteles, esančias „Dynamics 365 for Finance and Operations“, „Enterprise“ leidime, procesą .XML arba .TXT formatu. Pirma, turi būti sukurta abstraktaus duomenų modelio ir ER duomenų modelio konfigūracija, kad būtų rodomi importuojami duomenys. Tada turite nustatyti importuojamo failo struktūrą ir metodą, kurį naudosite duomenims iš failo į abstraktų duomenų modelį perkelti. ER formato konfigūracija, susiejama su sukurtu duomenų modeliu, turi būti sukurta tam abstrakčiam duomenų modeliui. Tada duomenų modelio konfigūracija turi būti išplėsta įtraukiant susiejimą, kuriame aprašoma, kokiu būdu importuoti duomenys išlaikomi kaip abstraktaus duomenų modelio duomenys ir kaip jie naudojami atnaujinant „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo lenteles.  ER duomenų modelio konfigūracija turi būti pridėta įtraukiant naujo modelio susiejimą, kuriame aprašomas duomenų modelio susiejimas su programos paskirties vietomis.  
    * Pateiktame scenarijuje parodytos ER duomenų importavimo galimybės. Tai apima tiekėjų operacijas, kurios sekamos išorėje, tada importuojamos į „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą ir vėliau įtraukiamos į 1099 tiekėjo sudengimo ataskaitą.   

## <a name="add-a-new-er-model-configuration"></a>Įtraukti naują ER modelio konfigūraciją
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Patikrinkite, ar pavyzdinės įmonės „Litware, Inc.‟ konfigūracijų teikėjas yra pasiekiamas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti procedūros „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu” veiksmus.“   
2. Spustelėkite Ataskaitų konfigūracijos.
    * Užuot kūrę naują modelį, skirtą duomenų importavimui palaikyti, įkelkite anksčiau atsisiųstą failą 1099model.xml. Šiame faile yra tiekėjų operacijų pasirinktinių duomenų modelis. Šis duomenų modelis susietas su „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo duomenų komponentais, esančiais AOT duomenų objekte.   
3. Spustelėkite Keitimas.
4. Spustelėkite Įkelti iš XML failo.
    * Spustelėkite Naršyti ir suraskite anksčiau atsisiųstą failą 1099model.xml.  
5. Spustelėkite GERAI.
6. Medyje pasirinkite „1099 mokėjimų modelis”.

## <a name="review-data-model-settings"></a>Peržiūrėti duomenų modelio parametrus
1. Spustelėkite Konstruktorius.
    * Šis modelis skirtas tiekėjų operacijoms verslo požiūriu pateikti ir „Dynamics 365 for Finance and Operations“, „Enterprise“ leidime diegiamas atskirai.   
2. Medyje išplėskite „1099-MISC”.
3. Medyje pasirinkite „1099-MISC \ Operacijos”.
4. Medyje išplėskite „1099-MISC \ Operacijos”.
    * Šio modelio operacijų elementas nurodo atskiras operacijas. Antriniai elementai naudojami reikiamai informacijai, pvz., kiekvienos operacijos tiekėjo kodui ir operacijos datai, nurodyti.   
5. Uždarykite puslapį.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Įtraukti naują ER formato konfigūraciją, kuri palaiko duomenų importavimą
    * Šios papildomos užduoties veiksmai paaiškina, kaip galima sukurti naują formato konfigūraciją norint valdyti duomenų importavimą iš išorinių failų.   
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
2. Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį 1099 mokėjimų modelis“.
3. Lauke Palaikomas duomenų importavimas pasirinkite Taip.
4. Norėdami uždaryti šį puslapį, paspauskite klavišą ESC.
    * Užuot kūrę naują formatą, skirtą duomenų importavimui palaikyti, įkelkite anksčiau atsisiųstą failą 1099format.xml. Šiame faile nustatyta importuojamo failo struktūra, susieta su tiekėjų operacijų pasirinktinių duomenų modeliu.   
5. Spustelėkite Keitimas.
6. Spustelėkite Įkelti iš XML failo.
    * Spustelėkite Naršyti ir suraskite anksčiau atsisiųstą failą 1099format.xml.  
7. Spustelėkite GERAI.
8. Medyje išplėskite „1099 mokėjimų modelis”.
9. Medyje pasirinkite „1099 mokėjimų modelis \ Formatas tiekėjų operacijoms importuoti”.

## <a name="review-format-settings"></a>Peržiūrėti formato parametrus
1. Spustelėkite Konstruktorius.
2. Įjunkite „Rodyti išsamią informaciją”.
3. Spustelėkite Išplėsti / sutraukti.
4. Spustelėkite Išplėsti / sutraukti.
    * Sukurtas formatas atitinka numatytą išorinio failo struktūrą. Šis failas turi būti XML formatu ir turėti sudengimo šakninį elementą. Kiekvieno tiekėjo operacija pateikiama pagal operacijos elementą, kuris apibrėžiamas kaip operacijų nuo nulio iki daugybės įvairovė. Tai reiškia, kad gaunamame faile gali būti maždaug nuo nulio iki kelių operacijų. Įdėtieji „operacijos” elementai atitinka vienos operacijos atributus. Atkreipkite dėmesį, kad visi atributai, išskyrus šalį, pažymėti kaip privalomi, t. y. būtina juos turėti importuojamame faile.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Peržiūrėti formato susiejimo su duomenų modeliu parametrus
1. Spustelėkite Susieti formatą su modeliu.
    * Susiejime „Importuoti tiekėjų operacijas” yra duomenų perkėlimo iš gaunamo XML failo į pasirinktinių duomenų modelio (nustatomo pasirenkant 1099-MISC aprašą) pasirinktą dalį taisyklės.  
2. Spustelėkite Konstruktorius.
3. Įjunkite „Rodyti išsamią informaciją”.
4. Medyje išplėskite „formatas: Įrašyti“.
5. Medyje pasirinkite „formatas: Įrašyti“.
    * Atkreipkite dėmesį, kad sukurtas formatas čia pateikiamas kaip duomenų šaltinio komponentas.  
6. Medyje išplėskite „formatas: Įrašyti\*sudengimas: XML elementas 1..1 (sudengimas): Įrašyti“.
7. Medyje išplėskite „formatas: Įrašyti\*sudengimas: XML elementas 1..1 (sudengimas): Įrašyti \ operacija: XML elementas 0..* (operacija): Įrašų sąrašas”.
8. Medyje išplėskite „formatas: Įrašyti\*sudengimas: XML elementas 1..1 (sudengimas): Įrašyti \ operacija: XML elementas 0..* (operacija): Įrašų sąrašas\*tiekėjas: XML elementas 1..1 (tiekėjas): Įrašyti”.
9. Medyje išplėskite „formatas: Įrašyti\*sudengimas: XML elementas 1..1 (sudengimas): Įrašyti \ operacija: XML elementas 0..* (operacija): Įrašų sąrašas \ šalis: XML elementas 0..1 (šalis): Įrašyti”.
10. Medyje pasirinkite „formatas: Įrašyti\*sudengimas: XML elementas 1..1 (sudengimas): Įrašyti \ operacija: XML elementas 0..* (operacija): Įrašų sąrašas\*tiekėjas: XML elementas 1..1 (tiekėjas): Įrašyti”.
    * Įsidėmėkite, kad privalomų ir pasirinktinių formato elementų pateikimas skiriasi nuo iš anksto nustatyto „formato” duomenų šaltinio komponento pateikimo.  
11. Medyje išplėskite „Operacijos: Įrašų sąrašas= format.settlement.„$išvardyta”.
    * Atminkite, kad formato, kuris nurodo importuoto failo struktūrą, elementai susieti su pasirinktinių duomenų modelio elementais. Pagal šiuos susiejimus importuoto XML failo turinys apdorojimo metu bus saugomas esamame duomenų modelyje. Atkreipkite dėmesį į šalies elemento susiejimą. Bet kurio operacijos elemento gaunant failą, kuriame nėra tokio elemento, atveju į duomenų modelį bus įvestas numatytasis šalies kodas „JAV”.  
12. Spustelėkite skirtuką Tikrinimai.
    * Šio formato susiejimas gali būti vartotojo nustatyta logika verslo požiūriu patikrinti importuotų duomenų tikslumą. Pavyzdžiui, pagal nustatymą bet kurios operacijos importuojamame faile be nustatyto šalies kodo atveju bus sugeneruotas įspėjamasis sistemos pranešimas, informuojantis vartotoją apie atvejį ir nurodantis operacijos sekos numerį.  
13. Uždarykite puslapį.

## <a name="run-the-format-mapping-to-the-data-model"></a>Vykdyti formato susiejimą su duomenų modeliu
    * Šio formato susiejimą vykdykite bandymams. Naudokite anksčiau atsisiųstą failą 1099entries.xml. Galite eksportuoti šį failą iš 1099entries.xlsx darbaknygės, naudojamos tiekėjų operacijoms valdyti. Sugeneruota išvestis bus importuota iš pasirinkto XML failo ir realiojo importo metu bus automatiškai įvestas pasirinktinių duomenų modelis.  
1. Spustelėkite Vykdyti.
    * Spustelėkite Naršyti ir suraskite anksčiau atsisiųstą failą 1099entries.xml.  
2. Spustelėkite GERAI.
    * Operacijos importuojant failą atveju atkreipkite dėmesį į įspėjamąjį pranešimą apie trūkstamą šalies kodą.  
    * Peržiūrėkite išvestį XML formatu, kuriuo rodomi iš pasirinkto failo importuoti ir į duomenų modelį perkelti duomenys.   
3. Uždarykite puslapį.
4. Uždarykite puslapį.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Peržiūrėti modelio susiejimo su paskirties vietomis parametrus
1. Medyje pasirinkite „1099 mokėjimų modelis”.
2. Spustelėkite Konstruktorius.
3. Spustelėkite „Susieti modelį su duomenų šaltiniu“.
    * Susiejimas Rankinis 1099 operacijų importavimas apibrėžtas naudojant krypties tipą Į paskirties vietą. Tai reiškia, kad jis įvestas duomenų importavimui palaikyti ir jame yra taisyklių nustatymas, apibrėžiantis, kokiu būdu importuotas ir kaip abstraktaus duomenų modelio duomenys išlaikytas išorinis failas naudojamas atnaujinant lenteles „Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo programoje.  
4. Spustelėkite Konstruktorius.
5. Medyje išplėskite „modelis: Duomenų modelis 1099 mokėjimų modelis”.
6. Medyje išplėskite „modelis: Duomenų modelis 1099 mokėjimų modelis \ Operacijos: Įrašų sąrašas”.
    * Atkreipkite dėmesį, kad sukurtas modelis čia pateikiamas kaip duomenų šaltinio elementas. Apdorojimo metu jame bus iš išorinio failo importuoti duomenys. Kaip duomenų šaltinio elementai buvo įtrauktos kelios lentelės siekiant užtikrinti, kad importuoti duomenys suderinami su dabartinės programos duomenimis, įskaitant tai, ar sistemoje galima rasti importuojamą operacijos tiekėjo kodą, ar tinkama importuojamos šalies ir apskričių kodų kombinacija ir kt.  
7. Medyje pasirinkite „modelis: Duomenų modelis 1099 mokėjimų modelis \ Operacijos: Įrašų sąrašas\$nepavyko: Apskaičiuotas laukas = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean'.
8. Spustelėkite Redaguoti.
9. Spustelėkite „Redaguoti formulę“.
    * Nepavykus patikrinti bent vienos importuotos operacijos, ši bus pažymėta kaip nepavykusi pagal duomenų šaltinio atributą „$nepavyko”.  
10. Uždarykite puslapį.
11. Spustelėkite Atšaukti.
12. Medyje pasirinkite „tax1099trans: Lentelės „VendSettlementTax1099” įrašai= model.Validated”.
13. Spustelėkite Redaguoti paskirties vietą.
    * Ši ER paskirties vieta įtraukta siekiant nurodyti, kaip importuoti duomenys atnaujins programos lenteles. Šiuo atveju pasirinkta duomenų lentelė VendSettlementTax1099. Importuotos operacijos bus įterptos į lentelę VendSettlementTax1099, todėl pasirinktas įrašo veiksmas Įterpti. Įsidėmėkite, kad vieno modelio susiejimas gali turėti kelias paskirties vietas. Tai reiškia, kad importuoti duomenys gali būti naudojami vienu metu atnaujinant kelias programos lenteles. Lenteles, rodinius ir duomenų objektus galima naudoti kaip ER paskirties vietas.   
    * Jei susiejimas bus iškviestas iš „Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo programos atskaitos taško (pvz., mygtuku ar meniu elementu), skirto būtent šiam veiksmui, ER paskirties vieta turi būti pažymėta kaip integravimo taškas. Šiame pavyzdyje tai yra ERTableDestination#VendSettlementTax1099 taškas.  
14. Spustelėkite Atšaukti.
15. Spustelėkite Rodyti viską.
16. Spustelėkite Rodyti tik susietus.
17. Medyje išplėskite „tax1099trans: Lentelės „VendSettlementTax1099” įrašai= model.Validated”.
    * Atkreipkite dėmesį, kad duomenų šaltinio elementas, kuriame yra tik patikrintos operacijos, susietas su sukurta paskirties vieta. Galite filtruoti importuotas operacijas, praleisdami tas, kurios nesuderinamos su programų duomenis.  
18. Medyje pasirinkite „nepavyko: Lentelės „VendSettlementTax1099Entity” įrašai= model.Failed”.
19. Spustelėkite skirtuką Tikrinimai.
    * Šio modelio susiejimas gali būti vartotojo nustatyta logika patikrinti importuotų duomenų iš esamų programos duomenų teisingumą. Pavyzdžiui, pagal dabartinį nustatymą bet kurios operacijos importuotame faile su sistemoje nesančiu tiekėjo kodu atveju bus sugeneruotas įspėjamasis pranešimas, informuojantis vartotoją ir nurodantis neteisingą tiekėjo kodą.  
    * Atminkite, kad parinktį Tolesnio tikrinimo veiksmas galima pritaikyti kiekvienam patikrinimui nurodant, ar būtina tęsti arba stabdyti importavimo procesą, taip pat, jei jau galima saugoti arba atšaukti atliktus įvykius / atnaujinimus.  
20. Spustelėkite Rodyti tik susietus.
21. Spustelėkite Rodyti viską.
22. Uždarykite puslapį.
    * Norėdami išbandyti sukurtą formatą ir modelių susiejimus, vykdykite šio modelio susiejimą. Naudokite failą 1099entries.xml. Duomenys iš pasirinkto failo bus importuoti į sistemą.  
23. Spustelėkite Vykdyti.
    * Atkreipkite dėmesį, kad dialogo lange nėra jokių papildomų klausimų apie formato susiejimą, kuris turi būti naudojamas importuotam failui išanalizuoti ir duomenims į duomenų modelį perkelti. Taip yra todėl, kad šiuo metu šiame modelyje, kuris pažymėtas kaip skirtas duomenų importavimui palaikyti, naudojamas tik vienas formatas.  
    * Jei norite atskirti importuotas operacijas nuo kitų operacijų, kurios jau buvo įvestos rankiniu būdu arba importuotos, nurodykite kvito ID.  
24. Lauke „Įveskite kvito ID” įveskite „IMPORT-001”.
    * Ieškokite failo „1099entries.xml”.  
25. Spustelėkite GERAI.
    * Pateiktų įspėjimų sąraše pateikiama informacija apie neteisingus tiekėjų kodus, netinkamą mokesčių 1099 langelio kodą, trūkstamus šalių kodus ir kt. Šį įspėjimų sąrašą palyginkite su turiniu, įtrauktu į XML vykdymo failą.  
26. Uždarykite puslapį.
27. Uždarykite puslapį.
28. Uždarykite puslapį.
29. Uždarykite puslapį.
30. Eikite į Mokėtinos sumos > Periodinės užduotys > Mokesčiai 1099 > 1099 tiekėjo sudengimas.
    * Šioje formoje rodomos pagal importuotas operacijas sukurtos lentelės Tax1099Summary kaupiamosios operacijos.  
31. Lauke Pradžios data nustatykite datą „2000-01-01“.
32. Spustelėkite Rankiniu būdu atliekamos 1099 operacijos.
    * Šioje formoje pateikiamas rankiniu būdu įtrauktų ir ką tik importuotų operacijų sąrašas.  
33. Atidarykite stulpelio filtrą Kvitas.
34. Įveskite filtro reikšmę „IMPORT-001” lauke „Kvitas” naudodami filtro operatorių „prasideda”.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Peržiūrėti ryšį tarp modelio ir formato susiejimų
1. Uždarykite puslapį.
2. Uždarykite puslapį.
3. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
4. Spustelėkite Ataskaitų konfigūracijos.
5. Medyje pasirinkite „1099 mokėjimų modelis”.
    * Tarkime, kad jums reikia pagalbos importuojant tuos pačius duomenis, bet iš .TXT failų formato.   
6. Spustelėdami Kurti konfigūraciją, atidarykite dialogo langą. 
7. Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį 1099 mokėjimų modelis“.
8. Lauke „Pavadinimas” įveskite „Importuoti duomenis iš TXT failo”.
9. Lauke Palaikomas duomenų importavimas pasirinkite Taip.
10. Spustelėkite Sukurti konfigūraciją.
11. Spustelėkite Konstruktorius.
12. Spustelėkite Susieti formatą su modeliu.
13. Spustelėkite Naujas.
14. Lauke Apibrėžtis įveskite arba pasirinkite reikšmę.
    * Pasirinkite parinktį „1099-MISC”.  
15. Lauke „Pavadinimas” įveskite „Importuoti duomenis iš TXT failo”.
16. Lauke „Aprašas” įveskite „Importuoti duomenis iš TXT failo”.
17. Spustelėkite Įrašyti.
18. Uždarykite puslapį.
19. Uždarykite puslapį.
20. Spustelėkite Redaguoti.
    * Jei įdiegėte karštąją pataisą „KB 4012871 GER duomenų modelio susiejimų į atskiras konfigūracijas su galimybe nurodyti būtinuosius skirtingų rūšių komponentus, diegiant juos kitose „Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo versijose, palaikymas” (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 ), vykdykite kitą veiksmą „Įjungti vėliavėlę Numatytoji modelio susiejimo reikšmė”, skirtą įvestai formato konfigūracijai. Kitu atveju praleiskite tolesnį veiksmą.  
21. Lauke Numatytoji modelio susiejimo reikšmė pasirinkite Taip.
22. Medyje pasirinkite „1099 mokėjimų modelis”.
23. Spustelėkite Konstruktorius.
24. Spustelėkite „Susieti modelį su duomenų šaltiniu“.
25. Spustelėkite Vykdyti.
    * Jei įdiegėte karštąją pataisą KB 4012871 GER duomenų modelio susiejimų į atskiras konfigūracijas su galimybe nurodyti būtinuosius skirtingų rūšių komponentus, diegiant juos kitose „Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo versijose, palaikymas (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 ), peržvalgos lauke pasirinkite pageidaujamo modelio susiejimą. Jei dar neįdiegėte karštosios pataisos, praleiskite tolesnį veiksmą, nes susiejimas jau pasirinktas nustatant numatytojo formato konfigūraciją.  
    * Jei neįdiegėte karštosios pataisos KB 4012871, atkreipkite dėmesį, kad dialogo lange pateikiamas papildomas modelio susiejimo klausimas, naudojamas importuojamam failui išanalizuoti. Tada duomenys perkeliami iš dialogo lango į duomenų modelį. Šiuo metu galite pasirinkti, koks formato susiejimas turi būti naudojamas atsižvelgiant į tai, kokio tipo failą norite importuoti.  
    * Jei šį modelio susiejimą ketinate iškviesti iš „Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo atskaitos taško, skirto būtent šiam veiksmui, ER paskirties vieta ir formato susiejimas turi būti pažymėtas kaip integravimo dalis.  
26. Spustelėkite Atšaukti.
27. Uždarykite puslapį.
28. Uždarykite puslapį.


