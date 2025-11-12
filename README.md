# Pi-hole Personal Lists

This repository contains custom allow and block lists for [Pi-hole](https://pi-hole.net/), a network-level ad blocker and privacy tool.

## Files

### `global-allow.txt`
A whitelist of domains that should always be allowed, even if they appear on block lists. This is useful for:
- Domains that are incorrectly blocked by public block lists
- Essential services that need to function properly
- Trusted domains that you want to ensure are never blocked

### `global-block.txt`
A blacklist of domains that should always be blocked. This is useful for:
- Additional domains you want to block beyond public block lists
- Known malicious, advertising, or tracking domains
- Specific domains you want to prevent access to on your network

## Usage

To use these lists in Pi-hole:

1. Navigate to your Pi-hole admin interface
2. Go to **Group Management** → **Adlists** (for block lists) or **Whitelist** (for allow lists)
3. Add the raw GitHub URLs for the lists you want to use:
   - Block list: `https://raw.githubusercontent.com/thiagosgarcia/lists/main/global-block.txt`
   - Allow list: `https://raw.githubusercontent.com/thiagosgarcia/lists/main/global-allow.txt`
4. Update Gravity to apply the changes

## Format

Each file should contain one domain per line, for example:
```
example.com
ads.example.net
tracker.example.org
```

## License

This project is released into the public domain under The Unlicense. See [LICENSE](LICENSE) for details.
