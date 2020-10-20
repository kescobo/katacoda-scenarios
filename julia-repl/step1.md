# Julia REPL

## Launch the REPL

`julia`{{execute}}

## Get into the Package Manager

`]`{{execute}}

`add https://github.com/kescobo/Airtable.jl`{{execute}}

## Overwrite the environment variabe

`ENV["AIRTABLE_KEY"]="{api_key}"`{{copy}}
`ENV["AIRTABLE_BASE"]="{airtable_base}"`{{copy}}

## Back to the Julia command prompt

````
using Airtable
key=Airtable.Credential(ENV["AIRTABLE_KEY"]);
base=ENV["AIRTABLE_BASE"]
table="Table 1"

req1 = Airtable.request("GET", key, base, table; maxRecords=2)
req1.records
````
