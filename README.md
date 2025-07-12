[![axone github banner](https://raw.githubusercontent.com/axone-protocol/.github/main/profile/static/axone-banner.png)](https://axone.xyz)

# Awesome AXONE

> Awesome AXONE is a curated list of awesome resources, documents, and tools for [AXONE](https://axone.xyz).

[![awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://axone.xyz/awesome)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](https://makeapullrequest.com)
[![lint](https://img.shields.io/github/actions/workflow/status/axone-protocol/awesome/lint.yml?label=Lint&style=for-the-badge&logo=github)](https://github.com/axone-protocol/awesome/actions/workflows/lint.yml)
[![conventional commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg?style=for-the-badge&logo=conventionalcommits)](https://conventionalcommits.org)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?style=for-the-badge)](https://github.com/semantic-release/semantic-release)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg?style=for-the-badge)](https://github.com/axone-protocol/.github/blob/main/CODE_OF_CONDUCT.md)
[![license](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg?style=for-the-badge)](https://opensource.org/licenses/BSD-3-Clause)

## 💫 Official AXONE links

- <img
  src="assets/linktree.webp" alt="Linkedtree icon" style="width:15px;height:15px;"> [Linktree](https://linktr.ee/axonexyz)
- <img
  src="assets/website.webp" alt="Website icon" style="width:15px;height:15px;"> [Website](https://axone.xyz/)
- <img
  src="assets/linkedin.webp" alt="LinkedIn icon" style="width:15px;height:15px;"> [LinkedIn](https://www.linkedin.com/company/axone-protocol)
- <img
  src="assets/twitter.webp" alt="Twitter icon" style="width:15px;height:15px;"> [Twitter](https://x.com/axonexyz)
- <img
  src="assets/github.webp" alt="GitHub icon" style="width:15px;height:15px;"> [GitHub](https://github.com/axone-protocol)
- <img
  src="assets/telegram.webp" alt="Telegram icon" style="width:15px;height:15px;"> [Telegram](https://t.me/axonexyz)
- <img
  src="assets/medium.webp" alt="Medium icon" style="width:15px;height:15px;"> [Medium](https://blog.axone.xyz/)
- <img
  src="assets/discord.webp" alt="Discord icon" style="width:15px;height:15px;"> [Discord](https://discord.com/invite/axone)

## 🌐 Networks

| Network            | Type        | Description                                | Link                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------ | ----------- | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `axone-1`          | **mainnet** | Live Axone network                         | [![axone mainnet](https://img.shields.io/badge/dynamic/json?style=for-the-badge&labelColor=steelblue&color=lightcyan&label=🟢%20axone%20mainnet&query=%24.block.header.height&url=https%3A%2F%2Faxone-api.highstakes.ch%2Fcosmos%2Fbase%2Ftendermint%2Fv1beta1%2Fblocks%2Flatest&cacheSeconds=300)](https://github.com/axone-protocol/networks/blob/main/chains/1/README.md)                           |
| `axone-dentrite-1` | **testnet** | Playground for testing and experimentation | [![axone-dentrite testnet](https://img.shields.io/badge/dynamic/json?style=for-the-badge&labelColor=teal&color=lightcyan&label=🟢%20axone-dentrite%20testnet&query=%24.block.header.height&url=https%3A%2F%2Faxone-api.jayjayinfra.space%2Fcosmos%2Fbase%2Ftendermint%2Fv1beta1%2Fblocks%2Flatest&cacheSeconds=300)](https://github.com/axone-protocol/networks/blob/main/chains/dentrite-1/README.md) |

## 📚 Documentation / Guides

| Type       | URL                                          | Status | Thanks To                  |
| ---------- | -------------------------------------------- | ------ | -------------------------- |
| Whitepaper | <https://docs.axone.xyz/whitepaper/abstract> | ✅     | [AXONE](https://axone.xyz) |

## 🔭 Block Explorers

| Thanks To | Explorer | URL | Status |
| --------- | -------- | --- | ------ |
  catsmile  | Ping.hub | explorer.catsmile.cloud | LIVE     |
## ⚙️ Services

> RPC

| Thanks To | URL | Status |
| :-------: | :-: | :----: |
| catsmile  | https://rpc-axone.catsmile.space | LIVE     |

> API

| Thanks To | URL | Status |
| :-------: | :-: | :----: |
| catsmile  | https://api-axone.catsmile.space | LIVE     |

> gRPC

| Thanks To | URL |
| --------- | --- |
| catsmile  | https://grpc-axone.catsmile.space | LIVE     |
> Addrbook

| Thanks To | URL | Status |
| --------- | --- | ------ |
| catsmile  | https://files-axone.catsmile.space/addrbook.json | LIVE     |
> Snapshot

| Thanks To | URL | Status |
| --------- | --- | ------ |
| catsmile  | https://files-axone.catsmile.space/snapshot_latest.tar.lz4 | LIVE     |

> State / Quick Sync

| Thanks To | URL | Status |
| --------- | --- | ------ |
| catsmile  | https://rpc-axone.catsmile.space | LIVE     |
# State Sync Config (Axone via catsmile)

STATE_SYNC_RPC=https://rpc-axone.catsmile.space
LATEST_HEIGHT=55797
TRUST_HASH=8C46A11303E10BC31FEF47F90B2DF3EC3E8184D96EB09523E63BA61819350290

sed -i.bak -e "s|^enable *=.*|enable = true|" \
  -e "s|^rpc_servers *=.*|rpc_servers = \"$STATE_SYNC_RPC,$STATE_SYNC_RPC\"|" \
  -e "s|^trust_height *=.*|trust_height = $LATEST_HEIGHT|" \
  -e "s|^trust_hash *=.*|trust_hash = \"$TRUST_HASH\"|" \
  -e "s|^seeds *=.*|seeds = \"\"|" \
  -e "s|^persistent_peers *=.*|persistent_peers = \"\"|" \
  ~/.axoned/config/config.toml

> Live Peer

| Thanks To | Live Peer |
| --------- | --------- |
| catsmile   | http://peer-axone.catsmile.space/peers.json | LIVE     |
## 📊 Dashboards

| Thanks To                  | Type                                | URL                         | Status |
| -------------------------- | ----------------------------------- | --------------------------- | ------ |
| catsmile                   | Tool Monitoring Validator Realtime on Web | https://monitor-pro.catsmile.clou | LIVE     |

## 🖥️ Applications

|            Thanks To            |             URL             |                                      Repository                                       | Description                                                        | Status |
| :-----------------------------: | :-------------------------: | :-----------------------------------------------------------------------------------: | ------------------------------------------------------------------ | :----: |
| [Keplr](https://www.keplr.app/) | <https://chains.keplr.app/> | [chainapsis/keplr-chain-registry](https://github.com/chainapsis/keplr-chain-registry) | Chain registry for integrating non-native chains into Keplr wallet |   ✅   |

## 🤖 BOTs

| Thanks To | Type | URL | Description |
| --------- | ---- | --- | ----------- |

## You want to get involved? 😍

Please submit a pull request if you know any resources that might be helpful to the community. ❤️

Don't forget to check out AXONE health files:

- [Contributing](https://github.com/axone-protocol/.github/blob/main/CONTRIBUTING.md)
- [Code of conduct](https://github.com/axone-protocol/.github/blob/main/CODE_OF_CONDUCT.md)
