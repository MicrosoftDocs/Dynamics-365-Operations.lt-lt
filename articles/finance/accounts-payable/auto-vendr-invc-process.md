---
title: Automatizuotų tiekėjo SF išrašymo procesų apžvalga
description: Šioje temoje aprašoma jūsų tiekėjo SF apdorojimo automatizavimo funkcija ir automatizuoto proceso naudojimo privalumai.
author: abruer
manager: AnnBe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9a033258feeccf172f1e2c03a9f49305054b24c2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972136"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Automatizuotų tiekėjo SF išrašymo procesų apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma jūsų tiekėjo SF apdorojimo automatizavimo funkcija ir automatizuoto proceso naudojimo privalumai. Šią funkciją sudaro funkcijos, įjungtos funkcijų valdyme. Šios funkcijos taikomos tik tiekėjo SF, o ne SF, kurios apdorojamos naudojant puslapius **SF žurnalas** arba **SF registro žurnalas**.

Organizacijos dažnai dirba su trečiosiomis šalimis, kad popierinės SF būtų apdorotos naudojant optinio ženklų atpažinimo (OCR) paslaugų teikėją. Paslaugų teikėjas pateikia kompiuteriu nuskaitomus SF metaduomenis. Modulio Mokėtinos sumos automatizavimo funkcijos leidžia naudoti šiuos artefaktus modulyje Mokėtinos sumos, kad būtų lengviau atlikti automatizavimą.

Galite automatizuoti kai kuriuos modulio Mokėtinos sumos tiekėjo SF išrašymo procesus. Šie procesai apima importuotų tiekėjo SF pateikimą darbo eigos sistemai ir užregistruotų produktų gavimo kvitų eilučių sugretinimas su patvirtinimo laukiančiomis tiekėjo SF eilutėmis. Automatizuotas procesas nurodo informaciją apie tiekėjo SF eigą, kai ji pereina kiekvieną procesą. Ši funkcija gali padėti modulio Mokėtinos sumos tarnautojams ir vadovams apdoroti tiekėjo SF efektyviau. Ji taip pat padeda sumažinti klaidų ir neveiksmingumo atvejų, kurie gali įvykti, kai informacija įvedama ir apdorojama neautomatiniu būdu, skaičių.

Automatizavimo procesai gali būti naudojami norint atlikti toliau nurodytas užduotis.

- Automatiškai pateikti importuotas SF darbo eigos sistemai.
- Gretinti produktų gavimo kvitus su patvirtinimo laukiančiomis tiekėjo SF eilutėmis.
- Imituoti registravimą prieš registruojant tiekėjo SF.
- Greitai ir efektyviai peržiūrėti darbo eigos bei automatizavimo retrospektyvą.
- Peržiūrėti ir analizuoti tiekėjo SF apdorojimo automatizavimo rezultatus.
- Tęsti automatizuotą kelių SF apdorojimą.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Tiekėjo SF automatizavimas – importuotų tiekėjo SF pateikimas darbo eigos sistemai

Bekontakčio modulio Mokėtinos sumos SF išrašymo proceso metu sistema gali automatiškai pateikti importuotą SF darbo eigos sistemai. Procesas bus vykdomas fone tokiu dažnumu, kokį nurodysite (kas valandą ar kas dieną). Norint automatiškai pateikti importuotas SF darbo eigos sistemai, reikia, kad jūsų procesas prasidėtų importuota SF. Norint užtikrinti, kad SF gali būti apdorota nuo pradžios iki pabaigos be rankinio įsikišimo, automatizuotos registravimo užduotys turi būti įtrauktos į darbo eigos konfigūraciją.

SF, susijusios su pirkimo užsakymais (PU), ir SF, kuriose yra ne PU įsigijimo kategorija ir nekaupiamų prekių eilučių, gali būti automatiškai pateiktos darbo eigos sistemai. SF, kurios yra įvedamos neautomatiniu būdu, ir SF, sukurtos naudojant darbo sritį **Tiekėjo bendradarbiavimo SF išrašymas**, turi būti pateiktos neautomatiniu būdu darbo eigos sistemai.

