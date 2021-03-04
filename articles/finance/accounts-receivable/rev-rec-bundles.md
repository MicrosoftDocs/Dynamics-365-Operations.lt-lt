---
title: Įplaukų pripažinimo grupavimai
description: Šioje temoje aprašomos grupavimo funkcijos, įtrauktos į įplaukų pripažinimo galimybę gautinose sumose. Grupavimas apima pirminę prekę ir keletą sudedamųjų prekių.
author: kweekley
manager: aolson
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: cf4d03c1a697259899c419ce084b35f4eddf13fe
ms.sourcegitcommit: bd53794cb94f8c1ce29a7d6102119a0975f155e3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142304"
---
# <a name="revenue-recognition-bundles"></a>Įplaukų pripažinimo grupavimai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos grupavimo funkcijos, įtrauktos į įplaukų pripažinimo galimybę gautinose sumose. Grupavimas apima pirminę prekę ir keletą sudedamųjų prekių. Pirminė prekė įvedama į pardavimo užsakymą, kad užsakymo įrašas būtų efektyvesnis. Tačiau tada ji išskaidoma į sudedamąsias prekes. Sudedamosios prekės bus nurodytos vidiniuose dokumentuose, pvz., važtaraščiuose. Tačiau išoriniuose dokumentuose bus nurodoma tik pirminė prekė.

> [!NOTE]
> „Microsoft Dynamics 365 Commerce“ kanalai, pavyzdžiui, internetiniai, elektroniniai kasos aparatai (EKA) ir skambučių centrai nepalaiko pripažinimo (įskaitant grupavimo funkciją). Tai taip pat apima Potencialių klientų ir grynųjų pinigų sprendimą, skirtą „Dynamics 365 Supply Chain Management“ ir „Dynamics 365 Sales“. Prekių, sukonfigūruotų naudoti įplaukų pripažinimą, negalima įtraukti į užsakymus ar operacijas, sukurtas „Commerce“ kanaluose arba Potencialių klientų ir grynųjų pinigų sprendime.

Jei norite nustatyti grupavimus, būtina įvesti konfigūracijos raktus įplaukų pripažinimui. Tačiau grupavimus galima naudoti, net jei įplaukų pripažinimas nėra nustatytas. Taip pat galima naudoti įplaukų pripažinimą, jei nėra nustatytas grupavimas. Jei nustatytas įplaukų pripažinimas, sudedamosios prekės apibrėžia įplaukų vertę ir įplaukų grafiką, naudojamą įplaukų pripažinimui arba atidėjimui, kai išrašoma pardavimo užsakymo SF.

Grupavimo nustatymas naudoja KS funkciją. Informaciją apie grupavimo prekių nustatymą žr. [Įplaukų pripažinimo nustatymas](revenue-recognition-setup.md). Jei pirminė prekė pažymėta kaip grupavimas, ji bus apdorota kitaip nei kitos KS prekės. Toliau pateiktas skirtumų sąrašas:

- Grupavimai turi būti išskleisti patvirtinus pardavimo užsakymą pardavimo užsakymo puslapio veiksmų srities skirtuke **Pardavimas** pasirenkant **Patvirtinti pardavimo užsakymą**. Grupavimo prekių negalima išskleisti „FastTab“ **Pardavimo užsakymo eilutės** meniu **Pardavimo užsakymo eilutė** srityje **Išskleisti** pasirenkant **KS eilutė**. Kitu atveju prekė bus naudojama kaip KS, o ne kaip grupavimas.
- Pardavimo užsakymas, kuriame yra sugrupuota prekė, turi būti patvirtintas prieš sukuriant važtaraštį arba SF.
- Kai grupavimas išskleidžiamas patvirtinant pardavimo užsakymą, pirminė prekė atšaukiama, jos vieneto kaina ir nuolaidos paskirstomos grupavimo sudedamosioms prekėms.
- Sudedamųjų prekių suma visada turi būti lygi pirminės prekės kainai. Todėl yra apribojimų laukuose, kuriuos galima atnaujinti arba pakeisti sudedamosiomis prekėmis. Pvz., vieneto kainos rankiniu būdu keisti negalima. Jos taip pat negalima keisti netiesiogiai priskiriant naujos kainos sutartį. Kad būtų išvengta naujos kainos sutarties, sudedamųjų prekių atsargų dimensijų keisti negalima.
- Kai spausdinamas išorinis dokumentas, pvz., pardavimo užsakymo patvirtinimas arba SF, spausdinama pirminė prekė, o ne sudedamosios prekės.

