# Bounties Network Audit

<img height="100px" Hspace="30" Vspace="10" align="right" src="static-content/diligence.png"/>

<!-- Don't remove this -->
<!--59bcc3ad6775562f845953cf01624225-->
<!-- Don't remove this -->

## 1 Summary

ConsenSys Diligence conducted a security audit on the smart contract system provided by the Bounties Network. This version adds a few new features to the existing smart contract: meta transaction support and ERC721 bounties.

<!-- Provide a headline description of what you have audited and what the goal or purpose of the audited project is.
Also add any other important context for the audit -->

### 1.1 Audit Dashboard

---

<img height="120px" Hspace="30" Vspace="10" align="right" src="static-content/dashboard.png"/>

#### Audit Details

- **Project Name:** Bounties Network
- **Client Name:** Bounties Network
- **Client Contact:** Mark Beylin
- **Auditors:** Daniel Luca, Sergii Kravchenko, Martin Ortner, Dean Pierce
- **GitHub :** ConsenSys/bounties-audit-2019-03
- **Languages:** Solidity
- **Date:** March 22nd, 2019

#### Number of issues per severity

<%= issue_overview %>

---

### 1.2 Audit Goals

The focus of the audit was to verify that the smart contract system is secure, resilient and working according to its specifications. The audit activities can be grouped in the following three categories:

**Security:** Identifying security related issues within each contract and within the system of contracts.

**Sound Architecture:** Evaluation of the architecture of this system through the lens of established smart contract best practices and general software best practices.

**Code Correctness and Quality:** A full review of the contract source code. The primary areas of focus include:

- Correctness
- Readability
- Sections of code with high complexity
- Improving scalability
- Quantity and quality of test coverage

### 1.3 System Overview

#### Documentation

The only documentation that was provided is in the form of source code comments.

#### Scope

The scope of the audit were the 2 active smart contracts:

|         File Name         |                SHA-1 Hash                |
| ------------------------- | ---------------------------------------- |
| BountiesMetaTxRelayer.sol | c2c00cd83814b2b2245d0354d613160db078ecae |
| StandardBounties.sol      | ad89921694268dfeba8e7bb1fedf7242bacda8ac |

Commit hash is `3d7c1771f78c5afdd896e2e2d34cf3dfc7fd4813`

#### Design

The `StandardBounties` contract contains the full functionality and represents the bounty registry; it holds the ERC20, ERC721 tokens and ether which represent the bounty reward.

`BountiesMetaTxRelayer` is a trusted meta transaction relayer that extracts the address of a signed message and calls the corresponding function in the `StandardBounties` contract.

### 1.4 Key Observations/Recommendations

#### Positive Observations

The code is written in a clear manner, groups modifiers, events, public and internal functions, making the codebase easy to audit. The repository contains a fair number of truffle tests that increase the confidence in the codebase and functionality correctness. It implements new features on the Bounties Network platform that might increase the adoption and usability of the platform.

#### Recommendations

##### Write tests for meta transactions

There are no written tests that check the meta transactions functionality. It will be useful to test this because they will guide the front-end implementation and will validate that the smart contracts in their current form are usable and self sufficient.

Along with adding tests for meta transactions the developer will realize he needs to make some changes to the code to handle **relayed ether bounties**. The current version does not do this because the ether is not relayed to the `StandardBounties` contract.

##### Reimplement handling of ERC721 tokens

The ERC721 tokens are handled as ERC20 tokens (for the most part). They should be handled differently because they are a different kind of tokens. Fungible tokens (ERC20) have some properties that do not apply to non fungible tokens (ERC721). The biggest change would be creating a map linking bounties and assigned ERC721 tokens instead of summing token IDs to handle ownership. This will change the code in multiple places and will generate significant amount work that needs to be audited once again. Take the time and carefully plan this reimplementation.

##### Remove unused code

Cleanup the repository by removing the token smart contracts and replacing them with only the interfaces. This decreases the reader's scope (whether the reader is a person or a tool) and makes clear the intention of the source files included in the repository, they should only define the token interfaces that are used in the `StandardBounties` smart contract.

##### Update documentation

Having good comments inside the contract is great but having dedicated documentation is better. We have provided a few diagrams that you can use or might inspire you to describe the system.

