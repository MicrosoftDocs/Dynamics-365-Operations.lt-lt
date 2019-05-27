---
title: Palūkanų ir mokesčių atsisakymas, grąžinimas arba atšaukimas
description: Šiame straipsnyje paaiškinama, kaip atsisakyti, grąžinti ir atšaukti mokesčius už palūkanas ir įmokas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfeab6f393b63b25d595067de3eb90fc899c508b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549178"
---
# <a name="waive-reinstate-or-reverse-interest-fees"></a>Palūkanų ir mokesčių atsisakymas, grąžinimas arba atšaukimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip atsisakyti, grąžinti ir atšaukti mokesčius už palūkanas ir įmokas.

Galite naudoti sąrašo puslapio **Visi klientai** skirtuke **Surinkimas** esančius mygtukus, norėdami atsisakyti mokesčių, juos atšaukti ar grąžinti.

-   Nuo atsisakytų mokesčių yra atleidžiama. Mokesčio galite atsisakyti, jei, pavyzdžiui, klientas nesutinka su mokesčiu, o jūs norite išlaikyti gerus verslo santykius su šiuo klientu.
-   Grąžinti mokesčiai apskaičiuojami dar kartą. Jūs galite grąžinti mokesčius, kurių anksčiau buvo atsisakyta. Gali reikėti grąžinti mokesčius, jei bus nustatyta, kad jų neturėjo būti atsisakyta.
-   Atšaukti mokesčiai yra pašalinami iš kliento sąskaitos ir jų nebereikia sumokėti. Mokesčius galite atšaukti, jei, pvz., neteisinga palūkanų norma buvo pasirinkta apskaičiuojant sumą, kurią klientas yra skolingas. Galite naudoti atskirą procesą, kad perskaičiuotumėte palūkanas ir sukurtumėte delspinigių pažymą, kurioje būtų nurodyti nauji klientui taikomi mokesčiai.

Atlikus visus šiuos veiksmus delspinigių pažyma pakeičiama. Delspinigių pažyma – tai verslo dokumentas, kuriame klientas informuojamas apie palūkanų arba mokesčių pritaikymo jo sąskaitoje datą. Kai atsisakote arba atšaukiate palūkanas arba mokesčius, kredito pažyma arba koregavimo sąskaita faktūra yra automatiškai sukuriama mokesčiams sudengti. Jei sugrąžinate atsisakytus mokesčius, automatiškai sukuriama sąskaita faktūra, kurioje nurodyta debeto suma, kad būtų grąžinti mokesčiai, kuriuos klientas yra skolingas. Toliau pateiktoje lentelėje aprašomi kiekvieno veiksmo rezultatai.

