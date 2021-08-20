---
title: Išankstinės SF, skirtos Rytų Europai
description: Išankstinė SF yra dokumentas, kurį galite kurti klientui arba tiekėjui. Ji nurodo pardavimo užsakymo sumą, kurią reikia apmokėti iš anksto. Šioje temoje pateikiama informacija apie išankstines SF, skirtas Rytų Europai.
author: EvgenyPopovMBS
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272643
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 3cf3f9b513c472b9b27f2d6b1b326767704e08da64b7da549c5d10105d8fc407
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763080"
---
# <a name="advance-invoices-for-eastern-europe"></a>Išankstinės SF, skirtos Rytų Europai

[!include [banner](../includes/banner.md)]

Išankstinė SF yra dokumentas, kurį galite kurti klientui arba tiekėjui. Ji nurodo pardavimo užsakymo sumą, kurią reikia apmokėti iš anksto. Šioje temoje pateikiama informacija apie išankstines SF, skirtas Rytų Europai.

Išankstinės SF funkcija suteikia galimybę atlikti tolesnes užduotis.

-   Išduoti išankstines SF klientams ir sekti tų išankstinių SF būseną (**Atvira**, **Iš dalies apmokėta** arba **Uždaryta**).
-   Registruoti išankstinių SF operacijas ir pridėtinės vertės mokesčio (PVM) operacijas (skirta tik Lenkijai).
-   Generuoti mokėjimo žurnalo eilutes automatiškai, atsižvelgiant į išankstinę SF.
-   Susieti išankstinius mokėjimus, gautus iš klientų, su išankstinėmis SF (prieš registruojant išankstinį mokėjimą arba po to).
-   Keisti užregistruotų išankstinių apmokėjimų PVM registravimą (t. y. konvertuoti išankstinį mokėjimą į mokėjimą ar mokėjimą į išankstinį apmokėjimą arba keisti registravimo datą, mokesčio tarifą ar sumą).
-   Kurti PVM apmokestinamo pristatymo mokesčių dokumentą (skirta tik Čekijos Respublikai).

## <a name="advance-invoices-for-poland"></a>Išankstinės SF, skirtos Lenkijai
Išankstinius mokėjimus gaunančios Lenkijos įmonės turi sukurti išankstinių mokėjimų klientui SF. Ši išankstinė SF užregistruojama DK ir ji yra privalomas dokumentas, naudojamas PVM mokesčių tikslais. Išankstinėje SF apskaičiuotas mokestis turi būti pateiktas mokesčių rinkėjui. Įvykdžius galutinį prekių pardavimą, išankstinė SF turėtų būti nurodyta pardavimo SF. Bendra pardavimo suma turi apimti išankstinius mokėjimus. Užregistravus pardavimo SF, sudengta išankstinė SF bus atšaukta. Pradinė išankstinė SF bus sudengta atšaukiant išankstinę SF.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Išankstinių SF gautinų sumų nustatymas
Puslapio **Gautinų sumų parametrai** skirtuke **Naujinimai** nurodykite tolesnius parametrus.


