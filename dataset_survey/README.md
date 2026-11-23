# Battery Data Commons survey

`dataset_survey_results.csv` grades the 379 active dataset records of the Battery Data Commons (repository commit 1fc38622, without software and withdrawn records) against the criteria of Table 1 of *How to Publish Five-Star Battery Data*, one row per dataset.

| Column | Content |
|---|---|
| `bdc_id`, `title`, `data_group`, `host`, `doi` | The Commons record and the host its DOI or first link resolves to |
| `licence`, `licence_source`, `licence_class` | The licence as stated by the repository, DataCite or the Commons record; `open` under the Open Definition, `closed` for NC or ND terms, `none`, or `unclear` |
| `access` | `open`, `open (browser only)` when the host needs no account but blocks scripted downloads, `account required`, `not reachable`, or `unknown` |
| `file_evidence` | `downloaded files`, `repository file list`, `Commons format field`, or `none` |
| `share_open`, `share_excel`, `share_matlab`, `share_vendor` | Share of the structured data in each format family, by bytes where sizes are known and by file count otherwise |
| `star1` to `star5`, `star3_lenient` | Whether each criterion holds; `star3_lenient` counts spreadsheet and MATLAB files as open, which is the reading the article reports |
| `level`, `level_lenient` | The cumulative level under each Star Three reading; `1+` when the files of an openly licensed dataset could not be listed |
| `capped_by` | Why the dataset stops at its level |

Star One needs an Open Definition licence (CC BY, CC BY-SA, CC0 and other public-domain dedications, ODC-By, ODbL, CDLA-Permissive, Etalab, permissive software licences) and download without an account. Star Two needs structured data files, not only images, documents or code, classified by extension, with text files read for numeric tables. Star Three needs open formats to hold at least half of the structured data, by bytes or by file count; spreadsheet and MATLAB files count as open in the reported reading (268 datasets, 71 %) and as not open in the strict one (158, 42 %), and pickle, R data and vendor binaries as not open in both. Star Four needs RDF or JSON-LD inside the deposit (up to three metadata files and three RO-Crate manifests) that uses EMMO, BattINFO, QUDT or a related battery ontology, with at most 20 % malformed IRIs and 20 % unmapped JSON keys. Star Five adds a DOI and RDF links to external identifiers (ORCID, ROR, DOI, Wikidata) and to the deposit's own data records.

By hand, seven image-only deposits (bdc_000069, 000072, 000087, 000107, 000319, 000367, 000391) are graded as not structured, bdc_000040 as not reachable (its DOI returns 404), and Dryad deposits as open access, since the web download needs no account.
