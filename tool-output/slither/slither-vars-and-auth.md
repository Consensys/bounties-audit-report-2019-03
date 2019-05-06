```
INFO:Printers:
Contract Token
+--------------+-------------------------+--------------------------+
|   Function   | State variables written | Conditions on msg.sender |
+--------------+-------------------------+--------------------------+
|  balanceOf   |            []           |            []            |
|   transfer   |            []           |            []            |
| transferFrom |            []           |            []            |
|   approve    |            []           |            []            |
|  allowance   |            []           |            []            |
+--------------+-------------------------+--------------------------+
INFO:Printers:
Contract ERC20Token
+--------------+-------------------------+-------------------------------------------------------------------------------------+
|   Function   | State variables written |                               Conditions on msg.sender                              |
+--------------+-------------------------+-------------------------------------------------------------------------------------+
|  balanceOf   |            []           |                                          []                                         |
|   transfer   |       ['balances']      |                   ['balances[msg.sender] >= _value && _value > 0']                  |
| transferFrom | ['balances', 'allowed'] | ['balances[_from] >= _value && allowed[_from][msg.sender] >= _value && _value > 0'] |
|   approve    |       ['allowed']       |                                          []                                         |
|  allowance   |            []           |                                          []                                         |
+--------------+-------------------------+-------------------------------------------------------------------------------------+
INFO:Printers:
Contract SafeMath
+----------+-------------------------+--------------------------+
| Function | State variables written | Conditions on msg.sender |
+----------+-------------------------+--------------------------+
|   mul    |            []           |            []            |
|   div    |            []           |            []            |
|   sub    |            []           |            []            |
|   add    |            []           |            []            |
+----------+-------------------------+--------------------------+
INFO:Printers:
Contract AddressUtils
+------------+-------------------------+--------------------------+
|  Function  | State variables written | Conditions on msg.sender |
+------------+-------------------------+--------------------------+
| isContract |            []           |            []            |
+------------+-------------------------+--------------------------+
INFO:Printers:
Contract ERC165
+-------------------+-------------------------+--------------------------+
|      Function     | State variables written | Conditions on msg.sender |
+-------------------+-------------------------+--------------------------+
| supportsInterface |            []           |            []            |
+-------------------+-------------------------+--------------------------+
INFO:Printers:
Contract SupportsInterfaceWithLookup
+--------------------+-------------------------+--------------------------+
|      Function      | State variables written | Conditions on msg.sender |
+--------------------+-------------------------+--------------------------+
| supportsInterface  |            []           |            []            |
|    constructor     | ['supportedInterfaces'] |            []            |
| _registerInterface | ['supportedInterfaces'] |            []            |
+--------------------+-------------------------+--------------------------+
INFO:Printers:
Contract ERC721Receiver
+------------------+-------------------------+--------------------------+
|     Function     | State variables written | Conditions on msg.sender |
+------------------+-------------------------+--------------------------+
| onERC721Received |            []           |            []            |
+------------------+-------------------------+--------------------------+
INFO:Printers:
Contract ERC721Basic
+-------------------+-------------------------+--------------------------+
|      Function     | State variables written | Conditions on msg.sender |
+-------------------+-------------------------+--------------------------+
| supportsInterface |            []           |            []            |
|     balanceOf     |            []           |            []            |
|      ownerOf      |            []           |            []            |
|       exists      |            []           |            []            |
|      approve      |            []           |            []            |
|    getApproved    |            []           |            []            |
| setApprovalForAll |            []           |            []            |
|  isApprovedForAll |            []           |            []            |
|    transferFrom   |            []           |            []            |
|  safeTransferFrom |            []           |            []            |
|  safeTransferFrom |            []           |            []            |
+-------------------+-------------------------+--------------------------+
INFO:Printers:
Contract ERC721BasicToken
+--------------------------+------------------------------------------------------+------------------------------------------------------------------------------+
|         Function         |               State variables written                |                           Conditions on msg.sender                           |
+--------------------------+------------------------------------------------------+------------------------------------------------------------------------------+
|    supportsInterface     |                          []                          |                                      []                                      |
|    _registerInterface    |               ['supportedInterfaces']                |                                      []                                      |
|        balanceOf         |                          []                          |                                      []                                      |
|         ownerOf          |                          []                          |                                      []                                      |
|          exists          |                          []                          |                                      []                                      |
|         approve          |                  ['tokenApprovals']                  | ['require(bool)(msg.sender == owner || isApprovedForAll(owner,msg.sender))'] |
|       getApproved        |                          []                          |                                      []                                      |
|    setApprovalForAll     |                ['operatorApprovals']                 |                     ['require(bool)(_to != msg.sender)']                     |
|     isApprovedForAll     |                          []                          |                                      []                                      |
|       transferFrom       | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |          ['require(bool)(isApprovedOrOwner(msg.sender,_tokenId))']           |
|     safeTransferFrom     | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |          ['require(bool)(isApprovedOrOwner(msg.sender,_tokenId))']           |
|     safeTransferFrom     | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |          ['require(bool)(isApprovedOrOwner(msg.sender,_tokenId))']           |
|       constructor        |               ['supportedInterfaces']                |                                      []                                      |
|    isApprovedOrOwner     |                          []                          |                                      []                                      |
|          _mint           |          ['ownedTokensCount', 'tokenOwner']          |                                      []                                      |
|          _burn           | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |                                      []                                      |
|      clearApproval       |                  ['tokenApprovals']                  |                                      []                                      |
|        addTokenTo        |          ['ownedTokensCount', 'tokenOwner']          |                                      []                                      |
|     removeTokenFrom      |          ['ownedTokensCount', 'tokenOwner']          |                                      []                                      |
| checkAndCallSafeTransfer |                          []                          |                                      []                                      |
+--------------------------+------------------------------------------------------+------------------------------------------------------------------------------+
INFO:Printers:
Contract ERC721BasicTokenMock
+--------------------------+------------------------------------------------------+------------------------------------------------------------------------------+
|         Function         |               State variables written                |                           Conditions on msg.sender                           |
+--------------------------+------------------------------------------------------+------------------------------------------------------------------------------+
|    supportsInterface     |                          []                          |                                      []                                      |
|       constructor        |               ['supportedInterfaces']                |                                      []                                      |
|    _registerInterface    |               ['supportedInterfaces']                |                                      []                                      |
|        balanceOf         |                          []                          |                                      []                                      |
|         ownerOf          |                          []                          |                                      []                                      |
|          exists          |                          []                          |                                      []                                      |
|         approve          |                  ['tokenApprovals']                  | ['require(bool)(msg.sender == owner || isApprovedForAll(owner,msg.sender))'] |
|       getApproved        |                          []                          |                                      []                                      |
|    setApprovalForAll     |                ['operatorApprovals']                 |                     ['require(bool)(_to != msg.sender)']                     |
|     isApprovedForAll     |                          []                          |                                      []                                      |
|       transferFrom       | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |          ['require(bool)(isApprovedOrOwner(msg.sender,_tokenId))']           |
|     safeTransferFrom     | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |          ['require(bool)(isApprovedOrOwner(msg.sender,_tokenId))']           |
|     safeTransferFrom     | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |          ['require(bool)(isApprovedOrOwner(msg.sender,_tokenId))']           |
|    isApprovedOrOwner     |                          []                          |                                      []                                      |
|          _mint           |          ['ownedTokensCount', 'tokenOwner']          |                                      []                                      |
|          _burn           | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |                                      []                                      |
|      clearApproval       |                  ['tokenApprovals']                  |                                      []                                      |
|        addTokenTo        |          ['ownedTokensCount', 'tokenOwner']          |                                      []                                      |
|     removeTokenFrom      |          ['ownedTokensCount', 'tokenOwner']          |                                      []                                      |
| checkAndCallSafeTransfer |                          []                          |                                      []                                      |
|           mint           |          ['ownedTokensCount', 'tokenOwner']          |                                      []                                      |
|           burn           | ['ownedTokensCount', 'tokenOwner', 'tokenApprovals'] |                                      []                                      |
+--------------------------+------------------------------------------------------+------------------------------------------------------------------------------+
INFO:Printers:
Contract StandardBounties
+---------------------+-----------------------------+-------------------------------------------------------------------------+
|       Function      |   State variables written   |                         Conditions on msg.sender                        |
+---------------------+-----------------------------+-------------------------------------------------------------------------+
|     constructor     |          ['owner']          |                                    []                                   |
|   setMetaTxRelayer  |      ['metaTxRelayer']      |                  ['require(bool)(msg.sender == owner)']                 |
|     issueBounty     | ['numBounties', 'bounties'] | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|      contribute     |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|  refundContribution |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
| refundContributions |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|    performAction    |              []             | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|    fulfillBounty    |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|  updateFulfillment  |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|  acceptFulfillment  |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|   fulfillAndAccept  |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|     changeBounty    |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|     changeIssuer    |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|    changeApprover   |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|      changeData     |              []             | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|    changeDeadline   |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|      addIssuers     |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|    replaceIssuers   |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|     addApprovers    |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|   replaceApprovers  |         ['bounties']        | ['require(bool)(msg.sender == _sender || msg.sender == metaTxRelayer)'] |
|      getBounty      |              []             |                                    []                                   |
|    transferTokens   |              []             |                                    []                                   |
+---------------------+-----------------------------+-------------------------------------------------------------------------+
INFO:Printers:
Contract BountiesMetaTxRelayer
+-------------------------+-------------------------+--------------------------+
|         Function        | State variables written | Conditions on msg.sender |
+-------------------------+-------------------------+--------------------------+
|       constructor       |   ['bountiesContract']  |            []            |
|     metaIssueBounty     |     ['replayNonce']     |            []            |
|      metaContribute     |     ['replayNonce']     |            []            |
|  metaRefundContribution |     ['replayNonce']     |            []            |
| metaRefundContributions |     ['replayNonce']     |            []            |
|    metaPerformAction    |     ['replayNonce']     |            []            |
|    metaFulfillBounty    |     ['replayNonce']     |            []            |
|  metaUpdateFulfillment  |     ['replayNonce']     |            []            |
|  metaAcceptFulfillment  |     ['replayNonce']     |            []            |
|   metaFulfillAndAccept  |     ['replayNonce']     |            []            |
|     metaChangeBounty    |     ['replayNonce']     |            []            |
|     metaChangeIssuer    |     ['replayNonce']     |            []            |
|    metaChangeApprover   |     ['replayNonce']     |            []            |
|      metaChangeData     |     ['replayNonce']     |            []            |
|    metaChangeDeadline   |     ['replayNonce']     |            []            |
|      metaAddIssuers     |     ['replayNonce']     |            []            |
|    metaReplaceIssuers   |     ['replayNonce']     |            []            |
|     metaAddApprovers    |     ['replayNonce']     |            []            |
|   metaReplaceApprovers  |     ['replayNonce']     |            []            |
|        getSigner        |            []           |            []            |
+-------------------------+-------------------------+--------------------------+
INFO:Slither:BountiesMetaTxRelayer_flat.sol analyzed (12 contracts)
```
