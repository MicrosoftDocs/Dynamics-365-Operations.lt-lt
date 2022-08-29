---
title: Išmokų valdymo apžvalga
description: Šiame straipsnyje pateikta išmokų valdymo funkcijos apžvalga Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e3fa839b6e0f3cbaea8d2225b5a42ee8a368272
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337350"
---
# <a name="benefits-management-overview"></a>Išmokų valdymo apžvalga

Norėdami išlikti konkurencingi, turite pasiūlyti gausų išmokų rinkinį, kad pritrauktumėte ir išlaikytumėte savo geriausius darbuotojus. Be įprastų privalumų, pvz., sveikatos ir dantų priežiūros draudimo, taip pat galite siūlyti išplėstines paslaugas, pvz., įvaikinimo pagalbą, poilsio programas ir išmokas drabužiams. Išmokų valdymas programoje „Microsoft Dynamics 365 Human Resources“ – dinamiškas sprendimas, palaikantis daugybę išmokų parinkčių. „Human Resources“ taip pat apima lengvai naudojamas darbuotojų funkcijas, kuriomis demonstruojami jūsų pasiūlymai.

- Išplėstiniai išmokų planai leidžia kurti ir valdyti unikalius išmokų planus ir palaikymo sudėtinių išmokų tarifų lenteles ir įdėtąsias pakopas. Galite lengvai sukurti išmokų programas, paketus ir automatinės registracijos taisykles, kad palengvintumėte darbuotojo patirtį.
- Lanksčiųjų kreditų programomis galite proporcingai paskirstyti, kad būtų palaikomi išėjimas į pensiją ir kiti gyvenimo įvykiai.
- Dėl platesnių tinkamumo taisyklių galite būti užtikrinti, kad reikiamos išmokos pasieks reikiamus darbuotojus.
- Internetine išmokų registracija suteikiama puiki jūsų darbuotojų patirtis.
- Tinkamo gyvenimo įvykio apdorojimas palaiko būsimus gyvenimo įvykius.

Jei norite gauti prieigą prie demonstracinių duomenų, turite iš naujo įdiegti savo smėlio dėžės aplinką.