| Veiksmas                                                                                                                                                                                                            | Rezultatas klientui                                                                                             | Apdoroti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visiškai atsisakoma delspinigių pažymų ir į jas įtrauktų visų palūkanų ir mokesčių. –arba– Pasirenkama ir atsisakoma į delspinigių pažymas įtrauktų mokesčių arba palūkanų operacijų.                                        | Nuo mokesčių atleidžiama.                                                                                           | Kredito pažyma, arba koregavimo SF, sukuriama klientui. Kredito pažyma naudojama delspinigių pažymai arba pasirinktoms palūkanų operacijoms arba mokesčiams automatiškai sudengti. Sudengta suma lygi skirtumui, gaunamam iš bendros mokesčių sumos atėmus visų kliento anksčiau atliktų mokėjimų sumą bei visas anksčiau atsisakytas arba nurašytas sumas. Jei kredito pažymos suma viršija sumą, kurią klientas yra skolingas, galite konvertuoti kredito pažymą į tiekėjo sąskaitą faktūrą. Tada galite grąžinti lėšas klientui.                                                       |
| Visiškai grąžinamos delspinigių pažymos ir į jas įtrauktos visos palūkanos ir mokesčiai. –arba– Pasirenkama į delspinigių pažymas įtrauktų mokesčių arba palūkanų operacijų ir jos yra grąžinamos.                                | Atsisakyta suma vėl yra taikoma.                                                                                     | Sukuriama SF, kurioje nurodyta debeto suma, o suma automatiškai sudengiama pagal mokesčius, kurių anksčiau buvo atsisakyta. Faktinės delspinigių pažymos negrąžinamos. Vietoj to, sukuriama sąskaita faktūra, kurioje rodoma suma, kurią turi sumokėti klientas. Kredito pažymos arba koregavimo SF, kurios buvo sukurtos atsisakytoms delspinigių pažymoms sudengti, gali ir toliau išlikti, jei jos nebuvo naudojamos delspinigių pažymoms sudengti. Tokiu atveju neapmokėtos kredito pažymos yra atšaukiamos. Neapmokėtos kredito pažymos yra paprastai automatiškai sudengiamos, kai atsisakoma delspinigių pažymų. Tačiau neapmokėta kredito pažyma gali būti, jei kliento apmokėjo delspinigių pažymą, net jei klientas nesutiko su mokesčiais. |
| Visiškai atšaukiamos delspinigių pažymos. –arba– Atšaukiamos pasirinktos į delspinigių pažymas įtrauktos palūkanų operacijos. **Pastaba.** Negalite atšaukti mokesčio. Tačiau galite visiškai atšaukti delspinigių pažymą, į kurią įtrauktas mokestis. | Mokesčiai klientui daugiau nebegalioja. Tačiau mokesčiai įsigalios vėl, jei perskaičiuosite palūkanas. | Šis procesas sutampa su delspinigių pažymų arba pasirinktų palūkanų operacijų atsisakymo procesu. Kredito pažyma, arba koregavimo SF, sukuriama klientui. Ši kredito pažyma naudojama delspinigių pažymai automatiškai sudengti. Jūs galite naudoti atskirą procesą, kad perskaičiuotumėte palūkanas ir sukurtumėte naują delspinigių pažymą.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Galite naudoti ir atskirą procesą netinkamoms skoloms nurašyti. Vykdant šį procesą pažymimos visos kliento sudengimo operacijos, o nėra atsisakoma tik į delspinigių pažymas įtrauktų mokesčių.

## <a name="adjust-interest-for-invoices"></a>Koreguoti sąskaitų faktūrų palūkanas
Galite ne tik koreguoti delspinigių pažymas, bet ir naudodami kurį nors toliau nurodytą procesą pašalinti palūkanų mokesčius sąskaitose faktūrose. Vykdant šiuos procesus koreguojamos ir susijusios delspinigių pažymos.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Ištaisyti SF, kurioje nurodytos susietos palūkanos

Galite pataisyti užregistruotą SF, kuri įtraukta į delspinigių pažymą. Vykdant šį procesą nukopijuojama esamos SF informacija į naują SF, kad atliktumėte tik norimus pataisymus. SF atšaukiama ir sukuriama nauja SF. Operacijos palūkanos taip pat yra atšaukiamos delspinigių pažymoje, jei delspinigių pažyma užregistruota. 

Galite koreguoti naudodami laisvos formos SF veiksmų srities mygtuką **Taisyti SF**. Šį mygtuką galima naudoti tik pasirinkus konfigūracijos raktą **Laisvos formos SF taisymas**.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Atšaukti kliento operaciją, kurioje nurodytos susietos palūkanos

Jei sąskaita faktūra buvo netinkamai sukurta, joje galite atšaukti kliento operaciją. Jei atšauktoje kliento operacijoje nurodytos į delspinigių pažymą įtrauktos palūkanos, o delspinigių pažyma buvo užregistruota, operacijos palūkanos taip pat bus atšaukiamos delspinigių pažymoje. Jei delspinigių pažyma nebuvo užregistruota, ji bus atšaukta. 

Naudodami puslapio **Kliento operacijos** mygtuką **Atšaukti**galite atšaukti kliento operacijas.

