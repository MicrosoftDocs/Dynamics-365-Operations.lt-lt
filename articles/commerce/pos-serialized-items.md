---
title: Darbas su EKA serijos prekėmis
description: Šioje temoje paaiškinama, kaip valdyti serijos prekes elektroninio kasos aparato (EKA) programoje.
author: boycezhu
manager: annbe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eedb64ae04345cb94bdd8cc68de833cfcfd40119
ms.sourcegitcommit: 39981582778b0a62567324452485a6721ca18284
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2020
ms.locfileid: "3407503"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Darbas su EKA serijos prekėmis

[!include [banner](includes/banner.md)]

Daug mažmenininkų parduoda produktus, kuriems reikia serijos valdymo. Šios prekės vadinamos *serijos prekėmis*. Kai kurie mažmenininkai gali norėti tvarkyti serijos numerius stebėjimo tikslais. Kiti mažmenininkai gali norėti fiksuoti serijos numerius pardavimo proceso metu paslaugų ir garantijos tikslais. Šioje temoje paaiškinama, kaip galite valdyti serijos prekes „Microsoft Dynamics 365 Commerce” elektroninio kasos aparato (EKA) programoje.

## <a name="serial-number-configurations"></a>Serijos numerių konfigūracijos

Prekė yra serijos prekė, jei jai priskirta sekimo dimensijos grupė, nustatyta leisti serijos numerius. „Commerce“ būstinės puslapyje **Sekimo dimensijų grupės** pasirinkite parinktį **Aktyvi**, kad įgalintumėte atsargų proceso serijos numerius. Norėdami įgalinti pardavimo proceso serijos numerius, pasirinkite parinktį **Aktyvūs pardavimo procese**.

Jei įjungta parinktis **Galimas tuščias gavimas**, „FastTab” **Sekimo dimensijos** serijos numeris yra pasirinktinė įvestis atsargų gavimo proceso metu. Jei parinktis išjungta, reikia nurodyti serijos numerį.

Jei įjungta parinktis **Serijos numerių kontrolė**, „FastTab” **Serijos numeriai** serijos numeris vienete turi būti unikalus. Kitaip tariant, dubliuoti serijos numeriai neleidžiami.

## <a name="serialized-items-in-the-receiving-process"></a>Gavimo proceso serijos prekės

EKA programos operacija **Gaunamos atsargos** leidžia vartotojams atlikti toliau pateiktas serijos prekių užduotis.

- Registruokite serijos numerius pagal serijos prekes, kai tos prekės gaunamos parduotuvėje naudojant pirkimo užsakymą.
- Tikrinkite anksčiau registruotus serijos numerius pagal serijos prekes, kai tos prekės gaunamos parduotuvėje naudojant pirkimo užsakymą arba perkėlimo užsakymą.

> [!NOTE]
> Norint naudoti operaciją **Gaunamos atsargos** serijos prekei registruoti arba patikrinti, prekei turi būti priskirta sekimo dimensijos grupė, nustatyta leisti serijos numerius parinktyje **Aktyvi**, o ne parinktyje **Aktyvūs pardavimo procese**.

Norėdami pradėti gavimo procesą, operacijos **Gaunamos atsargos** rodinyje **Gaunama dabar** galite pradėti prekės brūkšninio kodo nuskaitymą ir prekės ID įvedimą. Taip pat rodinyje **Visas užsakymų sąrašas** galite pradėti peržiūrą neautomatiniu būdu pasirinkdami prekę.

Jei pasirenkama arba gaunama prekė yra serijos prekė, srityje **Išsami informacija** yra saitas **Valdyti serijos numerį**, atidarantis puslapį **Serijos numerio valdymas**. Taip pat galite atidaryti puslapį **Serijos numerio valdymas** pasirinkdami **Serijos numeris** užsakymo informacijos rodinio programos juostoje arba **Valdyti serijos numerį** dialogo lange, raginančiame gavimo proceso metu. Puslapyje **Serijos numerio valdymas** išvardijamos visos atidarytos serijos numerių eilutės, laukiančios užregistravimo arba tikrinimo. Šiame puslapyje gali būti du skirtukai: pasirinktos prekės skirtukas ir visų užsakymo serijos prekių skirtukas.

Puslapio **Serijos numerio valdymas** laukas **Būsena** suteikia informacijos apie dabartinį etapą, kuriame yra kiekvienas serijos numeris.

