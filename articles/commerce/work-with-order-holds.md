---
title: Skambučių centro užsakymo sulaikymo funkcijų konfigūravimas ir darbas su jomis
description: Šioje temoje aprašoma, kaip dirbti su užsakymo sulaikymo funkcijomis naudojant „Dynamics 365 Commerce“.
author: josaw1
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f474b5936f2ae154ad54185becd91865642e8efe3cf10e7dcdbb650c6c833b21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762601"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Skambučių centro užsakymo sulaikymo funkcijų konfigūravimas ir jų naudojimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos „Dynamics 365 Commerce“ užsakymo sulaikymo funkcijos, skirtos skambučių centro užsakymams.

## <a name="configuring-call-center-order-holds"></a>Skambučių centro užsakymo sulaikymo funkcijų konfigūravimas

Norėdami naudoti skambučių centro užsakymo sulaikymo funkcijas, pirmiausia turite apibrėžti sulaikymo kodus. Norėdami sukurti vartotojo apibrėžtų sulaikymo kodų rinkinį pagal savo verslo poreikius, eikite į **Pardavimas ir rinkodara** \> **Sąranka** \> **Pardavimo užsakymai** \> **Užsakymo sulaikymo kodai**. Galite pasirinktinai pažymėti vieną iš šių sulaikymo kodų kaip numatytąjį sulaikymo kodą nustatydami parinkties **Numatytasis pardavimo užsakymo nustatymas** parametrą **Taip**. Šis sulaikymo kodas bus naudojamas visada, kai sulaikomas pardavimo užsakymas. Jei pardavimo užsakyme yra rezervuotų atsargų ir rezervavimai turi būti automatiškai pašalinti, kai užsakymas sulaikomas dėl konkrečios priežasties, nustatykite priežasties kodų parinkties **Pašalinti atsargų rezervavimus** parametrą **Taip**.

Norėdami nurodyti pastabos, kuri bus įrašyta, kai pardavimo užsakymą sulaikantys vartotojai įves papildomų pastabų, tipą, eikite į **Gautinos sumos** \> **Sąranka** \> **Gautinų sumų parametrai**, tada „FastTab“ **Pardavimo sąrankos** skirtuke **Bendra** nustatykite lauką **Pastabos tipas**. Lauke **Sulaikyto pardavimo užsakymo būsena** nurodykite spalvą, kuria bus pažymėti sulaikyti pardavimo užsakymai, juos peržiūrint puslapyje **Klientų aptarnavimas**.

Norėdami sukurti pasirinktinį sulaikymo priežasčių kodų rinkinį, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo nustatymas** \> **Informacijos kodai**. Šiuos informacijos kodus galima naudoti kaip antrinį priežasties kodą, kuris papildomai apibūdina pagrindinį sulaikymo kodą. Pasirinkite **Naujas**, kad sukurtumėte priežasties kodų rinkinį, tada pasirinkite **Antriniai kodai**, kad apibrėžtumėte papildomų priežasčių sąrašą. Norėdami susieti bet kokius apibrėžtus informacijos kodus su skambučių centro kanalu, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalai** \> **Skambučių centrai** \> **Visi skambučių centrai**. „FastTab“ **Bendra** nustatykite lauką **Sulaikymo kodas**.

## <a name="putting-orders-on-hold"></a>Užsakymų sulaikymas

Užsakymus, kuriuos skambučių centro vartotojai sukuria naudodami operacijų skyriaus programą „Commerce“, galima sulaikyti rankiniu būdu arba automatiškai.

Įvesdami užsakymą, bet prieš atlikdami užsakymo pateikimo ir patvirtinimo veiksmus, skambučių centro vartotojai gali rankiniu būdu sulaikyti užsakymą, kad jis nebūtų išleistas toliau apdoroti į sandėlį. Pavyzdžiui, užsakymą pateikiantis klientas gali būti nepasiruošęs laikytis įsipareigojimų arba trūksta kritinių duomenų, kurių reikia užsakymui apdoroti.

Užsakymo įvedimo puslapyje skambučių centro vartotojas gali sulaikyti užsakymą naudodamas užsakymo įvedimo meniu skirtuko **Pardavimo užsakymas** parinktį **Užsakymo sulaikymas**. Taip pat vartotojas gali pasirinkti meniu elementą **Sulaikyti**, esantį puslapyje **Pardavimo užsakymo suvestinė**, kuris rodomas, kai vartotojas pasirenka skambučių centro pardavimo užsakymo parinktį **Baigti**.

Abiem atvejais rodomas puslapis **Užsakymo sulaikymai**. Tada vartotojas gali pasirinkti **Naujas**, kad sukurtų užsakymo sulaikymą. Lauke **Sulaikymo kodas** vartotojas turi pasirinkti kodą, kuris geriausiai apibūdina sulaikymo priežastį. Lauke **Priežasties kodas** vartotojas gali pasirinktinai pasirinkti papildomą kodą, kuris yra antrinio lygio sulaikymo aprašas.

