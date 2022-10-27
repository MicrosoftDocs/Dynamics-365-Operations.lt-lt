---
title: Riboti mokėjimo atpažinimo ženklo naudojimą
description: Šiame straipsnyje aprašoma funkcija, pagal kurią ribojami mokėjimo atpažinimo ženklų naudojami apribojimai Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709376"
---
# <a name="limit-payment-token-usage"></a>Riboti mokėjimo atpažinimo ženklo naudojimą

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šiame straipsnyje aprašoma funkcija, pagal kurią ribojami mokėjimo atpažinimo ženklų naudojami apribojimai Microsoft Dynamics 365 Commerce. Atpažinimo ženklo naudojimas apribotas iki pardavimo užsakymo apimties arba, jei leidžiamas kliento sutikimas, saugomas kaip kortelė faile.

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | Aprašymas |
|---|---|
| Atpažinimo ženklas | Nuoroda į XML BLOB "Dynamics 365" sistemoje, kurioje saugomos mokėjimo nuorodos operacijų tikslais. |
| Kortelė faile | Įrašytas kortelės nuorodos atpažinimo ženklas, dėl kurio sutarta, kad ji bus naudojama "Dynamics 365" sistemoje arba mokėjimo šliuze ir kuris yra konkretus kliento sąskaitai. |

Mokėjimo atpažinimo ženklo naudojimo ribos taikomos bet kuriai aplinkai, kuri naudoja mokėjimo šliuzo paslaugą, kurioje naudojami pasikartojantys atpažinimo ženklas. Programos " [Dynamics 365" mokėjimo jungtis, skirta "Adyen](adyen-connector.md) ", naudoja pasikartojančių mokėjimų atpažinimo ženklus vėlesniems užsakymo veiksmams, pvz., autorizavimo koregavimams ir pakartotiniam autorizavimui, atlikti.

Siekiant padėti kontroliuoti, kaip šie periodiniai mokėjimo atpažinimo ženklų naudojami visoje sistemoje, **apriboti** mokėjimo atpažinimo ženklo naudojimą užsakymo konteksto funkcija apriboja pasikartojančio atpažinimo ženklo naudojimą pardavimo užsakymo aprėptimi sistemoje. Kai šis raktas įgalintas, priemonė modifikuoja "Commerce Headquarters" vartotojo sąsają (UI) atnaujindama mokėjimo įvesties puslapius ir apribodama galimybę pasirinkti buvusias kliento mokėjimo nuorodas, kurios bus naudojamos naujuose operacijos egzemplioriuose.

Ši funkcija padeda atitikti kai kurių mokėjimo išdavėjų, pvz., "Visa", naudojimo taisykles. ["Visa Core" taisyklėse ir "Visa Product and Service"](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) taisyklėse "Visa" nurodo, kad mokėjimo atpažinimo ženklų naudojimas turi būti apribotas operacijos aprėptimi, nebent kortelės savininkas sutinka kitaip.

Mokėjimo **atpažinimo ženklo naudojimo užsakymo kontekste** funkcija svarbi tik jei naudojate mokėjimo šliuzo tarnybą, kuri naudoja periodinio mokėjimo atpažinimo ženklo nuorodas.

## <a name="enable-the-feature"></a>Įjungti funkciją

Norėdami įgalinti **mokėjimo atpažinimo ženklo naudojimo apribojimas naudojant užsakymo konteksto funkciją, "Commerce Headquarters" jūsų aplinkoje eikite į Darbo sričių funkcijų valdymą,** **\>** **sąraše suraskite ir pasirinkite Apriboti mokėjimo atpažinimo ženklo naudojimą kaip Užsakymo kontekstą,** tada pasirinkite Įgalinti dabar.**·**

## <a name="limit-payment-token-usage"></a>Riboti mokėjimo atpažinimo ženklo naudojimą

Įgalinus funkciją, "Commerce Headquarters" puslapiai, naudojami mokėjimo metodo fiksavimui, atnaujins, kaip jie nurodo kliento mokėjimo būdus, kurie yra faile klientui. Šis atnaujinimas pirmiausiai turės įtakos dviem operacijų sritims:

- Kaip kliento kortelė faile įvedama kliento vardu
- Kaip išsaugoma mokėjimo pagal klientą informacija dėl būsimų pardavimo užsakymo mokėjimo įrašų