|     FastTab     |             Parametras             |                                                                                                                                                                                           aprašymas                                                                                                                                                                                           |
|-----------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Išankstinė SF |          Registravimo šablonas          | Pasirinkite registravimo šabloną, kurį naudosite išrašydami išankstinės SF (skirta tik Lenkijai). <strong>Svarbu:</strong> Čekijos Respublikoje ir Vengrijoje išankstinės SF nėra laikomos apskaitos arba mokesčių dokumentais ir nėra registruojamos DK. Todėl šiose šalyse šį lauką turite palikti tuščią, kad išankstinės SF nebūtų užregistruotos DK. |
|                 |                                   |                                                                                                                                                                                                                                                                                                                                                                                                 |
| Išankstinė SF |                Išjungta                |                                                                                                                                                                                           sąskaita                                                                                                                                                                                           |
| Išankstinė SF |          PVM grupė          |                                                                                                                                                      Pasirinkite PVM grupę, naudotiną skaičiuojant išankstinių SF PVM.                                                                                                                                                      |
| Išankstinė SF |      Atšaukimas kaip koregavimas       |                                                                                                                                                 Pažymėkite šį žymės langelį, jei išankstinės SF atšaukimas turi būti laikomas koregavimu.                                                                                                                                                  |
| Išankstinė SF |      Atšaukti datą      |                                                                                                                                                     Pažymėkite šį žymės langelį, norėdami išankstinį mokėjimą atšaukti SF registravimo dieną.                                                                                                                                                     |
|     Mokėjimas     |     Kelios išankstinio apmokėjimo datos     |                                                                                                                                        Pasirinkite vieną iš šių parinkčių: <strong>Priimti</strong>, <strong>Įspėjimas</strong> arba <strong>Klaida</strong>.                                                                                                                                         |
|     Mokėjimas     |           Datos nesutapimas           |                                                                                                                                        Pasirinkite vieną iš šių parinkčių: <strong>Priimti</strong>, <strong>Įspėjimas</strong> arba <strong>Klaida</strong>.                                                                                                                                         |
|     Mokėjimas     |          Sumos nesutapimas          |                                                                                                                                        Pasirinkite vieną iš šių parinkčių: <strong>Priimti</strong>, <strong>Įspėjimas</strong> arba <strong>Klaida</strong>.                                                                                                                                         |
|     Mokėjimas     | Susiejimas su užregistruota išankstine SF |                                                                                                                                        Pasirinkite vieną iš šių parinkčių: <strong>Priimti</strong>, <strong>Įspėjimas</strong> arba <strong>Klaida</strong>.                                                                                                                                         |
|     Mokėjimas     | (CZE), (POL) Išankstinio mokėjimo tvarkymas  |                                                                                                                                                                                Pasirinkite <strong>Išankstinis</strong>.                                                                                                                                                                                |

Skirtuke **Numeracijos** nustatykite tolesnių nuorodų numeracijas.

-   Mokesčio dokumentas
-   Mokesčių kredito pažyma
-   Išankstinė SF
-   Išankstinės SF kredito pažyma
-   Išankstinės SF atšaukimas
-   Išankstinės SF kvitas
-   Išankstinės SF kredito pažymos kvitas
-   Išankstinės SF atšaukimo kvitas

## <a name="create-a-customer-advance-invoice"></a>Kliento išankstinės SF kūrimas
Spustelėkite **Gautinos sumos** &gt; **Bendra** &gt; **Išankstinės SF** &gt; **Visos išankstinės SF**. Norėdami kurti naują išankstinę SF, veiksmų srities skirtuke **Išankstinė SF** spustelėkite **Išankstinė SF**. Įveskite reikiamą informaciją ir tada spustelėkite **Registruoti**, norėdami registruoti išankstinę SF. Išankstinės SF būsena gali būti tokia: **Atvira**, **Iš dalies apmokėta** arba **Uždaryta**. Galite neautomatiniu būdu keisti užregistruotos išankstinės SF būseną. Spustelėkite **Būsena** ir tada puslapio **Išankstinės SF būsenos keitimas** lauke **Nauja būsena** pasirinkite naują išankstinės SF būseną. **Pastaba:** išankstinės SF būseną galite keisti bet kada. Negalima apdoroti uždarytų išankstinių SF operacijose. **Pastaba:** Lenkijoje išankstinių SF operacijos generuojamos, jei nustatote išankstinių SF registravimo šabloną puslapyje Gautinų sumų parametrai. Norėdami peržiūrėti užregistruotas operacijas, puslapyje **Išankstinės SF** spustelėkite **Kvitas**.

