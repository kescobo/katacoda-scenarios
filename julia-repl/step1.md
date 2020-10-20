# Julia REPL

## Set the environment variabe

`AIRTABLE_KEY='shrx4BWLV1HurniFD'`{{copy}}

Replace the value with the one of the base that you want to access.

`AIRTABLE_BASE='appphImnhJO8AXmmo'`{{copy}}

## Launch the REPL

`julia`{{execute}}

## Get into the Package Manager

`]`{{execute}}

`add https://github.com/kescobo/Airtable.jl`{{execute}}

Then click on the terminal and type a backspace to exit the Package manager

## Back to the Julia command prompt

````
using Airtable
key=Airtable.Credential();
AIRTABLE_BASE=ENV["AIRTABLE_BASE"]
AIRTABLE_TABLE="Table 1"

req1 = Airtable.request("GET", key, AIRTABLE_BASE, AIRTABLE_TABLE; maxRecords=2)
req1.records
````{{execute}}
