---
title: EKA operacija Atšaukti užsakymą
description: Šioje temoje paaiškinamos funkcijų galimybės, pasiekiamos patobulintuose užsakymų atšaukimo puslapiuose EKA.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42b11ff16757d633b868dfdf248341193a44378f
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665303"
---
# <a name="recall-order-operation-in-pos"></a>EKA operacija Atšaukti užsakymą

[!include [banner](includes/banner.md)]

**Užsakymo atšaukimo** veiksmas komercijos prekybos taške (POS) leidžia naujinti užsakymo paiešką ir filtravimo funkcijas bei su konkrečiu užsakymu susijusią informaciją. Ši funkcija pasiekiama 10.0.15 arba vėlesnės versijos „Commerce“.

Norėdami įgalinti šią funkciją, įjunkite funkciją **Patobulinta EKA operacija Atšaukti užsakymą** „Commerce Headquarters“ darbo srityje **Funkcijų valdymas**. Įjungę funkciją, apsvarstykite galimybę atnaujinti jūsų [ekrano maketus](pos-screen-layouts.md) EKA, kad pasinaudotumėte kai kuriomis pakitusiomis galimybėmis.

Operacijos **Atšaukti užsakymą** mygtuko konfigūracija leidžia organizacijoms diegti operaciją su iš anksto nustatytu rodiniu.

![Mygtukyno konfigūracija](media/recallorderbuttongrid.png)

Toliau nurodytos galimos rodymo parinktys.
- **Nėra** – ši parinktis įdiegia operaciją be konkretaus rodinio. Kai vartotojas atidaro šios konfigūracijos operaciją, jis bus paragintas ieškoti užsakymų arba pasirinkti iš iš anksto nustatyto užsakymų filtro.
- **Užsakymai, kuriuos reikia įvykdyti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kuriuos turi įvykdyti parduotuvė, sąrašą. Šie užsakymai sukonfigūruoti paėmimui parduotuvėje arba parduotuvės siuntimui ir šių užsakymų eilutės dar nebuvo paimtos ar supakuotos.
- **Užsakymai, kuriuos reikia paimti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti paėmimui vartotojo dabartinėje parduotuvėje, sąrašą.
- **Užsakymai, kuriuos reikia išsiųsti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti siuntimui iš vartotojo dabartinės parduotuvės, sąrašą.

Paleidus operaciją **Atšaukti užsakymą** EKA, jei rodinys sukonfigūruotas pagal parinktį **Nėra**, vartotojas galės ieškoti ir nuskaityti užsakymus vienu iš toliau pateiktų būdų.
- Nuskaityti užsakymo brūkšninius kodus. Šiuo atveju bus ieškoma atitikimų užsakymo numerio, kanalo nuorodos ir kvitų ID laukų.
- Norėdami naudoti filtravimo mechanizmą, kad būtų surasti užsakymai, atitinkantys filtro kriterijus, programų juostoje pasirinkite piktogramą **Ieškoti užsakymų** arba **Ieškoti ir filtruoti**.
- Pasirinkite iš iš anksto nustatyto filtro išplečiamajame meniu **Rodyti užsakymus** (užsakymus, kuriuos reikia įvykdyti, paimti arba išsiųsti).

![RecallOrderMainMenu](media/recallordermain.png)

Pritaikius ieškos kriterijus, programoje bus rodomas atitinkančių pardavimo užsakymų sąrašas.

![RecallOrderDetail](media/orderrecalldetail.png)

Vartotojas gali pasirinkti sąrašo užsakymą, norėdamas peržiūrėti papildomą informaciją. Informacijos skydas dešiniajame ekrano krašte rodo konkrečią pasirinkto užsakymo informaciją, įskaitant užsakymo eilutės, pristatymo ir įvykdymo informaciją.

Programų juostoje vartotojas gali pasirinkti operaciją. Atsižvelgiant į užsakymo būseną, tam tikros operacijos gali būti neįjungtos.

- **Grąžinti** – vykdo vienos ar daugiau SF, susijusių su pasirinktu kliento užsakymu, grąžinimą.

- **Atšaukti** – išduoda visą pasirinkto pardavimo užsakymo atšaukimą.

- **Įvykdyti** – perkelia vartotoją į užsakymo įvykdymo puslapį, iš anksto filtruotą pagal pasirinktą užsakymą. Bus rodomos tik tos pasirinkto užsakymo eilutės, kurias vartotojo parduotuvė atidarė įvykdymui.

- **Redaguoti** – leidžia vartotojams atlikti pasirinkto kliento užsakymo keitimus.

- **Paimti** – paleidžia paėmimo srautą, leidžiantį vartotojui pasirinkti produktus, kurie bus paimti, ir sukuria paėmimo pardavimo operaciją.


[!INCLUDE[footer-include](../includes/footer-banner.md)]