„FastTab“ **Pastabos** lauke **Sulaikymo pastabos** vartotojas gali įvesti papildomų, laisvos formos pastabų, kad pateiktų papildomo konteksto arba informacijos apie sulaikymą. Šios pastabos gali padėti kitiems vartotojams, kurie vėliau peržiūrės ar dirbs su sulaikymo užsakymu.

Įvedęs ir įrašęs sulaikymo informaciją, vartotojas gali uždaryti puslapį **Užsakymo sulaikymai**. Tada vartotojas nukreipiamas atgal į pardavimo užsakymo įvedimo puslapį. Jei su pardavimo užsakymu nereikia atlikti jokių papildomų veiksmų, vartotojas gali uždaryti pardavimo užsakymo įvedimo puslapį.

Jei skambučių centro kanale pažymėta žymė **Įgalinti užsakymo baigimą**, mokėjimas neturi būti taikomas sulaikytam užsakymui. Tačiau jei pardavimo užsakymas nėra sulaikytas, vartotojai negali išeiti iš pardavimo užsakymo įvedimo puslapio, kol nebus pritaikytas mokėjimas. Žinoma, mokėjimas bus reikalingas prieš atšaukiant užsakymo sulaikymą.

Be to, skambučių centro vartotojai gali dėl kokios nors priežasties rankiniu būdu sulaikyti įtartinus užsakymus dėl galimos apgaulės. Užsakymai taip pat gali būti sulaikyti automatiškai, kai jie atitinka aktyvius apgaulės kriterijus ir taisykles. Daugiau informacijos apie šį užsakymo sulaikymo tipą žr. [Įspėjimų dėl apgaulės nustatymas](/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Sulaikytų užsakymų peržiūra ir tvarkymas

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Vieno pardavimo užsakymo sulaikymo informacijos peržiūra

Puslapyje **Klientų aptarnavimas** vartotojai gali vizualiai identifikuoti sulaikytus užsakymus, nes užsakymų eilutės yra paryškintos tam tikra spalva. Ši spalva nustatoma puslapio **Gautinų sumų parametrai** lauke **Sulaikyto pardavimo užsakymo būsena**.

> [!NOTE]
> Puslapyje pasirinkus eilutę, paryškinimo spalva nematoma.

Vartotojai taip pat gali peržiūrėti išsamią pardavimo užsakymo būsenos informaciją, kad sužinotų, ar užsakymas yra sulaikytas. Išsamią būsenos informaciją galima pasiekti puslapyje **Visi pardavimo užsakymai** arba **Klientų aptarnavimas**. Jei užsakymas sulaikytas, jam taikoma žymė **Neapdoroti** ir lauke **Išsami būsena** rodoma būsena **Sulaikyta** arba **Sulaikymas dėl apgaulės**, atsižvelgiant į atvejį.

Norėdami peržiūrėti išsamią atskiro užsakymo sulaikymo informaciją, vartotojai gali puslapyje **Klientų aptarnavimas** atidaryti išsamų puslapio **Užsakymo sulaikymas** rodinį, naudodami pasirinkto užsakymo meniu **Parinktys**. Vartotojai taip pat gali pasiekti šį rodinį puslapyje **Visi pardavimo užsakymai**, pasirinkdami skirtuko **Pardavimo užsakymas** meniu elementą **Užsakymo sulaikymai**.

### <a name="viewing-all-orders-that-are-on-hold"></a>Visų sulaikytų užsakymų peržiūra

Norėdami peržiūrėti visus užsakymus, kurie buvo sulaikyti rankiniu arba automatiniu būdu, eikite į **Mažmeninė prekyba ir prekyba** \> **Klientai** \> **Užsakymo sulaikymai**.

Darbo srityje **Užsakymo sulaikymai** pateikiamas visų užsakymų, kurie yra sulaikyti rankiniu būdu arba taikant su apgaule susijusius sulaikymo veiksmus, sąrašo rodinys. Puslapyje naudodami standartines filtravimo ir rūšiavimo parinktis, vartotojai gali kurti rodinius, kuriuose galės dirbti su konkrečiais sulaikymo kodais, kuriuos turi peržiūrėti. Darbo srityje **Užsakymo sulaikymai** taip pat rodomas dienų, kiek užsakymas yra sulaikytas, skaičius. Ši informacija gali padėti nustatyti prioritetus eilėje.

Norėdami gauti išsamesnį sulaikytų užsakymų rodinį, vartotojai gali spustelėti meniu parinktį **Užsakymo sulaikymas**. Šiame rodinyje pateikiama informacija apie klientą, bet kokios pastabos, taikomos užsakymui, klientui arba sulaikymo veiksmui. Rodinyje taip pat pateikiama informacijos apie automatinio sulaikymo priežastį, jei užsakymas buvo sulaikytas dėl to, kad atitiko apgaulės taisyklę.

Ir sąrašo rodinyje, ir išsamiame puslapio **Užsakymo sulaikymai** rodinyje vartotojai gali peržiūrėti arba redaguoti papildomą su užsakymu susijusią informaciją, pvz., mokėjimus, bendrąsias sumas ir pastabas.

Skirtuko **Sulaikyti pirkimo užbaigimą** parinktys gali praversti, jei vienu metu keli vartotojai jūsų įmonėje dirba su sulaikytų užsakymų eile. Pasirinkdami parinktį **Išregistruoti** vartotojai gali nurodyti, kad jie peržiūri ir analizuoja tą konkretų sulaikytą užsakymą. Tokiu būdu kiti vartotojai negaiš laiko bandydami padaryti tą patį darbą. Išsamiame puslapio **Užsakymo sulaikymai** rodinyje vartotojai gali peržiūrėti informaciją apie išregistravimo datą ir laiką bei vartotoją, kuris paėmė sulaikymo įrašą.

Išregistravus sulaikymo įrašą, išregistravimą gali atšaukti tik tas vartotojas, kuris tą įrašą išregistravo. Šis apribojimas padeda išvengti atvejų, kai vartotojai paima įrašus, su kuriais jau dirba kiti vartotojai. Norėdamas grąžinti užsakymą atgal į eilę, kad su juo galėtų dirbti kiti vartotojai, įrašą išregistravęs vartotojas turi pasirinkti parinktį **Valyti išregistravimą**.

> [!NOTE]
> Išvalius išregistravimą sulaikymas nėra atšaukiamas.

Kai kuriais atvejais, pvz., kai vartotojas serga arba paliko įmonę, įrašus, kuriuos išregistravo tas vartotojas, gali reikėti perskirti kitam vartotojui. Vadovas gali perskirti įrašus naudodamas parinktį **Perrašyti išregistravimą**.

## <a name="releasing-orders-that-are-on-hold"></a>Užsakymų sulaikymo atšaukimas

Sąrašo rodinyje ir išsamiame puslapio **Užsakymo sulaikymai** rodinyje esančiame skirtuke **Išvalyti sulaikymą** yra parinkčių, kurias naudojant galima atšaukti užsakymo sulaikymą. Naudodami parinktį **Išvalyti sulaikymą** atšaukite užsakymui taikomą pasirinktą sulaikymo kodą.

Skambučių centro užsakymai reikalauja mokėjimo. Todėl sulaikymo negalima visiškai išvalyti, jei užsakymui nepritaikytas mokėjimas. Puslapio **Skambučių centro parametrai** skirtuke **Sulaikymai** įjunkite parametrą **Pateikti išvalius**. Šis parametras padeda užtikrinti, kad užsakymas, kurio sulaikymas išvalytas, teisinga tvarka pereis pateikimo logikos procesą, kad būtų galima patvirtinti ir įgalioti mokėjimus. Jei mokėjimų nėra, vartotojui pateikiama klaida ir sulaikymo kodas nėra išvalomas.

Jei parametras **Pateikti išvalius** nenustatytas, vartotojai turi pasirinkti meniu **Išvalyti sulaikymą** parinktį **Valyti ir pateikti**, siekiant padėti užtikrinti, kad užsakymui būtų taikomi visi būtini mokėjimo patvirtinimo procesai. Jei užsakymo pateikti nepavyksta, kai skambučių centro kanale įjungta žymė **Įgalinti užsakymo baigimą**, užsakymo sulaikymo būsena yra panaikinta, bet liko nustatyta žymė **Neapdoroti**. Todėl užsakymas nebus išleistas į sandėlį, kol nebus pritaikyti ir patvirtinti tinkami mokėjimai.

Jei vartotojai nori išvalyti sulaikymą ir pakeisti užsakymą prieš jį išleisdami apdoroti toliau, jie gali pasirinkti parinktį **Valyti ir modifikuoti**. Naudojant šią parinktį pašalinamas sulaikymo kodas ir atidaroma išsami pardavimo užsakymo informacija, kad vartotojai galėtų atlikti papildomus užsakymo pakeitimus. Vartotojai taip pat gali taikyti mokėjimą ir pateikti pardavimo užsakymą naudodami mokėjimo patvirtinimo logiką, kai įjungta skambučių centro kanalo žymė **Įgalinti užsakymo baigimą**.

## <a name="reporting-options"></a>Ataskaitų parinktys

Eikite į **Mažmeninė prekyba ir prekyba** \> **Užklausos ir ataskaitos** \> **Skambučių centro ataskaitos** \> **Užsakymų sulaikymų ataskaita**, kad sugeneruotumėte ataskaitą apie sulaikytus užsakymus pagal datos diapazoną, sulaikymo kodą ar kitus susijusius kriterijus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]