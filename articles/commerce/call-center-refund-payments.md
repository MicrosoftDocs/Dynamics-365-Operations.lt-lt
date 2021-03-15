---
title: Grąžinimo mokėjimo tvarkymas skambučių centruose
description: Šiame skyriuje paaiškinta, kaip mokėjimo grąžinimai yra sukuriam per skambučių centrus, sukuriant grąžinimus ar kai užsakymai ar jų eilutės yra atšaukti.
author: hhainesms
manager: annbe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f98fbc14fc2946499a9c003eb0bd0edb7f2017e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991420"
---
# <a name="refund-payment-processing-in-call-centers"></a>Grąžinimo mokėjimo tvarkymas skambučių centruose

Šiame skyriuje paaiškinta, kaip mokėjimo grąžinimai yra sukuriam per skambučių centrus, sukuriant grąžinimus ar kai užsakymai ar jų eilutės yra atšaukti.

Vartotojas sukūręs grąžinimo užsakymą klientui kaip skambučių centro vartotoją „Microsoft Dynamics 365 Commerce“ būstinė naudoja **Grąžinamo užsakymo** puslapį, kuris sukuria pradinį grąžinimo medžiagų leidimą. RMA nustato produktus, kuriuos klientas nori grąžinti ar keisti ir sukuria susietą grąžinimo prekybos užsakymą, kurio užsakymo tipas yra **Grąžintas užsakymas**. Šis susietas grąžinimo užsakymas yra naudojamas siekiant sekti grąžinamo inventoriaus publikavimą ir visas publikuotas kredito pastabas ar mokėjimo grąžinimus.

Jei **Įjungti užsakymo užbaigimo** parinktis yra nustatyta į **Taip** skambučių centro kanalui, skambučių centro vartotojas sukuriantis RMA privalo vykdyti užsakymo užbaigimo tvarkymo eigą pasirinkdamas **Užbaigta** puslapyje **Grąžinimo užsakymas**. Funkcija **Užbaigimas** leidžia apskaičiuoti grąžinamą sumą, kuri nurodo mokėtiną grąžinimo sumą. Taip pat, kai ji teisingai sukonfigūruota, ji sistemiškai sukuria grąžinamo mokėjimo eilutę pagal grąžintą užsakymą.

Skambučių centro logika nustato mokėjimo metodą grąžinamo mokėjimo eilute, kuri pagrįsta mokėjimo metodu naudojamu originaliame užsakyme. Jei grąžinamas užsakymas yra sukuriamas ir nėra susietas su originaliu užsakymu, yra taikomas numatyto mokėjimo metodas, paimamas iš sistemos parametro.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Kaip skambučių centras nustato, kuris mokėjimo metodas turi būti taikomas grąžinimo užsakymui

Skambučių centras naudoja originalaus užsakymo mokėjimo metodą siekiant nustatyti mokėjimo metodą, kuris turi būti taikomas grąžinamam užsakymui. Štai kaip šis procesas veikia tolesniems originalaus mokėjimo metodams:

- **Įprastai** (grynieji) ar **Patikra** – Kai grąžinimo užsakymas yra sukuriamas ir nukreipia į originalų užsakymą, kuris buvo sumokėtas naudojant įprastus (grynus) ar čekio mokėjimo tipą, skambučių centro programa nurodo konfigūravimus **Skambučių centro grąžinimo metodų** puslapyje. Šis puslapis leidžia organizacijoms pagal užsakymo valiutą nustatyti, kaip grąžinimai išduodami klientams užsakymams, kurie originaliai buvo mokami naudojant įprastą ar čekio mokėjimo tipą. Puslapis **Skambučių centro grąžinimo metodai** taip pat leidžia organizacijoms pasirinkti, ar sistemos sukurtas grąžinimo čekis yra siunčiamas klientui, ar kliento paskyros kreditas yra sukuriamas pagal vidinį kliento sąskaitos balansą. Šiais scenarijais, skambučių centro logika nukreipia grąžinamo užsakymo valiutą ir tada naudoja **Mažmenos mokėjimo metodo** vertę tai valiutai tam, kad sukurtų grąžinamo mokėjimo eilutę grąžinimo pardavimų užsakyme. Vėliau, gautinų sąskaitų kliento mokėjimo žurnalas, naudojantis žemėlapio gautinų sąskaitų mokėjimo metodą yra susietas su valiuta.

    Tolesnis paveikslėli rodo konfigūravimus scenarijui, kai kliento grąžinimo produktai iš prekybos užsakymo, susieto su USD valiuta ir tai, kad jis buvo iš pradžių sumokėtas naudojant įprastą ir čekio mokėjimo tipą. Šiame scenarijuje, grąžinimas bus išduodamas klientui per sistemos sukurtą grąžinimo čekį. **REF-CHK** grąžinamų sąskaitų metodas buvo sukonfigūruotas kaip grąžinimo čekio mokėjimo tipas.

    ![Skambučių centro grąžinimo metodų konfigūravimas įprastiems ir čekio originaliems mokėjimams](media/callcenterrefundmethods.png)