Kai kliento operacijos atsiranda dėl "Commerce" kanalų, mokėjimo informacija saugoma pardavimo užsakymo kontekste. Pardavimo užsakymo kontekstas riboja mokėjimo atpažinimo ženklą, kad jis nebūtų naudojamas kaip mokėjimo nuoroda pagal naujo ar redaguotų pardavimo užsakymo mokėjimų "Commerce Headquarters" kliento įrašą mokėjimo puslapiuose.

### <a name="payment-form-changes"></a>Mokėjimo formos pakeitimai

Kai skambučių centras arba "Commerce Headquarters" vartotojas paima kliento mokėjimą pagal pardavimo užsakymą, mokėjimo puslapyje pateikiama mokėjimo būdo informacija. Kai mokėjimo **atpažinimo ženklo** naudojimo apribojimas užsakymo kontekste yra įgalintas, vartotojui pasirinkus pliuso ženklą (**+**) mokėjimo puslapyje, rodoma tik įrašyta "kortelės faile" įrašai. Pakeitimai reikalauja, kad skambučių centro arba "Commerce Headquarters" vartotojas turėtų įvesti visą mokėjimo informaciją, kurią klientas **pateikė**, kai jis užpildė naujos pardavimo užsakymo operacijos kliento mokėjimo informacijos puslapį.

Verčių sąraše, skirtame laukui **Numeris**, yra tik kortelės nuorodos, kurios susietos su klientu, kuris turi kortelę faile. Filtruoja visas buvusias mokėjimo nuorodas, kurių aprėptis nėra pardavimo užsakymas.

Pliuso ženklas (**+**) **lauke** Numeris lieka pasiekiamas ir gali būti naudojamas mokėjimo informacijai, kurią klientas pateikė operacijai, susijusiai su apdorojamu pardavimo užsakymu, įvesti.

### <a name="how-cards-on-file-work"></a>Kaip veikia kortelės faile

Kai mokėjimo **atpažinimo** ženklo naudojimo apribojimas užsakymo konteksto funkcija yra įgalinta, kortelė faile yra periodinio mokėjimo atpažinimo ženklas, kuris įrašomas kliento įraše ir neapriboja pardavimo užsakymo aprėpties. Failo kortelė leidžia greitai nuorodai į "Commerce Headquarters" vartotojus, kai jie užpildo naujo pardavimo užsakymo mokėjimo puslapį. Ši atpažinimo ženklo nuoroda taikoma tik "Dynamics 365" aplinkai. Interneto kanalams iFrame, kurie naudoja mokėjimų šliuzo paslaugą, suteikia galimybę vartotojams įrašyti mokėjimo būdą, kad ateityje jį būtų galima naudoti mokėjimo modulyje, mokėjimo šliuze šios nuorodos saugomos kaip atskira failo "Dynamics 365" kortelės nuoroda.

Pavyzdžiui, Dynamics 365 Commerce jei Adyen mokėjimo jungtis naudojama interneto kanale, klientai, kurie mokėjimo modulyje įveda savo kredito kortelės informaciją, iFrame mato tik šliuzo tarnybos įrašytas kortelių nuorodas į kitą internetinį pirkimą, kai jos autentifikuotos. Jie nematote "Dynamics 365" aplinkoje saugomos kortelės faile kaip mokėjimo modulio pasirinktis iFrame. Panašiai, kai pirkėjai užsakymus gali pateikti per skambučių centrą, jų įrašytos nuorodos į internetą nebus pateikiamos kaip skambučių centro vartotojo pasirinktys. Skambučių centro vartotojas mato tik ankstesnę kortelę su failo nuorodomis iš "Dynamics 365" sistemos (kaip sutarta kliento), kad įrašytų būsimus užsakymus.

"Commerce Headquarters" vartotojai gali įrašyti kliento kortelę į **failą nueidami į "Retail" ir "Commerce \> Customers** " ir pasirinkdami kliento sąskaitos įrašą. Klientų rinkinio **skyriuje \>** vartotojai, kurie turi teisę apdoroti mokėjimo **puslapius**, gali naudoti kredito kortelių įvedimo puslapį mokėjimo kortelei, kuri bus saugoma faile būsimose operacijose, įvesti. Ši operacija padeda sutaupyti laiko, kai klientas apdoros būsimus pardavimo užsakymo mokėjimus. Skambučių centro ir "Commerce Headquarters" vartotojai failo kortelės informaciją turėtų įvesti tik tada, jei klientas sutinka naudoti kortelės nuorodą būsimoms operacijoms.

