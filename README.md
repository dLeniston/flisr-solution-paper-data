# Implementation of a software defined FLISR solution on an active distribution grid

This repository contains selected background data utilised to realise the Fault Isolation, Identification and Service Resoration (FLISR) solution developed as part of the SOGNO and edgeFLEX projects. The solution was tested on a distribution grid in the South East of Ireland, operated by Irelands leading Distribution Grid Operator, ESB Networks.

## Contents

- Documentation

The `/docs` directory contains a decision tree which informed the development of the FLISR solution algorithm, it represents graphically the conditions under which certain fault cases occur.

- CIM model

The `/cim` directory contains a Common Information Model (CIM) representation of one of the circuits (E11) on which the solution was trialled. This file is written in JavaScript Object Notation (JSON) format and contains metadata relating to nodes on this circuit and their location relative to other assets. These models were utilised to give the FLISR solution system awareness in terms of where pole mounted switches and reclosers are located relative to one another to enable the solution to produce meaningful outputs.

- Sample asset readings & fault cases

The `/data` directory contains both sample data and fault case data. The sample data set is provided in a CSV file for investigation or importing into a time series database such as [InfluxDB](https://www.influxdata.com/time-series-platform/). The fault cases can be found in the `/test_case_seeds` directory. These test cases are based on the decision tree located in `/docs` and were used to drive and test development of the FLISR solution, the test cases for the E11 circuit are included and are intended for use with an InfluxDB database.

Each test case `seed.txt` file contains the asset readings required to trigger a particular fault, each can be found in their respective directory `fault_case_1`, `fault_case_2`, etc.

Author Darren Leniston <darren.leniston@waltoninstitute.ie>

This research is supported by European Union’s Horizon 2020 research and innovation programme under grant agreement No 883710, project edgeFLEX (Providing fexibility to the grid by enabling VPPs to oer both fast and slow dynamics control services).
