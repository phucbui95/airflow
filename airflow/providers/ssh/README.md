<!--
 Licensed to the Apache Software Foundation (ASF) under one
 or more contributor license agreements.  See the NOTICE file
 distributed with this work for additional information
 regarding copyright ownership.  The ASF licenses this file
 to you under the Apache License, Version 2.0 (the
 "License"); you may not use this file except in compliance
 with the License.  You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing,
 software distributed under the License is distributed on an
 "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
 KIND, either express or implied.  See the License for the
 specific language governing permissions and limitations
 under the License.
 -->


# Package apache-airflow-backport-providers-ssh

Release: 2020.5.20

**Table of contents**

- [Backport package](#backport-package)
- [Installation](#installation)
- [Compatibility](#compatibility)
- [PIP requirements](#pip-requirements)
- [Provider class summary](#provider-class-summary)
    - [Operators](#operators)
        - [Moved operators](#moved-operators)
    - [Hooks](#hooks)
        - [Moved hooks](#moved-hooks)
- [Releases](#releases)
    - [Release 2020.5.20](#release-2020520)

## Backport package

This is a backport providers package for `ssh` provider. All classes for this provider package
are in `airflow.providers.ssh` python package.

**Only Python 3.6+ is supported for this backport package.**

While Airflow 1.10.* continues to support Python 2.7+ - you need to upgrade python to 3.6+ if you
want to use this backport package.



## Installation

You can install this package on top of an existing airflow 1.10.* installation via
`pip install apache-airflow-backport-providers-ssh`

## Compatibility

For full compatibility and test status of the backport packages check
[Airflow Backport Package Compatibility](https://cwiki.apache.org/confluence/display/AIRFLOW/Backported+providers+packages+for+Airflow+1.10.*+series)

## PIP requirements

| PIP package   | Version required   |
|:--------------|:-------------------|
| paramiko      | &gt;=2.6.0            |
| pysftp        | &gt;=0.2.9            |
| sshtunnel     | &gt;=0.1.4,&lt;0.2       |

# Provider class summary

All classes in Airflow 2.0 are in `airflow.providers.ssh` package.


## Operators




### Moved operators

| Airflow 2.0 operators: `airflow.providers.ssh` package                                                            | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                                                |
|:------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [operators.ssh.SSHOperator](https://github.com/apache/airflow/blob/master/airflow/providers/ssh/operators/ssh.py) | [contrib.operators.ssh_operator.SSHOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/operators/ssh_operator.py) |







## Hooks



### Moved hooks

| Airflow 2.0 hooks: `airflow.providers.ssh` package                                                    | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                            |
|:------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [hooks.ssh.SSHHook](https://github.com/apache/airflow/blob/master/airflow/providers/ssh/hooks/ssh.py) | [contrib.hooks.ssh_hook.SSHHook](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/hooks/ssh_hook.py) |






## Releases

### Release 2020.5.20

| Commit                                                                                         | Committed   | Subject                                                                    |
|:-----------------------------------------------------------------------------------------------|:------------|:---------------------------------------------------------------------------|
| [0b0e4f7a4](https://github.com/apache/airflow/commit/0b0e4f7a4cceff3efe15161fb40b984782760a34) | 2020-05-26  | Preparing for RC3 relase of backports (#9026)                              |
| [00642a46d](https://github.com/apache/airflow/commit/00642a46d019870c4decb3d0e47c01d6a25cb88c) | 2020-05-26  | Fixed name of 20 remaining wrongly named operators. (#8994)                |
| [375d1ca22](https://github.com/apache/airflow/commit/375d1ca229464617780623c61c6e8a1bf570c87f) | 2020-05-19  | Release candidate 2 for backport packages 2020.05.20 (#8898)               |
| [12c5e5d8a](https://github.com/apache/airflow/commit/12c5e5d8ae25fa633efe63ccf4db389e2b796d79) | 2020-05-17  | Prepare release candidate for backport packages (#8891)                    |
| [f3521fb0e](https://github.com/apache/airflow/commit/f3521fb0e36733d8bd356123e56a453fd37a6dca) | 2020-05-16  | Regenerate readme files for backport package release (#8886)               |
| [92585ca4c](https://github.com/apache/airflow/commit/92585ca4cb375ac879f4ab331b3a063106eb7b92) | 2020-05-15  | Added automated release notes generation for backport operators (#8807)    |
| [21cc7d729](https://github.com/apache/airflow/commit/21cc7d729827e9f3af0698bf647b2d41fc87b11c) | 2020-05-10  | Document default timeout value for SSHOperator (#8744)                     |
| [4bde99f13](https://github.com/apache/airflow/commit/4bde99f1323d72f6c84c1548079d5e98fc0a2a9a) | 2020-03-23  | Make airflow/providers pylint compatible (#7802)                           |
| [74c2a6ded](https://github.com/apache/airflow/commit/74c2a6ded4d615de8e1b1c04a25146344138e920) | 2020-03-23  | Add call to Super class in &#39;ftp&#39; &amp; &#39;ssh&#39; providers (#7822)                 |
| [df24b4337](https://github.com/apache/airflow/commit/df24b43370ca5812273ecd91d35104e023a407e6) | 2020-02-14  | [AIRFLOW-6800] Close file object after parsing ssh config (#7415)          |
| [97a429f9d](https://github.com/apache/airflow/commit/97a429f9d0cf740c5698060ad55f11e93cb57b55) | 2020-02-02  | [AIRFLOW-6714] Remove magic comments about UTF-8 (#7338)                   |
| [9a04013b0](https://github.com/apache/airflow/commit/9a04013b0e40b0d744ff4ac9f008491806d60df2) | 2020-01-27  | [AIRFLOW-6646][AIP-21] Move protocols classes to providers package (#7268) |