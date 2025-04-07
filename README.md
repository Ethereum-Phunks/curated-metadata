# Curated Collections Metadata

This repository contains metadata for collections curated on the Ethereum Phunks marketplace. It serves as a public resource for builders and tinkerers who want to work with the metadata of collections featured on our platform.

## Purpose

The repository aims to:
- Provide easy access to metadata for all collections curated on Ethereum Phunks
- Enable developers to build tools and applications using this metadata
- Maintain a standardized format for collection metadata

## Usage

### TypeScript Support

The repository includes TypeScript type definitions for the metadata structure. You can import these types in your project:

```typescript
import { Metadata, CollectionMetadata, CollectionItem, Attribute } from './types';
```

### Example Usage

```typescript
import { Metadata } from './types';

// Load metadata for a specific collection
const dystoPhunksMetadata: CollectionMetadata = require('./metadata/dysto-phunks.json');

// Access collection information
console.log(dystoPhunksMetadata.name);
console.log(dystoPhunksMetadata.description);

// Access individual items
const firstItem = dystoPhunksMetadata.collection_items[0];
console.log(firstItem.name);
console.log(firstItem.attributes);
```

## Metadata Structure

Each collection metadata file follows this structure:

```typescript
interface CollectionMetadata {
  name: string;
  logo_image: string | null;
  banner_image: string | null;
  total_supply: number;
  slug: string;
  description: string;
  website_url: string | null;
  twitter_url: string | null;
  discord_url: string | null;
  background_color: string | null;
  collection_items: CollectionItem[];
}
```

## License

This metadata is released into the public domain under The Unlicense.

Note: While this metadata is released into the public domain, the original collections may have their own licenses. Please refer to the respective collection's terms and conditions for information about the underlying assets.

## Support

For questions or support, please:
- Open an issue in this repository
- Follow us on [Twitter](https://twitter.com/etherphunks)