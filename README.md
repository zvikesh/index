# ABAP Package Tree

# Migrate Everything from below to Capacities

## Side by Side Extension Guidelines

Naming Conventions, Best Practices, Troubleshooting and Performance Optimization etc.

### ADT

- ADT Tips and Tricks
  - [Core Development](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/tips-and-tricks-abap-core-tools?version=sap_btp)
  - [CDS Development](https://help.sap.com/docs/abap-cloud/abap-cds-tools-user-guide/tips-and-tricks-abap-cds-tools)
- Performance Optimization
  - Code Profiling
  - ABAP Tracing and SQL Monitor
- Troubleshooting
  - Debugger Tips and Tricks (TBD Check Notes) 
- Best Practices (TBD: Add from Notes like: Use Released APIs, KTD etc. and below extension contracts)
- Best Practices (TBD: Add from Notes)

### ABAP Data Modelling and Annotations

- abap-data-modelling-and-annotations (merge all into this new repository)
- Naming Conventions : [naming-conventions](https://github.com/zvikesh/naming-conventions)
- Modelling Cheatsheet: [VDM Data Modelling](https://app.excalidraw.com/l/5eMbpiBu0l3/5sRgLPpDEZj)
- Modelling Annotations Cheatsheet: [abap-data-modelling-vdm](https://github.com/zvikesh/abap-data-modelling-vdm)
- RAP Annotations Cheatsheet: [rap-annotations-cheat-sheet](https://github.com/zvikesh/rap-annotations-cheat-sheet)
 
### S4 HANA ABAP Programming

- OpenSQL 7.4+ Conclusive Guideline: </br> **Note**: Check Readme.md for conclusive guideline
- Object Orient Parallel ABAP: [oo-parallel-abap](https://github.com/zvikesh/oo-parallel-abap)

### Fiori 

- Fiori Content Management: (Page1: Naming Convention:)
- Fiori Elements App Dev Guidelines: (TBD)
- SAP UI5 App Dev Guidelines: (TBD)
- N/A: troubleshooting_apps_and_api (TBD)

### BRF+

- Naming Conventions
- Performance Guidelines
- Enhancing through Application Exit

### Flexible Worfklow

- Troubleshooting: SWIA, SWI1 or SWI2_ DIAG | SWUE, SWUS | SWELS, SWEL | Add from Notes | SAP Press Worfklow Page 501 | SWI5 How to Find the Workitem that is pending in a User SAP Inbox

## Devlelopers Extension

### Extension Contracts

Key User Tools
- Custom Fields, Custom Logic, Custom CDS, Custom Analytical Queries etc.

Extensions (**C0**) 
- [Affected Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/2ce344a782d74d8aab073fa188af5116.html)
- Key User Extensibility: Can be extend using Key User tools. 
- Developer Extensibility (Cloud Development): Can be extended using ADT. 

System-Internal Use (**C1**) 
- [Affected Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/3ccb57a1a4d04ee192fdc2a849a89158.html)
- Key User Extensibility: Can be consumed by custom solution built using Key User tools.
- Developer Extensibility (Cloud Development): Can be consumed by custom solution built using ADT.
- **Deprecated**: Objects with C1 contract can be [deprecated](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/f64ebfd241fe4b40b5902b8630d26db6.html) by a successor object. While, consuming C1 contract object customer should mark their objects too as released and later adapt by marking existing [custom object as deprecated](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/a0b0c2282d49442dad541468f68f14e6.html) and replacing it with custom successor object.
- **Decommissioned**: After 12+ months of deprecation, object will be decommissioned and can no longer be used in production.  

Remote API Use (**C2**) 
- [Affected Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/9c7f9ba825064053874d5870bcb991fb.html)
- Can be used as Remote API, upgrade modification will not break the existing conumption as an API.

Manage Configuration Content (**C3**) 
- [Affected Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/8b734a3c1f2f416fb077675df46037b5.html)
- Optional non-key fields might be added later, but existing fields must not be changed or even removed. 
 - Alphanumeric fields might be elongated but will never be shortened.

AMDP (**C4**) 
- [Affected Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/288854b83f764fc2b7ae8c5f62140cfe.html)
- Same as C1, AMDP method can be consumed by custom solution but unlike C1 no deprecation or modification will be done.

Impementation using ATC variant:
- **ABAP_CLOUD_READINESS**: Custom code created with classic extensibility (language version Standard ABAP) uses any CDS views that don't have the status released.
- _With each software upgrade, customer will automatically receive syntax warnings of occurrences of deprecated CDS views or deprecated CDS view elements in the custom 
  content that was created with developer extensibility. This prompts customer to rework their content accordingly._

## Key Users Extension

## Coding Samples

**Auxiliary ABAP Packages**

- BTP Trial - Demo Package
  - /DMO/FLIGHT_SWC
  - /DMO/FEATURE_SHOWCASE_APP
- Root Package
  - zvks_root
- Utility Objects
  - zvks_utility: [utility](https://github.com/zvikesh/utility)
- DDIC Artifacts
  - zvks_ddic: [data-dictionary](https://github.com/zvikesh/data-dictionary)

**Open SQL**

- zvks_open_sql: [open-sql](https://github.com/zvikesh/open-sql)

**Fiori Elements**

- Read Only List Report
  - zvks_flight_ro zvks_fe_flight_ro: [flight-read-only](https://github.com/zvikesh/flight-read-only)
- Read Only List Report (BAPI)
  - zvks_fe_flight_ro_bapi
- Transactional List Report (Managed)
  - zvks_fe_flight_tp_man
- Transactional List Report (Managed with Unmanaged Save)
  - zvks_fe_flight_tp_unm
- Transactional List Report (Unmanaged)
- Transactional List Report (Unmanaged with Query)**
- Heirarichal List Report**
- Overview Page Report**
- Analytical List Page Report**

**Embedded Analytics**

- Multi Dimensional Report**
- Smart Business Report with KPI**

**SAP UI5**

**Custom Flexible Workflow**
- zvks_fwf_prd_crt: flex-workflow-product-creation [flexible-workflow](https://github.com/zvikesh/flexible-workflow/tree/main)

  - zvks_cust_fwf_cust_evt: custom-flex-wf-for-custom-event
  - zvks_cust_fwf_std_evt: custom-flex-wf-for-standard-event
  - zvks_std_so_fwf: standard-sales-order-flex-wf
  - zvks_ext_std_so_fwf: extending-standard-sales-order-flex-wf
- zvks_flight : Flight Scenario for Practise
  - zvks_flight_ddic : [flight-ddic](https://github.com/zvikesh/flight-ddic)

**SWE2/SWETYPV Event Handling**
- [swe2-evt-handling](https://github.com/zvikesh/swe2-evt-handling/)

RAP TP scripts
- Basic View to demonstrate most of semantic annotations usage.

  </br> **Note**: First import DDIC repository and activate it, activate Domains > Data Elements ? Structure > Table, then followed by any other dependent repository.
- N/A : [code-snippets](https://github.com/zvikesh/code-snippets)

- Check how frameworks handles the data validation for domain value and value table without value help.
- How it handles after adding value help.
- How to highlight the box for which the error occured during save sequence.
- Try creating duplicate entries.
- Dynamic behaviour on clicking checkbox and entering field value.

## Extension Coding Samples

# BTP

Official Guide </br>

https://help.sap.com/docs/btp/best-practices/best-practices-for-sap-btp

# MDG

