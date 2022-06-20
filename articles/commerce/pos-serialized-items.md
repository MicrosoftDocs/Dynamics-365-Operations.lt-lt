---
title: Darbas su EKA serijos prekėmis
description: Šiame straipsnyje paaiškinama, kaip valdyti eilutėmis išrašytas prekes point point of sale (EKA) programoje.
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 8a715a9d025f36656506daeb9e611bfacdafa102
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880034"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Darbas su EKA serijos prekėmis

[!include [banner](includes/banner.md)]

Daug mažmenininkų parduoda produktus, kuriems reikia serijos valdymo. Šie produktai vadinami *serijos prekėmis*. Kai kurie mažmenininkai gali norėti tvarkyti parduotuvės ar sandėlio atsargų serijos numerius stebėjimo tikslais. Kiti mažmenininkai gali norėti fiksuoti serijos numerius pardavimo proceso metu paslaugų ir garantijos tikslais. Šiame straipsnyje paaiškinama, kaip valdyti išrašytas prekes point Microsoft Dynamics 365 Commerce sale (EKA) programoje.

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

## <a name="sell-serialized-items-in-pos"></a>Parduoti serijines prekes EKA

Kai EKA programa visuomet palaikoma parduodamose serijinėse prekėse, „Commerce“ versijoje 10.0.17 ir vėlesnėse, organizacijos gali įjungti funkcijas, kurios apima verslo logiką paleistą kai parduodami produktai konfigūruojami serijinio numerio sekimui.

Kai **Apimtas serijinio numerio patvirtinimas EKA užsakyme apima ir užsakymo įgyvendinimo** funkcija yra išjungta, tolesnės produkto konfigūracijos yra įvertinamos kai parduodami produktai serijiniai per EKA:

- **Serijos tipas** produkto nustatymas (**aktyvus** ar **aktyvus prekyboje**).
- **Tuščios problemos leidimas** nustatymai produktui.
- **Fizinis neigiamas inventorius** nustatymas produktui ir (ar) pardavimo sandėliui.

### <a name="active-serial-configurations"></a>Aktyvios serijinės konfigūracijos

Kai prekės parduodamos EKA, kuris sukonfigūruotas su **Aktyviu** serijinio numerio sekimo dimensija, EKA pradeda patvirtinimo logiką, kuri apsaugo vartotojus nuo serijinės prekės pardavimo užbaigimo su serijiniu numeriu, kurio rasti nepavyksta pardavimo sandėlio esamame inventoriuje. Šiai tvirtinimo taisyklei yra dvi išlygos:

- Prekė taip pat konfigūruojama su **Tuščios problemos leidimas** įjungta, vartotojai gali praleisti serijinio numerio įrašymą ir parduoti prekę be jokio paskirto serijinio numerio.
- Jei prekė ir (ar) pardavimo sandėlis yra konfigūruojamas su **Fiziniu neigiamu inventoriumi** įjungtu, programa priima ir parduoda serijinį numerį, kuris negali būti patvirtintas inventoriuje sandėlyje, kuris parduodamas pagal jį. Šis konfigūravimas leidžia inventoriaus transakciją konkrečiai prekei ar serijiniam numeriui būti neigiamam ir dėl to, sistema leis nežinomų serijinių numerių prekybą.

> [!IMPORTANT]
> Siekiant įsitikinti, kad EKA programa gali tinkamai tvirtinti, ar serijinis numeris yra parduodamas kaip **Aktyvus** serijinis prekių tipas, kuris yra pardavimo sandėlio inventoriuje, būtina organizacijoms **Produkto prieinamumas su sekimo dimensijos** darbą atlikti „Commerce“ štabe ir kartu **1130** produkto prieinamumo paskirstymo darbą per „Commerce“ štabo dažniu režimu. Kadangi naujas serijinės atsargos yra gaunamos į pardavimo sandėlį siekiant EKA patvirtinti inventoriaus serijinių numerių prieinamumą, inventoriaus pagrindiniai duomenys turi dažnai naujinti kanalo duomenų bazę su naujausiais inventoriaus prieinamumo duomenimis. Darbas **Produkto prieinamumas su sekimo dimensijomis** ima momentinę ekrano nuotrauką pagrindinio inventoriaus, įskaitant serijinius numerius visiems įmonių sandėliams. **1130** paskirstymo darbas paima to inventoriaus momentinę ekrano nuotrauką ir ją bendrina su visomis konfigūruotomis kanalo duomenų bazėmis.

### <a name="active-in-sales-process-serial-configurations"></a>Aktyvios pardavimų proceso serijinėse konfigūracijose

