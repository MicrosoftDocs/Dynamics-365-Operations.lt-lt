---
title: Taisyti planavimo modulio klaidą "Nepakanka pajėgumo" ir riboto pajėgumo
description: Šiame straipsnyje pateikiama informacija apie gamybos užsakymo priežastis ir nutarimus, kurių %1 nepavyko suplanuoti. Išspręskite planavimo mechanizmo klaidą „Nepavyko rasti pakankamai pajėgumo“.
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135606"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Išspręskite planavimo mechanizmo klaidą „Nepavyko rasti pakankamai pajėgumo“

[!include [banner](../includes/banner.md)]

Kai bandote įgalinti schemas, galite gauti tokį klaidos pranešimą:

> Gamybos užsakymo %1 planuoti negalima. Rasta nepakankamai pajėgumų.

Yra kelios priežastys, dėl kurių planavimo variklis gali neį nepavykti ir šis klaidos pranešimas. Šiame straipsnyje pateikiamos gairės, kurios padės rasti šakninį klaidos priežastį ir tada ją sumažins.

## <a name="review-the-applicable-resources"></a>Peržiūrėti taikytinus išteklius

Klaida gali įvykti, jei jokie taikomi ištekliai neatitinka operacijos reikalavimų gamybos užsakymo vietoje.

Norėdami peržiūrėti skaičiavimo rezultatus, atlikite tokius veiksmus.

1. Pasirinkite **Gamybos kontrolės \> gamybos užsakymus \> Visi gamybos užsakymai**, ir atidarykite arba pasirinkite gamybos užsakymą, kurį negalima suplanuoti.
1. Veiksmų juostoje, **Gamybos užsakymas** skirtuke, **Gamybos išsami informacija** grupėje pasirinkite **Maršrutas**.
1. Puslapyje **Gamybos maršrutas** pasirinkite operaciją, tada veiksmų srityje pasirinkite **Taikomi ištekliai**.
1. Dialogo lange **Taikomi ištekliai** nustatykite **Naudojimo reikalavimus** kaip *Operacijų planavimas* arba *Užduočių planavimas*, atsižvelgiant į planavimo tipą, kurį naudojate.
1. Įsitikinkite, kad yra taikomi ištekliai gamybos užsakymo vietoje.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Peržiūrėkite su kalendorius susietus su ištekliais.

Klaida gali įvykti, jei su ištekliais ar išteklių grupe nėra susieto kalendoriaus arba jei netinkamai nustatytas susijęs kalendorius (pvz., jis neturi darbo laiko arba jo efektyvumas procentais yra 0 \[nulis\]).

Norėdami patikrinti, ar kalendorius yra susietas su ištekliais arba išteklių grupe, atlikite šiuos veiksmus.

1. Pasirinkite **Gamybos kontrolės \> gamybos užsakymus \> Visi gamybos užsakymai**, ir atidarykite arba pasirinkite gamybos užsakymą, kurį negalima suplanuoti.
1. Veiksmų juostoje, **Gamybos užsakymas** skirtuke, **Gamybos išsami informacija** grupėje pasirinkite **Maršrutas**.
1. Puslapyje **Gamybos maršrutas** pasirinkite operaciją, tada veiksmų srityje pasirinkite **Taikomi ištekliai**.
1. Dialogo lange **Taikomi ištekliai** pasirinkite išteklius, tada pasirinkite **Peržiūrėti išteklius**. Arba pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) **Išteklių grupės** lauke ir pasirinkite **Peržiūrėti informaciją**.
1. Puslapyje **Ištekliai** ar **išteklių grupių** puslapyje, „FastTab“ **Kalendoriai** įsitikinkite, kad kalendorius susietas su ištekliais arba išteklių grupe.

> [!NOTE]
> Jei planuojant operaciją įvyksta klaida, turite įsitikinti, kad kalendorius susietas su visomis taikytinomis išteklių grupėmis.

Norėdami peržiūrėti kalendoriaus nustatymus, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimo \> nustatymo \> kalendorius \> kalendorius** ir pasirinkite kalendorių, kuris susietas su ištekliais ar išteklių grupe.
1. Veiksmų srityje pasirinkite **Darbo laikai**.
1. Darbo **laiko puslapyje** įsitikinkite, kad puslapis nėra tuščias. Be to, norėdami sužinoti, kiek dienų norėtumėte, įsitikinkite, kad laukas **Valdiklis** nėra nustatytas kaip *Uždaryta*, ra darbo laikas, o laukas **Efektyvumas yra procentas** laukas nėra nustatytas į *0* (nulį).

