# Selecting atoms by autodetection

GSL offers macros that automatically detect and select common molecular components. These macros simplify selections without needing to specify detailed criteria. GSL macros support atomistic, united-atom, and coarse-grained systems.

### Available macros:

- `@protein`: Selects all amino acid atoms (supports ~140 different amino acids).
- `@water`: Selects all water atoms.
- `@ion`: Selects all ion atoms.
- `@membrane`: Selects membrane lipid atoms (supports over 200 lipid types).
- `@dna`: Selects all DNA molecule atoms.
- `@rna`: Selects all RNA molecule atoms.

### Example usage:

```gsl
@protein or @membrane
```

*Selects all protein and membrane lipid atoms.*

> **Caution:** While these macros are generally reliable, they may not always perfectly identify all relevant atoms. Use them judiciously, especially when working with custom molecules.

### Macro definitions:

The following list shows how GSL macros currently expand. Note that these definitions may change in future versions to support additional atom matching:

- `@protein` = `resname ABU ACE AIB ALA ARG ARGN ASN ASN1 ASP ASP1 ASPH ASPP ASH CT3 CYS CYS1 CYS2 CYSH DALA GLN GLU GLUH GLUP GLH GLY HIS HIS1 HISA HISB HISH HISD HISE HISP HSD HSE HSP HYP ILE LEU LSN LYS LYSN LYSH MELEU MET MEVAL NAC NME NHE NH2 PHE PHEH PHEU PHL PRO SER THR TRP TRPH TRPU TYR TYRH TYRU VAL PGLU HID HIE HIP LYP LYN CYN CYM CYX DAB ORN HYP NALA NGLY NSER NTHR NLEU NILE NVAL NASN NGLN NARG NHID NHIE NHIP NHISD NHISE NHISH NTRP NPHE NTYR NGLU NASP NLYS NORN NDAB NLYSN NPRO NHYP NCYS NCYS2 NMET NASPH NGLUH CALA CGLY CSER CTHR CLEU CILE CVAL CASN CGLN CARG CHID CHIE CHIP CHISD CHISE CHISH CTRP CPHE CTYR CGLU CASP CLYS CORN CDAB CLYSN CPRO CHYP CCYS CCYS2 CMET CASPH CGLUH`
- `@water` = `name W OW HW1 HW2 OH2 H1 H2 and resname SOL WAT HOH OHH TIP T3P T4P T5P T3H W TIP3 TIP4 SPC SPCE`
- `@ion` = `name NA NA+ CL CL- K K+ SOD CLA CA CA2+ MG ZN CU1 CU LI RB CS F BR I OH Cal CAL IB+ and resname ION NA NA+ CL CL- K K+ SOD CLA CA CA2+ MG ZN CU1 CU LI RB CS F BR I OH Cal CAL IB+`
- `@membrane` = `resname DAPC DBPC DFPC DGPC DIPC DLPC DNPC DOPC DPPC DUPC DRPC DTPC DVPC DXPC DYPC LPPC PAPC PEPC PGPC PIPC POPC PRPC PUPC DAPE DBPE DFPE DGPE DIPE DLPE DNPE DOPE DPPE DRPE DTPE DUPE DVPE DXPE DYPE LPPE PAPE PGPE PIPE POPE PQPE PRPE PUPE DAPS DBPS DFPS DGPS DIPS DLPS DNPS DOPS DPPS DRPS DTPS DUPS DVPS DXPS DYPS LPPS PAPS PGPS PIPS POPS PQPS PRPS PUPS DAPG DBPG DFPG DGPG DIPG DLPG DNPG DOPG DPPG DRPG DTPG DVPG DXPG DYPG JFPG JPPG LPPG OPPG PAPG PGPG PIPG POPG PRPG DAPA DBPA DFPA DGPA DIPA DLPA DNPA DOPA DPPA DRPA DTPA DVPA DXPA DYPA LPPA PAPA PGPA PIPA POPA PRPA PUPA DPP1 DPP2 DPPI PAPI PIPI POP1 POP2 POP3 POPI PUPI PVP1 PVP2 PVP3 PVPI PADG PIDG PODG PUDG PVDG TOG APC CPC IPC LPC OPC PPC TPC UPC VPC BNSM DBSM DPSM DXSM PGSM PNSM POSM PVSM XNSM DPCE DXCE PNCE XNCE DBG1 DPG1 DPG3 DPGS DXG1 DXG3 PNG1 PNG3 XNG1 XNG3 DFGG DFMG DPGG DPMG DPSG FPGG FPMG FPSG OPGG OPMG OPSG CHOA CHOL CHYO BOG DDM DPC EO5 SDS BOLA BOLB CDL0 CDL1 CDL2 CDL DBG3 ERGO HBHT HDPT HHOP HOPR ACA ACN BCA BCN LCA LCN PCA PCN UCA UCN XCA XCN RAMP REMP OANT`
- `@dna` = `resname DA DG DC DT DA5 DG5 DC5 DT5 DA3 DG3 DC3 DT3 DAN DGN DCN DTN`
- `@rna` = `resname A U C G RA RU RC RG RA5 RT5 RU5 RC5 RG5 RA3 RT3 RU3 RC3 RG3 RAN RTN RUN RCN RGN`