> [!NOTE]
> Dabar galite pritaikyti išmokų valdymo puslapius. Dabar galite pridėti pasirinktinius laukus, susijusius su padengimo **tarifais, į išmokų** planų parinkties puslapį. Norėdami gauti daugiau informacijos apie darbą su pasirinktinais laukais, žr. [Pasirinktini laukai](hr-developer-custom-fields.md).
>
> ![Išmokų valdymo pasirinktiniai laukai](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Išmokų valdymo įjungimas

Šiame straipsnyje aprašoma, kaip įjungti „Human Resources“ funkcijas. Joje taip pat nurodoma, kurios esamos Personalo funkcijos pakeičiamos Išmokų valdymu arba kurios funkcijos bus išjungiamos, kai įjungsite Išmokų valdymą.

> [!IMPORTANT]
> Po to, kai **gamybos** aplinkoje įgalinate išmokų valdymą, jo išjungti negalima. Rekomenduojame įjungti ir testuoti išmokų valdymą **smėlio dėžės** aplinkoje prieš įjungiant jį **gamybos** aplinkoje. Yra reikšmingų skirtumų tarp pasenusių išmokų funkcijų ir naujų išmokų valdymo funkcijų – joms reikalingi papildomi nustatymai ir tikrinimai prieš įtraukiant į gamybos procesą.

Norėdami gauti daugiau informacijos, žr. [Funkcijų valdymas](hr-admin-manage-features.md).

## <a name="process-overview"></a>Proceso apžvalga

Išmokų konfigūravimo procesą sudaro šios užduotys:

1.  Reikalingos išmokų informacijos nustatymas.
2.  Papildomos išmokų informacijos nustatymas.
3.  Išmokų planų nustatymas.
4.  Lanksčių kredito programų nustatymas (pasirinktinai).
5.  Reikalingos darbuotojo informacijos konfigūravimas.
6.  Papildomos darbuotojo informacijos konfigūravimas.
7.  Darbuotojų apdorojimas tinkamumo nustatymui.
8.  Darbuotojai pasirenka planus per darbuotojų savitarną (pasirinktinai).
9.  Darbuotojo plano pasirinkimų patvirtinimas.
10. Gyvenimo įvykių apdorojimas (pasirinktinai).
11. Tarifo naujinimai (pasirinktinai).

## <a name="set-up-required-benefit-information"></a>Reikalingos išmokų informacijos nustatymas

Tam, kad darbuotojai galėtų būti įtraukti į planus, reikia nustatyti kelis komponentus:

- **Išmokų valdymo parametrai** – šie parametrai yra bendrai naudojami visose įmonėse. Galite nustatyti numatytuosius priežasčių kodus, įgalinti **Išmokų metinio atlyginimo** parinktį, nustatyti numatytąjį naujų samdomų darbuotojų mokėjimo dažnumą ir įgalinti gyvenimo įvykius. Daugiau informacijos rasite [Išmokų valdymo parametrų nustatymas](hr-benefits-setup-parameters.md).
- **Asmeninių kontaktų tinkamumo parinktys** – asmeniniai kontaktai yra asmenys, kurie bus priklausomieji arba gavėjai nustatomosiose planuose. Įprastai jie yra vaikai, sutuoktiniai arba patikėjimo organizacijos. Daugiau informacijos žr. [Asmeninių kontaktų tinkamumo parinkčių konfigūravimas](hr-benefits-setup-contact-eligibility-options.md).
- **Padengimo parinktys** – nustatyti padengimo tipus, kurie bus prieinami planui. Tiksliau, nurodykite, kas turėtų būti apdraustas arba koks padengimas ura galimas. Daugiau informacijos rasite [Padengimo parinkčių kūrimas](hr-benefits-setup-coverage-options.md).
- **Plano tipai** – nustatykite planų tipus, kurie bus pasiekiami jums kuriant išmokų planą. Plano tipų pavyzdžiai apima **Dantų**, **Regėjimo** ir **Santaupų**. Kai kurie svarbūs plano tipo parametrai nustato išmokų planui galimus parametrus. Daugiau informacijos žr. dalyje [Planų tipų kūrimas](hr-benefits-setup-plan-types.md).
- **Tinkamumo taisyklės** – tinkamumo taisyklės yra naudojamos norint nustatyti, ar darbuotojas atitinka plano reikalavimus. Nors viena tinkamumo taisyklė turi būti susieta su kiekvienu išmokų planu. Daugiau informacijos rasite [Tinkamumo taisyklių ir parinkčių konfigūravimas](hr-benefits-setup-eligibility-rules.md).
- **Mokėjimo dažnumas** – mokėjimo dažnumas reikalingas, kai konfigūruojami išmokų tarifai. Mokėjimo dažnumas naudojamas pagal tarifą padeda nustatyti sumą, kurią darbuotojas ir (arba) darbdavys turi sumokėti kas savaitę, kas mėnesį arba kasmet. Daugiau informacijos rasite [Mokėjimo dažnumo nustatymas](hr-benefits-setup-payment-frequencies.md).
- **Tarifai** – jie apibrėžia, kiek išmoka kainuos arba darbuotojui, arba darbdaviui. Jei pinigai turėtų būti grąžinami darbuotojui (pavyzdžiui, kreditas sporto klubo narystei), įvedamas neigiamas tarifas. Daugiau informacijos rasite [Tarifų konfigūravimas](hr-benefits-setup-rates.md).
- **Pakopiniai tarifai** – pakopiniai tarifai naudojami, kai tarifas turi keistis pagal tam tikrus kriterijus. Dažniausias pakopinis tarifas yra viena pakopa, pagrįsta amžiumi. Tačiau taip pat galima nustatyti dvigubos pakopos tarifus, kai tarifas gali keistis pagal lytį, amžių ar kitus kriterijus.
- **Atskaitymai** – jie iš esmės yra antraštės informacija/kodai, kurie bus perduoti algalapio sistemai, kad būtų galima identifikuoti išmokos atskaitymą. Privalote nustatyti šiuos atskaitymus, nes jie bus reikalingi išmokų plane. Daugiau informacijos rasite [Atskaitymų konfigūravimas](hr-benefits-setup-deductions.md).
- **Išmokų laikotarpiai** – išmokų laikotarpis yra laikotarpis, per kurį darbuotojai turės išmokų draudimą. Jis taip pat yra žinomas kaip plano metai. Čia taip pat nustatomi atviros registracijos laikotarpiai.

## <a name="set-up-optional-benefit-information"></a>Papildomos išmokų informacijos nustatymas

Norint sukurti išmokų planą nereikia nustatyti šių komponentų:

- **Programos** – programa yra išmokų rinkinys, kurį reglamentuoja tos pačios tinkamumo taisyklės. Pavyzdžiui, visi pardavimų skyriaus darbuotojai gali gauti mobilųjį telefoną.
- **Grupavimai** – grupavimas yra išmokų grupė, kurioje reikia pasirinkti vieną planą, kad būtų galima papildomų planų pasirinkimo parinktis. Pavyzdžiui, labai atskaitantis medicininis planas gali būti sugrupuotas su sveikatos taupomosios sąskaitos (HSA) planu.
- **Gyvenimo įvykių tipai** – tai įvykiai, leidžiantys keisti darbuotojo padengimą. Gyvenimo įvykių tipai yra susieti su plano tipu. Pavyzdžiui, medicininio plano tipas gali leisti pakeitimus dėl gimimo ar įvaikinimo, arba dėl pasikeitusios šeimyninės padėties. Tačiau draudimo plano tipas gali neleisti jokių pakeitimų, kilusių dėl gyvenimo įvykių. Daugiau informacijos rasite [Gyvenimo įvykių tipų konfigūravimas](hr-benefits-setup-life-event-types.md).
- **Laukimo dienos ir laukimo laikotarpiai** – išmokų plane galima nustatyti padengimo laukimo laikotarpį. Pavyzdžiui, naujai pasamdytas darbuotojas gali užsiregistruoti į 401(k) tik po trijų mėnesių darbo. Šiuo atveju laukimo laikotarpis yra trys mėnesiai. Laukimo dienos yra naudojamos laukimo laikotarpiu, jei naujas registracijas galima apdoroti ir pateikti teikėjui tik konkrečią mėnesio dieną. Pavyzdžiui, jei 401(k) registracijos gali būti apdorojamos tik penkioliktą mėnesio dieną po trijų mėnesių darbo, nustatytas laukimo laikotarpis yra trys mėnesiai, o laukimo diena yra penkiolikta. Daugiau informacijos rasite [Laukimo dienų konfigūravimas](hr-benefits-setup-waiting-days.md) ir [Laukimo periodų konfigūravimas](hr-benefits-setup-waiting-periods.md).
- **Priežasčių kodai** – jie yra naudojami paaiškinti, kodėl darbuotojui gali keistis išmoka. Daugiau informacijos rasite [Priežasčių kodų nustatymas](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Išmokų planų nustatymas

Kai nustatote išmokų planą, prieš užregistruodami darbuotojus turite atlikti šiuos veiksmus:

- Priskirti išmokų laikotarpį.
- Pridėti padengimo parinktis.
- Nustatykite „galioja nuo” ir „galioja iki” datas **Bendra** skirtuke.
- Priskirti bent vieną tinkamumo taisyklę.
- Nustatykite **Leisti/tęsti registraciją** skirtuko **Nustatymas** lauke.

Daugiau informacijos apie tai, kaip nustatyti išmokų planus, rasite [Išmokų planų nustatymas](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Lanksčių kredito programų nustatymas (pasirinktinai)

Galite naudoti lanksčiųjų kreditų programas, kad užregistruotumėte darbuotojus išmokoms gauti, remiantis iš anksto nustatytu lanksčiųjų kreditų skaičiumi. Darbuotojai gali pasirinkti savo lanksčiųjų kreditų paskirstymą. Pavyzdžiui, jei darbuotojai jau yra apdrausti pagal sutuoktinio sveikatos draudimo planą, jiems nebūtina naudoti savo kreditų sveikatos draudimui. Todėl vietoj to, jie gali norėti naudoti kreditus kitoms išmokoms. Daugiau informacijos apie lanksčias kredito programas rasite [Lanksčių kredito programų nustatymas](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Reikalingos darbuotojo informacijos konfigūravimas

Tam, kad užregistruotumėte darbuotojus išmokoms gauti, jiems turite pateikti reikiamą informaciją. 

Darbuotojui turi būti priskirtos **pareigos**. Pareigos **gali** būti priskirtos darbuotojui darbuotojo **arba pareigų** puslapiuose **·**, atnaujinant darbuotojo **priskyrimą**. 

Tada darbuotojai turi būti įtraukti į pastoviosios atlyginimo dalies planą jų darbo pradžios datą arba gauti atlyginimo **sumą metiniu atlyginimu**. Prieš priskiriant Darbuotojui **pastoviąsias** atlyginimo dalis, pareigos **turi** būti priskirtos. 

> [!NOTE] 
> Pastoviosios **atlyginimo dalies pradžios** data negali būti prieš pareigų **priskyrimo datą**.

Taip pat, jei turite darbuotoją, kuris gauna papildomą atlyginimą kaip komisinius, **galite pridėti išmokų metinę** atlyginimo sumą iš darbuotojo įrašo. Personalo valdymo metu apibrėžiant padengimo sumas **bus naudojama** išmokų metinė atlyginimo suma, o ne pastoviosios **atlyginimo dalies metinė** suma. **Išmokų metinė alga** turi būti galiojanti nuo darbuotojo pradžios dienos arba nuo išmokos laikotarpio pradžios, priklausomai nuo to, kuri data yra naujausia. Tačiau tam, kad būtų galima priskirti metinį išmokų atlyginimą **, pareigų nėra**. Norėdami įgalinti atlyginimo **išmokų funkciją**, eikite į personalo **bendrinamų parametrų** puslapį, išmokų **valdymo skirtuke** . Numatyta, kad ši funkcija išjungta.

> [!IMPORTANT]
> Jei darbuotojui **įvesta ir pastovioji** **atlyginimo** dalis, ir išmokų metinė atlyginimo suma, **nustatant padengimo** sumas bus naudojamas išmokų metinis atlyginimas. Darbuotojo puslapio **skyriuje** Išsami įdarbinimo **informacija** turite pasirinkti vertę lauke Išmokos **mokėjimo dažnumas**.

## <a name="configure-optional-employee-information"></a>Papildomos darbuotojo informacijos konfigūravimas
Kai kuriate išmokų planą, naudojantį tarifus, pagrįstus lytimi arba amžiumi, turite įvesti darbuotojo gimimo datą ir lytį, kad būtų apskaičiuota išmokų savikaina.

## <a name="process-employees-to-determine-eligibility"></a>Darbuotojų apdorojimas tinkamumo nustatymui
Tam, kad darbuotojai galėtų būti įtraukti į planus, vykdomas tinkamumo apdorojimas, siekiant nustatyti, kuriems planams jie yra tinkami. Galite peržiūrėti tinkamumo proceso rezultatus proceso rezultatų **peržiūros programoje**. Daugiau informacijos rasite [Dalyvavimo tinkamumo apdorojimas](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Darbuotojai pasirenka planus naudodamiesi **darbuotojų savitarnos paslauga** (pasirinktinai)

Kai yra atidarytas aptarnavimas, darbuotojai pasamdyti naujai arba įvyksta gyvenimo įvykis, darbuotojai gali pasirinkti arba atnaujinti savo išmokas naudodamiesi **darbuotojų savitarnos paslauga**. Daugiau informacijos rasite [Darbuotojo savitarnos konfigūravimas](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Darbuotojo plano pasirinkimų patvirtinimas

Išmokos, kurias pasirenka darbuotojai, turi būti patvirtintos prieš tai, kai darbuotojai bus laikomi įtrauktais į jas. Išmokas taip pat galima pasirinkti darbuotojo vardu. Norėdami pasirinkti arba patvirtinti išmokas, puslapio **Darbuotojas** skirtuke **Išmokos** pasirinkite **Darbuotojų išmokų planai**. Norėdami pasirinkti arba patvirtinti išmokas keliems darbuotojams, naudokite **Darbuotojų išmokų planų masinis naujinimas** puslapį.

## <a name="life-event-processing-optional"></a>Gyvenimo įvykių apdorojimas (pasirinktinai)

Darbuotojo gyvenimo ciklo metu kiekvienas darbuotojas gali patirti įvairių gyvenimo įvykių, pavyzdžiui, santuoką, darbo pasikeitimus arba priklausomų asmenų ar naudos gavėjų pakeitimus. Norėdami naudoti gyvenimo įvykius, turite juos įgalinti **Bendrai naudojami personalo parametrai** puslapyje. Nustatykite gyvenimo įvykių tipus ir gyvenimo įvykių parinktis planų tipams.

Tam, kad galėtumėte apdoroti gyvenimo įvykius, turite būti bent vieną kartą paleidę atvirą registraciją per samdymo laiko intervalą. Jungtinėse Valstijose atvira registracija įprastai vyksta vieną kartą per metus. Už Jungtinių Valstijų ribų atvira registracija gali vykti samdymo metu. Gyvenimo įvykių apdorojimas nereikalauja, kad darbuotojai pasirinktų išmokų planą. Tačiau darbuotojai turi būti įtraukti į atviros registracijos apdorojimą. Daugiau informacijos ieškokite šiose temose:

- [Gyvenimo įvykių apdorojimas](hr-benefits-process-life-events.md)
- [Gyvenimo įvykių keitimų apdorojimas](hr-benefits-process-life-event-changes.md)
- [Gyvenimo įvykių tinkamumo apdorojimas](hr-benefits-process-life-event-eligibility.md)

Pasibaigus gyvenimo įvykio apdorojimui ir tol, kol laikotarpis yra atviras galiojimo įvykio registracijos laikotarpiui, darbuotojai gali pakeisti plano parinktis, kurios paveiktos gyvenimo įvykio. Administratoriai gali atlikti keitimus darbuotojų vardu. Pasibaigus registracijos laikotarpiui ir jokie nepatvirtinti plano tipai nėra susiję su gyvenimo įvykio operacija, operacija uždaroma.

Visi planai, kuriems daro poveikį gyvenimo įvykis, turi būti pasirinkti arba atmesti, o tada patvirtinti. Jei planas neparinktas, jo atsisakyta ir jis nėra patvirtintas, gyvenimo įvykio operacija neuždaroma.

Administratoriai gali rankiniu būdu uždaryti gyvenimo įvykio operaciją pagal tai, pasirinkdami ją, o tada pasirinkdami **Uždaryti**. Jei operacijoje yra nepatvirtintų planų ir administratorius nori jį uždaryti, gyvenimo įvykio sustabdymas gali apriboti tų planų redagavimus.

Uždarytų galiojimo laiko įvykių panaikinti negalima.

Administratoriai gali atidaryti operaciją iš naujo pagal laiką, pasirinkdami ją ir pasirinkdami Atidaryti iš **naujo**.

## <a name="rate-updates-optional"></a>Tarifų naujinimai (pasirinktinai)

Kartais išmokos dydis pasikeičia plano laikotarpiu. Norėdami atnaujinti į planą jau įtrauktų darbuotojų tarifus, privalote apdoroti tarifo pakeitimus. Daugiau informacijos rasite [Tarifo pakeitimų apdorojimas](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
