# Version used

```console
$ npx truffle version 
Truffle v5.0.8 (core: 5.0.8)
Solidity - 0.5.0 (solc-js)
Node v8.15.1
Web3.js v1.0.0-beta.37
````

---

# Test Suite - Output

The test-suite yields six errors due to a call to a non-existent function `getBountyFulfillments()` in contract `StandardBounties`.

```console

> StandardBounties@0.1.0 test ./bounties-audit-2019-03
> truffle test

No secrets.json found. If you are trying to publish EPM this will fail. Otherwise, you can ignore this message!
Using network 'test'.


Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.


  Contract: StandardBounties
    ✓ [ERC20] Verifies that the StandardBounties registry works (5320382 gas)
    ✓ [ERC20] Verifies that I can issue a bounty paying in ERC20 tokens without locking up funds (6684587 gas)
    ✓ [ERC20] Verifies that I can issue a bounty paying in ERC20 tokens while locking up funds (6856381 gas)
    ✓ [ERC20] Verifies that I can't issue a bounty in tokens contributing both tokens and ETH (6816967 gas)
    ✓ [ERC20] Verifies that I can't issue a bounty contributing less than the deposit amount (6820749 gas)
    ✓ [ERC20] Verifies that I can contribute to a bounty in ERC20 tokens (6961863 gas)
    ✓ [ERC20] Verifies that I can't contribute to a bounty which is out of bounds (6753955 gas)
    ✓ [ERC20] Verifies that I can't contribute to a bounty and send less than the deposit amount (6844782 gas)
    ✓ [ERC20] Verifies that I can't contribute to a bounty and send both tokens and ETH (6840860 gas)
    ✓ [ERC20] Verifies that contributing emits an event (6880198 gas)
    ✓ [ERC20] Verifies that I can refund a contribution in ERC20 tokens (6953865 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution to a bounty which is out of bounds (6937054 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution which is out of bounds (6937381 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution which isn't mine (7139696 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution which has already been refunded (6979916 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution before the deadline has elapsed (6906561 gas)
    ✓ [ERC20] Verifies that refunding a contribution emits an event (6953865 gas)
    ✓ [ERC20] Verifies that I can perform an action for a bounty (6712705 gas)
    ✓ [ERC20] Verifies that I can't perform an action for an out of bounds bounty (6709968 gas)
    ✓ [ERC20] Verifies that performing an action emits an event (6712705 gas)

    1) [ERC20] Verifies that I can fulfill a bounty

    Events emitted during test:
    ---------------------------

    BountyIssued(_bountyId: 0 (uint256), _creator: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address), _issuers: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address[]), _approvers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _deadline: 2528821098 (uint256), _token: 0xE53A3Bac98c9D304a3bB6Ce34ed37923BC25117a (address), _tokenVersion: 20 (uint256))
    BountyFulfilled(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _submitter: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address))

    ---------------------------
    ✓ [ERC20] Verifies that I can't fulfill an out of bounds bounty (6713887 gas)
    ✓ [ERC20] Verifies that I can't fulfill a bounty after the deadline has elapsed (6885673 gas)
    ✓ [ERC20] Verifies that I can't fulfill a bounty with 0 fulfillers (6755938 gas)
    ✓ [ERC20] Verifies that fulfilling a bounty emits an event (6821375 gas)

    2) [ERC20] Verifies that I can update a fulfillment

    Events emitted during test:
    ---------------------------

    BountyIssued(_bountyId: 0 (uint256), _creator: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address), _issuers: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address[]), _approvers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _deadline: 2528821098 (uint256), _token: 0x3c43493ca8e7BDFA174ee77a05bC44f1986fDA41 (address), _tokenVersion: 20 (uint256))
    BountyFulfilled(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _submitter: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address))
    FulfillmentUpdated(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0x821aEa9a577a9b44299B9c15c88cf3087F3b5544,0x0d1d4e623D10F9FBA5Db95830F7d3839406C6AF2 (address[]), _data: data2 (string))

    ---------------------------
    ✓ [ERC20] Verifies that I can't update a fulfillment for an out of bounds bounty (6851076 gas)
    ✓ [ERC20] Verifies that I can't update an out of bounds fulfillment (6851467 gas)
    ✓ [ERC20] Verifies that I can't update a fulfillment which was submitted by someone else (6851102 gas)
    ✓ [ERC20] Verifies that updating a fulfillment emits an event (6873124 gas)
    ✓ [ERC20] Verifies that I can accept a fulfillment as an issuer (7113324 gas)
    ✓ [ERC20] Verifies that I can accept a fulfillment paying different amounts to different fulfillers (7113324 gas)
    ✓ [ERC20] Verifies that I can accept a fulfillment as an approver (7113388 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment on an out of bounds bounty (7041384 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment which is out of bounds (7041647 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment if I'm not an approver (7042239 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (7062910 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (7042303 gas)
    ✓ [ERC20] Verifies that accepting a fulfillment emits an event (7090827 gas)
    ✓ [ERC20] Verifies that I can fulfill and accept a bounty simultaneously (7090499 gas)
    ✓ [ERC20] Verifies that I can change all of a bounty's info (6928681 gas)
    ✓ [ERC20] Verifies that I can't change an out of bounds bounty (6889232 gas)
    ✓ [ERC20] Verifies that I can't change a bounty if I'm not an issuer' (6890168 gas)
    ✓ [ERC20] Verifies that I can change the issuer of my bounty (6891699 gas)
    ✓ [ERC20] Verifies that I can't change the issuer of an out of bounds bounty (6882384 gas)
    ✓ [ERC20] Verifies that I can't change the issuer of a bounty if I didn't issue it (6883664 gas)
    ✓ [ERC20] Verifies that I can't the issuer with an out of bounds issuer ID (6882739 gas)
    ✓ [ERC20] Verifies that I can't the issuer changing an out of bounds issuer ID (6883083 gas)
    ✓ [ERC20] Verifies that changing a bounty's issuer emits an event (6891699 gas)
    ✓ [ERC20] Verifies that I can change the approver of my bounty (6891392 gas)
    ✓ [ERC20] Verifies that I can't change the approver of an out of bounds bounty (6882142 gas)
    ✓ [ERC20] Verifies that I can't change the approver of a bounty if I didn't issue it (6883078 gas)
    ✓ [ERC20] Verifies that I can't the issuer with an out of bounds issuer ID (6882497 gas)
    ✓ [ERC20] Verifies that I can't the issuer changing an out of bounds approver ID (6883433 gas)
    ✓ [ERC20] Verifies that changing a bounty's approver emits an event (6891456 gas)
    ✓ [ERC20] Verifies that I can change the data of my bounty (6885614 gas)
    ✓ [ERC20] Verifies that I can't change the data of an out of bounds bounty (6881780 gas)
    ✓ [ERC20] Verifies that I can't change the data of a bounty if I didn't issue it (6882652 gas)
    ✓ [ERC20] Verifies that I can't change the data with an out of bounds issuer ID (6882135 gas)
    ✓ [ERC20] Verifies that changing a bounty's data emits an event (6885486 gas)
    ✓ [ERC20] Verifies that I can change the deadline of my bounty (6889062 gas)
    ✓ [ERC20] Verifies that I can't change the deadline of an out of bounds bounty (6881108 gas)
    ✓ [ERC20] Verifies that I can't change the deadline of a bounty if I didn't issue it (6881980 gas)
    ✓ [ERC20] Verifies that I can't change the deadline with an out of bounds issuer ID (6881463 gas)
    ✓ [ERC20] Verifies that changing a bounty's deadline emits an event (6889126 gas)
    ✓ [ERC20] Verifies that I can add issuers to my bounty (6940826 gas)
    ✓ [ERC20] Verifies that I can't add issuers to an out of bounds bounty (6884842 gas)
    ✓ [ERC20] Verifies that I can't add issuers to a bounty if I didn't issue it (6885778 gas)
    ✓ [ERC20] Verifies that I can't add issuers with an out of bounds issuer ID (6885197 gas)
    ✓ [ERC20] Verifies that adding issuers to a bounty emits an event (6940826 gas)
    ✓ [ERC20] Verifies that I can replace the issuers of my bounty (6920289 gas)
    ✓ [ERC20] Verifies that I can't replace issuers for an out of bounds bounty (6884688 gas)
    ✓ [ERC20] Verifies that I can't replace issuers for a bounty if I didn't issue it (6885560 gas)
    ✓ [ERC20] Verifies that I can't replace issuers with an out of bounds issuer ID (6884979 gas)
    ✓ [ERC20] Verifies that replacing issuers of a bounty emits an event (6920289 gas)
    ✓ [ERC20] Verifies that I can add approvers to my bounty (6940518 gas)
    ✓ [ERC20] Verifies that I can't add approvers to an out of bounds bounty (6884470 gas)
    ✓ [ERC20] Verifies that I can't add approvers to a bounty if I didn't issue it (6885470 gas)
    ✓ [ERC20] Verifies that I can't add approvers with an out of bounds issuer ID (6884889 gas)
    ✓ [ERC20] Verifies that adding approvers to a bounty emits an event (6940518 gas)
    ✓ [ERC20] Verifies that I can replace the approvers of my bounty (6905179 gas)
    ✓ [ERC20] Verifies that I can't replace approvers for an out of bounds bounty (6884578 gas)
    ✓ [ERC20] Verifies that I can't replace approvers for a bounty if I didn't issue it (6885514 gas)
    ✓ [ERC20] Verifies that I can't replace approvers with an out of bounds issuer ID (6884933 gas)
    ✓ [ERC20] Verifies that replacing approvers of a bounty emits an event (6905115 gas)

  Contract: StandardBounties
    ✓ [ERC721] Verifies that the StandardBounties registry works (5320382 gas)
    ✓ [ERC721] Verifies that I can issue a bounty paying in ERC721 tokens without locking up funds (7270882 gas)
    ✓ [ERC721] Verifies that I can issue a bounty paying in ERC721 tokens while locking up funds (7492684 gas)
    ✓ [ERC721] Verifies that I can't issue a bounty in tokens contributing both tokens and ETH (7470331 gas)
    ✓ [ERC721] Verifies that I can't issue a bounty contributing less than the deposit amount (7473510 gas)
    ✓ [ERC721] Verifies that I can contribute to a bounty in ERC721 tokens (7693303 gas)
    ✓ [ERC721] Verifies that I can't contribute to a bounty which is out of bounds (7407009 gas)
    ✓ [ERC721] Verifies that I can't contribute to a bounty and send less than the deposit amount (7497543 gas)
    ✓ [ERC721] Verifies that I can't contribute to a bounty and send both tokens and ETH (7494352 gas)
    ✓ [ERC721] Verifies that contributing emits an event (7516437 gas)
    ✓ [ERC721] Verifies that I can refund a contribution in ERC721 tokens (7620456 gas)
    ✓ [ERC721] Verifies that I can refund multiple contributions in ERC721 tokens (7907349 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution to a bounty which is out of bounds (7573293 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution which is out of bounds (7573684 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution which isn't mine (7774912 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution which has already been refunded (7646507 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution before the deadline has elapsed (7542864 gas)
    ✓ [ERC721] Verifies that refunding a contribution emits an event (7620456 gas)
    ✓ [ERC721] Verifies that I can perform an action for a bounty (7299000 gas)
    ✓ [ERC721] Verifies that I can't perform an action for an out of bounds bounty (7296263 gas)
    ✓ [ERC721] Verifies that performing an action emits an event (7299000 gas)

    3) [ERC721] Verifies that I can fulfill a bounty

    Events emitted during test:
    ---------------------------

    BountyIssued(_bountyId: 0 (uint256), _creator: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address), _issuers: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address[]), _approvers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _deadline: 2528821098 (uint256), _token: 0xe94fa3040d20a01a1b8f42De7c430A11c27e2524 (address), _tokenVersion: 721 (uint256))
    BountyFulfilled(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _submitter: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address))

    ---------------------------
    ✓ [ERC721] Verifies that I can't fulfill an out of bounds bounty (7300182 gas)
    ✓ [ERC721] Verifies that I can't fulfill a bounty after the deadline has elapsed (7522040 gas)
    ✓ [ERC721] Verifies that I can't fulfill a bounty with 0 fulfillers (7518906 gas)
    ✓ [ERC721] Verifies that fulfilling a bounty emits an event (7407670 gas)

    4) [ERC721] Verifies that I can update a fulfillment

    Events emitted during test:
    ---------------------------

    BountyIssued(_bountyId: 0 (uint256), _creator: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address), _issuers: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address[]), _approvers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _deadline: 2528821098 (uint256), _token: 0x13C72f3c8bC7AfC2609a9da61a0d185c50085Cf8 (address), _tokenVersion: 721 (uint256))
    BountyFulfilled(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _submitter: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address))
    FulfillmentUpdated(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0x821aEa9a577a9b44299B9c15c88cf3087F3b5544,0x0d1d4e623D10F9FBA5Db95830F7d3839406C6AF2 (address[]), _data: data2 (string))

    ---------------------------
    ✓ [ERC721] Verifies that I can't update a fulfillment for an out of bounds bounty (7437435 gas)
    ✓ [ERC721] Verifies that I can't update an out of bounds fulfillment (7437762 gas)
    ✓ [ERC721] Verifies that I can't update a fulfillment which was submitted by someone else (7437333 gas)
    ✓ [ERC721] Verifies that updating a fulfillment emits an event (7459419 gas)
    ✓ [ERC721] Verifies that I can accept a fulfillment paying different 721 tokens to different fulfillers (7980810 gas)
    ✓ [ERC721] Verifies that I can accept a fulfillment as an approver (7980874 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment on an out of bounds bounty (7878306 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment which is out of bounds (7878633 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment if I'm not an approver (7879161 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (7899832 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (7879225 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment paying out in tokens I dont have (7879097 gas)
    ✓ [ERC721] Verifies that accepting a fulfillment emits an event (7980874 gas)
    ✓ [ERC721] Verifies that I can fulfill and accept a bounty simultaneously (7957991 gas)
    ✓ [ERC721] Verifies that I can change all of a bounty's info (7564984 gas)
    ✓ [ERC721] Verifies that I can't change an out of bounds bounty (7525535 gas)
    ✓ [ERC721] Verifies that I can't change a bounty if I'm not an issuer' (7526407 gas)
    ✓ [ERC721] Verifies that I can change the issuer of my bounty (7528002 gas)
    ✓ [ERC721] Verifies that I can't change the issuer of an out of bounds bounty (7518687 gas)
    ✓ [ERC721] Verifies that I can't change the issuer of a bounty if I didn't issue it (7519967 gas)
    ✓ [ERC721] Verifies that I can't the issuer with an out of bounds issuer ID (7519042 gas)
    ✓ [ERC721] Verifies that I can't the issuer changing an out of bounds issuer ID (7519386 gas)
    ✓ [ERC721] Verifies that changing a bounty's issuer emits an event (7528002 gas)
    ✓ [ERC721] Verifies that I can change the approver of my bounty (7527759 gas)
    ✓ [ERC721] Verifies that I can't change the approver of an out of bounds bounty (7518381 gas)
    ✓ [ERC721] Verifies that I can't change the approver of a bounty if I didn't issue it (7519381 gas)
    ✓ [ERC721] Verifies that I can't the issuer with an out of bounds issuer ID (7518800 gas)
    ✓ [ERC721] Verifies that I can't the issuer changing an out of bounds approver ID (7519800 gas)
    ✓ [ERC721] Verifies that changing a bounty's approver emits an event (7527695 gas)
    ✓ [ERC721] Verifies that I can change the data of my bounty (7521917 gas)
    ✓ [ERC721] Verifies that I can't change the data of an out of bounds bounty (7518083 gas)
    ✓ [ERC721] Verifies that I can't change the data of a bounty if I didn't issue it (7519019 gas)
    ✓ [ERC721] Verifies that I can't change the data with an out of bounds issuer ID (7518438 gas)
    ✓ [ERC721] Verifies that changing a bounty's data emits an event (7521917 gas)
    ✓ [ERC721] Verifies that I can change the deadline of my bounty (7525429 gas)
    ✓ [ERC721] Verifies that I can't change the deadline of an out of bounds bounty (7517411 gas)
    ✓ [ERC721] Verifies that I can't change the deadline of a bounty if I didn't issue it (7518347 gas)
    ✓ [ERC721] Verifies that I can't change the deadline with an out of bounds issuer ID (7517766 gas)
    ✓ [ERC721] Verifies that changing a bounty's deadline emits an event (7525429 gas)
    ✓ [ERC721] Verifies that I can add issuers to my bounty (7577129 gas)
    ✓ [ERC721] Verifies that I can't add issuers to an out of bounds bounty (7521145 gas)
    ✓ [ERC721] Verifies that I can't add issuers to a bounty if I didn't issue it (7522081 gas)
    ✓ [ERC721] Verifies that I can't add issuers with an out of bounds issuer ID (7521500 gas)
    ✓ [ERC721] Verifies that adding issuers to a bounty emits an event (7577065 gas)
    ✓ [ERC721] Verifies that I can replace the issuers of my bounty (7556592 gas)
    ✓ [ERC721] Verifies that I can't replace issuers for an out of bounds bounty (7520991 gas)
    ✓ [ERC721] Verifies that I can't replace issuers for a bounty if I didn't issue it (7521863 gas)
    ✓ [ERC721] Verifies that I can't replace issuers with an out of bounds issuer ID (7521346 gas)
    ✓ [ERC721] Verifies that replacing issuers of a bounty emits an event (7556592 gas)
    ✓ [ERC721] Verifies that I can add approvers to my bounty (7576821 gas)
    ✓ [ERC721] Verifies that I can't add approvers to an out of bounds bounty (7520837 gas)
    ✓ [ERC721] Verifies that I can't add approvers to a bounty if I didn't issue it (7521773 gas)
    ✓ [ERC721] Verifies that I can't add approvers with an out of bounds issuer ID (7521192 gas)
    ✓ [ERC721] Verifies that adding approvers to a bounty emits an event (7576821 gas)
    ✓ [ERC721] Verifies that I can replace the approvers of my bounty (7541482 gas)
    ✓ [ERC721] Verifies that I can't replace approvers for an out of bounds bounty (7520881 gas)
    ✓ [ERC721] Verifies that I can't replace approvers for a bounty if I didn't issue it (7521817 gas)
    ✓ [ERC721] Verifies that I can't replace approvers with an out of bounds issuer ID (7521172 gas)
    ✓ [ERC721] Verifies that replacing approvers of a bounty emits an event (7541418 gas)

  Contract: StandardBounties
    ✓ [ETH] Verifies that the StandardBounties registry works (5320382 gas)
    ✓ [ETH] Verifies that I can issue a bounty paying in ETH without locking up funds (5513008 gas)
    ✓ [ETH] Verifies that I can issue a bounty paying in ETH while locking up funds (5602794 gas)
    ✓ [ETH] Verifies that I can't issue a bounty contributing more than the deposit amount (5599949 gas)
    ✓ [ETH] Verifies that I can't issue a bounty contributing less than the deposit amount (5599949 gas)
    ✓ [ETH] Verifies that I can contribute to a bounty in ETH (5686394 gas)
    ✓ [ETH] Verifies that I can't contribute to a bounty which is out of bounds (5537247 gas)
    ✓ [ETH] Verifies that I can't contribute to a bounty and send less than the deposit amount (5623970 gas)
    ✓ [ETH] Verifies that contributing emits an event (5626608 gas)
    ✓ [ETH] Verifies that I can refund a contribution in ETH (5706798 gas)
    ✓ [ETH] Verifies that I can't refund a contribution to a bounty which is out of bounds (5683464 gas)
    ✓ [ETH] Verifies that I can't refund a contribution which is out of bounds (5683791 gas)
    ✓ [ETH] Verifies that I can't refund a contribution which isn't mine (5768000 gas)
    ✓ [ETH] Verifies that I can't refund a contribution which has already been refunded (5732849 gas)
    ✓ [ETH] Verifies that I can't refund a contribution before the deadline has elapsed (5652971 gas)
    ✓ [ETH] Verifies that refunding a contribution emits an event (5706798 gas)
    ✓ [ETH] Verifies that I can perform an action for a bounty (5541126 gas)
    ✓ [ETH] Verifies that I can't perform an action for an out of bounds bounty (5538389 gas)
    ✓ [ETH] Verifies that performing an action emits an event (5541126 gas)

    5) [ETH] Verifies that I can fulfill a bounty

    Events emitted during test:
    ---------------------------

    BountyIssued(_bountyId: 0 (uint256), _creator: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address), _issuers: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address[]), _approvers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _deadline: 2528821098 (uint256), _token: 0x0000000000000000000000000000000000000000 (address), _tokenVersion: 0 (uint256))
    BountyFulfilled(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _submitter: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address))

    ---------------------------
    ✓ [ETH] Verifies that I can't fulfill an out of bounds bounty (5542308 gas)
    ✓ [ETH] Verifies that I can't fulfill a bounty after the deadline has elapsed (5632150 gas)
    ✓ [ETH] Verifies that I can't fulfill a bounty with 0 fulfillers (5539230 gas)
    ✓ [ETH] Verifies that fulfilling a bounty emits an event (5649796 gas)

    6) [ETH] Verifies that I can update a fulfillment

    Events emitted during test:
    ---------------------------

    BountyIssued(_bountyId: 0 (uint256), _creator: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address), _issuers: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address[]), _approvers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _deadline: 2528821098 (uint256), _token: 0x0000000000000000000000000000000000000000 (address), _tokenVersion: 0 (uint256))
    BountyFulfilled(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0xf17f52151EbEF6C7334FAD080c5704D77216b732,0xC5fdf4076b8F3A5357c5E395ab970B5B54098Fef (address[]), _data: data (string), _submitter: 0x627306090abaB3A6e1400e9345bC60c78a8BEf57 (address))
    FulfillmentUpdated(_bountyId: 0 (uint256), _fulfillmentId: 0 (uint256), _fulfillers: 0x821aEa9a577a9b44299B9c15c88cf3087F3b5544,0x0d1d4e623D10F9FBA5Db95830F7d3839406C6AF2 (address[]), _data: data2 (string))

    ---------------------------
    ✓ [ETH] Verifies that I can't update a fulfillment for an out of bounds bounty (5679561 gas)
    ✓ [ETH] Verifies that I can't update an out of bounds fulfillment (5679888 gas)
    ✓ [ETH] Verifies that I can't update a fulfillment which was submitted by someone else (5679523 gas)
    ✓ [ETH] Verifies that updating a fulfillment emits an event (5701609 gas)
    ✓ [ETH] Verifies that I can accept a fulfillment as an issuer (5827783 gas)
    ✓ [ETH] Verifies that I can accept a fulfillment paying different amounts to different fulfillers (5827783 gas)
    ✓ [ETH] Verifies that I can accept a fulfillment as an approver (5827847 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment on an out of bounds bounty (5787797 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment which is out of bounds (5788124 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment if I'm not an approver (5788716 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (5809323 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (5788716 gas)
    ✓ [ETH] Verifies that accepting a fulfillment emits an event (5805286 gas)
    ✓ [ETH] Verifies that I can fulfill and accept a bounty simultaneously (5804964 gas)
    ✓ [ETH] Verifies that I can change all of a bounty's info (5675094 gas)
    ✓ [ETH] Verifies that I can't change an out of bounds bounty (5635645 gas)
    ✓ [ETH] Verifies that I can't change a bounty if I'm not an issuer' (5636581 gas)
    ✓ [ETH] Verifies that I can change the issuer of my bounty (5638112 gas)
    ✓ [ETH] Verifies that I can't change the issuer of an out of bounds bounty (5628797 gas)
    ✓ [ETH] Verifies that I can't change the issuer of a bounty if I didn't issue it (5630077 gas)
    ✓ [ETH] Verifies that I can't the issuer with an out of bounds issuer ID (5629152 gas)
    ✓ [ETH] Verifies that I can't the issuer changing an out of bounds issuer ID (5629496 gas)
    ✓ [ETH] Verifies that changing a bounty's issuer emits an event (5638112 gas)
    ✓ [ETH] Verifies that I can change the approver of my bounty (5637869 gas)
    ✓ [ETH] Verifies that I can't change the approver of an out of bounds bounty (5628555 gas)
    ✓ [ETH] Verifies that I can't change the approver of a bounty if I didn't issue it (5629491 gas)
    ✓ [ETH] Verifies that I can't the issuer with an out of bounds issuer ID (5628910 gas)
    ✓ [ETH] Verifies that I can't the issuer changing an out of bounds approver ID (5629910 gas)
    ✓ [ETH] Verifies that changing a bounty's approver emits an event (5637869 gas)
    ✓ [ETH] Verifies that I can change the data of my bounty (5632027 gas)
    ✓ [ETH] Verifies that I can't change the data of an out of bounds bounty (5628193 gas)
    ✓ [ETH] Verifies that I can't change the data of a bounty if I didn't issue it (5629129 gas)
    ✓ [ETH] Verifies that I can't change the data with an out of bounds issuer ID (5628548 gas)
    ✓ [ETH] Verifies that changing a bounty's data emits an event (5632027 gas)
    ✓ [ETH] Verifies that I can change the deadline of my bounty (5635539 gas)
    ✓ [ETH] Verifies that I can't change the deadline of an out of bounds bounty (5627521 gas)
    ✓ [ETH] Verifies that I can't change the deadline of a bounty if I didn't issue it (5628457 gas)
    ✓ [ETH] Verifies that I can't change the deadline with an out of bounds issuer ID (5627876 gas)
    ✓ [ETH] Verifies that changing a bounty's deadline emits an event (5635539 gas)
    ✓ [ETH] Verifies that I can add issuers to my bounty (5687239 gas)
    ✓ [ETH] Verifies that I can't add issuers to an out of bounds bounty (5631255 gas)
    ✓ [ETH] Verifies that I can't add issuers to a bounty if I didn't issue it (5632191 gas)
    ✓ [ETH] Verifies that I can't add issuers with an out of bounds issuer ID (5631610 gas)
    ✓ [ETH] Verifies that adding issuers to a bounty emits an event (5687239 gas)
    ✓ [ETH] Verifies that I can replace the issuers of my bounty (5666702 gas)
    ✓ [ETH] Verifies that I can't replace issuers for an out of bounds bounty (5631101 gas)
    ✓ [ETH] Verifies that I can't replace issuers for a bounty if I didn't issue it (5632037 gas)
    ✓ [ETH] Verifies that I can't replace issuers with an out of bounds issuer ID (5631456 gas)
    ✓ [ETH] Verifies that replacing issuers of a bounty emits an event (5666702 gas)
    ✓ [ETH] Verifies that I can add approvers to my bounty (5686931 gas)
    ✓ [ETH] Verifies that I can't add approvers to an out of bounds bounty (5630947 gas)
    ✓ [ETH] Verifies that I can't add approvers to a bounty if I didn't issue it (5631883 gas)
    ✓ [ETH] Verifies that I can't add approvers with an out of bounds issuer ID (5631302 gas)
    ✓ [ETH] Verifies that adding approvers to a bounty emits an event (5686931 gas)
    ✓ [ETH] Verifies that I can replace the approvers of my bounty (5651592 gas)
    ✓ [ETH] Verifies that I can't replace approvers for an out of bounds bounty (5630991 gas)
    ✓ [ETH] Verifies that I can't replace approvers for a bounty if I didn't issue it (5631927 gas)
    ✓ [ETH] Verifies that I can't replace approvers with an out of bounds issuer ID (5631346 gas)
    ✓ [ETH] Verifies that replacing approvers of a bounty emits an event (5651592 gas)

·---------------------------------------------------------------------------------|----------------------------·
|                                       Gas                                       ·  Block limit: 6721975 gas  │
················································|·································|·····························
|  Methods                                      ·           6 gwei/gas            ·       140.38 usd/eth       │
·························|······················|··········|··········|···········|··············|··············
|  Contract              ·  Method              ·  Min     ·  Max     ·  Avg      ·  # calls     ·  usd (avg)  │
·························|······················|··········|··········|···········|··············|··············
|  ERC721BasicTokenMock  ·  approve             ·   45626  ·   45690  ·    45684  ·          86  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  ERC721BasicTokenMock  ·  mint                ·   51198  ·   66198  ·    64454  ·          86  ·       0.05  │
·························|······················|··········|··········|···········|··············|··············
|  HumanStandardToken    ·  approve             ·   45001  ·   45129  ·    45118  ·          73  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  HumanStandardToken    ·  transfer            ·       -  ·       -  ·    51095  ·           1  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  acceptFulfillment   ·   65704  ·  128286  ·    94397  ·          11  ·       0.08  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  addApprovers        ·       -  ·       -  ·    84137  ·           6  ·       0.07  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  addIssuers          ·       -  ·       -  ·    84445  ·           6  ·       0.07  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeApprover      ·       -  ·       -  ·    35075  ·           6  ·       0.03  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeBounty        ·       -  ·       -  ·    72300  ·           3  ·       0.06  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeData          ·       -  ·       -  ·    29233  ·           6  ·       0.02  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeDeadline      ·       -  ·       -  ·    32745  ·          25  ·       0.03  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeIssuer        ·       -  ·       -  ·    35318  ·           6  ·       0.03  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  contribute          ·   83600  ·  150482  ·   115426  ·          42  ·       0.10  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  fulfillAndAccept    ·  179673  ·  242191  ·   211162  ·           3  ·       0.18  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  fulfillBounty       ·       -  ·       -  ·   136788  ·          42  ·       0.12  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  issueBounty         ·  192626  ·  373143  ·   296258  ·         240  ·       0.25  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  performAction       ·       -  ·       -  ·    28118  ·           6  ·       0.02  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  refundContribution  ·   40922  ·  101210  ·    57838  ·          11  ·       0.05  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  replaceApprovers    ·       -  ·       -  ·    48798  ·           6  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  replaceIssuers      ·       -  ·       -  ·    63908  ·           6  ·       0.05  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  updateFulfillment   ·       -  ·       -  ·    51813  ·           3  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  Deployments                                  ·                                 ·  % of limit  ·             │
················································|··········|··········|···········|··············|··············
|  ERC721BasicTokenMock                         ·       -  ·       -  ·  1726444  ·      25.7 %  ·       1.45  │
················································|··········|··········|···········|··············|··············
|  HumanStandardToken                           ·       -  ·       -  ·  1140224  ·        17 %  ·       0.96  │
················································|··········|··········|···········|··············|··············
|  StandardBounties                             ·       -  ·       -  ·  5320382  ·      79.1 %  ·       4.48  │
·-----------------------------------------------|----------|----------|-----------|--------------|-------------·

  249 passing (4m)
  6 failing

  1) Contract: StandardBounties
       [ERC20] Verifies that I can fulfill a bounty:
     TypeError: registry.getBountyFulfillments is not a function
      at Context.it (test/StandardBountiesInERC20.js:379:39)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:189:7)

  2) Contract: StandardBounties
       [ERC20] Verifies that I can update a fulfillment:
     TypeError: registry.getBountyFulfillments is not a function
      at Context.it (test/StandardBountiesInERC20.js:461:39)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:189:7)

  3) Contract: StandardBounties
       [ERC721] Verifies that I can fulfill a bounty:
     TypeError: registry.getBountyFulfillments is not a function
      at Context.it (test/StandardBountiesInERC721.js:439:39)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:189:7)

  4) Contract: StandardBounties
       [ERC721] Verifies that I can update a fulfillment:
     TypeError: registry.getBountyFulfillments is not a function
      at Context.it (test/StandardBountiesInERC721.js:523:39)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:189:7)

  5) Contract: StandardBounties
       [ETH] Verifies that I can fulfill a bounty:
     TypeError: registry.getBountyFulfillments is not a function
      at Context.it (test/StandardBountiesInETH.js:313:39)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:189:7)

  6) Contract: StandardBounties
       [ETH] Verifies that I can update a fulfillment:
     TypeError: registry.getBountyFulfillments is not a function
      at Context.it (test/StandardBountiesInETH.js:383:39)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:189:7)