Jei kalendorius susietas su baziniu kalendoriumi, turite peržiūrėti pagrindinio kalendoriaus nustatymą.

> [!NOTE]
> Operacijos planavimo metu išteklių grupės kalendorius naudojamas nustatyti kiekvienos operacijos pradžios ir pabaigos laikus. Taip pat apribojama, kiek laiko sistema gali planuoti vienai konkrečiai operacijai per vieną konkrečią dieną vienoje konkretausje išteklių grupėje. Pavyzdžiui, jei išteklių grupės darbo laikas konkrečią dieną yra nuo 8:00 iki 4:00, krovinys, kurį viena operacija įkelia į išteklių grupę, negali viršyti krovinio, kuris gali sutapti su aštuoniomis valandomis, nepaisant galimų pajėgumų, kurį išteklių grupė turi tą dieną, kiekio. Nepaisant to, prieinamas pajėgumas gali dar labiau apriboti apkrovą.

## <a name="review-the-scheduling-parameters"></a>Peržiūrėti tvarkaraščių parametrus

Siekiant užtikrinti tinkamą našumą, planavimo modulis ieško išteklių tik tam tikrą laiką ir konkretų planavimo nesuderinamumų skaičių.

Norėdami peržiūrėti parametrų tvarkaraščius, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas \> Sąranka \> Tvarkaraščių parametrai**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei įgalinta **planavimo skirtasis** laikas, nustatyta parinktis *Ne*, pereikite į 3 veiksmą.
    - Jei **planavimo skirtasis laikas** parinktis nustatyta į *Taip*, padidinkite **Maksimalus planavimo laikas vertę pagal seką** kad apdorojimui būtų daugiau laiko, kuris turi būti baigtas.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei įgalinta **planavimo optimizavimo skirtasis** laikas, nustatyta parinktis *Ne*, pereikite į 4 veiksmą.
    - Jei **planavimo optimizavimo skirtasis laikas** parinktis nustatyta į *Taip*, padidinkite **Optimizavimo bandymo skirtasis laikas** kad apdorojimui būtų daugiau laiko, kuris turi būti baigtas.

1. Jei pakeitėte kurį nors puslapio parametrą, perplanuoti užsakymą, kad būtų mėginta dar kartą.

## <a name="review-capacity"></a>Peržiūrėti pajėgumą

Klaida gali įvykti, kai atliekate ribotas planavimą, bet pajėgumo nėra.

Norėdami atlikti neribotą pajėgumo planavimą, atlikite šiuos veiksmus.

1. Pasirinkite **Gamybos kontrolės \> gamybos užsakymus \> Visi gamybos užsakymai**, ir rinkitės ar atidarykite arba pasirinkite gamybos užsakymą, kurį negalima suplanuoti.
1. Veiksmų srities skirtuko Grafikas **gamybos** užsakymų **grupėje pasirinkite** rinkitės **Planavimo operacijos** ar **Planuoti užduotis**.
1. Dialogo **lange Operacijų** planavimas arba **Užduočių planavimas** nustatykite parinktį **Ribotas pajėgumas** kaip *Ne*.
1. Norėdami suplanuoti paketinę užsakymą pasirinkite **Gerai**.

Norėdami peržiūrėti galimų išteklių pajėgumą, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimo \> išteklių \> išteklius**, ir pasirinkite išteklių, kurie taikomi užsakymui, kuris negali būti suplanuotas.
1. Veiksmų srities skirtuke Ištekliai, **grupėje** Rodinys, **·** **pasirinkite Pajėgumas arba Pajėgumas,** grafiniu formatu ir įsitikinkite, kad yra turimas pajėgumas.**·**

