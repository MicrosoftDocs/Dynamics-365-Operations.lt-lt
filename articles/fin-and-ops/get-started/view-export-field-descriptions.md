---
title: "Laukų aprašų peržiūra ir eksportas"
description: "Šiame straipsnyje aprašoma, kaip peržiūrėti laukų aprašymus ir kaip naudoti puslapį Laukų aprašymai, norint eksportuoti aprašymus."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 7be1495fc42b5f19884a7d9df747f6bec9b64680
ms.contentlocale: lt-lt
ms.lasthandoff: 12/18/2018

---

# <a name="view-and-export-field-descriptions"></a>Laukų aprašų peržiūra ir eksportas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip peržiūrėti laukų aprašymus ir kaip naudoti puslapį Laukų aprašymai, norint eksportuoti aprašymus.

„Microsoft Dynamics 365 for Finance and Operations“ pateikiami kai kurių sudėtingesnių laukų aprašai. Šie aprašymai bus rodomi, kai užveskite pelės žymeklį virš lauko. Puslapyje **Laukų aprašymai** aprašymus taip pat galite peržiūrėti ir eksportuoti.

Laukų aprašai yra ne visuose puslapiuose. Norime pateikti tik sudėtingesnių laukų aprašymus, o ne tų, kurių naudojimas yra aiškus. Todėl kai kuriuose puslapiuose aprašymai nerodomi, kai kuriuose puslapiuose rodomi keli aprašymai, o kai kuriuose sudėtingesniuose puslapiuose, pvz., daugelyje parametrų puslapių, rodoma daug aprašymų.

