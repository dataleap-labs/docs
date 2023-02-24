# API Documentation

If you have any feedback please write us directly on Telegram @jh_damm and @jan_rue. Thank you!

## Entities
- Protocol
- Project
- Contract
- Audit & Auditor
- Bounty & Bounty Platform
- InsurancePolicy & Insurace Platform

## Available endpoints

### Contracts
```bash
# /contracts/{address}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/contracts'

# /contracts/project/{projectId}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/contracts/project/xxx'

# /contracts/protocol/{protocolId}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/contracts/protocol/xxx'
```

### Projects & Protocols
```bash
# /projects
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/projects'

# /projects/{id}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/projects/xxx'

# /protocols
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/protocols'

# /protocols/{id}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/protocols/xxx'
```

### Audits & Auditors

```bash
# /auditors
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/auditors'

# /auditors/{id}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/auditors/xxx'

# /audits/{id}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/audits/xxx'
```

### Bounties & Bounty Platforms
```bash
# /bountyPlatforms
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/bountyPlatforms'

# /bountyPlatforms/{id}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/bountyPlatforms/xxx'

# /bounties/{id}
curl --location --request GET 'https://api.staging.dataleap.xyz/v1/bounties/xxx'
```

### Insurance Policies & Insurance Platforms
Coming soon - stay tuned!



