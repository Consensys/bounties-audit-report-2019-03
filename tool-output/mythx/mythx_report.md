```sh-session
$ mythos analyze contracts/BountiesMetaTxRelayer_flat.sol BountiesMetaTxRelayer
Reading contract contracts/BountiesMetaTxRelayer_flat.sol... done
Downloading Solidity version v0.5.0+commit.1d4f565a
(node:12424) V8: soljson-v0.5.0+commit.1d4f565a.js:3 Invalid asm.js: Invalid member of stdlib
Compiling contract contracts/BountiesMetaTxRelayer_flat.sol... done
Analyzing contract BountiesMetaTxRelayer... done
Report found 1 issues
Title: State Variable Default Visibility
Severity: Medium
Head: The state variable visibility is not set.
Description: It is best practice to set the visibility of state variables explicitly. The default visibility for "balances" is internal. Other possible visibility values are public and private.
Source code:

contracts/BountiesMetaTxRelayer_flat.sol 107:33
--------------------------------------------------
balances
--------------------------------------------------

==================================================

Title: State Variable Default Visibility
Severity: Medium
Head: The state variable visibility is not set.
Description: It is best practice to set the visibility of state variables explicitly. The default visibility for "allowed" is internal. Other possible visibility values are public and private.
Source code:

contracts/BountiesMetaTxRelayer_flat.sol 108:54
--------------------------------------------------
allowed
--------------------------------------------------

==================================================

Title: State Variable Default Visibility
Severity: Medium
Head: The state variable visibility is not set.
Description: It is best practice to set the visibility of state variables explicitly. The default visibility for "owner" is internal. Other possible visibility values are public and private.
Source code:

contracts/BountiesMetaTxRelayer_flat.sol 736:10
--------------------------------------------------
owner
--------------------------------------------------

==================================================

Title: State Variable Default Visibility
Severity: Medium
Head: The state variable visibility is not set.
Description: It is best practice to set the visibility of state variables explicitly. The default visibility for "metaTxRelayer" is internal. Other possible visibility values are public and private.
Source code:

contracts/BountiesMetaTxRelayer_flat.sol 737:10
--------------------------------------------------
metaTxRelayer
--------------------------------------------------

==================================================

Title: State Variable Default Visibility
Severity: Medium
Head: The state variable visibility is not set.
Description: It is best practice to set the visibility of state variables explicitly. The default visibility for "bountiesContract" is internal. Other possible visibility values are public and private.
Source code:

contracts/BountiesMetaTxRelayer_flat.sol 1419:19
--------------------------------------------------
bountiesContract
--------------------------------------------------

==================================================

Title: Shadowing State Variables
Severity: Medium
Head: State variable shadows another state variable.
Description: The state variable "ERC721_RECEIVED" in contract "ERC721Receiver" shadows another state variable with the same name "ERC721_RECEIVED" in contract "ERC721BasicToken".
Source code:

contracts/BountiesMetaTxRelayer_flat.sol 269:2
--------------------------------------------------
bytes4 internal constant ERC721_RECEIVED = 0xf0b9e5ba
--------------------------------------------------

==================================================

Title: Shadowing State Variables
Severity: Medium
Head: Local variable shadows a state variable.
Description: The local variable "owner" in contract "ERC721BasicToken" shadows the state variable with the same name "owner" in contract "StandardBounties".
Source code:

contracts/BountiesMetaTxRelayer_flat.sol 427:4
--------------------------------------------------
address owner
--------------------------------------------------
contracts/BountiesMetaTxRelayer_flat.sol 438:4
--------------------------------------------------
address owner
--------------------------------------------------
contracts/BountiesMetaTxRelayer_flat.sol 451:4
--------------------------------------------------
address owner
--------------------------------------------------
contracts/BountiesMetaTxRelayer_flat.sol 590:4
--------------------------------------------------
address owner
--------------------------------------------------

==================================================

Done
```