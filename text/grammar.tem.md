# Mietvertrag

__Ich__ vermiete meine _Wohnung_ {{address}} an {{mieter}} fuer den Zeitraum von {{erstes_datum as "MM/DD/YYYY"}} bis {{zweites_datum}} fuer einen ***Monatlichen*** preis von {{preis}}.
{{%
    if pleite  
    then "mieter kann nicht zahlen"       
    else "Mieter zahlt fristgerecht"
%}} 
{{#if erspartes}} Der Mieter kann doch noch zahlen. {{else}} selbst die Sparbüchse ist leer {{/if}}

## Payment 

{{#clause paymentClause}}
Der mieter muss dem vermieter die {{amountText}} ({{amount}}) {{paymethod}}.
{{/clause}}