Prekės konfigūruotos su serijine dimensija kaip **Aktyvios pardavimo procese** nepereina per inventoriaus tvirtinimo logiką, nes konfigūravimas taikomas inventoriaus serijiniams numeriams nėra registruojamas iš anksto atsargoms ir serijiniai numeriai nėra aprėpiami pardavimo metu.  

Jei **Tuščia problema leidžiama** taip pat konfigūruojama **Aktyvios prekybos procese** konfigūruotos prekės, serijinio numerio įrašas gali būti praleistas. Jei **Tuščia problema leidžiama** nėra konfigūruota, programa prašo vartotojo įvesti serijinį numerį net jei jis nebus patvirtintas pagal prieinamą inventorių.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Taikyti serijinius numerius EKA transakcijų kūrimo metu

EKA programa nedelsiant skatina vartotojus serijiniams numeriams apimti, kai parduodamos serijinės prekės, bet programa leidžia vartotojams praleisti įvedimą serijinio numerio iki tam tikro taško pardavimo metu. Vartotojui pradėjus apimti mokėjimą, programa įgalina ir reikalauja serijinio numerio įvedimo bet kurioms prekėms, kurios nėra konfigūruotos siekiant atitikti per tolesnius siuntimus ar paėmimus. Bet kurios serijinės prekės sukonfigūruotos grynų ir atsiėmimo ar atsiėmimo įgyvendinimo metu, prašo vartotojo apimti serijinį numerį (ar sutikti palikti tuščią, jei prekių konfigūravimas leidžia tą daryti) prieš užbaigiant pardavimą.

Serijinės prekės parduodamos ateities paėmimui ar siuntimui, EKA vartotojai gali praleisti serijinio numerio įvedimą iš pradžių ir vis dar užbaigti kliento užsakymo kūrimą.   

> [!NOTE]
> Parduodant ar įgyvendinant serijinius produktus per EKA programą, „1“ kiekis yra įgalinamas serijinėms prekėms pardavimo transakcijoje. Tai yra rezultatas, kaip serijinio numerio informacija sekama pardavimų eilutėje. Parduodant ar įgyvendinant transakciją keliems serijiniams produktams per EKA, kiekviena eilutė turi būti konfigūruojama su „1“ kiekiu. 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Taikyti serijinius numerius kliento užsakymo įgyvendinimo ar paėmimo metu

Įgyvendinant kliento užsakymo eilutes serijiniams produktams naudojant **Užsakymo įgyvendinimo** veiksmą EKA, EKA įgalina aprėpti serijinį numerį prieš paskutinį įgyvendinimą. Dėl to, jei serijinis numeris nėra pateiktas pradinio užsakymo aprėpties metu, jis turi būti apimtas paėmimo, supakavimo ar siuntimo procesuose EKA. Tvirtinimas yra atliekamas kiekvienu veiksmu ir vartotojo tik bus paklausta serijinio numerio duomenų, jei jų nėra ar jie negalioja. Pavyzdžiui, jei vartotojas praleidžia paėmimą ar supakavimo žingsnius ir nedelsiant pradeda siuntimą, o serijinis numeris nėra registruotas eilutei, EKA reikalaus serijinio numerio įvedimo prieš paskutinio sąskaitos veiksmo užbaigimą. Kai EKA vykdant serijos numerio įrašymo įvykdymą EKA reikia įvykdyti visas anksčiau šiame straipsnyje nurodytas taisykles. Tik serijinės prekės, konfigūruotos kaip **Aktyvios** pereina per serijinio numerio inventoriaus atsargų tvirtinimą. Prekės konfigūruotos kaip **Aktyvios prekybos procese** nebus patvirtintos. Jei **Fizinės neigiamos atsargos** leidžiamos **Aktyviose** produktuose, bet koks serijinis numeris bus priimtas nepriklausomai nuo atsargų prieinamumo. Abiem **Aktyviems** ir **Aktyviems prekybos procesams** prekėms, jei **Tuščia problema leidžiama** yra konfigūruota, vartotojas gali palikti serijinius numerius tuščius, jei nori paėmimo, pakavimo ir siuntimo veiksmų metu.

Patvirtinimai serijiniams numeriams taip pat vyks, kai vartotojas atliks paėmimo veiksmus kliento užsakymuose EKA. EKA programa neleidžia atlikti paėmimo serijiniams produktams, nebent jis praeina pro patvirtinimą kaip minėta anksčiau. Patvirtinimai visada paremti produkto sekimo dimensija ir pardavimo sandėlio konfigūravimais. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Atvežamų atsargų operacija EKA](./pos-inbound-inventory-operation.md)

[Siunčiamų atsargų operacija EKA](./pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]