## <a name="vat-on-advance-invoices"></a>Išankstinių SF PVM
Įmonės turi įrašyti klientų išankstinių mokėjimų PVM, net jei pardavimas nebuvo baigtas. Norėdami registruoti išankstinio mokėjimo PVM, į išankstinę SF galite įtraukti eilutę, kurioje yra PVM specifikacija. Išankstinės SF gali turėti kelias eilutes, o eilutėse gali būti PVM specifikacijos, paimtos iš pardavimo užsakymo eilučių. Todėl išankstinio mokėjimo PVM galite registruoti tik pagal pardavimo užsakymo eilutes. **Pastaba:** PVM specifikacijos kopijuojamos į išankstinės SF eilutes tik tada, kai puslapio **Mokesčio tipas** laukas **PVM kodai** nustatytas į parinktį **Standartinis PVM** arba **Sumažintas PVM**. Kitu atveju eilutė kopijuojama į išankstinę SF taip, lyg PVM suma būtų 0 (nulis).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Išankstinės SF susiejimas su pardavimo užsakymu arba laisvos formos SF
Kiekvieną išankstinę SF vienu metu galima susieti tik su vienu pardavimo užsakymu arba laisvos formos SF. Esamą išankstinę SF galite perskirti kitam pardavimo užsakymui arba laisvos formos SF, jei su išankstine SF nesusieta jokių išankstinių mokėjimų. Norėdami išankstinę SF susieti su pardavimo užsakymu, puslapyje **Visos išankstinės SF** pasirinkite išankstinę SF. Veiksmų srityje spustelėkite **Išankstinės SF**, tada spustelėkite **Pardavimo užsakymas**. Tada pasirinkite pardavimo užsakymą, su kuriuo norite susieti išankstinę SF, ir spustelėkite **Gerai**. Norėdami išankstinę SF susieti su laisvos formos SF, puslapyje **Visos išankstinės SF** pasirinkite išankstinę SF. Veiksmų srityje spustelėkite **Išankstinės SF**, tada spustelėkite **Laisvos formos SF**. Tada pasirinkite laisvos formos SF, su kuria norite susieti išankstinę SF, ir spustelėkite **Gerai**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Kliento išankstinės SF kūrimas iš pardavimo užsakymo
Sukurkite pardavimo užsakymą arba pasirinkite esamą. Spustelėkite **SF**, o tada spustelėkite **Generuoti** &gt; **Išankstinė SF**. Puslapyje **Išankstinės SF kūrimas** nustatykite tolesnius laukus.

| Laukas                                           | aprašymas                                                                                                                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procentas                                         | Nurodykite pardavimo užsakymo išankstinio mokėjimo procentą.                                                                                                                                                                             |
| Korespondentinė sąskaita                                  | Pasirinkti numatytąją korespondentinę sąskaitą, naudotiną išrašant išankstines SF.                                                                                                                                                                         |
| Užsakymo naujinimas                                    | Pasirinkite vieną iš šių pasirinkčių: **Visi**, **Pristatyti dabar**, **Paimta**, **Važtaraštis** arba **Paimtas kiekis ir atsargose nelaikomi produktai**. Išankstinės SF suma bus apskaičiuota pagal prekių pardavimo užsakymo sumas. |
| Registruoti PVM                                        | Nurodykite, ar PVM turi būti registruojamas išankstinės SF registravimo metu.                                                                                                                                                                      |
| PVM registravimo data                                   | Nurodykite PVM registravimo datą.                                                                                                                                                                                                         |
| Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu | Nurodykite išankstinio mokėjimo registravimo šabloną.                                                                                                                                                                                           |
| Kurti mokesčio dokumentą                             | Nurodykite, ar turi būti sukurtas mokesčių dokumentas.                                                                                                                                                                                         |

> [!PASTABA} Lenkijoje išankstinių SF operacijos generuojamos, jei nustatote išankstinių SF registravimo šabloną puslapyje Gautinų sumų parametrai.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Kliento išankstinės SF kūrimas naudojant laisvos formos SF
Sukurkite laisvos formos SF arba pasirinkite esamą laisvos formos SF. Skirtuko **SF** dalyje **Nauja** spustelėkite **Išankstinė SF**. Tada galite sukurti naują išankstinę SF, kuri bus susieta su laisvos formos SF. **Pastaba:** Lenkijoje išankstinių SF operacijos generuojamos, jei nustatote išankstinių SF registravimo šabloną puslapyje Gautinų sumų parametrai.

