---
title: Darbas su EKA serijos prekėmis
description: Šioje temoje paaiškinama, kaip valdyti serijos prekes elektroninio kasos aparato (EKA) programoje.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978368"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Darbas su EKA serijos prekėmis

[!include [banner](includes/banner.md)]

Daug mažmenininkų parduoda produktus, kuriems reikia serijos valdymo. Šie produktai vadinami *serijos prekėmis*. Kai kurie mažmenininkai gali norėti tvarkyti parduotuvės ar sandėlio atsargų serijos numerius stebėjimo tikslais. Kiti mažmenininkai gali norėti fiksuoti serijos numerius pardavimo proceso metu paslaugų ir garantijos tikslais. Šioje temoje paaiškinama, kaip galite valdyti serijos prekes „Microsoft Dynamics 365 Commerce” elektroninio kasos aparato (EKA) programoje.

## <a name="serial-number-configurations"></a>Serijos numerių konfigūracijos

Prekė yra serijos prekė, jei jai priskirta sekimo dimensijos grupė, nustatyta leisti serijos numerius. „Commerce Headquarters” puslapyje **Sekimo dimensijų grupės** pasirinkite parinktį **Aktyvūs**, norėdami įgalinti atsargų proceso serijos numerius, arba pasirinkite parinktį **Aktyvūs pardavimo procese**, norėdami įgalinti pardavimų proceso serijos numerius.

„FastTab” **Sekimo dimensijos** įjunkite parametrą **Galimas tuščias gavimas**, kad serijos numeris būtų pasirinktinė įvestis serijos prekės atsargų gavimo proceso metu. Išjungus šį parametrą reikia įvesti serijos numerį. Be to, parametras **Galimas tuščias išdavimas** kontroliuoja, ar serijos numeris yra būtinas atliekant atsargų siuntimo procesą.

> [!NOTE]
> Norėdami naudoti operaciją **Gaunamos atsargos** ir EKA operacijas **Siunčiamos atsargos** serijos numeriams registruoti arba patikrinti pagal serijos prekę, turite sukonfigūruoti prekę, kad ji būtų priskirta sekimo dimensijos grupei, nustatytai leisti serijos numerius parinktyje **Aktyvūs**, o ne parinktyje **Aktyvūs pardavimo procese**.

## <a name="serial-number-management-page"></a>Puslapis Serijos numerių valdymas

Jei prekė, pasirenkama, gaunama arba siunčiama EKA operacijose **Gaunamos atsargos** ir **Siunčiamos atsargos**, yra serijos prekė, srityje **Išsami informacija** yra parinktis **Valdyti serijos numerį**, kuri susieja su puslapiu **Serijos numerių valdymas**, kuriame galite registruoti arba tikrinti prekės serijos numerius. Taip pat galite atidaryti puslapį **Serijos numerio valdymas** pasirinkdami veiksmą **Serijos numeris** užsakymo informacijos rodinio programos juostoje arba parinktį **Valdyti serijos numerį** dialogo lange, raginančiame gavimo arba siuntimo proceso metu. 

Puslapyje **Serijos numerio valdymas** išvardijamos visos atidarytos serijos numerių eilutės, laukiančios užregistravimo arba tikrinimo. Šiame puslapyje gali būti du skirtukai: pasirinktos prekės skirtukas ir visų užsakymo serijos prekių skirtukas.

Puslapio **Serijos numerio valdymas** laukas **Būsena** suteikia informacijos apie dabartinį etapą, kuriame yra kiekvienas serijos numeris.

- **Neužregistruota** – serijos numeris nepateiktas arba anksčiau registruotas serijos numeris dar nėra patikrintas (gavimo proceso metu).
- **Užregistruota** – serijos numeris buvo užregistruotas ir įrašytas vietoje į parduotuvės kanalo duomenų bazę arba patikrintas anksčiau registruotas serijos numeris. Kai baigsite gavimą arba vykdymą, „Commerce“ būstinei bus pateikti tik serijos numeriai, kurių būsena **Užregistruota**.

## <a name="receive-serialized-items"></a>Serijos prekių gavimas

EKA operacija **Gaunamos atsargos** leidžia vartotojams atlikti toliau pateiktas serijos prekių užduotis.

- Registruokite serijos numerius pagal serijos prekes, kai tos prekės gaunamos parduotuvėje naudojant pirkimo užsakymą.
- Tikrinkite anksčiau registruotus serijos numerius pagal serijos prekes, kai tos prekės gaunamos parduotuvėje naudojant pirkimo užsakymą arba perkėlimo užsakymą.

### <a name="register-serial-numbers-against-serialized-items"></a>Serijos numerių registravimas pagal serijos prekes

Jei dirbate su pirkimo užsakymu, dialogo langas, raginantis serijos prekės gavimo proceso metu, siūlo parinktį **Valdyti serijos numerį**. Galite pasirinkti šią pasirinktį, norėdami atidaryti puslapį **Serijos numerio valdymas** ir pradėti registruoti serijos numerius. Taip pat galite praleisti šį veiksmą gavimo proceso metu ir pateikti įvestį vėliau, prieš užregistruodami gavimą.