Automatizavimo funkcija suteikia lanksčią sistemą, leidžiančią nustatyti įmonei būdingas taikomas taisykles, skirtas pateikti importuotas tiekėjo SF darbo eigos sistemai ir gretinti produktų gavimo kvitų eilutes su patvirtinimo laukiančiomis tiekėjo SF eilutėmis.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Tiekėjo SF automatizavimas – produkto gavimo kvitų gretinimas su SF eilutėmis, kurių strategija yra trišalė atitikimo strategija

Sistema gali automatiškai sugretinti užregistruotus produktų gavimo kvitus su SF eilutėmis, kurias apibrėžia trišalė atitikimo strategija. Procesas bus vykdomas, kol sugretinto produkto gavimo kvito kiekis bus lygus SF kiekiui. Šio proceso metu galite nurodyti maksimalų kartų, kai sistema turi bandyti sugretinti produkto gavimo kvitus su SF eilute prieš padarydama išvadą, kad procesas nepavyko, skaičių. Procesas bus vykdomas fone kas valandą arba kas dieną. Automatizuotą atitikimo procesą galite vykdyti kaip SF pateikimo darbo eigos sistemai proceso dalį. Taip pat jį galite vykdyti kaip atskirą procesą.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Tiekėjo SF automatizavimas – išankstinis tiekėjo SF registravimo tikrinimas

Registravimo modeliavimas užbaigia tikrinimo veiksmus, atliekamus tiekėjo SF registravimo proceso metu, bet sąskaitos neatnaujinamos. Norėdami vykdyti procesą, galite pasirinkti vieną arba kelias SF puslapyje **Laukiančios tiekėjo SF**.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Tiekėjo SF automatizavimas – patobulinta tiekėjo SF darbo eigos ir automatizavimo retrospektyvos informacijos peržiūra

Pateikiamas lengvai skaitomas tiekėjo SF darbo eigos retrospektyvos rodinys. Tiekėjo SF darbo eigos retrospektyvą galima pasiekti tiesiogiai iš tiekėjo SF. Todėl, norint rasti šią informaciją, reikia atlikti mažiau spustelėjimų. Jei jūsų organizacija yra įjungusi galimybę automatiškai pateikti importuotas tiekėjo SF į darbo eigą, yra pateikiama importuotų SF automatizavimo retrospektyva. Automatizavimo retrospektyva padeda rasti dabartinį proceso veiksmą bei jau baigtus veiksmus. Kai veiksmas nesėkmingas, sistema pateikia išsamią informaciją, kuri padės suprasti gedimo priežastį.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Tiekėjo SF automatizavimas – analizė ir metrika

Darbo sritis **Tiekėjo SF įrašas** leidžia sutelkti dėmesį į tiekėjo SF, kurios neperėjo automatizuoto proceso. Darbo srities plytelės teikia informaciją apie tiekėjo SF, kurios nebuvo sėkmingai pateiktos darbo eigos sistemai, importuotos ar sugretintos su produktų gavimo kvitais. Taip pat pateikiama „Microsoft Power BI” metrika, siekiant suteikti modulio Mokėtinos sumos vadovams įžvalgų apie tiekėjo SF automatizavimo efektyvumą.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Tiekėjo SF automatizavimas – kelių SF automatizuoto apdorojimo tęsimas
Kai importuota SF sėkmingai nepateikta į darbo eigą naudojant automatinį procesą, sistema ją pašalina iš tolesnio automatizuoto apdorojimo. Mokėtinų sumų klerkas gali peržiūrėti ir redaguoti sąskaitą faktūrą, prieš tai, kai automatizuotas procesas iš naujo pateikia ją darbo eigai. Kai gedimo priežastis gali būti išspręsta naudojant tą patį pataisymą keliose SF, galite iš naujo paleisti automatizuotą procesą puslapyje **Automatizuoto SF apdorojimo tęsimas**. 