Įrašyti **, kad būtų galima naudoti** ateityje, "Commerce Headquarters" mokėjimo puslapių apačioje esantis žymės langelis leidžia vartotojams įrašyti kortelę faile, kad būtų galima naudoti ateityje. Šis žymės langelis turi būti naudojamas tik tada, jei klientas sutinka naudoti kortelę faile būsimose operacijose. Galite rodyti arba **apriboti** **·** **·** **žymės** langelį Įrašyti ateityje naudodami failo skirtuko Mokėjimas parinktį Leisti kliento kortelę, kuri yra "Commerce Headquarters" puslapyje Skambučių centro parametrai. Kai ši parinktis nustatyta kaip **Taip**, "Commerce Headquarters" vartotojai, kurie turi teises apdoroti mokėjimo puslapius **, gali įrašyti kortelę faile, naudodami žymės langelį Įrašyti, kad ateityje būtų** galima naudoti. Kai nustatyta parinktis **Ne**, žymės langelis yra negalimas "Commerce Headquarters" vartotojams, kurie turi teises apdoroti mokėjimo puslapius. **Failo** pasirinktyje leisti kliento kortelę gali būti naudojama, jei jūsų įmonė nori apriboti pasikartojančių atpažinimo ženklų naudojimą "Commerce Headquarters", tačiau dar nenori leisti įrašyti failo kortelės be procedūros, siekiant užtikrinti, kad bus suteiktas kliento sutikimas.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>"Commerce Headquarters" puslapiai, kuriuose taikomi pasikartojančio atpažinimo ženklo apribojimai

Atpažinimo ženklo apribojimo pakeitimas veikia šias "Commerce Headquarters" sritis, kai ši funkcija įgalinta:

- Kliento mokėjimo informacija pardavimo užsakymo **mokėjimuose \> Įvesti \> kliento mokėjimą**
- Tęstinumo užsakymai
- Dalinės įmokos
- Gautinų sumų kredito kortelių mokėjimai

### <a name="manage-payment-tokens-archiving-or-removal"></a>Valdyti mokėjimo atpažinimo ženklus (archyvavimas arba šalinimas)

Mokėjimo atpažinimo **ženklų**, kurie buvo sukurti prieš įgalinus mokėjimo atpažinimo ženklo naudojimo užsakymo kontekste vėliavėlę (arba išjungus funkciją), sistemoje liks "neapriboti" ir juos galima nurodyti pasirinkimo sąrašuose "Commerce Headquarters" mokėjimo puslapyje. Šiuos atpažinimo ženklus "Commerce Headquarters" galima reguliariai pašalinti dviem būdais:

- Norėdami nustatyti **užduotį, kuri reguliariai** išvalo ar archyvuos mokėjimo atpažinimo ženklus, naudokite archyvo kredito kortelės operacijų duomenų puslapį. Jei nustatote pasirinktį **Panaikinti duomenis jų archyvavimo** **metu kaip Taip**, atpažinimo ženklo, **atitinkančio minimalaus operacijos amžiaus (dienomis),** nustatymas bus panaikintas. Daugiau informacijos ieškokite Archive [credit card transaction data](archive-cc-data.md).
- Naudokite naują **puslapį Šalinti kredito kortelių atpažinimo ženklus** (**\>\>\> Gautinų sumų užklausos ir ataskaitos Valyti kredito kortelės atpažinimo ženklus**), tai leidžia paleisti arba nustatyti paketinę užduotį, kuri panaikina mokėjimo atpažinimo ženklus. Nustatykite šiuos parametrus:

    - Minimalus **atpažinimo ženklo amžius dienomis** turi būti 90 dienų arba daugiau.
    - Parametrai **Vykdyti fono parametruose** gali būti naudojami pasikartojimo ar **įspėjimų** **parametrams** nustatyti.
    - Paketų grupė gali būti priskirta tam tikros grupės užduočiai vykdyti.
    - Jei pasirinktis **Privatus** nustatyta kaip **Taip**, ją vykdyti gali tik užduotį sukūrusis vartotojas.
    - Parametras Taip **,** jei pasirinktis **Kritinė** užduotis užtikrina, kad sistema aktyviai seks užduoties būseną.

Panaikintų atpažinimo ženklų nuskaityti negalima. Lauke Minimalus **atpažinimo ženklo** amžius dienomis nustatykite į diapazoną, kuris atitinka ilgiausiai jūsų aplinkoje operacijų trukmę (nuo autorizavimo iki fiksavimo ar grąžinimo).

## <a name="additional-resources"></a>Papildomi ištekliai

[DUK apie mokėjimus](payments-retail.md)

[Pirkimo užbaigimo modulis](../add-checkout-module.md)

[Mokėjimo modulis](../payment-module.md)
