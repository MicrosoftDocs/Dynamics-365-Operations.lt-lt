---
title: Įtraukti duomenų laukus į mokesčių integravimą naudojant plėtinius
description: Šioje temoje paaiškinama, kaip naudoti X++ plėtinius norint įtraukti duomenų laukus į mokesčių integravimą.
author: qire
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: acbe8070424febf24883362448ea56857d9d72d9
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323578"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Įtraukti duomenų laukus į mokesčių integravimą naudojant plėtinį

[!include [banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip naudoti X++ plėtinius norint įtraukti duomenų laukus į mokesčių integravimą. Šiuos laukus galima išplėsti iki mokesčių tarnybos mokesčių duomenų modelio ir naudoti mokesčių kodams nustatyti. Daugiau informacijos ieškokite Mokesčių [konfigūracijų duomenų laukų](tax-service-add-data-fields-tax-configurations.md) įtraukimas.

## <a name="data-model"></a>Duomenų modelis

Duomenų modelio duomenis vykdo objektai ir su įdiegė klasės.

Toliau pateiktas pagrindinių objektų sąrašas:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Šioje iliustracijoje parodyta, kaip šie objektai yra susiję.

[![Duomenų modelio objekto ryšys.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Dokumento **objekte** gali būti **daug eilutės** objektų. Kiekviename objekte yra mokesčių tarnybos metaduomenys.

- `TaxIntegrationDocumentObject` yra `originAddress` metaduomenų, kuriuose yra informacijos apie šaltinio adresą ir `includingTax` metaduomenis, kurie nurodo, ar eilutės suma apima PVM.
- `TaxIntegrationLineObject` yra `itemId`, `quantity` ir `categoryId` metaduomenys.

> [!NOTE]
> `TaxIntegrationLineObject` taip pat įdiegia **mokesčio** objektus.

## <a name="integration-flow"></a>integravimo eiga

Srauto duomenis valdo veikla.

### <a name="key-activities"></a>Pagrindinės veiklos

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Veiklos yra paleidžiamos tokia tvarka:

1. Nustatomas nuskaitimas
2. Duomenų nuskaitymas
3. Skaičiavimo tarnyba
4. Valiutos kursas
5. Duomenų pastovumas

Pavyzdžiui, **pratęskite duomenų** nuskaitymą prieš skaičiavimo **paslaugas**.

#### <a name="data-retrieval-activities"></a>Duomenų gavimo veiklos

**Duomenų** nuskaityme nuskaitomi duomenys iš duomenų bazės. Skirtingų operacijų adapterius galima nuskaityti duomenis iš skirtingų operacijų lentelių:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

Šiose duomenų **nuskaityme** duomenys kopijuojami iš duomenų bazės į `TaxIntegrationDocumentObject` ir `TaxIntegrationLineObject`. Kadangi visos šios veiklos išplečia tą pačią abstrakčią šablono klasę, jos turi bendrus metodus.

#### <a name="calculation-service-activities"></a>Apskaičiavimo paslaugų veikla

Skaičiavimo **paslaugos veikla yra sąsaja tarp mokesčių tarnybos ir mokesčių** integravimo. Ši veikla yra atsakinga už šias funkcijas:

1. Kurti užklausą.
2. Užregistruokite užklausą mokesčių tarnybai.
3. Gauti atsakymą iš mokesčių tarnybos.
4. Atmesti atsakymą.

Duomenų laukas, kurį įtraukiate į užklausą, bus registruojamas kartu su kitais metaduomenimis. 

## <a name="extension-implementation"></a>Plėtinio diegimas

Šiame skyriuje pateikiami išsamūs veiksmai, paaiškinays, kaip įdiegti plėtinį. Jis naudoja išlaidų **centrą ir projekto finansines** **dimensijas** kaip pavyzdžius.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>1 veiksmas. Įtraukti duomenų kintamąjį į objektų klasę

Objekto klasėje yra duomenų kintamųjų ir getterių/seter metodų. Priklausomai nuo lauko lygio, `TaxIntegrationDocumentObject` duomenų ar `TaxIntegrationLineObject`, lauką įtraukite į jį arba į jį. Toliau pavyzdyje naudojamas eilutės lygis, o failo vardas `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Jei duomenų laukas, kurį pridedate, yra dokumento lygyje, pakeiskite failo vardą į `TaxIntegrationDocumentObject_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**Išlaidų centras** ir projektas įtraukiami kaip privačios **kintamieji**. Sukurkite šių duomenų laukų getterio ir nustatymo metodus duomenims valdyti.

### <a name="step-2-retrieve-data-from-the-database"></a>2 veiksmas. Nuskaityti duomenis iš duomenų bazės

Nurodykite operaciją ir pratęskite atitinkamas adapterio klases, kad gautumėte duomenis. Pavyzdžiui, jei naudojate pirkimo užsakymo **operaciją**, turite išplėsti `TaxIntegrationPurchTableDataRetrieval` ir `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` yra paveldėta iš `TaxIntegrationPurchTableDataRetrieval`. Jos keisti negalima, nebent skiriasi `purchTable` lentelių ir lentelių `purchParmTable` logika.

Jei duomenų laukas turi būti pridėtas prie visų operacijų, išplėskite visas `DataRetrieval` klases.

Kadangi visos **duomenų** nuskaitymos veiklos išplečia tą pačią šablono klasę, klasių struktūros, kintamieji ir metodai yra panašūs.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

Šiame pavyzdyje parodyta pagrindinė struktūra, `PurchTable` kai naudojama lentelė.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

`CopyToDocument` Iškvietus metodą, `this.purchTable` buferis jau yra. Šio metodo paskirtis yra kopijuoti visus reikiamus duomenis iš objekto naudojant klasėje sukurtą `this.purchTable` į `document` `DocumentObject` metodą.

Taip pat šis metodas `this.purchLine` jau yra `CopyToLine` buferis. Šio metodo paskirtis yra kopijuoti visus reikiamus duomenis iš objekto naudojant klasėje sukurtą `this.purchLine` į `_line` `LineObject` metodą.

Pats tiesiausias būdas yra išplėsti `CopyToDocument` ir `CopyToLine` metodus. Tačiau pirmiausia rekomenduojame išbandyti `copyToDocumentFromHeaderTable` ir `copyToLineFromLineTable` metodus. Jei jie neveikia taip, kaip jums reikia, įtinkite savo metodą ir iškieskite `CopyToDocument` ir `CopyToLine`. Yra trys bendrosios situacijos, kuriose galite naudoti šį būdą:

- Būtinas laukas yra `PurchTable` arba `PurchLine`. Tokiu atveju galite išplėsti `copyToDocumentFromHeaderTable` ir `copyToLineFromLineTable`. Čia yra pavyzdžio kodas.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- Reikalaujami duomenys nėra numatytoje operacijos lentelėje. Tačiau kai kurie ryšiai su numatytąja lentele yra sujungti, o lauką reikia naudoti daugelyje eilučių. Tokiu atveju pakeiskite lentelę `getDocumentQueryObject` arba `getLineObject` pateikite užklausą dėl ryšio sujungtų ryšių. Šiame pavyzdyje laukas **Pristatyti dabar yra** integruotas su pardavimo užsakymu eilutės lygiu.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    Šiame pavyzdyje `mcrSalesLineDropShipment` buferis paskelbiamas ir užklausa apibrėžiama `getLineQueryObject`. Užklausa naudoja `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`ryšį. Kol išplečiate šią situaciją, galite pakeisti savo `getLineQueryObject` sudaryti užklausos objektą. Tačiau atminkite tolesnius taškus:

    * Kadangi yra metodo grąžinama `getLineQueryObject` vertė, turite `SysDaQueryObject` sudaryti šį objektą naudodami SysDa būdą.
    * Negalima pašalinti buvusios lentelės.

- Reikiami duomenys sudėtingu sujungimo ryšiu yra susiję su operacijų lentele arba ryšys nėra vienas su vienu (1:1), o su daugeliu (1:N). Šioje situacijoje dalykai tampa šiek tiek sudėtingi. Ši situacija taikoma finansinių dimensijų pavyzdyje. 

    Tokiu atveju galite įdiegti savo metodą duomenims nuskaityti. Čia yra pavyzdžio kodas `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` faile.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>3 veiksmas. Įtraukti duomenis į užklausą

Išplėskite `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` arba `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` metodą, norėdami įtraukti duomenis į užklausą. Čia yra pavyzdžio kodas `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` faile.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

Šiuo kodu yra `_destination` viršelio objektas, naudojamas registruoti užklausai generuoti, `_source` ir yra `TaxIntegrationLineObject` objektas.

> [!NOTE]
> Nustatykite raktą, kuris naudojamas užklausos formoje kaip privatus const **str**. Eilutė turi būti lygiai tokia pati, kaip ir temoje įtrauktas matavimo pavadinimas: [įtraukti duomenų laukus į mokesčių konfigūracijas](tax-service-add-data-fields-tax-configurations.md).
> Nustatykite lauką **copyToTaxableDocumentLineWraobjectFromTaxIntegrationLineObjectByLine** metode naudodami **SetField** metodą. Antrojo parametro duomenų tipas turi būti **eilutė**. Jei duomenų tipas nėra eilutė **, konvertuokite** jį.
> Jei X++ išvarditi **tipas** išplėstas, atsidėmėkite skirtumą tarp jo vertės, žymės ir pavadinimo.
> 
>   - Išvarditi vertė yra integer.
>   - Išvardi jos žymė gali skirtis pageidaujamose kalbose. Nenaudokite enum2Str **enum2Str** enum tipui konvertuoti į eilutę.
>   - Išvarditi rekomenduojama, nes jis fiksuotas. **enum2Symbol** gali būti naudojamas konvertuojant išvardiimą į jo pavadinimą. Išvardijimo reikšmė, įtraukta į mokesčių konfigūraciją, turi būti lygiai tokia pati kaip išvardijimo pavadinimas.

## <a name="model-dependency"></a>Modelio priklausomybė

Norėdami sėkmingai sukurti projektą, modelio priklausomybei įtraukite šiuos nuorodų modelius:

- Application Programos forma
- Application Mokėjimo prašymas
- Mokesčių modulis
- Dimensijos, jei naudojama finansinė dimensija
- Kiti reikalingi modeliai, nurodyti kode

## <a name="validation"></a>Patikrinimas

Atlikę ankstesnius veiksmus, galite patikrinti savo keitimus.

1. Finansuose eikite į **mokėtinas** sumas ir **į URL įtraukite &debug=vsCconfirmExit%2>**. Pavyzdžiui,https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&. Galutinis yra **&** būtinas.
2. Atidaryti pirkimo **užsakymo puslapį** ir pasirinkti **Naujas,** kad būtų sukurtas pirkimo užsakymas.
3. Nustatykite pritaikyto lauko vertę ir pasirinkite **PVM**. Trikčių diagnostikos failas su prefiksu, **TaxServiceTroubleshootingLog atsisiųstas** automatiškai. Šiame faile yra operacijos informacija, užregistruota Mokesčių skaičiavimo paslaugoje. 
4. Patikrinkite, ar pritaikytas įtrauktas laukas yra mokesčių tarnybos skaičiavimo įvesties **JSON skyriuje** ir ar jo vertė teisinga. Jei vertė neteisinga, šiame dokumente du kartus patikrinkite veiksmus.

Failo pavyzdys:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>Priedas

Šiame priede rodomas visas pavyzdinis kodas, skirtas finansinių dimensijų, **išlaidų centro ir** **projekto integravimui** eilutės lygiu.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
