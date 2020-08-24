# Mietvertrag

__Ich__{{#with vermieter}}{{partyId}} {{nachname}} {{/with}}vermiete meine _Wohnung_ {{address}} an {{#with mieter}}{{partyId}} {{nachname}}{{/with}} fuer den Zeitraum von {{erstes_datum as "MM/DD/YYYY"}} bis {{zweites_datum}} fuer einen ***Monatlichen*** preis von {{preis}}.
{{#if pleite}}Mieter kann nicht zahlen{{else}}Mieter zahlt fristgerecht{{/if}}
{{%
    if pleite  
    then "Mieter kann nicht zahlen"       
    else "Mieter zahlt fristgerecht"
%}} 
{{#if erspartes}}Der Mieter kann doch noch zahlen.{{else}}selbst die Sparbüchse ist leer{{/if}}

## Payment 

{{#clause paymentClause}}
Der mieter muss dem vermieter die {{amountText}} ({{amount}}) {{paymethod}}.
{{/clause}}