Pagal numatytuosius nustatymus rodomas pasirinktos prekės skirtukas. Visose serijos numerių eilutėse yra tuščia serijos numerio reikšmė ir būsena **Neužregistruota**. Galite nuskaityti serijos numerių brūkšninius kodus arba programos juostoje galite pasirinkti **Serijos numeris**, kad serijos numeriai būtų nuolat įvedami. Įvesti serijos numeriai rodomi sąraše, o jų būsena pasikeičia į **Užregistruota**. Maksimalus serijos numerių, kuriuos galite užregistruoti sąraše, skaičius lygus gavimo kiekiui. Jei padarėte klaidą, srityje **Išsami informacija** galite pasirinkti **Redaguoti** arba **Valyti**, kad būtų pakeisti įvesti serijos numeriai.

Taip pat galite užregistruoti serijos numerius puslapio **Serijos numerio valdymas** skirtuke **Visos serijos prekės**. Sąraše pasirinkite prekę, pagal kurią norite registruoti serijos numerius.

### <a name="validate-serial-numbers-on-serialized-items"></a>Serijos prekių serijos numerių tikrinimas

Jei dirbate su perkėlimo užsakymu, siunčianti šalis turi iš anksto užregistruoti serijos prekių serijos numerius siuntimo proceso metu. Jei dirbate su pirkimo užsakymu, tiekėjas gali pateikti serijos numerio informaciją naudodamas išankstinį siuntimo pranešimą (ASN), o jūs galite iš anksto registruoti siunčiamų prekių numerius. Abiem atvejais serijos numeriai žinomi prieš gavimą. Todėl gaunančiai šaliai tereikia patikrinti, kad gavo tai, ką turėjo gauti.

Norėdami patikrinti serijos numerius, galite atidaryti puslapį **Serijos numerio valdymas** gavimo proceso metu arba bet kada iki gavimo užregistravimo. Visi kiekvienos serijos prekės, kurios serijos numeriai yra anksčiau registruoti, serijos numeriai šiame puslapyje automatiškai nustatomi į pradinę būseną **Neužregistruota**. Norėdami patikrinti serijos numerius, galite juos nuskaityti arba įvesti. Įvedus serijos numerius, programa patikrina, ar jie atitinka anksčiau registruotus serijos numerius. Jei jie sutampa, jų būsena pasikeičia į **Užregistruota**. Kitu atveju gaunate klaidos pranešimą. Taip pat galite tiesiogiai pasirinkti serijos numerį, tada srityje **Išsami informacija** pasirinkti parinktį **Tikrinti serijos numerį**, norėdami greitai pažymėti tą serijos numerį kaip patikrintą. Maksimalus serijos numerių, kuriuos galite tikrinti sąraše, skaičius lygus gavimo kiekiui.

Taip pat galite tikrinti serijos numerius puslapio **Serijos numerio valdymas** skirtuke **Visos serijos prekės**. Sąraše pasirinkite prekę, pagal kurią norite tikrinti serijos numerius.

## <a name="ship-serialized-items"></a>Serijos prekių siuntimas

Galite naudoti EKA operaciją **Siunčiamos atsargos**, norėdami registruoti serijos numerius pagal serijos prekes, kai jos siunčiamos iš esamos parduotuvės naudojant perkėlimo užsakymą.

### <a name="register-serial-numbers-against-serialized-items"></a>Serijos numerių registravimas pagal serijos prekes

Jei dirbate su perkėlimo užsakymu, dialogo langas, raginantis serijos prekės siuntimo proceso metu, siūlo parinktį **Valdyti serijos numerį**. Galite pasirinkti šią pasirinktį, norėdami atidaryti puslapį **Serijos numerio valdymas** ir pradėti registruoti serijos numerius. Taip pat galite praleisti šį veiksmą siuntimo proceso metu ir pateikti įvestį vėliau, prieš užregistruodami siuntimą.

Pagal numatytuosius nustatymus rodomas pasirinktos prekės skirtukas. Visose serijos numerių eilutėse yra tuščia serijos numerio reikšmė ir būsena **Neužregistruota**. Galite nuskaityti serijos numerių brūkšninius kodus arba programos juostoje galite pasirinkti **Serijos numeris**, kad serijos numeriai būtų nuolat įvedami. Įvesti serijos numeriai rodomi sąraše, o jų būsena pasikeičia į **Užregistruota**. Maksimalus serijos numerių, kuriuos galite užregistruoti sąraše, skaičius lygus siuntimo kiekiui. Jei padarėte klaidą, srityje **Išsami informacija** galite pasirinkti **Redaguoti** arba **Valyti**, kad būtų pakeisti įvesti serijos numeriai.

Taip pat galite užregistruoti serijos numerius puslapio **Serijos numerio valdymas** skirtuke **Visos serijos prekės**. Sąraše pasirinkite prekę, pagal kurią norite registruoti serijos numerius.

Jei norite, galite įjungti serijos numerio pasiekiamumo tikrinimą serijos numerio registracijos pagal siunčiamą perkėlimo užsakymą metu. Jei šio tikrinimo metu bandysite išsiųsti serijos numerį, kurio nėra siunčiančios parduotuvės atsargose, gausite klaidos pranešimą ir turėsite nurodyti kitą numerį.

Norėdami įjungti šį tikrinimą, būtina suplanuoti toliau pateiktas užduotis, kad jos būtų vykdomos reguliariai.

- **„Retail“ ir „Commerce“** > **„Retail“ ir „Commerce“ IT** > **Produktai ir atsargos** > **Produkto pasiekiamumas su sekimo dimensijomis**.
- **„Retail“ ir „Commerce“** > **Paskirstymo grafikai** > **1130** (**Produkto pasiekiamumas**)

## <a name="additional-resources"></a>Papildomi ištekliai

[Atvežamų atsargų operacija EKA](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Siunčiamų atsargų operacija EKA](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
