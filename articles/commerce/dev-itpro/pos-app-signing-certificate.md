---
title: Pasirašyti MPOS .appx failą su kodo pasirašymo sertifikatu
description: Šiame straipsnyje paaiškinama, kaip pasirašyti MPOS naudojant kodo pasirašymo sertifikatą.
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 7e998514081cad1c7302aacb1cd74373f896f2d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865974"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Pasirašyti MPOS .appx failą su kodo pasirašymo sertifikatu

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Norėdami įdiegti modernų EKA (MPOS) turite pasirašyti MPOS programą su patikimo tiekėjo kodo pasirašymo sertifikatu ir įdiegti tą patį sertifikatą visuose kompiuteriuose, kuriuose MPOS įdiegtas pagal patikimą dabartinio vartotojo šakninį aplanką.

Norėdami pasirašyti MPOS programą su sertifikatu, naudokite vieną iš šių parinkčių faile **Retail SDK\\Build tool\\Customization.settings**:

- Įtraukite saugių failų užduoties dalį į kūrimo Azure DevOps veiksmus ir įkelkite sertifikatą, kad apsaugotumėte failo užduotį. Naudokite saugaus failo užduoties išvesties maršruto kintamąjį kaip parametrą faile Customization.settings.

    > [!NOTE]
    > Saugos failo užduotis nepalaiko sertifikato, apsaugoto nuo slaptažodžio. Prieš įkeldami šią užduotį turite pašalinti slaptažodį. Kadangi sertifikatas įkeltas į saugių failų sistemos užduotį "Azure", slaptažodį galima pašalinti tik šio veiksmo metu. Tačiau reikėtų aptarti slaptažodžio pašalinimą su savo saugos ekspertais, kad nustatytumėte, ar tai teisingas jūsų projekto veiksmas. Pašalinkite kitų scenarijų sertifikato slaptažodį.
- Naudoti failų sistemoje yra sertifikatą. Norėdami tai padaryti, atsisiųskite arba sugeneruokite sertifikatą ir perkelkite jį į failų sistemą, kurioje veikia versija. "Microsoft" nuomojamas agentas arba kūrimo vartotojas turi turėti prieigą prie šio maršruto ir failo.
- Norėdami ieškoti parduotuvės sertifikato ir prisijungti naudodami šį sertifikatą, naudokite nykščio atspaudą.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Naudoti saugių failų užduotį universaliojo "Windows" platformos programos pasirašymui

