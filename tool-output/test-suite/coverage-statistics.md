# Version used

```console
$ npx truffle version 
Truffle v5.0.8 (core: 5.0.8)
Solidity - 0.5.0 (solc-js)
Node v8.15.1
Web3.js v1.0.0-beta.37

$ npm install --dev ethereumjs-testrpc-sc
$ npm list | grep ethereumjs-testrpc-sc
├─┬ ethereumjs-testrpc-sc@6.1.6
````

---

# Code Coverage

The following coverage statistics are generated after applying the patch fixing the test-suite errors mentioned in [test-results](./test-results). The coverage setup was missing the dependency `ethereumjs-testrpc-sc` which had to be installed manually. 

```console
$ npm run cvg

> StandardBounties@0.1.0 cvg ./bounties-audit-2019-03
> solidity-coverage

Generating coverage environment
No secrets.json found. If you are trying to publish EPM this will fail. Otherwise, you can ignore this message!
Running: truffle compile  
(this can take a few seconds)...

Compiling your contracts...
===========================
> Compiling ./contracts/BountiesMetaTxRelayer.sol
> Compiling ./contracts/StandardBounties.sol
> Compiling ./contracts/inherited/ERC20Token.sol
> Compiling ./contracts/inherited/ERC721Basic.sol
> Compiling ./contracts/inherited/HumanStandardToken.sol
> Compiling ./contracts/inherited/Migrations.sol
> Compiling ./contracts/inherited/Token.sol

    > compilation warnings encountered:

./bounties-audit-2019-03/coverageEnv/contracts/StandardBounties.sol:2:1: Warning: Experimental features are turned on. Do not use experimental features on live deployments.
pragma experimental ABIEncoderV2;
^-------------------------------^
,./bounties-audit-2019-03/coverageEnv/contracts/BountiesMetaTxRelayer.sol:2:1: Warning: Experimental features are turned on. Do not use experimental features on live deployments.
pragma experimental ABIEncoderV2;
^-------------------------------^

> Artifacts written to ./bounties-audit-2019-03/coverageEnv/build/contracts
> Compiled successfully using:
   - solc: 0.5.0+commit.1d4f565a.Emscripten.clang

Instrumenting  ./coverageEnv/contracts/BountiesMetaTxRelayer.sol
Skipping instrumentation of  ./coverageEnv/contracts/inherited/ERC20Token.sol
Skipping instrumentation of  ./coverageEnv/contracts/inherited/ERC721Basic.sol
Skipping instrumentation of  ./coverageEnv/contracts/inherited/HumanStandardToken.sol
Skipping instrumentation of  ./coverageEnv/contracts/inherited/Migrations.sol
Skipping instrumentation of  ./coverageEnv/contracts/inherited/Token.sol
Instrumenting  ./coverageEnv/contracts/StandardBounties.sol
Running: truffle compile  
(this can take a few seconds)...

Compiling your contracts...
===========================
> Compiling ./contracts/BountiesMetaTxRelayer.sol
> Compiling ./contracts/StandardBounties.sol
> Compiling ./contracts/inherited/ERC20Token.sol
> Compiling ./contracts/inherited/ERC721Basic.sol
> Compiling ./contracts/inherited/HumanStandardToken.sol
> Compiling ./contracts/inherited/Migrations.sol
> Compiling ./contracts/inherited/Token.sol

    > compilation warnings encountered:

./bounties-audit-2019-03/coverageEnv/contracts/StandardBounties.sol:2:1: Warning: Experimental features are turned on. Do not use experimental features on live deployments.
pragma experimental ABIEncoderV2;
^-------------------------------^
,./bounties-audit-2019-03/coverageEnv/contracts/BountiesMetaTxRelayer.sol:2:1: Warning: Experimental features are turned on. Do not use experimental features on live deployments.
pragma experimental ABIEncoderV2;
^-------------------------------^
,./bounties-audit-2019-03/coverageEnv/contracts/inherited/ERC721Basic.sol:12:3: Warning: Function state mutability can be restricted to pure
  function mul(uint256 a, uint256 b) internal      returns (uint256 c) {
  ^ (Relevant source part starts here and spans across multiple lines).
,./bounties-audit-2019-03/coverageEnv/contracts/inherited/ERC721Basic.sol:28:3: Warning: Function state mutability can be restricted to pure
  function div(uint256 a, uint256 b) internal      returns (uint256) {
  ^ (Relevant source part starts here and spans across multiple lines).
,./bounties-audit-2019-03/coverageEnv/contracts/inherited/ERC721Basic.sol:38:3: Warning: Function state mutability can be restricted to pure
  function sub(uint256 a, uint256 b) internal      returns (uint256) {
  ^ (Relevant source part starts here and spans across multiple lines).
,./bounties-audit-2019-03/coverageEnv/contracts/inherited/ERC721Basic.sol:46:3: Warning: Function state mutability can be restricted to pure
  function add(uint256 a, uint256 b) internal      returns (uint256 c) {
  ^ (Relevant source part starts here and spans across multiple lines).
,./bounties-audit-2019-03/coverageEnv/contracts/inherited/ERC721Basic.sol:65:3: Warning: Function state mutability can be restricted to view
  function isContract(address addr) internal      returns (bool) {
  ^ (Relevant source part starts here and spans across multiple lines).

> Artifacts written to ./bounties-audit-2019-03/coverageEnv/build/contracts
> Compiled successfully using:
   - solc: 0.5.0+commit.1d4f565a.Emscripten.clang

Launched testrpc on port 8555
Running: truffle test  
(this can take a few seconds)...
Using network 'development'.


Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.



  Contract: StandardBounties
    ✓ [ERC20] Verifies that the StandardBounties registry works (97ms)
    ✓ [ERC20] Verifies that I can issue a bounty paying in ERC20 tokens without locking up funds (273ms)
    ✓ [ERC20] Verifies that I can issue a bounty paying in ERC20 tokens while locking up funds (324ms)
    ✓ [ERC20] Verifies that I can't issue a bounty in tokens contributing both tokens and ETH (360ms)
    ✓ [ERC20] Verifies that I can't issue a bounty contributing less than the deposit amount (378ms)
    ✓ [ERC20] Verifies that I can contribute to a bounty in ERC20 tokens (377ms)
    ✓ [ERC20] Verifies that I can't contribute to a bounty which is out of bounds (264ms)
    ✓ [ERC20] Verifies that I can't contribute to a bounty and send less than the deposit amount (329ms)
    ✓ [ERC20] Verifies that I can't contribute to a bounty and send both tokens and ETH (313ms)
    ✓ [ERC20] Verifies that contributing emits an event (290ms)
    ✓ [ERC20] Verifies that I can refund a contribution in ERC20 tokens (553ms)
    ✓ [ERC20] Verifies that I can't refund a contribution to a bounty which is out of bounds (377ms)
    ✓ [ERC20] Verifies that I can't refund a contribution which is out of bounds (388ms)
    ✓ [ERC20] Verifies that I can't refund a contribution which isn't mine (584ms)
    ✓ [ERC20] Verifies that I can't refund a contribution which has already been refunded (513ms)
    ✓ [ERC20] Verifies that I can't refund a contribution before the deadline has elapsed (379ms)
    ✓ [ERC20] Verifies that refunding a contribution emits an event (491ms)
    ✓ [ERC20] Verifies that I can perform an action for a bounty (221ms)
    ✓ [ERC20] Verifies that I can't perform an action for an out of bounds bounty (231ms)
    ✓ [ERC20] Verifies that performing an action emits an event (218ms)
    ✓ [ERC20] Verifies that I can fulfill a bounty (325ms)
    ✓ [ERC20] Verifies that I can't fulfill an out of bounds bounty (241ms)
    ✓ [ERC20] Verifies that I can't fulfill a bounty after the deadline has elapsed (327ms)
    ✓ [ERC20] Verifies that I can't fulfill a bounty with 0 fulfillers (279ms)
    ✓ [ERC20] Verifies that fulfilling a bounty emits an event (247ms)
    ✓ [ERC20] Verifies that I can update a fulfillment (388ms)
    ✓ [ERC20] Verifies that I can't update a fulfillment for an out of bounds bounty (299ms)
    ✓ [ERC20] Verifies that I can't update an out of bounds fulfillment (309ms)
    ✓ [ERC20] Verifies that I can't update a fulfillment which was submitted by someone else (332ms)
    ✓ [ERC20] Verifies that updating a fulfillment emits an event (289ms)
    ✓ [ERC20] Verifies that I can accept a fulfillment as an issuer (473ms)
    ✓ [ERC20] Verifies that I can accept a fulfillment paying different amounts to different fulfillers (419ms)
    ✓ [ERC20] Verifies that I can accept a fulfillment as an approver (431ms)
    ✓ [ERC20] Verifies that I can't accept a fulfillment on an out of bounds bounty (370ms)
    ✓ [ERC20] Verifies that I can't accept a fulfillment which is out of bounds (421ms)
    ✓ [ERC20] Verifies that I can't accept a fulfillment if I'm not an approver (391ms)
    ✓ [ERC20] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (406ms)
    ✓ [ERC20] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (431ms)
    ✓ [ERC20] Verifies that accepting a fulfillment emits an event (471ms)
    ✓ [ERC20] Verifies that I can fulfill and accept a bounty simultaneously (412ms)
    ✓ [ERC20] Verifies that I can change all of a bounty's info (367ms)
    ✓ [ERC20] Verifies that I can't change an out of bounds bounty (364ms)
    ✓ [ERC20] Verifies that I can't change a bounty if I'm not an issuer' (322ms)
    ✓ [ERC20] Verifies that I can change the issuer of my bounty (329ms)
    ✓ [ERC20] Verifies that I can't change the issuer of an out of bounds bounty (345ms)
    ✓ [ERC20] Verifies that I can't change the issuer of a bounty if I didn't issue it (325ms)
    ✓ [ERC20] Verifies that I can't the issuer with an out of bounds issuer ID (304ms)
    ✓ [ERC20] Verifies that I can't the issuer changing an out of bounds issuer ID (320ms)
    ✓ [ERC20] Verifies that changing a bounty's issuer emits an event (365ms)
    ✓ [ERC20] Verifies that I can change the approver of my bounty (336ms)
    ✓ [ERC20] Verifies that I can't change the approver of an out of bounds bounty (295ms)
    ✓ [ERC20] Verifies that I can't change the approver of a bounty if I didn't issue it (327ms)
    ✓ [ERC20] Verifies that I can't the issuer with an out of bounds issuer ID (372ms)
    ✓ [ERC20] Verifies that I can't the issuer changing an out of bounds approver ID (333ms)
    ✓ [ERC20] Verifies that changing a bounty's approver emits an event (313ms)
    ✓ [ERC20] Verifies that I can change the data of my bounty (313ms)
    ✓ [ERC20] Verifies that I can't change the data of an out of bounds bounty (356ms)
    ✓ [ERC20] Verifies that I can't change the data of a bounty if I didn't issue it (320ms)
    ✓ [ERC20] Verifies that I can't change the data with an out of bounds issuer ID (319ms)
    ✓ [ERC20] Verifies that changing a bounty's data emits an event (305ms)
    ✓ [ERC20] Verifies that I can change the deadline of my bounty (385ms)
    ✓ [ERC20] Verifies that I can't change the deadline of an out of bounds bounty (297ms)
    ✓ [ERC20] Verifies that I can't change the deadline of a bounty if I didn't issue it (322ms)
    ✓ [ERC20] Verifies that I can't change the deadline with an out of bounds issuer ID (310ms)
    ✓ [ERC20] Verifies that changing a bounty's deadline emits an event (353ms)
    ✓ [ERC20] Verifies that I can add issuers to my bounty (333ms)
    ✓ [ERC20] Verifies that I can't add issuers to an out of bounds bounty (290ms)
    ✓ [ERC20] Verifies that I can't add issuers to a bounty if I didn't issue it (336ms)
    ✓ [ERC20] Verifies that I can't add issuers with an out of bounds issuer ID (364ms)
    ✓ [ERC20] Verifies that adding issuers to a bounty emits an event (300ms)
    ✓ [ERC20] Verifies that I can replace the issuers of my bounty (331ms)
    ✓ [ERC20] Verifies that I can't replace issuers for an out of bounds bounty (299ms)
    ✓ [ERC20] Verifies that I can't replace issuers for a bounty if I didn't issue it (377ms)
    ✓ [ERC20] Verifies that I can't replace issuers with an out of bounds issuer ID (312ms)
    ✓ [ERC20] Verifies that replacing issuers of a bounty emits an event (310ms)
    ✓ [ERC20] Verifies that I can add approvers to my bounty (349ms)
    ✓ [ERC20] Verifies that I can't add approvers to an out of bounds bounty (349ms)
    ✓ [ERC20] Verifies that I can't add approvers to a bounty if I didn't issue it (317ms)
    ✓ [ERC20] Verifies that I can't add approvers with an out of bounds issuer ID (308ms)
    ✓ [ERC20] Verifies that adding approvers to a bounty emits an event (306ms)
    ✓ [ERC20] Verifies that I can replace the approvers of my bounty (344ms)
    ✓ [ERC20] Verifies that I can't replace approvers for an out of bounds bounty (349ms)
    ✓ [ERC20] Verifies that I can't replace approvers for a bounty if I didn't issue it (322ms)
    ✓ [ERC20] Verifies that I can't replace approvers with an out of bounds issuer ID (308ms)
    ✓ [ERC20] Verifies that replacing approvers of a bounty emits an event (357ms)

  Contract: StandardBounties
    ✓ [ERC721] Verifies that the StandardBounties registry works (79ms)
    ✓ [ERC721] Verifies that I can issue a bounty paying in ERC721 tokens without locking up funds (204ms)
    ✓ [ERC721] Verifies that I can issue a bounty paying in ERC721 tokens while locking up funds (357ms)
    ✓ [ERC721] Verifies that I can't issue a bounty in tokens contributing both tokens and ETH (359ms)
    ✓ [ERC721] Verifies that I can't issue a bounty contributing less than the deposit amount (360ms)
    ✓ [ERC721] Verifies that I can contribute to a bounty in ERC721 tokens (415ms)
    ✓ [ERC721] Verifies that I can't contribute to a bounty which is out of bounds (267ms)
    ✓ [ERC721] Verifies that I can't contribute to a bounty and send less than the deposit amount (335ms)
    ✓ [ERC721] Verifies that I can't contribute to a bounty and send both tokens and ETH (322ms)
    ✓ [ERC721] Verifies that contributing emits an event (354ms)
    ✓ [ERC721] Verifies that I can refund a contribution in ERC721 tokens (475ms)
    ✓ [ERC721] Verifies that I can refund multiple contributions in ERC721 tokens (733ms)
    ✓ [ERC721] Verifies that I can't refund a contribution to a bounty which is out of bounds (401ms)
    ✓ [ERC721] Verifies that I can't refund a contribution which is out of bounds (473ms)
    ✓ [ERC721] Verifies that I can't refund a contribution which isn't mine (542ms)
    ✓ [ERC721] Verifies that I can't refund a contribution which has already been refunded (553ms)
    ✓ [ERC721] Verifies that I can't refund a contribution before the deadline has elapsed (443ms)
    ✓ [ERC721] Verifies that refunding a contribution emits an event (443ms)
    ✓ [ERC721] Verifies that I can perform an action for a bounty (205ms)
    ✓ [ERC721] Verifies that I can't perform an action for an out of bounds bounty (266ms)
    ✓ [ERC721] Verifies that performing an action emits an event (206ms)
    ✓ [ERC721] Verifies that I can fulfill a bounty (254ms)
    ✓ [ERC721] Verifies that I can't fulfill an out of bounds bounty (298ms)
    ✓ [ERC721] Verifies that I can't fulfill a bounty after the deadline has elapsed (421ms)
    ✓ [ERC721] Verifies that I can't fulfill a bounty with 0 fulfillers (463ms)
    ✓ [ERC721] Verifies that fulfilling a bounty emits an event (230ms)
    ✓ [ERC721] Verifies that I can update a fulfillment (313ms)
    ✓ [ERC721] Verifies that I can't update a fulfillment for an out of bounds bounty (290ms)
    ✓ [ERC721] Verifies that I can't update an out of bounds fulfillment (344ms)
    ✓ [ERC721] Verifies that I can't update a fulfillment which was submitted by someone else (275ms)
    ✓ [ERC721] Verifies that updating a fulfillment emits an event (287ms)
    ✓ [ERC721] Verifies that I can accept a fulfillment paying different 721 tokens to different fulfillers (594ms)
    ✓ [ERC721] Verifies that I can accept a fulfillment as an approver (630ms)
    ✓ [ERC721] Verifies that I can't accept a fulfillment on an out of bounds bounty (503ms)
    ✓ [ERC721] Verifies that I can't accept a fulfillment which is out of bounds (571ms)
    ✓ [ERC721] Verifies that I can't accept a fulfillment if I'm not an approver (520ms)
    ✓ [ERC721] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (589ms)
    ✓ [ERC721] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (521ms)
    ✓ [ERC721] Verifies that I can't accept a fulfillment paying out in tokens I dont have (531ms)
    ✓ [ERC721] Verifies that accepting a fulfillment emits an event (628ms)
    ✓ [ERC721] Verifies that I can fulfill and accept a bounty simultaneously (582ms)
    ✓ [ERC721] Verifies that I can change all of a bounty's info (385ms)
    ✓ [ERC721] Verifies that I can't change an out of bounds bounty (384ms)
    ✓ [ERC721] Verifies that I can't change a bounty if I'm not an issuer' (355ms)
    ✓ [ERC721] Verifies that I can change the issuer of my bounty (356ms)
    ✓ [ERC721] Verifies that I can't change the issuer of an out of bounds bounty (325ms)
    ✓ [ERC721] Verifies that I can't change the issuer of a bounty if I didn't issue it (462ms)
    ✓ [ERC721] Verifies that I can't the issuer with an out of bounds issuer ID (324ms)
    ✓ [ERC721] Verifies that I can't the issuer changing an out of bounds issuer ID (346ms)
    ✓ [ERC721] Verifies that changing a bounty's issuer emits an event (388ms)
    ✓ [ERC721] Verifies that I can change the approver of my bounty (357ms)
    ✓ [ERC721] Verifies that I can't change the approver of an out of bounds bounty (323ms)
    ✓ [ERC721] Verifies that I can't change the approver of a bounty if I didn't issue it (348ms)
    ✓ [ERC721] Verifies that I can't the issuer with an out of bounds issuer ID (389ms)
    ✓ [ERC721] Verifies that I can't the issuer changing an out of bounds approver ID (351ms)
    ✓ [ERC721] Verifies that changing a bounty's approver emits an event (329ms)
    ✓ [ERC721] Verifies that I can change the data of my bounty (326ms)
    ✓ [ERC721] Verifies that I can't change the data of an out of bounds bounty (385ms)
    ✓ [ERC721] Verifies that I can't change the data of a bounty if I didn't issue it (349ms)
    ✓ [ERC721] Verifies that I can't change the data with an out of bounds issuer ID (338ms)
    ✓ [ERC721] Verifies that changing a bounty's data emits an event (325ms)
    ✓ [ERC721] Verifies that I can change the deadline of my bounty (399ms)
    ✓ [ERC721] Verifies that I can't change the deadline of an out of bounds bounty (362ms)
    ✓ [ERC721] Verifies that I can't change the deadline of a bounty if I didn't issue it (337ms)
    ✓ [ERC721] Verifies that I can't change the deadline with an out of bounds issuer ID (322ms)
    ✓ [ERC721] Verifies that changing a bounty's deadline emits an event (361ms)
    ✓ [ERC721] Verifies that I can add issuers to my bounty (389ms)
    ✓ [ERC721] Verifies that I can't add issuers to an out of bounds bounty (312ms)
    ✓ [ERC721] Verifies that I can't add issuers to a bounty if I didn't issue it (341ms)
    ✓ [ERC721] Verifies that I can't add issuers with an out of bounds issuer ID (371ms)
    ✓ [ERC721] Verifies that adding issuers to a bounty emits an event (324ms)
    ✓ [ERC721] Verifies that I can replace the issuers of my bounty (349ms)
    ✓ [ERC721] Verifies that I can't replace issuers for an out of bounds bounty (326ms)
    ✓ [ERC721] Verifies that I can't replace issuers for a bounty if I didn't issue it (380ms)
    ✓ [ERC721] Verifies that I can't replace issuers with an out of bounds issuer ID (323ms)
    ✓ [ERC721] Verifies that replacing issuers of a bounty emits an event (326ms)
    ✓ [ERC721] Verifies that I can add approvers to my bounty (367ms)
    ✓ [ERC721] Verifies that I can't add approvers to an out of bounds bounty (376ms)
    ✓ [ERC721] Verifies that I can't add approvers to a bounty if I didn't issue it (338ms)
    ✓ [ERC721] Verifies that I can't add approvers with an out of bounds issuer ID (333ms)
    ✓ [ERC721] Verifies that adding approvers to a bounty emits an event (379ms)
    ✓ [ERC721] Verifies that I can replace the approvers of my bounty (357ms)
    ✓ [ERC721] Verifies that I can't replace approvers for an out of bounds bounty (336ms)
    ✓ [ERC721] Verifies that I can't replace approvers for a bounty if I didn't issue it (362ms)
    ✓ [ERC721] Verifies that I can't replace approvers with an out of bounds issuer ID (387ms)
    ✓ [ERC721] Verifies that replacing approvers of a bounty emits an event (333ms)

  Contract: StandardBounties
    ✓ [ETH] Verifies that the StandardBounties registry works (73ms)
    ✓ [ETH] Verifies that I can issue a bounty paying in ETH without locking up funds (164ms)
    ✓ [ETH] Verifies that I can issue a bounty paying in ETH while locking up funds (193ms)
    ✓ [ETH] Verifies that I can't issue a bounty contributing more than the deposit amount (310ms)
    ✓ [ETH] Verifies that I can't issue a bounty contributing less than the deposit amount (235ms)
    ✓ [ETH] Verifies that I can contribute to a bounty in ETH (233ms)
    ✓ [ETH] Verifies that I can't contribute to a bounty which is out of bounds (172ms)
    ✓ [ETH] Verifies that I can't contribute to a bounty and send less than the deposit amount (220ms)
    ✓ [ETH] Verifies that contributing emits an event (191ms)
    ✓ [ETH] Verifies that I can refund a contribution in ETH (348ms)
    ✓ [ETH] Verifies that I can't refund a contribution to a bounty which is out of bounds (301ms)
    ✓ [ETH] Verifies that I can't refund a contribution which is out of bounds (311ms)
    ✓ [ETH] Verifies that I can't refund a contribution which isn't mine (419ms)
    ✓ [ETH] Verifies that I can't refund a contribution which has already been refunded (412ms)
    ✓ [ETH] Verifies that I can't refund a contribution before the deadline has elapsed (294ms)
    ✓ [ETH] Verifies that refunding a contribution emits an event (335ms)
    ✓ [ETH] Verifies that I can perform an action for a bounty (203ms)
    ✓ [ETH] Verifies that I can't perform an action for an out of bounds bounty (239ms)
    ✓ [ETH] Verifies that performing an action emits an event (172ms)
    ✓ [ETH] Verifies that I can fulfill a bounty (216ms)
    ✓ [ETH] Verifies that I can't fulfill an out of bounds bounty (186ms)
    ✓ [ETH] Verifies that I can't fulfill a bounty after the deadline has elapsed (229ms)
    ✓ [ETH] Verifies that I can't fulfill a bounty with 0 fulfillers (254ms)
    ✓ [ETH] Verifies that fulfilling a bounty emits an event (194ms)
    ✓ [ETH] Verifies that I can update a fulfillment (277ms)
    ✓ [ETH] Verifies that I can't update a fulfillment for an out of bounds bounty (239ms)
    ✓ [ETH] Verifies that I can't update an out of bounds fulfillment (254ms)
    ✓ [ETH] Verifies that I can't update a fulfillment which was submitted by someone else (234ms)
    ✓ [ETH] Verifies that updating a fulfillment emits an event (248ms)
    ✓ [ETH] Verifies that I can accept a fulfillment as an issuer (388ms)
    ✓ [ETH] Verifies that I can accept a fulfillment paying different amounts to different fulfillers (343ms)
    ✓ [ETH] Verifies that I can accept a fulfillment as an approver (343ms)
    ✓ [ETH] Verifies that I can't accept a fulfillment on an out of bounds bounty (281ms)
    ✓ [ETH] Verifies that I can't accept a fulfillment which is out of bounds (291ms)
    ✓ [ETH] Verifies that I can't accept a fulfillment if I'm not an approver (342ms)
    ✓ [ETH] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (319ms)
    ✓ [ETH] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (290ms)
    ✓ [ETH] Verifies that accepting a fulfillment emits an event (316ms)
    ✓ [ETH] Verifies that I can fulfill and accept a bounty simultaneously (326ms)
    ✓ [ETH] Verifies that I can change all of a bounty's info (321ms)
    ✓ [ETH] Verifies that I can't change an out of bounds bounty (231ms)
    ✓ [ETH] Verifies that I can't change a bounty if I'm not an issuer' (251ms)
    ✓ [ETH] Verifies that I can change the issuer of my bounty (254ms)
    ✓ [ETH] Verifies that I can't change the issuer of an out of bounds bounty (220ms)
    ✓ [ETH] Verifies that I can't change the issuer of a bounty if I didn't issue it (306ms)
    ✓ [ETH] Verifies that I can't the issuer with an out of bounds issuer ID (234ms)
    ✓ [ETH] Verifies that I can't the issuer changing an out of bounds issuer ID (243ms)
    ✓ [ETH] Verifies that changing a bounty's issuer emits an event (231ms)
    ✓ [ETH] Verifies that I can change the approver of my bounty (258ms)
    ✓ [ETH] Verifies that I can't change the approver of an out of bounds bounty (273ms)
    ✓ [ETH] Verifies that I can't change the approver of a bounty if I didn't issue it (245ms)
    ✓ [ETH] Verifies that I can't the issuer with an out of bounds issuer ID (229ms)
    ✓ [ETH] Verifies that I can't the issuer changing an out of bounds approver ID (254ms)
    ✓ [ETH] Verifies that changing a bounty's approver emits an event (235ms)
    ✓ [ETH] Verifies that I can change the data of my bounty (274ms)
    ✓ [ETH] Verifies that I can't change the data of an out of bounds bounty (225ms)
    ✓ [ETH] Verifies that I can't change the data of a bounty if I didn't issue it (245ms)
    ✓ [ETH] Verifies that I can't change the data with an out of bounds issuer ID (305ms)
    ✓ [ETH] Verifies that changing a bounty's data emits an event (229ms)
    ✓ [ETH] Verifies that I can change the deadline of my bounty (255ms)
    ✓ [ETH] Verifies that I can't change the deadline of an out of bounds bounty (267ms)
    ✓ [ETH] Verifies that I can't change the deadline of a bounty if I didn't issue it (242ms)
    ✓ [ETH] Verifies that I can't change the deadline with an out of bounds issuer ID (231ms)
    ✓ [ETH] Verifies that changing a bounty's deadline emits an event (223ms)
    ✓ [ETH] Verifies that I can add issuers to my bounty (258ms)
    ✓ [ETH] Verifies that I can't add issuers to an out of bounds bounty (274ms)
    ✓ [ETH] Verifies that I can't add issuers to a bounty if I didn't issue it (251ms)
    ✓ [ETH] Verifies that I can't add issuers with an out of bounds issuer ID (236ms)
    ✓ [ETH] Verifies that adding issuers to a bounty emits an event (236ms)
    ✓ [ETH] Verifies that I can replace the issuers of my bounty (256ms)
    ✓ [ETH] Verifies that I can't replace issuers for an out of bounds bounty (293ms)
    ✓ [ETH] Verifies that I can't replace issuers for a bounty if I didn't issue it (244ms)
    ✓ [ETH] Verifies that I can't replace issuers with an out of bounds issuer ID (228ms)
    ✓ [ETH] Verifies that replacing issuers of a bounty emits an event (220ms)
    ✓ [ETH] Verifies that I can add approvers to my bounty (253ms)
    ✓ [ETH] Verifies that I can't add approvers to an out of bounds bounty (266ms)
    ✓ [ETH] Verifies that I can't add approvers to a bounty if I didn't issue it (275ms)
    ✓ [ETH] Verifies that I can't add approvers with an out of bounds issuer ID (252ms)
    ✓ [ETH] Verifies that adding approvers to a bounty emits an event (250ms)
    ✓ [ETH] Verifies that I can replace the approvers of my bounty (263ms)
    ✓ [ETH] Verifies that I can't replace approvers for an out of bounds bounty (223ms)
    ✓ [ETH] Verifies that I can't replace approvers for a bounty if I didn't issue it (304ms)
    ✓ [ETH] Verifies that I can't replace approvers with an out of bounds issuer ID (240ms)
    ✓ [ETH] Verifies that replacing approvers of a bounty emits an event (240ms)


  255 passing (1m)

----------------------------|----------|----------|----------|----------|----------------|
File                        |  % Stmts | % Branch |  % Funcs |  % Lines |Uncovered Lines |
----------------------------|----------|----------|----------|----------|----------------|
 contracts/                 |    49.12 |    37.67 |    59.26 |    43.75 |                |
  BountiesMetaTxRelayer.sol |        0 |        0 |        0 |        0 |... 563,564,566 |
  StandardBounties.sol      |    93.33 |    80.88 |    94.12 |    94.23 |... 312,313,698 |
----------------------------|----------|----------|----------|----------|----------------|
All files                   |    49.12 |    37.67 |    59.26 |    43.75 |                |
----------------------------|----------|----------|----------|----------|----------------|

Istanbul coverage reports generated
Cleaning up...
Shutting down testrpc-sc (pid 8152)
Done.
```