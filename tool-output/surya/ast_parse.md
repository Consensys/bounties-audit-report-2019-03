# Abstract Syntax Tree parse

```console
$ surya parse StandardBounties.sol
├─ type: SourceUnit
└─ children
   ├─ 0
   │  ├─ type: PragmaDirective
   │  ├─ name: solidity
   │  └─ value: ^0.5.0
   ├─ 1
   │  ├─ type: PragmaDirective
   │  ├─ name: experimental
   │  └─ value: ABIEncoderV2
   ├─ 2
   │  ├─ type: ImportDirective
   │  ├─ path: ./inherited/ERC20Token.sol
   │  ├─ unitAlias
   │  └─ symbolAliases
   ├─ 3
   │  ├─ type: ImportDirective
   │  ├─ path: ./inherited/ERC721Basic.sol
   │  ├─ unitAlias
   │  └─ symbolAliases
   └─ 4
      ├─ type: ContractDefinition
      ├─ name: StandardBounties
      ├─ baseContracts
      ├─ subNodes
      │  ├─ 0
      │  │  ├─ type: StructDefinition
      │  │  ├─ name: Bounty
      │  │  └─ members
      │  │     ├─ 0
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ArrayTypeName
      │  │     │  │  ├─ baseTypeName
      │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │     │  │  │  ├─ name: address
      │  │     │  │  │  └─ stateMutability: payable
      │  │     │  │  └─ length
      │  │     │  ├─ name: issuers
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 1
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ArrayTypeName
      │  │     │  │  ├─ baseTypeName
      │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │     │  │  │  └─ name: address
      │  │     │  │  └─ length
      │  │     │  ├─ name: approvers
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 2
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ElementaryTypeName
      │  │     │  │  └─ name: uint
      │  │     │  ├─ name: deadline
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 3
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ElementaryTypeName
      │  │     │  │  └─ name: address
      │  │     │  ├─ name: token
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 4
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ElementaryTypeName
      │  │     │  │  └─ name: uint
      │  │     │  ├─ name: tokenVersion
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 5
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ElementaryTypeName
      │  │     │  │  └─ name: uint
      │  │     │  ├─ name: balance
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 6
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ElementaryTypeName
      │  │     │  │  └─ name: bool
      │  │     │  ├─ name: hasPaidOut
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 7
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ArrayTypeName
      │  │     │  │  ├─ baseTypeName
      │  │     │  │  │  ├─ type: UserDefinedTypeName
      │  │     │  │  │  └─ namePath: Fulfillment
      │  │     │  │  └─ length
      │  │     │  ├─ name: fulfillments
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     └─ 8
      │  │        ├─ type: VariableDeclaration
      │  │        ├─ typeName
      │  │        │  ├─ type: ArrayTypeName
      │  │        │  ├─ baseTypeName
      │  │        │  │  ├─ type: UserDefinedTypeName
      │  │        │  │  └─ namePath: Contribution
      │  │        │  └─ length
      │  │        ├─ name: contributions
      │  │        ├─ storageLocation
      │  │        ├─ isStateVar: false
      │  │        └─ isIndexed: false
      │  ├─ 1
      │  │  ├─ type: StructDefinition
      │  │  ├─ name: Fulfillment
      │  │  └─ members
      │  │     ├─ 0
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ArrayTypeName
      │  │     │  │  ├─ baseTypeName
      │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │     │  │  │  ├─ name: address
      │  │     │  │  │  └─ stateMutability: payable
      │  │     │  │  └─ length
      │  │     │  ├─ name: fulfillers
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     └─ 1
      │  │        ├─ type: VariableDeclaration
      │  │        ├─ typeName
      │  │        │  ├─ type: ElementaryTypeName
      │  │        │  └─ name: address
      │  │        ├─ name: submitter
      │  │        ├─ storageLocation
      │  │        ├─ isStateVar: false
      │  │        └─ isIndexed: false
      │  ├─ 2
      │  │  ├─ type: StructDefinition
      │  │  ├─ name: Contribution
      │  │  └─ members
      │  │     ├─ 0
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ElementaryTypeName
      │  │     │  │  ├─ name: address
      │  │     │  │  └─ stateMutability: payable
      │  │     │  ├─ name: contributor
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     ├─ 1
      │  │     │  ├─ type: VariableDeclaration
      │  │     │  ├─ typeName
      │  │     │  │  ├─ type: ElementaryTypeName
      │  │     │  │  └─ name: uint
      │  │     │  ├─ name: amount
      │  │     │  ├─ storageLocation
      │  │     │  ├─ isStateVar: false
      │  │     │  └─ isIndexed: false
      │  │     └─ 2
      │  │        ├─ type: VariableDeclaration
      │  │        ├─ typeName
      │  │        │  ├─ type: ElementaryTypeName
      │  │        │  └─ name: bool
      │  │        ├─ name: refunded
      │  │        ├─ storageLocation
      │  │        ├─ isStateVar: false
      │  │        └─ isIndexed: false
      │  ├─ 3
      │  │  ├─ type: StateVariableDeclaration
      │  │  ├─ variables
      │  │  │  └─ 0
      │  │  │     ├─ type: VariableDeclaration
      │  │  │     ├─ typeName
      │  │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  └─ name: uint
      │  │  │     ├─ name: numBounties
      │  │  │     ├─ expression
      │  │  │     ├─ visibility: public
      │  │  │     ├─ isStateVar: true
      │  │  │     ├─ isDeclaredConst: false
      │  │  │     └─ isIndexed: false
      │  │  └─ initialValue
      │  ├─ 4
      │  │  ├─ type: StateVariableDeclaration
      │  │  ├─ variables
      │  │  │  └─ 0
      │  │  │     ├─ type: VariableDeclaration
      │  │  │     ├─ typeName
      │  │  │     │  ├─ type: Mapping
      │  │  │     │  ├─ keyType
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  └─ valueType
      │  │  │     │     ├─ type: UserDefinedTypeName
      │  │  │     │     └─ namePath: Bounty
      │  │  │     ├─ name: bounties
      │  │  │     ├─ expression
      │  │  │     ├─ visibility: public
      │  │  │     ├─ isStateVar: true
      │  │  │     ├─ isDeclaredConst: false
      │  │  │     └─ isIndexed: false
      │  │  └─ initialValue
      │  ├─ 5
      │  │  ├─ type: StateVariableDeclaration
      │  │  ├─ variables
      │  │  │  └─ 0
      │  │  │     ├─ type: VariableDeclaration
      │  │  │     ├─ typeName
      │  │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  └─ name: address
      │  │  │     ├─ name: owner
      │  │  │     ├─ expression
      │  │  │     ├─ visibility: default
      │  │  │     ├─ isStateVar: true
      │  │  │     ├─ isDeclaredConst: false
      │  │  │     └─ isIndexed: false
      │  │  └─ initialValue
      │  ├─ 6
      │  │  ├─ type: StateVariableDeclaration
      │  │  ├─ variables
      │  │  │  └─ 0
      │  │  │     ├─ type: VariableDeclaration
      │  │  │     ├─ typeName
      │  │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  └─ name: address
      │  │  │     ├─ name: metaTxRelayer
      │  │  │     ├─ expression
      │  │  │     ├─ visibility: default
      │  │  │     ├─ isStateVar: true
      │  │  │     ├─ isDeclaredConst: false
      │  │  │     └─ isIndexed: false
      │  │  └─ initialValue
      │  ├─ 7
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: validateBountyArrayIndex
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _index
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: <
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: Identifier
      │  │        │     │     │  └─ name: _index
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: Identifier
      │  │        │     │        └─ name: numBounties
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 8
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: validateContributionArrayIndex
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 1
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _index
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: <
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: Identifier
      │  │        │     │     │  └─ name: _index
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: MemberAccess
      │  │        │     │        ├─ expression
      │  │        │     │        │  ├─ type: MemberAccess
      │  │        │     │        │  ├─ expression
      │  │        │     │        │  │  ├─ type: IndexAccess
      │  │        │     │        │  │  ├─ base
      │  │        │     │        │  │  │  ├─ type: Identifier
      │  │        │     │        │  │  │  └─ name: bounties
      │  │        │     │        │  │  └─ index
      │  │        │     │        │  │     ├─ type: Identifier
      │  │        │     │        │  │     └─ name: _bountyId
      │  │        │     │        │  └─ memberName: contributions
      │  │        │     │        └─ memberName: length
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 9
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: validateFulfillmentArrayIndex
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 1
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _index
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: <
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: Identifier
      │  │        │     │     │  └─ name: _index
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: MemberAccess
      │  │        │     │        ├─ expression
      │  │        │     │        │  ├─ type: MemberAccess
      │  │        │     │        │  ├─ expression
      │  │        │     │        │  │  ├─ type: IndexAccess
      │  │        │     │        │  │  ├─ base
      │  │        │     │        │  │  │  ├─ type: Identifier
      │  │        │     │        │  │  │  └─ name: bounties
      │  │        │     │        │  │  └─ index
      │  │        │     │        │  │     ├─ type: Identifier
      │  │        │     │        │  │     └─ name: _bountyId
      │  │        │     │        │  └─ memberName: fulfillments
      │  │        │     │        └─ memberName: length
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 10
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: validateIssuerArrayIndex
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 1
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _index
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: ||
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: BinaryOperation
      │  │        │     │     │  ├─ operator: <
      │  │        │     │     │  ├─ left
      │  │        │     │     │  │  ├─ type: Identifier
      │  │        │     │     │  │  └─ name: _index
      │  │        │     │     │  └─ right
      │  │        │     │     │     ├─ type: MemberAccess
      │  │        │     │     │     ├─ expression
      │  │        │     │     │     │  ├─ type: MemberAccess
      │  │        │     │     │     │  ├─ expression
      │  │        │     │     │     │  │  ├─ type: IndexAccess
      │  │        │     │     │     │  │  ├─ base
      │  │        │     │     │     │  │  │  ├─ type: Identifier
      │  │        │     │     │     │  │  │  └─ name: bounties
      │  │        │     │     │     │  │  └─ index
      │  │        │     │     │     │  │     ├─ type: Identifier
      │  │        │     │     │     │  │     └─ name: _bountyId
      │  │        │     │     │     │  └─ memberName: issuers
      │  │        │     │     │     └─ memberName: length
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: BinaryOperation
      │  │        │     │        ├─ operator: ==
      │  │        │     │        ├─ left
      │  │        │     │        │  ├─ type: Identifier
      │  │        │     │        │  └─ name: _index
      │  │        │     │        └─ right
      │  │        │     │           ├─ type: NumberLiteral
      │  │        │     │           ├─ number: 0
      │  │        │     │           └─ subdenomination
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 11
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: validateApproverArrayIndex
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 1
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _index
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: ||
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: BinaryOperation
      │  │        │     │     │  ├─ operator: <
      │  │        │     │     │  ├─ left
      │  │        │     │     │  │  ├─ type: Identifier
      │  │        │     │     │  │  └─ name: _index
      │  │        │     │     │  └─ right
      │  │        │     │     │     ├─ type: MemberAccess
      │  │        │     │     │     ├─ expression
      │  │        │     │     │     │  ├─ type: MemberAccess
      │  │        │     │     │     │  ├─ expression
      │  │        │     │     │     │  │  ├─ type: IndexAccess
      │  │        │     │     │     │  │  ├─ base
      │  │        │     │     │     │  │  │  ├─ type: Identifier
      │  │        │     │     │     │  │  │  └─ name: bounties
      │  │        │     │     │     │  │  └─ index
      │  │        │     │     │     │  │     ├─ type: Identifier
      │  │        │     │     │     │  │     └─ name: _bountyId
      │  │        │     │     │     │  └─ memberName: approvers
      │  │        │     │     │     └─ memberName: length
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: BinaryOperation
      │  │        │     │        ├─ operator: ==
      │  │        │     │        ├─ left
      │  │        │     │        │  ├─ type: Identifier
      │  │        │     │        │  └─ name: _index
      │  │        │     │        └─ right
      │  │        │     │           ├─ type: NumberLiteral
      │  │        │     │           ├─ number: 0
      │  │        │     │           └─ subdenomination
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 12
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: onlyIssuer
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _issuerId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: ==
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: Identifier
      │  │        │     │     │  └─ name: _sender
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: IndexAccess
      │  │        │     │        ├─ base
      │  │        │     │        │  ├─ type: MemberAccess
      │  │        │     │        │  ├─ expression
      │  │        │     │        │  │  ├─ type: IndexAccess
      │  │        │     │        │  │  ├─ base
      │  │        │     │        │  │  │  ├─ type: Identifier
      │  │        │     │        │  │  │  └─ name: bounties
      │  │        │     │        │  │  └─ index
      │  │        │     │        │  │     ├─ type: Identifier
      │  │        │     │        │  │     └─ name: _bountyId
      │  │        │     │        │  └─ memberName: issuers
      │  │        │     │        └─ index
      │  │        │     │           ├─ type: Identifier
      │  │        │     │           └─ name: _issuerId
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 13
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: onlySubmitter
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _fulfillmentId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: ==
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: Identifier
      │  │        │     │     │  └─ name: _sender
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: MemberAccess
      │  │        │     │        ├─ expression
      │  │        │     │        │  ├─ type: IndexAccess
      │  │        │     │        │  ├─ base
      │  │        │     │        │  │  ├─ type: MemberAccess
      │  │        │     │        │  │  ├─ expression
      │  │        │     │        │  │  │  ├─ type: IndexAccess
      │  │        │     │        │  │  │  ├─ base
      │  │        │     │        │  │  │  │  ├─ type: Identifier
      │  │        │     │        │  │  │  │  └─ name: bounties
      │  │        │     │        │  │  │  └─ index
      │  │        │     │        │  │  │     ├─ type: Identifier
      │  │        │     │        │  │  │     └─ name: _bountyId
      │  │        │     │        │  │  └─ memberName: fulfillments
      │  │        │     │        │  └─ index
      │  │        │     │        │     ├─ type: Identifier
      │  │        │     │        │     └─ name: _fulfillmentId
      │  │        │     │        └─ memberName: submitter
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 14
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: onlyContributor
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _contributionId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: ==
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: Identifier
      │  │        │     │     │  └─ name: _sender
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: MemberAccess
      │  │        │     │        ├─ expression
      │  │        │     │        │  ├─ type: IndexAccess
      │  │        │     │        │  ├─ base
      │  │        │     │        │  │  ├─ type: MemberAccess
      │  │        │     │        │  │  ├─ expression
      │  │        │     │        │  │  │  ├─ type: IndexAccess
      │  │        │     │        │  │  │  ├─ base
      │  │        │     │        │  │  │  │  ├─ type: Identifier
      │  │        │     │        │  │  │  │  └─ name: bounties
      │  │        │     │        │  │  │  └─ index
      │  │        │     │        │  │  │     ├─ type: Identifier
      │  │        │     │        │  │  │     └─ name: _bountyId
      │  │        │     │        │  │  └─ memberName: contributions
      │  │        │     │        │  └─ index
      │  │        │     │        │     ├─ type: Identifier
      │  │        │     │        │     └─ name: _contributionId
      │  │        │     │        └─ memberName: contributor
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 15
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: isApprover
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _approverId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: ==
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: Identifier
      │  │        │     │     │  └─ name: _sender
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: IndexAccess
      │  │        │     │        ├─ base
      │  │        │     │        │  ├─ type: MemberAccess
      │  │        │     │        │  ├─ expression
      │  │        │     │        │  │  ├─ type: IndexAccess
      │  │        │     │        │  │  ├─ base
      │  │        │     │        │  │  │  ├─ type: Identifier
      │  │        │     │        │  │  │  └─ name: bounties
      │  │        │     │        │  │  └─ index
      │  │        │     │        │  │     ├─ type: Identifier
      │  │        │     │        │  │     └─ name: _bountyId
      │  │        │     │        │  └─ memberName: approvers
      │  │        │     │        └─ index
      │  │        │     │           ├─ type: Identifier
      │  │        │     │           └─ name: _approverId
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 16
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: hasNotPaid
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _bountyId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: UnaryOperation
      │  │        │     │     ├─ operator: !
      │  │        │     │     ├─ subExpression
      │  │        │     │     │  ├─ type: MemberAccess
      │  │        │     │     │  ├─ expression
      │  │        │     │     │  │  ├─ type: IndexAccess
      │  │        │     │     │  │  ├─ base
      │  │        │     │     │  │  │  ├─ type: Identifier
      │  │        │     │     │  │  │  └─ name: bounties
      │  │        │     │     │  │  └─ index
      │  │        │     │     │  │     ├─ type: Identifier
      │  │        │     │     │  │     └─ name: _bountyId
      │  │        │     │     │  └─ memberName: hasPaidOut
      │  │        │     │     └─ isPrefix: true
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 17
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: hasNotRefunded
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 1
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _contributionId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: UnaryOperation
      │  │        │     │     ├─ operator: !
      │  │        │     │     ├─ subExpression
      │  │        │     │     │  ├─ type: MemberAccess
      │  │        │     │     │  ├─ expression
      │  │        │     │     │  │  ├─ type: IndexAccess
      │  │        │     │     │  │  ├─ base
      │  │        │     │     │  │  │  ├─ type: MemberAccess
      │  │        │     │     │  │  │  ├─ expression
      │  │        │     │     │  │  │  │  ├─ type: IndexAccess
      │  │        │     │     │  │  │  │  ├─ base
      │  │        │     │     │  │  │  │  │  ├─ type: Identifier
      │  │        │     │     │  │  │  │  │  └─ name: bounties
      │  │        │     │     │  │  │  │  └─ index
      │  │        │     │     │  │  │  │     ├─ type: Identifier
      │  │        │     │     │  │  │  │     └─ name: _bountyId
      │  │        │     │     │  │  │  └─ memberName: contributions
      │  │        │     │     │  │  └─ index
      │  │        │     │     │  │     ├─ type: Identifier
      │  │        │     │     │  │     └─ name: _contributionId
      │  │        │     │     │  └─ memberName: refunded
      │  │        │     │     └─ isPrefix: true
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 18
      │  │  ├─ type: ModifierDefinition
      │  │  ├─ name: senderIsValid
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: address
      │  │  │        ├─ name: _sender
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ body
      │  │     ├─ type: Block
      │  │     └─ statements
      │  │        ├─ 0
      │  │        │  ├─ type: ExpressionStatement
      │  │        │  └─ expression
      │  │        │     ├─ type: FunctionCall
      │  │        │     ├─ expression
      │  │        │     │  ├─ type: Identifier
      │  │        │     │  └─ name: require
      │  │        │     ├─ arguments
      │  │        │     │  └─ 0
      │  │        │     │     ├─ type: BinaryOperation
      │  │        │     │     ├─ operator: ||
      │  │        │     │     ├─ left
      │  │        │     │     │  ├─ type: BinaryOperation
      │  │        │     │     │  ├─ operator: ==
      │  │        │     │     │  ├─ left
      │  │        │     │     │  │  ├─ type: MemberAccess
      │  │        │     │     │  │  ├─ expression
      │  │        │     │     │  │  │  ├─ type: Identifier
      │  │        │     │     │  │  │  └─ name: msg
      │  │        │     │     │  │  └─ memberName: sender
      │  │        │     │     │  └─ right
      │  │        │     │     │     ├─ type: Identifier
      │  │        │     │     │     └─ name: _sender
      │  │        │     │     └─ right
      │  │        │     │        ├─ type: BinaryOperation
      │  │        │     │        ├─ operator: ==
      │  │        │     │        ├─ left
      │  │        │     │        │  ├─ type: MemberAccess
      │  │        │     │        │  ├─ expression
      │  │        │     │        │  │  ├─ type: Identifier
      │  │        │     │        │  │  └─ name: msg
      │  │        │     │        │  └─ memberName: sender
      │  │        │     │        └─ right
      │  │        │     │           ├─ type: Identifier
      │  │        │     │           └─ name: metaTxRelayer
      │  │        │     └─ names
      │  │        └─ 1
      │  │           ├─ type: ExpressionStatement
      │  │           └─ expression
      │  │              ├─ type: Identifier
      │  │              └─ name: _
      │  ├─ 19
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     └─ 0
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: BinaryOperation
      │  │  │           ├─ operator: =
      │  │  │           ├─ left
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: owner
      │  │  │           └─ right
      │  │  │              ├─ type: MemberAccess
      │  │  │              ├─ expression
      │  │  │              │  ├─ type: Identifier
      │  │  │              │  └─ name: msg
      │  │  │              └─ memberName: sender
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: true
      │  │  └─ stateMutability
      │  ├─ 20
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: setMetaTxRelayer
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: address
      │  │  │        ├─ name: _relayer
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: msg
      │  │  │     │     │     │  └─ memberName: sender
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: Identifier
      │  │  │     │     │        └─ name: owner
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: metaTxRelayer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     └─ 2
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: BinaryOperation
      │  │  │           ├─ operator: =
      │  │  │           ├─ left
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: metaTxRelayer
      │  │  │           └─ right
      │  │  │              ├─ type: Identifier
      │  │  │              └─ name: _relayer
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 21
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: issueBounty
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  └─ name: address
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _deadline
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 5
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _token
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 6
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _tokenVersion
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 7
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _depositAmount
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ||
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: BinaryOperation
      │  │  │     │     │     │  ├─ operator: ||
      │  │  │     │     │     │  ├─ left
      │  │  │     │     │     │  │  ├─ type: BinaryOperation
      │  │  │     │     │     │  │  ├─ operator: ==
      │  │  │     │     │     │  │  ├─ left
      │  │  │     │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  │  └─ name: _tokenVersion
      │  │  │     │     │     │  │  └─ right
      │  │  │     │     │     │  │     ├─ type: NumberLiteral
      │  │  │     │     │     │  │     ├─ number: 0
      │  │  │     │     │     │  │     └─ subdenomination
      │  │  │     │     │     │  └─ right
      │  │  │     │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     │     ├─ operator: ==
      │  │  │     │     │     │     ├─ left
      │  │  │     │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │     │  └─ name: _tokenVersion
      │  │  │     │     │     │     └─ right
      │  │  │     │     │     │        ├─ type: NumberLiteral
      │  │  │     │     │     │        ├─ number: 20
      │  │  │     │     │     │        └─ subdenomination
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: BinaryOperation
      │  │  │     │     │        ├─ operator: ==
      │  │  │     │     │        ├─ left
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: _tokenVersion
      │  │  │     │     │        └─ right
      │  │  │     │     │           ├─ type: NumberLiteral
      │  │  │     │     │           ├─ number: 721
      │  │  │     │     │           └─ subdenomination
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: uint
      │  │  │     │  │     ├─ name: bountyId
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: Identifier
      │  │  │     │     └─ name: numBounties
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: UserDefinedTypeName
      │  │  │     │  │     │  └─ namePath: Bounty
      │  │  │     │  │     ├─ name: newBounty
      │  │  │     │  │     ├─ storageLocation: storage
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: IndexAccess
      │  │  │     │     ├─ base
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: bounties
      │  │  │     │     └─ index
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: bountyId
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: newBounty
      │  │  │     │     │  └─ memberName: issuers
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _issuers
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: newBounty
      │  │  │     │     │  └─ memberName: approvers
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _approvers
      │  │  │     ├─ 5
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: newBounty
      │  │  │     │     │  └─ memberName: deadline
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _deadline
      │  │  │     ├─ 6
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: newBounty
      │  │  │     │     │  └─ memberName: token
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _token
      │  │  │     ├─ 7
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: newBounty
      │  │  │     │     │  └─ memberName: tokenVersion
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _tokenVersion
      │  │  │     ├─ 8
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: numBounties
      │  │  │     │     └─ isPrefix: false
      │  │  │     ├─ 9
      │  │  │     │  ├─ type: EmitStatement
      │  │  │     │  └─ eventCall
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: BountyIssued
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: bountyId
      │  │  │     │     │  ├─ 1
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _sender
      │  │  │     │     │  ├─ 2
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _issuers
      │  │  │     │     │  ├─ 3
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _approvers
      │  │  │     │     │  ├─ 4
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _data
      │  │  │     │     │  ├─ 5
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _deadline
      │  │  │     │     │  ├─ 6
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _token
      │  │  │     │     │  └─ 7
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _tokenVersion
      │  │  │     │     └─ names
      │  │  │     ├─ 10
      │  │  │     │  ├─ type: IfStatement
      │  │  │     │  ├─ condition
      │  │  │     │  │  ├─ type: BinaryOperation
      │  │  │     │  │  ├─ operator: >
      │  │  │     │  │  ├─ left
      │  │  │     │  │  │  ├─ type: Identifier
      │  │  │     │  │  │  └─ name: _depositAmount
      │  │  │     │  │  └─ right
      │  │  │     │  │     ├─ type: NumberLiteral
      │  │  │     │  │     ├─ number: 0
      │  │  │     │  │     └─ subdenomination
      │  │  │     │  ├─ trueBody
      │  │  │     │  │  ├─ type: Block
      │  │  │     │  │  └─ statements
      │  │  │     │  │     └─ 0
      │  │  │     │  │        ├─ type: ExpressionStatement
      │  │  │     │  │        └─ expression
      │  │  │     │  │           ├─ type: FunctionCall
      │  │  │     │  │           ├─ expression
      │  │  │     │  │           │  ├─ type: Identifier
      │  │  │     │  │           │  └─ name: contribute
      │  │  │     │  │           ├─ arguments
      │  │  │     │  │           │  ├─ 0
      │  │  │     │  │           │  │  ├─ type: Identifier
      │  │  │     │  │           │  │  └─ name: _sender
      │  │  │     │  │           │  ├─ 1
      │  │  │     │  │           │  │  ├─ type: Identifier
      │  │  │     │  │           │  │  └─ name: bountyId
      │  │  │     │  │           │  └─ 2
      │  │  │     │  │           │     ├─ type: Identifier
      │  │  │     │  │           │     └─ name: _depositAmount
      │  │  │     │  │           └─ names
      │  │  │     │  └─ falseBody
      │  │  │     └─ 11
      │  │  │        ├─ type: ReturnStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: TupleExpression
      │  │  │           ├─ components
      │  │  │           │  └─ 0
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: bountyId
      │  │  │           └─ isArray: false
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  └─ 0
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: senderIsValid
      │  │  │     └─ arguments
      │  │  │        └─ 0
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _sender
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability: payable
      │  ├─ 22
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: contribute
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _amount
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: MemberAccess
      │  │  │     │     │  │  ├─ expression
      │  │  │     │     │  │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  │  ├─ base
      │  │  │     │     │  │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  │  └─ name: bounties
      │  │  │     │     │  │  │  └─ index
      │  │  │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │  │  │     └─ name: _bountyId
      │  │  │     │     │  │  └─ memberName: contributions
      │  │  │     │     │  └─ memberName: push
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: Contribution
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _sender
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _amount
      │  │  │     │     │     │  └─ 2
      │  │  │     │     │     │     ├─ type: BooleanLiteral
      │  │  │     │     │     │     └─ value: false
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: +=
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: balance
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _amount
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: >
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _amount
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: NumberLiteral
      │  │  │     │     │        ├─ number: 0
      │  │  │     │     │        └─ subdenomination
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: IfStatement
      │  │  │     │  ├─ condition
      │  │  │     │  │  ├─ type: BinaryOperation
      │  │  │     │  │  ├─ operator: ==
      │  │  │     │  │  ├─ left
      │  │  │     │  │  │  ├─ type: MemberAccess
      │  │  │     │  │  │  ├─ expression
      │  │  │     │  │  │  │  ├─ type: IndexAccess
      │  │  │     │  │  │  │  ├─ base
      │  │  │     │  │  │  │  │  ├─ type: Identifier
      │  │  │     │  │  │  │  │  └─ name: bounties
      │  │  │     │  │  │  │  └─ index
      │  │  │     │  │  │  │     ├─ type: Identifier
      │  │  │     │  │  │  │     └─ name: _bountyId
      │  │  │     │  │  │  └─ memberName: tokenVersion
      │  │  │     │  │  └─ right
      │  │  │     │  │     ├─ type: NumberLiteral
      │  │  │     │  │     ├─ number: 0
      │  │  │     │  │     └─ subdenomination
      │  │  │     │  ├─ trueBody
      │  │  │     │  │  ├─ type: Block
      │  │  │     │  │  └─ statements
      │  │  │     │  │     └─ 0
      │  │  │     │  │        ├─ type: ExpressionStatement
      │  │  │     │  │        └─ expression
      │  │  │     │  │           ├─ type: FunctionCall
      │  │  │     │  │           ├─ expression
      │  │  │     │  │           │  ├─ type: Identifier
      │  │  │     │  │           │  └─ name: require
      │  │  │     │  │           ├─ arguments
      │  │  │     │  │           │  └─ 0
      │  │  │     │  │           │     ├─ type: BinaryOperation
      │  │  │     │  │           │     ├─ operator: ==
      │  │  │     │  │           │     ├─ left
      │  │  │     │  │           │     │  ├─ type: MemberAccess
      │  │  │     │  │           │     │  ├─ expression
      │  │  │     │  │           │     │  │  ├─ type: Identifier
      │  │  │     │  │           │     │  │  └─ name: msg
      │  │  │     │  │           │     │  └─ memberName: value
      │  │  │     │  │           │     └─ right
      │  │  │     │  │           │        ├─ type: Identifier
      │  │  │     │  │           │        └─ name: _amount
      │  │  │     │  │           └─ names
      │  │  │     │  └─ falseBody
      │  │  │     │     ├─ type: IfStatement
      │  │  │     │     ├─ condition
      │  │  │     │     │  ├─ type: BinaryOperation
      │  │  │     │     │  ├─ operator: ==
      │  │  │     │     │  ├─ left
      │  │  │     │     │  │  ├─ type: MemberAccess
      │  │  │     │     │  │  ├─ expression
      │  │  │     │     │  │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  │  ├─ base
      │  │  │     │     │  │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  │  └─ name: bounties
      │  │  │     │     │  │  │  └─ index
      │  │  │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │  │  │     └─ name: _bountyId
      │  │  │     │     │  │  └─ memberName: tokenVersion
      │  │  │     │     │  └─ right
      │  │  │     │     │     ├─ type: NumberLiteral
      │  │  │     │     │     ├─ number: 20
      │  │  │     │     │     └─ subdenomination
      │  │  │     │     ├─ trueBody
      │  │  │     │     │  ├─ type: Block
      │  │  │     │     │  └─ statements
      │  │  │     │     │     ├─ 0
      │  │  │     │     │     │  ├─ type: ExpressionStatement
      │  │  │     │     │     │  └─ expression
      │  │  │     │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     │     ├─ expression
      │  │  │     │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │     │  └─ name: require
      │  │  │     │     │     │     ├─ arguments
      │  │  │     │     │     │     │  └─ 0
      │  │  │     │     │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     │     │     ├─ operator: ==
      │  │  │     │     │     │     │     ├─ left
      │  │  │     │     │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │     │     │  ├─ expression
      │  │  │     │     │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │     │     │  │  └─ name: msg
      │  │  │     │     │     │     │     │  └─ memberName: value
      │  │  │     │     │     │     │     └─ right
      │  │  │     │     │     │     │        ├─ type: NumberLiteral
      │  │  │     │     │     │     │        ├─ number: 0
      │  │  │     │     │     │     │        └─ subdenomination
      │  │  │     │     │     │     └─ names
      │  │  │     │     │     └─ 1
      │  │  │     │     │        ├─ type: ExpressionStatement
      │  │  │     │     │        └─ expression
      │  │  │     │     │           ├─ type: FunctionCall
      │  │  │     │     │           ├─ expression
      │  │  │     │     │           │  ├─ type: Identifier
      │  │  │     │     │           │  └─ name: require
      │  │  │     │     │           ├─ arguments
      │  │  │     │     │           │  └─ 0
      │  │  │     │     │           │     ├─ type: FunctionCall
      │  │  │     │     │           │     ├─ expression
      │  │  │     │     │           │     │  ├─ type: MemberAccess
      │  │  │     │     │           │     │  ├─ expression
      │  │  │     │     │           │     │  │  ├─ type: FunctionCall
      │  │  │     │     │           │     │  │  ├─ expression
      │  │  │     │     │           │     │  │  │  ├─ type: Identifier
      │  │  │     │     │           │     │  │  │  └─ name: ERC20Token
      │  │  │     │     │           │     │  │  ├─ arguments
      │  │  │     │     │           │     │  │  │  └─ 0
      │  │  │     │     │           │     │  │  │     ├─ type: MemberAccess
      │  │  │     │     │           │     │  │  │     ├─ expression
      │  │  │     │     │           │     │  │  │     │  ├─ type: IndexAccess
      │  │  │     │     │           │     │  │  │     │  ├─ base
      │  │  │     │     │           │     │  │  │     │  │  ├─ type: Identifier
      │  │  │     │     │           │     │  │  │     │  │  └─ name: bounties
      │  │  │     │     │           │     │  │  │     │  └─ index
      │  │  │     │     │           │     │  │  │     │     ├─ type: Identifier
      │  │  │     │     │           │     │  │  │     │     └─ name: _bountyId
      │  │  │     │     │           │     │  │  │     └─ memberName: token
      │  │  │     │     │           │     │  │  └─ names
      │  │  │     │     │           │     │  └─ memberName: transferFrom
      │  │  │     │     │           │     ├─ arguments
      │  │  │     │     │           │     │  ├─ 0
      │  │  │     │     │           │     │  │  ├─ type: Identifier
      │  │  │     │     │           │     │  │  └─ name: _sender
      │  │  │     │     │           │     │  ├─ 1
      │  │  │     │     │           │     │  │  ├─ type: FunctionCall
      │  │  │     │     │           │     │  │  ├─ expression
      │  │  │     │     │           │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │           │     │  │  │  └─ typeName
      │  │  │     │     │           │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │           │     │  │  │     └─ name: address
      │  │  │     │     │           │     │  │  ├─ arguments
      │  │  │     │     │           │     │  │  │  └─ 0
      │  │  │     │     │           │     │  │  │     ├─ type: Identifier
      │  │  │     │     │           │     │  │  │     └─ name: this
      │  │  │     │     │           │     │  │  └─ names
      │  │  │     │     │           │     │  └─ 2
      │  │  │     │     │           │     │     ├─ type: Identifier
      │  │  │     │     │           │     │     └─ name: _amount
      │  │  │     │     │           │     └─ names
      │  │  │     │     │           └─ names
      │  │  │     │     └─ falseBody
      │  │  │     │        ├─ type: IfStatement
      │  │  │     │        ├─ condition
      │  │  │     │        │  ├─ type: BinaryOperation
      │  │  │     │        │  ├─ operator: ==
      │  │  │     │        │  ├─ left
      │  │  │     │        │  │  ├─ type: MemberAccess
      │  │  │     │        │  │  ├─ expression
      │  │  │     │        │  │  │  ├─ type: IndexAccess
      │  │  │     │        │  │  │  ├─ base
      │  │  │     │        │  │  │  │  ├─ type: Identifier
      │  │  │     │        │  │  │  │  └─ name: bounties
      │  │  │     │        │  │  │  └─ index
      │  │  │     │        │  │  │     ├─ type: Identifier
      │  │  │     │        │  │  │     └─ name: _bountyId
      │  │  │     │        │  │  └─ memberName: tokenVersion
      │  │  │     │        │  └─ right
      │  │  │     │        │     ├─ type: NumberLiteral
      │  │  │     │        │     ├─ number: 721
      │  │  │     │        │     └─ subdenomination
      │  │  │     │        ├─ trueBody
      │  │  │     │        │  ├─ type: Block
      │  │  │     │        │  └─ statements
      │  │  │     │        │     ├─ 0
      │  │  │     │        │     │  ├─ type: ExpressionStatement
      │  │  │     │        │     │  └─ expression
      │  │  │     │        │     │     ├─ type: FunctionCall
      │  │  │     │        │     │     ├─ expression
      │  │  │     │        │     │     │  ├─ type: Identifier
      │  │  │     │        │     │     │  └─ name: require
      │  │  │     │        │     │     ├─ arguments
      │  │  │     │        │     │     │  └─ 0
      │  │  │     │        │     │     │     ├─ type: BinaryOperation
      │  │  │     │        │     │     │     ├─ operator: ==
      │  │  │     │        │     │     │     ├─ left
      │  │  │     │        │     │     │     │  ├─ type: MemberAccess
      │  │  │     │        │     │     │     │  ├─ expression
      │  │  │     │        │     │     │     │  │  ├─ type: Identifier
      │  │  │     │        │     │     │     │  │  └─ name: msg
      │  │  │     │        │     │     │     │  └─ memberName: value
      │  │  │     │        │     │     │     └─ right
      │  │  │     │        │     │     │        ├─ type: NumberLiteral
      │  │  │     │        │     │     │        ├─ number: 0
      │  │  │     │        │     │     │        └─ subdenomination
      │  │  │     │        │     │     └─ names
      │  │  │     │        │     └─ 1
      │  │  │     │        │        ├─ type: ExpressionStatement
      │  │  │     │        │        └─ expression
      │  │  │     │        │           ├─ type: FunctionCall
      │  │  │     │        │           ├─ expression
      │  │  │     │        │           │  ├─ type: MemberAccess
      │  │  │     │        │           │  ├─ expression
      │  │  │     │        │           │  │  ├─ type: FunctionCall
      │  │  │     │        │           │  │  ├─ expression
      │  │  │     │        │           │  │  │  ├─ type: Identifier
      │  │  │     │        │           │  │  │  └─ name: ERC721BasicToken
      │  │  │     │        │           │  │  ├─ arguments
      │  │  │     │        │           │  │  │  └─ 0
      │  │  │     │        │           │  │  │     ├─ type: MemberAccess
      │  │  │     │        │           │  │  │     ├─ expression
      │  │  │     │        │           │  │  │     │  ├─ type: IndexAccess
      │  │  │     │        │           │  │  │     │  ├─ base
      │  │  │     │        │           │  │  │     │  │  ├─ type: Identifier
      │  │  │     │        │           │  │  │     │  │  └─ name: bounties
      │  │  │     │        │           │  │  │     │  └─ index
      │  │  │     │        │           │  │  │     │     ├─ type: Identifier
      │  │  │     │        │           │  │  │     │     └─ name: _bountyId
      │  │  │     │        │           │  │  │     └─ memberName: token
      │  │  │     │        │           │  │  └─ names
      │  │  │     │        │           │  └─ memberName: transferFrom
      │  │  │     │        │           ├─ arguments
      │  │  │     │        │           │  ├─ 0
      │  │  │     │        │           │  │  ├─ type: Identifier
      │  │  │     │        │           │  │  └─ name: _sender
      │  │  │     │        │           │  ├─ 1
      │  │  │     │        │           │  │  ├─ type: FunctionCall
      │  │  │     │        │           │  │  ├─ expression
      │  │  │     │        │           │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │        │           │  │  │  └─ typeName
      │  │  │     │        │           │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │        │           │  │  │     └─ name: address
      │  │  │     │        │           │  │  ├─ arguments
      │  │  │     │        │           │  │  │  └─ 0
      │  │  │     │        │           │  │  │     ├─ type: Identifier
      │  │  │     │        │           │  │  │     └─ name: this
      │  │  │     │        │           │  │  └─ names
      │  │  │     │        │           │  └─ 2
      │  │  │     │        │           │     ├─ type: Identifier
      │  │  │     │        │           │     └─ name: _amount
      │  │  │     │        │           └─ names
      │  │  │     │        └─ falseBody
      │  │  │     └─ 4
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: ContributionAdded
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: BinaryOperation
      │  │  │           │  │  ├─ operator: -
      │  │  │           │  │  ├─ left
      │  │  │           │  │  │  ├─ type: MemberAccess
      │  │  │           │  │  │  ├─ expression
      │  │  │           │  │  │  │  ├─ type: MemberAccess
      │  │  │           │  │  │  │  ├─ expression
      │  │  │           │  │  │  │  │  ├─ type: IndexAccess
      │  │  │           │  │  │  │  │  ├─ base
      │  │  │           │  │  │  │  │  │  ├─ type: Identifier
      │  │  │           │  │  │  │  │  │  └─ name: bounties
      │  │  │           │  │  │  │  │  └─ index
      │  │  │           │  │  │  │  │     ├─ type: Identifier
      │  │  │           │  │  │  │  │     └─ name: _bountyId
      │  │  │           │  │  │  │  └─ memberName: contributions
      │  │  │           │  │  │  └─ memberName: length
      │  │  │           │  │  └─ right
      │  │  │           │  │     ├─ type: NumberLiteral
      │  │  │           │  │     ├─ number: 1
      │  │  │           │  │     └─ subdenomination
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _amount
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  └─ 1
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: validateBountyArrayIndex
      │  │  │     └─ arguments
      │  │  │        └─ 0
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _bountyId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability: payable
      │  ├─ 23
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: refundContribution
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _contributionId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: >
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: now
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: MemberAccess
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: IndexAccess
      │  │  │     │     │        │  ├─ base
      │  │  │     │     │        │  │  ├─ type: Identifier
      │  │  │     │     │        │  │  └─ name: bounties
      │  │  │     │     │        │  └─ index
      │  │  │     │     │        │     ├─ type: Identifier
      │  │  │     │     │        │     └─ name: _bountyId
      │  │  │     │     │        └─ memberName: deadline
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: UserDefinedTypeName
      │  │  │     │  │     │  └─ namePath: Contribution
      │  │  │     │  │     ├─ name: contribution
      │  │  │     │  │     ├─ storageLocation: storage
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: IndexAccess
      │  │  │     │     ├─ base
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: contributions
      │  │  │     │     └─ index
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _contributionId
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: contribution
      │  │  │     │     │  └─ memberName: refunded
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: BooleanLiteral
      │  │  │     │        └─ value: true
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: -=
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: balance
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: MemberAccess
      │  │  │     │        ├─ expression
      │  │  │     │        │  ├─ type: Identifier
      │  │  │     │        │  └─ name: contribution
      │  │  │     │        └─ memberName: amount
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: transferTokens
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _bountyId
      │  │  │     │     │  ├─ 1
      │  │  │     │     │  │  ├─ type: MemberAccess
      │  │  │     │     │  │  ├─ expression
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: contribution
      │  │  │     │     │  │  └─ memberName: contributor
      │  │  │     │     │  └─ 2
      │  │  │     │     │     ├─ type: MemberAccess
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: contribution
      │  │  │     │     │     └─ memberName: amount
      │  │  │     │     └─ names
      │  │  │     └─ 5
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: ContributionRefunded
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  └─ 1
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _contributionId
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateContributionArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _contributionId
      │  │  │  ├─ 3
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: onlyContributor
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _sender
      │  │  │  │     ├─ 1
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 2
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _contributionId
      │  │  │  ├─ 4
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: hasNotPaid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  └─ 5
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: hasNotRefunded
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 1
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _contributionId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 24
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: refundContributions
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: uint
      │  │  │        │  └─ length
      │  │  │        ├─ name: _contributionIds
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     └─ 0
      │  │  │        ├─ type: ForStatement
      │  │  │        ├─ initExpression
      │  │  │        │  ├─ type: VariableDeclarationStatement
      │  │  │        │  ├─ variables
      │  │  │        │  │  └─ 0
      │  │  │        │  │     ├─ type: VariableDeclaration
      │  │  │        │  │     ├─ typeName
      │  │  │        │  │     │  ├─ type: ElementaryTypeName
      │  │  │        │  │     │  └─ name: uint
      │  │  │        │  │     ├─ name: i
      │  │  │        │  │     ├─ storageLocation
      │  │  │        │  │     ├─ isStateVar: false
      │  │  │        │  │     └─ isIndexed: false
      │  │  │        │  └─ initialValue
      │  │  │        │     ├─ type: NumberLiteral
      │  │  │        │     ├─ number: 0
      │  │  │        │     └─ subdenomination
      │  │  │        ├─ conditionExpression
      │  │  │        │  ├─ type: BinaryOperation
      │  │  │        │  ├─ operator: <
      │  │  │        │  ├─ left
      │  │  │        │  │  ├─ type: Identifier
      │  │  │        │  │  └─ name: i
      │  │  │        │  └─ right
      │  │  │        │     ├─ type: MemberAccess
      │  │  │        │     ├─ expression
      │  │  │        │     │  ├─ type: Identifier
      │  │  │        │     │  └─ name: _contributionIds
      │  │  │        │     └─ memberName: length
      │  │  │        ├─ loopExpression
      │  │  │        │  ├─ type: ExpressionStatement
      │  │  │        │  └─ expression
      │  │  │        │     ├─ type: UnaryOperation
      │  │  │        │     ├─ operator: ++
      │  │  │        │     ├─ subExpression
      │  │  │        │     │  ├─ type: Identifier
      │  │  │        │     │  └─ name: i
      │  │  │        │     └─ isPrefix: false
      │  │  │        └─ body
      │  │  │           ├─ type: Block
      │  │  │           └─ statements
      │  │  │              └─ 0
      │  │  │                 ├─ type: ExpressionStatement
      │  │  │                 └─ expression
      │  │  │                    ├─ type: FunctionCall
      │  │  │                    ├─ expression
      │  │  │                    │  ├─ type: Identifier
      │  │  │                    │  └─ name: refundContribution
      │  │  │                    ├─ arguments
      │  │  │                    │  ├─ 0
      │  │  │                    │  │  ├─ type: Identifier
      │  │  │                    │  │  └─ name: _sender
      │  │  │                    │  ├─ 1
      │  │  │                    │  │  ├─ type: Identifier
      │  │  │                    │  │  └─ name: _bountyId
      │  │  │                    │  └─ 2
      │  │  │                    │     ├─ type: IndexAccess
      │  │  │                    │     ├─ base
      │  │  │                    │     │  ├─ type: Identifier
      │  │  │                    │     │  └─ name: _contributionIds
      │  │  │                    │     └─ index
      │  │  │                    │        ├─ type: Identifier
      │  │  │                    │        └─ name: i
      │  │  │                    └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  └─ 0
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: senderIsValid
      │  │  │     └─ arguments
      │  │  │        └─ 0
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _sender
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 25
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: performAction
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: string
      │  │  │        ├─ name: _data
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     └─ 0
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: ActionPerformed
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _data
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  └─ 1
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: validateBountyArrayIndex
      │  │  │     └─ arguments
      │  │  │        └─ 0
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _bountyId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 26
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: fulfillBounty
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: string
      │  │  │        ├─ name: _data
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: <
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: now
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: MemberAccess
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: IndexAccess
      │  │  │     │     │        │  ├─ base
      │  │  │     │     │        │  │  ├─ type: Identifier
      │  │  │     │     │        │  │  └─ name: bounties
      │  │  │     │     │        │  └─ index
      │  │  │     │     │        │     ├─ type: Identifier
      │  │  │     │     │        │     └─ name: _bountyId
      │  │  │     │     │        └─ memberName: deadline
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: >
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _fulfillers
      │  │  │     │     │     │  └─ memberName: length
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: NumberLiteral
      │  │  │     │     │        ├─ number: 0
      │  │  │     │     │        └─ subdenomination
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: MemberAccess
      │  │  │     │     │  │  ├─ expression
      │  │  │     │     │  │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  │  ├─ base
      │  │  │     │     │  │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  │  └─ name: bounties
      │  │  │     │     │  │  │  └─ index
      │  │  │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │  │  │     └─ name: _bountyId
      │  │  │     │     │  │  └─ memberName: fulfillments
      │  │  │     │     │  └─ memberName: push
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: Fulfillment
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _fulfillers
      │  │  │     │     │     │  └─ 1
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _sender
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     └─ 3
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyFulfilled
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: TupleExpression
      │  │  │           │  │  ├─ components
      │  │  │           │  │  │  └─ 0
      │  │  │           │  │  │     ├─ type: BinaryOperation
      │  │  │           │  │  │     ├─ operator: -
      │  │  │           │  │  │     ├─ left
      │  │  │           │  │  │     │  ├─ type: MemberAccess
      │  │  │           │  │  │     │  ├─ expression
      │  │  │           │  │  │     │  │  ├─ type: MemberAccess
      │  │  │           │  │  │     │  │  ├─ expression
      │  │  │           │  │  │     │  │  │  ├─ type: IndexAccess
      │  │  │           │  │  │     │  │  │  ├─ base
      │  │  │           │  │  │     │  │  │  │  ├─ type: Identifier
      │  │  │           │  │  │     │  │  │  │  └─ name: bounties
      │  │  │           │  │  │     │  │  │  └─ index
      │  │  │           │  │  │     │  │  │     ├─ type: Identifier
      │  │  │           │  │  │     │  │  │     └─ name: _bountyId
      │  │  │           │  │  │     │  │  └─ memberName: fulfillments
      │  │  │           │  │  │     │  └─ memberName: length
      │  │  │           │  │  │     └─ right
      │  │  │           │  │  │        ├─ type: NumberLiteral
      │  │  │           │  │  │        ├─ number: 1
      │  │  │           │  │  │        └─ subdenomination
      │  │  │           │  │  └─ isArray: false
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillers
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _data
      │  │  │           │  └─ 4
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _sender
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  └─ 1
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: validateBountyArrayIndex
      │  │  │     └─ arguments
      │  │  │        └─ 0
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _bountyId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 27
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: updateFulfillment
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _fulfillmentId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: string
      │  │  │        ├─ name: _data
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: MemberAccess
      │  │  │     │     │  │  │  ├─ expression
      │  │  │     │     │  │  │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  │  │  ├─ base
      │  │  │     │     │  │  │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  │  │  └─ name: bounties
      │  │  │     │     │  │  │  │  └─ index
      │  │  │     │     │  │  │  │     ├─ type: Identifier
      │  │  │     │     │  │  │  │     └─ name: _bountyId
      │  │  │     │     │  │  │  └─ memberName: fulfillments
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: fulfillers
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _fulfillers
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: FulfillmentUpdated
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillmentId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillers
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _data
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateFulfillmentArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _fulfillmentId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlySubmitter
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _fulfillmentId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 28
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: acceptFulfillment
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _fulfillmentId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _approverId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: uint
      │  │  │        │  └─ length
      │  │  │        ├─ name: _tokenAmounts
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: hasPaidOut
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: BooleanLiteral
      │  │  │     │        └─ value: true
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: UserDefinedTypeName
      │  │  │     │  │     │  └─ namePath: Fulfillment
      │  │  │     │  │     ├─ name: fulfillment
      │  │  │     │  │     ├─ storageLocation: storage
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: IndexAccess
      │  │  │     │     ├─ base
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: fulfillments
      │  │  │     │     └─ index
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _fulfillmentId
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _tokenAmounts
      │  │  │     │     │     │  └─ memberName: length
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: MemberAccess
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: MemberAccess
      │  │  │     │     │        │  ├─ expression
      │  │  │     │     │        │  │  ├─ type: Identifier
      │  │  │     │     │        │  │  └─ name: fulfillment
      │  │  │     │     │        │  └─ memberName: fulfillers
      │  │  │     │     │        └─ memberName: length
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ForStatement
      │  │  │     │  ├─ initExpression
      │  │  │     │  │  ├─ type: VariableDeclarationStatement
      │  │  │     │  │  ├─ variables
      │  │  │     │  │  │  └─ 0
      │  │  │     │  │  │     ├─ type: VariableDeclaration
      │  │  │     │  │  │     ├─ typeName
      │  │  │     │  │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │     │  └─ name: uint256
      │  │  │     │  │  │     ├─ name: i
      │  │  │     │  │  │     ├─ storageLocation
      │  │  │     │  │  │     ├─ isStateVar: false
      │  │  │     │  │  │     └─ isIndexed: false
      │  │  │     │  │  └─ initialValue
      │  │  │     │  │     ├─ type: NumberLiteral
      │  │  │     │  │     ├─ number: 0
      │  │  │     │  │     └─ subdenomination
      │  │  │     │  ├─ conditionExpression
      │  │  │     │  │  ├─ type: BinaryOperation
      │  │  │     │  │  ├─ operator: <
      │  │  │     │  │  ├─ left
      │  │  │     │  │  │  ├─ type: Identifier
      │  │  │     │  │  │  └─ name: i
      │  │  │     │  │  └─ right
      │  │  │     │  │     ├─ type: MemberAccess
      │  │  │     │  │     ├─ expression
      │  │  │     │  │     │  ├─ type: MemberAccess
      │  │  │     │  │     │  ├─ expression
      │  │  │     │  │     │  │  ├─ type: Identifier
      │  │  │     │  │     │  │  └─ name: fulfillment
      │  │  │     │  │     │  └─ memberName: fulfillers
      │  │  │     │  │     └─ memberName: length
      │  │  │     │  ├─ loopExpression
      │  │  │     │  │  ├─ type: ExpressionStatement
      │  │  │     │  │  └─ expression
      │  │  │     │  │     ├─ type: UnaryOperation
      │  │  │     │  │     ├─ operator: ++
      │  │  │     │  │     ├─ subExpression
      │  │  │     │  │     │  ├─ type: Identifier
      │  │  │     │  │     │  └─ name: i
      │  │  │     │  │     └─ isPrefix: false
      │  │  │     │  └─ body
      │  │  │     │     ├─ type: Block
      │  │  │     │     └─ statements
      │  │  │     │        ├─ 0
      │  │  │     │        │  ├─ type: ExpressionStatement
      │  │  │     │        │  └─ expression
      │  │  │     │        │     ├─ type: FunctionCall
      │  │  │     │        │     ├─ expression
      │  │  │     │        │     │  ├─ type: Identifier
      │  │  │     │        │     │  └─ name: require
      │  │  │     │        │     ├─ arguments
      │  │  │     │        │     │  └─ 0
      │  │  │     │        │     │     ├─ type: BinaryOperation
      │  │  │     │        │     │     ├─ operator: >=
      │  │  │     │        │     │     ├─ left
      │  │  │     │        │     │     │  ├─ type: MemberAccess
      │  │  │     │        │     │     │  ├─ expression
      │  │  │     │        │     │     │  │  ├─ type: IndexAccess
      │  │  │     │        │     │     │  │  ├─ base
      │  │  │     │        │     │     │  │  │  ├─ type: Identifier
      │  │  │     │        │     │     │  │  │  └─ name: bounties
      │  │  │     │        │     │     │  │  └─ index
      │  │  │     │        │     │     │  │     ├─ type: Identifier
      │  │  │     │        │     │     │  │     └─ name: _bountyId
      │  │  │     │        │     │     │  └─ memberName: balance
      │  │  │     │        │     │     └─ right
      │  │  │     │        │     │        ├─ type: IndexAccess
      │  │  │     │        │     │        ├─ base
      │  │  │     │        │     │        │  ├─ type: Identifier
      │  │  │     │        │     │        │  └─ name: _tokenAmounts
      │  │  │     │        │     │        └─ index
      │  │  │     │        │     │           ├─ type: Identifier
      │  │  │     │        │     │           └─ name: i
      │  │  │     │        │     └─ names
      │  │  │     │        ├─ 1
      │  │  │     │        │  ├─ type: ExpressionStatement
      │  │  │     │        │  └─ expression
      │  │  │     │        │     ├─ type: BinaryOperation
      │  │  │     │        │     ├─ operator: -=
      │  │  │     │        │     ├─ left
      │  │  │     │        │     │  ├─ type: MemberAccess
      │  │  │     │        │     │  ├─ expression
      │  │  │     │        │     │  │  ├─ type: IndexAccess
      │  │  │     │        │     │  │  ├─ base
      │  │  │     │        │     │  │  │  ├─ type: Identifier
      │  │  │     │        │     │  │  │  └─ name: bounties
      │  │  │     │        │     │  │  └─ index
      │  │  │     │        │     │  │     ├─ type: Identifier
      │  │  │     │        │     │  │     └─ name: _bountyId
      │  │  │     │        │     │  └─ memberName: balance
      │  │  │     │        │     └─ right
      │  │  │     │        │        ├─ type: IndexAccess
      │  │  │     │        │        ├─ base
      │  │  │     │        │        │  ├─ type: Identifier
      │  │  │     │        │        │  └─ name: _tokenAmounts
      │  │  │     │        │        └─ index
      │  │  │     │        │           ├─ type: Identifier
      │  │  │     │        │           └─ name: i
      │  │  │     │        └─ 2
      │  │  │     │           ├─ type: IfStatement
      │  │  │     │           ├─ condition
      │  │  │     │           │  ├─ type: BinaryOperation
      │  │  │     │           │  ├─ operator: !=
      │  │  │     │           │  ├─ left
      │  │  │     │           │  │  ├─ type: IndexAccess
      │  │  │     │           │  │  ├─ base
      │  │  │     │           │  │  │  ├─ type: Identifier
      │  │  │     │           │  │  │  └─ name: _tokenAmounts
      │  │  │     │           │  │  └─ index
      │  │  │     │           │  │     ├─ type: Identifier
      │  │  │     │           │  │     └─ name: i
      │  │  │     │           │  └─ right
      │  │  │     │           │     ├─ type: NumberLiteral
      │  │  │     │           │     ├─ number: 0
      │  │  │     │           │     └─ subdenomination
      │  │  │     │           ├─ trueBody
      │  │  │     │           │  ├─ type: Block
      │  │  │     │           │  └─ statements
      │  │  │     │           │     └─ 0
      │  │  │     │           │        ├─ type: ExpressionStatement
      │  │  │     │           │        └─ expression
      │  │  │     │           │           ├─ type: FunctionCall
      │  │  │     │           │           ├─ expression
      │  │  │     │           │           │  ├─ type: Identifier
      │  │  │     │           │           │  └─ name: transferTokens
      │  │  │     │           │           ├─ arguments
      │  │  │     │           │           │  ├─ 0
      │  │  │     │           │           │  │  ├─ type: Identifier
      │  │  │     │           │           │  │  └─ name: _bountyId
      │  │  │     │           │           │  ├─ 1
      │  │  │     │           │           │  │  ├─ type: IndexAccess
      │  │  │     │           │           │  │  ├─ base
      │  │  │     │           │           │  │  │  ├─ type: MemberAccess
      │  │  │     │           │           │  │  │  ├─ expression
      │  │  │     │           │           │  │  │  │  ├─ type: Identifier
      │  │  │     │           │           │  │  │  │  └─ name: fulfillment
      │  │  │     │           │           │  │  │  └─ memberName: fulfillers
      │  │  │     │           │           │  │  └─ index
      │  │  │     │           │           │  │     ├─ type: Identifier
      │  │  │     │           │           │  │     └─ name: i
      │  │  │     │           │           │  └─ 2
      │  │  │     │           │           │     ├─ type: IndexAccess
      │  │  │     │           │           │     ├─ base
      │  │  │     │           │           │     │  ├─ type: Identifier
      │  │  │     │           │           │     │  └─ name: _tokenAmounts
      │  │  │     │           │           │     └─ index
      │  │  │     │           │           │        ├─ type: Identifier
      │  │  │     │           │           │        └─ name: i
      │  │  │     │           │           └─ names
      │  │  │     │           └─ falseBody
      │  │  │     └─ 4
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: FulfillmentAccepted
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillmentId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _tokenAmounts
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateFulfillmentArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _fulfillmentId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: isApprover
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _approverId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 29
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: fulfillAndAccept
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _approverId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 5
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: uint
      │  │  │        │  └─ length
      │  │  │        ├─ name: _tokenAmounts
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: fulfillBounty
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _sender
      │  │  │     │     │  ├─ 1
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _bountyId
      │  │  │     │     │  ├─ 2
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: _fulfillers
      │  │  │     │     │  └─ 3
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _data
      │  │  │     │     └─ names
      │  │  │     └─ 1
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: acceptFulfillment
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: BinaryOperation
      │  │  │           │  │  ├─ operator: -
      │  │  │           │  │  ├─ left
      │  │  │           │  │  │  ├─ type: MemberAccess
      │  │  │           │  │  │  ├─ expression
      │  │  │           │  │  │  │  ├─ type: MemberAccess
      │  │  │           │  │  │  │  ├─ expression
      │  │  │           │  │  │  │  │  ├─ type: IndexAccess
      │  │  │           │  │  │  │  │  ├─ base
      │  │  │           │  │  │  │  │  │  ├─ type: Identifier
      │  │  │           │  │  │  │  │  │  └─ name: bounties
      │  │  │           │  │  │  │  │  └─ index
      │  │  │           │  │  │  │  │     ├─ type: Identifier
      │  │  │           │  │  │  │  │     └─ name: _bountyId
      │  │  │           │  │  │  │  └─ memberName: fulfillments
      │  │  │           │  │  │  └─ memberName: length
      │  │  │           │  │  └─ right
      │  │  │           │  │     ├─ type: NumberLiteral
      │  │  │           │  │     ├─ number: 1
      │  │  │           │  │     └─ subdenomination
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approverId
      │  │  │           │  └─ 4
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _tokenAmounts
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  └─ 0
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: senderIsValid
      │  │  │     └─ arguments
      │  │  │        └─ 0
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _sender
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 30
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: changeBounty
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 5
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 6
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _deadline
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: issuers
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _issuers
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: approvers
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _approvers
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: deadline
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _deadline
      │  │  │     └─ 3
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyChanged
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuers
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approvers
      │  │  │           │  ├─ 4
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _data
      │  │  │           │  └─ 5
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _deadline
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 31
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: changeIssuer
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerIdToChange
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  ├─ name: address
      │  │  │        │  └─ stateMutability: payable
      │  │  │        ├─ name: _newIssuer
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: MemberAccess
      │  │  │     │     │  │  ├─ expression
      │  │  │     │     │  │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  │  ├─ base
      │  │  │     │     │  │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  │  └─ name: bounties
      │  │  │     │     │  │  │  └─ index
      │  │  │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │  │  │     └─ name: _bountyId
      │  │  │     │     │  │  └─ memberName: issuers
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _issuerIdToChange
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _newIssuer
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyIssuerChanged
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _newIssuer
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  ├─ 3
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerIdToChange
      │  │  │  └─ 4
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 32
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: changeApprover
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _approverId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  ├─ name: address
      │  │  │        │  └─ stateMutability: payable
      │  │  │        ├─ name: _approver
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: MemberAccess
      │  │  │     │     │  │  ├─ expression
      │  │  │     │     │  │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  │  ├─ base
      │  │  │     │     │  │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  │  └─ name: bounties
      │  │  │     │     │  │  │  └─ index
      │  │  │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │  │  │     └─ name: _bountyId
      │  │  │     │     │  │  └─ memberName: approvers
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _approverId
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _approver
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyApproverChanged
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: MemberAccess
      │  │  │           │  │  ├─ expression
      │  │  │           │  │  │  ├─ type: Identifier
      │  │  │           │  │  │  └─ name: msg
      │  │  │           │  │  └─ memberName: sender
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approverId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _approver
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  ├─ 3
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: onlyIssuer
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _sender
      │  │  │  │     ├─ 1
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 2
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 4
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: validateApproverArrayIndex
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 1
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _approverId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 33
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: changeData
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: string
      │  │  │        ├─ name: _data
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     └─ 0
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyDataChanged
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: MemberAccess
      │  │  │           │  │  ├─ expression
      │  │  │           │  │  │  ├─ type: Identifier
      │  │  │           │  │  │  └─ name: msg
      │  │  │           │  │  └─ memberName: sender
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _data
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 34
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: changeDeadline
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _deadline
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: deadline
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _deadline
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyDeadlineChanged
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _deadline
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 35
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: addIssuers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  ├─ name: address
      │  │  │        │  │  └─ stateMutability: payable
      │  │  │        │  └─ length
      │  │  │        ├─ name: _issuers
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ForStatement
      │  │  │     │  ├─ initExpression
      │  │  │     │  │  ├─ type: VariableDeclarationStatement
      │  │  │     │  │  ├─ variables
      │  │  │     │  │  │  └─ 0
      │  │  │     │  │  │     ├─ type: VariableDeclaration
      │  │  │     │  │  │     ├─ typeName
      │  │  │     │  │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │     │  └─ name: uint
      │  │  │     │  │  │     ├─ name: i
      │  │  │     │  │  │     ├─ storageLocation
      │  │  │     │  │  │     ├─ isStateVar: false
      │  │  │     │  │  │     └─ isIndexed: false
      │  │  │     │  │  └─ initialValue
      │  │  │     │  │     ├─ type: NumberLiteral
      │  │  │     │  │     ├─ number: 0
      │  │  │     │  │     └─ subdenomination
      │  │  │     │  ├─ conditionExpression
      │  │  │     │  │  ├─ type: BinaryOperation
      │  │  │     │  │  ├─ operator: <
      │  │  │     │  │  ├─ left
      │  │  │     │  │  │  ├─ type: Identifier
      │  │  │     │  │  │  └─ name: i
      │  │  │     │  │  └─ right
      │  │  │     │  │     ├─ type: MemberAccess
      │  │  │     │  │     ├─ expression
      │  │  │     │  │     │  ├─ type: Identifier
      │  │  │     │  │     │  └─ name: _issuers
      │  │  │     │  │     └─ memberName: length
      │  │  │     │  ├─ loopExpression
      │  │  │     │  │  ├─ type: ExpressionStatement
      │  │  │     │  │  └─ expression
      │  │  │     │  │     ├─ type: UnaryOperation
      │  │  │     │  │     ├─ operator: ++
      │  │  │     │  │     ├─ subExpression
      │  │  │     │  │     │  ├─ type: Identifier
      │  │  │     │  │     │  └─ name: i
      │  │  │     │  │     └─ isPrefix: false
      │  │  │     │  └─ body
      │  │  │     │     ├─ type: Block
      │  │  │     │     └─ statements
      │  │  │     │        └─ 0
      │  │  │     │           ├─ type: ExpressionStatement
      │  │  │     │           └─ expression
      │  │  │     │              ├─ type: FunctionCall
      │  │  │     │              ├─ expression
      │  │  │     │              │  ├─ type: MemberAccess
      │  │  │     │              │  ├─ expression
      │  │  │     │              │  │  ├─ type: MemberAccess
      │  │  │     │              │  │  ├─ expression
      │  │  │     │              │  │  │  ├─ type: IndexAccess
      │  │  │     │              │  │  │  ├─ base
      │  │  │     │              │  │  │  │  ├─ type: Identifier
      │  │  │     │              │  │  │  │  └─ name: bounties
      │  │  │     │              │  │  │  └─ index
      │  │  │     │              │  │  │     ├─ type: Identifier
      │  │  │     │              │  │  │     └─ name: _bountyId
      │  │  │     │              │  │  └─ memberName: issuers
      │  │  │     │              │  └─ memberName: push
      │  │  │     │              ├─ arguments
      │  │  │     │              │  └─ 0
      │  │  │     │              │     ├─ type: IndexAccess
      │  │  │     │              │     ├─ base
      │  │  │     │              │     │  ├─ type: Identifier
      │  │  │     │              │     │  └─ name: _issuers
      │  │  │     │              │     └─ index
      │  │  │     │              │        ├─ type: Identifier
      │  │  │     │              │        └─ name: i
      │  │  │     │              └─ names
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyIssuersAdded
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _issuers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 36
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: replaceIssuers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  ├─ name: address
      │  │  │        │  │  └─ stateMutability: payable
      │  │  │        │  └─ length
      │  │  │        ├─ name: _issuers
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: issuers
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _issuers
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyIssuersReplaced
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _issuers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 37
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: addApprovers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: address
      │  │  │        │  └─ length
      │  │  │        ├─ name: _approvers
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ForStatement
      │  │  │     │  ├─ initExpression
      │  │  │     │  │  ├─ type: VariableDeclarationStatement
      │  │  │     │  │  ├─ variables
      │  │  │     │  │  │  └─ 0
      │  │  │     │  │  │     ├─ type: VariableDeclaration
      │  │  │     │  │  │     ├─ typeName
      │  │  │     │  │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │     │  └─ name: uint
      │  │  │     │  │  │     ├─ name: i
      │  │  │     │  │  │     ├─ storageLocation
      │  │  │     │  │  │     ├─ isStateVar: false
      │  │  │     │  │  │     └─ isIndexed: false
      │  │  │     │  │  └─ initialValue
      │  │  │     │  │     ├─ type: NumberLiteral
      │  │  │     │  │     ├─ number: 0
      │  │  │     │  │     └─ subdenomination
      │  │  │     │  ├─ conditionExpression
      │  │  │     │  │  ├─ type: BinaryOperation
      │  │  │     │  │  ├─ operator: <
      │  │  │     │  │  ├─ left
      │  │  │     │  │  │  ├─ type: Identifier
      │  │  │     │  │  │  └─ name: i
      │  │  │     │  │  └─ right
      │  │  │     │  │     ├─ type: MemberAccess
      │  │  │     │  │     ├─ expression
      │  │  │     │  │     │  ├─ type: Identifier
      │  │  │     │  │     │  └─ name: _approvers
      │  │  │     │  │     └─ memberName: length
      │  │  │     │  ├─ loopExpression
      │  │  │     │  │  ├─ type: ExpressionStatement
      │  │  │     │  │  └─ expression
      │  │  │     │  │     ├─ type: UnaryOperation
      │  │  │     │  │     ├─ operator: ++
      │  │  │     │  │     ├─ subExpression
      │  │  │     │  │     │  ├─ type: Identifier
      │  │  │     │  │     │  └─ name: i
      │  │  │     │  │     └─ isPrefix: false
      │  │  │     │  └─ body
      │  │  │     │     ├─ type: Block
      │  │  │     │     └─ statements
      │  │  │     │        └─ 0
      │  │  │     │           ├─ type: ExpressionStatement
      │  │  │     │           └─ expression
      │  │  │     │              ├─ type: FunctionCall
      │  │  │     │              ├─ expression
      │  │  │     │              │  ├─ type: MemberAccess
      │  │  │     │              │  ├─ expression
      │  │  │     │              │  │  ├─ type: MemberAccess
      │  │  │     │              │  │  ├─ expression
      │  │  │     │              │  │  │  ├─ type: IndexAccess
      │  │  │     │              │  │  │  ├─ base
      │  │  │     │              │  │  │  │  ├─ type: Identifier
      │  │  │     │              │  │  │  │  └─ name: bounties
      │  │  │     │              │  │  │  └─ index
      │  │  │     │              │  │  │     ├─ type: Identifier
      │  │  │     │              │  │  │     └─ name: _bountyId
      │  │  │     │              │  │  └─ memberName: approvers
      │  │  │     │              │  └─ memberName: push
      │  │  │     │              ├─ arguments
      │  │  │     │              │  └─ 0
      │  │  │     │              │     ├─ type: IndexAccess
      │  │  │     │              │     ├─ base
      │  │  │     │              │     │  ├─ type: Identifier
      │  │  │     │              │     │  └─ name: _approvers
      │  │  │     │              │     └─ index
      │  │  │     │              │        ├─ type: Identifier
      │  │  │     │              │        └─ name: i
      │  │  │     │              └─ names
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyApproversAdded
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _approvers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 38
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: replaceApprovers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _sender
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: address
      │  │  │        │  └─ length
      │  │  │        ├─ name: _approvers
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: BinaryOperation
      │  │  │     │     ├─ operator: =
      │  │  │     │     ├─ left
      │  │  │     │     │  ├─ type: MemberAccess
      │  │  │     │     │  ├─ expression
      │  │  │     │     │  │  ├─ type: IndexAccess
      │  │  │     │     │  │  ├─ base
      │  │  │     │     │  │  │  ├─ type: Identifier
      │  │  │     │     │  │  │  └─ name: bounties
      │  │  │     │     │  │  └─ index
      │  │  │     │     │  │     ├─ type: Identifier
      │  │  │     │     │  │     └─ name: _bountyId
      │  │  │     │     │  └─ memberName: approvers
      │  │  │     │     └─ right
      │  │  │     │        ├─ type: Identifier
      │  │  │     │        └─ name: _approvers
      │  │  │     └─ 1
      │  │  │        ├─ type: EmitStatement
      │  │  │        └─ eventCall
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: BountyApproversReplaced
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _sender
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _approvers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  │  ├─ 0
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: senderIsValid
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _sender
      │  │  │  ├─ 1
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateBountyArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     └─ 0
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _bountyId
      │  │  │  ├─ 2
      │  │  │  │  ├─ type: ModifierInvocation
      │  │  │  │  ├─ name: validateIssuerArrayIndex
      │  │  │  │  └─ arguments
      │  │  │  │     ├─ 0
      │  │  │  │     │  ├─ type: Identifier
      │  │  │  │     │  └─ name: _bountyId
      │  │  │  │     └─ 1
      │  │  │  │        ├─ type: Identifier
      │  │  │  │        └─ name: _issuerId
      │  │  │  └─ 3
      │  │  │     ├─ type: ModifierInvocation
      │  │  │     ├─ name: onlyIssuer
      │  │  │     └─ arguments
      │  │  │        ├─ 0
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _sender
      │  │  │        ├─ 1
      │  │  │        │  ├─ type: Identifier
      │  │  │        │  └─ name: _bountyId
      │  │  │        └─ 2
      │  │  │           ├─ type: Identifier
      │  │  │           └─ name: _issuerId
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 39
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: getBounty
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _bountyId
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: UserDefinedTypeName
      │  │  │        │  └─ namePath: Bounty
      │  │  │        ├─ name
      │  │  │        ├─ storageLocation: memory
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     └─ 0
      │  │  │        ├─ type: ReturnStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: IndexAccess
      │  │  │           ├─ base
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: bounties
      │  │  │           └─ index
      │  │  │              ├─ type: Identifier
      │  │  │              └─ name: _bountyId
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability: view
      │  ├─ 40
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: transferTokens
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _to
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _amount
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     └─ 0
      │  │  │        ├─ type: IfStatement
      │  │  │        ├─ condition
      │  │  │        │  ├─ type: BinaryOperation
      │  │  │        │  ├─ operator: ==
      │  │  │        │  ├─ left
      │  │  │        │  │  ├─ type: MemberAccess
      │  │  │        │  │  ├─ expression
      │  │  │        │  │  │  ├─ type: IndexAccess
      │  │  │        │  │  │  ├─ base
      │  │  │        │  │  │  │  ├─ type: Identifier
      │  │  │        │  │  │  │  └─ name: bounties
      │  │  │        │  │  │  └─ index
      │  │  │        │  │  │     ├─ type: Identifier
      │  │  │        │  │  │     └─ name: _bountyId
      │  │  │        │  │  └─ memberName: tokenVersion
      │  │  │        │  └─ right
      │  │  │        │     ├─ type: NumberLiteral
      │  │  │        │     ├─ number: 0
      │  │  │        │     └─ subdenomination
      │  │  │        ├─ trueBody
      │  │  │        │  ├─ type: Block
      │  │  │        │  └─ statements
      │  │  │        │     └─ 0
      │  │  │        │        ├─ type: ExpressionStatement
      │  │  │        │        └─ expression
      │  │  │        │           ├─ type: FunctionCall
      │  │  │        │           ├─ expression
      │  │  │        │           │  ├─ type: MemberAccess
      │  │  │        │           │  ├─ expression
      │  │  │        │           │  │  ├─ type: Identifier
      │  │  │        │           │  │  └─ name: _to
      │  │  │        │           │  └─ memberName: transfer
      │  │  │        │           ├─ arguments
      │  │  │        │           │  └─ 0
      │  │  │        │           │     ├─ type: Identifier
      │  │  │        │           │     └─ name: _amount
      │  │  │        │           └─ names
      │  │  │        └─ falseBody
      │  │  │           ├─ type: IfStatement
      │  │  │           ├─ condition
      │  │  │           │  ├─ type: BinaryOperation
      │  │  │           │  ├─ operator: ==
      │  │  │           │  ├─ left
      │  │  │           │  │  ├─ type: MemberAccess
      │  │  │           │  │  ├─ expression
      │  │  │           │  │  │  ├─ type: IndexAccess
      │  │  │           │  │  │  ├─ base
      │  │  │           │  │  │  │  ├─ type: Identifier
      │  │  │           │  │  │  │  └─ name: bounties
      │  │  │           │  │  │  └─ index
      │  │  │           │  │  │     ├─ type: Identifier
      │  │  │           │  │  │     └─ name: _bountyId
      │  │  │           │  │  └─ memberName: tokenVersion
      │  │  │           │  └─ right
      │  │  │           │     ├─ type: NumberLiteral
      │  │  │           │     ├─ number: 20
      │  │  │           │     └─ subdenomination
      │  │  │           ├─ trueBody
      │  │  │           │  ├─ type: Block
      │  │  │           │  └─ statements
      │  │  │           │     └─ 0
      │  │  │           │        ├─ type: ExpressionStatement
      │  │  │           │        └─ expression
      │  │  │           │           ├─ type: FunctionCall
      │  │  │           │           ├─ expression
      │  │  │           │           │  ├─ type: Identifier
      │  │  │           │           │  └─ name: require
      │  │  │           │           ├─ arguments
      │  │  │           │           │  └─ 0
      │  │  │           │           │     ├─ type: FunctionCall
      │  │  │           │           │     ├─ expression
      │  │  │           │           │     │  ├─ type: MemberAccess
      │  │  │           │           │     │  ├─ expression
      │  │  │           │           │     │  │  ├─ type: FunctionCall
      │  │  │           │           │     │  │  ├─ expression
      │  │  │           │           │     │  │  │  ├─ type: Identifier
      │  │  │           │           │     │  │  │  └─ name: ERC20Token
      │  │  │           │           │     │  │  ├─ arguments
      │  │  │           │           │     │  │  │  └─ 0
      │  │  │           │           │     │  │  │     ├─ type: MemberAccess
      │  │  │           │           │     │  │  │     ├─ expression
      │  │  │           │           │     │  │  │     │  ├─ type: IndexAccess
      │  │  │           │           │     │  │  │     │  ├─ base
      │  │  │           │           │     │  │  │     │  │  ├─ type: Identifier
      │  │  │           │           │     │  │  │     │  │  └─ name: bounties
      │  │  │           │           │     │  │  │     │  └─ index
      │  │  │           │           │     │  │  │     │     ├─ type: Identifier
      │  │  │           │           │     │  │  │     │     └─ name: _bountyId
      │  │  │           │           │     │  │  │     └─ memberName: token
      │  │  │           │           │     │  │  └─ names
      │  │  │           │           │     │  └─ memberName: transfer
      │  │  │           │           │     ├─ arguments
      │  │  │           │           │     │  ├─ 0
      │  │  │           │           │     │  │  ├─ type: Identifier
      │  │  │           │           │     │  │  └─ name: _to
      │  │  │           │           │     │  └─ 1
      │  │  │           │           │     │     ├─ type: Identifier
      │  │  │           │           │     │     └─ name: _amount
      │  │  │           │           │     └─ names
      │  │  │           │           └─ names
      │  │  │           └─ falseBody
      │  │  │              ├─ type: IfStatement
      │  │  │              ├─ condition
      │  │  │              │  ├─ type: BinaryOperation
      │  │  │              │  ├─ operator: ==
      │  │  │              │  ├─ left
      │  │  │              │  │  ├─ type: MemberAccess
      │  │  │              │  │  ├─ expression
      │  │  │              │  │  │  ├─ type: IndexAccess
      │  │  │              │  │  │  ├─ base
      │  │  │              │  │  │  │  ├─ type: Identifier
      │  │  │              │  │  │  │  └─ name: bounties
      │  │  │              │  │  │  └─ index
      │  │  │              │  │  │     ├─ type: Identifier
      │  │  │              │  │  │     └─ name: _bountyId
      │  │  │              │  │  └─ memberName: tokenVersion
      │  │  │              │  └─ right
      │  │  │              │     ├─ type: NumberLiteral
      │  │  │              │     ├─ number: 721
      │  │  │              │     └─ subdenomination
      │  │  │              ├─ trueBody
      │  │  │              │  ├─ type: Block
      │  │  │              │  └─ statements
      │  │  │              │     └─ 0
      │  │  │              │        ├─ type: ExpressionStatement
      │  │  │              │        └─ expression
      │  │  │              │           ├─ type: FunctionCall
      │  │  │              │           ├─ expression
      │  │  │              │           │  ├─ type: MemberAccess
      │  │  │              │           │  ├─ expression
      │  │  │              │           │  │  ├─ type: FunctionCall
      │  │  │              │           │  │  ├─ expression
      │  │  │              │           │  │  │  ├─ type: Identifier
      │  │  │              │           │  │  │  └─ name: ERC721BasicToken
      │  │  │              │           │  │  ├─ arguments
      │  │  │              │           │  │  │  └─ 0
      │  │  │              │           │  │  │     ├─ type: MemberAccess
      │  │  │              │           │  │  │     ├─ expression
      │  │  │              │           │  │  │     │  ├─ type: IndexAccess
      │  │  │              │           │  │  │     │  ├─ base
      │  │  │              │           │  │  │     │  │  ├─ type: Identifier
      │  │  │              │           │  │  │     │  │  └─ name: bounties
      │  │  │              │           │  │  │     │  └─ index
      │  │  │              │           │  │  │     │     ├─ type: Identifier
      │  │  │              │           │  │  │     │     └─ name: _bountyId
      │  │  │              │           │  │  │     └─ memberName: token
      │  │  │              │           │  │  └─ names
      │  │  │              │           │  └─ memberName: safeTransferFrom
      │  │  │              │           ├─ arguments
      │  │  │              │           │  ├─ 0
      │  │  │              │           │  │  ├─ type: FunctionCall
      │  │  │              │           │  │  ├─ expression
      │  │  │              │           │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │              │           │  │  │  └─ typeName
      │  │  │              │           │  │  │     ├─ type: ElementaryTypeName
      │  │  │              │           │  │  │     └─ name: address
      │  │  │              │           │  │  ├─ arguments
      │  │  │              │           │  │  │  └─ 0
      │  │  │              │           │  │  │     ├─ type: Identifier
      │  │  │              │           │  │  │     └─ name: this
      │  │  │              │           │  │  └─ names
      │  │  │              │           │  ├─ 1
      │  │  │              │           │  │  ├─ type: Identifier
      │  │  │              │           │  │  └─ name: _to
      │  │  │              │           │  └─ 2
      │  │  │              │           │     ├─ type: Identifier
      │  │  │              │           │     └─ name: _amount
      │  │  │              │           └─ names
      │  │  │              └─ falseBody
      │  │  │                 ├─ type: Block
      │  │  │                 └─ statements
      │  │  │                    └─ 0
      │  │  │                       ├─ type: ExpressionStatement
      │  │  │                       └─ expression
      │  │  │                          ├─ type: FunctionCall
      │  │  │                          ├─ expression
      │  │  │                          │  ├─ type: Identifier
      │  │  │                          │  └─ name: revert
      │  │  │                          ├─ arguments
      │  │  │                          └─ names
      │  │  ├─ visibility: internal
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 41
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyIssued
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _creator
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  └─ name: address
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 5
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _deadline
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 6
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _token
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 7
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _tokenVersion
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 42
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: ContributionAdded
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _contributionId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _contributor
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _amount
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 43
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: ContributionRefunded
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 1
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _contributionId
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 44
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: ActionPerformed
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _fulfiller
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: string
      │  │  │        ├─ name: _data
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 45
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyFulfilled
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _fulfillmentId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: address
      │  │  │        ├─ name: _submitter
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 46
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: FulfillmentUpdated
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _fulfillmentId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: string
      │  │  │        ├─ name: _data
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 47
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: FulfillmentAccepted
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _fulfillmentId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _approver
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: uint
      │  │  │        │  └─ length
      │  │  │        ├─ name: _tokenAmounts
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 48
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyChanged
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 5
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _deadline
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 49
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyIssuerChanged
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  ├─ name: address
      │  │  │        │  └─ stateMutability: payable
      │  │  │        ├─ name: _issuer
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 50
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyIssuersAdded
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  ├─ name: address
      │  │  │        │  │  └─ stateMutability: payable
      │  │  │        │  └─ length
      │  │  │        ├─ name: _issuers
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 51
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyIssuersReplaced
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  ├─ name: address
      │  │  │        │  │  └─ stateMutability: payable
      │  │  │        │  └─ length
      │  │  │        ├─ name: _issuers
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 52
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyApproverChanged
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _approverId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  ├─ name: address
      │  │  │        │  └─ stateMutability: payable
      │  │  │        ├─ name: _approver
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 53
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyApproversAdded
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: address
      │  │  │        │  └─ length
      │  │  │        ├─ name: _approvers
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 54
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyApproversReplaced
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ArrayTypeName
      │  │  │        │  ├─ baseTypeName
      │  │  │        │  │  ├─ type: ElementaryTypeName
      │  │  │        │  │  └─ name: address
      │  │  │        │  └─ length
      │  │  │        ├─ name: _approvers
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  ├─ 55
      │  │  ├─ type: EventDefinition
      │  │  ├─ name: BountyDataChanged
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclaration
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _changer
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 2
      │  │  │        ├─ type: VariableDeclaration
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: string
      │  │  │        ├─ name: _data
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  └─ isAnonymous: false
      │  └─ 56
      │     ├─ type: EventDefinition
      │     ├─ name: BountyDeadlineChanged
      │     ├─ parameters
      │     │  ├─ type: ParameterList
      │     │  └─ parameters
      │     │     ├─ 0
      │     │     │  ├─ type: VariableDeclaration
      │     │     │  ├─ typeName
      │     │     │  │  ├─ type: ElementaryTypeName
      │     │     │  │  └─ name: uint
      │     │     │  ├─ name: _bountyId
      │     │     │  ├─ isStateVar: false
      │     │     │  └─ isIndexed: false
      │     │     ├─ 1
      │     │     │  ├─ type: VariableDeclaration
      │     │     │  ├─ typeName
      │     │     │  │  ├─ type: ElementaryTypeName
      │     │     │  │  └─ name: address
      │     │     │  ├─ name: _changer
      │     │     │  ├─ isStateVar: false
      │     │     │  └─ isIndexed: false
      │     │     └─ 2
      │     │        ├─ type: VariableDeclaration
      │     │        ├─ typeName
      │     │        │  ├─ type: ElementaryTypeName
      │     │        │  └─ name: uint
      │     │        ├─ name: _deadline
      │     │        ├─ isStateVar: false
      │     │        └─ isIndexed: false
      │     └─ isAnonymous: false
      └─ kind: contract

```