## <a name="print-an-advance-invoice"></a>Išankstinės SF spausdinimas
Norėdami spausdinti išankstinę SF, puslapyje **Išankstinė SF** spustelėkite **Spausdinti**. Lenkijoje galima spausdinti finansinio dokumento išankstinės SF dokumentą. Pasirinkite parinktį išankstinės SF registravimo metu. Lenkijoje pardavimo SF ir laisvos formos SF dokumentų maketas turėtų apimti toliau nurodytą informaciją apie sudengiamą išankstinę SF.

-   Išankstinės SF numeris
-   Išankstinės SF data
-   Suma be PVM, PVM suma, suma su PVM ir valiuta
-   Mokesčio procentas

PVM sumų suvestinėje turėtų būti **Išankstinės SF mokestis**. Apmokėtiną sumą turėtų sumažinti išankstinės SF suma.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Mokėjimo pasiūlymo kūrimas naudojant išankstinę SF
Generuoti mokėjimo žurnalo eilutes galima automatiškai, atsižvelgiant į išankstinę SF. Kai kuriate naują mokėjimų žurnalą, puslapyje **Mokėjimų žurnalas** pasirinkite parinktį **Išankstinio mokėjimo žurnalo kvitas** ir spustelėkite **Eilutės**. Puslapyje **Žurnalo kvitas** galite spustelėti **Mokėjimo pasiūlymas** &gt; **Mokėjimo pasiūlymas naudojant išankstinę SF**, kad sukurtumėte mokėjimo pasiūlymą naudodami išankstines SF. Iš išankstinės SF paimama informacija, pvz., registravimo šablonas ir PVM grupės. **Pastaba:** nauji išankstiniai mokėjimai bus automatiškai susieti su išankstinėmis SF, jei puslapyje **Kurti išankstinio mokėjimo pasiūlymą naudojant išankstines SF** pasirinktos parinktys **Susieti išankstinius mokėjimus** ir **Keisti būseną**.

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Išankstinio mokėjimo susiejimas su išankstine SF
Jei norite išankstinį mokėjimą susieti su išankstine SF naudodami mokėjimų žurnalą, atidarykite mokėjimų žurnalą, pasirinkite eilutę, kurioje yra išankstinis mokėjimas, o tada spustelėkite **Funkcijos** &gt; **Susieti su išankstinėmis SF**. Jei norite išankstinį mokėjimą susieti su išankstine SF naudodami puslapį **Kliento operacijos**, spustelėkite **Visi klientai** &gt; **Klientas** &gt; **Operacijos**. Pasirinkite mokėjimų žurnalą, pasirinkite eilutę, kurioje yra išankstinis mokėjimas, o tada spustelėkite **Funkcijos** &gt; **Susieti su išankstinėmis SF**.

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Išankstinės SF susiejimas su išankstiniu mokėjimu
Norėdami išankstinę SF susieti su išankstinio mokėjimo eilute, puslapyje **Visos išankstinės SF** pasirinkite išankstinę SF. Veiksmų srityje spustelėkite **Išankstinės SF**, tada spustelėkite **Išankstinis mokėjimas**. Tada pasirinkite išankstinio mokėjimo eilutę, su kuria norite susieti išankstinę SF, ir spustelėkite **Gerai**.

## <a name="advance-invoice-credit-note"></a>Išankstinės SF kredito pažyma
-   (POL) Norėdami atšaukti išankstinę SF, galite kurti išankstinės SF kredito pažymą ir užregistruoti ją DK.
-   Norėdami kurti kredito pažymą, galite kurti naują išankstinę SF ir tada spustelėti **Kredito pažyma**. Tada galite pasirinkti atšauktiną išankstinę SF.
-   Taip pat galima kurti pardavimo SF, kurioje pateikiamas išankstinės SF sudengimas, kredito pažymą.
-   Išankstinės SF kredito pažymos SF makete pateikiama informacija apie eilutes prieš ir po koregavimo.
-   (POL) DK operacijos kuriamos užregistravus išankstinės SF kredito pažymą.

