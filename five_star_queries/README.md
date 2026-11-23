# Querying the three deposits as one graph

`five_star_queries.ipynb` loads the JSON-LD metadata of the three deposits into one RDF dataset, one named graph per deposit, and queries it. `metadata/` holds the copies it reads with their checksums, `contexts/`, `ontologies/` and `schemas/` the JSON-LD contexts, EMMO modules and table schema, and `results/` every result as CSV. The data files read in section 10 are not included. `requirements.txt` lists the packages.

| Deposit | Record | Licence |
|---|---|---|
| AURORA | https://zenodo.org/records/15481956 | CC BY 4.0 |
| MORROW | https://zenodo.org/records/24261116 | CC BY 4.0 |
| Microsoft | https://zenodo.org/records/24005755 | CDLA-Permissive-2.0, text in `LICENSES/` |

The metadata copies keep these licences. The ontology modules are CC BY 4.0 and the table schema Apache 2.0, as released by their authors. The rest is CC BY 4.0.
