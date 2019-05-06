```
INFO:Detectors:
AddressUtils.isContract (BountiesMetaTxRelayer_flat.sol#175-186) is declared view but contains assembly code
BountiesMetaTxRelayer.getSigner (BountiesMetaTxRelayer_flat.sol#1951-1980) is declared view but contains assembly code
Reference: https://github.com/trailofbits/slither/wiki/Detectors-Documentation#constant-functions-changing-the-state
INFO:Detectors:
ERC721Basic (BountiesMetaTxRelayer_flat.sol#296-336) has incorrect ERC20 function interface(s):
	-approve (BountiesMetaTxRelayer_flat.sol#317)
ERC721BasicToken (BountiesMetaTxRelayer_flat.sol#342-684) has incorrect ERC20 function interface(s):
	-approve (BountiesMetaTxRelayer_flat.sol#450-457)
Reference: https://github.com/trailofbits/slither/wiki/Detectors-Documentation#incorrect-erc20-interface
INFO:Detectors:
Contract locking ether found in BountiesMetaTxRelayer_flat.sol:
	Contract BountiesMetaTxRelayer has payable functions:
	 - metaIssueBounty (BountiesMetaTxRelayer_flat.sol#1427-1470)
	 - metaContribute (BountiesMetaTxRelayer_flat.sol#1470-1495)
	But does not have a function to withdraw the ether
Reference: https://github.com/trailofbits/slither/wiki/Detectors-Documentation#contracts-that-lock-ether
INFO:Detectors:
StandardBounties.contribute (BountiesMetaTxRelayer_flat.sol#924-960) does not use the value returned by external calls:
	-ERC721BasicToken(bounties[_bountyId].token).transferFrom(_sender,address(this),_amount) (BountiesMetaTxRelayer_flat.sol#949-952)
Reference: https://github.com/trailofbits/slither/wiki/Detectors-Documentation#unused-return
INFO:Slither:BountiesMetaTxRelayer_flat.sol analyzed (12 contracts), 6 result(s) found
```
