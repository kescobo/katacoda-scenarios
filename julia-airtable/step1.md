# Julia REPL

## Set the environment variables

`export AIRTABLE_KEY='{api_key}'`{{copy}}
`export AIRTABLE_BASE='{airtable_base}'`{{copy}}

## Launch the REPL

`julia`{{execute}}

## Get into the Package Manager

`]`{{execute}}

`add https://github.com/kescobo/Airtable.jl`{{execute}}

## Back to the Julia command prompt

```
using Airtable
key=Airtable.Credential(ENV["AIRTABLE_KEY"]);
base=ENV["AIRTABLE_BASE"]
table="Table 1"

req1 = Airtable.request("GET", key, base, table; maxRecords=2)
req1.records
```{{execute}}