## <a name="cze-tax-documents"></a>(CZE) Mokesčių dokumentai
Čekijos Respublikoje galite kurti mokesčių dokumentą, pagrįstą PVM apmokestinamo pristatymo išankstinio mokėjimo informacija. Galite kurti, kurti ir rodyti arba kurti ir spausdinti mokesčių dokumentą naudodami išankstinių mokėjimų puslapį. Spustelėkite **Funkcijos** &gt; **Mokesčių dokumentas** ir pažymėkite vieną iš parinkčių. Mokesčių dokumente pateikiama išsami informacija apie PVM, pvz., PVM tipas, vertė ir pagrindinė suma apskaitos valiuta bei operacijos valiuta.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Išankstinių SF mokėtinų sumų nustatymas
Puslapio **Mokėtinų sumų parametrai** skirtuke **Numeracijos** nurodykite išankstinių SF numeraciją.

## <a name="create-a-vendor-advance-invoice"></a>Tiekėjo išankstinės SF kūrimas
Galite neautomatiniu būdu kurti išankstinę SF. Be to, nauja išankstinė SF gali būti pagrįsta esamu pirkimo užsakymu.

## <a name="manually-create-a-vendor-advance-invoice"></a>Tiekėjo išankstinės SF neautomatinis kūrimas
Spustelėkite **Mokėtinos sumos** &gt; **Bendra** &gt; **Išankstinės SF** &gt; **Visos išankstinės SF**. Norėdami kurti naują išankstinę SF, veiksmų srities skirtuke **Išankstinė SF** spustelėkite **Išankstinė SF**. Tada įveskite reikiamą informaciją ir spustelėkite **Registruoti**, norėdami registruoti išankstinę SF. Išankstinės SF būsena gali būti tokia: **Atvira**, **Iš dalies apmokėta** arba **Uždaryta**. Galite neautomatiniu būdu keisti užregistruotos išankstinės SF būseną. Spustelėkite **Būsena** ir tada puslapio **Išankstinės SF būsenos keitimas** lauke **Nauja būsena** pasirinkite naują išankstinės SF būseną. **Pastaba:** išankstinės SF būseną galite keisti bet kada. Negalima apdoroti uždarytų išankstinių SF operacijose. **Pastaba:** PVM specifikacijos kopijuojamos į išankstinės SF eilutes tik tada, kai puslapio **Mokesčio tipas** laukas **PVM kodai** nustatytas į parinktį **Standartinis PVM** arba **Sumažintas PVM**. Kitu atveju eilutė kopijuojama į išankstinę SF taip, lyg PVM suma būtų 0 (nulis).

## <a name="link-an-advance-invoice-to-a-purchase-order"></a>Išankstinės SF susiejimas su pirkimo užsakymu
Kiekvieną išankstinę SF vienu metu galima susieti tik su vienu pirkimo užsakymu. Esamą išankstinę SF galite perskirti kitam pirkimo užsakymui, jei su išankstine SF nesusieta jokių išankstinių mokėjimų. Norėdami išankstinę SF susieti su pirkimo užsakymu, puslapyje **Visos išankstinės SF** pasirinkite išankstinę SF. Veiksmų srityje spustelėkite **Išankstinės SF**, tada spustelėkite **Pirkimo užsakymas**. Tada pasirinkite pirkimo užsakymą, su kuriuo norite susieti išankstinę SF, ir spustelėkite **Gerai**.

## <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Tiekėjo išankstinės SF kūrimas naudojant pirkimo užsakymą
Sukurkite pirkimo užsakymą arba pasirinkite esamą. Spustelėkite **SF**, o tada spustelėkite **Generuoti** &gt; **Išankstinė SF**. Puslapyje **Išankstinės SF kūrimas** nustatykite tolesnius laukus.

| Laukas                                           | aprašymas                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Procentas                                         | Nurodykite pirkimo užsakymo išankstinio mokėjimo procentą.                                                         |
| Atnaujinti pirkimą                                 | Galite pasirinkti iš tolesnių pasirinkčių. Išankstinės SF suma bus apskaičiuota pagal prekių pirkimo užsakymo sumą. |
| Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu | Nurodykite išankstinio mokėjimo registravimo šabloną.                                                                          |








[!INCLUDE[footer-include](../../includes/footer-banner.md)]