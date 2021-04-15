---
title: Įdarbinti darbo kandidatai
description: Ši tema rodo, kaip įdarbinti kandidatus „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9259cfa78d65f36da653c807a66e291b3cb01c63
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802532"
---
# <a name="recruit-job-candidates"></a>Įdarbinti darbo kandidatai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Dynamics 365 Human Resources“ jums padeda valdyti įdarbinimo užklausas. Ji taip pat padeda jums be požymių perkelti darbo užklausas darbuotojams. Jei jūsų organizacija naudoja atskirą įdarbinimo paraišką, jūsų įdarbinimo procesas gali apimti šiuos žingsnius:

- Įveskite savo įdarbinimo užklausą žmogiškuosiuose ištekliuose.
- Gaukite kandidato nuorodas žmogiškuosiuose ištekliuose iš įdarbinimo parašikos.
- Užbaikite kandaidato patvirtinimo procesą žmogiškuosiuose ištekliuose.

Jei nenaudojate atskiros įdarbinimo parašikos, galite taip pat rankiniu būdu valdyti kandidatus žmogiškuosiuose ištekliuose.

>[!NOTE]
>Jei esate administratorius ar kūrėjas ir norite integruoti „Human Resources“ su trečiosios šalies įdarbinimo programa, žr. [Konfigūruoti „Dataverse“ integravimą](hr-admin-integration-common-data-service.md) ir [Konfigūruoti „Dataverse“ virtualias lenteles](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Galite taip pat surasti įdarbinimo integravimo programas [„AppSource“](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
> Pabandykite peržiūros funkciją integravimui su „LinkedIn Talent Hub“, žr. [integruoti su „LinkedIn Talent Hub“](hr-admin-integration-linkedin.md).

## <a name="enable-recruiting-requests"></a>Įjungti įdarbinimo užklausas

Jei norite pateikti įdarbinimo užklausas „Human Resources“, pirmiausia turite įjungti funkcijas **Žmogiškųjų išteklių bendrintuose parametruose**.

1. Darbo erdvėje **Personalo valdymas** rinkitės **Nuorodos**.

2. Skyriuje **Nustatymai**, Rinkitės **žmogiškųjų išteklių bendrinti parametrai**.

3. Skirtuke **Įdarbinimas** skyriuje **ĮDARBINIMAS**, nustatykite **Įjungti įdarbinimo užklausas** į **Taip**.

## <a name="add-a-recruiting-request-location"></a>Įtrauktei įdarbinimo užklausos vietą

Jei jūsų organizacija turi kelias vietas, galite įtraukti jas taip, kad besikreipiantys galėtų pasirinkti vietą, kruioje naujas įdarbinimas veiks. Vieta bus įtraukta į darbo skelbimą.

1. Paieškos juostoje įveskite **įdarbinimo užklausos vieta**.

2. Pasirinkite **Naujas**.

3. Laukelyje **Įdarbinimo užklausos vieta** įveskite vietos pavadinimą.

   ![Įtrauktei įdarbinimo užklausos vietą](./media/hr-recruit-0a-add-location.png)

4. **Aprašas** laukelyje įveskite vietos aprašą.

5. Skyriuje **Vietą**, rinkitės **Įtraukti**. Jei iššoka **Naujas adresas** įveskite adresą vietai.

   ![Įvesti adresą](./media/hr-recruit-0b-address.png)

6. Skyriuje **Kontaktinė informacija**, įveskite informaciją vietos kontaktui.

7. Pasirinkite **Įrašyti**.

## <a name="add-a-recruiting-request"></a>Įtrauktei įdarbinimo užklausą

Vadovai gali pateikti įdarbinimo užklausas žmogiškuosiuose ištekliuose. Jei naudojate atskirą įdarbinimo užklausą, šių žingsnių užbaigimas nusiųs įdarbinimo užklausą ir pradės įdarbinimo procesą toje paraiškoje. Kitu atveju, užbaikite šią procedūrą, kad pradėtumėte darbo eigą jūsų vidiniam įdarbinimo procesui.

1. Rinkitės **Darbuotojo savitarna**.

2. Rinkitės **Mano komanda** skirtuką.

3. pasirinkite **Prašyti įdarbinti**.

   ![Pradėti įdarbinimo užklausą](./media/hr-recruit-1-request-to-recruit.png)

4. Užbaikite **Aprašas**, **Darbas** ir **Apskaičiuota pradžios data** laukelius.

   ![Užbaikite įdarbinimo užklausą](./media/hr-recruit-2-request-to-recruit.png)

5. Pasirinkite **Tęsti**. Įdarbinimo užklausa rodoma jūsų vietai.

6. Skyriuje **Bendri**, pasirinkite įdarbintoją iš **Įdarbintojo** iškrentančio meniu ir pasirinkite vietą iš **Įdarbinimo užklausos vietos** iškrentančio meniu.

7. Skyriuje **Darbas**, pakeiskite visą būtiną informaciją ir rinkitės **Sukurti išsamią informaciją darbui**.

   ![Kuri išsamią informaciją iš užduoties](./media/hr-recruit-3-create-details-from-job.png)

   Likusi įdarbinimo prašymo dalis bus užpildyta nustatąja informacijas darbui, kurį įvedėte.

8. Skyriuje **Išorinis aprašas**, įveskite išorėje matomo darbo aprašą.

9. Skyriuje **Pareigos**, rinkitės **Įtraukti** ir tada pasirinkite darbą šiam įdarbinimo prašymui.

   ![Įtraukite pareigas](./media/hr-recruit-4-select-position.png)

10. Skyriuje **Įgūdžiai**, pasirinkite **Įtraukti** ir tada rinkitės įgūdžius.

11. Skyriuje **Išsilavinimo reikalavimai**, Rinkitės **Įtraukiti** ir tada rinkitės vertes iš **Išsilavinimas** ir **Išsilavinimo lygio** iškrentančių meniu.

   ![Įtraukti išsilavinimo reikalavimus](./media/hr-recruit-5-select-educational-requirements.png)

12. Skyriuje **Komentaras**, įtraukite komentarus, kaip būtina.

13. Skyriuje **Užmokestis**, pasirinkite iš iškrentančio meniu **Lygį** ir tad akeiskite **Apatinis slenkstis**, **Patikros taškas** ir **Viršutinis slenkstis** kaip būtina.

14. Kai jūsų jūsų įdarbinimo užklausa yra užbaigta ir esate pasirengęs pradėti įdarbinimo procesą, pasirinkite **Įjungti** meniu juostoje.

   ![Įjungti įdarbinimo užklausą](./media/hr-recruit-6-activate-recruit-request.png)

15. Pasirinkite **Įrašyti**.

## <a name="view-and-edit-your-recruiting-requests"></a>Peržiūrėti ir redaguoti jūsų įdarbinimo užklausas

Jei esate vadovas ir norite peržiūrėti savo turimas užklausas:

1. Rinkitės **Darbuotojo savitarna**.

2. Rinkitės **Mano komanda** skirtuką.

3. Skyriuje **Mano komandos informacija**, rinkitės skirtuką **Įdarbinimo užklausos**.

   ![Pasirinkite įdarbinimo užklausų skirtuką](./media/hr-recruit-7-recruiting-requests.png)

4. Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.

Jei esate žmogiškųjų išteklių profesionalas ir norite peržiūrėti visas įdarbinimo užklausas:

1. Rinkitės **Personalo valdymas**.

2. Pasirinkite **įdarbinimo užklausos**.

   ![Peržiūrėti įdarbinimo užklausas personalo valdyme](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.

## <a name="add-or-edit-a-candidate-profile"></a>Įtraukti ar redaguoti kandidato profilį

Jei jūsų organizacija integravo su kita programa siekiant valdyti įdarbinimo užklausas, įdarbinimo užklausos persiunčiamos tai programai. Įdarbinimo programa tada siunčia kandidato informaciją atgal žmogiškiesiems ištekliams. Kitu atveju, galite sekti savo turimus vidaus įdarbinimo procesus ir įvesti kandidato informaciją rankiniu būdu.

1. Rinkitės **Personalo valdymas**.

2. Pasirinkite **Nuorodos**.

3. Skyriuje **Įdarbinimas**, rinkitės **Kandidatai**.

   ![Peržiūrėti kandidatus](./media/hr-recruit-9-candidates.png)

4. Norėdami įtraukti kandidatą, rinkitės **Naujas**. Norėdami redaguoti esamą kandidatą, rinkitės jį iš sąrašo ir tada rinkitės **Redaguoti**. Rodomas kandidato profilis.

5. Skyriuje **Kandidato suvestinė**, įveskite ar redaguokite kandidato informaciją, kaip būtina.

6. Skyriuje **Įdarbinimo užklausa**, rinkitės įdarbinimo užklausą siekiant susieti su kandidatu. Tuomet užbaikite **Apskaičiuota pradžios data**, **Įdarbinimo vadovas**, **Pareigos** ir **Aprašymo laukeliai** kaip būtina.

   ![Susiekite su įdarbinimo užklausa](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Užbaikite visą informaciją tolesnėse srityse, kurias norite įtraukti į kandidato įrašą:
   - **Komentarai**
   - **Profesinė patirtis**
   - **Kontaktinė informacija**
   - **Išsilavinimas**
   - **Įgūdžiai**
   - **Sertifikatai**
   - **Atrankos**

8. Pasirinkite **Įrašyti**.

## <a name="hire-a-candidate"></a>Samdyti kandidatą

Kai esate pasirengę samdyti kandidatą, atlikite šią procedūrą siekiant perkelti kandidatą į darbuotoją.

1. Kandidato formoje rinkitės **Samdyti**.

   ![Samdyti kandidatą](./media/hr-recruit-11-hire.png)

2. Formoje **Samdyti naują darbuotoją** skyriuje **Išsami informacija**, užbaikite visus laukelius.

   ![Įveskite naujo įdarbinto asmens išsamią informaciją](./media/hr-recruit-12-hire-new-worker.png)

3. Skyriuje **Pareigų išsami informacija**, patikrinkite ir keiskite informaciją, kaip būtina.

4. Skyriuje **Įtraukti tikrinimo sąrašai**, pasirinkite atitinkamus įtrauktus tikrinimo sąrašus šiam darbuotojui.

5. Rinkitės **Tęsti** norėdami sukurti darbuotojo įrašą.

   >[!NOTE]
   >Priklausomai nuo jūsų organizacijos darbo eigų, kandidato įrašas gali praeiti pro papildomus patvirtinimo žingsnius prieš tai, kai taps darbuotojo įrašu.

## <a name="decide-not-to-hire-a-candidate"></a>Sprendimas nesamdyti kandidato

Jei nusprendžiate nesamdyti kandidato, laikykitės šios procedūros siekiant pašalinti jį iš vertinimo proceso. 

1. Kandidato formoje rinkitės **Nesamdyti**.

   ![Nesamdyti kandidato](./media/hr-recruit-13-do-not-hire.png)

2. Rinkitės **Priežasties kodą** ir įtraukite visus komentarus.

3. Pasirinkite **Gerai**.

## <a name="dismiss-a-candidate"></a>Atmesti kandidatą

Jei reikia, galite atmesti kandidatą po jo pasamdymo. Pavyzdžiui, kandidatas gali atsisakyti pasiūlymo arba nepasirodyti pirmąją dieną.

- Kandidato formoje rinkitės **Atmesti kandidatą**.

  ![Atmesti kandidatą](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Konfigūruokite „Dataverse“ virtualias lenteles](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Darbo jėgos organizavimas](hr-personnel-departments-jobs-positions.md)<br>
[Užduoties komponentų nustatymas](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