- **Kredito kortelė** – Kai grąžinimo užsakymas yra sukurtas ir nukreipia į pradinį užsakymą, kuris buvo sumokėtas naudojant kredito kortelę, skambučių centro logika grąžinimo mokėjimams taikoma tai pačiai kredito kortelei grąžinimo užsakymui.
- **Lojalumo kortelė** – Kai grąžinimo užsakymas yra sukurtas ir nukreipia į pradinį užsakymą, kuris buvo sumokėtas naudojant kliento lojalumo kortelęč, skambučių centro logika grąžinimo mokėjimams taikoma grąžinimui į tą pačią lojalumo kortelę.
- **Dovanų kortelė** (vidinė) – Kai grąžinimo užsakymas yra sukuriamas ir nukreipiamas į pradinį užsakymą, kuris buvo sumokėtas naudojant dovanų kortelę, kurią išdavė „Dynamics 365 Commerce“ (vidinės dovanų kortelės funkcijos), skambučių centro logika grąžinimo užsakymams taikoma siekiant grąžinti tą patį originalios dovanų kortelės numerį.
- **Dovanų kortelė** (Išorinė) – Kai grąžinimo užsakymas yra sukuriamas ir nukreipiamas į pradinį užsakymą, kuris buvo sumokėtas naudojant išorinę trečiųjų šalių dovanų kortelę, skambučių centro logiką grąžinamiems mokėjimams taikoma nustatytam grąžinimo mokėjimo metodui, kkuris nustatytas **RMA/Grąžinimo** skirtuke **Skambučių centro parametrų** puslapyje.

Jei pradinis užsakymo mokėjimo tipas yra nežinomas dėl kokios nors priežasties ar keli mokėjimo metodai buvo naudoti siekiant sumokėti pradinį užsakymą, skambučių centro logika yra taikoma nustatam **RMA/Grąžinimo** skirtukui puslapyje **Skambučių centro parametrai**.

Tolesniame paveikslėlyje rodomas **Mokėjimo metodo** laukelis skirtuke **RMA/grąžinimas** puslapyje **Skambučių centro parametrai**.

![Mokėjimo metodo laukelis skirtuke RMA/grąžinimas puslapyje Skambučių centro parametrai](media/callcenterrefundparameters.png)

> [!NOTE]
> Grąžinimo tvarkymo taisyklės aprašytos anksčiau taip pat yra taikomos užsakymams ar jų eilutėms, kurias skambučių centro vartotojas atšaukia prekybos būstinėje. Jei užsakymo ar konkrečių užsakymo eilučių atšaukimas sudaro kokius nors permokėjimus, tos pačios taisyklės bus naudojams siekiant sukurti grąžinimo mokėjimų eilutes.