## <a name="waive-or-reinstate-interest-notes"></a>Atsisakyti arba atkurti delspinigių pažymas
Galite atsisakyti visų pasirinktų delspinigių pažymų mokesčių arba juos grąžinti. Kai atsisakote mokesčių, bendroji atsisakymo suma negali viršyti jokių nustatytų sumos ribų. Delspinigių pažymą galite atkurti tik tada, jei jos buvo anksčiau atsisakyta. 

Naudodami puslapio **Klientas** skirtuko **Surinkimas** mygtuką **Delspinigių pažyma** galite atsisakyti delspinigių pažymų arba jas atkurti.

## <a name="waive-or-reinstate-interest-transactions"></a>Atsisakyti arba atkurti palūkanų operacijas
Delspinigių pažymoje galite atsisakyti konkrečių palūkanų operacijų arba jas atkurti ir nekoreguoti visų šios delspinigių pažymos mokesčių. Kai atsisakote mokesčių, bendroji atsisakymo suma negali viršyti jokių nustatytų sumos ribų. Palūkanų operaciją galite atkurti tik tada, jei jos buvo anksčiau atsisakyta. 

Naudodami puslapio **Klientas** skirtuko **Surinkimas** mygtuką **Operacijos palūkanos** galite atsisakyti delspinigių pažymų arba jas atkurti.

## <a name="waive-or-reinstate-fees"></a>Atsisakyti arba atkurti mokesčius
Delspinigių pažymoje galite atsisakyti konkrečių mokesčių arba juos grąžinti ir nekoreguoti visų šios delspinigių pažymos mokesčių. Kai atsisakote mokesčių, bendroji atsisakymo suma negali viršyti jokių nustatytų sumos ribų. Mokestį galite atkurti tik tada, jei anksčiau jo buvo atsisakyta. 

Naudodami puslapio **Klientas** skirtuko **Surinkimas** mygtuką **Mokestis** galite atsisakyti delspinigių pažymų arba jas atkurti.

## <a name="reverse-interest-notes"></a>Atšaukti delspinigių pažymas
Galite atšaukti visus pasirinktus delspinigių pažymų mokesčius. Atšaukti mokesčiai yra pašalinami iš kliento sąskaitos ir jų nebereikia sumokėti. Po to, kai delspinigių pažyma atšaukiama, gali perskaičiuoti palūkanas ir kurti naują delspinigių pažymą. 

Naudodami puslapio **Klientas** skirtuko **Surinkimas** mygtuką **Delspinigių pažyma**galite atšaukti delspinigių pažymas.

## <a name="reverse-interest-transactions"></a>Atšaukti palūkanų operacijas
Galite atšaukti visas pasirinktas palūkanų operacijas. Atšaukti mokesčiai yra pašalinami iš kliento sąskaitos ir jų nebereikia sumokėti. Po to, kai operacijos atšaukiamos, gali perskaičiuoti palūkanas ir kurti naują delspinigių pažymą.

Naudodami puslapio **Klientas** skirtuko **Surinkimas** mygtuką **Operacijos palūkanos** galite atšaukti palūkanų operacijas.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Peržiūrėti mokesčių, kurių buvo atsisakyta, kurie buvo atkurti arba atšaukti, koregavimų retrospektyvą
Peržiūrėkite išsamią retrospektyvą koregavimų, kurie buvo atlikti delspinigių pažymoms, pvz., vartotoją, kuris įvedė koregavimą, koregavimo tipą, sumą ir kada koregavimas buvo įvestas. Pavyzdžiui, galbūt norėsite peržiūrėti ankstesnius koregavimus, kurie buvo įvesti delspinigių pažymoje, prieš kurdami naują delspinigių pažymą. 

Naudodami puslapio **Klientas** skirtuko **Surinkimas** mygtuką **Retrospektyva**galite atšaukti palūkanų operacijas.



