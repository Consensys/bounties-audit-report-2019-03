## Sūrya's Description Report

### Files Description Table


|  File Name  |  SHA-1 Hash  |
|-------------|--------------|
| StandardBounties.sol | 72e3143a8b669a247b8af84297e926671542f0b0 |
| BountiesMetaTxRelayer.sol | c6c4e0f60f43ebcf30fe8adf9578b7bb12b33737 |


### Contracts Description Table


|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     └      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
||||||
| **StandardBounties** | Implementation |  |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | setMetaTxRelayer | Public ❗️ | 🛑  |NO❗️ |
| └ | issueBounty | Public ❗️ |  💵 | senderIsValid |
| └ | contribute | Public ❗️ |  💵 | senderIsValid validateBountyArrayIndex |
| └ | refundContribution | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateContributionArrayIndex onlyContributor hasNotPaid hasNotRefunded |
| └ | refundContributions | Public ❗️ | 🛑  | senderIsValid |
| └ | performAction | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex |
| └ | fulfillBounty | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex |
| └ | updateFulfillment | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateFulfillmentArrayIndex onlySubmitter |
| └ | acceptFulfillment | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateFulfillmentArrayIndex isApprover |
| └ | fulfillAndAccept | Public ❗️ | 🛑  | senderIsValid |
| └ | changeBounty | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | changeIssuer | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | changeApprover | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer validateApproverArrayIndex |
| └ | changeData | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | changeDeadline | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | addIssuers | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | replaceIssuers | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | addApprovers | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | replaceApprovers | Public ❗️ | 🛑  | senderIsValid validateBountyArrayIndex validateIssuerArrayIndex onlyIssuer |
| └ | getBounty | Public ❗️ |   |NO❗️ |
| └ | transferTokens | Internal 🔒 | 🛑  | |
||||||
| **BountiesMetaTxRelayer** | Implementation |  |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | metaIssueBounty | Public ❗️ |  💵 |NO❗️ |
| └ | metaContribute | Public ❗️ |  💵 |NO❗️ |
| └ | metaRefundContribution | Public ❗️ | 🛑  |NO❗️ |
| └ | metaRefundContributions | Public ❗️ | 🛑  |NO❗️ |
| └ | metaPerformAction | Public ❗️ | 🛑  |NO❗️ |
| └ | metaFulfillBounty | Public ❗️ | 🛑  |NO❗️ |
| └ | metaUpdateFulfillment | Public ❗️ | 🛑  |NO❗️ |
| └ | metaAcceptFulfillment | Public ❗️ | 🛑  |NO❗️ |
| └ | metaFulfillAndAccept | Public ❗️ | 🛑  |NO❗️ |
| └ | metaChangeBounty | Public ❗️ | 🛑  |NO❗️ |
| └ | metaChangeIssuer | Public ❗️ | 🛑  |NO❗️ |
| └ | metaChangeApprover | Public ❗️ | 🛑  |NO❗️ |
| └ | metaChangeData | Public ❗️ | 🛑  |NO❗️ |
| └ | metaChangeDeadline | Public ❗️ | 🛑  |NO❗️ |
| └ | metaAddIssuers | Public ❗️ | 🛑  |NO❗️ |
| └ | metaReplaceIssuers | Public ❗️ | 🛑  |NO❗️ |
| └ | metaAddApprovers | Public ❗️ | 🛑  |NO❗️ |
| └ | metaReplaceApprovers | Public ❗️ | 🛑  |NO❗️ |
| └ | getSigner | Internal 🔒 |   | |


### Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    🛑    | Function can modify state |
|    💵    | Function is payable |
