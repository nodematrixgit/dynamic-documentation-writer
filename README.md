# NodeMatrix Dynamic Documentation Writer

GitBook-style documentation templates for NodeMatrix Documentation Generator node. These templates define the section structure and content for different token types.

**Note:** This repository is used with the Documentation Generator node in NodeMatrix. When you use the Documentation Generator node in your workflow, it references these templates to generate comprehensive documentation sections for your token projects.

## What is This?

This repository contains GitBook-style documentation templates organized by token type. Each template defines:

- Section structure (overview, tokenomics, utility, etc.)
- Section order and organization
- Default content and descriptions
- Section types (custom, api_docs, use_cases, social_proof, bento)

## Available Templates

### Utility Token Template
Sections: Overview, Tokenomics, Token Utility, API Documentation, Use Cases, Roadmap, Team

### Game Token Template
Sections: Game Overview, Gameplay, NFTs, Rewards, Tokenomics, Roadmap

### DeFi Token Template
Sections: DeFi Protocol, Features, Yield Farming, Tokenomics

### NFT Token Template
Sections: NFT Collection, Collection Details, NFT Utility, Roadmap

### Meme Token Template
Sections: Overview, Tokenomics, Community

### Custom Template
Sections: Overview, Tokenomics, Utility, Roadmap

## Template Structure

Each template is defined in `templates.json` with the following structure:

```json
{
  "token-type": [
    {
      "section_key": "section-name",
      "section_type": "custom|api_docs|use_cases|social_proof|bento",
      "enabled": true,
      "order_index": 0,
      "defaultContent": {
        "title": "Section Title",
        "description": "Section description"
      },
      "defaultConfig": {}
    }
  ]
}
```

## Section Types

- **custom**: Standard markdown content section
- **api_docs**: API documentation with code examples
- **use_cases**: Use case showcase section
- **social_proof**: Community and social links section
- **bento**: Feature grid/bento box layout section

## How It Works

1. Documentation Generator node reads `templates.json`
2. Selects template based on token type (utility-token, game-token, etc.)
3. Creates documentation sections based on template structure
4. Populates sections with token information from RunConfig
5. Generates GitBook-style documentation

## Usage

The Documentation Generator node automatically uses these templates when generating documentation. You can:

- Select a template in the Token Info node (template field)
- Customize sections after generation
- Add or remove sections as needed
- Modify section content and order

## Customization

After documentation is generated, you can:

- Edit section content
- Reorder sections
- Enable/disable sections
- Add custom sections
- Modify section configurations

## File Structure

```
dynamic-documentation-writer/
├── README.md          # This file
├── templates.json     # Template definitions
└── .gitignore         # Git ignore file
```

## Support

For questions about NodeMatrix:

- Visit nodematrix.one/docs for documentation
- Check api.nodematrix.one for API reference
- Open an issue on GitHub

## License

MIT License - use these templates freely for your projects.
