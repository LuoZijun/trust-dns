# Change Log: TRust-DNS Resolver

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## 0.5.0

### Added

- Generic record type lookup

### Changed

- refactored lru cache and resolver to better cache other record types

## 0.4.0

### Removed

- *breaking* impl `Iterator` removed from `LookupIp` result type, see `LookupIp::iter` for replacement

### Added

- Support for DNSSec validation
- LRU Cache

## 0.3.0

### Added

- `options attempts:N` aka `ResolverOpts::attempts` support, aka retries
- Google IPv6 nameservers as defaults for `ResolverConfig::default`
- support for domain name search in `ResolverConfig` and `LookupIpFuture`
- support for search names in `ResolverConfig` and `LookupIpFuture`
- `LookupIpFuture` type alias to `InnerLookupIpFuture<NameServerPool>` *compatibility*

### Changed

- *breaking* `LookupIpFuture` renamed to `InnerLookupIpFuture`
- *breaking* `InnerLookupIpFuture` now takes a generic parameter, generally `<NameServerPool>`

## 0.2.0

### Added

- ipv6 parallel lookup
- multiple ipv4 and ipv6 lookup strategies
- library documentation examples
- test coverage for resolver

## 0.1.0

### Added

- Initial release of the TRust-DNS Resolver