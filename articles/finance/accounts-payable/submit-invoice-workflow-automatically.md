---
title: Sąskaitų faktūrų pateikimas darbo eigos sistemai ir produkto gavimo kvito eilučių sugretinimas
description: Šioje temoje paaiškinama, kaip pateikti tiekėjo sąskaitas faktūras į darbo eigos sistemą ir automatiškai sugretinti užregistruotų produktų gavimo kvito eilutes su tiekėjo sąskaitomis faktūromis.
author: abruer
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fd7ec9f4f30c444fd6442c9a2f1333fcaba4246520de3997f3bb9064a8ee16e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736976"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Sąskaitų faktūrų pateikimas darbo eigos sistemai ir produkto gavimo kvito eilučių sugretinimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip pateikti tiekėjo sąskaitas faktūras į darbo eigos sistemą ir automatiškai sugretinti užregistruotų produktų gavimo kvito eilutes su tiekėjo sąskaitomis faktūromis.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Importuotų tiekėjo sąskaitų faktūrų pateikimas į darbo eigos sistemą ir užregistruotų produktų gavimo kvitų eilučių sugretinimas su patvirtinimo laukiančiomis tiekėjo sąskaitos faktūros eilutėmis

Bekontakčio modulio Mokėtinos sumos SF išrašymo proceso metu sistema gali automatiškai pateikti importuotą SF darbo eigos sistemai. Importuotų sąskaitų faktūrų pateikimą į darbo eigos sistemą galite konfigūruoti skirtuke **Tiekėjo sąskaitų faktūrų automatizavimas**, esančiame puslapyje **Mokėtinų sumų parametrai** (**Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**). Pateikimo į darbo eigą procesas bus vykdomas fone jūsų nurodytu dažnumu (kas valandą arba kas dieną).

Kai sąskaitas faktūras į darbo eigos sistemą pateikiate automatiškai, turite pradėti nuo importuotos sąskaitos faktūros. Norint užtikrinti, kad sąskaita faktūra galėtų būti apdorota nuo pradžios iki pabaigos be rankiniu būdu atliekamų veiksmų, į darbo eigos konfigūraciją turite įtraukti automatizuotą registravimo užduotį. Sąskaitos faktūros, susijusios su pirkimo užsakymais (PU), ir sąskaitos faktūros, kuriose yra ne PU įsigijimo kategorija ir nekaupiamų prekių eilučių, gali būti automatiškai pateiktos darbo eigos sistemai. Sąskaitos faktūros, kurios yra įvestos rankiniu būdu, darbo eigos sistemai turi būti pateiktos rankiniu būdu.

Darbo eigos vertė **Pateikė** yra vartotojo ID, įvestas foninei užduočiai **Pateikti tiekėjo sąskaitas faktūras darbo eigai** puslapyje **Proceso automatizavimas**. Jei reikia, vartotojas su šiuo vartotojo ID gali atšaukti sąskaitą faktūrą iš darbo eigos sistemos.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Registruotų gavimo kvitų sugretinimas su sąskaitos faktūros eilutėmis, kurioms taikoma trišalė atitikimo strategija

Vykdant bekontakčio mokėtinų sumų sąskaitos faktūros išrašymo procesą, sistema gali automatiškai sugretinti registruotų produktų gavimo kvitus su sąskaitos faktūros eilutėmis. Šiai užduočiai reikia sukonfigūruoti trišalę atitikimo strategiją. Šią funkciją galima naudoti, jei funkcija **Tiekėjo sąskaitų faktūrų automatizavimas** yra įjungta puslapyje **Funkcijų valdymas**.

Atitikimo procesas bus vykdomas, kol sugretinto produkto gavimo kvito kiekis bus lygus SF kiekiui. Tačiau, jei vienoje SF eilutėje yra keli produkto gavimo kvitai, norint pasiekti visą kiekį, reikės kelis kartus paleisti procesą, kad būtų pasiektas visas kiekis. Šio proceso metu galite nurodyti maksimalų kartų, kai sistema turi bandyti sugretinti produkto gavimo kvitus su SF eilute prieš padarydama išvadą, kad procesas nepavyko, skaičių. Procesas bus vykdomas fone kas valandą arba kas dieną. 

Automatizuotą atitikimo procesą galite vykdyti kaip SF pateikimo darbo eigos sistemai proceso dalį. Taip pat jį galite vykdyti kaip atskirą procesą. Produktų kvitų sugretinimo su sąskaitos faktūros eilutėmis parametrus galima konfigūruoti skirtuke **Tiekėjo sąskaitų faktūrų automatizavimas**, esančiame puslapyje **Mokėtinų sumų parametrai** (**Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**).

Sąskaitos faktūros eilutės, kurioms taikoma trišalė atitikimo strategija, kai sugretintas gautas kiekis yra mažesnis nei sąskaitoje faktūroje nurodytas kiekis, bus įtrauktos į automatizuoto sugretinimo su produkto gavimo kvitu procesą.

Norėdami peržiūrėti **Paskutinis sugretinimas** būseną sąskaitų faktūrų, kurios nėra automatizuoto pateikimo darbo eigai proceso dalis, atidarykite sąskaitą faktūrą puslapyje **Tiekėjo sąskaitos faktūros**. Kai peržiūrite sąskaitą faktūrą, sutampanti patvirtinimo informacija yra atnaujinama. Būsena **Paskutinis sutapimas** gali būti naujinama automatiškai naudojant **Patvirtinimo sąskaitos atitikimo** fono užduotį. Galite konfigūruoti automatinį procesą naujinant **Paskutinio atitikimo** būseną **Fono procesuose** skirtuke **Tvarkyti automatizavimus** puslapyje (**Sistemos administravimas\> Nustatymai\> Tvarkyti automatizavimus**).

Sąskaitos faktūros eilutė bus pašalinta iš automatizuoto vykdymo, jei tenkinama kuri nors iš šių sąlygų:

- Sąskaitos faktūros eilutės **Automatizuoto kvito sugretinimo būsena** vertė yra **Nepavyko**.
- Sąskaita faktūra yra naudojama.
- Sąskaita faktūra yra darbo eigos sistemoje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