## <a name="bundles-on-sales-orders"></a>Pardavimo užsakymų grupavimai

Demonstracinė įmonė USMF apima šiuos grupavimo nustatymus. Atkreipkite dėmesį, kad visas įplaukų pripažinimo nustatymas, pvz., įplaukų grafikų nustatymas, buvo pašalintas iš prekių, kurie yra įtraukti į šį scenarijų.

**Pirminė prekė:** nešiojamųjų kompiuterių grupavimas

- **Sudedamoji prekė**: prekės 1000 kiekis 1
- **Sudedamoji prekė**: prekės S0021 kiekis 1
- **Sudedamoji prekė**: prekės Palaikymas kiekis 1

Sudedamųjų prekių *bazinė pardavimo kaina* yra pagrindinė komponentų nustatymo dalis. Bazinė pardavimo kaina apibrėžiama prekės „FastTab **Pardavimas**. Ji naudojama paskirstymo koeficientui skaičiuoti, kai pirminės prekės vieneto kaina yra paskirstoma sudedamosioms prekėms. Prekybos sutarties pardavimo kainos niekada nėra naudojamos šiuo tikslu.

Tolesnės bazinės pardavimo kainos apibrėžiamos sudedamosioms prekėms:

- **1000:** 1 900,00 $
- **S0021:** 150,00 $
- **Palaikymas:** 500,00 $

Įvedamas kliento US-004, „Cave Wholesales“, pardavimo užsakymas. Vienintelė įvedama eilutė, skirta nešiojamojo kompiuterio grupavimo prekei. Numatytąją pirminės eilutės vieneto kainą galima paimti iš daugelio vietų, pvz., prekybos sutarties arba bazinės pardavimo kainos. Šiame pavyzdyje 2 300 $ įvesta rankiniu būdu kaip vieneto kaina.

[![Nešiojamųjų kompiuterių grupavimo prekė pardavimo užsakyme](./media/bundle-01.png)](./media/bundle-01.png)

Kadangi pardavimo užsakyme yra grupavimas, jį reikia patvirtinti. Patvirtinimo dialogo lange rodomi grupavimo komponentai.

[![Dialogo langas Patvirtinti pardavimo užsakymą, kuriame pateiktos sudedamosios prekės](./media/bundle-02.png)](./media/bundle-02.png)

Tačiau išspausdintoje patvirtinimo ataskaitoje bus rodoma tik pirminė grupavimo prekė, nes ta ataskaita yra klientui skirtas išorinis dokumentas.

[![Patvirtinimo ataskaita, kurioje rodoma tik pirminė prekė](./media/bundle-03.png)](./media/bundle-03.png)

Patvirtinus pardavimo užsakymą, pirminė prekė vis dar rodoma pardavimo užsakyme, tačiau jos būsena pakeičiama į **Atšaukta**. Be to, grynoji suma sekama lauke **Grupavimo grynoji suma**. Šios sumos reikia norint išspausdinti SF, nes SF rodoma pirminė prekė, o ne sudedamosios prekės.

Sudedamųjų prekių suma turi būti lygi pirminės prekės **grupavimo grynosios sumos** vertei, nes ši vertė yra suma, kuri pateikiama klientui išspausdintoje SF. Siekiant užtikrinti, kad SF sutampa su DK užregistruotomis sumomis, ribojami sudedamųjų prekių redagavimai. Pvz., vietos ir sandėlio pakeisti negalima, nes dėl šių pakeitimų, remiantis prekybos sutartimi, gali pasikeisti kaina.

Pirminės prekės vieneto kaina iš eilutės paskirstoma komponentams tokiu būdu:

**Bendros bazinės pardavimo kainos iš komponentų:** 1 900 $ + 500 $ + 150 $ = 2 550 $