```console
$ surya parse BountiesMetaTxRelayer.sol
├─ type: SourceUnit
└─ children
   ├─ 0
   │  ├─ type: PragmaDirective
   │  ├─ name: solidity
   │  └─ value: ^0.5.0
   ├─ 1
   │  ├─ type: PragmaDirective
   │  ├─ name: experimental
   │  └─ value: ABIEncoderV2
   ├─ 2
   │  ├─ type: ImportDirective
   │  ├─ path: ./StandardBounties.sol
   │  ├─ unitAlias
   │  └─ symbolAliases
   └─ 3
      ├─ type: ContractDefinition
      ├─ name: BountiesMetaTxRelayer
      ├─ baseContracts
      ├─ subNodes
      │  ├─ 0
      │  │  ├─ type: StateVariableDeclaration
      │  │  ├─ variables
      │  │  │  └─ 0
      │  │  │     ├─ type: VariableDeclaration
      │  │  │     ├─ typeName
      │  │  │     │  ├─ type: UserDefinedTypeName
      │  │  │     │  └─ namePath: StandardBounties
      │  │  │     ├─ name: bountiesContract
      │  │  │     ├─ expression
      │  │  │     ├─ visibility: default
      │  │  │     ├─ isStateVar: true
      │  │  │     ├─ isDeclaredConst: false
      │  │  │     └─ isIndexed: false
      │  │  └─ initialValue
      │  ├─ 1
      │  │  ├─ type: StateVariableDeclaration
      │  │  ├─ variables
      │  │  │  └─ 0
      │  │  │     ├─ type: VariableDeclaration
      │  │  │     ├─ typeName
      │  │  │     │  ├─ type: Mapping
      │  │  │     │  ├─ keyType
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  └─ valueType
      │  │  │     │     ├─ type: ElementaryTypeName
      │  │  │     │     └─ name: uint
      │  │  │     ├─ name: replayNonce
      │  │  │     ├─ expression
      │  │  │     ├─ visibility: public
      │  │  │     ├─ isStateVar: true
      │  │  │     ├─ isDeclaredConst: false
      │  │  │     └─ isIndexed: false
      │  │  └─ initialValue
      │  ├─ 2
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: address
      │  │  │        ├─ name: _contract
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     └─ 0
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: BinaryOperation
      │  │  │           ├─ operator: =
      │  │  │           ├─ left
      │  │  │           │  ├─ type: Identifier
      │  │  │           │  └─ name: bountiesContract
      │  │  │           └─ right
      │  │  │              ├─ type: FunctionCall
      │  │  │              ├─ expression
      │  │  │              │  ├─ type: Identifier
      │  │  │              │  └─ name: StandardBounties
      │  │  │              ├─ arguments
      │  │  │              │  └─ 0
      │  │  │              │     ├─ type: Identifier
      │  │  │              │     └─ name: _contract
      │  │  │              └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: true
      │  │  └─ stateMutability
      │  ├─ 3
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaIssueBounty
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  └─ name: address
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _deadline
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 5
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: address
      │  │  │     │  ├─ name: _token
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 6
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _tokenVersion
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 7
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _depositAmount
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 8
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     └─ 0
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaIssueBounty
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuers
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approvers
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _data
      │  │  │     │     │     │  ├─ 5
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _deadline
      │  │  │     │     │     │  ├─ 6
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _token
      │  │  │     │     │     │  ├─ 7
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _tokenVersion
      │  │  │     │     │     │  ├─ 8
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _depositAmount
      │  │  │     │     │     │  └─ 9
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ReturnStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: issueBounty
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: FunctionCall
      │  │  │           │  │  ├─ expression
      │  │  │           │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │           │  │  │  └─ typeName
      │  │  │           │  │  │     ├─ type: ElementaryTypeName
      │  │  │           │  │  │     └─ name: address
      │  │  │           │  │  ├─ arguments
      │  │  │           │  │  │  └─ 0
      │  │  │           │  │  │     ├─ type: FunctionCall
      │  │  │           │  │  │     ├─ expression
      │  │  │           │  │  │     │  ├─ type: ElementaryTypeNameExpression
      │  │  │           │  │  │     │  └─ typeName
      │  │  │           │  │  │     │     ├─ type: ElementaryTypeName
      │  │  │           │  │  │     │     └─ name: uint160
      │  │  │           │  │  │     ├─ arguments
      │  │  │           │  │  │     │  └─ 0
      │  │  │           │  │  │     │     ├─ type: Identifier
      │  │  │           │  │  │     │     └─ name: signer
      │  │  │           │  │  │     └─ names
      │  │  │           │  │  └─ names
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuers
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approvers
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _data
      │  │  │           │  ├─ 4
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _deadline
      │  │  │           │  ├─ 5
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _token
      │  │  │           │  ├─ 6
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _tokenVersion
      │  │  │           │  └─ 7
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _depositAmount
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability: payable
      │  ├─ 4
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaContribute
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _amount
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaContribute
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _amount
      │  │  │     │     │     │  └─ 4
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: contribute
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: FunctionCall
      │  │  │           │  │  ├─ expression
      │  │  │           │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │           │  │  │  └─ typeName
      │  │  │           │  │  │     ├─ type: ElementaryTypeName
      │  │  │           │  │  │     └─ name: address
      │  │  │           │  │  ├─ arguments
      │  │  │           │  │  │  └─ 0
      │  │  │           │  │  │     ├─ type: FunctionCall
      │  │  │           │  │  │     ├─ expression
      │  │  │           │  │  │     │  ├─ type: ElementaryTypeNameExpression
      │  │  │           │  │  │     │  └─ typeName
      │  │  │           │  │  │     │     ├─ type: ElementaryTypeName
      │  │  │           │  │  │     │     └─ name: uint160
      │  │  │           │  │  │     ├─ arguments
      │  │  │           │  │  │     │  └─ 0
      │  │  │           │  │  │     │     ├─ type: Identifier
      │  │  │           │  │  │     │     └─ name: signer
      │  │  │           │  │  │     └─ names
      │  │  │           │  │  └─ names
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _amount
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability: payable
      │  ├─ 5
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaRefundContribution
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _contributionId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaRefundContribution
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _contributionId
      │  │  │     │     │     │  └─ 4
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: refundContribution
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _contributionId
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 6
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaRefundContributions
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  └─ name: uint
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _contributionIds
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaRefundContributions
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _contributionIds
      │  │  │     │     │     │  └─ 4
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: refundContributions
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _contributionIds
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 7
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaPerformAction
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 3
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaPerformAction
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _data
      │  │  │     │     │     │  └─ 4
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: performAction
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  └─ 2
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _data
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 8
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaFulfillBounty
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaFulfillBounty
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _fulfillers
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _data
      │  │  │     │     │     │  └─ 5
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: fulfillBounty
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillers
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _data
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 9
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaUpdateFulfillment
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _fulfillmentId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 5
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaUpdateFulfillment
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _fulfillmentId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _fulfillers
      │  │  │     │     │     │  ├─ 5
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _data
      │  │  │     │     │     │  └─ 6
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: updateFulfillment
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillmentId
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillers
      │  │  │           │  └─ 4
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _data
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 10
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaAcceptFulfillment
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _fulfillmentId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _approverId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  └─ name: uint
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _tokenAmounts
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 5
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaAcceptFulfillment
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _fulfillmentId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approverId
      │  │  │     │     │     │  ├─ 5
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _tokenAmounts
      │  │  │     │     │     │  └─ 6
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: acceptFulfillment
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillmentId
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approverId
      │  │  │           │  └─ 4
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _tokenAmounts
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 11
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaFulfillAndAccept
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _fulfillers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _approverId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 5
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  └─ name: uint
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _tokenAmounts
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 6
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaFulfillAndAccept
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _fulfillers
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _data
      │  │  │     │     │     │  ├─ 5
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approverId
      │  │  │     │     │     │  ├─ 6
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _tokenAmounts
      │  │  │     │     │     │  └─ 7
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: fulfillAndAccept
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _fulfillers
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _data
      │  │  │           │  ├─ 4
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approverId
      │  │  │           │  └─ 5
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _tokenAmounts
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 12
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaChangeBounty
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 5
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 6
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _deadline
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 7
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaChangeBounty
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuers
      │  │  │     │     │     │  ├─ 5
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approvers
      │  │  │     │     │     │  ├─ 6
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _data
      │  │  │     │     │     │  ├─ 7
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _deadline
      │  │  │     │     │     │  └─ 8
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: changeBounty
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuers
      │  │  │           │  ├─ 4
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approvers
      │  │  │           │  ├─ 5
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _data
      │  │  │           │  └─ 6
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _deadline
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 13
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaChangeIssuer
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerIdToChange
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _newIssuer
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 5
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaChangeIssuer
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerIdToChange
      │  │  │     │     │     │  ├─ 5
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _newIssuer
      │  │  │     │     │     │  └─ 6
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: changeIssuer
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerIdToChange
      │  │  │           │  └─ 4
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _newIssuer
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 14
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaChangeApprover
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _approverId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  ├─ name: address
      │  │  │     │  │  └─ stateMutability: payable
      │  │  │     │  ├─ name: _approver
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 5
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaChangeApprover
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approverId
      │  │  │     │     │     │  ├─ 5
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approver
      │  │  │     │     │     │  └─ 6
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: changeApprover
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  ├─ 3
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _approverId
      │  │  │           │  └─ 4
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _approver
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 15
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaChangeData
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: string
      │  │  │     │  ├─ name: _data
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaChangeData
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _data
      │  │  │     │     │     │  └─ 5
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: changeData
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _data
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 16
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaChangeDeadline
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _deadline
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaChangeDeadline
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _deadline
      │  │  │     │     │     │  └─ 5
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: changeDeadline
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _deadline
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 17
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaAddIssuers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaAddIssuers
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuers
      │  │  │     │     │     │  └─ 5
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: addIssuers
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _issuers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 18
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaReplaceIssuers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _issuers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaReplaceIssuers
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuers
      │  │  │     │     │     │  └─ 5
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: replaceIssuers
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _issuers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 19
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaAddApprovers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaAddApprovers
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approvers
      │  │  │     │     │     │  └─ 5
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: addIssuers
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _approvers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  ├─ 20
      │  │  ├─ type: FunctionDefinition
      │  │  ├─ name: metaReplaceApprovers
      │  │  ├─ parameters
      │  │  │  ├─ type: ParameterList
      │  │  │  └─ parameters
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: bytes
      │  │  │     │  ├─ name: _signature
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _bountyId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  └─ name: uint
      │  │  │     │  ├─ name: _issuerId
      │  │  │     │  ├─ storageLocation
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: Parameter
      │  │  │     │  ├─ typeName
      │  │  │     │  │  ├─ type: ArrayTypeName
      │  │  │     │  │  ├─ baseTypeName
      │  │  │     │  │  │  ├─ type: ElementaryTypeName
      │  │  │     │  │  │  ├─ name: address
      │  │  │     │  │  │  └─ stateMutability: payable
      │  │  │     │  │  └─ length
      │  │  │     │  ├─ name: _approvers
      │  │  │     │  ├─ storageLocation: memory
      │  │  │     │  ├─ isStateVar: false
      │  │  │     │  └─ isIndexed: false
      │  │  │     └─ 4
      │  │  │        ├─ type: Parameter
      │  │  │        ├─ typeName
      │  │  │        │  ├─ type: ElementaryTypeName
      │  │  │        │  └─ name: uint256
      │  │  │        ├─ name: _nonce
      │  │  │        ├─ storageLocation
      │  │  │        ├─ isStateVar: false
      │  │  │        └─ isIndexed: false
      │  │  ├─ returnParameters
      │  │  ├─ body
      │  │  │  ├─ type: Block
      │  │  │  └─ statements
      │  │  │     ├─ 0
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: bytes32
      │  │  │     │  │     ├─ name: metaHash
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: keccak256
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: FunctionCall
      │  │  │     │     │     ├─ expression
      │  │  │     │     │     │  ├─ type: MemberAccess
      │  │  │     │     │     │  ├─ expression
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: abi
      │  │  │     │     │     │  └─ memberName: encodePacked
      │  │  │     │     │     ├─ arguments
      │  │  │     │     │     │  ├─ 0
      │  │  │     │     │     │  │  ├─ type: FunctionCall
      │  │  │     │     │     │  │  ├─ expression
      │  │  │     │     │     │  │  │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │     │  │  │  └─ typeName
      │  │  │     │     │     │  │  │     ├─ type: ElementaryTypeName
      │  │  │     │     │     │  │  │     └─ name: address
      │  │  │     │     │     │  │  ├─ arguments
      │  │  │     │     │     │  │  │  └─ 0
      │  │  │     │     │     │  │  │     ├─ type: Identifier
      │  │  │     │     │     │  │  │     └─ name: this
      │  │  │     │     │     │  │  └─ names
      │  │  │     │     │     │  ├─ 1
      │  │  │     │     │     │  │  ├─ type: StringLiteral
      │  │  │     │     │     │  │  └─ value: metaReplaceApprovers
      │  │  │     │     │     │  ├─ 2
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _bountyId
      │  │  │     │     │     │  ├─ 3
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _issuerId
      │  │  │     │     │     │  ├─ 4
      │  │  │     │     │     │  │  ├─ type: Identifier
      │  │  │     │     │     │  │  └─ name: _approvers
      │  │  │     │     │     │  └─ 5
      │  │  │     │     │     │     ├─ type: Identifier
      │  │  │     │     │     │     └─ name: _nonce
      │  │  │     │     │     └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 1
      │  │  │     │  ├─ type: VariableDeclarationStatement
      │  │  │     │  ├─ variables
      │  │  │     │  │  └─ 0
      │  │  │     │  │     ├─ type: VariableDeclaration
      │  │  │     │  │     ├─ typeName
      │  │  │     │  │     │  ├─ type: ElementaryTypeName
      │  │  │     │  │     │  └─ name: address
      │  │  │     │  │     ├─ name: signer
      │  │  │     │  │     ├─ storageLocation
      │  │  │     │  │     ├─ isStateVar: false
      │  │  │     │  │     └─ isIndexed: false
      │  │  │     │  └─ initialValue
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: getSigner
      │  │  │     │     ├─ arguments
      │  │  │     │     │  ├─ 0
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: metaHash
      │  │  │     │     │  └─ 1
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: _signature
      │  │  │     │     └─ names
      │  │  │     ├─ 2
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: !=
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: signer
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: FunctionCall
      │  │  │     │     │        ├─ expression
      │  │  │     │     │        │  ├─ type: ElementaryTypeNameExpression
      │  │  │     │     │        │  └─ typeName
      │  │  │     │     │        │     ├─ type: ElementaryTypeName
      │  │  │     │     │        │     └─ name: address
      │  │  │     │     │        ├─ arguments
      │  │  │     │     │        │  └─ 0
      │  │  │     │     │        │     ├─ type: NumberLiteral
      │  │  │     │     │        │     ├─ number: 0
      │  │  │     │     │        │     └─ subdenomination
      │  │  │     │     │        └─ names
      │  │  │     │     └─ names
      │  │  │     ├─ 3
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: FunctionCall
      │  │  │     │     ├─ expression
      │  │  │     │     │  ├─ type: Identifier
      │  │  │     │     │  └─ name: require
      │  │  │     │     ├─ arguments
      │  │  │     │     │  └─ 0
      │  │  │     │     │     ├─ type: BinaryOperation
      │  │  │     │     │     ├─ operator: ==
      │  │  │     │     │     ├─ left
      │  │  │     │     │     │  ├─ type: Identifier
      │  │  │     │     │     │  └─ name: _nonce
      │  │  │     │     │     └─ right
      │  │  │     │     │        ├─ type: IndexAccess
      │  │  │     │     │        ├─ base
      │  │  │     │     │        │  ├─ type: Identifier
      │  │  │     │     │        │  └─ name: replayNonce
      │  │  │     │     │        └─ index
      │  │  │     │     │           ├─ type: Identifier
      │  │  │     │     │           └─ name: signer
      │  │  │     │     └─ names
      │  │  │     ├─ 4
      │  │  │     │  ├─ type: ExpressionStatement
      │  │  │     │  └─ expression
      │  │  │     │     ├─ type: UnaryOperation
      │  │  │     │     ├─ operator: ++
      │  │  │     │     ├─ subExpression
      │  │  │     │     │  ├─ type: IndexAccess
      │  │  │     │     │  ├─ base
      │  │  │     │     │  │  ├─ type: Identifier
      │  │  │     │     │  │  └─ name: replayNonce
      │  │  │     │     │  └─ index
      │  │  │     │     │     ├─ type: Identifier
      │  │  │     │     │     └─ name: signer
      │  │  │     │     └─ isPrefix: false
      │  │  │     └─ 5
      │  │  │        ├─ type: ExpressionStatement
      │  │  │        └─ expression
      │  │  │           ├─ type: FunctionCall
      │  │  │           ├─ expression
      │  │  │           │  ├─ type: MemberAccess
      │  │  │           │  ├─ expression
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: bountiesContract
      │  │  │           │  └─ memberName: replaceIssuers
      │  │  │           ├─ arguments
      │  │  │           │  ├─ 0
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: signer
      │  │  │           │  ├─ 1
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _bountyId
      │  │  │           │  ├─ 2
      │  │  │           │  │  ├─ type: Identifier
      │  │  │           │  │  └─ name: _issuerId
      │  │  │           │  └─ 3
      │  │  │           │     ├─ type: Identifier
      │  │  │           │     └─ name: _approvers
      │  │  │           └─ names
      │  │  ├─ visibility: public
      │  │  ├─ modifiers
      │  │  ├─ isConstructor: false
      │  │  └─ stateMutability
      │  └─ 21
      │     ├─ type: FunctionDefinition
      │     ├─ name: getSigner
      │     ├─ parameters
      │     │  ├─ type: ParameterList
      │     │  └─ parameters
      │     │     ├─ 0
      │     │     │  ├─ type: Parameter
      │     │     │  ├─ typeName
      │     │     │  │  ├─ type: ElementaryTypeName
      │     │     │  │  └─ name: bytes32
      │     │     │  ├─ name: _hash
      │     │     │  ├─ storageLocation
      │     │     │  ├─ isStateVar: false
      │     │     │  └─ isIndexed: false
      │     │     └─ 1
      │     │        ├─ type: Parameter
      │     │        ├─ typeName
      │     │        │  ├─ type: ElementaryTypeName
      │     │        │  └─ name: bytes
      │     │        ├─ name: _signature
      │     │        ├─ storageLocation: memory
      │     │        ├─ isStateVar: false
      │     │        └─ isIndexed: false
      │     ├─ returnParameters
      │     │  ├─ type: ParameterList
      │     │  └─ parameters
      │     │     └─ 0
      │     │        ├─ type: Parameter
      │     │        ├─ typeName
      │     │        │  ├─ type: ElementaryTypeName
      │     │        │  └─ name: address
      │     │        ├─ name
      │     │        ├─ storageLocation
      │     │        ├─ isStateVar: false
      │     │        └─ isIndexed: false
      │     ├─ body
      │     │  ├─ type: Block
      │     │  └─ statements
      │     │     ├─ 0
      │     │     │  ├─ type: VariableDeclarationStatement
      │     │     │  ├─ variables
      │     │     │  │  └─ 0
      │     │     │  │     ├─ type: VariableDeclaration
      │     │     │  │     ├─ typeName
      │     │     │  │     │  ├─ type: ElementaryTypeName
      │     │     │  │     │  └─ name: bytes32
      │     │     │  │     ├─ name: r
      │     │     │  │     ├─ storageLocation
      │     │     │  │     ├─ isStateVar: false
      │     │     │  │     └─ isIndexed: false
      │     │     │  └─ initialValue
      │     │     ├─ 1
      │     │     │  ├─ type: VariableDeclarationStatement
      │     │     │  ├─ variables
      │     │     │  │  └─ 0
      │     │     │  │     ├─ type: VariableDeclaration
      │     │     │  │     ├─ typeName
      │     │     │  │     │  ├─ type: ElementaryTypeName
      │     │     │  │     │  └─ name: bytes32
      │     │     │  │     ├─ name: s
      │     │     │  │     ├─ storageLocation
      │     │     │  │     ├─ isStateVar: false
      │     │     │  │     └─ isIndexed: false
      │     │     │  └─ initialValue
      │     │     ├─ 2
      │     │     │  ├─ type: VariableDeclarationStatement
      │     │     │  ├─ variables
      │     │     │  │  └─ 0
      │     │     │  │     ├─ type: VariableDeclaration
      │     │     │  │     ├─ typeName
      │     │     │  │     │  ├─ type: ElementaryTypeName
      │     │     │  │     │  └─ name: uint8
      │     │     │  │     ├─ name: v
      │     │     │  │     ├─ storageLocation
      │     │     │  │     ├─ isStateVar: false
      │     │     │  │     └─ isIndexed: false
      │     │     │  └─ initialValue
      │     │     ├─ 3
      │     │     │  ├─ type: IfStatement
      │     │     │  ├─ condition
      │     │     │  │  ├─ type: BinaryOperation
      │     │     │  │  ├─ operator: !=
      │     │     │  │  ├─ left
      │     │     │  │  │  ├─ type: MemberAccess
      │     │     │  │  │  ├─ expression
      │     │     │  │  │  │  ├─ type: Identifier
      │     │     │  │  │  │  └─ name: _signature
      │     │     │  │  │  └─ memberName: length
      │     │     │  │  └─ right
      │     │     │  │     ├─ type: NumberLiteral
      │     │     │  │     ├─ number: 65
      │     │     │  │     └─ subdenomination
      │     │     │  ├─ trueBody
      │     │     │  │  ├─ type: Block
      │     │     │  │  └─ statements
      │     │     │  │     └─ 0
      │     │     │  │        ├─ type: ReturnStatement
      │     │     │  │        └─ expression
      │     │     │  │           ├─ type: FunctionCall
      │     │     │  │           ├─ expression
      │     │     │  │           │  ├─ type: ElementaryTypeNameExpression
      │     │     │  │           │  └─ typeName
      │     │     │  │           │     ├─ type: ElementaryTypeName
      │     │     │  │           │     └─ name: address
      │     │     │  │           ├─ arguments
      │     │     │  │           │  └─ 0
      │     │     │  │           │     ├─ type: NumberLiteral
      │     │     │  │           │     ├─ number: 0
      │     │     │  │           │     └─ subdenomination
      │     │     │  │           └─ names
      │     │     │  └─ falseBody
      │     │     ├─ 4
      │     │     │  ├─ type: InlineAssemblyStatement
      │     │     │  ├─ language
      │     │     │  └─ body
      │     │     │     ├─ type: AssemblyBlock
      │     │     │     └─ operations
      │     │     │        ├─ 0
      │     │     │        │  ├─ type: AssemblyAssignment
      │     │     │        │  ├─ names
      │     │     │        │  │  └─ 0
      │     │     │        │  │     ├─ type: Identifier
      │     │     │        │  │     └─ name: r
      │     │     │        │  └─ expression
      │     │     │        │     ├─ type: AssemblyCall
      │     │     │        │     ├─ functionName: mload
      │     │     │        │     └─ arguments
      │     │     │        │        └─ 0
      │     │     │        │           ├─ type: AssemblyCall
      │     │     │        │           ├─ functionName: add
      │     │     │        │           └─ arguments
      │     │     │        │              ├─ 0
      │     │     │        │              │  ├─ type: AssemblyCall
      │     │     │        │              │  ├─ functionName: _signature
      │     │     │        │              │  └─ arguments
      │     │     │        │              └─ 1
      │     │     │        │                 ├─ type: DecimalNumber
      │     │     │        │                 └─ value: 32
      │     │     │        ├─ 1
      │     │     │        │  ├─ type: AssemblyAssignment
      │     │     │        │  ├─ names
      │     │     │        │  │  └─ 0
      │     │     │        │  │     ├─ type: Identifier
      │     │     │        │  │     └─ name: s
      │     │     │        │  └─ expression
      │     │     │        │     ├─ type: AssemblyCall
      │     │     │        │     ├─ functionName: mload
      │     │     │        │     └─ arguments
      │     │     │        │        └─ 0
      │     │     │        │           ├─ type: AssemblyCall
      │     │     │        │           ├─ functionName: add
      │     │     │        │           └─ arguments
      │     │     │        │              ├─ 0
      │     │     │        │              │  ├─ type: AssemblyCall
      │     │     │        │              │  ├─ functionName: _signature
      │     │     │        │              │  └─ arguments
      │     │     │        │              └─ 1
      │     │     │        │                 ├─ type: DecimalNumber
      │     │     │        │                 └─ value: 64
      │     │     │        └─ 2
      │     │     │           ├─ type: AssemblyAssignment
      │     │     │           ├─ names
      │     │     │           │  └─ 0
      │     │     │           │     ├─ type: Identifier
      │     │     │           │     └─ name: v
      │     │     │           └─ expression
      │     │     │              ├─ type: AssemblyCall
      │     │     │              ├─ functionName: byte
      │     │     │              └─ arguments
      │     │     │                 ├─ 0
      │     │     │                 │  ├─ type: DecimalNumber
      │     │     │                 │  └─ value: 0
      │     │     │                 └─ 1
      │     │     │                    ├─ type: AssemblyCall
      │     │     │                    ├─ functionName: mload
      │     │     │                    └─ arguments
      │     │     │                       └─ 0
      │     │     │                          ├─ type: AssemblyCall
      │     │     │                          ├─ functionName: add
      │     │     │                          └─ arguments
      │     │     │                             ├─ 0
      │     │     │                             │  ├─ type: AssemblyCall
      │     │     │                             │  ├─ functionName: _signature
      │     │     │                             │  └─ arguments
      │     │     │                             └─ 1
      │     │     │                                ├─ type: DecimalNumber
      │     │     │                                └─ value: 96
      │     │     ├─ 5
      │     │     │  ├─ type: IfStatement
      │     │     │  ├─ condition
      │     │     │  │  ├─ type: BinaryOperation
      │     │     │  │  ├─ operator: <
      │     │     │  │  ├─ left
      │     │     │  │  │  ├─ type: Identifier
      │     │     │  │  │  └─ name: v
      │     │     │  │  └─ right
      │     │     │  │     ├─ type: NumberLiteral
      │     │     │  │     ├─ number: 27
      │     │     │  │     └─ subdenomination
      │     │     │  ├─ trueBody
      │     │     │  │  ├─ type: Block
      │     │     │  │  └─ statements
      │     │     │  │     └─ 0
      │     │     │  │        ├─ type: ExpressionStatement
      │     │     │  │        └─ expression
      │     │     │  │           ├─ type: BinaryOperation
      │     │     │  │           ├─ operator: +=
      │     │     │  │           ├─ left
      │     │     │  │           │  ├─ type: Identifier
      │     │     │  │           │  └─ name: v
      │     │     │  │           └─ right
      │     │     │  │              ├─ type: NumberLiteral
      │     │     │  │              ├─ number: 27
      │     │     │  │              └─ subdenomination
      │     │     │  └─ falseBody
      │     │     └─ 6
      │     │        ├─ type: IfStatement
      │     │        ├─ condition
      │     │        │  ├─ type: BinaryOperation
      │     │        │  ├─ operator: &&
      │     │        │  ├─ left
      │     │        │  │  ├─ type: BinaryOperation
      │     │        │  │  ├─ operator: !=
      │     │        │  │  ├─ left
      │     │        │  │  │  ├─ type: Identifier
      │     │        │  │  │  └─ name: v
      │     │        │  │  └─ right
      │     │        │  │     ├─ type: NumberLiteral
      │     │        │  │     ├─ number: 27
      │     │        │  │     └─ subdenomination
      │     │        │  └─ right
      │     │        │     ├─ type: BinaryOperation
      │     │        │     ├─ operator: !=
      │     │        │     ├─ left
      │     │        │     │  ├─ type: Identifier
      │     │        │     │  └─ name: v
      │     │        │     └─ right
      │     │        │        ├─ type: NumberLiteral
      │     │        │        ├─ number: 28
      │     │        │        └─ subdenomination
      │     │        ├─ trueBody
      │     │        │  ├─ type: Block
      │     │        │  └─ statements
      │     │        │     └─ 0
      │     │        │        ├─ type: ReturnStatement
      │     │        │        └─ expression
      │     │        │           ├─ type: FunctionCall
      │     │        │           ├─ expression
      │     │        │           │  ├─ type: ElementaryTypeNameExpression
      │     │        │           │  └─ typeName
      │     │        │           │     ├─ type: ElementaryTypeName
      │     │        │           │     └─ name: address
      │     │        │           ├─ arguments
      │     │        │           │  └─ 0
      │     │        │           │     ├─ type: NumberLiteral
      │     │        │           │     ├─ number: 0
      │     │        │           │     └─ subdenomination
      │     │        │           └─ names
      │     │        └─ falseBody
      │     │           ├─ type: Block
      │     │           └─ statements
      │     │              └─ 0
      │     │                 ├─ type: ReturnStatement
      │     │                 └─ expression
      │     │                    ├─ type: FunctionCall
      │     │                    ├─ expression
      │     │                    │  ├─ type: Identifier
      │     │                    │  └─ name: ecrecover
      │     │                    ├─ arguments
      │     │                    │  ├─ 0
      │     │                    │  │  ├─ type: FunctionCall
      │     │                    │  │  ├─ expression
      │     │                    │  │  │  ├─ type: Identifier
      │     │                    │  │  │  └─ name: keccak256
      │     │                    │  │  ├─ arguments
      │     │                    │  │  │  └─ 0
      │     │                    │  │  │     ├─ type: FunctionCall
      │     │                    │  │  │     ├─ expression
      │     │                    │  │  │     │  ├─ type: MemberAccess
      │     │                    │  │  │     │  ├─ expression
      │     │                    │  │  │     │  │  ├─ type: Identifier
      │     │                    │  │  │     │  │  └─ name: abi
      │     │                    │  │  │     │  └─ memberName: encodePacked
      │     │                    │  │  │     ├─ arguments
      │     │                    │  │  │     │  ├─ 0
      │     │                    │  │  │     │  │  ├─ type: StringLiteral
      │     │                    │  │  │     │  │  └─ value: \x19Ethereum Signed Message:\n32
      │     │                    │  │  │     │  └─ 1
      │     │                    │  │  │     │     ├─ type: Identifier
      │     │                    │  │  │     │     └─ name: _hash
      │     │                    │  │  │     └─ names
      │     │                    │  │  └─ names
      │     │                    │  ├─ 1
      │     │                    │  │  ├─ type: Identifier
      │     │                    │  │  └─ name: v
      │     │                    │  ├─ 2
      │     │                    │  │  ├─ type: Identifier
      │     │                    │  │  └─ name: r
      │     │                    │  └─ 3
      │     │                    │     ├─ type: Identifier
      │     │                    │     └─ name: s
      │     │                    └─ names
      │     ├─ visibility: internal
      │     ├─ modifiers
      │     ├─ isConstructor: false
      │     └─ stateMutability: pure
      └─ kind: contract

```