```

# Test Suite - Fix

```diff
diff --git a/test/StandardBountiesInERC20.js b/test/StandardBountiesInERC20.js
index 0dfa1c1..6f1c532 100644
--- a/test/StandardBountiesInERC20.js
+++ b/test/StandardBountiesInERC20.js
@@ -376,7 +376,10 @@ contract('StandardBounties', function(accounts) 

     await registry.fulfillBounty(accounts[0], 0, [accounts[1], accounts[2]], "data");

-    let fulfillments = await registry.getBountyFulfillments(0);
+
+    let bounty = await registry.getBounty(0);
+    let fulfillments = bounty.fulfillments;
+
     assert(fulfillments.length == 1);
     assert(fulfillments[0].fulfillers[0] == accounts[1]);
     assert(fulfillments[0].fulfillers[1] == accounts[2]);
@@ -458,7 +461,9 @@ contract('StandardBounties', function(accounts) {

     await registry.updateFulfillment(accounts[0], 0, 0, [accounts[3], accounts[4]], "data2");

-    let fulfillments = await registry.getBountyFulfillments(0);
+
+    let bounty = await registry.getBounty(0);
+    let fulfillments = bounty.fulfillments;

     assert(fulfillments.length == 1);
     assert(fulfillments[0].fulfillers[0] == accounts[3]);
diff --git a/test/StandardBountiesInERC721.js b/test/StandardBountiesInERC721.js
index 39c3fc1..630ef9c 100644
--- a/test/StandardBountiesInERC721.js
+++ b/test/StandardBountiesInERC721.js
@@ -436,7 +436,10 @@ contract('StandardBounties', function(accounts) {

     await registry.fulfillBounty(accounts[0], 0, [accounts[1], accounts[2]], "data");

-    let fulfillments = await registry.getBountyFulfillments(0);
+
+    let bounty = await registry.getBounty(0);
+    let fulfillments = bounty.fulfillments;
+
     assert(fulfillments.length == 1);
     assert(fulfillments[0].fulfillers[0] == accounts[1]);
     assert(fulfillments[0].fulfillers[1] == accounts[2]);
@@ -520,7 +523,9 @@ contract('StandardBounties', function(accounts) {

     await registry.updateFulfillment(accounts[0], 0, 0, [accounts[3], accounts[4]], "data2");

-    let fulfillments = await registry.getBountyFulfillments(0);
+
+    let bounty = await registry.getBounty(0);
+    let fulfillments = bounty.fulfillments;

     assert(fulfillments.length == 1);
     assert(fulfillments[0].fulfillers[0] == accounts[3]);
diff --git a/test/StandardBountiesInETH.js b/test/StandardBountiesInETH.js
index de9c12b..ca8a027 100644
--- a/test/StandardBountiesInETH.js
+++ b/test/StandardBountiesInETH.js
@@ -310,7 +310,9 @@ contract('StandardBounties', function(accounts) {

     await registry.fulfillBounty(accounts[0], 0, [accounts[1], accounts[2]], "data");

-    let fulfillments = await registry.getBountyFulfillments(0);
+    let bounty = await registry.getBounty(0);
+    let fulfillments = bounty.fulfillments;
+
     assert(fulfillments.length == 1);
     assert(fulfillments[0].fulfillers[0] == accounts[1]);
     assert(fulfillments[0].fulfillers[1] == accounts[2]);
@@ -380,7 +382,8 @@ contract('StandardBounties', function(accounts) {

     await registry.updateFulfillment(accounts[0], 0, 0, [accounts[3], accounts[4]], "data2");

-    let fulfillments = await registry.getBountyFulfillments(0);
+    let bounty = await registry.getBounty(0);
+    let fulfillments = bounty.fulfillments;

     assert(fulfillments.length == 1);
     assert(fulfillments[0].fulfillers[0] == accounts[3]);
```

# Fixed Test Suite - Output 

```console

> StandardBounties@0.1.0 test ./bounties-audit-2019-03
> truffle test

No secrets.json found. If you are trying to publish EPM this will fail. Otherwise, you can ignore this message!
Using network 'test'.


Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.


  Contract: StandardBounties
    ✓ [ERC20] Verifies that the StandardBounties registry works (5320382 gas)
    ✓ [ERC20] Verifies that I can issue a bounty paying in ERC20 tokens without locking up funds (6684587 gas)
    ✓ [ERC20] Verifies that I can issue a bounty paying in ERC20 tokens while locking up funds (6856381 gas)
    ✓ [ERC20] Verifies that I can't issue a bounty in tokens contributing both tokens and ETH (6816967 gas)
    ✓ [ERC20] Verifies that I can't issue a bounty contributing less than the deposit amount (6820749 gas)
    ✓ [ERC20] Verifies that I can contribute to a bounty in ERC20 tokens (6961863 gas)
    ✓ [ERC20] Verifies that I can't contribute to a bounty which is out of bounds (6753955 gas)
    ✓ [ERC20] Verifies that I can't contribute to a bounty and send less than the deposit amount (6844782 gas)
    ✓ [ERC20] Verifies that I can't contribute to a bounty and send both tokens and ETH (6840860 gas)
    ✓ [ERC20] Verifies that contributing emits an event (6880198 gas)
    ✓ [ERC20] Verifies that I can refund a contribution in ERC20 tokens (6953865 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution to a bounty which is out of bounds (6937054 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution which is out of bounds (6937381 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution which isn't mine (7139696 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution which has already been refunded (6979916 gas)
    ✓ [ERC20] Verifies that I can't refund a contribution before the deadline has elapsed (6906561 gas)
    ✓ [ERC20] Verifies that refunding a contribution emits an event (6953865 gas)
    ✓ [ERC20] Verifies that I can perform an action for a bounty (6712705 gas)
    ✓ [ERC20] Verifies that I can't perform an action for an out of bounds bounty (6709968 gas)
    ✓ [ERC20] Verifies that performing an action emits an event (6712705 gas)
    ✓ [ERC20] Verifies that I can fulfill a bounty (6821375 gas)
    ✓ [ERC20] Verifies that I can't fulfill an out of bounds bounty (6713887 gas)
    ✓ [ERC20] Verifies that I can't fulfill a bounty after the deadline has elapsed (6885673 gas)
    ✓ [ERC20] Verifies that I can't fulfill a bounty with 0 fulfillers (6755938 gas)
    ✓ [ERC20] Verifies that fulfilling a bounty emits an event (6821375 gas)
    ✓ [ERC20] Verifies that I can update a fulfillment (6873188 gas)
    ✓ [ERC20] Verifies that I can't update a fulfillment for an out of bounds bounty (6851076 gas)
    ✓ [ERC20] Verifies that I can't update an out of bounds fulfillment (6851467 gas)
    ✓ [ERC20] Verifies that I can't update a fulfillment which was submitted by someone else (6851102 gas)
    ✓ [ERC20] Verifies that updating a fulfillment emits an event (6873124 gas)
    ✓ [ERC20] Verifies that I can accept a fulfillment as an issuer (7113324 gas)
    ✓ [ERC20] Verifies that I can accept a fulfillment paying different amounts to different fulfillers (7113324 gas)
    ✓ [ERC20] Verifies that I can accept a fulfillment as an approver (7113388 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment on an out of bounds bounty (7041384 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment which is out of bounds (7041647 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment if I'm not an approver (7042239 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (7062910 gas)
    ✓ [ERC20] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (7042303 gas)
    ✓ [ERC20] Verifies that accepting a fulfillment emits an event (7090827 gas)
    ✓ [ERC20] Verifies that I can fulfill and accept a bounty simultaneously (7090499 gas)
    ✓ [ERC20] Verifies that I can change all of a bounty's info (6928681 gas)
    ✓ [ERC20] Verifies that I can't change an out of bounds bounty (6889232 gas)
    ✓ [ERC20] Verifies that I can't change a bounty if I'm not an issuer' (6890168 gas)
    ✓ [ERC20] Verifies that I can change the issuer of my bounty (6891699 gas)
    ✓ [ERC20] Verifies that I can't change the issuer of an out of bounds bounty (6882384 gas)
    ✓ [ERC20] Verifies that I can't change the issuer of a bounty if I didn't issue it (6883664 gas)
    ✓ [ERC20] Verifies that I can't the issuer with an out of bounds issuer ID (6882739 gas)
    ✓ [ERC20] Verifies that I can't the issuer changing an out of bounds issuer ID (6883083 gas)
    ✓ [ERC20] Verifies that changing a bounty's issuer emits an event (6891699 gas)
    ✓ [ERC20] Verifies that I can change the approver of my bounty (6891392 gas)
    ✓ [ERC20] Verifies that I can't change the approver of an out of bounds bounty (6882142 gas)
    ✓ [ERC20] Verifies that I can't change the approver of a bounty if I didn't issue it (6883078 gas)
    ✓ [ERC20] Verifies that I can't the issuer with an out of bounds issuer ID (6882497 gas)
    ✓ [ERC20] Verifies that I can't the issuer changing an out of bounds approver ID (6883433 gas)
    ✓ [ERC20] Verifies that changing a bounty's approver emits an event (6891456 gas)
    ✓ [ERC20] Verifies that I can change the data of my bounty (6885614 gas)
    ✓ [ERC20] Verifies that I can't change the data of an out of bounds bounty (6881780 gas)
    ✓ [ERC20] Verifies that I can't change the data of a bounty if I didn't issue it (6882652 gas)
    ✓ [ERC20] Verifies that I can't change the data with an out of bounds issuer ID (6882135 gas)
    ✓ [ERC20] Verifies that changing a bounty's data emits an event (6885486 gas)
    ✓ [ERC20] Verifies that I can change the deadline of my bounty (6889062 gas)
    ✓ [ERC20] Verifies that I can't change the deadline of an out of bounds bounty (6881108 gas)
    ✓ [ERC20] Verifies that I can't change the deadline of a bounty if I didn't issue it (6881980 gas)
    ✓ [ERC20] Verifies that I can't change the deadline with an out of bounds issuer ID (6881463 gas)
    ✓ [ERC20] Verifies that changing a bounty's deadline emits an event (6889126 gas)
    ✓ [ERC20] Verifies that I can add issuers to my bounty (6940826 gas)
    ✓ [ERC20] Verifies that I can't add issuers to an out of bounds bounty (6884842 gas)
    ✓ [ERC20] Verifies that I can't add issuers to a bounty if I didn't issue it (6885778 gas)
    ✓ [ERC20] Verifies that I can't add issuers with an out of bounds issuer ID (6885197 gas)
    ✓ [ERC20] Verifies that adding issuers to a bounty emits an event (6940826 gas)
    ✓ [ERC20] Verifies that I can replace the issuers of my bounty (6920289 gas)
    ✓ [ERC20] Verifies that I can't replace issuers for an out of bounds bounty (6884688 gas)
    ✓ [ERC20] Verifies that I can't replace issuers for a bounty if I didn't issue it (6885560 gas)
    ✓ [ERC20] Verifies that I can't replace issuers with an out of bounds issuer ID (6884979 gas)
    ✓ [ERC20] Verifies that replacing issuers of a bounty emits an event (6920289 gas)
    ✓ [ERC20] Verifies that I can add approvers to my bounty (6940518 gas)
    ✓ [ERC20] Verifies that I can't add approvers to an out of bounds bounty (6884470 gas)
    ✓ [ERC20] Verifies that I can't add approvers to a bounty if I didn't issue it (6885470 gas)
    ✓ [ERC20] Verifies that I can't add approvers with an out of bounds issuer ID (6884889 gas)
    ✓ [ERC20] Verifies that adding approvers to a bounty emits an event (6940518 gas)
    ✓ [ERC20] Verifies that I can replace the approvers of my bounty (6905179 gas)
    ✓ [ERC20] Verifies that I can't replace approvers for an out of bounds bounty (6884578 gas)
    ✓ [ERC20] Verifies that I can't replace approvers for a bounty if I didn't issue it (6885514 gas)
    ✓ [ERC20] Verifies that I can't replace approvers with an out of bounds issuer ID (6884933 gas)
    ✓ [ERC20] Verifies that replacing approvers of a bounty emits an event (6905115 gas)

  Contract: StandardBounties
    ✓ [ERC721] Verifies that the StandardBounties registry works (5320382 gas)
    ✓ [ERC721] Verifies that I can issue a bounty paying in ERC721 tokens without locking up funds (7270882 gas)
    ✓ [ERC721] Verifies that I can issue a bounty paying in ERC721 tokens while locking up funds (7492684 gas)
    ✓ [ERC721] Verifies that I can't issue a bounty in tokens contributing both tokens and ETH (7470331 gas)
    ✓ [ERC721] Verifies that I can't issue a bounty contributing less than the deposit amount (7473510 gas)
    ✓ [ERC721] Verifies that I can contribute to a bounty in ERC721 tokens (7693303 gas)
    ✓ [ERC721] Verifies that I can't contribute to a bounty which is out of bounds (7407009 gas)
    ✓ [ERC721] Verifies that I can't contribute to a bounty and send less than the deposit amount (7497543 gas)
    ✓ [ERC721] Verifies that I can't contribute to a bounty and send both tokens and ETH (7494352 gas)
    ✓ [ERC721] Verifies that contributing emits an event (7516437 gas)
    ✓ [ERC721] Verifies that I can refund a contribution in ERC721 tokens (7620456 gas)
    ✓ [ERC721] Verifies that I can refund multiple contributions in ERC721 tokens (7907349 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution to a bounty which is out of bounds (7573293 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution which is out of bounds (7573684 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution which isn't mine (7774912 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution which has already been refunded (7646507 gas)
    ✓ [ERC721] Verifies that I can't refund a contribution before the deadline has elapsed (7542864 gas)
    ✓ [ERC721] Verifies that refunding a contribution emits an event (7620456 gas)
    ✓ [ERC721] Verifies that I can perform an action for a bounty (7299000 gas)
    ✓ [ERC721] Verifies that I can't perform an action for an out of bounds bounty (7296263 gas)
    ✓ [ERC721] Verifies that performing an action emits an event (7299000 gas)
    ✓ [ERC721] Verifies that I can fulfill a bounty (7407670 gas)
    ✓ [ERC721] Verifies that I can't fulfill an out of bounds bounty (7300182 gas)
    ✓ [ERC721] Verifies that I can't fulfill a bounty after the deadline has elapsed (7522040 gas)
    ✓ [ERC721] Verifies that I can't fulfill a bounty with 0 fulfillers (7518906 gas)
    ✓ [ERC721] Verifies that fulfilling a bounty emits an event (7407670 gas)
    ✓ [ERC721] Verifies that I can update a fulfillment (7459483 gas)
    ✓ [ERC721] Verifies that I can't update a fulfillment for an out of bounds bounty (7437435 gas)
    ✓ [ERC721] Verifies that I can't update an out of bounds fulfillment (7437762 gas)
    ✓ [ERC721] Verifies that I can't update a fulfillment which was submitted by someone else (7437333 gas)
    ✓ [ERC721] Verifies that updating a fulfillment emits an event (7459419 gas)
    ✓ [ERC721] Verifies that I can accept a fulfillment paying different 721 tokens to different fulfillers (7980810 gas)
    ✓ [ERC721] Verifies that I can accept a fulfillment as an approver (7980874 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment on an out of bounds bounty (7878306 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment which is out of bounds (7878633 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment if I'm not an approver (7879161 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (7899832 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (7879225 gas)
    ✓ [ERC721] Verifies that I can't accept a fulfillment paying out in tokens I dont have (7879097 gas)
    ✓ [ERC721] Verifies that accepting a fulfillment emits an event (7980874 gas)
    ✓ [ERC721] Verifies that I can fulfill and accept a bounty simultaneously (7957991 gas)
    ✓ [ERC721] Verifies that I can change all of a bounty's info (7564984 gas)
    ✓ [ERC721] Verifies that I can't change an out of bounds bounty (7525535 gas)
    ✓ [ERC721] Verifies that I can't change a bounty if I'm not an issuer' (7526407 gas)
    ✓ [ERC721] Verifies that I can change the issuer of my bounty (7528002 gas)
    ✓ [ERC721] Verifies that I can't change the issuer of an out of bounds bounty (7518687 gas)
    ✓ [ERC721] Verifies that I can't change the issuer of a bounty if I didn't issue it (7519967 gas)
    ✓ [ERC721] Verifies that I can't the issuer with an out of bounds issuer ID (7519042 gas)
    ✓ [ERC721] Verifies that I can't the issuer changing an out of bounds issuer ID (7519386 gas)
    ✓ [ERC721] Verifies that changing a bounty's issuer emits an event (7528002 gas)
    ✓ [ERC721] Verifies that I can change the approver of my bounty (7527759 gas)
    ✓ [ERC721] Verifies that I can't change the approver of an out of bounds bounty (7518381 gas)
    ✓ [ERC721] Verifies that I can't change the approver of a bounty if I didn't issue it (7519381 gas)
    ✓ [ERC721] Verifies that I can't the issuer with an out of bounds issuer ID (7518800 gas)
    ✓ [ERC721] Verifies that I can't the issuer changing an out of bounds approver ID (7519800 gas)
    ✓ [ERC721] Verifies that changing a bounty's approver emits an event (7527695 gas)
    ✓ [ERC721] Verifies that I can change the data of my bounty (7521917 gas)
    ✓ [ERC721] Verifies that I can't change the data of an out of bounds bounty (7518083 gas)
    ✓ [ERC721] Verifies that I can't change the data of a bounty if I didn't issue it (7519019 gas)
    ✓ [ERC721] Verifies that I can't change the data with an out of bounds issuer ID (7518438 gas)
    ✓ [ERC721] Verifies that changing a bounty's data emits an event (7521917 gas)
    ✓ [ERC721] Verifies that I can change the deadline of my bounty (7525429 gas)
    ✓ [ERC721] Verifies that I can't change the deadline of an out of bounds bounty (7517411 gas)
    ✓ [ERC721] Verifies that I can't change the deadline of a bounty if I didn't issue it (7518347 gas)
    ✓ [ERC721] Verifies that I can't change the deadline with an out of bounds issuer ID (7517766 gas)
    ✓ [ERC721] Verifies that changing a bounty's deadline emits an event (7525429 gas)
    ✓ [ERC721] Verifies that I can add issuers to my bounty (7577129 gas)
    ✓ [ERC721] Verifies that I can't add issuers to an out of bounds bounty (7521145 gas)
    ✓ [ERC721] Verifies that I can't add issuers to a bounty if I didn't issue it (7522081 gas)
    ✓ [ERC721] Verifies that I can't add issuers with an out of bounds issuer ID (7521500 gas)
    ✓ [ERC721] Verifies that adding issuers to a bounty emits an event (7577065 gas)
    ✓ [ERC721] Verifies that I can replace the issuers of my bounty (7556592 gas)
    ✓ [ERC721] Verifies that I can't replace issuers for an out of bounds bounty (7520991 gas)
    ✓ [ERC721] Verifies that I can't replace issuers for a bounty if I didn't issue it (7521863 gas)
    ✓ [ERC721] Verifies that I can't replace issuers with an out of bounds issuer ID (7521346 gas)
    ✓ [ERC721] Verifies that replacing issuers of a bounty emits an event (7556592 gas)
    ✓ [ERC721] Verifies that I can add approvers to my bounty (7576821 gas)
    ✓ [ERC721] Verifies that I can't add approvers to an out of bounds bounty (7520837 gas)
    ✓ [ERC721] Verifies that I can't add approvers to a bounty if I didn't issue it (7521773 gas)
    ✓ [ERC721] Verifies that I can't add approvers with an out of bounds issuer ID (7521192 gas)
    ✓ [ERC721] Verifies that adding approvers to a bounty emits an event (7576821 gas)
    ✓ [ERC721] Verifies that I can replace the approvers of my bounty (7541482 gas)
    ✓ [ERC721] Verifies that I can't replace approvers for an out of bounds bounty (7520881 gas)
    ✓ [ERC721] Verifies that I can't replace approvers for a bounty if I didn't issue it (7521817 gas)
    ✓ [ERC721] Verifies that I can't replace approvers with an out of bounds issuer ID (7521172 gas)
    ✓ [ERC721] Verifies that replacing approvers of a bounty emits an event (7541418 gas)

  Contract: StandardBounties
    ✓ [ETH] Verifies that the StandardBounties registry works (5320382 gas)
    ✓ [ETH] Verifies that I can issue a bounty paying in ETH without locking up funds (5513008 gas)
    ✓ [ETH] Verifies that I can issue a bounty paying in ETH while locking up funds (5602794 gas)
    ✓ [ETH] Verifies that I can't issue a bounty contributing more than the deposit amount (5599949 gas)
    ✓ [ETH] Verifies that I can't issue a bounty contributing less than the deposit amount (5599949 gas)
    ✓ [ETH] Verifies that I can contribute to a bounty in ETH (5686394 gas)
    ✓ [ETH] Verifies that I can't contribute to a bounty which is out of bounds (5537247 gas)
    ✓ [ETH] Verifies that I can't contribute to a bounty and send less than the deposit amount (5623970 gas)
    ✓ [ETH] Verifies that contributing emits an event (5626608 gas)
    ✓ [ETH] Verifies that I can refund a contribution in ETH (5706798 gas)
    ✓ [ETH] Verifies that I can't refund a contribution to a bounty which is out of bounds (5683464 gas)
    ✓ [ETH] Verifies that I can't refund a contribution which is out of bounds (5683791 gas)
    ✓ [ETH] Verifies that I can't refund a contribution which isn't mine (5768000 gas)
    ✓ [ETH] Verifies that I can't refund a contribution which has already been refunded (5732849 gas)
    ✓ [ETH] Verifies that I can't refund a contribution before the deadline has elapsed (5652971 gas)
    ✓ [ETH] Verifies that refunding a contribution emits an event (5706798 gas)
    ✓ [ETH] Verifies that I can perform an action for a bounty (5541126 gas)
    ✓ [ETH] Verifies that I can't perform an action for an out of bounds bounty (5538389 gas)
    ✓ [ETH] Verifies that performing an action emits an event (5541126 gas)
    ✓ [ETH] Verifies that I can fulfill a bounty (5649796 gas)
    ✓ [ETH] Verifies that I can't fulfill an out of bounds bounty (5542308 gas)
    ✓ [ETH] Verifies that I can't fulfill a bounty after the deadline has elapsed (5632150 gas)
    ✓ [ETH] Verifies that I can't fulfill a bounty with 0 fulfillers (5539230 gas)
    ✓ [ETH] Verifies that fulfilling a bounty emits an event (5649796 gas)
    ✓ [ETH] Verifies that I can update a fulfillment (5701609 gas)
    ✓ [ETH] Verifies that I can't update a fulfillment for an out of bounds bounty (5679561 gas)
    ✓ [ETH] Verifies that I can't update an out of bounds fulfillment (5679888 gas)
    ✓ [ETH] Verifies that I can't update a fulfillment which was submitted by someone else (5679523 gas)
    ✓ [ETH] Verifies that updating a fulfillment emits an event (5701609 gas)
    ✓ [ETH] Verifies that I can accept a fulfillment as an issuer (5827783 gas)
    ✓ [ETH] Verifies that I can accept a fulfillment paying different amounts to different fulfillers (5827783 gas)
    ✓ [ETH] Verifies that I can accept a fulfillment as an approver (5827847 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment on an out of bounds bounty (5787797 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment which is out of bounds (5788124 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment if I'm not an approver (5788716 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment by passing in the wrong number of token amounts corresponding to the number of fulfillers (5809323 gas)
    ✓ [ETH] Verifies that I can't accept a fulfillment paying out more than the balance of my bounty (5788716 gas)
    ✓ [ETH] Verifies that accepting a fulfillment emits an event (5805286 gas)
    ✓ [ETH] Verifies that I can fulfill and accept a bounty simultaneously (5804964 gas)
    ✓ [ETH] Verifies that I can change all of a bounty's info (5675094 gas)
    ✓ [ETH] Verifies that I can't change an out of bounds bounty (5635645 gas)
    ✓ [ETH] Verifies that I can't change a bounty if I'm not an issuer' (5636581 gas)
    ✓ [ETH] Verifies that I can change the issuer of my bounty (5638112 gas)
    ✓ [ETH] Verifies that I can't change the issuer of an out of bounds bounty (5628797 gas)
    ✓ [ETH] Verifies that I can't change the issuer of a bounty if I didn't issue it (5630077 gas)
    ✓ [ETH] Verifies that I can't the issuer with an out of bounds issuer ID (5629152 gas)
    ✓ [ETH] Verifies that I can't the issuer changing an out of bounds issuer ID (5629496 gas)
    ✓ [ETH] Verifies that changing a bounty's issuer emits an event (5638112 gas)
    ✓ [ETH] Verifies that I can change the approver of my bounty (5637869 gas)
    ✓ [ETH] Verifies that I can't change the approver of an out of bounds bounty (5628555 gas)
    ✓ [ETH] Verifies that I can't change the approver of a bounty if I didn't issue it (5629491 gas)
    ✓ [ETH] Verifies that I can't the issuer with an out of bounds issuer ID (5628910 gas)
    ✓ [ETH] Verifies that I can't the issuer changing an out of bounds approver ID (5629910 gas)
    ✓ [ETH] Verifies that changing a bounty's approver emits an event (5637869 gas)
    ✓ [ETH] Verifies that I can change the data of my bounty (5632027 gas)
    ✓ [ETH] Verifies that I can't change the data of an out of bounds bounty (5628193 gas)
    ✓ [ETH] Verifies that I can't change the data of a bounty if I didn't issue it (5629129 gas)
    ✓ [ETH] Verifies that I can't change the data with an out of bounds issuer ID (5628548 gas)
    ✓ [ETH] Verifies that changing a bounty's data emits an event (5632027 gas)
    ✓ [ETH] Verifies that I can change the deadline of my bounty (5635539 gas)
    ✓ [ETH] Verifies that I can't change the deadline of an out of bounds bounty (5627521 gas)
    ✓ [ETH] Verifies that I can't change the deadline of a bounty if I didn't issue it (5628457 gas)
    ✓ [ETH] Verifies that I can't change the deadline with an out of bounds issuer ID (5627876 gas)
    ✓ [ETH] Verifies that changing a bounty's deadline emits an event (5635539 gas)
    ✓ [ETH] Verifies that I can add issuers to my bounty (5687239 gas)
    ✓ [ETH] Verifies that I can't add issuers to an out of bounds bounty (5631255 gas)
    ✓ [ETH] Verifies that I can't add issuers to a bounty if I didn't issue it (5632191 gas)
    ✓ [ETH] Verifies that I can't add issuers with an out of bounds issuer ID (5631610 gas)
    ✓ [ETH] Verifies that adding issuers to a bounty emits an event (5687239 gas)
    ✓ [ETH] Verifies that I can replace the issuers of my bounty (5666702 gas)
    ✓ [ETH] Verifies that I can't replace issuers for an out of bounds bounty (5631101 gas)
    ✓ [ETH] Verifies that I can't replace issuers for a bounty if I didn't issue it (5632037 gas)
    ✓ [ETH] Verifies that I can't replace issuers with an out of bounds issuer ID (5631456 gas)
    ✓ [ETH] Verifies that replacing issuers of a bounty emits an event (5666702 gas)
    ✓ [ETH] Verifies that I can add approvers to my bounty (5686931 gas)
    ✓ [ETH] Verifies that I can't add approvers to an out of bounds bounty (5630947 gas)
    ✓ [ETH] Verifies that I can't add approvers to a bounty if I didn't issue it (5631883 gas)
    ✓ [ETH] Verifies that I can't add approvers with an out of bounds issuer ID (5631302 gas)
    ✓ [ETH] Verifies that adding approvers to a bounty emits an event (5686931 gas)
    ✓ [ETH] Verifies that I can replace the approvers of my bounty (5651592 gas)
    ✓ [ETH] Verifies that I can't replace approvers for an out of bounds bounty (5630991 gas)
    ✓ [ETH] Verifies that I can't replace approvers for a bounty if I didn't issue it (5631927 gas)
    ✓ [ETH] Verifies that I can't replace approvers with an out of bounds issuer ID (5631346 gas)
    ✓ [ETH] Verifies that replacing approvers of a bounty emits an event (5651592 gas)

·---------------------------------------------------------------------------------|----------------------------·
|                                       Gas                                       ·  Block limit: 6721975 gas  │
················································|·································|·····························
|  Methods                                      ·           6 gwei/gas            ·       140.48 usd/eth       │
·························|······················|··········|··········|···········|··············|··············
|  Contract              ·  Method              ·  Min     ·  Max     ·  Avg      ·  # calls     ·  usd (avg)  │
·························|······················|··········|··········|···········|··············|··············
|  ERC721BasicTokenMock  ·  approve             ·   45626  ·   45690  ·    45684  ·          86  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  ERC721BasicTokenMock  ·  mint                ·   51198  ·   66198  ·    64454  ·          86  ·       0.05  │
·························|······················|··········|··········|···········|··············|··············
|  HumanStandardToken    ·  approve             ·   45001  ·   45129  ·    45118  ·          73  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  HumanStandardToken    ·  transfer            ·       -  ·       -  ·    51095  ·           1  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  acceptFulfillment   ·   65704  ·  128286  ·    94397  ·          11  ·       0.08  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  addApprovers        ·       -  ·       -  ·    84137  ·           6  ·       0.07  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  addIssuers          ·       -  ·       -  ·    84445  ·           6  ·       0.07  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeApprover      ·       -  ·       -  ·    35075  ·           6  ·       0.03  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeBounty        ·       -  ·       -  ·    72300  ·           3  ·       0.06  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeData          ·       -  ·       -  ·    29233  ·           6  ·       0.02  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeDeadline      ·       -  ·       -  ·    32745  ·          25  ·       0.03  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  changeIssuer        ·       -  ·       -  ·    35318  ·           6  ·       0.03  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  contribute          ·   83600  ·  150482  ·   115426  ·          42  ·       0.10  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  fulfillAndAccept    ·  179673  ·  242191  ·   211162  ·           3  ·       0.18  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  fulfillBounty       ·       -  ·       -  ·   136788  ·          48  ·       0.12  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  issueBounty         ·  192626  ·  373143  ·   294241  ·         246  ·       0.25  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  performAction       ·       -  ·       -  ·    28118  ·           6  ·       0.02  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  refundContribution  ·   40922  ·  101210  ·    57838  ·          11  ·       0.05  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  replaceApprovers    ·       -  ·       -  ·    48798  ·           6  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  replaceIssuers      ·       -  ·       -  ·    63908  ·           6  ·       0.05  │
·························|······················|··········|··········|···········|··············|··············
|  StandardBounties      ·  updateFulfillment   ·       -  ·       -  ·    51813  ·           6  ·       0.04  │
·························|······················|··········|··········|···········|··············|··············
|  Deployments                                  ·                                 ·  % of limit  ·             │
················································|··········|··········|···········|··············|··············
|  ERC721BasicTokenMock                         ·       -  ·       -  ·  1726444  ·      25.7 %  ·       1.46  │
················································|··········|··········|···········|··············|··············
|  HumanStandardToken                           ·       -  ·       -  ·  1140224  ·        17 %  ·       0.96  │
················································|··········|··········|···········|··············|··············
|  StandardBounties                             ·       -  ·       -  ·  5320382  ·      79.1 %  ·       4.48  │
·-----------------------------------------------|----------|----------|-----------|--------------|-------------·

  255 passing (4m)


```