> [!NOTE]
> Be to, "Azure Key Vault" galite saugoti sertifikatą ir naudoti "Azure" ženklo įrankį norėdami pasirašyti "Modern POS" ".appx" failą ir savitarnos diegimo programą. Pavyzdžio pardavimo galimybių scenarijų ir papildomos informacijos žr [. Pardavimo galimybių generavimas Azure DevOps siekiant sugeneruoti "Retail" savitarnos paketus](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Saugių failų užduoties naudojimas yra rekomenduojamas universaliosios Windows platformos (UWP) programos pasirašymo būdas. Norėdami gauti daugiau informacijos apie paketo pasirašymą, žr. Pakuotės [pasirašymo konfigūravimas](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Šis procesas rodomas toliau pateiktame paveikslėlyje.

![MPOS programos pasirašymo srautas.](media/POSSigningFlow.png)

> [!NOTE]
> Šiuo metu OOB pakuotė palaiko tik .appx failo pasirašymą, skirtingos savitarnos diegimo programos, pvz., MPOIS, PSTU ir HWS, nėra pasirašiusios šio proceso. Turite rankiniu būdu pasirašyti jį naudodami SignTool ar kitus pasirašymo įrankius. Sertifikatas, naudojamas .appx failui pasirašyti, turi būti įdiegtas kompiuteryje, kuriame įdiegtas "Modern POS".

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Registravimosi "Azure" pardavimo galimybėse sertifikato konfigūravimo veiksmai

### <a name="certificate-in-the-file-systemsecure-location"></a>Sertifikatas failų sistemos / saugioje vietoje

Atsisiųskite [DownloadFile](/visualstudio/msbuild/downloadfile-task) užduotį ir įtraukite ją kaip pirmą kūrimo proceso veiksmą. Saugių failų užduoties naudojimo pranašumas yra tai, kad kuriant failas yra užkoduojamas ir įdedamas į diską, nesvarbu, ar kurti pardavimo galimybes pavyko, ar ne, arba yra atšauktas. Baigus kūrimo procesą failas panaikinamas iš atsisiuntimo vietos.

1. Atsisiųskite ir pridėkite saugaus failo užduotį kaip pirmą "Azure" pardavimo galimybių kūrimo veiksmą. Galite atsisiųsti saugaus failo užduotį iš [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
1. Įkelkite sertifikatą į saugiojo failo užduotį ir nustatykite nuorodos pavadinimą išvesties kintamieji, kaip parodyta toliau pateiktame paveikslėlyje.
    > [!div class="mx-imgBorder"]
    > ![Failo saugos užduotis.](media/SecureFile.png)
1. Sukurkite naują "Azure" pardavimo galimybių kintamąjį skirtuke **Kintamieji** **pasirinkdami Naujas kintamasis**.
1. Vertės lauke pateikite kintamojo pavadinimą, pvz., **MySigningCert**.
1. Įrašyti kintamąjį.
1. Atidarykite **customization.settings** **failą iš RetailSDK\\BuildTools** **ir atnaujinkite ModernPOSPackageCertificateKeyFile** kintamojo pavadinimu, sukurtu pardavimo galimybėse (3 veiksmas). Pvz.:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Šis veiksmas būtinas, jei sertifikatas nėra apsaugotas slaptažodis. Jei sertifikato slaptažodis apsaugotas, atlikite nurodytus veiksmus.
    
1. Jei norite laiko žymę MPOS .appx failui pasirašyti su sertifikatu, **atidarykite "Retail SDK\\ Build tool\\ Customization.settings** **" failą ir atnaujinkite "ModernPOSPackageCertificateTimes" kintamąjį** laiko žymos teikėju (pvz., `http://timestamp.digicert.com`).
1. Pardavimo galimybių kintamųjų **skirtuke** pridėkite naują saugiojo teksto kintamąjį. Nustatykite pavadinimą **MySigningCert.secret** ir nustatykite sertifikato slaptažodžio vertę. Pasirinkti užrakto piktogramą kintamajam apsaugoti.
1. Į pardavimo **galimybes įtraukite "** Powershell" scenarijaus užduotį (po atsisiuntimo saugio failo ir prieš kūrimo veiksmą). Pateikite **rodomą** pavadinimą ir nustatykite tipą kaip **eilučių skaičių**. Į scenarijaus skyrių nukopijuokite ir įklijuokite toliau nurodytus dalykus.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Atidarykite **customization.settings** **failą iš RetailSDK\\BuildTools** **ir atnaujinkite ModernPOSPackageCertificateThumbprint** sertifikato nykščio atspaudo reikšmę.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Informacijos apie tai, kaip gauti sertifikato nykščio atspaudą, ieškokite [nuskaitykite sertifikato nykščio atspaudą](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Atsisiųskite arba sugeneruokite sertifikatą, norėdami pasirašyti MPOS programą rankiniu būdu, naudodami msbuild SDK

Jei atsisiųstas arba sugeneruotas sertifikatas naudojamas MPOS programai pasirašyti, **tada atnaujinkite mazgą ModernPOSPackageCertificateKeyFile** **, nurodytą BuildTools\\ Customization.settings faile**, kad būtų galima nurodyti pfx failo vietą (**$(SdkReferencesPath)\\ appxsignkey.pfx**). Pvz.:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

Šiuo atveju sertifikato failo vardas yra **appxsignkey.pfx**, esantis mažmeninės **prekybos SDK\\Reference** aplanke.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Naudoti nykščio atspaudą MPOS programai pasirašyti

Jei naudojate nykščio atspaudą MPOS programai pasirašyti, įdiekite sertifikatą vietoje. Atnaujinkite nykščio atspaudo vertę failo **BuildTools\\Customization.settings** mazge **ModernPOSPackageCertificateThumbprint**.

Ši pasirinktis veiks, jei kūrimo vartotojas yra vietinis vartotojas. Tačiau jei Azure DevOps naudojate agentus generuoti versiją, agentui gali būti taip, kad jis neturi teisės pasiekti parduotuvės, kad galėtų naudoti sertifikatą pasirašymui arba sukurtai mašinai nebus įdiegtas sertifikatas. Šiuo atveju problemos sprendimas yra pakeisti kūrimo vartotoją į vietinį vartotoją ir įdiegti sertifikatą lange. Tačiau, ši parinktis neveikia, jei neturite administratoriaus prieigos prie lango.

> [!NOTE]
> Jei .pfx failo arba saugaus failo užduoties parinktis naudojama programai pasirašyti, **tada Customization.settings palikite ModernPOSPackageCertificateThumbprint** **mazgą.parametrai tušti**. Jei naudojama nykščio atspaudo parinktis **, tada ModernPOSPackageCertificateKeyFile palikite tuščią**. Jei atnaujinamos abi vertės, nepavyks sukurti.

### <a name="certification-renewal"></a>Sertifikavimo atnaujinimas

### <a name="renew-a-certificate-from-trusted-ca"></a>Atnaujinti sertifikatą iš patikimo CA

Kreipkitės į savo sertifikavimo instituciją (CA) dėl sertifikato atnaujinimo proceso. Norint sukurti patikimą sertifikatą, MPOS pusėje nereikia jokių veiksmų.

### <a name="renew-a-self-signed-certificate"></a>Atnaujinti pasirašantį sertifikatą

Nenaudokite pavyzdžio sertifikato, prieinamo "Retail" SDK gamybai. Gali būti naudojama tik kūrimo tikslais. "Contoso" sertifikato pavyzdžio atnaujinti negalima, o pavyzdžio sertifikato, įtraukto į "Retail SDK" 10.0.16 ar ankstesnę versiją, galiojimas baigsis 2020 m. gruodžio 31 d. Jei šis sertifikatas arba pasirašytasis sertifikatas buvo naudojamas pasirašyti pritaikytą "Modern POS", gali būti, kad po šios datos "Modern POS" tinkamai neveiks.
 
### <a name="impact"></a>Poveikis
 
Jei tai galioja jums, problema, kuri jums bus skirta, yra ta, kad diegimo programa negalės veikti po 2020 m. gruodžio 31 d. Atsižvelgiant į naudojamas įmonės IT strategijas, "Modern POS" gali nepavykti veikti. Labai svarbu, kad tai išbandykite pakeisdami datą laikinai į būsimą datą, kad nustatytumėte poveikį jūsų organizacijai.
 
### <a name="steps-to-determine-the-issue"></a>Veiksmai išdavimui nustatyti
 
1.  Norėdami pakeisti kompiuterio atėjimo į darbą datą ir laiką 2021 metais, naudokite Windows parametrus.
2.  Patikrinkite, ar galima atidaryti modernų EKA, prisijungti ir užbaigti operaciją.
3.  Patikrinkite, ar modernaus EKA savitarnos diegimo pavyko paleisti ir ar taip, kad diegimas bus sėkmingai baigtas.
4.  Grąžinti teisingą Windows laikrodžio parametrų datą ir laiką.
 
Jei visus šiuos veiksmus galite atlikti be išdavimo, galėsite dirbti su dabartiniu sertifikatu, kuris buvo 2020 m. gruodžio 31 d.  
 
### <a name="steps-going-forward"></a>Žingsniai į priekį 

Rekomenduojama atnaujinti anksčiau naudotą sertifikatą. Primygtinai rekomenduojame įsigyti naują sertifikatą. Norėdami tai padaryti, turite atlikti vieną iš toliau nurodytų veiksmų.
 
- **Pageidaujama –** gauti kodo pasirašymo sertifikatą iš patikimo sertifikato institucijos.

- **Nepalaikomas –** sugeneruokite pasirašy tikrą kodo pasirašymo sertifikatą, kurį reikia naudoti. Ši informacija paprastai naudojama tik kūrimo domene tikslais, ir gamybai nerekomenduojama. 

- **Galimas kaip laikinas sprendimas – naudokite** atnaujintą "Contoso" kodo pasirašymo sertifikatą. Paprastai naudojama bandymo tikslais, todėl nerekomenduojama jo įdiegti gamyboje.
 
Tada sugeneruokite naują pritaikytą "Modern POS" paketą, pasirašytą naudojant šį sertifikatą, gautą iš vieno iš anksčiau nurodytų veiksmų. Atsižvelgiant į sertifikatą turi būti sekamas vienas iš šių veiksmų:
 
- Jei naudojate naują, patikimą sertifikatą (arba naują, pasirašymą) sertifikatą, jums reikės kiekviename įrenginyje įdiegti naują sertifikatą. Po to turite imtis naujai sukurto "Modern POS" paketo (diegimo programos), pašalinti esamą programą ir iš naujo įdiegti naują "Modern POS" paketą. Naudojant kiekvieną įrenginį reikės aktyvinti įrenginį ir naudoti "Modern POS".

- Jei naudojate atnaujintą "Contoso" sertifikatą, reikės įdiegti naują sertifikatą kiekviename įrenginyje ir įdiegti "Modern POS" paketą (diegimo priemonė). Jums nereikia pašalinti, tačiau turite iš naujo įdiegti įrenginį. Atkreipkite dėmesį, kad "Modern POS" įrenginio aktyvinimas nereikalaujamas. Ši pasirinktis yra laikinas sprendimas. Naudokite šią pasirinktį tik norėdami išvengti suaktyvinimo iš naujo ir išspręsti problemą prieš gaunant naują patikimą sertifikatą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