## 2 Issue Overview

The following table contains all the issues discovered during the audit. The issues are ordered based on their severity. More detailed description on the levels of severity can be found in Appendix 2. The table also contains the Github status of any discovered issue.

<%= issue_list %>

## 3 Issue Detail

<%= issues_markdown %>

## 4 Threat Model

The creation of a threat model is beneficial when building smart contract systems as it helps to understand the potential security threats, assess risk, and identify appropriate mitigation strategies. This is especially useful during the design and development of a contract system as it allows to create a more resilient design which is more difficult to change post-development.

A threat model was created during the audit process in order to analyze the attack surface of the contract system and to focus review and testing efforts on key areas that a malicious actor would likely also attack. It consists of two parts a high level design diagram that help to understand the attack surface and a list of threats that exist for the contract system.

The Bounties Network smart contract system enables anyone to create a bounty and safely distribute the rewards. The following Threat Model is an abstraction of the current system and has been compiled based on the understanding of how the smart contracts have been implemented. It does not claim completeness and can be considered as a complementary analysis type to the manual code review and automated tool analysis.

### 4.1 Overview

#### System components

The Bounties Network system has a few components that are deployed by the Bounties Network team or by a third party.

- **StandardBounties**: See chapter [1.3 System Overview](#13-system-overview)
- **BountiesMetaTxRelayer**: See chapter [1.3 System Overview](#13-system-overview)
- **ERC20 / ERC721 contracts**: These contracts hold token balances and they can be bounty rewards.

#### Actors

A list of actors has been created:

- **Issuer**: Has complete control over the bounty, can edit any of its parameters, including but not limited to changing the list of issuers, approvers and other bounty details.
- **Approver**: Is allowed to accept the fulfillment submitted to a bounty, effectively sending rewards to fulfillers.
- **Fulfiller**: Receives rewards based on a submission.
- **Submitter**: Submits fulfillments, which contain a list of fulfillers' addresses.
- **Contributor**: Contributes with funds to the bounty, increasing the bounty size.
- **StandardBounties Owner**: Can set once the `metaTxRelayer` as being smart contract relaying meta transactions.

#### Assets

Assets need to be protected and must be disbursed as rewards by the approvers. They must be protected, as potential threats could result in considerable loss for actors as well as loss of trust in the system.
The following assets were identified:

- **ERC20 / ERC721 tokens and ether**: bounty rewards, owned by contributors.
- **Signed meta transactions**: generated by the original address that wants to initiate actions on the system, owned by original address and the relayer.
- **StandardBounties**: contract owner account can set `MetaTxRelayer`
- **Bounty metadata**: IPFS hashes of JSON data structures composed of mandatory and optional fields.

#### Threats

- Because all of the bounties are stored in the same smart contract, finding a security issue in the system can put all bounties at risk. At the moment we're fairly sure the system is safe (apart from the issues we already described), but future updates can add problems to the system.
  - **Risk**: High
  - **Mitigation**: Audit each change to the system.

- The `MetaTxRelayer` may be used to call `StandardBounties` with various unpredictable (ecrecover) addresses. This can effectively grief the MetaTxRelayer account, draining the ether that is needed to pay for the transaction fee.
  - **Risk**: Medium
  - **Mitigation**: We cannot suggest a mitigation because the relayer component is not yet built.

- An attacker can hack any one of the issuers or approvers (or an issuer gone rogue) and remove all other issuers from the bounty, add themselves as an approver, fulfil the bounty and run off with the funds. The risk is limited to the current bounty only.
  - **Risk**: Low
  - **Mitigation**: A high value bounty can be managed by a multi-sig contract that requires a sufficiently high number of signers to make actions on the Bounties Network platform. Because this needs significant setup, one should only do this with high value bounties.

- Someone could front-run a fulfilment. By cloning another fulfillment and paying more gas to make sure your transaction is picked up by the miners before the original transaction, your fulfillment will be displayed before the original one on the website. The approver will not be able to know which is the original submission.
  - **Risk**: Medium
  - **Mitigation**: Delaying the IPFS metadata submission on the web front-end until the transaction was mined can mitigate this problem. This assumes a `fulfiller` property exists in the metadata and uniquely identifies the original fulfiller.

- Someone may collect all IPFS metadata hashes from calls to StandardBounties to collect personal data (optional e-mail, name, ...) of participants. This can also raise concerns over data privacy and GDPR compliance.
  - **Risk**: Low
  - **Mitigation**: Consider encrypting the metadata using an asymmetric encryption scheme.

- Malicious users can impersonate other users on the platform by creating accounts with the same name and picture.
  - **Risk**: Low
  - **Mitigation**: Make the trustworthiness "Network Stats" more visible on the bounty website UI.

- Anyone can trigger the `ActionPerformed` event.
  - **Risk**: Low
  - **Mitigation**: Consider restricting access to it if possible.

- Information emitted or stored within the contract may break assumptions in the context of the website.
  - **Risk**: Medium
  - **Mitigation**: Sanitize and validate the user provided data before using it on the website.

### 4.2 Detail

A detailed overview of the system has been created and it contains all of the methods contained in the system and the actors.

![Detailed overview](./static-content-project-specific/overview-detail.png)

## 5 Tool based analysis

The issues from the tool based analysis have been reviewed and the relevant issues have been listed in chapter 3 - Issues.

### 5.1 Mythril and Mythx

<img height="120px" align="right" src="static-content/mythril.png"/>

#### Mythril

Mythril is a security analysis tool for Ethereum smart contracts. It uses concolic analysis to detect various types of issues. The tool was used for automated vulnerability discovery for all audited contracts and libraries. More details on Mythril's current vulnerability coverage can be found [here](https://github.com/ConsenSys/mythril/wiki).

The raw output of the Mythril vulnerability scan can for smart contracts did not find anything and can be found [here](./tool-output/mythril/).

#### MythX

MythX is a security analysis API for Ethereum smart contracts. It performs multiple types of analysis, including fuzzing and symbolic execution, to detect many common vulnerability types. The tool was used for automated vulnerability discovery for all audited contracts and libraries. More details on MythX can be found at [mythx.io](https://mythx.io).

MythX was run on the on the flattened `BountiesMetaTxRelayer` which contains all of the contracts in the audit's scope. The raw output can be found [here](./tool-output/mythx/mythx_report.md).

### 5.2 Solhint

<img height="120px" align="right" src="static-content/solhint.png"/>

This is an open source project for linting Solidity code. The project provides both Security and Style Guide validations. The issues of Solhint were analyzed for security relevant issues only. It is still recommended to use Solhint during development to improve code quality while writing smart contracts.

The raw output of the Solhint vulnerability scan can be found [here](./tool-output/solhint/solhint_report.md).

### 5.3 Ethlint

<img height="120px" align="right" src="static-content/ethlint.png"/>

[Ethlint](https://www.ethlint.com/) is an open source project for linting Solidity code. Only security-related issues were reviewed by the audit team.

The raw output of the Ethlint vulnerability scan can be found [here](./tool-output/ethlint/ethlint_report.md).

### 5.4 Surya

Surya is a utility tool for smart contract systems. It provides a number of visual outputs and information about the structure of smart contracts. It also supports querying the function call graph in multiple ways to aid in the manual inspection and control flow analysis of contracts.

A complete list of functions with their visibility and modifiers can be found [here](./tool-output/surya/surya_report.md).

### 5.5 Slither

Slither is a static analysis framework for quickly finding interesting solidity issues in smart contracts, and printing out the relevant properties.

Issues found by Slither can be found [here](./tool-output/slither/slither.md), as well as a [function summary](./tool-output/slither/slither-function-summary.md) and information about [variables and authentication](./tool-output/slither/slither-vars-and-auth.md).

### 5.6 Odyssey

<img height="120px" align="right" src="static-content/odyssey.png"/>

Odyssey is an audit tool that acts as the glue between developers, auditors and tools. It leverages Github as the platform for building software and aligns to the approach that quality needs to be addressed as early as possible in the development life cycle and small iterative security activities spread out through development help to produce a more secure smart contract system.
In its current version Odyssey helps to better communicate audit issues to development teams and to successfully close them.

## 6 Test Coverage Measurement

The test-suite is implemented using Truffle and consists of 255 individual tests in three token specific suites covering `ETH`, `ERC20` and `ERC721` token handling of the system. 

Executing the [test-suite](./tool-output/test-suite/test-results.md#Test-Suite---Output) yields **<u>six failing test-cases</u>** caused by calling the non-existent function `getBountyFulfillments()` of contract `StandardBounties`. 

* Failure to detect failing test-cases can have severe operative and security related consequences and must be avoided under all circumstances. It is therefore recommended to make sure the test-suite is run for every release candidate, ideally automated as part of a CI/CD pipeline. It is further recommended to set-up the CI system to annotate every change that is proposed to the system with test-suite results (i.e. indicate test-suite errors for github pull-requests). 
* In order to provide more accurate coverage statistics we provide a [patch](./tool-output/test-suite/test-results.md#Test-Suit---Fix) fixing the test-suite.
* The [fixed test-suite](./tool-output/test-suite/test-results.md#Fixed-Test-Suite---Output) passes for all of the 255 test-cases.
* The test-suite is homogeneously, mainly focussed on testing specific units and appears to be lacking a set of negative tests and broader focussed integration tests. Test-cases often initialize an empty `StandardBounties` registry to perform very specific tests on. While this is okay for unit-tests it is recommended to also provide broader test-cases to cover variations of unique internal states (e.g. an empty registry, a registry with multiple empty bounties, a registry with multiple empty, non-empty bounties with issuers/approvers/.. being set/empty). More variation allows to better cover the fact that with potential future code one bounty might have an effect on other bounties during various calls (modifiers checking certain assumptions, functions looping over approvers/issuers/...). 

Code coverage metrics indicate the amount of lines/statements/branches that are covered by the test-suite. It's important to note that "100% test coverage" is not a silver bullet. Our review also included an inspection of the test suite to ensure that testing included important edge cases. Be aware that code coverage does not provide information about the individual test-cases quality.

For code coverage to be generated it was required to install the missing dependency `ethereumjs-testrpc-sc`. For details please refer to the [coverage statistics console output](./tool-output/test-suite/coverage-statistics.md) and the [coverage statistics html output](./coverage-reports/index.html).

* The code coverage of `49.12%` for Statements, `37.67%` for Branches, `59.26%` for Functions and `43.75%` Lines is very low. 
* The main contributing fact to the low coverage statistics is that `BountiesMetaTxRelayer.sol` is not covered at all. It is strongly recommended to fully cover this sourceUnit before releasing using the system.
* `StandardBounties.sol` yields an overall coverage of  `~94%` (`~80%` branch coverage).
  *  `StandardBounties.setMetaTxRelayer()` and `StandardBounties.refundContributions()` are not covered by any tests (e.g. `setMetaTxRelayer()` can only be called once and successfully stores the MetaTxRelayer address) 
  * `onlySubmitter()` and `hasNotPaid()` are only partially covered, missing tests covering the case that the `require` assertion may be violated.
  * `issueBounty()` is missing a test for an invalid `_tokenversion`.
  * `contribute` is missing a test for someone contributing an invalid amount.
  * `contribute` is missing a test for the case that due to an error someone might be able to contribute to a bounty that specifies an invalid token.
  * `transferTokens` is missing a test for the scenario that an external call to `ERC20.transfer()` might return `false` and therefore fail.
  * `transferTokens` is missing a test verifying that trying to transfer tokens for bounty with an invalid `tokenversion` reverts.
  * `acceptFulfillment()` is missing a test for the case that the bounty does not have sufficient balance to make the payout.
  * `acceptFulfillment()` is missing a test case for the case that the beneficiary of the bounty may receive zero tokens (item in `_tokenAmounts[]` is zero; verify receiver does not receive any tokens).


Both test coverage and quality are rather weak. One module is seriously lacking coverage. Only `80%-94%` of the code of the main contract is covered. In general we recommend to strive for a 100% coverage on all modules relevant to the system before releasing it. A smart contract system carries considerable risk and it should by all means be avoided to not being able to detect undesired, interface and assumption breaking or security relevant changes. The test-suite should consist of both unit specific and integration tests explicitly verifying security relevant assumptions, negative cases and edge-cases.


## Appendix 1 - File Hashes

The SHA1 hashes of the source code files in scope of the audit are listed in the table below.

|         File Name         |                SHA-1 Hash                |
| ------------------------- | ---------------------------------------- |
| BountiesMetaTxRelayer.sol | c2c00cd83814b2b2245d0354d613160db078ecae |
| StandardBounties.sol      | ad89921694268dfeba8e7bb1fedf7242bacda8ac |

## Appendix 2 - Severity

### A.2.1 - Minor

Minor issues are generally subjective in nature, or potentially deal with topics like "best practices" or "readability". Minor issues in general will not indicate an actual problem or bug in code.

The maintainers should use their own judgment as to whether addressing these issues improves the codebase.

### A.2.2 - Medium

Medium issues are generally objective in nature but do not represent actual bugs or security problems.

These issues should be addressed unless there is a clear reason not to.

### A.2.3 - Major

Major issues will be things like bugs or security vulnerabilities. These issues may not be directly exploitable, or may require a certain condition to arise in order to be exploited.

Left unaddressed these issues are highly likely to cause problems with the operation of the contract or lead to a situation which allows the system to be exploited in some way.

### A.2.4 - Critical

Critical issues are directly exploitable bugs or security vulnerabilities.

Left unaddressed these issues are highly likely or guaranteed to cause major problems or potentially a full failure in the operations of the contract.

## Appendix 3 - Disclosure

ConsenSys Diligence (“CD”) typically receives compensation from one or more clients (the “Clients”) for performing the analysis contained in these reports (the “Reports”). The Reports may be distributed through other means, including via ConsenSys publications and other distributions.

The Reports are not an endorsement or indictment of any particular project or team, and the Reports do not guarantee the security of any particular project. This Report does not consider, and should not be interpreted as considering or having any bearing on, the potential economics of a token, token sale or any other product, service or other asset. Cryptographic tokens are emergent technologies and carry with them high levels of technical risk and uncertainty. No Report provides any warranty or representation to any Third-Party in any respect, including regarding the bugfree nature of code, the business model or proprietors of any such business model, and the legal compliance of any such business. No third party should rely on the Reports in any way, including for the purpose of making any decisions to buy or sell any token, product, service or other asset. Specifically, for the avoidance of doubt, this Report does not constitute investment advice, is not intended to be relied upon as investment advice, is not an endorsement of this project or team, and it is not a guarantee as to the absolute security of the project. CD owes no duty to any Third-Party by virtue of publishing these Reports.

PURPOSE OF REPORTS The Reports and the analysis described therein are created solely for Clients and published with their consent. The scope of our review is limited to a review of Solidity code and only the Solidity code we note as being within the scope of our review within this report. The Solidity language itself remains under development and is subject to unknown risks and flaws. The review does not extend to the compiler layer, or any other areas beyond Solidity that could present security risks. Cryptographic tokens are emergent technologies and carry with them high levels of technical risk and uncertainty.

CD makes the Reports available to parties other than the Clients (i.e., “third parties”) -- on its Github account (https://github.com/ConsenSys). CD hopes that by making these analyses publicly available, it can help the blockchain ecosystem develop technical best practices in this rapidly evolving area of innovation.

LINKS TO OTHER WEB SITES FROM THIS WEB SITE You may, through hypertext or other computer links, gain access to web sites operated by persons other than ConsenSys and CD. Such hyperlinks are provided for your reference and convenience only, and are the exclusive responsibility of such web sites' owners. You agree that ConsenSys and CD are not responsible for the content or operation of such Web sites, and that ConsenSys and CD shall have no liability to you or any other person or entity for the use of third party Web sites. Except as described below, a hyperlink from this web Site to another web site does not imply or mean that ConsenSys and CD endorses the content on that Web site or the operator or operations of that site. You are solely responsible for determining the extent to which you may use any content at any other web sites to which you link from the Reports. ConsenSys and CD assumes no responsibility for the use of third party software on the Web Site and shall have no liability whatsoever to any person or entity for the accuracy or completeness of any outcome generated by such software.

TIMELINESS OF CONTENT The content contained in the Reports is current as of the date appearing on the Report and is subject to change without notice. Unless indicated otherwise, by ConsenSys and CD.
