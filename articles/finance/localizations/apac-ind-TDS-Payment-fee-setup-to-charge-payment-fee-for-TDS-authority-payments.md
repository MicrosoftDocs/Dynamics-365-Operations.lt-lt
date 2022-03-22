---
title: Nustatykite TDS įstaigos mokėjimų mokėjimo mokesčius
description: Šioje temoje paaiškinama, kaip nustatyti mokėjimo mokesčius, kurie taikomi šaltinio (TDS) valdžios institucijos mokėjimams.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1c17a00a9c62627e37533b43c38d94d57b00d1eb6c6b55de197dcd6d00d02db6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712200"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Nustatykite TDS įstaigos mokėjimų mokėjimo mokesčius

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti mokėjimo mokesčius, kurie taikomi šaltinio (TDS) valdžios institucijos mokėjimams.

1. Pasirinkite **Mokėtinos sumos \> Mokėjimų sąranka \> Mokėjimo mokestis**.

    [![Mokėjimo mokesčio puslapis.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Rinkitės **Nauja** norėdami sukurti mokėjimo mokestį ir įveskite reikiamą informaciją.
3. Lauke **Mokesčio tipas** pasirinkite mokesčio atributo tipą.

    - **None**
    - **Palūkanos** – skaičiuojamos pavėluotų mokėjimų, kurie atliekami TDS institucijos tiekėjui, palūkanos.
    - **Kiti** – skaičiuojamos kiti mokesčiai, kurie atliekami TDS institucijos tiekėjui, palūkanos.

    Jei pasirenkate **Palūkanos** arba **Kita**, laukas mokestis automatiškai **nustatomas** į **DK**.

4. Jei pasirinkote **Palūkanos** arba **Kita** lauke **Lauko tipas** laukelyje **Pagrindinė sąskaita** rinkitės DK, į kurią registruosite palūkanas ir kitas išlaidas.
5. Įveskite kitą reikiamą informaciją.
6. Veiksmų juostoje rinkitės **Mokesčio mokėjimo nustatymas** norėdami atverti **Mokesčio nustatymą** puslapį, kuriame galite nustatyti įvairių bankų, mokėjimo būdų, mokėjimo specifikacijų, valiutų ir datos intervalų mokėjimo mokesčius.

    [![Mokėjimo mokesčių puslapis.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Lauko **Grupavimai** skirtuke **Peržiūra** nurodykite, kuriems bankams nustatote mokėjimo mokestį:

    - **Lentelė** – mokestis taikomas konkrečiai banko sąskaitai.
    - **Grupė** – mokestis taikomas konkrečiai banko grupei.
    - **Visi** – Mokestis galioja visoms banko sąskaitoms.

8. Jei pasirinkote **Lentelė** ar **Grupė** lauke **Grupavimas** laukelyje **Banko ataskaita** pasirinkite konkrečią banko sąskaitą ar grupę, kurios mokėjimo mokestį nustatote.
9. Lauke **Mokėjimo būdas** pasirinkite dabartinio mokesčio mokėjimo būdą.
10. Mokėjimo specifikacijos **lauke pasirinkite** arba įveskite mokėjimo specifikacijos kodą, kuris buvo sugeneruotas **mokėjimo specifikacijos** puslapyje.
    - Mokėjimo specifikacija naudojama su elektroniniais mokėjimo lėšų pervedimo būdais.
12. Lauke **Mokėjimo valiuta** pasirinkite mokesčio valiutą, kuri įjungia mokestį. Tik operacijos, kurios naudoja pasirinktą valiutą, gali suaktyvinti mokestį. Jei paliksite šį lauką tuščią, mokestį suaktyvins visos valiutos.
13. Lauke **Procentai/suma** pasirinkite skaičiavimo metodą. Galimos pasirinktys: **Suma**, **Procentas** ir **Intervalas**.
14. Mokesčio **sumos lauke** nurodykite mokesčio sumą kaip mokėjimo procentą arba kaip vieno mokėjimo sumą.
15. Lauke **Mokesčio valiuta** nurodykite mokesčio valiutos kodą.
16. Pasirinkite skirtuką **Bendra**, norėdami peržiūrėti arba modifikuoti pasirinktos banko sąskaitos informaciją.

    [![Skirtukas Bendra.](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Lauke **Minimali** įveskite minimalią mokestį suaktyvinaą operacijos sumą.
17. Lauke **Maksimali** įveskite maksimalų mokestį suaktyvinaą operacijos sumą.
18. Laukuose **Nuo datos** ir **Iki datos** nurodykite mokesčių skaičiavimo datų diapazoną.
19. Mokesčio **Minimalus mokestis** nurodykite mokesčio sumą kaip mokėjimo procentą arba kaip vieno mokėjimo sumą.
20. Lauke **PVM grupė** pasirinkite PVM grupę, kurią naudosite skaičiuodami mokesčio sumos PVM.
21. Lauke **Prekės PVM grupė** pasirinkite prekės PVM grupę, kurią naudosite skaičiuodami prekės mokesčio sumos PVM.
22. Pasirinkite skirtuką **Intervalas**. 

    [![Skirtukas Intervalas.](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Laukelyje **Dienos** įveskite dienų tarp mokesčio registravimo datos (nuolaidos datos) ir paprastojo vekselio termino skaičių.
24. Lauke **Procentai/suma** pasirinkite ar specifikacija yra procentas, ar nustatyta suma.
25. Mokesčio **Mokesčio suma** įveskite mokesčio sumą kaip mokėjimo procentą arba kaip vieno mokėjimo sumą.
26. Uždarykite mokėjimo **mokesčio nustatymo** puslapį.
27. Uždarykite **mokėjimo mokesčio** puslapį.