- **Neužregistruota** – serijos numeris nepateiktas arba anksčiau registruotas serijos numeris dar nėra patikrintas.
- **Užregistruota** – serijos numeris buvo užregistruotas ir įrašytas vietoje į parduotuvės kanalo duomenų bazę arba patikrintas anksčiau registruotas serijos numeris. Kai baigsite gavimą, „Commerce“ būstinei bus pateikti tik serijos numeriai, kurių būsena **Užregistruota**.

### <a name="register-serial-numbers-against-serialized-items"></a>Serijos numerių registravimas pagal serijos prekes

Jei dirbate su pirkimo užsakymu, dialogo langas, raginantis serijos prekės gavimo proceso metu, siūlo parinktį **Valdyti serijos numerį**. Galite pasirinkti šią pasirinktį, norėdami atidaryti puslapį **Serijos numerio valdymas** ir pradėti registruoti serijos numerius. Taip pat galite praleisti šį veiksmą gavimo proceso metu ir pateikti įvestį vėliau, prieš užregistruodami gavimą.

Pagal numatytuosius nustatymus rodomas pasirinktos prekės skirtukas. Visose serijos numerių eilutėse yra tuščia serijos numerio reikšmė ir būsena **Neužregistruota**. Galite nuskaityti serijos numerių brūkšninius kodus arba programos juostoje galite pasirinkti **Serijos numeris**, kad serijos numeriai būtų nuolat įvedami dialogo lange. Įvesti serijos numeriai rodomi sąraše, o serijos numerio eilučių būsena pasikeičia į **Užregistruota**. Maksimalus serijos numerių, kuriuos galite užregistruoti sąraše, skaičius lygus gavimo kiekiui. Jei padarėte klaidą, srityje **Išsami informacija** galite pasirinkti **Redaguoti** arba **Valyti**, kad būtų pakeisti įvesti serijos numeriai.

Taip pat galite užregistruoti serijos numerius puslapio **Serijos numerio valdymas** skirtuke **Visos serijos prekės**. Sąraše pasirinkite prekę, pagal kurią norite registruoti serijos numerius.

Šiame puslapyje atliekant serijos numerių registravimą vykdomas dubliavimo patikrinimas. Jei bandote įvesti dubliuotą serijos numerį pagal prekę, kuriai įjungtas serijos numerio valdymas, gausite klaidos pranešimą ir turėsite nurodyti kitą numerį.

### <a name="validate-serial-numbers-on-serialized-items"></a>Serijos prekių serijos numerių tikrinimas

Jei dirbate su perkėlimo užsakymu, siunčianti šalis turi iš anksto užregistruoti serijos prekių serijos numerius siuntimo proceso metu. Jei dirbate su pirkimo užsakymu, tiekėjas gali pateikti serijos numerio informaciją naudodamas išankstinį siuntimo pranešimą (ASN), o jūs galite iš anksto registruoti siunčiamų prekių numerius. Abiem atvejais serijos numeriai žinomi prieš gavimą. Todėl gaunančiai šaliai tereikia patikrinti, kad gavo tai, ką turėjo gauti.

Norėdami patikrinti serijos numerius, galite atidaryti puslapį **Serijos numerio valdymas** gavimo proceso metu arba bet kada iki gavimo užregistravimo. Visi kiekvienos serijos prekės, kurios serijos numeriai yra anksčiau registruoti, serijos numeriai šiame puslapyje automatiškai nustatomi į pradinę būseną **Neužregistruota**. Norėdami patikrinti serijos numerius, galite juos nuskaityti arba įvesti. Įvedus serijos numerius, programa patikrina, ar jie atitinka anksčiau registruotus serijos numerius. Jei jie sutampa, jų būsena pasikeičia į **Užregistruota**. Kitu atveju gaunate klaidos pranešimą. Maksimalus serijos numerių, kuriuos galite tikrinti sąraše, skaičius lygus gavimo kiekiui.

Taip pat galite tikrinti serijos numerius puslapio **Serijos numerio valdymas** skirtuke **Visos serijos prekės**. Sąraše pasirinkite prekę, pagal kurią norite tikrinti serijos numerius.

## <a name="additional-resources"></a>Papildomi ištekliai

[Atvežamų atsargų operacija EKA](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