Dažniausiai, grąžinimo užsakymas pereina per standartinį procesą, kai inventorius yra gaunamas (ar jo atsisakom), pakavimo lapelis yra publikuojamas pagal grąžinimo užsakymą ir tuomet sąskaitos publikavimo procesas yra vykdomas grąžinimo prekybos užsakymui. Grąžinimo prekybos užsakymas yra susietas ir sistemiškai sukuriamas kaip grąžinimo užsakymo sukūrimo proceso dalis. Dažniausiai scenarijais, mokėjimo grąžinimai nėra išduodami klientams, kol sąskaita už grąžinimo prekybos užsakymą yra publikuota.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Kas atsitinka, kai sąskaita yra publikuojama grąžinimo prekybos užsakyme

Tolesni scenarijai paaiškina, kas atsitinka, kai sąskaita yra publikuojama grąžinimo prekybos užsakyme:

- Jei grąžinamas mokėjimas grąžinimo užsakyme yra kredito kortelei, papildoma logika pasitelkiama, kai sąskaita publikuojama. Ši logika iškviečia paskatina tvarkytoją grąžinti mokėjimą į kliento kredito kortelę. Grąžinamo kliento mokėjimo kuponas taip pat sukuriamas ir sistemiškai publikuojamas pagal kliento sąskaitą. Šis mokėjimo žurnalas bus nustatytas pagal grąžinimo užsakymo kredito pranešimo kuponą.
- Jei grąžinimo mokėjimas turi būti išduodamas patikrinimo mokėjimo tipui, kliento mokėjimo kuponas, naudojants AR mokėjimo metodą yra sukuriamas ir turi būti rankiniu būdu publikuojamas ar atspausdinamas prieš tai, kai mokėjimo kuponas gali būti publikuojamas pagal kliento sąskaitą. Norėdami sutvarkymo grąžinimo patikrą, klientai gali naudoti **Kliento mokėjimo žurnalo** puslapį Gaunamose sąskaitose ar specializuojamasi **Grąžinimo patikro sutvarkymo** puslapyje Mažmeninėje prekyboje ir komercijoje.
- Jei grąžinimo mokėjimas turi būti išduodamas vidinei dovanų kortelei ar lojalumo kortelės mokėjimo tipui, kai grąžinimo užsakymas yra įtraukiamas į sąskaitą, gražinimo mokėjimo kuponas sukuriamas ir publikuojamas pagal kliento sąskaitą. Šis sąskaitos išrašymo žingsnis taip pat įtraukia grąžinimo sumą į kliento vidaus sekimo dovanų kortelės balansą ar lojalumo taškų balansą.
- Jei mokėjimo metodas naudoja **Kliento** funkciją (pavyzdžiui, kliento paskyrą), jis yra susiejamas su grąžinimo prekybos užsakymu, kredito limito patvirtinimai ignoruojami, kai mokėjimas yra apdorojamas. Nesukuriamas ir nepublikuojamas joks mokėjimo kuponas šiame kontekste. Kai kliento mokėjimo tipas yra naudoajmas grąžinimo užsakyme, kredito pranešimo kuponas, kurį sutvarko sąskaitos publikavimas, yra naudojamas kaip kliento kredito kuponas ir nurodo atlyginimą į kliento gautinų sąskaitų balansą.

## <a name="advance-credit"></a>Išankstinis kreditas

Kai klientas sutvarko grąžinimo užsakymus kaip skambučių centro vartotojas skambučių centre, kuriame **Įjungti užsakymo užbaigimo** parinktis nustatyta į **Taip**, išlyga į anksčiau aprašytą procesą dėl grąžinimo mokėjimo publikavimo gali įvykti, jei skambučių centro vartotojas, sukuriantis grąžinimo užsakymą nustato **Išankstinis kreditas** parinktį į **Taip** skirtuke **RMA/Grąžinimas** puslapyje **Skambučių centro parametrai**. Šiuo atveju, mokėjimo grąžinimas vyksta iš karto po to, kai grąžinimo užsakymas yra sėkmingai pateikiamas naudojant **Pateikimo** funkciją **Grąžinimo santrauka** puslapyje. Sistema nedelsiant sukuria išankstinio mokėjimo kliento mokėjimo kuponą grąžinamai vertei, net jei grąžinimo prekybos užsakymas dar nebuvo įtrauktas į sąskaitą. Toks požiūris gali būti naudojamas tada, kai organizacija turi išduoti grąžinimus klientams iš anksto dėl kliento paslaugų problemų ir nenori reikalauti grąžinti inventorių ir gauti prieš išduodant grąžinimus.

