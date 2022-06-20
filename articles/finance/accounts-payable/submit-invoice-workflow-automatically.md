---
title: Sąskaitų faktūrų pateikimas darbo eigos sistemai ir produkto gavimo kvito eilučių sugretinimas
description: Šiame straipsnyje paaiškinamas tiekėjo SF pateikimo darbo eigos sistemai procesas ir automatiškai gretinimas su užregistruotomis gavimo dokumentų eilutėmis tiekėjo SF.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 960a08eb5e98cac034bbd41335b616ff41bf6fd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861624"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Sąskaitų faktūrų pateikimas darbo eigos sistemai ir produkto gavimo kvito eilučių sugretinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinamas tiekėjo SF pateikimo darbo eigos sistemai procesas ir automatiškai gretinimas su užregistruotomis gavimo dokumentų eilutėmis tiekėjo SF.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Importuotų tiekėjo sąskaitų faktūrų pateikimas į darbo eigos sistemą ir užregistruotų produktų gavimo kvitų eilučių sugretinimas su patvirtinimo laukiančiomis tiekėjo sąskaitos faktūros eilutėmis

Kaip nenaudingo mokėtinų sumų SF išrašymo proceso dalis, importuota SF gali būti automatiškai pateikta darbo eigos sistemai. Importuotų sąskaitų faktūrų pateikimą į darbo eigos sistemą galite konfigūruoti skirtuke **Tiekėjo sąskaitų faktūrų automatizavimas**, esančiame puslapyje **Mokėtinų sumų parametrai** (**Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**). Pateikimo į darbo eigą procesas bus vykdomas fone jūsų nurodytu dažnumu (kas valandą arba kas dieną).

Kai sąskaitas faktūras į darbo eigos sistemą pateikiate automatiškai, turite pradėti nuo importuotos sąskaitos faktūros. Norint užtikrinti, kad sąskaita faktūra galėtų būti apdorota nuo pradžios iki pabaigos be rankiniu būdu atliekamų veiksmų, į darbo eigos konfigūraciją turite įtraukti automatizuotą registravimo užduotį. Sąskaitos faktūros, susijusios su pirkimo užsakymais (PU), ir sąskaitos faktūros, kuriose yra ne PU įsigijimo kategorija ir nekaupiamų prekių eilučių, gali būti automatiškai pateiktos darbo eigos sistemai. Sąskaitos faktūros, kurios yra įvestos rankiniu būdu, darbo eigos sistemai turi būti pateiktos rankiniu būdu.

Darbo eigos vertė **Pateikė** yra vartotojo ID, įvestas foninei užduočiai **Pateikti tiekėjo sąskaitas faktūras darbo eigai** puslapyje **Proceso automatizavimas**. Jei reikia, vartotojas su šiuo vartotojo ID gali atšaukti sąskaitą faktūrą iš darbo eigos sistemos.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Registruotų gavimo kvitų sugretinimas su sąskaitos faktūros eilutėmis, kurioms taikoma trišalė atitikimo strategija

Kaip neskiriamos mokėtinų sumų SF išrašymo proceso dalis, užregistruoti produkto gavimo kvitai gali būti automatiškai sugretinti su SF eilutėmis. Šiai užduočiai reikia sukonfigūruoti trišalę atitikimo strategiją. Šią funkciją galima naudoti, jei funkcija **Tiekėjo sąskaitų faktūrų automatizavimas** yra įjungta puslapyje **Funkcijų valdymas**.

Atitikimo procesas bus vykdomas, kol sugretinto produkto gavimo kvito kiekis bus lygus SF kiekiui. Tačiau, jei vienoje SF eilutėje yra keli produkto gavimo kvitai, norint pasiekti visą kiekį, reikės kelis kartus paleisti procesą, kad būtų pasiektas visas kiekis. Šio proceso metu galite nurodyti maksimalų kartų, kai sistema turi bandyti sugretinti produkto gavimo kvitus su SF eilute prieš padarydama išvadą, kad procesas nepavyko, skaičių. Procesas bus vykdomas fone kas valandą arba kas dieną. 

Automatizuotą atitikimo procesą galite vykdyti kaip SF pateikimo darbo eigos sistemai proceso dalį. Taip pat galite paleisti jį kaip atskirą procesą. Produktų kvitų sugretinimo su sąskaitos faktūros eilutėmis parametrus galima konfigūruoti skirtuke **Tiekėjo sąskaitų faktūrų automatizavimas**, esančiame puslapyje **Mokėtinų sumų parametrai** (**Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**).

Sąskaitos faktūros eilutės, kurioms taikoma trišalė atitikimo strategija, kai sugretintas gautas kiekis yra mažesnis nei sąskaitoje faktūroje nurodytas kiekis, bus įtrauktos į automatizuoto sugretinimo su produkto gavimo kvitu procesą.

Norėdami peržiūrėti **Paskutinis sugretinimas** būseną sąskaitų faktūrų, kurios nėra automatizuoto pateikimo darbo eigai proceso dalis, atidarykite sąskaitą faktūrą puslapyje **Tiekėjo sąskaitos faktūros**. Kai peržiūrite sąskaitą faktūrą, sutampanti patvirtinimo informacija yra atnaujinama. Būsena **Paskutinis sutapimas** gali būti naujinama automatiškai naudojant **Patvirtinimo sąskaitos atitikimo** fono užduotį. Galite konfigūruoti automatinį procesą naujinant **Paskutinio atitikimo** būseną **Fono procesuose** skirtuke **Tvarkyti automatizavimus** puslapyje (**Sistemos administravimas\> Nustatymai\> Tvarkyti automatizavimus**).

Sąskaitos faktūros eilutė bus pašalinta iš automatizuoto vykdymo, jei tenkinama kuri nors iš šių sąlygų:

- Sąskaitos faktūros eilutės **Automatizuoto kvito sugretinimo būsena** vertė yra **Nepavyko**.
- Sąskaita faktūra yra naudojama.
- Sąskaita faktūra yra darbo eigos sistemoje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
