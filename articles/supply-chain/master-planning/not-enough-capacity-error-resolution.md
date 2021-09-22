---
title: Išspręskite planavimo mechanizmo klaidą „Nepavyko rasti pakankamai pajėgumo“
description: Šioje temoje pateikiama informacija apie gamybos užsakymo priežastis ir nutarimus, kurių %1 nepavyko suplanuoti. Išspręskite planavimo mechanizmo klaidą „Nepavyko rasti pakankamai pajėgumo“.
author: crytt
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 37c990067a0c175d93ecf298866041f4d2afc1bc
ms.sourcegitcommit: ab1455c67f6ee6ca36bec148bea0dbb0f7704eda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/26/2021
ms.locfileid: "7428948"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Išspręskite planavimo mechanizmo klaidą „Nepavyko rasti pakankamai pajėgumo“

[!include [banner](../includes/banner.md)]

Kai bandote įgalinti schemas, galite gauti tokį klaidos pranešimą:

> Gamybos užsakymo %1 planuoti negalima. Rasta nepakankamai pajėgumų.

Yra kelios priežastys, dėl kurių planavimo variklis gali neį nepavykti ir šis klaidos pranešimas. Šioje temoje pateikiamos gairės, kurios padės rasti šakninį klaidos priežastį ir ją sumažinti.

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

Klaida gali įvykti, kai atliekate ribotas planavimą, tačiau pajėgumo nėra.

Norėdami atlikti neribotą pajėgumo planavimą, atlikite šiuos veiksmus.

1. Pasirinkite **Gamybos kontrolės \> gamybos užsakymus \> Visi gamybos užsakymai**, ir rinkitės ar atidarykite arba pasirinkite gamybos užsakymą, kurį negalima suplanuoti.
1. Veiksmų srities skirtuko Grafikas **gamybos** užsakymų **grupėje pasirinkite** rinkitės **Planavimo operacijos** ar **Planuoti užduotis**.
1. Dialogo **lange Operacijų** planavimas arba **Užduočių planavimas** nustatykite parinktį **Ribotas pajėgumas** kaip *Ne*.
1. Norėdami suplanuoti paketinę užsakymą pasirinkite **Gerai**.

Norėdami peržiūrėti galimų išteklių pajėgumą, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimo \> išteklių \> išteklius**, ir pasirinkite išteklių, kurie taikomi užsakymui, kuris negali būti suplanuotas.
1. Veiksmų srities skirtuke Ištekliai, grupėje **Peržiūra** rinkitės **Peržiūros** grupę ir tada **Pajėgumas** ar **Pajėgumas grafiškai** ir įsitikinkite, kad pajėgumo užtektų.

Norėdami peržiūrėti galimų išteklių grupę, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimo \> išteklių \> Išteklių grupė**, ir pasirinkite išteklių grupę, kurie taikomi užsakymui, kuris negali būti suplanuotas.
1. Veiksmų srities skirtuke Ištekliai, grupėje **Išteklių grupė** rinkitės **Peržiūros** grupę ir tada **Pajėgumas** ar **Pajėgumas grafiškai** ir įsitikinkite, kad pajėgumo užtektų.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
