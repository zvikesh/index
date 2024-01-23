# S/4 HANA ABAP

## Best Practices and Development Guidelines

**ADT**

- Generic Tips and Tricks: [Official Guide](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/tips-and-tricks-abap-core-tools?version=sap_btp)
- CDS 

**ABAP Data Modelling**

- Naming Conventions : [naming-conventions](https://github.com/zvikesh/naming-conventions)
- Modelling Cheatsheet: [VDM Data Modelling](https://app.excalidraw.com/l/5eMbpiBu0l3/5sRgLPpDEZj)
- Modelling Annotations Cheatsheet: [abap-data-modelling-vdm](https://github.com/zvikesh/abap-data-modelling-vdm)
- RAP Annotations Cheatsheet: [rap-annotations-cheat-sheet](https://github.com/zvikesh/rap-annotations-cheat-sheet)
 
**OpenSQL 7.4+**

- Definitive Guideline   </br> **Note**: Check Readme.md for conclusive guideline

**Fiori Content Management**

- Naming Convention:
- Development Guidelines:

**Fiori Troubleshooting**

- N/A: troubleshooting_apps_and_api (TBD)

**BRF+**

- Naming Conventions
- Performance Guidelines
- Enhancing through Application Exit


## Coding Samples

BTP Trial - Demo Package
- /DMO/FLIGHT_SWC
- /DMO/FEATURE_SHOWCASE_APP

zvks_root: Root Package
- zvks_utility: [utility](https://github.com/zvikesh/utility)
- zvks_ddic: [data-dictionary](https://github.com/zvikesh/data-dictionary)
- zvks_open_sql: [open-sql](https://github.com/zvikesh/open-sql)
- RAP Development
  - zvks_rap_prd_ro (TBD)
  - zvks_rap_po_tp_man (TBD)
  - zvks_rap_po_tp_unm (TBD)
  - zvks_rap_***_unm_qry (TBD)
  - zvks_rap_po_ext (TBD)
  - zvks_rap_***_hier (TBD)
- Embedded Analytics
  - ea-mdr
  - ea-alp
  - ea-sba
  - zvks_ea-value-help
- Fiori Element Extension
  - List Report
  - MDR/SBA
  - ALP
- zvks_fwf: Flexible Workflow [flexible-workflow](https://github.com/zvikesh/flexible-workflow/tree/main)
  - zvks_cust_fwf_cust_evt: custom-flex-wf-for-custom-event
  - zvks_cust_fwf_std_evt: custom-flex-wf-for-standard-event
  - zvks_std_so_fwf: standard-sales-order-flex-wf
  - zvks_ext_std_so_fwf: extending-standard-sales-order-flex-wf
- zvks_evt_list_class Event Driven Architecture
  - zvks_eda_list_class Event Listener Class
- zvks_flight : Flight Scenario for Practise
  - zvks_flight_ddic : [flight-ddic](https://github.com/zvikesh/flight-ddic)
  - zvks_flight_ro   : [flight-read-only](https://github.com/zvikesh/flight-read-only)

RAP TP scripts
- Basic View to demonstrate most of semantic annotations usage.

  </br> **Note**: First import DDIC repository and activate it, activate Domains > Data Elements ? Structure > Table, then followed by any other dependent repository.
- N/A : [code-snippets](https://github.com/zvikesh/code-snippets)


- Check how frameworks handles the data validation for domain value and value table without value help.
- How it handles after adding value help.
- How to highlight the box for which the error occured during save sequence.
- Try creating duplicate entries.
- Dynamic behaviour on clicking checkbox and entering field value.

# BTP

Official Guide </br>

https://help.sap.com/docs/btp/best-practices/best-practices-for-sap-btp
