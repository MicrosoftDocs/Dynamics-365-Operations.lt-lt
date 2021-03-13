---
title: Formato keitimas siekiant generuti dokumentus, kuriuose yra prašymo duomenys
description: Šioje temoje aprašoma, kaip kurti elektroninių ataskaitų konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e820e909bcd80b4747c06ccaaeb05c03f52b6963
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129402"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Formato keitimas siekiant generuti dokumentus, kuriuose yra prašymo duomenys

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (3 dalis: modifikuoti modelį ir susiejimą)“.

Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis. Taikydami šią procedūrą modifikuosite ER konfigūracijas, kad jas naudotumėte ne tik elektroniniams dokumentams generuoti, bet ir programos duomenims atnaujinti. Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.


## <a name="modify-format-to-collect-details-of-reporting"></a>Keiskite formatą, norėdami rinkti ataskaitų informaciją
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite „Intrastat (model)“.
3. Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.
4. Spustelėkite Konstruktorius.
5. Medyje išplėskite „File“.
6. Medyje išplėskite „File\Declaration“.
7. Medyje pasirinkite „File\Declaration\Data“.
8. Lauke Daugialypumas pasirinkite „Vienas daug“.
    * Konfigūruokite šį formato elementą informacijai apie Intrastat ataskaitų kūrimo procesą archyvuoti. Šis elementas nurodo archyvo antraštės įrašą.  
9. Medyje išplėskite „File\Declaration\Data“.
10. Medyje pasirinkite „File\Declaration\Data\Item“.
11. Lauke Daugialypumas pasirinkite „Nulis daug“.
    * Konfigūruokite šį formato elementą informacijai apie Intrastat ataskaitų kūrimo procesą archyvuoti. Šis elementas nurodo suarchyvuotų eilučių sąrašą.  
12. Medyje išplėskite „File\Declaration\Data\Item“.
13. Medyje pasirinkite „File\Declaration\Data\Item\Dim1“.
14. Lauke Neįtraukta pasirinkite Taip.
    * Jūs nearchyvuosite šių duomenų, todėl galite pašalinti šį formato elementą iš Intrastat ataskaitų informacijos duomenų šaltinio.  
15. Medyje išplėskite „File\Declaration\Data\Item\Dim1“.
16. Medyje pasirinkite „File\Declaration\Data\Item\Dim1\property“.
17. Lauke Neįtraukta pasirinkite Taip.
18. Medyje pasirinkite „File\Declaration\Data\Item\Dim1\date“.
19. Lauke Neįtraukta pasirinkite Taip.
20. Medyje pasirinkite „File\Declaration\Data\Item\Dim2“.
21. Lauke Neįtraukta pasirinkite Taip.
22. Medyje išplėskite „File\Declaration\Data\Item\Dim2“.
23. Medyje pasirinkite „File\Declaration\Data\Item\Dim2\property“.
24. Lauke Neįtraukta pasirinkite Taip.
25. Medyje pasirinkite „File\Declaration\Data\Item\Dim2\code“.
26. Lauke Neįtraukta pasirinkite Taip.
27. Medyje pasirinkite „File\Declaration\Data\Item\Dim3“.
    * Keli formato elementai gali turėti tokį patį pavadinimą. Pavyzdžiui, Dim. Negalite aiškiai atpažinti jų, kai naudojate šį formatą kaip duomenų šaltinį Intrastat ataskaitų informacijai archyvuoti, todėl turite nurodyti alternatyvius šių formato elementų pavadinimus.   
28. Lauke „Pavadinimas“ įveskite „Suma“.
    * Suma  
29. Lauke Daugialypumas pasirinkite „Tiksliai vienas“.
30. Medyje pasirinkite „File\Declaration\Data\Item\Dim4“.
31. Lauke „Pavadinimas“ įveskite „Prekė“.
    * Produktas  
32. Lauke Daugialypumas pasirinkite „Tiksliai vienas“.
    * Be dizaino formato elementų, šie Intrastat ataskaitos duomenys turi būti archyvuoti: unikalus kiekvienos paskelbtos prekės įrašo identifikatorius ir sugeneruoto failo vardas. Kadangi šie duomenys nebus perkelta į Intrastat ataskaitą, turite pridėti formatą, kuris yra susijęs su šiais informacijos elementais, kaip duomenų šaltinio elementai.  
33. Medyje pasirinkite „File\Declaration\Data“.
34. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
35. Medyje pasirinkite „Data source\Item“.
36. Lauke Pavadinimas įveskite Failo vardas.
    * Failo vardas  
