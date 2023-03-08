# API Documentation

If you have any feedback please write us directly on Telegram @jh_damm and @jan_rue or book at slot in our [calendar](https://cal.com/jan/30-min-chat) for 30 min meeting. Thank you!

⚠️ The API is under **active development**. Breaking changes can occur at anytime.

## Entities
The API covers the following entities:

- Protocol: e.g. Aave
- Project: e.g. Aave V2
- Contract: e.g. Aave V2 LendingPool contract
- Audit & Auditor: audits are provided on a project level
- Bounty & Bounty Platform: bounties are also provided on a project level
- InsurancePolicy & Insurace Platform: insurace policies are also provided on a project level

## Available endpoints
We recommend to try out the different endpoints yourself to get to know their behaviour and return values. An OpenAPI documentation which explains the endpoints and return types in more detail will be available shortly. If a contract is not covered yet in our dataset, you will get a `500` error.


### Addresses

The `addresses` endpoint currenntly supports 241634 contracts, token and dex wallets which correspond to ~60% of all transactions/events/traces on Ethereum mainnet.

```bash
# /addresses/{address}
curl --request GET 'https://api.staging.dataleap.xyz/v1/addresses/0xf42aa99f011a1fa7cda90e5e98b277e306bca83e'
```

Response
```json
{
  "address":"0xf42aa99f011a1fa7cda90e5e98b277e306bca83e",
  "category":"contract", # can be: contract, token or wallet
  "label":"looksrare: Transfer Manager ERC 721",
  "tokenInfo":
  {
    "contractName":"",
    "type":"" # can be: erc20, erc721, erc1155 or unknown
  },
  "contractInfo":
  {
    "contractName":"Transfer Manager ERC 721",
    "protocol":"looksrare"
  }
}
```

### Contracts

```bash
# /contracts/{address}
curl --request GET 'https://api.staging.dataleap.xyz/v1/contracts/0x7d2768de32b0b80b7a3454c06bdac94a69ddc7a9'

# /contracts/project/{projectId}
curl --request GET 'https://api.staging.dataleap.xyz/v1/contracts/project/ac8c0b55-0ad5-4dbe-b584-ee5f99d67a50'

# /contracts/protocol/{protocolId}
curl --request GET 'https://api.staging.dataleap.xyz/v1/contracts/protocol/dc1d69e2-6361-468f-a5fd-b61c7877ad98'
```

### Projects & Protocols
```bash
# /projects
curl --request GET 'https://api.staging.dataleap.xyz/v1/projects'

# /projects/{id}
curl --request GET 'https://api.staging.dataleap.xyz/v1/projects/ac8c0b55-0ad5-4dbe-b584-ee5f99d67a50'

# /protocols
curl --request GET 'https://api.staging.dataleap.xyz/v1/protocols'

# /protocols/{id}
curl --request GET 'https://api.staging.dataleap.xyz/v1/protocols/dc1d69e2-6361-468f-a5fd-b61c7877ad98'
```

### Audits & Auditors

```bash
# /auditors
curl --request GET 'https://api.staging.dataleap.xyz/v1/auditors'

# /auditors/{id}
curl --request GET 'https://api.staging.dataleap.xyz/v1/auditors/8ec6383f-8352-4e57-93ab-b55f0b3419f9'

# /audits/{id}
curl --request GET 'https://api.staging.dataleap.xyz/v1/audits/9263c2d0-152b-4bdf-acdb-97762f18731d'
```

### Bounties & Bounty Platforms
```bash
# /bountyPlatforms
curl --request GET 'https://api.staging.dataleap.xyz/v1/bountyPlatforms'

# /bountyPlatforms/{id}
curl --request GET 'https://api.staging.dataleap.xyz/v1/bountyPlatforms/de6373fd-ff90-44f7-ab02-dacb52e4214f'

# /bounties/{id}
curl --request GET 'https://api.staging.dataleap.xyz/v1/bounties/c1d685fc-94b8-4b0d-bbae-70b404f8ee35'
```

### Insurance Policies & Insurance Platforms
Coming soon - stay tuned!



