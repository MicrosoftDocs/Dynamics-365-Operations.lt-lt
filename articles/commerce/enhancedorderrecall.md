---
title: EKA operacija Atšaukti užsakymą
description: Šiame straipsnyje paaiškinamos funkcijų galimybės, kurios galimos pagerėjusių EKA užsakymų atšaukimo puslapių.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3723b40209ee1f8fb0ef77cb1ad52d123ff2a02f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869467"
---
# <a name="recall-order-operation-in-pos"></a>EKA operacija Atšaukti užsakymą

[!include [banner](includes/banner.md)]

**Užsakymo atšaukimo** veiksmas komercijos prekybos taške (POS) leidžia naujinti užsakymo paiešką ir filtravimo funkcijas bei su konkrečiu užsakymu susijusią informaciją. Ši funkcija pasiekiama 10.0.15 arba vėlesnės versijos „Commerce“.

Norėdami įgalinti šią funkciją, įjunkite funkciją **Patobulinta EKA operacija Atšaukti užsakymą** „Commerce Headquarters“ darbo srityje **Funkcijų valdymas**. Įjungę funkciją, apsvarstykite galimybę atnaujinti jūsų [ekrano maketus](pos-screen-layouts.md) EKA, kad pasinaudotumėte kai kuriomis pakitusiomis galimybėmis.

Operacijos **Atšaukti užsakymą** mygtuko konfigūracija leidžia organizacijoms diegti operaciją su iš anksto nustatytu rodiniu.

![Mygtukų tinklelio konfigūracija.](media/recallorderbuttongrid.png)

Toliau nurodytos galimos rodymo parinktys.
- **Nėra** – ši parinktis įdiegia operaciją be konkretaus rodinio. Kai vartotojas atidaro šios konfigūracijos operaciją, jis bus paragintas ieškoti užsakymų arba pasirinkti iš iš anksto nustatyto užsakymų filtro.
- **Užsakymai, kuriuos reikia įvykdyti** – kai naudotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kuriuos turi įvykdyti dabartinė naudotojo parduotuvė, sąrašą. Šie užsakymai sukonfigūruoti paėmimui parduotuvėje arba parduotuvės siuntimui ir šių užsakymų eilutės dar nebuvo paimtos ar supakuotos.
- **Užsakymai, kuriuos reikia paimti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti paėmimui vartotojo dabartinėje parduotuvėje, sąrašą.
- **Užsakymai, kuriuos reikia išsiųsti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti siuntimui iš vartotojo dabartinės parduotuvės, sąrašą.

Paleidus operaciją **Atšaukti užsakymą** EKA, jei rodinys sukonfigūruotas pagal parinktį **Nėra**, vartotojas galės ieškoti ir nuskaityti užsakymus vienu iš toliau pateiktų būdų.
- Nuskaityti užsakymo brūkšninius kodus. Šiuo atveju bus ieškoma atitikimų užsakymo numerio, kanalo nuorodos ir kvitų ID laukų.
- Norėdami naudoti filtravimo mechanizmą, kad būtų surasti užsakymai, atitinkantys filtro kriterijus, programų juostoje pasirinkite piktogramą **Ieškoti užsakymų** arba **Ieškoti ir filtruoti**.
- Pasirinkite iš iš anksto nustatyto filtro išplečiamajame meniu **Rodyti užsakymus** (užsakymus, kuriuos reikia įvykdyti, paimti arba išsiųsti).

![„RecallOrderMainMenu”.](media/recallordermain.png)

Pritaikius ieškos kriterijus, programoje bus rodomas atitinkančių pardavimo užsakymų sąrašas. Svarbu pažymėti, kad naudojant ieškos / filtro parinktis, nuskaityti užsakymai neturi būti susieti su dabartine naudotojo parduotuve. Šis ieškos procesas nuskaitys ir rodys visus kliento užsakymus, atitinkančius paieškos kriterijus, net jei užsakymas buvo sukurtas arba nustatytas įvykdyti kitoje parduotuvės /kanalo ar sandėlio vietoje.

![„RecallOrderDetail”.](media/orderrecalldetail.png)

Vartotojas gali pasirinkti sąrašo užsakymą, norėdamas peržiūrėti papildomą informaciją. Informacijos skydas dešiniajame ekrano krašte rodo konkrečią pasirinkto užsakymo informaciją, įskaitant užsakymo eilutės, pristatymo ir įvykdymo informaciją.

Programų juostoje vartotojas gali pasirinkti operaciją. Atsižvelgiant į užsakymo būseną, tam tikros operacijos gali būti neįjungtos.

- **Grąžinimas** – inicijuojamas bet kurio kliento užsakymo produktų, kuriems išrašyta SF, grąžinimo kūrimo procesas.

- **Atšaukti** – išduoda visą pasirinkto pardavimo užsakymo atšaukimą. Ši parinktis negalima užsakymams, inicijuojamiems skambučių centro kanalu, ir negali būti naudojama užsakymui iš dalies atšaukti.

- **Įvykdyti** – perkelia vartotoją į užsakymo įvykdymo puslapį, iš anksto filtruotą pagal pasirinktą užsakymą. Bus rodomos tik tos pasirinkto užsakymo eilutės, kurias vartotojo parduotuvė atidarė įvykdymui.

- **Redaguoti** – leidžia vartotojams atlikti pasirinkto kliento užsakymo keitimus. Užsakymus galima redaguoti tik [tam tikruose scenarijuose](customer-orders-overview.md#edit-an-existing-customer-order).

- **Paėmimas** – ši pasirinktis bus galima, jei užsakyme yra viena ar daugiau eilučių, kurias galima paimti esamoje naudotojo parduotuvėje. Ši operacija paleidžia paėmimo srautą, leidžiantį vartotojui pasirinkti produktus, kurie bus paimti, ir sukuria paėmimo pardavimo operaciją.

## <a name="add-notifications-to-the-recall-order-operation"></a>Pranešimų, skirtų užsakymo operacijai atšaukti, pridėjimas

Prireikus, 10.0.18 ir vėlesnėse versijose galima konfigūruoti EKA pranešimus ir tiesioginės plytelės įspėjimus, skirtus operacijai **Užsakymo atšaukimas**. Daugiau informacijos žr. skyriuje [Užsakymo pranešimų elektroniniame kasos aparate (EKA) rodymas](notifications-pos.md).  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
