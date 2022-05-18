---
title: Įdarbinti darbo kandidatai
description: Šioje temoje aprašoma, kaip samdyti kandidatus Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef2f2c82708fd48055faa7546e7e0c4da51e7b6c
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733991"
---
# <a name="recruit-job-candidates"></a>Įdarbinti darbo kandidatai


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Dynamics 365 Human Resources“ jums padeda valdyti įdarbinimo užklausas. Ji taip pat padeda jums be požymių perkelti darbo užklausas darbuotojams. Jei jūsų organizacija naudoja atskirą įdarbinimo paraišką, jūsų įdarbinimo procesas gali apimti šiuos žingsnius:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- Įveskite savo įdarbinimo užklausą žmogiškuosiuose ištekliuose.
- Gaukite kandidato nuorodas žmogiškuosiuose ištekliuose iš įdarbinimo parašikos.
- Užbaikite kandaidato patvirtinimo procesą žmogiškuosiuose ištekliuose.

Jei nenaudojate atskiros įdarbinimo parašikos, galite taip pat rankiniu būdu valdyti kandidatus žmogiškuosiuose ištekliuose.

> [!NOTE]
> Jei jūs esate administratorius arba programuotojas ir norite integruoti Personalo duomenis į trečiosios šalies įdarbinimo prašymą, [eikite į Konfigūruoti Dataverse](hr-admin-integration-common-data-service.md) integravimą ir Konfigūruoti [virtualias Dataverse lenteles](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Galite taip pat surasti įdarbinimo integravimo programas [„AppSource“](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Įgalinti įdarbinimo užklausas susietos infrastruktūrose

Jei norite pateikti įdarbinimo užklausas personalo įdarbinimo srityje, pirmiausia **turite įgalinti personalo vartotojo** patirties ir įdarbinimo **proceso valdymo** priemones.

Kai priemonės įjungtos, pasirinkite funkcijas, atlikite šiuos veiksmus: 
1. Eiti į **Human resourcesSetupHuman** > **·** > **išteklių parametrus**.
2. Skirtuke  **Recruitment**  nustatykite lauką **Įdarbinimas išjungtas** kaip **Ne**.
3. Išplečiamajame **įdarbinimo patirties** sąraše pasirinkite Personalo **įdarbinimas**.   

> [!Note] 
> Pasirinkus **personalo įdarbinimą**, įdarbinimo **projektai** (iš senesni) bus tik skaitomi. 


## <a name="add-a-recruiting-request-location"></a>Įtrauktei įdarbinimo užklausos vietą

Jei jūsų organizacija turi kelias vietas, galite įtraukti jas taip, kad besikreipiantys galėtų pasirinkti vietą, kruioje naujas įdarbinimas veiks. Vieta bus įtraukta į darbo skelbimą.

1. Ieškos juostoje įveskite įdarbinimo **užklausos vietą**.
2. Pasirinkite **Nauja**.
3. Laukelyje **Įdarbinimo užklausos vieta** įveskite vietos pavadinimą.

    ![Įtraukti įdarbinimo užklausos vietą.](./media/hr-recruit-0a-add-location.png)

4. **Įveskite** vietos aprašymą.
5. Skyriuje **Vietą**, rinkitės **Įtraukti**. Jei atsiranda **naujo** adreso dialogo langas, įveskite vietos adresą.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Įvesti adresą.](./media/hr-recruit-0b-address.png)

6. Skyriuje **Kontaktinė informacija**, įveskite informaciją vietos kontaktui.
7. Pasirinkite **Įrašyti**.

## <a name="add-a-recruiting-request"></a>Įtrauktei įdarbinimo užklausą

Vadovai gali pateikti įdarbinimo užklausas žmogiškuosiuose ištekliuose. Jei naudojate atskirą įdarbinimo užklausą, šių žingsnių užbaigimas nusiųs įdarbinimo užklausą ir pradės įdarbinimo procesą toje paraiškoje. Kitu atveju, užbaikite šią procedūrą, kad pradėtumėte darbo eigą jūsų vidiniam įdarbinimo procesui.

1. Rinkitės **Darbuotojo savitarna**.
2. Rinkitės **Mano komanda** skirtuką.
3. Pasirinkite **Įdarbinimo užklausą**.

    ![Pradėti įdarbinimo užklausą.](./media/hr-recruit-1-request-to-recruit.png)

4. Užbaikite **Aprašas**, **Darbas** ir **Apskaičiuota pradžios data** laukelius.

    ![Užbaikite įdarbinimo užklausą.](./media/hr-recruit-2-request-to-recruit.png)

5. Pasirinkite **Tęsti**. Įdarbinimo užklausa rodoma jūsų vietai.
6. Išplečiamajame **įdarbinimo** sąraše pasirinkite **įdarbinėją**, **tada išplečiamajame sąraše Įdarbinimas pasirinkite** vietą.
7. Skyriuje **Darbas**, pakeiskite visą būtiną informaciją ir rinkitės **Sukurti išsamią informaciją darbui**.

    ![Kuri išsamią informaciją iš užduoties.](./media/hr-recruit-3-create-details-from-job.png)

    Likusi įdarbinimo užklausos dalis bus užpildyta numatytąja jūsų įvestos užduoties informacija.

8. Skyriuje **Išorinis aprašas**, įveskite išorėje matomo darbo aprašą.
9. Skyriuje **Pareigos**, rinkitės **Įtraukti** ir tada pasirinkite darbą šiam įdarbinimo prašymui.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Įtraukite pareigas.](./media/hr-recruit-4-select-position.png)

