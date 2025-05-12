# Microsoft Fabric Eventhouse Oefening

## Overzicht
Deze repository bevat een oefening waarin een **Eventhouse** wordt gecreëerd en gegevens worden geanalyseerd met **Kusto Query Language (KQL)** en **Transact-SQL (T-SQL)** in **Microsoft Fabric**.

## Inhoud
Tijdens deze oefening heb ik:
1. Een **Microsoft Fabric-werkruimte** aangemaakt.
2. Een **Eventhouse** aangemaakt en een KQL-database gebruikt.
3. Gegevens opgehaald en gefilterd met **KQL**.
4. Gegevens gesorteerd, geaggregeerd en gegroepeerd met **KQL**.
5. Gegevens opgehaald en gefilterd met **T-SQL** via het T-SQL-eindpunt.
6. De werkruimte opgeruimd na de analyse.

## Queryvoorbeelden
### KQL Query - Gegevens ophalen
```kql
Bikestream
| take 100

T-SQL Query - Gegevens samenvatten

sql
SELECT SUM(No_Bikes) AS [Totaal aantal fietsen]
FROM Bikestream

KQL Query - Sorteren en groeperen

kql
Bikestream
| summarize ["Totaal aantal fietsen"] = sum(No_Bikes) by Neighbourhood
| order by Neighbourhood asc

Microsoft Fabric
Microsoft Fabric biedt een platform voor real-time data-analyse, waarmee gebruikers gegevens kunnen opslaan, verwerken en analyseren met krachtige tools zoals KQL en SQL.

# Work-with-data-in-a-Microsoft-Fabric-eventhouse