Norėdami peržiūrėti galimų išteklių grupę, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimo \> išteklių \> Išteklių grupė**, ir pasirinkite išteklių grupę, kurie taikomi užsakymui, kuris negali būti suplanuotas.
1. Veiksmų srities skirtuko **Išteklių** **·** **·** **grupė grupėje Peržiūrėti pasirinkite Pajėgumas arba Pajėgumas, grafiniu formatu ir įsitikinkite,** kad yra turimas pajėgumas.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Bendrojo planavimo knygos yra ištekliai uždarius išteklių kalendorių

Planuojant operacijas, bendrasis planavimas suplanuos pajėgumus pagal pirminės išteklių grupės kalendorių. Ji rezervuos antrinę operaciją tuo pačiu metu kaip ir pirminė operacija, ir neatims jokių antrinės operacijos kalendorių ar pajėgumo. Tai gali baigti gamybos užsakymo grafiką uždarytame kalendoriuje arba tuo metu, kai negalima naudoti antrinės operacijos (kalendorius uždarytas, pajėgumas nėra pajėgumo).

Planuojant užduotis, bendrojo planavimo metu planuojant užsakymą bus atsižvelgiama į pirminės ir antrinės operacijų pajėgumą ir kalendorių. Norint suplanuoti užsakymą, abiejų operacijų išteklių kalendoriai turi būti atviri ir turėti atvirą pajėgumą.

## <a name="maximum-job-lead-time-is-too-short"></a>Maksimalus užduoties gamybos laikas yra per trumpas

Planavimo variklis **negalės** planuoti užsakymo, jei nustatytas maksimalus jūsų svetainės užduoties gamybos laikas yra trumpesnis už prekės gamybos laiką, nurodytą jos numatytuose užsakymo parametruose arba padengimo parametruose.

Norėdami peržiūrėti arba redaguoti svetainės **maksimalaus užduoties vykdymo** laiko parametrą, eikite į Gamybos **kontrolės \>\> nustatymo gamybos kontrolės parametrus** ir atidarykite skirtuką **Bendra**.

Norėdami peržiūrėti arba redaguoti numatytuosius prekės užsakymo parametrus, atlikite šiuos veiksmus:

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Raskite ir pasirinkite reikiamą produktą iš sąrašo.
1. Veiksmų srityje atidarykite skirtuką Valdyti **atsargas ir** pasirinkite Numatytuosius **užsakymo parametrus**.
1. Išplėskite **atsargų "** FastTab" ir peržiūrėkite ar redaguokite **atsargų vykdymo laiko** parametrą, kaip reikia.

Norėdami peržiūrėti arba redaguoti prekės padengimo parametrus, atlikite šiuos veiksmus:

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Raskite ir pasirinkite reikiamą produktą iš sąrašo.
1. Veiksmų srityje atidarykite skirtuką Planas **ir pasirinkite Prekės** padengimas **·**.
1. Atidarykite **skirtuką Gamybos** laikas ir peržiūrėkite arba redaguokite **gamybos laiko** vertę.

## <a name="excessive-quantity-of-required-resources"></a>Perviršinis reikalingų išteklių kiekis

Planuojant, modulis bando suderinti reikiamą maršruto operacijos išteklių kiekį su taikomais ištekliais pagal operacijos išteklių reikalavimus. Nustačius per aukštą išteklių kiekį, maršrutas gali būti neįmanomas, todėl bus įvyko planavimo klaida.

Norėdami patikrinti pasirinkto produkto, maršruto ir maršruto operacijos nurodytą kiekį ir taikomus išteklius, naudokite šią procedūrą:

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Rasti ir pasirinkti atitinkamą produktą tinklelyje.
1. Veiksmų srityje atidarykite skirtuką Inžinierius **ir** pasirinkite **Maršrutas**.
1. Rasti ir pasirinkti reikiamą maršrutą tinklelyje.
1. Atidarykite **skirtuko** Peržiūra puslapio apačioje.
1. Pasirinkti operaciją iš pasirinktų maršruto operacijų sąrašo.
1. Pasirinkite **taikytinus** išteklius, kad atidarytumėte dialogo langą, kuriame galite peržiūrėti pasirinktos maršruto operacijos taikomus išteklius.
1. Atidarykite skirtuką **Išteklių apkrova** . Lauke **Kiekis** rodomas ištekliaus kiekis, kurio reikia norint atlikti pasirinktą maršruto operaciją. Peržiūrėkite ir (arba) redaguokite pagal poreikį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