37. Lauke Duomenų tipas pasirinkite „Eilutė“.
38. Spustelėkite GERAI.
39. Medyje pasirinkite „File\Declaration\Data\Item“.
40. Spustelėkite Įtraukti prekę.
41. Lauke Pavadinimas įrašykite „Prekės įr. ID“.
    * Prekės įr. ID  
42. Lauke Duomenų tipas pasirinkite „Int64“.
43. Spustelėkite Gerai.
44. Spustelėkite skirtuką „Susiejimas“.
45. Medyje pasirinkite „File\Declaration\Data\File name“.
46. Spustelėkite Susieti.
47. Medyje išplėskite „modelis‟.
48. Medyje išplėskite „model\Transactions“.
49. Medyje pasirinkite „File\Declaration\Data\Item = model.Transactions\Commodity rec ID“.
50. Medyje pasirinkite „model\Transactions\Commodity rec ID“.
51. Spustelėkite Susieti.
52. Spustelėkite Įrašyti.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Keiskite formatą, norėdami įsiminti ataskaitų informaciją

1. Spustelėkite Susieti formatą su modeliu.
2. Spustelėkite Naujas.
3. Lauke Apibrėžtis įveskite arba pasirinkite šakninį elementą „Programos duomenų naujinimui“.
    * Programos duomenų atnaujinimui.
4. Lauke Pavadinimas įrašykite „Susiejimas duomenų atnaujinimui“.
    * Susiejimas duomenims atnaujinti  
5. Spustelėkite Įrašyti.
    * Šis susiejimas apibrėžia, kaip „Intrastat“ ataskaitos duomenys surenkami duomenų modelyje, kurio struktūra yra nustatoma pagal pasirinktą šakninį elementą „Programos duomenų naujinimui“. Šie duomenys, modelio susiejimas su tuo pačiu šakniniu elementu „Programos duomenų naujinimui“ ir kryptis „Į paskirties vietą“ bus naudojami programos duomenų naujinimui. Programos duomenų atnaujinimas prasideda iš karto po to, kai sugeneruojama siunčiama Intrastat ataskaita. Programos duomenų atnaujinimas gali būti praleidžiamas vykdymo metu, tačiau duomenų modelis turi būti tuščias (su tuščiu įrašų sąrašu).
6. Spustelėkite Konstruktorius.
    * Siunčiamos Intrastat ataskaitos formatas yra įtrauktas numatytai kaip šio modelio susiejimo duomenų šaltinis.  
    * Susiekite sukurtos ataskaitos elementus (pateikiamus kaip duomenų šaltinis) su duomenų modelio, kuris filtruojamas pagal pasirinktą modelio šakninį elementą, elementais.  
7. Medyje išplėskite „Archyvo antraštė“.
8. Medyje išplėskite „Archive header\Archive lines“.
9. Medyje išplėskite „format“.
10. Medyje pasirinkite „format\Declaration: XML Element(Declaration)“.
11. Medyje išplėskite „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)“.
12. Medyje išplėskite „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)“.
13. Medyje išplėskite „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)“.
14. Medyje išplėskite „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)“.
15. Medyje pasirinkite „Archive header\Number of lines“.
16. Spustelėkite Redaguoti.
17. Medyje pasirinkite „List\COUNT“.
18. Spustelėkite „Įtraukti funkciją“.
19. Medyje išplėskite „format“.
20. Medyje pasirinkite „format\Declaration: XML Element(Declaration)“.
21. Medyje išplėskite `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`.
22. Medyje pasirinkite `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
23. Spustelėkite „Įtraukti duomenų šaltinį“.
24. Lauke Formulė įveskite „COUNT(format.Declaration.Data.Item)“.
    * COUNT(format.Declaration.Data.Item)  
25. Spustelėkite Įrašyti.
26. Uždarykite puslapį.
27. Medyje pasirinkite „Archive header\File name“.
28. Medyje pasirinkite „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name)“.
29. Spustelėkite Susieti.
30. Medyje pasirinkite `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)`.
31. Medyje pasirinkite „Archive header\Archive lines\Item number“.
32. Spustelėkite Susieti.
33. Medyje pasirinkite `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)`.
34. Medyje pasirinkite „Archive header\Archive lines\Amount“.
35. Spustelėkite Susieti.
36. Medyje pasirinkite `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)`.
37. Medyje pasirinkite „Archive header\Archive lines\Commodity rec ID“.
38. Spustelėkite Susieti.
39. Medyje pasirinkite „Archive header\Archive lines“.
40. Medyje pasirinkite `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
41. Spustelėkite Susieti.
42. Medyje pasirinkite „Archyvo antraštė“.
43. Medyje pasirinkite `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`.
44. Spustelėkite Susieti.
45. Spustelėkite Įrašyti.
46. Uždarykite puslapį.
47. Uždarykite puslapį.
48. Uždarykite puslapį.