Jei turite prieigą prie „Finance and Operations“ programavimo aplinkos, galite įtraukti naujų laukų aprašų ir tinkinti esamus aprašus. Pavyzdžiui, į lauko aprašymą galite įtraukti įmonei būdingą informaciją. Daugiau informacijos žr. dalyje [Lauko žinyno tinkinimas](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Peržiūrėkite laukų aprašymus vartotojo sąsajoje.

Laukų aprašus galite peržiūrėti užvesdami pelės žymeklį virš lauko. Jei aprašymo nėra, užvedę pelės žymeklį virš lauko matysite lauko pavadinimą.

> [!NOTE]
> Naudojant „Dynamics AX“ 7.0 versiją (2016 m. vasario mėn.), laukų aprašymus galima peržiūrėti tik puslapyje **Laukų aprašymai**.

Toliau pateiktoje iliustracijoje parodytas lauko aprašymas, kuris rodomas pelės žymeklį užvedus virš lauko **Blokuoti prekes jas inventorizuojant**.

[![Lauko aprašo pavyzdys](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Puslapio Laukų aprašymai naudojimas lauko žinynui peržiūrėti ir eksportuoti

Puslapyje **Laukų aprašymai** galite peržiūrėti ir eksportuoti laukų aprašymus. Galite peržiūrėti aprašus, kurie vienu metu pateikiami viename puslapyje.

### <a name="view-the-descriptions-for-a-page"></a>Puslapio laukų aprašų peržiūra

Norėdami peržiūrėti puslapio laukų aprašymus, atlikite tolesnį veiksmą.

- Lauke **Pasirinkti puslapį** įveskite puslapio pavadinimą. Arba spustelėkite rodyklę, norėdami atidaryti visų puslapių sąrašą, o tada sąrašą naršykite arba filtruokite.

Galite naudoti puslapio, kuris rodomas vartotojo sąsajoje, pavadinimą (pvz., **Klientai**) arba kodo pavadinimą (AOT pavadinimą), kur pasiekiamas puslapyje spustelėjus dešiniuoju pelės klavišu, (pvz., **CustTable**).

Informacijos apie įvairius būdus, kaip filtruoti puslapių sąrašą, žr. tolesnėje šio straipsnio dalyje „Puslapio ieška“.

Nustačius parinktį **Įtraukti laukus be aprašymo** į **Taip**, visi bus rodomi visi puslapio laukai nepriklausomai nuo to, ar jie turi laukų aprašymus.

### <a name="export-the-descriptions-for-a-page"></a>Puslapio laukų aprašų eksportavimas

Norėdami eksportuoti puslapio laukų aprašymus, atlikite tolesnius veiksmus.

1. Lauke **Pasirinkti puslapį** pasirinkite puslapį.
2. Spustelėkite viršutiniame dešiniajame kampe esantį mygtuką **Atidaryti naudojant „Microsoft Office“**, tada pasirinkite **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Puslapio paieška

Lauke **Pasirinkti puslapį** puslapio galima ieškoti keliais būdais. Daugeliu atvejų reikia spustelėti rodyklę lauke **Pasirinkti puslapį**, norint atidaryti išplečiamąjį sąrašą, ir tada pasirinkti iš filtruoto puslapių sąrašo.

- Įrašykite dalį pavadinimo, o tada atidarykite išplečiamąjį sąrašą, kad pasirinktumėte iš filtruoto puslapių sąrašo.
- Atidarykite išplečiamąjį sąrašą ir tada spustelėkite antraštę **Puslapio pavadinimas** sąrašo viršuje arba antraštę **Puslapio AOT pavadinimas**. Atidaromas dialogo langas, kuriame galite naudoti išplėstinio filtravimo parinktis, pvz., **Puslapio pavadinimas prasideda**.
- Įrašyti visą puslapio pavadinimą. Jei naudojate šią parinktį, geriausia atidaryti išplečiamąjį sąrašą ir peržiūrėti, kas dar yra sąraše, net jei rodomi laukų aprašymai.

    - Jei yra tik vienas tikslus pavadinimo atitikmuo, bus rodomi puslapio laukų aprašymai.
    - Jei yra daugiau nei vienas tikslus atitikmuo, aprašymai nebus rodomi. Jums reikės atidaryti išplečiamąjį sąrašą ir pasirinkti tą puslapį, kurio reikia.
    - Jei įrašytasis pavadinimas taip pat yra ir kito puslapio pavadinimo dalis, matysite savo puslapio laukų aprašymus. Tačiau jei atidarysite išplečiamąjį sąrašą, pamatysite papildomus puslapius, kurie apima šį pavadinimą.

Pavyzdžiui, aprašymai nepateikiami lauke **Pasirinkti puslapį** įvedant **Skaičiavimas**. Jei atidarysite išplečiamąjį sąrašą, pamatysite, kad yra du puslapiai pavadinimu **Skaičiavimas**, taip pat keli puslapiai, kurių pavadinimuose yra žodis „Skaičiavimas“. Jei pasirinksite puslapį, kurio AOT pavadinimas yra **InventJournalCount**, bus rodomi to puslapio laukų aprašymai. Tačiau jei dar kartą atidarysite išplečiamąjį sąrašą, pamatysite, kad sąraše pateikti visi puslapiai, kurių AOT puslapio pavadinimai apima „InventJournalCount“.

## <a name="troubleshooting"></a>Trikčių diagnostika

Šiame skyriuje pateikiama informacija, kuria siekiama padėti jums išspręsti problemas, galinčias kilti naudojant laukų aprašymus.

### <a name="i-cant-find-a-field-description"></a>Nepavyksta rasti lauko aprašo

Mes rengiamės įtraukti sudėtingesnių laukų aprašų. Jei jums reikia pagalbos dėl konkretaus lauko, susisiekite su mumis parašydami komentarą prie šios temos.

### <a name="the-field-description-isnt-helpful"></a>Lauko aprašas nenaudingas

Susisiekite su mumis parašydami komentarą prie šios temos. Jei galite, apibūdinkite papildomą informaciją, kuri jums reikalinga.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Puslapyje Laukų aprašymai negaliu rasti lauko

Norėdami, kad visi laukai būtų rodomi puslapyje, pasirinkite pasirinkties **Įtraukti laukus be aprašo** nustatymą **Taip**. Spustelėkite lauką **Pasirinkti puslapį** ir įsitikinkite, kad pasirinkote teisingą puslapį. Jei jūsų įvestas pavadinimas yra kito lauko pavadinimo dalis, galbūt jūs pasirinkote puslapį, kurio pavadinimas ilgesnis.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Puslapyje Laukų aprašymai negaliu rasti puslapio

Informacijos apie įvairius būdus, kaip rasti puslapius, žr. ankstesnėje šio straipsnio dalyje „Puslapių ieška“. Įrašius tikslų puslapio pavadinimą, laukų aprašymai gali būti nerodomi, jei yra daugiau nei vienas puslapis tokiu pačiu pavadinimu. Spustelėkite rodyklę lauke **Pasirinkti puslapį**, jei norite atidaryti filtruotą puslapių sąrašą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Lauko žinyno tinkinimas](../../dev-itpro/user-interface/customize-field-help.md)