## <a name="replacement-orders"></a>Pakeitimo užsakymai

Išdavus grąžinimo užsakymą **Užsakymo keitimo** funkcija gali būti naudojama siekiant sukurti naują prekybos užsakymą klientui. Toks požiūris gali būti naudojamas apsikeitimo scenarijais. Funkcija **Pakeitimo užsakymas** sukuria kitą prekybos užsakymą naujiems objektams, kurie turi būti siunčiami, tačiau kryžminė nuorods sąsaja **RMA/Grąžinimo** skirtuke puslapyje **Skambučių centro parametrai** susieja pakeitimo užsakymą, RMA ir grąžinimo prekybos užsakymą.

Kai mokėjimai pakaitiniame užsakyme yra apdorojami, organizacijos turi dvi parinktis:

- Grąžinti klientui grąžinimo užsakymą pagal pradinio mokėjimo metodą ir tada surinkti atskirą mokėjimą dėl pakaitinio užsakymo. Šiai parinkčiai naudoti nereikia jokios papildomos konfigūracijos.
- Nustatykite **Taikyti kreditą** parinktį į **Taip** skirtuke **RMA/Grąžinimas** puslapyje **Skambučių centro parametrai**. Tokiu atveju, kliento mokėjimo metodas sistemiškai taikomas grąžinimo užsakymui ir keitimo užsakymui. Ši parinktis gali padėti apsaugoti visus išorinius grąžinimo mokėjimus nuo išdavimo. Tai taip pat padeda apsaugoti visus mokėjimo tvarkymus transakcijoje. Jis gali būti naudingas tada, kai lygus keitimas yra tvarkomas ir organizacija nori naudoti kredito kuponą, sukurtą, kai grąžinimo užsakymas įtraukiamas į sąskaitą siekiant sumokėti už sąskaitą, kuri buvo sukurta keitimo užsakymo. Nustačius **Taikyti kreditą** parinktį į **Taip**, organizacija privalo rankiniu būdu nustatyti kredito pranešimą pagal pakeitimo užsakymo sąskaitą, kai abu minėti finansiniai dokumentai buvo sukurti.

Nustačius **Taip** parinkčiai **Taikyti kreditą**, ji yra taikoma tik grąžinimo užsakymai, kuris bus susietas su pakeitimo užsakymu. Tokiu atveju, kliento mokėjimo metodas bus naudojamas sistemiškai sumokėti už grąžinimo ir pakeitimo užsakymą, kuris nustatomas **Taikydi kreditų mokėjimo metodą** laukelyje **RMA/Grąžinimo** skirtuke **Skambučių centro parametrų** puslapis. Tik **Kliento** funkcijos mokėjimo tipas gali būti pasirenkamas šiame laukelyje.

> [!NOTE]
> Grąžinimo užsakymui, kuris nebuvo susietas su jokiu pakeitimo užsakymu, parinkties **Taip** nustatymas **Taikyti kreditą** niekaip neveiks grąžinimo užsakymo mokėjimo logikos, nes šis nustatymas taikomas tik pakeitimo užsakymams.