10. Skyriuje **Įgūdžiai**, pasirinkite **Įtraukti** ir tada rinkitės įgūdžius.
11. Dalyje **Išsilavinimo** reikalavimai pasirinkite **Įtraukti**, tada išplečiamajame meniu **Išsilavinimas** **ir Išsilavinimo lygis** pasirinkite vertes.

    ![Įtraukti išsilavinimo reikalavimus.](./media/hr-recruit-5-select-educational-requirements.png)

12. Skyriuje **Komentaras**, įtraukite komentarus, kaip būtina.
13. Dalies Atlyginimas išplečiamajame sąraše **Pasirinkite** lygį ir, jei reikia, koreguokite žemą **ribinę** vertę, **·** **kontrolės tašką ir aukštą slenkstį**.**·**
14. Kai jūsų jūsų įdarbinimo užklausa yra užbaigta ir esate pasirengęs pradėti įdarbinimo procesą, pasirinkite **Įjungti** meniu juostoje.

    ![Įjungti įdarbinimo užklausą.](./media/hr-recruit-6-activate-recruit-request.png)

15. Pasirinkite **Įrašyti**.

## <a name="view-and-edit-your-recruiting-requests"></a>Peržiūrėti ir redaguoti jūsų įdarbinimo užklausas

Jei esate vadovas ir norite peržiūrėti savo turimas užklausas:

1. Rinkitės **Darbuotojo savitarna**.
2. Rinkitės **Mano komanda** skirtuką.
3. Skyriuje **Mano komandos informacija**, rinkitės skirtuką **Įdarbinimo užklausos**.

    ![Pasirinkite įdarbinimo užklausų skirtuką.](./media/hr-recruit-7-recruiting-requests.png)

4. Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.

Jei esate žmogiškųjų išteklių profesionalas ir norite peržiūrėti visas įdarbinimo užklausas:

1. Rinkitės **Personalo valdymas**.
2. Pasirinkite **įdarbinimo užklausos**.

    ![Peržiūrėti įdarbinimo užklausas personalo valdyme.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.

## <a name="add-or-edit-a-candidate-profile"></a>Įtraukti ar redaguoti kandidato profilį

Jei jūsų organizacija integravo su kita programa siekiant valdyti įdarbinimo užklausas, įdarbinimo užklausos persiunčiamos tai programai. Įdarbinimo programa tada siunčia kandidato informaciją atgal žmogiškiesiems ištekliams. Kitu atveju, galite sekti savo turimus vidaus įdarbinimo procesus ir įvesti kandidato informaciją rankiniu būdu.

1. Rinkitės **Personalo valdymas**.
2. Pasirinkite **Nuorodos**.
3. Skyriuje **Įdarbinimas**, rinkitės **Kandidatai**.

    ![Peržiūrėti kandidatus.](./media/hr-recruit-9-candidates.png)

4. Norėdami įtraukti kandidatą, rinkitės **Naujas**. Norėdami redaguoti esamą kandidatą, rinkitės jį iš sąrašo ir tada rinkitės **Redaguoti**. Rodomas kandidato profilis.
5. Skyriuje **Kandidato suvestinė**, įveskite ar redaguokite kandidato informaciją, kaip būtina.
6. Skyriuje **Įdarbinimo užklausa**, rinkitės įdarbinimo užklausą siekiant susieti su kandidatu. Tada atitinkamai **užpildykite laukus** Įvertinta **pradžios data**, Samdos **vadybininkas**, **Pareigos** ir Aprašymas.

    ![Susiekite su įdarbinimo užklausa.](./media/hr-recruit-10-link-to-recruiting-request.png)

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

1. Kandidato **puslapyje** pasirinkti **Samdyti**.

    ![Samdyti kandidatą.](./media/hr-recruit-11-hire.png)

2. **Dalies Išsami informacija puslapyje** Samdyti naują **darbuotoją** užpildykite visus laukus.

    ![Įveskite naujo įdarbinto asmens išsamią informaciją.](./media/hr-recruit-12-hire-new-worker.png)

3. Skyriuje **Pareigų išsami informacija**, patikrinkite ir keiskite informaciją, kaip būtina.
4. Skyriuje **Įtraukti tikrinimo sąrašai**, pasirinkite atitinkamus įtrauktus tikrinimo sąrašus šiam darbuotojui.
5. Rinkitės **Tęsti** norėdami sukurti darbuotojo įrašą.

    > [!NOTE]
    > Priklausomai nuo jūsų organizacijos darbo eigų, kandidato įrašas gali pereiti per papildomus patvirtinimo veiksmus prieš tampant darbuotojo įrašu.

## <a name="decide-not-to-hire-a-candidate"></a>Sprendimas nesamdyti kandidato

Jei nusprendžiate nesamdyti kandidato, laikykitės šios procedūros siekiant pašalinti jį iš vertinimo proceso. 

1. Kandidato **puslapyje** pasirinkti **Nesamdyti**.

    ![Nesamdyti kandidato.](./media/hr-recruit-13-do-not-hire.png)

2. Rinkitės **Priežasties kodą** ir įtraukite visus komentarus.
3. Pasirinkite **Gerai**.

## <a name="dismiss-a-candidate"></a>Atmesti kandidatą

Jei reikia, galite atmesti kandidatą po jo pasamdymo. Pavyzdžiui, kandidatas gali atsisakyti pasiūlymo arba nepasirodyti pirmąją dieną.

- Kandidato puslapyje **pasirinkti atleidimo kandidatą** **.**

    ![Atmesti kandidatą.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Konfigūruokite „Dataverse“ virtualias lenteles](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Darbo jėgos organizavimas](hr-personnel-departments-jobs-positions.md)<br>
[Užduoties komponentų nustatymas](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