- **1 komponentas:** 2 300 $ × (1 900 ÷ 2 550) = 1 713,73 $
- **2 komponentas:** 2 300 $ × (500 ÷ 2 550) = 450,98 $
- **3 komponentas:** 2 300 $ × (150 ÷ 2 550) = 135,29 $

Komponentų suma turi būti lygi 2 300 $ ir ji tokia yra (1 713,73 $ + 450,98 $ + 135,29 $ = 2 300 $).

Jei pakeitimai būtini visome sudedamosioms prekėms, galima pašalinti pirminę prekę. Tokiu atveju sudedamosios prekės taip pat pašalinamos. Tada pirminę prekę galima įtraukti dar kartą, o būtinus redagavimus galima baigti prieš patvirtinant pardavimo užsakymą.

[![Grupavimo prekė, į kurią įtraukti sudedamųjų prekių pakeitimai](./media/bundle-04.png)](./media/bundle-04.png)

Kai pardavimo užsakymas paimtas ir supakuotas, dokumentuose bus įtraukti tik grupavimo komponentai. Į važtaraštį ir SF turi būti įtraukti visi grupavimai. Kitu atveju jų registruoti negalima. Pavyzdžiui, dialogo lange rodomos trys sudedamosios prekės. Jei bandysite panaikinti vieną iš jų, gausite klaidos pranešimą, kuriame teigiama, kad visi grupavimo produktai turi būti išsiųsti prieš išrašant SF.

Grupavimas turi būti išsiųstas ir jam išrašyta SF kaip visam grupavimui. Pavyzdžiui, jei keičiate prekės 1000 kiekį į 4, bet kitų sudedamųjų prekių kiekį paliekate kaip 5, važtaraščio ir SF registruoti negalima.

Dalinę sumą galima išsiųsti ir išrašyti SF tik tada, jei visų grupavimo komponentų kiekis yra sumažintas. Pavyzdžiui, pardavimo užsakyme įvedamas nešiojamojo kompiuterio grupavimo prekės kiekis 5. Patvirtinus pardavimo užsakymą, pardavimo užsakyme rodomos trys sudedamosios prekės, kurių kiekvienos kiekis yra 5. Pagal numatytuosius nustatymus, siuntimo ir SF išrašymo metu kiekvieno komponento kiekis bus nustatytas į 5. Tačiau visų trijų sudedamųjų prekių kiekį galima koreguoti iki 3. Tokiu atveju bus išsiųsti trys išsamūs grupavimai ir išrašyta SF. Likusios dvi grupavimo prekės (trijų sudedamųjų prekių 2 kiekis) gali būti išsiųstos vėliau ir išrašyta SF.

Paskutinis veiksmas yra pardavimo užsakymo SF išrašymas. SF išrašymo metu SF dialogo lange bus rodomos sudedamosios prekės.

[![Dialogo langas Sąskaita faktūra, kuriame pateiktos sudedamosios prekės](./media/bundle-06.png)](./media/bundle-06.png)

Tačiau išspausdintoje SF bus nurodoma tik pirminė prekė.
 
[![Išspausdinta SF, kurioje rodoma tik pirminė prekė](./media/bundle-07.png)](./media/bundle-07.png)

SF žurnale, kuris sukuriamas atlikus registravimą, neįtraukiama pirminė prekė iš grupavimo, nes tos prekės būsena yra **Atšaukta**.

[![SF žurnalas, kuris neapima pirminės prekės](./media/bundle-08.png)](./media/bundle-08.png)

Svarbu, kad į SF žurnalą nebūtų įtraukta pirminė prekė iš grupavimo, nes visi procesai, atliekami užregistravus SF, yra pagrįsti tuo SF žurnalu. Pavyzdžiui, jei veiksmų srities skirtuke **Pardavimas** sukursite kredito pažymą, sukurtoje kredito pažymoje bus sudedamosios prekės, tačiau ne pirminė prekė.

[![Kredito pažyma, kurioje rodomos sudedamosios prekės, tačiau ne pirminė prekė](./media/bundle-09.png)](./media/bundle-09.png)