![Taikyti kreditų mokėjimo metodo laukelį skirtuke RMA/grąžinimas puslapyje Skambučių centro parametrai](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Jei vartotojai, sukūrę pakeitimo užsakymus, planuoja naudoti **Taikyti kreditą** parinktį, jie neturėtų vykdyti **Užbaigti** funkciją grąžinimo užsakyme prieš nustatę **Taikyti kreditą** parintkį į **Taip**. Įvykdžius funkciją **Užbaigta**, grąžinimo mokėjimas yra apskaičiuojamas ir taikomas grąžinimo prekybos užsakymui. Bet koks bandymas nustatyti **Taikyti kreditą** parinktį į **Taip** po to, kai grąžinimo mokėjimas jau buvo apskaičiuotas ir taikomas, neiššauks grąžinimo mokėjimo perskaičiavimo ir mokėjimo metodas pasirinktas **Taikyti kreditų mokėjimo metodą** laukelyje taikomas nebus. Jei **Taikyti kreditą** parinktis turi būti naudojama šiame kontekste, vartotojas privalo panaikinti keitimo užsakymą ir RMA bei iš naujo pradėti ir sukurti naują RMA. Dabar vartotojas privalo užtikrinti, kad **Taikyti kreditą** parinktis yra nustatyta į **Taip** prieš **Užbaigti** funkcijos vykdymą.

## <a name="payment-overrides-for-call-center-returns"></a>Mokėjimas viršija skambučių centrų grąžinimus

Nepaisant to, kad skambučių centro logika sistemiškai nustato grąžinimo mokėjimo metodą aprašytą toliau šioje temoje, vartotojams kartais gali reikėti viršyti šiuos mokėjimus. Pavyzdžiui, vartotojui gali reikėti redaguoti ar pašalinti esančias grąžinimo mokėjimo eilutes ir taikyti naujas mokėjimo eilutes. Sistemos aspakčiuoti grąžinimo mokėjimai gali būti keičiami tik vartotojų, turinčių tinkamas viršijimo teises. Šios teisės gali būti konfigūruojamos **Viršyti teises** puslapyje Mažmenos prekyboje ir Komercijoje. Norėdami atlikti grąžinimo mokėjimo viršijimą, vartotojai turi būti susieti su saugos vaidmeniu, kuriame **Leisti alternatyvų mokėjimą** parinktis yra nustatyta į **Taip** puslapyje **Viršyti leidimus**.

![Leisti alternatyvią mokėjimo parinktį Viršyti teises puslapyje](media/overridepermissions.png)

Kitu atveju, organizacija gali nustatyti **Leistim mokėjimo viršijimo** parinktį į **Taip** puslapyje **RMA/Grąžinimas** skirtuke, **Skambučių centro parametrai** puslapyje. Tokiu atveju, saugos viršijimo kodas turi būti pasirinktas **Saugo viršijimo kodo** laukelyje. Saugumo viršijimo kodas yra skaitinis ir raidnis kodas, kuris turi būti sutvarkytas išorėje, nes vartotojai negali peržiūrėti jo Komercijos būstinėje po jo nustatymo. Saugos viršijimo kodas turi būti žinomas tik keliams pagrindiniams, organizacijoje pasitikėjimą turintiems asmenims. Kai **Leisti mokėjimo viršijimą** parinktis yra nustatyta į **Taip**, jei bet kokie vartotojai, neturintys tinkamo vaidmens teisių bando pakeisti mokėjimo metodą grąžinimo užsakyme, jie turės parinktį įvesti saugos viršijimo kodą. Jei jie jo nežino ar vadovas, arba viršininkas negali jo įvesti puslapyje jų vardu, jie negalės viršyti grąžinimo mokėjimo metodo.

> [!NOTE]
> Jei saugos viršijimo kodas yra prarastas ar pamirštas, organizacija turės jį paleisti iš naujo nustatydama naują saugos viršijimo kodą **Saugos viršijimo kodo** laukelyje **RMA/Grąžinimo** skirtukas puslapyje **Skambučių centro parametrai**.

![Mokėjimo viršijimo parametrai RMA/grąžinimas puslapyje Skambučių centro parametrai](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Prieš tai, kai organizacijos bando viršyti grąžinimo mokėjimus, kurie naudoja kredito kortelės mokėjimo tipus, jie turi bandyti patvirtinti, kad jų kredito kortelės tvarkytojas leidžia nesusietus grąžinimus. Daugelis tvarkytojų prašo grąžinimus pervesti į pradinę kortelę. Visi bandymai išduoti grąžinimą į kortelę, kuri neturi ankstesnių duomenų, gali sukelti publikavimo klaidas su tvarkytoju.

## <a name="additional-resources"></a>Papildomi ištekliai

[Mokėjimo būdai skambučių centruose](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]